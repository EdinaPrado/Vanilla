# Estágio 1: Compilação (Build)
FROM node:20-alpine AS build

# Define o diretório de trabalho dentro do container
WORKDIR /app

# Copia apenas os arquivos de definição de dependências
COPY package*.json ./

# Instala as dependências de forma limpa
RUN npm ci

# Copia todo o restante dos arquivos do projeto
COPY . .

# Executa o comando de build do Vite (gera a pasta dist)
RUN npm run build

# Estágio 2: Produção (Servidor Nginx)
FROM nginx:alpine

# Copia os arquivos compilados do estágio anterior para a pasta pública do Nginx
COPY --from=build /app/dist /usr/share/nginx/html

# Expõe a porta padrão do Nginx
EXPOSE 80


