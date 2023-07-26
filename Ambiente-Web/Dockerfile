# Define a imagem base
FROM ubuntu:latest

# Define as variáveis de ambiente
ENV DEBIAN_FRONTEND=noninteractive

# Atualiza o sistema e instala as dependências necessárias
RUN apt-get update && apt-get install -y \
    curl \
    wget \
    gnupg \
    git \
    php \
    nodejs \
    npm \
    && rm -rf /var/lib/apt/lists/*

# Instala o VSCode Server
RUN curl -fsSL https://code-server.dev/install.sh | sh

# Define o diretório de trabalho
WORKDIR /app

# Expõe a porta 4000 para acesso à aplicação web
EXPOSE 4000

# Inicia o VSCode Server
CMD [ "code-server", "--bind-addr", "0.0.0.0:4000" ]
