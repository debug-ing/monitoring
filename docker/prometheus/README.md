## prometheus

this repository docker prometheus + nginx (for secure connection)

```bash
# make password
$  htpasswd -c .htpasswd <username>
```

```bash
# run on docker
$ docker-compose up -d

# stop and remote from docker 
$ docker-compose down --volumes --remove-orphans
```