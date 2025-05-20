# AWS Project: End-to-End AWS Web Application

## Project Description and Resources Used

  For this project I’m building an end-to-end application where I can request a unicorn to give me a ride (from the original Amazon Workshop). The website should take me through the process of creating an account, logging in, and accessing the map (powered by ArcGIS) to ask for the ride.

  Link to the tutorial followed: [Tiny Technical Tutorials](https://www.youtube.com/watch?v=K6v6t5z6AsU)

## AWS Services and Integration

- GitHub - Used as a source control system to create the wildryde-sites repo where the code will live.
- AWS Amplify - Amplify will allow me to build and host the static website. It will be hooked up to the wildrydes-sites GitHub repo for retrieving the code, and help trigger the CICD pipeline automatically.
- Amazon Cognito - Used for authentication and registration. The user pool will be set up manually and then updated on the code to hook things up.
- AWS Lambda - Used to create/trigger a function when the end user requests a ride.
- Amazon DynamoDB - After the Lambda function is invoked, the function will select a unicorn for them and record the request in the DynamoDB table and respond to the front end with details about the unicorn that will come and pick them up.
- AWS IAM - Used to create an execution role to grant Lambda write permissions to DynamoDB.
- API Gateway - Used to build HTTP, REST and WebSocket APIs. It will be in charge of invoking the Lambda function.

## WildRydes Website

- Link to the static website: https://main.d2qzfmq4oht1md.amplifyapp.com/ 
- Link to the sign-in page: https://main.d2qzfmq4oht1md.amplifyapp.com/signin.html 
- Link to the rides page: https://main.d2qzfmq4oht1md.amplifyapp.com/ride.html 

Step-by-step followed guide: https://docs.google.com/document/d/1pO0Kc02djy6pl5VeJXP4KS10JA3yOiBfJi54SVl3BDw/edit?usp=sharing
