# ServerlessCRUDAPI
Scalable serverless CRUD API on AWS with Lambda, API Gateway, DynamoDB, and CloudWatch logging
 Serverless CRUD API (AWS Lambda + API Gateway + DynamoDB)

This project is a serverless REST API built on AWS that performs basic CRUD operations using:
AWS Lambda (backend logic)
API Gateway (REST endpoints)
DynamoDB (database)
IAM (permissions/security)
CloudWatch (logging/monitoring)

Features
Create an item
Read all items
Read a single item
Update an item
Delete an item

Architecture
Client > API Gateway > Lambda > DynamoDB > Logs > CloudWatch

Tech Stack
AWS Lambda
Amazon API Gateway
Amazon DynamoDB
AWS IAM
Amazon CloudWatch

API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | /items | Get all items |
| GET | /items/{id} | Get single item |
| POST | /items | Create item |
| PUT | /items/{id} | Update item |
| DELETE | /items/{id} | Delete item |

Example Request (POST)
```json
{
	"name": "do dishes",
    "completed": false
}
```
Example Request (Patch)
```json
{
"id": "(insert ID)",
    "name": "wash car",
    "completed": true
}
```
Deployed using AWS Console / AWS CLI (or SAM / Serverless Framework if you used it)

IAM Permissions
Lambda role includes permissions for:
DynamoDB read/write access
CloudWatch logs
What I Learned
How serverless architecture works on AWS
Connecting API Gateway to Lambda
Using DynamoDB as a NoSQL database
Managing IAM roles and permissions
Monitoring logs in CloudWatch

Future Improvements
Add authentication (Cognito or JWT)
Add input validation
Add pagination for GET requests
