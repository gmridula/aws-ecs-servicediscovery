# aws-ecs-servicediscovery
Demo for ECS Service Discovery

This provides two docker containers: backend and worker. Both run simple flask apps. We are using the ".corp" domain name.

**Clean Up Steps**: 

Since the services created the hosted zones, they will have to be deleted first and deletion of the namespace will take care of cleaning up the route53 hosted zones.

 1. ECS >> Clusters >> Select the Cluster >> Go to Services >> Delete the running Services
 2. Delete the cluster from the AWS console
 3. Verify that the services are cleaned up from AWS CLI by using the command ***aws servicediscovery list-services***
 4. Delete the services if they still show up from CLI using command: ***aws servicediscovery delete-service --id=id_name***
 5. List the namespaces using CLI command: ***aws servicediscovery list-namespaces***
 6. Delete the namespaces: ***aws servicediscovery delete-namespace --id=id_name***


