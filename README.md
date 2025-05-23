# DevOps / SRE Task

### Premisses:
- Use Terraform as IaaC. Must follow the terraform best practices.
- Use Ansible to configure host services.
- Use the smallest instances; free tier is encouraged but not mandatory.
- Docker logs must be delivered to Cloudwatch.
- Deliver it to a git repository (Github for example).
- Please ensure that you can explain the steps followed and the reasoning behind the technical decisions made. We discourage the use of generative AI for this task, as the purpose is to evaluate your thought process and understanding.

- Provide a **README.md** with instructions to reproduce and include to the **README.md** how did you come up with the solution (Google, Books, Manual, Stackoverflow). The source of your information is welcome.

### What to deliver:
**Using Terraform:**
```
- VPC 10.161.0.0/24.
- Adjust subnets and networking following best practices.
- 3 EC2 instances without public access.
- 1 EC2 instance for jumphost (bastion host) to access the other instances.
- The ALB should route traffic to port 80 on each EC2 instance. Each instance should run Nginx with a basic /health endpoint configured for the ALB’s health checks.
- Create the relevant IAM roles and permissions for EC2 and Cloudwatch access.
```

**Using Ansible:**
```
- Deploy and configure an Nginx Docker container on each private EC2 instance.
- Each nginx instance must have a different index.html (e.g. Hello, server1; Hello, server2; Hello, server3). Use Jinja2.
```
For further clarifications, please contact the recruitment contact.
