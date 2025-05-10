# Orquestra_Conteiner
Estudo e prática sobre Containers e Docker.

## Comando Basicos

#### Verificação se o docker foi devidamente instalado
`docker`

#### Verificação da versão atual do docker
`docker -v`

#### Coletando informações básicas do docker
`docker info`

#### Puxando uma imagem do registry (Docker Hub)
`docker pull python`

#### Rodando um container docker da imagem puxada do registry
`docker run python`

#### Listando todos os containers e suas informações básicas
`docker ps -a`

#### Listando todos os containers ativos
`docker ps`

#### Listando as imagens que estão na máquina
`docker images`

#### Hello World - Docker
`docker pull hello-world`
`docker images`
`docker run hello-world`

#### Gera a imagem a partir do Dockerfile com o nome imagem-script
`docker build . -t imagem-script`

#### Remove um container parado
`docker rm [id-conteiner]`

#### Remove forçadamente um container em execução
`docker rm -f [id-conteiner]`

#### Remove uma imagem Docker
`docker rmi [id-imagem]`

#### Remove forçadamente uma imagem Docker em execução
`docker rmi -f [id-imagem]`

#### Parar o container
`docker stop <nome-do-container>`

#### Parando todos os containers que estão em execução
`docker stop $(docker ps -a -q)`

#### Iniciando o container com o nome definido
`docker start <nome-do-container>`

#### Removendo todos os containers que estão parados
`docker rm $(docker ps -a -q)`

#### Rodar o container e remover ele após rodar todos os comandos
`docker run --rm imagem-script`

#### Executa um container em segundo plano com um nome fixo e usando uma imagem específica com tag (versão)
`docker run -d --name <nome-do-container> <nome-da-imagem>:<tag>`

#### Acessa interativamente o terminal do container chamado <nome-do-container>
`docker exec -it <nome-do-container> bash`

#### Executa um container em segundo plano, com volume local mapeado para o diretório /app no container
`docker run -d --name <nome-do-container> -v ${PWD}/volume:/app <nome-da-imagem>:<tag>`

#### Exibe informações detalhadas (JSON) sobre o container especificado
`docker inspect <nome-do-container>`

#### Executa um container em segundo plano, mapeando a porta 8000 do host para a porta 8000 do container
`docker run -d -p 8000:8000 --name <nome-do-container> -v ${PWD}/app:/api/app <nome-da-imagem>:<tag>`

#### Gerar as imagens de todos os serviços do arquivo docker-compose.yaml
`docker-compose build`

#### Rodar os containers de todos os serviços do docker-compose.yaml em segundo plano
`docker-compose up -d`

#### Derrubar o conjunto de containers utilizando o comando down
`docker-compose down`

#### Cria uma imagem local com nome e tag, pronta para envio ao Docker Hub
`docker build . -t <usuario-dockerhub>/<nome-da-imagem>:<tag>`

#### Envia a imagem criada localmente para o repositório do Docker Hub
`docker push <usuario-dockerhub>/<nome-da-imagem>:<tag>`

#### Baixa a imagem do Docker Hub para a máquina local
`docker pull <usuario-dockerhub>/<nome-da-imagem>:<tag>`
