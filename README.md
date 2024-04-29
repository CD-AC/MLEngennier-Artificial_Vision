
# Object Detection Application with YOLOv5 on AWS
![Banner Image](https://raw.githubusercontent.com/CD-AC/MLEngennier_ArtificialVision/main/Architecture.png)

This repository contains the source code for an object detection application built using Ionic framework for the frontend and AWS services for the backend. The application allows users to capture photos using their devices and submit them to an API hosted on AWS. The submitted images are then analyzed using the YOLOv5 model to predict the objects present in the image along with their quantities.

## Architecture Overview
The application architecture consists of the following components:

Ionic Application: The frontend interface where users capture and submit photos.
API Gateway: Hosts the API endpoints to receive images from the Ionic application.
Amazon S3: Stores the images uploaded by users and the JSON files containing the object detection results.
AWS Lambda: Triggers on image uploads to S3, performs object detection using the YOLOv5 model, and saves the results as JSON files in S3.
Event Notifications: S3 triggers notifications to an AWS Lambda function, which sends the processed JSON back to the Ionic application.
## Setup Instructions
To deploy and run the application, follow these steps:

Clone this repository to your local machine.
Deploy the Ionic application to your desired platform (AWS Amplify, Elastic Beanstalk, etc.).
Configure the API Gateway to accept image uploads and trigger AWS Lambda functions.
Set up Amazon S3 buckets for input and output storage.
Deploy the AWS Lambda function for image analysis using YOLOv5.
Configure event notifications from the output S3 bucket to trigger a Lambda function to send JSON data back to the Ionic application.
Update the Ionic application to handle incoming JSON data and display the object detection results.
For detailed setup instructions and additional documentation, refer to the respective directories in this repository.
