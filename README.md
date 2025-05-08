# Creating IAM Users and Groups in AWS

## Project Overview
This guide demonstrates how to implement AWS identity management best practices by creating IAM users and groups with appropriate permissions. Following the principle of least privilege, this approach improves security by avoiding the use of the root account for daily operations.

## Technologies Used
- AWS Identity and Access Management (IAM)
- IAM Users
- IAM Groups
- IAM Policies
- AWS Management Console

## Implementation Steps

### Creating an IAM Group with Administrative Permissions
1. Logged in to the AWS Management Console
2. Navigated to the IAM service dashboard
3. Selected "User groups" from the left navigation panel
4. Created a new group named "admins"
5. Attached the "AdministratorAccess" policy to the group
6. Reviewed policy permissions and confirmed group creation

### Creating an IAM User
1. Navigated to the "Users" section in the IAM dashboard
2. Initiated the user creation process
3. Configured a username with AWS Management Console access
4. Set a custom password with appropriate security settings
5. Proceeded to permission assignment

### Assigning the User to a Group
1. Selected the "Add user to group" permission option
2. Added the new user to the previously created admin group
3. Reviewed the permissions inheritance structure
4. Confirmed user and group association

### Accessing the New IAM User Account
1. Copied the custom IAM user sign-in URL
2. Tested access using an incognito browser window
3. Successfully authenticated with the new credentials
4. Verified appropriate region selection (US East/N. Virginia)
5. Confirmed administrative permissions were correctly applied

## Challenges and Solutions

### Challenge: Determining Appropriate Permission Levels
**Issue:** Deciding between direct policy attachment and group-based permissions management.  
**Solution:** Implemented group-based permission management for scalability and easier administration of multiple users.

### Challenge: Secure Credential Management
**Issue:** Ensuring secure transfer of initial credentials to the user.  
**Solution:** Generated custom password and required password change at first login, testing the authentication flow in a separate private browser session.

## Screenshots

### IAM Group Creation
![Screenshot 2025-05-07 at 9 56 26 PM](https://github.com/user-attachments/assets/2e66bbcf-819a-4857-bba6-a00a236bfd6d)


### IAM User Configuration
![Screenshot 2025-05-07 at 10 01 13 PM](https://github.com/user-attachments/assets/80cef270-ac02-4078-a2b4-ea52a2cf2a77)
![Screenshot 2025-05-07 at 10 02 28 PM](https://github.com/user-attachments/assets/b30d26e5-d625-428f-9adb-5b11613aa116)


### Group Permission Assignment
![Screenshot 2025-05-07 at 9 56 45 PM](https://github.com/user-attachments/assets/449ab8dd-bc13-49e6-8618-f45b6dd87806)
![Screenshot 2025-05-07 at 10 02 07 PM](https://github.com/user-attachments/assets/711a51b8-a41f-4361-8cdc-efcc6f169533)


### Successful IAM User Login
![Screenshot 2025-05-07 at 10 02 41 PM](https://github.com/user-attachments/assets/67f62760-e3c6-48d7-ba27-72f174e1d147)
![Screenshot 2025-05-07 at 10 05 51 PM](https://github.com/user-attachments/assets/c566e61d-ae50-460e-8420-ca1d8f1ce230)
![Screenshot 2025-05-07 at 10 09 09 PM](https://github.com/user-attachments/assets/0d8bdcd3-2a21-484a-bd9c-86526a1206a2)
![Screenshot 2025-05-07 at 10 09 23 PM](https://github.com/user-attachments/assets/a3098114-0d4b-4dbc-bc8d-cbddc91297f1)


## Documentation

### Best Practices Implemented

#### Security Considerations
- **Principle of Least Privilege:** Created specific groups with appropriate permission sets
- **Root Account Protection:** Established IAM users for daily operations to avoid using the root account
- **Password Policies:** Implemented strong password requirements for the IAM user

#### Administration Efficiency
- **Group-Based Management:** Used groups to simplify permission management for multiple users
- **Documentation:** Created clear step-by-step procedures for recreating the setup
- **Testing:** Verified access and permissions before deployment

### Next Steps and Recommendations
- Create additional groups with more restricted permissions for non-administrative users
- Enable Multi-Factor Authentication (MFA) for enhanced security
- Set up IAM password policies to enforce password complexity requirements
- Implement regular access key rotation for programmatic access

## References
- [AWS IAM Best Practices](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html)
- [AWS IAM User Guide](https://docs.aws.amazon.com/IAM/latest/UserGuide/introduction.html)
