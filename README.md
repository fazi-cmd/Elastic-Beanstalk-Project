# 🚀 AWS Elastic Beanstalk Learning Journey & Project

Welcome to my AWS Elastic Beanstalk learning repository! 

This repository documents my hands-on journey in mastering AWS Elastic Beanstalk. My goal with this project was to move beyond theory and actually deploy, manage, and understand the infrastructure behind a modern application. I am highly eager to learn, and this is a reflection of my continuous progress in cloud computing and DevOps concepts.

## 📚 What I Have Learned

Through this project, I explored the core concepts of AWS Elastic Beanstalk and compared its deployment models.

### 1. Deployment Modes Explored
*   **Standard Mode:** I learned that this is best for single or low-traffic apps. It provides full instance-level access and is perfect for standard web servers. It also supports free-tier eligible instances, making it great for learning.
*   **Cluster Mode (New):** I explored this mode to understand how Elastic Beanstalk scales for larger workloads. It is powered by Amazon EKS (Kubernetes) and is cost-effective at scale, ideal for multiple apps sharing infrastructure.

### 2. IAM Roles & Security
*   Created and configured specific IAM roles:
    *   `eb-compute-tester`: The instance profile role attached to the EC2 instances.
    *   `eb-environment-tester`: The service role allowing Elastic Beanstalk to manage the necessary AWS resources.
*   Learned the importance of granting least-privilege permissions and using temporary credentials.

### 3. Docker & Platform Management
*   Deployed a containerized application using a `docker-compose.yml` file.
*   Utilized the `eb init` and `eb create` CLI commands to launch the environment directly from the terminal.
*   Learned how Elastic Beanstalk packages the application, uploads it to Amazon S3, and deploys it to the Docker platform running on 64-bit Amazon Linux 2023.

---

## 🛠️ Project: Flask App Deployment

For practical application, I deployed a sample Flask application using the **Docker platform**.

### Project Details:
*   **Application Name:** `flask-app` / `my-store-eb`
*   **Environment Name:** `Flask-app-env` / `eb-environment-tester`
*   **Platform:** Docker running on 64bit Amazon Linux 2023/4.13.11
*   **Instance Type:** `t3.micro` (used for cost-efficiency during learning)
*   **Region:** `us-west-2` (Oregon)

### The Process (CLI & Console):
1.  Navigated to the project directory and created the `docker-compose.yml`.
2.  Initialized the Elastic Beanstalk application using `eb init`.
3.  Created the environment using `eb create --single --instance_type t3.micro`.
4.  Monitored the deployment via the AWS Management Console and the `eb status` CLI command.
5.  Successfully achieved a **Green** health status and a **Ready** environment state.

*(Note: The `docker-compose.yml` file used for this project is included in this repository for reference).*

---

## 📸 Project Screenshots & Evidence

Here is a visual walkthrough of my learning and deployment process:

### IAM & Security Configuration
*Setting up the necessary roles for the Elastic Beanstalk environment and EC2 instances.*


### Deployment Modes
*Exploring the Standard vs. Cluster deployment options in the new AWS Console.*

### Environment Overview (AWS Console)
*Successfully deployed and healthy environment showing the platform and application details.*

### CLI Deployment & Status
*Using the AWS CLI (EB CLI) to initialize, create, and monitor the environment, proving my comfort with terminal-based cloud management.*


<img width="1920" height="911" alt="Screenshot from 2026-10-23 21-27-49" src="https://github.com/user-attachments/assets/80fce638-074e-4958-b591-4361a1507c29" />


<img width="1920" height="911" alt="Screenshot from 2026-10-23 21-28-47" src="https://github.com/user-attachments/assets/2e0a37f1-110f-4adf-a729-2ae45cfee949" />



<img width="1920" height="911" alt="Screenshot from 2026-10-23 21-28-57" src="https://github.com/user-attachments/assets/da5e33f4-fdba-4836-8b7a-53e05f812f02" />




<img width="1920" height="911" alt="Screenshot from 2026-10-23 21-49-02" src="https://github.com/user-attachments/assets/99084108-b8ce-4e3a-994d-18bba4c43d35" />



<img width="1012" height="722" alt="Screenshot from 2026-10-23 22-11-20" src="https://github.com/user-attachments/assets/7a5d3fdb-db65-45bc-b897-b93eafe035f1" />




<img width="1012" height="722" alt="Screenshot from 2026-10-23 22-13-33" src="https://github.com/user-attachments/assets/f38b64ba-7752-40fe-a960-0f671ed704f9" />



## 🔭 What's Next? (Continuous Learning)

I am incredibly eager to keep learning and growing in the AWS ecosystem. My next goals include:
*   [ ] Implementing CI/CD pipelines (AWS CodePipeline) to automate deployments.
*   [ ] Learning how to use `.ebextensions` to customize the environment.
*   [ ] Exploring advanced networking and Load Balancers (ALB) with Elastic Beanstalk.
*   [ ] Diving deeper into EKS since Cluster mode utilizes it.

**Thank you for visiting my repository!** I am always open to feedback, mentorship, and opportunities to learn more about Cloud Engineering and DevOps. Feel free to reach out or connect!
