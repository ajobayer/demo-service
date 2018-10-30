# Demo Service (Python && Docker && Openshift)
Python service which returns Hello my friend when hit

## Building A Demo Docker Image For A Python Service
1. At first install python3 in your system (Note Mac OS python2 is default so need to change the $PATH variables)
2. git clone https://github.com/ajobayer/hello-service.git
3. pip3 install -r requirements.txt
4. python3 demo-service.py

Hitting the service at http://localhost:5858 will display the demo world message:
------------------------------------------------------------
Hello my friend:


Hitting the service at http://localhost:5858/check-msg will display the demo world message:
------------------------------------------------------------
Hello my friend: check-msg


5. Dockerwise 

docker build -t docker-python-demo-world .

6. Openshift

Login to Openshift using oc cli

then fire 

oc new-app -f demo-service.yaml 
