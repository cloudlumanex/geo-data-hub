# Geo Data Hub

## Problem

Geological field data in Nigeria is fragmented.

- Data lives in notebooks, spreadsheets, and local files
- Teams cannot access data in real time
- Data gets lost or overwritten
- Decision making is slow during exploration

There is no simple, cloud-based system to ingest, store, and query geological data.

## Solution

This project builds a serverless platform to centralize geological data.

- Upload field data through an API
- Store raw data in S3 with versioning
- Process and structure data using Lambda
- Store structured data in DynamoDB
- Expose APIs for querying geological records

This creates a single source of truth for exploration data.

## Use Case
- Field engineers upload sample data
- System processes and stores the data automatically
- Engineers and analysts query data in seconds

Example query:

“Find all tin samples in Jos with depth greater than 40m”

## Architecture

### Flow:

- Client uploads data
- API Gateway receives request
- Data stored in S3
- S3 event triggers Lambda
- Lambda processes and stores data in DynamoDB
- API serves query requests

## Tech Stack

- AWS Lambda
- API Gateway
- S3
- DynamoDB
- EventBridge
- Terraform
- GitHub Actions

## Project Structure

```

geo-data-hub/
├── infra/          # Terraform infrastructure
├── app/            # Lambda functions
├── events/         # Sample test events
├── tests/          # Unit tests
└── README.md

```

## Current Status

In progress

 - [x] Repository setup
 - [ ] Infrastructure provisioning
 - [ ] File upload pipeline
 - [ ] Data processing Lambda
 - [ ] Query API
 - [ ] Monitoring and logging


## Why This Project

This project combines:

* Geology domain knowledge
* Cloud engineering
* DevOps practices

It demonstrates how to build a production-ready, event-driven data platform for real-world use in Nigeria’s resource sector.

## Future Improvements
- Geo-spatial queries using PostGIS
- Data visualization dashboard
- Role-based access control
- Batch data processing
- Integration with GIS tools


## Author

Emmanuel Ulu
Cloud / DevOps Engineer




















