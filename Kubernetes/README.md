                                                                                                          
Using this document you can install Kubernetes Cluster with Ansible Automation

Follow below steps to setup k8s cluster:

1) Create an ssh connection with remote machine with the controller machine:
   
 -   ssh-keygen			# .ssh/id_rsa.pub is the public key
 -   ssh-copy-id root@"Target Master Node IP"
 -   ssh-copy-id root@"Target Worker Node IP"
 
2) Run the given command to start the installation:
 
 -   ansible-playbook install.yml -i inventory.txt

 - Type "no" for "Do you want to enable docker nightly repo(optional) [yes/no]:"
 - Type "no" for "Do you want to enable docker test repo(optional) [yes/no]:"
 - Type "yes" for "Do you want to enable reset before kubeadm installation [yes/no]:"
 
3) After installation run the given command to see the k8s cluster
 -  kubectl get nodes