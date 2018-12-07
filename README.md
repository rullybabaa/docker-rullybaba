<h1>DOCKER COMPOSE </h1>
<h2>membuat file dengan nama docker-compose.yml dan isinya seperti di bawah ini</h2>
web:<br>
  build: .<br>

  links:<br>
    - redis<br>

  ports:<br>
    - "3000"<br>
    - "8000"<br>

redis:<br>
  image: redis:alpine<br>
  volumes:<br>
    - /var/redis/data:/data<br>
	
<h2> selanjutnya buka Command Prompt dan masukan perintah di bawah ini</h2>
docker-compose up -d

<h2>Docker Management</h2>
Not only can Docker Compose manage starting containers but it also provides a way manage all the containers using a single command.

For example, to see the details of the launched containers you can use docker-compose ps

To access all the logs via a single stream you use docker-compose logs

Other commands follow the same pattern. Discover them by typing docker-compose.
