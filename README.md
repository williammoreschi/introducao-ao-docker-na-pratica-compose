# Docker Compose
Esse projeto é uma continuação do projeto anterior. 

No anterior eu precisava executar 6 comandos para que a aplicação ficasse de pé e mais um para criar o banco e a tabela.

Usando o composer com um único comando a aplicação está de pé, e mais um para criar o banco e tabela.

### Para por os containers de pé
```sh
docker-compose up -d
```

A primeira vez que usar o comando acima o banco não vai existir execute esses comandos.
```sh
docker exec -i mysql-container mysql -uroot -pdocker < db/script.sql
docker exec -d -i node-container npm start
```

**Caso o comando mysql der erro aguarde um pouco tente novamente*


### Derrubar todos os containers
```sh
docker-compose stop
```

Projeto Anterior: 
<a href='https://github.com/williammoreschi/introducao-ao-docker-na-pratica'>Projeto Anterior</a>

Link da aula: 
<a href='https://www.youtube.com/watch?v=HxPz3eLnXZk'>EAD #7: Docker compose na API</a>


Para ter acesso aos dados via api acesse localhost:9001/users

Para ter acesso aos dados via website acesse localhost:8888