# Week 1 — App Containerization

## Required Homework / Tasks

### Containerize Backend-flask and Frontend-react

I followed Andrew's Week1 video and containerized each individually:

I first containerized backend-flask with it's own dockerfile
![Proof of Individually Containerized Apps (backend-flask)](assets/proof-containerize-backend-flask-dockerfile.png)

I next containerized containerized frontend-react-js with its own dockerfile 
![Proof of Individually Containerized Apps (backend-flask)](assets/proof-containerize-frontend-react-dockerfile.png)

### Create docker-compose file to run multiple containers

I created the docker-compose file to run backend-flask and frontend-react-js (this screenshot also has the dynamodb and postgres databases and client included in the configuration.
![Proof of Creating and Running docker-compose to run Multiple Containers](assets/proof-docker-compose-file-created-and-functioning-with-multiple-containers.png)

### Add DynamoDB Local and Postgres

I did watch the follow up video "Week 1 - DynamoDB and Postgres vs Docker" and was able to walk through the steps with Andrew in order to create the dynamodb local and postgres databases.  

I was able to connect to the postgres SQL database server

![Proof of connecting to Postgres SQL server](assets/proof-of-Postgres-client-connection.png)

I was also able to create and connect to the dynamodb local database, create the table Music, and add the records (copy/paste from 100daysofcloud repo) but I didn't  take any screenshots of the proof when running the terminal commands.

### Create the Notifications Feature

I followed along with Andrew's followup video "Week 1 - Create the notification feature (Backend and Front)" and was able to successfully implement the Notifications feature in Cruddur with the dummy data.

![Proof of backend-flask notifications with personalized cruddur message - json output](assets/proof-of-json-for-backend-with-personalized-post.png)
![Proof of frontend react notifications with personalized cruddur message](assets/Proof-of-Notifications-setup.png)

## Homework Challenges
Still behind on the coursework.......
