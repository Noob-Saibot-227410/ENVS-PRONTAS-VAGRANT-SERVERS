# Dockerfile
FROM ubuntu:focal

# Instalação de pacotes iniciais
RUN apt-get update
    # && apt-get install -y wget unzip libxrandr2 xdg-utils git

# Instalação do Visual Studio Code
# RUN wget -O code.deb https://go.microsoft.com/fwlink/?LinkID=760868 \
#     && dpkg -i code.deb \
#     && apt-get install -f --fix-missing \
#     && apt-get install -y apt-transport-https \
#     && wget -q https://packages.microsoft.com/keys/microsoft.asc -O- | gpg --dearmor > packages.microsoft.gpg \
#     && install -o root -g root -m 644 packages.microsoft.gpg /etc/apt/trusted.gpg.d/ \
#     && echo "deb [arch=amd64] https://packages.microsoft.com/repos/vscode stable main" > /etc/apt/sources.list.d/vscode.list \
#     && apt-get update \
#     && apt-get install -y code

# Instalação do Terraform
# RUN wget https://releases.hashicorp.com/terraform/1.4.6/terraform_1.4.6_linux_amd64.zip \
#     && unzip terraform_1.4.6_linux_amd64.zip \
#     && mv terraform /usr/local/bin/ \
#     && echo 'export PATH=$PATH:/usr/local/bin' >> ~/.bashrc \
#     && source ~/.bashrc

# Instalação do AWS CLI
# RUN apt-get install -y awscli

# Instalação do Code Server
# RUN wget -O code-server.tar.gz https://github.com/cdr/code-server/releases/download/v3.11.1/code-server-3.11.1-linux-amd64.tar.gz \
#     && tar -xzvf code-server.tar.gz \
#     && mv code-server-3.11.1-linux-amd64 /usr/local/lib/code-server \
#     && rm code.deb code-server.tar.gz terraform_1.4.6_linux_amd64.zip

# Configuração do VS Code Server
# ENV PORT=3000
# CMD /usr/local/lib/code-server/code-server --user-data-dir=/vagrant --bind-addr=0.0.0.0:$PORT --auth none
