Redis
=====
Pasos a seguir para instalar redis en equipo windows  
1. Se debe instalar [DOCKER](https://www.docker.com)
2. Descargar imagen con el comando
    `docker run --name some-redis -d redis redis-server --appendonly yes`
3. Iniciar cliente 
    `docker run -it --link some-redis:redis --rm redis redis-cli -h redis -p 6379`

Link:
* [www.redis.io](http://redis.io)

## Comandos
1. [SET](https://redis.io/commands/set) mykey "Hola Mundo" ex 10 
    - Asigna valor a key y ex asigna tiempo de expiracion
2. [GET](https://redis.io/commands/get) mykey 
    - Obtiene key
3. [DEL](https://redis.io/commands/del) mykey 
    - Elimina key
4. [KEYS](https://redis.io/commands/keys) * 
    - Obtiene todas las keys
5. [MSET](https://redis.io/commands/mset) mykey "Hola Mundo" mykey2 "Hola Mundo 2" 
    - Asigna multiple key   
6. [MGET](https://redis.io/commands/mget) mykey mykey2 
    - Obtiene multiple key
7. [EXISTS](https://redis.io/commands/exists) mykey 
    - Valida si existe key
8. [EXPIRE](https://redis.io/commands/expire) mykey 10 
    - Asigna segundos de expiracion
9. [TTL](https://redis.io/commands/ttl) mykey 
    - Obtiene tiempo restante de experiacion
10. [HMSET](https://redis.io/commands/hmset) myhash field1 "Hello" field2 "World"
    - Asigna valor a la llave
11. [HGET](https://redis.io/commands/hget) myhash field1
    - Obtiene valor de la llave
12. [HMGET](https://redis.io/commands/hmget) myhash field1 field2
    - Obtiene multiple valor de la llave
13. [HGETALL](https://redis.io/commands/hgetall) myhash field1
    - Obtiene todos los valores de la llave
14. [HINCRBY](https://redis.io/commands/hincrby) usuario:1 edad 10
    - Incrementa valor de edad en 10
15. [SADD](https://redis.io/commands/sadd) myNumber 1 2 3 4
    - Agrega valor a la llave y concatena valores si ya existe
16. [SMEMBERS](https://redis.io/commands/smembers) myNumber 
    - Obtiene los miembres de la llave (sin ordenar) y se pueden realizar busqueda por elementos 
17. [SINTER](https://redis.io/commands/sinter) tags:csharp:blog tags:javascript:blog
    - Obtiene miembros en comun las llaves (tipo join en SQL)
18. [SUNIONSOTRE](https://redis.io/commands/sunionstore) tagsUnidos tags:nodejs:blog tags:visualstudio:blog
    - crea nueva llave con los valores distintos de las 2 llaves
    - tambien copia llave si solo tiene una llave
19. [SPOP](https://redis.io/commands/spop) myNumber
    - Elimina el primer miembro de la llave
