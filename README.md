
# Setup Base
aws cloudformation deploy --stack-name networking --template-file networking.yaml --capabilities CAPABILITY_NAMED_IAM --profile buenoh 

# Setup ECS Cluster
aws cloudformation deploy --stack-name ecs-cluster --template-file ecs-cluster-log.yaml --capabilities CAPABILITY_NAMED_IAM --profile buenoh 

# Setup Service
aws cloudformation deploy --stack-name service --template-file service.yaml --capabilities CAPABILITY_NAMED_IAM --profile buenoh 

# Setup Pipeline
aws cloudformation deploy --stack-name pipeline --template-file pipeline.yaml --capabilities CAPABILITY_IAM --profile buenoh 
