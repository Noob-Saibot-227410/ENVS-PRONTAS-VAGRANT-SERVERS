# Base image com JDK instalado
FROM openjdk:latest

# Instalação das dependências do IntelliJ IDEA
RUN apt-get update && apt-get install -y libxrender1 libxtst6 libxi6 libfreetype6

# Download e instalação do IntelliJ IDEA Community Edition
RUN wget -O intellij.tar.gz https://download.jetbrains.com/idea/ideaIC-2021.1.3.tar.gz && \
    tar -xzf intellij.tar.gz && \
    rm intellij.tar.gz

# Variáveis de ambiente
ENV PATH="/idea-IC-211.7628.21/bin:${PATH}"

# Diretório de trabalho
WORKDIR /app

# Comando de inicialização (opcional)
CMD ["/idea-IC-211.7628.21/bin/idea.sh"]

---

docker build -t intellij-container .

---

No power shell

$env:DISPLAY = "host.docker.internal:0.0"

---

docker run -it --rm -e DISPLAY=$DISPLAY -v /tmp/.X11-unix:/tmp/.X11-unix intellij1-container
docker run -it --rm -e DISPLAY=$DISPLAY -v /tmp/.X11-unix:/tmp/.X11-unix intellij2-container
