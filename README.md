# docker-gitlab
**GitLab with Docker Compose** 

Using Docker Compose to start a GitLab.

## Prerequisite

+ Install [Docker][1] and [Docker Compose][2] in your testing environment

## Start with following steps

+ (0) Modify hosts as follows:

```
Server's IP gitlab.9f0.net
```

+ (1) Start gitlab

```
docker-compose up -d
```

The result is 

```
Creating network "docker-gitlab_bridge" with driver "bridge"
Creating docker-gitlab_gitlab_1 ... done
```

+ (2) Check the status of GitLab

```
docker-compose ps
```

The result is 

```
         Name                Command               State                          Ports               
------------------------------------------------------------------------------------------------------
docker-gitlab_gitlab_1   /assets/wrapper   Up (health: starting)   22/tcp, 443/tcp, 0.0.0.0:80->80/tcp
```

Waiting a few minutes:

```
         Name                Command          State                      Ports               
---------------------------------------------------------------------------------------------
docker-gitlab_gitlab_1   /assets/wrapper   Up (healthy)   22/tcp, 443/tcp, 0.0.0.0:80->80/tcp
```

+ (3) Login GitLab and change root password : http://gitlab.9f0.net


[1]: https://www.docker.com
[2]: https://docs.docker.com/compose/

## License

Apache 2.0 license
