# Docker: tips and trics:

Check out the [repository by Thijs for tips and trics in docker](https://github.com/cor-mobile-robotics/docker_intro)

## Docker good-practice
To avoid large un-used containers, occasionally remove un-used containers:
```bash
sudo docker images -a | grep none | awk '{ print $3; }' | sudo xargs docker rmi –force #delete all images called "none"
docker system prune #delete all old/unused files in /var/lib/docker/
sudo docker container prune #delete ALL containers
```

## Useful basic docker images:
- [ This docker image](https://github.com/nachovizzo/ros_in_docker) uses docker-compose.yaml. Your local src folder gets updated locally and in the docker when adapted. Be aware that a an integrating of a catkin build (or catkin_make) might not be possible within the Dockerfile (as the src folder needs to be mounted for this). 
- [In this repo](https://github.com/saraybakker1/kuka_workspace_docker), I made my own docker image for the Kuka iiwa 14, which doesn't have a locally mounted src folder. Write me a message for access :). 
