# SA58_AlvinLee_Fibonacci

## Description
This repository contains the project files for the frontend (React.js) and backend (Spring Boot) of a RESTful API webservice that takes in a target amount e.g., `1250.00` and an array of coin denominations e.g., `["1000.0","100.0","50.0"]`.

It returns a JSON that states the target amount, coin denominations, and the minimum number of coins required to get the target amount e.g., `{"targetAmount":"1250.00","coinDenominations":["1000.0","100.0","50.0"],"minimumCoins":{"1000.0":1,"100.0":2,"50":1}}`.

## Using the service
1. Visit the frontend via http://13.54.119.163:3000/
2. Test the api via Postman
    > POST: http://13.54.119.163:8080/api/coin-request
    > Body, raw, JSON: {"targetAmount": 1250.0,"coinDenominations": [1000.0,100.0,50.0]}
3. Access the api via command line
    - Linux:
    > `curl -H "Accept: application/json" -H "Content-type: application/json" -X POST -d '{"targetAmount": 1250.0,"coinDenominations": [1000.0,100.0,50.0]}' http://13.54.119.163:8080/api/coin-request`

## Languages / Frameworks
Java (OpenJDK-17), Spring Boot, React.js

## Building and running the application locally

### Git Clone
In your target directory, run `git clone git@github.com:zephyrdark/SA58_AlvinLee_Fibonacci.git`

### Docker
When you're ready, start your application by running:
`docker compose up --build`.

Your application will be available at http://localhost:8080.

### Deploying your application to the cloud

First, build your image, e.g.: `docker build -t myapp .`.
If your cloud uses a different CPU architecture than your development
machine (e.g., you are on a Mac M1 and your cloud provider is amd64),
you'll want to build the image for that platform, e.g.:
`docker build --platform=linux/amd64 -t myapp .`.

Then, push it to your registry, e.g. `docker push myregistry.com/myapp`.

Consult Docker's [getting started](https://docs.docker.com/go/get-started-sharing/)
docs for more detail on building and pushing.
