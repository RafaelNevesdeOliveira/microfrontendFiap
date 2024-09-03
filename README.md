# MicrofrontendFiap

Este projeto foi gerado com [Angular CLI](https://github.com/angular/angular-cli) versão 17.3.8.

## Índice
- [Pré-requisitos](#pré-requisitos)
- [Instalação](#instalação)
- [Serviço de Desenvolvimento](#serviço-de-desenvolvimento)
- [Estrutura do Projeto](#estrutura-do-projeto)
- [Comandos Disponíveis](#comandos-disponíveis)
- [Build](#build)
- [Testes](#testes)
- [Configurações Personalizadas](#configurações-personalizadas)
- [Ajuda Adicional](#ajuda-adicional)

## Pré-requisitos
- Node.js versão 18 ou superior
- Angular CLI
- NPM ou Yarn

## Instalação

Clone o repositório e instale as dependências:
```bash
git clone <URL-do-repositorio>
cd MicrofrontendFiap
npm install
````

## Start Projeto
```bash
 npm run build:host-app - # Rodar projeto Host
 npm run build:microfront-app - # Rodar projeto microfront
```

## Estrutura do Projeto

- **projects/microfront-app**: Aplicação microfrontend.
- **projects/host-app**: Aplicação host para integração do microfrontend.
- **dist**: Diretório de saída dos builds.
- **src**: Código-fonte principal.

## Comandos Disponíveis

- **Gerar Componente**: `ng generate component component-name`
- **Gerar Serviço**: `ng generate service service-name`
- **Build**: `ng build`
- **Testes Unitários**: `ng test`
- **Testes End-to-End**: `ng e2e`
