# docker-lab-test
Docker images file to test port container
You can clone this git to test docker

First, open cli and mkdir some file to keep this git, and cd to that file 
For window command : ipconfig
FOR linux command : ifconfig
//find you ip address and remember it.

command : git clone https://github.com/thanwaICT/docker-lab-test.git

command : cd docker-lab-test.git

In window, you can view file by "type <filename>"
In Linux use "cat <filename>"

Ok, let build a docker images.

command : docker build -t test .
//-t for create name of this images

command : docker images
//to see is images that we create

Now, we will run this image.

command : docker run --name testport -p 4000:80 test
//--name <name> for create name of this container
//you can put -d in front of -p to run container in the background.
//-p <host port>:<container port> <image name> to config port between host and container

it will show this inthe last line
* Running on http://0.0.0.0:80/ (Press CTRL+C to quit)

Now, open web browser.
and enter <host ip>:<port of host>
//we set port is 4000
example like this: 127.0.0.0:4000
and see the result. yeah! now, you are using container of docker

Come back to cli and check container
command : docker ps
//to see running container 

command : docker ps -a 
//to see all container

command : docker stop testport
//to stop running container

command : docker rm testport
//to remove container
