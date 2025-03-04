# Imagem base
FROM ubuntu:22.04

# Atualiza o sistema e instala dependências
RUN apt update -y && apt upgrade -y && \
    apt install -y curl sudo

# Baixa e instala o code-server
RUN curl -fsSL https://code-server.dev/install.sh | sh

# Define o diretório de trabalho para os projetos
WORKDIR /root/projects

# Copia o arquivo de configuração do code-server para o local padrão
COPY config.yaml /root/.config/code-server/config.yaml

# Expõe a porta code-server
EXPOSE 4277

# Comando para iniciar o code-server
CMD ["code-server", "--bind-addr", "0.0.0.0:4277"]