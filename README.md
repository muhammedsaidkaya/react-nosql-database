
<h3>Introduction</h3>
<p>React application which is document-based NoSQL database demo that stores data to local storage. ( Cloud Firestore Demo ). Command Pattern for encapsulating CRUD requests on any document and by using stack of requests, undoable redoable operations created and collections are committed, extracted (XML, JSON) </p>Hacettepe University, Bachelor's Degree, Computer Engineering - Design Patterns Course Term Project <br/> <br/> 

Use-cases: https://www.youtube.com/watch?v=P5j-L-Bs5AY <br/>

<hr/>

<b>You can download image of this project in the below link. </b> <br/>

Image: https://hub.docker.com/r/uzumlukek/local-firestore <br/>

<b> You can clone the repository and edit source code and up the project. </b> <br/>

git clone https://github.com/muhammedsaidkaya/react-nosql-database-demo.git <br/>
cd react-nosql-database-demo <br/>
docker-compose up --build <br/>

<hr/>


<b> You can make a demo of project </b> <br/>

Live: http://load-balancer-said-1025287615.eu-central-1.elb.amazonaws.com/ <br/>

<b>  The project deployed the instances by following steps.</b> <br/>

<ul>
  <li>Creating a Virtual Private Cloud</li>
  <li>Subnet creation in 2 different availabiltiy zones</li>
  <li>Receiving external requests to VPC with Internet Gateway</li>
  <li>Associating requests to subnets with route table</li>
  <li>Launching 2 EC2 instances on 2 subnets and pulling the image from Docker Hub and run the container</li>
  <li>Allowing port 80 of EC2 instances with secure groups</li>
  <li>Accessing 2 EC2 instances from the same dns name with load balancer</li>
</ul>

<b>  The container run on the EC2 instance by following script. </b> <br/>

#!/bin/bash -ex <br/>
curl -fsSL https://get.docker.com -o get-docker.sh <br/>
sh get-docker.sh <br/>
sudo usermod -aG docker $(whoami) <br/>
sudo docker container run -p 80:3000 -d uzumlukek/local-firestore:testing <br/>

<hr/>


<b> You can see the images of project. </b> <br/>

<img src="images/json.jpeg" />
<img src="images/edit.jpeg" />
<img src="images/xml.jpeg" />




