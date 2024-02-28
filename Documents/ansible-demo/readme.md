CONFIGUIRING MULTIPLE SERVERS WITH ANSIBLE

-Create three ec2 instances with help of terraform module that is used.
-make one of the server as master server  and other two servers as worker nodes.
-ssh into the master server and generate a ssh-key gen using : "ssh-keygen"
-copy the ssh  public key to authorized_keys file on all the other worker  nodes.
-now check whether the other  two workers are reachable from master or not by pinging them .
-create a directory for ansible and cd  into it.
-create an inventory.ini file in which we will add our workers private ips as myhosts
-Ping the myhosts group in your inventory.
-"ansible myhosts -m ping -i inventory.ini" : use this to ping  all the workers mentioned in the inventory file.
-Create a file named playbook.yaml in your ansible directory, that you created earlier
-run your playbook with : "ansible-playbook -i inventory.ini playbook.yaml"


