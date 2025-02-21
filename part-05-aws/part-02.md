# How to Create an IAM User and How to Use It

## Step 1: Sign in to the AWS Management Console

1. Open the AWS Management Console at https://aws.amazon.com/console/.
2. Sign in with your AWS account credentials.

## Step 2: Navigate to the IAM Console

1. In the AWS Management Console, navigate to the IAM (Identity and Access Management) service.
2. You can find IAM under the "Security, Identity, & Compliance" section or by searching for "IAM" in the search bar.

## Step 3: Create a New IAM User

1. In the IAM dashboard, click on "Users" in the left-hand navigation pane.
2. Click the "Add user" button.
3. Enter a username for the new user.
4. Select the type of access for the user:
   - **Programmatic access**: Provides access to the AWS API, CLI, SDK, and other development tools.
   - **AWS Management Console access**: Provides access to the AWS Management Console.
5. Click the "Next: Permissions" button.

## Step 4: Set Permissions for the IAM User

1. Choose how you want to set permissions for the user:
   - **Attach existing policies directly**: Select from existing policies to attach to the user.
   - **Add user to group**: Add the user to one or more existing groups with predefined permissions.
   - **Copy permissions from existing user**: Copy permissions from an existing user.
   - **Attach policies directly**: Create a custom policy for the user.
2. After setting the permissions, click the "Next: Tags" button.

## Step 5: Add Tags (Optional)

1. Add any tags you want to associate with the user. Tags are key-value pairs that can help you manage and organize your AWS resources.
2. Click the "Next: Review" button.

## Step 6: Review and Create the User

1. Review the user details and permissions.
2. Click the "Create user" button.

## Step 7: Download the User Credentials

1. After the user is created, you will see a confirmation page with the user's access credentials.
2. Download the `.csv` file containing the user's access key ID and secret access key.
3. Store the credentials securely, as you will not be able to view the secret access key again.

## Step 8: Use the IAM User Credentials

1. **For AWS Management Console Access**:

   - Provide the user with the sign-in URL and their username and password.
   - The user can sign in to the AWS Management Console using these credentials.

2. **For Programmatic Access**:
   - Use the access key ID and secret access key to configure the AWS CLI, SDK, or other development tools.
   - Example for configuring AWS CLI:
     ```sh
     aws configure
     ```
     Follow the prompts to enter the access key ID, secret access key, default region, and output format.

## Step 9: Manage and Monitor the IAM User

1. Regularly review and update the user's permissions as needed.
2. Monitor the user's activity using AWS CloudTrail and other monitoring tools.
3. Rotate the user's access keys periodically to enhance security.
