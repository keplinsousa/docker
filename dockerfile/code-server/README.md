# Code-Server 🖥️  
Este repositório contém um Dockerfile para criar uma imagem do [Code-Server](https://github.com/coder/code-server), permitindo que você execute o VS Code em um navegador.  

***
## 📦 Construindo a Imagem  
Para criar a imagem Docker do Code-Server, execute o seguinte comando no diretório onde está o Dockerfile:  
```sh
docker build -t code-server .
```

***
## 🚀 Executando o Container
Para rodar o Code-Server em um container, execute:
```sh
docker run -d --name code-server -p 4277:4277 meu-code-server
```
Isso fará com que o Code-Server fique acessível em:
```sh
http://localhost:4277
```

***
## ⚙️ Configuração
O arquivo config.yaml define as configurações do Code-Server. Por padrão:
A autenticação está desativada (auth: none).
O servidor não utiliza HTTPS (cert: false).
O Code-Server está configurado para rodar na porta 4277.

***
## 🛑 Parando e Removendo o Container
Para parar o container:
```sh
docker stop code-server
```

Para removê-lo:
```sh
docker rm code-server
```

Agora você pode rodar seu VS Code diretamente no navegador com essa imagem Docker! 🚀