# Notes

# Docker commands

- docker run <image> [args]
- docker start
- docker stop
- docker ps
- docker ps -a //
- docker ps -l //created
- docker rm
- docker images
- docker build -t <new-image-name> . 
- docker rmi -f <img or name>
- docker -t --help 
- CMD [docker cmd ref](https://docs.docker.com/engine/reference/builder/#cmd) or (docker best practices; find cmd)(https://docs.docker.com/engine/userguide/eng-image/dockerfile_best-practices/)
- [-t and -i](https://coreos.com/os/docs/latest/getting-started-with-docker.html)

# Setup

# vim ~/.bash_profile 

- echo 'echoes something when you start a terminal'
- alias commandName='echo "echoes something in the terminal when you enter run the commandName" '
- methodName(){ } //this is a function takes $1, ... $n arguments and can be run in the terminal w/ methodName args1 .. argsN

# vim /etc/hosts

- <ip.address> myvm.instance  // so now you can ssh user@myvm.instance
