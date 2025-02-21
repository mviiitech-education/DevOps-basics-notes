# Setting Up Jenkins on AWS EC2 Instance

## Prerequisites

- AWS account
- EC2 instance (Ubuntu)
- Security group with ports 22 (SSH) and 8080 (Jenkins) open

## Steps

1. **Launch EC2 Instance**

- Go to the AWS Management Console.
- Launch a new EC2 instance with Ubuntu AMI.
- Configure security group to allow SSH (port 22) and HTTP (port 8080).

2. **Connect to Your Instance**

- Use SSH to connect to your instance:
  ```sh
  ssh -i /path/to/your-key-pair.pem ubuntu@your-ec2-public-dns
  ```

3. **Install Java**

- Update the package index:
  ```sh
  sudo apt-get update
  ```
- Install Java:
  ```sh
  sudo apt-get install openjdk-21-jdk -y
  ```

4. **Install Jenkins**

- Add the Jenkins repository and key:
  ```sh
  sudo wget -O /usr/share/keyrings/jenkins-keyring.asc \
   https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key
  echo "deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
   https://pkg.jenkins.io/debian-stable binary/" | sudo tee \
   /etc/apt/sources.list.d/jenkins.list > /dev/null
  sudo apt-get update
  sudo apt-get install jenkins -y
  ```

5. **Start Jenkins**

- Start the Jenkins service:
  ```sh
  sudo systemctl start jenkins
  ```
- Enable Jenkins to start on boot:
  ```sh
  sudo systemctl enable jenkins
  ```

6. **Configure Jenkins**

- Open your web browser and navigate to `http://your-ec2-public-dns:8080`.
- Retrieve the initial admin password:
  ```sh
  sudo cat /var/lib/jenkins/secrets/initialAdminPassword
  ```
- Follow the on-screen instructions to complete the setup.

## Conclusion

You have successfully set up Jenkins on an AWS EC2 instance. You can now start creating and managing your Jenkins jobs.
