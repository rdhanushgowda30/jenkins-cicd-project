<h1 align="center">CI/CD Pipeline Automation using Jenkins, Docker & AWS EC2</h1>

<p align="center">
Automated Continuous Integration and Deployment Pipeline using Jenkins, Docker, GitHub Webhooks, Apache Web Server, and AWS EC2.
</p>

<hr>

<h2>📌 Project Overview</h2>

<p>
This project demonstrates the implementation of a Continuous Integration (CI) pipeline using Jenkins, Docker, GitHub, and AWS EC2.
The Jenkins server is deployed inside a Docker container running on an AWS EC2 Ubuntu instance. GitHub repositories are integrated with Jenkins, and GitHub Webhooks are configured to automatically trigger builds whenever code changes are pushed to the repository.
</p>

<p>
A static web application is hosted on an Apache Web Server running on AWS EC2, showcasing automated build execution and deployment workflows.
</p>

<hr>

<h2>🏗️ Architecture</h2>

<pre>
Developer
    │
    ▼
GitHub Repository
    │
    ▼
GitHub Webhook
    │
    ▼
Jenkins (Docker Container)
    │
    ▼
AWS EC2 Ubuntu Instance
    │
    ▼
Apache Web Server
    │
    ▼
Static Website Deployment
</pre>

<hr>

<h2>🛠️ Technologies Used</h2>

<ul>
<li>Jenkins</li>
<li>Docker</li>
<li>AWS EC2</li>
<li>Ubuntu Server</li>
<li>Git</li>
<li>GitHub</li>
<li>GitHub Webhooks</li>
<li>Apache HTTP Server</li>
</ul>

<hr>

<h2>🎯 Key Features</h2>

<ul>
<li>Deployed Jenkins inside a Docker container on AWS EC2.</li>
<li>Integrated GitHub repositories with Jenkins.</li>
<li>Configured GitHub Webhooks for automatic build triggering.</li>
<li>Implemented Continuous Integration (CI) workflow.</li>
<li>Automated build execution on code commits.</li>
<li>Managed Docker containers and Jenkins jobs.</li>
<li>Performed Linux server administration on Ubuntu.</li>
<li>Hosted a static website using Apache Web Server.</li>
<li>Used Git and GitHub for version control and collaboration.</li>
</ul>

<hr>

<h2>⚙️ AWS EC2 Setup</h2>

<p>Launch an Ubuntu EC2 instance and allow the following ports:</p>

<ul>
<li>22 - SSH</li>
<li>80 - HTTP</li>
<li>8080 - Jenkins</li>
</ul>

<hr>

<h2>🐳 Docker Installation</h2>

<pre>
sudo apt update
sudo apt install docker.io -y
sudo systemctl start docker
sudo systemctl enable docker
docker --version
</pre>

<hr>

<h2>🚀 Jenkins Deployment Using Docker</h2>

<pre>
docker pull jenkins/jenkins:lts

docker run -d \
--name jenkins-server \
-p 8080:8080 \
-p 50000:50000 \
-v jenkins_home:/var/jenkins_home \
jenkins/jenkins:lts
</pre>

<hr>

<h2>🔗 GitHub Integration</h2>

<ul>
<li>Connected GitHub repository with Jenkins.</li>
<li>Configured repository URL and branch details.</li>
<li>Enabled automatic source code polling and build execution.</li>
</ul>

<hr>

<h2>📡 GitHub Webhook Configuration</h2>

<p><b>Webhook URL:</b></p>

<pre>
http://3.237.98.56:8080/github-webhook/
</pre>

<p><b>Event:</b></p>

<pre>
Just the push event
</pre>

<hr>

<h2>🔄 CI Workflow</h2>

<pre>
Code Commit
    │
    ▼
GitHub Repository
    │
    ▼
Webhook Trigger
    │
    ▼
Jenkins Build
    │
    ▼
Build Validation
    │
    ▼
Deployment
    │
    ▼
Apache Web Server
    │
    ▼
Live Website
</pre>

<hr>

<h2>🌐 Apache Web Server Setup</h2>

<pre>
sudo apt update
sudo apt install apache2 -y
sudo systemctl start apache2
sudo systemctl enable apache2
</pre>

<p>Deploy website files to:</p>

<pre>
/var/www/html/
</pre>

<hr>

<h2>📂 Project Structure</h2>

<pre>
CI-CD-Pipeline-Automation/
│
├── README.md
├── screenshots/
│   ├── jenkins-dashboard.png
│   ├── build-success.png
│   ├── webhook-config.png
│   ├── docker-container.png
│   └── website-hosted.png
│
├── website/
│   ├── index.html
</pre>


<h2>📚 Learning Outcomes</h2>

<ul>
<li>Continuous Integration (CI) implementation.</li>
<li>Jenkins administration and job configuration.</li>
<li>Docker container deployment and management.</li>
<li>AWS EC2 provisioning and configuration.</li>
<li>GitHub Webhook integration.</li>
<li>Linux server administration.</li>
<li>Apache web server configuration.</li>
<li>Version control using Git and GitHub.</li>
</ul>

<hr>

<h2>👨‍💻 Author</h2>

<p>
Developed as a hands-on DevOps project to demonstrate CI/CD automation using Jenkins, Docker, GitHub, and AWS Cloud Infrastructure.
</p>
