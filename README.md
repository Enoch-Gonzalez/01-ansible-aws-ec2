# Ansible EC2 Instances Deployment

This Ansible project automates the deployment of EC2 instances on AWS and configures each instance with an Nginx server. Additionally, a web application is deployed on these instances.

## Prerequisites

Before getting started, ensure you have the following prerequisites:

- [Ansible](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html) installed locally.
- [boto2](https://boto.cloudhackers.com/en/latest/) and [boto3](https://boto3.amazonaws.com/v1/documentation/api/latest/index.html) libraries installed.
- An AWS account with necessary permissions, including access key, secret key, and a PEM key for SSH access.
- Git installed on your machine.

## Getting Started

Follow these steps to set up the project on your local machine:

1. Clone the Repository

- Clone this repository to your local machine using Git:

    ```bash
    git clone https://github.com/Enoch-Gonzalez/01-ansible-aws-ec2.git
    ```

    ```bash
    cd /01-ansible-aws-ec2
    ```

2. Configuration

Navigate to the project directory and configure the necessary files:

- Update group_vars/tag_Name_Ansible with your AWS credentials.
- Customize any other variables or configurations in the playbook (ec2_playbook.yaml) or relevant files based on your requirements. If you wish to have the latest AWS Red Hat image make sure to copy it form the EC2 Dashboard and paste it in the ec2_playbook.yaml.

3. Execute the Playbook

- In your local terminal, run the Ansible playbook to provision EC2 instances, deploy Nginx, and the web app:

    ```bash
    ansible-playbook ec2_playbook.yaml
    ```

- Upon successful execution, the playbook will output a public IP. Access the deployed application via the provided IP address. Click on the app's logo for an Easter egg.

- A prompt will be waiting in the terminal so that ansible can eliminate the resources created.

### Important Notes

    - AWS Charges: Be aware that running this playbook may incur AWS charges. Ensure to terminate all resources created by the playbook to avoid unexpected charges.

    - Resource Cleanup: Use caution when running the termination task. It will delete all AWS resources provisioned by this playbook.

### Disclaimer

The creator of this repository is not responsible for any AWS charges incurred. Users must ensure proper resource cleanup by terminating all resources created by this playbook.

## License

This project is licensed under the MIT License - see the LICENSE file for details.
