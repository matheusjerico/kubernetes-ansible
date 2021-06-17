# Kubernetes, Ansible e AWS

This project have a goal to provisioning and installing the Kubernetes cluster with Ansible and AWS.

## Project steps
- Provisioning => Create EC2 instances for our cluster;
- Install_k8s => Create Kubernetes Cluster.
- Deploy_app => Deploy two applications
- Extra =>  hehehehe

## Install

Use the package manager [pip](https://pip.pypa.io/en/stable/) to install ansible.

```bash
pip install ansible
```

#### Provisioning
We need the AWS credentials configured to execute this playbook. Go to inside `provisioning` directory and execute:
```bash
ansible-playbook -i hosts main.yml
```

#### Instal Kubernetes
We need the AWS credentials configured to execute this playbook. Go to inside `install_k8s` directory and execute:
```bash
ansible-playbook -i aws_ec2.yml main.yml
```

#### Deploy App
We need the AWS credentials configured to execute this playbook. Go to inside `deploy_app` directory and execute:

- Deploy app version 1.0.0: go to insede `deploy_app/deploy-app-v1`:
```bash
ansible-playbook -i aws_ec2.yml main.yml
```

- Deploy app version 2.0.0: go to insede `deploy_app/deploy-app-v2`:
```bash
ansible-playbook -i aws_ec2.yml main.yml
```

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License
[MIT](https://choosealicense.com/licenses/mit/)