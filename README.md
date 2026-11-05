Highly Available Web Application using AWS

About the Project

I created this project to understand how a web application can be hosted on AWS and how incoming traffic can be handled using a Load Balancer.

In this project, I used EC2 instances to host a simple website and configured an Application Load Balancer to distribute incoming traffic. I also used an Auto Scaling Group to manage the EC2 instances.

AWS Services Used

- EC2: Used to host the website.
- Application Load Balancer: Distributes incoming traffic between EC2 instances.
- Target Group: Connects the Load Balancer to EC2 instances and checks their health.
- Auto Scaling Group: Maintains the required number of EC2 instances.
- Launch Template: Contains the configuration used to launch instances.
- CloudWatch: Used to monitor CPU utilization.
- Internet Gateway: Allows internet connectivity.

Project Configuration

- Region: Asia Pacific (Sydney)
- Operating System: Amazon Linux 2023
- Instance Type: t3.micro
- Web Server: Nginx
- Load Balancer: HA-WebApp-ALB
- Target Group: HA-TG-1
- Auto Scaling Group: Desired capacity – 2
- Launch Template: HA-WebApp-LT

What I Did

1. Created EC2 instances and installed Nginx.
2. Hosted a simple web page on the instances.
3. Created a Target Group and configured health checks.
4. Created an Application Load Balancer.
5. Created a Launch Template and Auto Scaling Group.
6. Configured the Auto Scaling Group to maintain two instances.
7. Checked the target health and accessed the website through the Load Balancer.
8. Monitored CPU utilization using CloudWatch.

Project Output

The website was successfully accessible through the Application Load Balancer.

Website output: My AWS Web Application

What I Learned

While doing this project, I got practical experience with EC2, Load Balancer, Target Groups, Auto Scaling Groups and CloudWatch. I also understood how these services work together when hosting a web application on AWS.

## Architecture Diagram

```mermaid
flowchart TD
    A[Internet Users] --> B[Application Load Balancer]
    B --> C[Target Group]
    C --> D[EC2 Instance 1]
    C --> E[EC2 Instance 2]
    F[Auto Scaling Group] --> D
    F --> E
    G[CloudWatch] --> F

## project Screenshots
