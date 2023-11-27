# Deploy Java Application on AWS 3-Tier Architecture

<img width="664" alt="aws 3 tier app" src="https://github.com/mericalp/llkk/assets/83503845/c82f1f10-8823-4620-b242-293822384456">

## Pre-Deployment
* Create Global AMI
  * AWS CLI
  * Cloudwatch agent
  * Install AWS SSM agent
* Create Golden AMI using Global AMI for Nginx application
  * Install Nginx
  * Push custom memory metrics to Cloudwatch.
* Create Golden AMI using Global AMI for Apache Tomcat application
  * Install Apache Tomcat
  * Configure Tomcat as Systemd service
  * Install JDK 11
  * Push custom memory metrics to Cloudwatch.
* Create Golden AMI using Global AMI for Apache Maven Build Tool
  * Install Apache Maven
  * Install Git
  * Install JDK 11
  * Update Maven Home to the system PATH environment variable

VPC Deployment:

<img width="758" alt="Screenshot 2023-11-26 at 8 41 23 PM" src="https://github.com/mericalp/llkk/assets/83503845/97c87c1c-a600-4b94-ad0d-5ad56a78da26">

Maven Build:

<img width="788" alt="Screenshot 2023-11-26 at 8 41 27 PM" src="https://github.com/mericalp/llkk/assets/83503845/8ced33b5-271e-4658-ae3e-ceb031b2c991">

3 Tier Arc:

<img width="789" alt="Screenshot 2023-11-26 at 8 41 31 PM" src="https://github.com/mericalp/llkk/assets/83503845/9766c79f-e6fb-4901-ba0d-337b42375188">

<img width="764" alt="Screenshot 2023-11-26 at 8 41 37 PM" src="https://github.com/mericalp/llkk/assets/83503845/93f1dcc1-bb53-47eb-8af0-4941a6b42d8f">
