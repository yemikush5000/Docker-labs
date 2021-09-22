# Docker-lab
This Project uses tool like Docker, Ansibles, Jenkins, Git, mysql, 
it comprise of 1 centos host running 3 containers
1 jenkins container - also runing jenkins, git and ansible on this container
1 Remote-host containers running centos 7, having mysql client, aws cli,ssh server,
1 mysql database which holds some database tables that we backup to s3 bucket using jenkins
