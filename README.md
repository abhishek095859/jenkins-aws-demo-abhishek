 # Accessing jenkins with EC2 Instance
 In this we need to create ec2 instance with name " MASTER NODE" and another with "Agent Node"
 then we make connection between master and agent node
  I have created the ec2 instance wit terraform as main.tf
  and security group with SSH and custom TCP then create the instance 
  ![Screenshot 2025-06-24 170620](https://github.com/user-attachments/assets/3e11a26b-5ef8-4b34-8356-eb280e0ad662)
  ![Screenshot 2025-06-24 170150](https://github.com/user-attachments/assets/3e615b30-fc33-4a5b-84ed-7b780601b5b9)


  then we can see the master node and agent node public ip's 
  then now after creation ssh the instance
  ![Screenshot 2025-06-24 170251](https://github.com/user-attachments/assets/1da44685-74f0-475c-ad93-8e9e1e22a31a)
  after the ssh we can connevt to the jenkins with master public ip and port as 8080
  then click on install plugins then open the jenkins
  then ssh to the agent node with master ip 
  ssh into master node server the jenkins user need ssh key to connect to agent 
  ![Screenshot 2025-06-24 170334](https://github.com/user-attachments/assets/e3d18b60-a619-487b-9d80-cedd542976a6)

  ![Screenshot 2025-06-24 170351](https://github.com/user-attachments/assets/3e48be5f-7c3e-4123-8c84-1832811d2f7b)
  ![Screenshot 2025-06-24 170428](https://github.com/user-attachments/assets/f39512dd-73d4-491e-8ef4-a1797119caa0)
   then ssh to the agent node with master ip 



  ![Screenshot 2025-06-24 170428](https://github.com/user-attachments/assets/79627b76-441b-414d-b8cd-ac45c986e4c7)
  before creating the node we need credential and other configurations 
  ![Screenshot 2025-06-24 170500](https://github.com/user-attachments/assets/e7fbad39-2959-469b-96ab-810081dcd36f)
  the private key which have to paste here is from master node 
  then create a  node with name as proper naming convention 
  then configure the requirements host as ip address of private of the agent node 
  label as ubuntu 
  launch method as launch agent via ssh 
  ![Screenshot 2025-06-24 170517](https://github.com/user-attachments/assets/8296cfa9-ebae-44fb-8dca-3df5ea7de09e)
![Screenshot 2025-06-24 170534](https://github.com/user-attachments/assets/b30c8c75-05ca-4ee3-9ca7-008eeb04c7e5)
then build the pipeline and build the configure the requriments where the nodes and connected or not 
then build the pipeline see the pipeline is success or not 
![Screenshot 2025-06-24 165221](https://github.com/user-attachments/assets/9f44147a-fd7e-42e7-b87f-8f3420acf745)
![Screenshot 2025-06-24 165246](https://github.com/user-attachments/assets/73e2734b-475c-4cab-85ca-ce0a4f862c7c)
this is the final requriement to see the pipeline is automated and it is success the master and agent is connected 
to destroy the ec2 instance and other use 
terraform destroy
![Screenshot 2025-06-24 170752](https://github.com/user-attachments/assets/fed38cc9-7d57-4d55-990e-21110c03abaf)





