# AWS Project: End-to-End AWS Web Application
May 20, 2025

In this project, I’m developing a full end-to-end web application inspired by Amazon’s original workshop, where users can actually summon a ride from a unicorn! 🦄 The application features a seamless user journey: from account creation and secure login to an interactive, real-time map powered by ArcGIS, enabling users to request their magical ride with just a few clicks. This hands-on build combines modern authentication flows, geospatial mapping, and dynamic frontend-backend integration to deliver an immersive and technically robust experience.

Link to the tutorial followed: [Tiny Technical Tutorials](https://www.youtube.com/watch?v=K6v6t5z6AsU)

## Architecture Diagram

![Image](https://github.com/user-attachments/assets/1d21b90a-eb59-47b4-a379-a60c6286e699)

## AWS Services and Integration

- GitHub - Used as a source control system to create the repo where the code will live.
- AWS Amplify - Amplify will allow me to build and host the static website. It will be hooked up to the GitHub repo for retrieving the code, and help trigger the CICD pipeline automatically.
- Amazon Cognito - Used for authentication and registration. The user pool will be set up manually and then updated on the code to hook things up.
- AWS Lambda - Used to create/trigger a function when the end user requests a ride.
- Amazon DynamoDB - After the Lambda function is invoked, the function will select a unicorn for them and record the request in the DynamoDB table and respond to the front end with details about the unicorn that will come and pick them up.
- AWS IAM - Used to create an execution role to grant Lambda write permissions to DynamoDB.
- API Gateway - Used to build HTTP, REST and WebSocket APIs. It will be in charge of invoking the Lambda function.

Step-by-step project summary: https://drive.google.com/file/d/1vU64uZzDsTDYpq3J01dhSdE8jOOdfd1E/view
