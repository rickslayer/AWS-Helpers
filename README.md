# AWS-Helpers

### AWS LOGIN CLI
|Command | Description |
| ------- | ----------- |
| `aws configure` | On CLI ask for your client and secret keys |
### AWS ECS CLI
|Command | Description |
| ------- | ----------- |
| `ecs-cli configure --cluster fancy-cluster --default-launch-type EC2 --config-name fancy-cluster --region us-west-2` | Create a new cluster using ECS |
|`ecs-cli up --keypair vockey --capability-iam --size 4 --instance-type m4.large --cluster-config fancy-cluster --port 8080`| Create a EC2 Instances


### AWS ECR 
|Command | Description |
| ------- | ----------- |
| `aws ecr describe-repositories` | List your repositories in ECR |

### UPLOADING DOCKER IMAGE TO AWS ECR
|Command | Description |
| ------- | ----------- |
| `docker tag image:version {repositoryURI}` | taging your image |
| `aws ecr get-login --region us-east-1 > text.txt` |Retriving the login token and put in a txt file|
|`docker login -u AWS {repositoryURI} -p --password-stdin text.txt` | Loging in your register|
|`docker push {repositoryUri}/{image-tag}:latest`|Push your image to your ECR repository| 
|`aws ecr --repository-name={repositoryName} describe-images`| Now you can check the images passing by repository name|
`


