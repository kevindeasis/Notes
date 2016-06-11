# Notes

# Go
- [Go CLI cmd](https://golang.org/cmd/go/)
- [Running Unix execuctables & path](http://stackoverflow.com/questions/15080835/running-an-executable-in-mac-terminal)
- [go path playlist](https://www.youtube.com/watch?v=M2TTpIi62PQ&index=9&list=PLSak_q1UXfPpqIlNiyBhFQLMUvbkeWM7F)
- [Workspace](https://golang.org/doc/code.html#Workspaces)
- [Go Wiki](https://github.com/golang/go/wiki/Learn)
- [Go Tour](https://tour.golang.org/basics/1)
>
```
$ mkdir $HOME/work
//add to bashprofile
export GOPATH=$HOME/work
//OR
$ export GOPATH=$HOME/work
$ export PATH=$PATH:$GOPATH/bin
```


# Docker commands

- docker run [flags] <image> [args]
- docker start
- docker stop
- docker ps
- docker ps -a //
- docker ps -l //last created
- docker rm // remove container
- docker images
- docker-machine ip // get the ip of virtual host
- docker port <Container_Name> <Port Number> // find the mapping for external port given <Container_name> and <Port_Number>
- docker build -t <new-image-name> . 
- docker rmi -f <img or name> //remove image from the host
- docker -t --help 
- docker inspect <container_name>
- CMD [docker cmd ref](https://docs.docker.com/engine/reference/builder/#cmd) or (docker best practices; find cmd)(https://docs.docker.com/engine/userguide/eng-image/dockerfile_best-practices/)
- [-t and -i](https://coreos.com/os/docs/latest/getting-started-with-docker.html)

## Docker Args
> ```
-t  flag assigns a pseudo-tty or terminal inside the new container.
-i  flag allows you to make an interactive connection by grabbing the standard in (STDIN) of the container.
-d  background mound aka detached mode
```
## build
>docker build -t ourdockermicroservice:0.1 . //run inside directory with Dockerfile

## naming container
>docker run -d -P --name web training/webapp python app.py
## logs
>docker logs -f nostalgic_morse // -f is tail

## find process running inside container
>docker top nostalgic_morse

## docker commit
>docker commit -m "Added json gem" -a "Kevin De Asis" <image_id> kevindeas/appname:tagNumber

# Docker Example APP
>docker run -d -p 80:5000 training/webapp python app.py

>docker machine ls //get hostnames

>docker-machine ip [hostname]

>docker port <Container_Name> <Port Number>

given the information above:

>Open Browser to <DOCKER_IP>:<External_PORT>


# Setup
```
docker run -d -p 4321:8000 -w /workingDirectory

docker-machine create -help | grep [google, digitalocean ,...]

docker inspect nostalgic_morse // inspect
```

# vim ~/.bash_profile 

- echo 'echoes something when you start a terminal'
- alias commandName='echo "echoes something in the terminal when you enter run the commandName" '
- methodName(){ } //this is a function takes $1, ... $n arguments and can be run in the terminal w/ methodName args1 .. argsN

# vim /etc/hosts

- <ip.address> myvm.instance  // so now you can ssh user@myvm.instance

# Process
>```
ps aux | grep mysqld
pidof mysqld
kill -9 pid
killall <processName>
```
# Gcloud
>```
gcloud config set project <project-id>
gcloud compute instances list
gcloud components reinstall

gcloud preview app deploy
or gcloud preview app deploy app.yaml //docker

```

# Networking
>```
ifconfig //iptable for mac
dig google.com // swiss army knife for querying DNS servers
```

# Other Command Line stuff
>```
env //environment
$PATH
$HOME
//add to $PATH
//make it permanent by putting it in .bashrc in $HOME directory
export PATH=$PATH:$HOME/bin
```
more about [bash rc](http://superuser.com/questions/147043/where-to-find-the-bashrc-file-on-mac-os-x-snow-leopard-and-lion)

# [Build a command line tool](http://blog.npmjs.org/post/118810260230/building-a-simple-command-line-tool-with-npm)

# YC Questions
> ```
2 key metrics
How much does it cost is it to make a sale? (How easy is it to make a sale)
How cheap is it to serve a customer?
```

>"So what are you working on?",
  - "Have you raised funding?",
  - "What makes new users try you?",
  - "What competition do you fear most?",
  - "What’s the worst thing that has happened?",
  - "Will you reincorporate as a US company?",
  - "What’s an impressive thing you have done?",
  - "Where is the rocket science here?",
  - "Why did you pick this idea to work on?",
  - "Why do the reluctant users hold back?",
  - "Who would you hire or how would you add to your team?",
  - "What problems/hurdles are you anticipating?",
  - "Who is “the boss”?",
  - "What is the next step with the product evolution?",
  - "What obstacles will you face and how will you overcome them?",
  - "Who needs what you’re making?",
  - "How does your product work in more detail?",
  - "What are you going to do next?",
  - "What do you understand that others don’t?",
  - "Where do new users come from?",
  - "How big an opportunity is there?",
  - "Six months from now, what’s going to be your biggest problem?",
  - "What’s the funniest thing that has happened to you?",
  - "Tell us something surprising you have done?",
  - "Who are your competitors?",
  - "What’s new about what you make?",
  - "How many users do you have?",
  - "Why isn’t someone already doing this?",
  - "What are the top things users want?",
  - "What is your burn rate?",
  - "How do you know customers need what you’re making?",
  - "What domain expertise do you have?",
  - "What, exactly, makes you different from existing options?",
  - "What’s the conversion rate?",
  - "What systems have you hacked?",
  - "Who would use your product?",
  - "How will customers and/or users find out about you?",
  - "Why did your team get together?",
  - "In what ways are ysou resourceful?",
  - "What is your distribution strategy?",
  - "What has surprised you about user behaviour?",
  - "What part of your project are you going to build first?",
  - "What resistance will they have to trying you and how will you overcome it?",
  - "How are you understanding customer needs?",
  - "What’s the biggest mistake you have made?",
  - "Who might become competitors?",
  - "What do you understand about your users?",
  - "What is your user growth rate?",
  - "What are the key things about your field that outsiders don’t understand?",
  - "Who is going to be your first paying customer?",
  - "If your startup succeeds, what additional areas might you be able to expand into?",
  - "Who would be your next hire?",
  - "How do you know people want this?",
  - "Would you relocate to Silicon Valley?",
  - "What do you know about this space/product others don’t know?",
  - "How much money could you make per year?",
  - "How long can you go before funding?",
  - "How will you make money?",
  - "Will your team stick at this?",
  - "How much does customer acquisition cost?",
  - "How did your team meet?",
  - "Who in your team does what?",
  - "How are you meeting customers?",
  - "How many users are paying?",
  - "How is your product different?",
  - "Are you open to changing your idea?",
  - "How do we know your team will stick together?",
  - "What is your growth like?"
