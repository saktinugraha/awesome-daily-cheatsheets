# AWS CLI Commands

## General

| Command                                  | Description                                                                                              |
|------------------------------------------|----------------------------------------------------------------------------------------------------------|
| `aws help`                               | Show AWS CLI help.                                                                                      |
| `aws --version`                          | Show the current AWS CLI version.                                                                       |
| `aws configure`                          | Configure AWS Key ID, AWS Secret, default region, and default output format for the AWS CLI.            |
| `aws configure --profile <profile_name>` | Configure using a specific profile name. Profiles are stored in `~/.aws/credentials` (Linux and MacOS). |

---

## EC2

**Note:** Specify a region for EC2 commands by configuring a default region (`aws configure`) or setting the `AWS_DEFAULT_REGION` environment variable.  
Example: `AWS_DEFAULT_REGION=us-east-1 aws ec2 describe-instances`

| Command                                                                                      | Description                                                                              |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| `aws ec2 describe-instances`                                                                 | Describe all instances in the current region.                                           |
| `aws ec2 describe-instances --instance-ids <instance_id_1> <instance_id_2>`                  | Describe specific instances by their IDs.                                               |
| `aws ec2 describe-instances --filters Name=<instance_name>`                                  | Filter and describe instances by name.                                                  |
| `aws ec2 start-instances --instance-ids <instance_id_1> <instance_id_2>`                     | Start previously stopped instances by their IDs.                                        |
| `aws ec2 stop-instances --instance-ids <instance_id_1> <instance_id_2>`                      | Stop running instances by their IDs.                                                   |
| `aws ec2 terminate-instances --instance-ids <instance_id_1> <instance_id_2>`                 | Terminate the specified instances by their IDs.                                         |

---

## S3

**Note:** The root directory of an S3 bucket is specified using the syntax: `s3://<bucket_name>`

| Command                                                                  | Description                                                                                   |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| `aws s3 ls`                                                              | List S3 objects and common prefixes under a prefix or all S3 buckets.                        |
| `aws s3 ls s3://<bucket_name>`                                           | List objects and common prefixes under a specified bucket and prefix.                        |
| `aws s3 mb s3://<bucket_name>`                                           | Create a specific S3 bucket.                                                                 |
| `aws s3 rb s3://<bucket_name>`                                           | Remove an empty specific S3 bucket by name.                                                  |
| `aws s3 mv <local_file_path> s3://<bucket_name>/<destination_file_path>` | Move a file from `local_file_path` to a specific bucket at `destination_file_path`.           |
| **Example:** `aws s3 mv text.txt s3://mybucket/text.txt`                 |                                                                                               |
| `aws s3 mv s3://<bucket_name_1> s3://<bucket_name_2> --recursive`        | Move all objects from `bucket_name_1` to `bucket_name_2`.                                     |
| `aws s3 sync <source> <target>`                                          | Sync all contents from `source` to `target`. Copies and updates missing or outdated files.   |
| **Examples:** `aws s3 sync . s3://mybucket`, `aws s3 sync s3://bucket_1 s3://bucket_2` |                                                        |
| `aws s3 sync <source> <target> --delete`                                 | Sync all contents from `source` to `target` and remove files in the target not in the source.|