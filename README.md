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
- docker-machine ip // get the ip of virtual host
- docker port <Container_Name> <Port Number> // find the mapping for external port given <Container_name> and <Port_Number>
- docker build -t <new-image-name> . 
- docker rmi -f <img or name>
- docker -t --help 
- CMD [docker cmd ref](https://docs.docker.com/engine/reference/builder/#cmd) or (docker best practices; find cmd)(https://docs.docker.com/engine/userguide/eng-image/dockerfile_best-practices/)
- [-t and -i](https://coreos.com/os/docs/latest/getting-started-with-docker.html)

>docker build -t ourdockermicroservice:0.1 . //run inside directory with Dockerfile

# Docker Example APP
>docker run -d -p 80:5000 training/webapp python app.py

>docker machine ls //get hostnames

>docker-machine ip [hostname]

>docker port <Container_Name> <Port Number>

given the information above:

>Open Browser to <DOCKER_IP>:<External_PORT>


# Setup
docker run -d -p 4321:8000 -w /workingDirectory

>docker-machine create -help | grep [google, digitalocean ,...]

# vim ~/.bash_profile 

- echo 'echoes something when you start a terminal'
- alias commandName='echo "echoes something in the terminal when you enter run the commandName" '
- methodName(){ } //this is a function takes $1, ... $n arguments and can be run in the terminal w/ methodName args1 .. argsN

# vim /etc/hosts

- <ip.address> myvm.instance  // so now you can ssh user@myvm.instance

# Process
> ps aux | grep mysqld
pidof mysqld
kill -9 pid
killall <processName>
