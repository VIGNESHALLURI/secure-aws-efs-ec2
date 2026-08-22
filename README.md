# Secure AWS EFS with EC2

This is a hands-on AWS project where I connected an Amazon EFS file system to an EC2 instance running Amazon Linux 2023.

I created the EFS file system, configured the mount target and security group, mounted EFS on the EC2 instance, and tested file access.

## What I used

- AWS EC2
- Amazon EFS
- Amazon VPC
- Security Groups
- Amazon Linux 2023
- Linux
- Bash
- Git and GitHub

## What I did

1. Created an EC2 instance using Amazon Linux 2023.
2. Created an Amazon EFS file system.
3. Configured the EFS mount target.
4. Configured the Security Group for NFS traffic on port 2049.
5. Connected to the EC2 instance using EC2 Instance Connect.
6. Mounted EFS on the EC2 instance.
7. Created and tested files on the EFS storage.
8. Created a Bash script to verify the EFS mount.
9. Uploaded the project to GitHub.

## How it works

The EC2 instance accesses the EFS file system using NFS.

```text
EC2 Instance
    |
    | NFS - TCP 2049
    |
    v
Amazon EFS
