# AWS CI/CD Pipeline for Automated Web Deployment

A hands-on DevOps project demonstrating automated web application deployment using AWS developer tools, Git, and an Ubuntu EC2 instance running NGINX.

## Project Overview

This project implements a CI/CD pipeline to validate application files, package deployment artifacts, and deploy a website to an EC2 instance. It demonstrates how cloud services can work together to automate application delivery and reduce manual deployment steps.

## Architecture

```text
AWS CodeCommit
      |
      v
AWS CodePipeline
      |
      v
AWS CodeBuild
      |
      v
Amazon S3 (Build Artifacts)
      |
      v
AWS CodeDeploy
      |
      v
Amazon EC2 (Ubuntu + NGINX)
      |
      v
Web Application
```

## AWS Services Used

- **AWS CodeCommit:** Stores the application source code.
- **AWS CodePipeline:** Orchestrates the source, build, and deployment stages.
- **AWS CodeBuild:** Validates required files and prepares build artifacts.
- **Amazon S3:** Stores the packaged deployment artifacts.
- **AWS CodeDeploy:** Automates deployment to the EC2 instance.
- **Amazon EC2:** Hosts the web application.
- **NGINX:** Serves the deployed HTML page.

## Technologies

- AWS
- Linux (Ubuntu)
- Git and GitHub
- HTML
- YAML
- Bash scripting
- NGINX
- CI/CD automation

## Repository Structure

```text
aws-codebuild-artifacts-demo/
├── index.html
├── buildspec.yml
├── appspec.yml
└── scripts/
    ├── install_nginx.sh
    └── start_nginx.sh
```

### Key Files

| File | Purpose |
|---|---|
| `index.html` | Web application and portfolio page |
| `buildspec.yml` | Defines build commands and output artifacts |
| `appspec.yml` | Defines deployment files and lifecycle hooks |
| `scripts/install_nginx.sh` | Installs NGINX during deployment |
| `scripts/start_nginx.sh` | Starts or restarts the NGINX service |

## How the Pipeline Works

1. Application code is stored in AWS CodeCommit.
2. CodePipeline detects source changes and starts the workflow.
3. CodeBuild checks the required deployment files and packages the application artifacts.
4. Build artifacts are stored in Amazon S3.
5. CodeDeploy deploys the files to the target EC2 instance.
6. NGINX serves the updated website to visitors.

## Key Learning Outcomes

- Building and configuring an AWS CI/CD pipeline.
- Managing source code with Git.
- Writing build specifications and deployment manifests in YAML.
- Packaging and storing build artifacts in Amazon S3.
- Automating deployments to an EC2 instance.
- Using Linux shell scripts to manage a web server.
- Troubleshooting CI/CD build and deployment issues.

## Live Demo

**Website:** http://16.171.253.43

*The demo depends on the EC2 instance being running and publicly accessible.*

## GitHub Repository

[View the project source code](https://github.com/khushbakht-student/aws-codebuild-artifacts-demo)

## Author

**Khush Bakht**  
Aspiring DevOps Engineer

- [GitHub Profile](https://github.com/khushbakht-student)
- [LinkedIn Profile](https://www.linkedin.com/in/khush-bakht-9a0b17198/)

---

This project was created as a hands-on learning exercise to develop practical skills in AWS DevOps, CI/CD automation, Linux administration, and cloud deployment.
