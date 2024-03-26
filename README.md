# Timepiece Traders

Project lead of a team of 6 engineers for Software Engineering final project. We developed an auction system for users to buy and sell luxury watches. Users can create an account and post their own watches for sale with extensive customization options and auction deadline scheduling. Users can also search/filter for watches for sale, see auction information as well as the current bid, place their own bids or buy now, and track auctions they've won in their cart for checkout.

## Building the Application

Architecture:
1. Python / Flask - Flask was chosen as it is a lightweight and simple backend RESTful framework, team had high familiarity with Python already. With our microservices architecture, services are loosely coupled, so was set up well to have mulitple Flask server to encapsulate various business functions.
2. Node.js and Express.js - Node was chosen as a simple orchestrator for page components built using React. Express.js was chosen as it is an effective and commonly used middleware for routing requests to the backend, and would also support more advanced request authentication in the future.
3. RabbitMQ - didn't require large scale, retention of messages or data streaming initially, RabbitMQ chosen to handle simple inter-service communication.
4. Docker - containerized each microservice to allow a modular architecture, independent scaling if needed, and simplify pushing updates and deploying across a distributed team

<img width="1009" alt="Screen Shot 2023-12-13 at 10 56 54 AM" src="https://github.com/esegerberg3112/auction-site/assets/61920056/b9cce8c6-ade6-49b7-b980-f5114ab0c16a">

Technology Stack:

Frontend:
1. Node.js for serving the website
2. Express.js for the API Gateway and request routing
3. React.js / HTML / CSS for website pages

Backend:
1. Python - Flask
2. RabbitMQ for microservice communication

Databases:
1. MySQL - hosted in separate Docker containers (accounts, items, notifications, auctions)
2. Redis - hosted in Docker container (bidding)


## Running the Application
0. Download the repo and have Docker Desktop. In the root directory of this project locally, pip install microservices/requirements.txt
1. Run Docker Desktop App in your local machine
2. From a fresh terminal window, access the root directory of this project
3. Run: docker-compose build
4. Run: docker-compose up
5. Open a separate terminal and navigate to the same root directory
6. Run: bash start_application.sh
7. Acess a browser window, and search: "http://localhost:3000"
