# node-ansible
Use ansible to remote desktop connection


### aws cli command to check ips
aws ec2 describe-instances --instance-ids $instance_id \
    --query 'Reservations[*].Instances[*].PublicIpAddress' \
    --output text >> inventory
    
    
### command to change permmisiion of ssh key
chmod 600 wsl.pem

### ansible command to do remote command
ansible-playbook main.yml -i inventory --private-key wsl.pem

    
