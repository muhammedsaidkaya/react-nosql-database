<b>You can download image of this project in the below link. </b> <br/>

Image: https://hub.docker.com/r/uzumlukek/local-firestore <br/>

<b> You can clone the repository and edit source code and up the project. </b> <br/>

git clone https://github.com/muhammedsaidkaya/react-nosql-database-demo.git <br/>
cd react-nosql-database-demo <br/>
docker-compose up --build <br/>


<b> You can make a demo of project </b> <br/>

Live: http://load-balancer-said-1025287615.eu-central-1.elb.amazonaws.com/ <br/>

<b>  The project deployed the instances by following steps.</b> <br/>

Creating a Virtual Private Cloud <br/>
Subnet creation in 2 different availabiltiy zones <br/>
Receiving external requests to VPC with Internet Gateway <br/>
Associating requests to subnets with route table <br/>
Launching 2 EC2 instances on 2 subnets and pulling the image from Docker Hub and run the container <br/>
Allowing port 80 of EC2 instances with secure groups <br/>
Accessing 2 EC2 instances from the same dns name with load balancer <br/>

<b>  The container run on the EC2 instance by following script. </b> <br/>

#!/bin/bash -ex <br/>
curl -fsSL https://get.docker.com -o get-docker.sh <br/>
sh get-docker.sh <br/>
sudo usermod -aG docker $(whoami) <br/>
sudo docker container run -p 80:3000 -d uzumlukek/local-firestore:testing <br/>

<b> You can see the images of project. </b> <br/>

<img src="images/json.jpeg" />
<img src="images/edit.jpeg" />
<img src="images/xml.jpeg" />




