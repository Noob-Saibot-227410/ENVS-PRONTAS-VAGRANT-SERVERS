# Base da imagem
FROM ubuntu:20.04

# Configuração da máquina
RUN apt-get update && \
    apt-get install -y wget && \
    wget https://repo.anaconda.com/archive/Anaconda3-2021.05-Linux-x86_64.sh && \
    chmod +x Anaconda3-2021.05-Linux-x86_64.sh && \
    ./Anaconda3-2021.05-Linux-x86_64.sh -b -p /root/anaconda3 && \
    echo 'export PATH="/root/anaconda3/bin:$PATH"' >> /root/.bashrc && \
    . /root/.bashrc && \
    conda install jupyter -y && \
    conda update -n base -c defaults conda -y

# Configuração do contêiner
EXPOSE 8888

# Comando de inicialização do Jupyter Notebook
CMD jupyter notebook --ip=0.0.0.0 --no-browser
