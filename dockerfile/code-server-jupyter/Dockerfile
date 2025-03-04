# Usar uma imagem base do Ubuntu
FROM ubuntu:22.04

# Atualizar pacotes e instalar dependências essenciais
RUN apt update && apt install -y \
    curl \
    wget \
    sudo \
    gnupg \
    software-properties-common \
    python3 \
    python3-pip \
    python3-venv \
    && rm -rf /var/lib/apt/lists/*

# Instalar o Code-Server (VS Code Server)
RUN curl -fsSL https://code-server.dev/install.sh | sh

# Define o diretório de trabalho para os projetos
WORKDIR /root/projects

# Copia o arquivo de configuração do code-server para o local padrão
COPY config.yaml /root/.config/code-server/config.yaml

# Expõe a porta padrão do code-server
EXPOSE 8080

# Comando para iniciar o code-server sem usuário extra
CMD ["code-server", "--bind-addr", "0.0.0.0:8080"]