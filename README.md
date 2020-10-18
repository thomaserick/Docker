# Docker

### Comandos

- docker ps
	- Verifica os containers rodando
	
- docker exec "container_id"
	- Executa o container
	
- docker "container_id" exec -it /bin/bash
	- Terminal dentro do container
	- pode pegar os três primeiros numeros

- docker stop "container_id"
	- stopa o shutdown no servidor docker

- Gerar o container com as imagens
	- docker-compose up --build --force-recreate
	
### Comandos Dockerfile
- FROM

  - Imagens

- COPY

  - Mesmo diretório que está o dockerfile
  - Copia o arquivo dentro do container

- ADD

  - Mesma coisa que o copia
  - Especifica uma url para executar o download
  - Arquivo remoto
  - Descompactar um arquivo .tar

- RUN

  - Executa algum comando no container
  - EX: mkdir /XPTO

- CMD

  - Executa alguma coisa quando o container estiver executado
  - Ex:["ls"]
  - Ex com entrypoint ["/app"]

- ENTRYPOINT [ "ls"]

  - Quando tem os dois comandos CMD executa como parametro do entrypoint

- WORKDIR /app

  - Diretorio que o container vai estar(Raiz)

- ENV
  - Ex: MINHA_APLICAÇÃO=app.jar
  - Faz a criação de uma variável de ambiente

- EXPOSE
  - Ex: 8080
  - expor alguma porta dentro do container
  
# Docker-composer

- Rodar o docker
	- docker-compose up
- VERSION
	- versao do dockercomposer
- SERVICES
	- imagens que vao disponibilizar
- IMAGE
	- imagem configurada
- VOLUMES
	- ./project:/var/www/html/
- PORTS
	- "80:80"
- DB	
	- image:mysql:
	- ports:
		- "3306:3306"
	- enviroment
		- MYSQL_ROOT_HOST=%
		- MYSQL_DATABASE=mysql
		- MYSQL_USER=root
		- MYSQL_ALLOW_EMPTY_PASSWORD=true
	volumes:
	- ./docker/mysql_volume:/var/lib/mysql
- BUILD
	- CONTEXT
		- Pasta que está o docker file
	- DOCKERFILE
		- nome do arquivo "Dockerfile"
	- IMAGEM
		- Nome da imagem que está buildando
- LINK
	- Linkar os dois serviços

### Instalação

- Docker
  - docker -v

## DockerFile

### Adendo

**Helpers**

- [Docker](https://docs.docker.com/get-started/)
- [Format GitHub](https://help.github.com/en/articles/basic-writing-and-formatting-syntax)
