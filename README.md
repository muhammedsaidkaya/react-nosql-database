
<h3>Introduction</h3>
<p>React application which is document-based NoSQL database demo that stores data to local storage. ( Cloud Firestore Demo ). Command Pattern for encapsulating CRUD requests on any document and by using stack of requests, undoable redoable operations created and collections are committed, extracted (XML, JSON) </p>Hacettepe University, Bachelor's Degree, Computer Engineering - Design Patterns Course Term Project <br/> <br/> 

Use-cases: https://www.youtube.com/watch?v=P5j-L-Bs5AY <br/>

<hr/>

<b>You can download Docker image of this project in the below link. </b> <br/>

Image: https://hub.docker.com/r/uzumlukek/local-firestore <br/>

<b> Image created with following Dockerfile. </b> <br/>
```bash
FROM node:12-alpine
WORKDIR /usr/src/app 
COPY package*.json ./
RUN npm install
COPY . .
EXPOSE 3000
CMD [ "npm", "start" ]
```

<hr/>

<b> You can clone the repository and edit source code and up the project. </b> <br/>
```bash
git clone https://github.com/muhammedsaidkaya/react-nosql-database-demo.git
cd react-nosql-database-demo
.
.
docker-compose up --build
```
<hr/>

<b>  You can deploy the application on AWS EC2 instances by following steps.</b> <br/>

<ul>
  <li>Creating a Virtual Private Cloud</li>
  <li>Subnet creation in 2 different availabiltiy zones</li>
  <li>Receiving external requests to VPC with Internet Gateway</li>
  <li>Associating requests to subnets with route table</li>
  <li>Launching 2 EC2 instances on 2 subnets and pulling the image from Docker Hub and run the container</li>
  <li>Allowing port 80 of EC2 instances with secure groups</li>
  <li>Accessing 2 EC2 instances from the same dns name with load balancer</li>
</ul>

<b>  Userdata </b> <br/>
```bash
#!/bin/bash -ex 
curl -fsSL https://get.docker.com -o get-docker.sh 
sh get-docker.sh 
sudo usermod -aG docker $(whoami) 
sudo docker container run -p 80:3000 -d uzumlukek/local-firestore:testing 
```
<hr/>


<b> You can see the images of project. </b> <br/>

<img src="images/json.jpeg" />
<img src="images/edit.jpeg" />
<img src="images/xml.jpeg" />




