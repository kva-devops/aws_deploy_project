# aws_deploy_projet
Dynamic Inventory AWS

Customization AmazonLinux host for dynamic control inventory file in AWS

1. See documentation:
https://docs.ansible.com/ansible/2.9/user_guide/intro_dynamic_inventory.html#inventory-script-example-aws-ec2

2. See pip version and install python and pip
pip --version
curl -O https://bootstrap.pypa.io/get-pip.py
sudo yum install python3
python3 get-pip.py
pip --version

3. Change PYTHONPATH
export PYTHONPATH=/home/ec2-user/.local/lib/python3.7/site-packages

4. Execute ec2.py (before change rights: sudo chmod +x ec2.py
./ec2.py --list

PS. 
ansible -i (replace hosts) ec2.py group-hosts
ec2.ini - config file for control ec2.py
change rights ssh-keys hosts: sudo chmod 400 key-name

xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
Playbook for EC2 up

curl -O https://bootstrap.pypa.io/get-pip.py
sudo yum install python3 -y
python3 get-pip.py
pip install botocore
pip install boto3
