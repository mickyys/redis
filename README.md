Redis
=====
Pasos a seguir para instalar redis en equipo windows  

Link:
* [www.redis.io](URL "https://redis.io/")

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
