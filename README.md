
# AWS Envirnoment

Building quick AWS environment covering all aspects of Devops and DevSecops.

# Environment Variable Setup
- Step 1: Create .env

- copy the template:
cp .env.example .env

Step 2: Update values in .env

# AWS / ECR Configuration

- AWS_ACCOUNT_ID=your-aws-account-id 
- AWS_REGION=your-region (e.g. us-east-1)

# Image Tag (from GitHub Actions) 
- IMAGE_TAG=<"enter your github commit id"> (or take it from ECR)

# Important Notes
- .env is NOT committed (listed in .gitignore)
- Each team member uses their own AWS account
- Do NOT store AWS secrets here


# Running the Application (Docker Compose)

# Docker Compose Run

Step 1: Login to ECR locally:

- Before running docker compose, make sure to login to your AWS ECR locally

- aws ecr get-login-password --region <REGION> | \
- docker login --username AWS --password-stdin <AWS_ACCOUNT_ID>.dkr.ecr.<REGION>.amazonaws.com

Step 2: Pull images
- docker-compose pull

Step 3: Start the Application:
- docker-compose up

# Access the application

- Frontend → http://localhost:8080
- Backend API → http://localhost:3000/api/db

## Screenshots

![App Screenshot](/images/AWS-Environment.jpg)

## Acknowledgements

## License

[MIT](https://choosealicense.com/licenses/mit/)




