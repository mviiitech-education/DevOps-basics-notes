# Cloning a Private GitHub Repository to an EC2 Instance

## Prerequisites

1. **AWS EC2 Instance**: Ensure you have an EC2 instance running.
2. **SSH Access**: You should have SSH access to your EC2 instance.
3. **GitHub Account**: You need a GitHub account with access to the private repository.
4. **Git Installed**: Ensure Git is installed on your EC2 instance.

## Steps

[Follow this link](./../part-01-git/part-04.md){:target="\_blank"}

1. Generate SSH Key Pair
1. Add SSH Key to GitHub
1. Clone the Repository

### 4. Serve the Repository

To make the repository accessible via an IP address, you can use a simple HTTP server. Navigate to the cloned repository and start the server:

```sh
cd your-private-repo-path
# as per instruction run the application.
```

Ensure port number is open in your EC2 security group settings.

### 5. Access the Repository

Open a web browser and navigate to `http://your-ec2-ip`. You should see the contents of your repository.

## Conclusion

You have successfully cloned a private GitHub repository to your EC2 instance and made it accessible via an IP address.
