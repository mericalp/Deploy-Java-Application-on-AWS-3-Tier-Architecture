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
