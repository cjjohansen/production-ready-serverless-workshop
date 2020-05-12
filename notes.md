Pool Id us-east-1_dNdrAJDOU

App client web

ID 1eu8g2l13b9oi1ja6g7gmkji7d

App client server

ID 6g5j94ucg2loh223st4vatidlu


curl -d '{"theme":"cartoon"}' -H "Content-Type: application/json" -X POST https://52lk47kcw6.execute-api.eu-west-1.amazonaws.com/dev/restaurants/search




DynamoDB code tries to determine environment from
1) explicitly defined in code

2) environment vairable AWS_REGION can be set by setx in wondows. and viewed with echo %AWS_REGION% 

3)aws cli account  region. Can be changed with aws config command

Since our recources dynamoDB etc are reciding in eu-west-1 region tests will fail, since our AWS_REGION is not set or our aws config is not set to anything. SEtting one of these to eu-west-1 and closing all instances of visual studio code and running tests again should result in success. 



curl -d '{"theme":"cartoon"}' -H "Content-Type: application/json" -X POST https://xxx-api.us-east-1.amazonaws.com/dev/restaurants/search