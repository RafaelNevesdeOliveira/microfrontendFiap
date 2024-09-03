# Stage 1: Build the Angular application
FROM node:18 as build

# Defina o diretório de trabalho dentro do contêiner
WORKDIR /usr/local/app

# Copie apenas os arquivos necessários do projeto Angular para o contêiner
COPY ./projects/host-app/package*.json ./

# Instale o npm na versão desejada
RUN npm install -g npm@8.12.1

# Instale as dependências do projeto
RUN npm install

# Copie o restante do código do projeto para o diretório de trabalho do contêiner
COPY ./projects/host-app/ .

# Construa o projeto Angular
RUN npm run build -- --output-path=dist/host-app

# Stage 2: Configure Nginx to serve the application
FROM nginx:latest

# Remova a configuração padrão do Nginx e adicione a sua configuração personalizada
COPY ./nginx/nginx.conf /etc/nginx/conf.d/default.conf

# Copie o build da aplicação Angular para o diretório servido pelo Nginx
COPY --from=build /usr/local/app/dist/host-app /usr/share/nginx/html

# Exponha a porta 80 para o Nginx
EXPOSE 80

# Comando para iniciar o Nginx
CMD ["nginx", "-g", "daemon off;"]
