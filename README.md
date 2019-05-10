# Docker snippet
## Container
### Bash no container
```ssh
docker exec -it nome_container bash
```
## Mysql
### Dump
```ssh
$ docker exec nome_container /usr/bin/mysqldump -u usuario --password=senha name_base > dump.sql
```
### Restore
```ssh
$ docker exec -i nome_container /usr/bin/mysql -u usuario --password=senha name_base < dump.sql
```
## Erros
> erro  The 'INFORMATION_SCHEMA.GLOBAL_STATUS' feature is disabled: see the documentation for 'show_compatibility_56' (3167)

entrar no container "docker exec -it nome_container bash" depois no mysql
```ssh
$ set @@global.show_compatibility_56=ON;
```