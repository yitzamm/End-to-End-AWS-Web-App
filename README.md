# AWS Project: End-to-End AWS Web Application

## Architecture Diagram

![Image](https://github.com/user-attachments/assets/1d21b90a-eb59-47b4-a379-a60c6286e699)

## Project Description and Resources Used

For this project, I’m building a full end-to-end web application inspired by Amazon’s original workshop—where you can actually request a ride from a unicorn! 🦄 The site will guide users through creating an account, logging in, and accessing an interactive map powered by ArcGIS to summon their magical ride.

Link to the tutorial followed: [Tiny Technical Tutorials](https://www.youtube.com/watch?v=K6v6t5z6AsU)

## AWS Services and Integration

- GitHub - Used as a source control system to create the repo where the code will live.
- AWS Amplify - Amplify will allow me to build and host the static website. It will be hooked up to the GitHub repo for retrieving the code, and help trigger the CICD pipeline automatically.
- Amazon Cognito - Used for authentication and registration. The user pool will be set up manually and then updated on the code to hook things up.
- AWS Lambda - Used to create/trigger a function when the end user requests a ride.
- Amazon DynamoDB - After the Lambda function is invoked, the function will select a unicorn for them and record the request in the DynamoDB table and respond to the front end with details about the unicorn that will come and pick them up.
- AWS IAM - Used to create an execution role to grant Lambda write permissions to DynamoDB.
- API Gateway - Used to build HTTP, REST and WebSocket APIs. It will be in charge of invoking the Lambda function.


Step-by-step project guide: https://docs.google.com/document/d/1pO0Kc02djy6pl5VeJXP4KS10JA3yOiBfJi54SVl3BDw/edit?usp=sharing
