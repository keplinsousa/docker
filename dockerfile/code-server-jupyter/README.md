# Code-Server com Jupyter 🖥️📓  
Este repositório contém um Dockerfile para criar uma imagem do [Code-Server](https://github.com/coder/code-server) com suporte a Jupyter Notebooks, permitindo que você execute notebooks dentro do VS Code no navegador.  

## 📦 Construindo a Imagem  
Para criar a imagem Docker do Code-Server com Jupyter, execute o seguinte comando no diretório onde está o Dockerfile:  
```sh
docker build -t code-server-jupyter .
```

## 🚀 Executando o Container
Para rodar o Code-Server com Jupyter em um container, execute:
```sh
docker run -d --name code-server-jupyter -p 8080:8080 code-server-jupyter
```

Isso fará com que o Code-Server fique acessível em:
```sh
http://localhost:8080
```

## ⚙️ Configuração
O arquivo config.yaml define as configurações do Code-Server. Por padrão:
- A autenticação está desativada (auth: none).
- O servidor não utiliza HTTPS (cert: false).
- O Code-Server está configurado para rodar na porta 8080.


## 🛑 Parando e Removendo o Container
Para parar o container:
```sh
docker stop code-server-jupyter
```

Para removê-lo:
```sh
docker rm code-server-jupyter
```

Agora você pode rodar seu VS Code com suporte a Jupyter diretamente no navegador! 🚀