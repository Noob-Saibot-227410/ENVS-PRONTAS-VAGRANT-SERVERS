# Define a imagem base
FROM ubuntu:latest

# Instalação das dependências do IntelliJ IDEA, do wget e do OpenJDK
RUN apt-get update && apt-get install -y \
    libxrender1 \
    libxtst6 \
    libxi6 \
    libfreetype6 \
    wget \
    openjdk-11-jdk \
    xauth \
    x11-apps

# Configuração do servidor X
ENV DISPLAY=host.docker.internal:0

# Download e instalação do IntelliJ IDEA Community Edition
RUN wget -O intellij.tar.gz https://download.jetbrains.com/idea/ideaIC-2021.1.3.tar.gz && \
    tar -xzf intellij.tar.gz && \
    rm intellij.tar.gz

# Diretório de trabalho
WORKDIR /app

# Comando de inicialização
CMD ["sh", "-c", "/idea-IC-211.7628.21/bin/idea.sh"]
