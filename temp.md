
aws s3 cp s3://jenkins-build/CM/AupBuild/master/7.5.4/ C:\Users\singha\Desktop\Newfolder\CORE --recursive

\\192.168.254.1\Temporary\Navaratna_Chaudhary\CM-V7.5.5\DB
\\192.168.254.1\Release\CM\2024\CM-CS-DBS-V1.0.2

To check enableExecuteCommand status:
aws ecs describe-tasks --cluster <example-cluster-name> --tasks <example-task-id>| grep enableExecuteCommand
 
aws ecs describe-tasks --cluster analec-dev-ecs-cluster --tasks 6df9145b12e0434abd7140214fa72252 | grep enableExecuteCommand
 
To update enableExecuteCommand to true:
aws ecs update-service --service <example-service> --cluster <example-cluster-name> --region <example-region> --enable-execute-command
 
aws ecs update-service --service loadtesting --cluster analec-pre-prod-ecs-cluster_load_testing --region us-west-2 --enable-execute-command
 
To connect ECS container:
aws ecs execute-command --region us-west-2 --cluster cluster --task 3adc46c5f20a553a24ca1d9d80a --command "/bin/bash" --interactive
aws ecs execute-command --region us-west-2 --cluster cluster_load_testing --task 7f6c3ac4c20475f2eb75 --command "/bin/bash" --interactive
aws ecs execute-command --region us-west-2 --cluster cluster_load_testing --task 3f69357e5d8199cd41034792fa32 --command "/bin/bash" --interactive


apt install nmon
c for cpu
m for memory
h for help
q for quit

aws ecs execute-command --region us-west-2 --cluster cluster --task e3a355c7a07eb76699cb5cb6 --command "/bin/bash" --interactive
apt install htop
htop [-dChusv]
