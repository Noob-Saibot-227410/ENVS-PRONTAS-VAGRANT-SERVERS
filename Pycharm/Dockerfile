# Imagem base com Python e dependências gráficas
FROM python:latest

# Instalação das dependências gráficas
RUN apt-get update && apt-get install -y libxrender1 libxtst6 libxi6

# Download e instalação do PyCharm Community Edition
RUN wget -O pycharm.tar.gz https://download.jetbrains.com/python/pycharm-community-2021.1.3.tar.gz && \
    tar -xzf pycharm.tar.gz && \
    rm pycharm.tar.gz

# Variáveis de ambiente para suporte gráfico
ENV DISPLAY=:0
ENV QT_X11_NO_MITSHM=1

# Diretório de trabalho
WORKDIR /app

# Comando de inicialização do PyCharm
CMD ["/bin/bash", "-c", "/pycharm-community-2021.1.3/bin/pycharm.sh"]
