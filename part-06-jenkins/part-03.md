# Steps to Set Up Git Credential Using SSH Key in Jenkins

1. **Generate SSH Key Pair**

   - Open a terminal on your Jenkins server.
   - Run the following command to generate an SSH key pair:
     ```sh
     ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
     ```
   - Follow the prompts to save the key pair. By default, it will be saved in `~/.ssh/id_rsa`.

2. **Add SSH Key to Git Repository**

   - Copy the contents of the public key file (`~/.ssh/id_rsa.pub`).
   - Go to your Git repository hosting service (e.g., GitHub, GitLab, Bitbucket).
   - Navigate to the SSH keys section in your account settings.
   - Add a new SSH key and paste the copied public key.

3. **Configure Jenkins with SSH Key**

   - Open Jenkins in your web browser.
   - Go to `Manage Jenkins` > `Manage Credentials`.
   - Select the appropriate domain (e.g., `Global`).
   - Click on `Add Credentials`.
   - Choose `SSH Username with private key` as the kind.
   - Enter the username (e.g., `git`).
   - Select `Enter directly` and paste the contents of the private key file (`~/.ssh/id_rsa`).
   - Optionally, add a description for the credential.
   - Click `OK` to save the credential.

4. **Use SSH Credential in Jenkins Job**

   - Create or configure a Jenkins job.
   - In the job configuration, go to the `Source Code Management` section.
   - Select `Git` as the repository type.
   - Enter the repository URL (use the SSH URL, e.g., `git@github.com:username/repo.git`).
   - Under `Credentials`, select the SSH credential you added earlier.
   - Save the job configuration.

5. **Test the Configuration**
   - Trigger a build for the Jenkins job.
   - Check the build logs to ensure that Jenkins is able to clone the repository using the SSH key.

By following these steps, you can set up Git credentials using an SSH key in Jenkins.
