# Vanilla

Aplicação front-end criada com **Vite** e **JavaScript puro** (sem framework), empacotada em um container **Docker**.

O projeto serve como base para estudar o fluxo completo de uma aplicação web: desenvolvimento local, build de produção e execução em container.

## Tecnologias

- [Vite](https://vitejs.dev/): servidor de desenvolvimento e build
- JavaScript, HTML e CSS
- Docker

## Pré-requisitos

- [Node.js](https://nodejs.org/) 18 ou superior e npm
- [Docker](https://www.docker.com/) (opcional, só para rodar em container)

## Como rodar localmente

```bash
git clone https://github.com/EdinaPrado/Vanilla.git
cd Vanilla/app-vite
npm install
npm run dev
```

O Vite mostra no terminal o endereço da aplicação (normalmente `http://localhost:5173`).

## Build de produção

```bash
npm run build
npm run preview
```

Os arquivos otimizados são gerados na pasta `dist/`.

## Como rodar com Docker

```bash
cd app-vite
docker build -t vanilla .
docker run -p 8080:80 vanilla
```

<!-- Confirmar no Dockerfile qual porta o container expõe e ajustar o -p acima -->

Depois, acesse `http://localhost:8080`.

## Estrutura do projeto

```
Vanilla/
└── app-vite/
    ├── public/          # arquivos estáticos
    ├── src/             # código-fonte da aplicação
    ├── index.html       # página principal
    ├── Dockerfile       # imagem Docker da aplicação
    ├── package.json     # dependências e scripts
    └── package-lock.json
```

## Autora

**Edina do Prado**: [github.com/EdinaPrado](https://github.com/EdinaPrado)
