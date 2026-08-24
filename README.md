Secure AWS EFS with EC2

This is a hands-on AWS project where I connected an Amazon EFS file system to an EC2 instance running Amazon Linux 2023.

I created the EFS file system, configured the mount target and security group, mounted EFS on the EC2 instance, and tested file access.

What I Used
AWS EC2
Amazon EFS
Amazon VPC
Security Groups
Amazon Linux 2023
Linux
Bash
Git
GitHub
What I Did
Created an EC2 instance using Amazon Linux 2023.
Created an Amazon EFS file system.
Configured the EFS mount target.
Configured the Security Group for NFS traffic on port 2049.
Connected to the EC2 instance using EC2 Instance Connect.
Mounted EFS on the EC2 instance using TLS.
Created, wrote, and read test files on the EFS storage.
Configured the EFS mount for persistent access.
Created a Bash script to verify the EFS mount.
Documented the setup and uploaded the project to GitHub.
EFS Mount

The EFS file system was mounted on the EC2 instance at:

/mnt/efs

I verified the mount using Linux commands and confirmed that the file system was accessible.

Security Configuration

The Security Group was configured to allow NFS traffic required for communication between the EC2 instance and EFS.

Protocol: TCP
Port: 2049
Service: NFS

The EFS file system policy was also configured to allow the required client access while using secure transport.

Testing

I tested the EFS connection by creating a file on the mounted file system:

echo "EFS working successfully" | sudo tee /mnt/efs/efs-test.txt

I then verified that the file was successfully created and accessible from the mounted EFS file system.

Outcome / Benefits
Successfully connected Amazon EFS to an EC2 instance for shared file storage.
Demonstrated how AWS compute and storage services work together.
Stored files on EFS instead of relying only on the EC2 instance's local storage.
Demonstrated scalable and persistent file storage using Amazon EFS.
Configured security controls to allow the required NFS communication between EC2 and EFS.
Verified that files could be created, written, and read successfully from the mounted EFS file system.
Gained practical hands-on experience with AWS EC2, EFS, VPC, Security Groups, Linux, and Bash.
Screenshots

Screenshots of the AWS configuration and verification steps are available in the screenshots folder.

EC2 Instance
EFS File System
EFS Mount Target
EFS Security Group
EFS Verification


