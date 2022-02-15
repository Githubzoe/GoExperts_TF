#Repo for GoExperts Terraform files.

If you want to construct all your infrastructure, e.g. frontend, backend, lambda, etc., you should put your tf files here.
1.  **DO NOT** operate on the `main` branch directly. Checkout your own branch instead, e.g. feature/new_terraform.
2.  Put different files to the 3 directories:
    - `modules`: resusable terraform modules.
    - `applications`: deployment files.
    - `cicd`: pipeline files, e.g. Jenkinsfile.

One example: 

```bash
.
├── applications
│   ├── aws_api_lambda
│   ├── aws_backend
│   ├── aws_frontend
│   ├── backend-lock
│   ├── gcp_backend
│   ├── gcp_frontend
│   └── lambda_backend
├── cicd
│   ├── Jenkinsfile.aws_fe
│   └── Jenkinsfile.lambda
└── modules
    ├── aws-dynamodb-lock
    ├── aws-ecs-alb-asg
    ├── aws-s3-cloudfront
    ├── gcp-gcs
    ├── gcp-gke-vpc
    └── lambda-api-gateway
```
