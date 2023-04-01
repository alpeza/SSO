# SSO
Ejemplo de SSO con nginx

1.- Levantar el NPM

```bash
docker-compose -f "npm/docker-compose.yml" up -d
```

2.- `/etc/hosts`


```bash
127.0.0.1       service1.example.com
127.0.0.1       service2.example.com
127.0.0.1       service3.example.com
```

* Service 1: `service1.example.com:5004` o `localhost:5004` 
* Service 2: `service2.example.com:5005` o `localhost:5005` 
* Service 3: `service3.example.com:5006` o `localhost:5006` 


2.- Levantar los servicios

```bash
docker-compose -f "services/docker-compose.yml" up -d
```

Accedemos a `localhost:81`

```
admin@example.com
changeme
```
adminx@example.com

```bash
docker network inspect npm_ssonet --format '{{range $id, $container := .Containers}}{{$container.Name}} - {{$container.IPv4Address}}{{println}}{{end}}'
```

```
docker-compose -f "authentik/docker-compose.yml" up -d
``` 

[localhost:9000/if/flow/initial-setup/](http://localhost:9090/if/flow/initial-setup/)

```bash
127.0.0.1       auth.example.com
```