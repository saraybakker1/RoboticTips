# Docker: tips and trics:

## Docker good-practice
To avoid large un-used containers, occasionally remove un-used containers:
```bash
sudo docker images -a | grep none | awk '{ print $3; }' | sudo xargs docker rmi –force #delete all images called "none"
docker system prune #delete all old/unused files in /var/lib/docker/
