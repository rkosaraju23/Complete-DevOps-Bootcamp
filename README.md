# Complete-DevOps-Bootcamp
DevOps Roadmap

<img width="800" height="891" alt="image" src="https://github.com/user-attachments/assets/d3c20cd1-ef06-4fe2-b30b-f91fec67d31f" />

1. Complete DevOps Learning Roadmap
Phase	What to learn	Recommended tools	Estimated time
1	Linux fundamentals	Ubuntu, Bash	2–3 weeks
2	Networking fundamentals	TCP/IP, DNS, HTTP, SSH	1–2 weeks
3	Git and version control	Git, GitHub	1 week
4	Scripting	Bash, Python basics	2–3 weeks
5	CI/CD pipelines	Jenkins, GitHub Actions	2–3 weeks
6	Containers	Docker, Docker Compose	2 weeks
7	Cloud computing	AWS or Azure	3–4 weeks
8	Infrastructure as Code	Terraform	2–3 weeks
9	Kubernetes	Kubernetes, Helm	3–4 weeks
10	Monitoring and logging	Prometheus, Grafana	1–2 weeks
11	Security and DevSecOps	IAM, secrets, vulnerability scanning	1–2 weeks
12	Projects and interview preparation	Real-world projects	3–4 weeks


Estimated total: Around 4–6 months at a consistent pace of 2–3 hours daily. Your timeline will depend on your current technical knowledge and practice.
2. What to Learn in Each Phase
Phase 1: Linux and Networking
Start here, even if you have no IT experience.

Linux topics:
- Basic commands: ls, cd, pwd, cp, mv, rm
- File permissions: chmod, chown
- Users and groups
- Processes: ps, top, kill
- Services: systemctl
- Logs: journalctl
- SSH and remote server access
- Bash scripting
Networking topics:
- IP addresses and subnets
- DNS
- TCP/IP
- HTTP and HTTPS
- Ports and firewalls
- SSH
- Load balancers
Practice project: Write a Bash script that checks CPU usage, memory usage, disk space, and server status.
Phase 2: Git and GitHub
Learn how developers collaborate and manage code.

Important commands:
git init
git clone
git add .
git commit -m "Initial commit"
git push
git pull
git branch
git merge

Learn branches, pull requests, merge conflicts, and repository management.

Practice project: Create a GitHub repository for your Linux scripts and document each script.
Phase 3: Cloud Computing — AWS
Choose one cloud platform first. I recommend starting with Amazon Web Services (AWS).

Learn these services:
AWS service	Purpose
EC2	Virtual servers
IAM	Access and permissions
S3	Object storage
VPC	Cloud networking
ELB	Load balancing
Auto Scaling	Automatically adjust server capacity
RDS	Managed relational databases
CloudWatch	Monitoring and logs


Start with EC2, IAM, S3, and VPC before moving to more advanced services.

Official resource: AWS Skill Builder

Practice project: Deploy a simple website on an EC2 instance and configure secure access.
Phase 4: Docker
Docker helps you package applications and their dependencies into containers.

Learn:
- Images and containers
- Dockerfiles
- Docker commands
- Volumes and networks
- Docker Hub
- Docker Compose
- Container troubleshooting
Official resource: Docker Get Started

Practice project: Build a Docker image for a simple web application and run it locally.
Phase 5: CI/CD
CI/CD automates application testing, building, and deployment.

Learn one tool first:
- GitHub Actions
- Jenkins
Understand this workflow:

Developer pushes code → Automated tests → Build Docker image → Push image to registry → Deploy application

Official resources:
- GitHub Actions Documentation
- Jenkins Documentation
Practice project: Build a pipeline that automatically tests your application and builds a Docker image whenever code is pushed to GitHub.
Phase 6: Terraform and Ansible
These tools help automate infrastructure and server configuration.

Terraform: Learn providers, resources, variables, modules, state, and infrastructure provisioning.

Ansible: Learn inventories, playbooks, variables, roles, and server configuration.

Official resources:
- Terraform Tutorials
- Ansible Documentation
Practice project: Use Terraform to create cloud infrastructure and Ansible to configure a Linux server.
Phase 7: Kubernetes
Learn Kubernetes after you understand Docker and basic cloud networking.

Focus on:
- Kubernetes architecture
- Pods and Deployments
- Services
- Namespaces
- ConfigMaps and Secrets
- Persistent storage
- Ingress
- Helm
- Scaling and troubleshooting
Official resource: Kubernetes Tutorials

Practice project: Deploy a containerized application to a local Kubernetes cluster, expose it through a Service, and configure replicas.
Phase 8: Monitoring and DevSecOps
A DevOps engineer must understand what happens after deployment.

Learn:
- Prometheus for metrics
- Grafana for dashboards
- Centralized logging
- Alerts and incident troubleshooting
- IAM and least-privilege access
- Secrets management
- Container image scanning
- Backup and recovery
Official resources:
- Prometheus Documentation
- Grafana Documentation
3. Six-Month DevOps Study Plan
Here is a practical schedule if you can study for approximately 2–3 hours per day.
Month	Main focus	Expected outcome
Month 1	Linux, networking, Git	Manage Linux systems and use Git confidently
Month 2	Bash, Python basics, AWS	Automate simple tasks and deploy a basic cloud application
Month 3	Docker, CI/CD	Containerize an application and automate its build
Month 4	Terraform, Ansible	Provision and configure infrastructure using code
Month 5	Kubernetes, Helm	Deploy and troubleshoot containerized applications
Month 6	Monitoring, security, projects, interviews	Build an end-to-end portfolio and prepare for interviews


The sequence is a guide, not a deadline. Spend more time on Linux, networking, or scripting if those fundamentals are still difficult.
4. Three Projects to Put on Your Resume
Don't just complete tutorials. Build projects that demonstrate how the tools work together.

Project 1: Automated CI/CD Pipeline
- Store application code on GitHub.
- Use GitHub Actions to run tests.
- Build a Docker image.
- Publish the image to a container registry.
- Deploy the application to a test environment.
Project 2: AWS Infrastructure Automation
- Create cloud infrastructure using Terraform.
- Configure access permissions with IAM.
- Deploy an application to AWS.
- Configure monitoring and alerts.
- Document the architecture and cleanup procedure.
Project 3: Kubernetes Deployment and Monitoring
- Deploy a containerized application to Kubernetes.
- Configure Services and replicas.
- Manage configuration and secrets securely.
- Set up Prometheus and Grafana.
- Document troubleshooting steps and recovery procedures.
For every project, publish a README, architecture diagram, setup instructions, screenshots where useful, and a description of the problems you solved.
5. Free DevOps Learning Resources
Resource	Best for	Link
Linux Journey	Linux fundamentals	Linux Journey
Pro Git	Git and version control	Pro Git Book
AWS Skill Builder	Cloud fundamentals	AWS Skill Builder
Docker Docs	Containers	Docker Documentation
HashiCorp Developer	Terraform	Terraform Tutorials
Kubernetes Docs	Container orchestration	Kubernetes Tutorials
Roadmap reference	Complete learning path	DevOps Roadmap 2026 on GitHub
