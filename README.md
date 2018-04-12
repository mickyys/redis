Redis
=====
Pasos a seguir para instalar redis en equipo windows  
1. Se debe instalar [DOCKER](URL "https://www.docker.com")
2. Descargar imagen con el comando
    `docker run --name some-redis -d redis redis-server --appendonly yes`
3. Iniciar cliente 
    `docker run -it --link some-redis:redis --rm redis redis-cli -h redis -p 6379`

Link:
* [www.redis.io](URL "http://redis.io/")

## Comandos
1. [SET](URL "https://redis.io/commands/set") mykey "Hola Mundo" ex 10 
    - Asigna valor a key y ex asigna tiempo de expiracion
2. [GET](URL "https://redis.io/commands/get") mykey 
    - Obtiene key
3. [DEL](URL "https://redis.io/commands/del") mykey 
    - Elimina key
4. [KEYS](URL "https://redis.io/commands/keys") * 
    - Obtiene todas las keys
5. [MSET](URL "https://redis.io/commands/mset") mykey "Hola Mundo" mykey2 "Hola Mundo 2" 
    - Asigna multiple key   
6. [MGET](URL "https://redis.io/commands/mget") mykey mykey2 
    - Obtiene multiple key
7. [EXISTS](URL "https://redis.io/commands/exists") mykey 
    - Valida si existe key
8. [EXPIRE](URL "https://redis.io/commands/expire") mykey 10 
    - Asigna segundos de expiracion
9. [TTL](URL "https://redis.io/commands/ttl") mykey 
    - Obtiene tiempo restante de experiacion
