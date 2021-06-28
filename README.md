<b>You can download image of this project in the below link. </b> <br/>

Image: https://hub.docker.com/r/uzumlukek/local-firestore <br/>

<b> You can clone the repository and up the project. </b> <br/>

git clone https://github.com/muhammedsaidkaya/react-nosql-database-demo.git <br/>
cd react-nosql-database-demo <br/>
docker-compose up --build <br/>


<b> You can make a demo of project on AWS EC2 Instance </b> <br/>

Live: http://load-balancer-said-1025287615.eu-central-1.elb.amazonaws.com/ <br/>

<b>  The project deployed the instance by following script. </b> <br/>

#!/bin/bash -ex <br/>
curl -fsSL https://get.docker.com -o get-docker.sh <br/>
sh get-docker.sh <br/>
sudo usermod -aG docker $(whoami) <br/>
sudo docker container run -p 80:3000 -d uzumlukek/local-firestore:testing <br/>


<b> You can see the images of project. </b> <br/>

<img src="images/json.jpeg" />
<img src="images/edit.jpeg" />
<img src="images/xml.jpeg" />




