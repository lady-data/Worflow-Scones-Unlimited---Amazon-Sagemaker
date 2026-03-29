# ML Workflow with AWS SageMaker, Lambda & Step Functions
 
Serverless machine learning workflow orchestrating model training and inference using Amazon SageMaker, Lambda, and Step Functions.
 
## Overview
 
This project builds a production-style ML pipeline for Scones Unlimited, a fictional bakery delivery company. The workflow automates image classification using a serverless architecture: SageMaker handles model training and inference, Lambda functions process inputs/outputs, and Step Functions orchestrate the entire pipeline.
 
## Architecture
 
```
Input Image → Lambda (preprocessing) → SageMaker Endpoint (inference) → Lambda (postprocessing) → Output
                                    ↑
                        Step Functions (orchestration)
```
 
## Components
 
- **Amazon SageMaker** — Model training and real-time inference endpoint
- **AWS Lambda** — Serverless functions for data preprocessing and result handling
- **AWS Step Functions** — Workflow orchestration connecting all services
- **Amazon S3** — Data and model artifact storage
 
## Repository Structure
 
```
├── Notebook.ipynb            # Full pipeline notebook
├── Lambda.py                 # Lambda function code
├── Workflow.json             # Step Functions workflow definition
├── Execution event history.PNG
├── Execution output.PNG
└── Success.PNG
```
