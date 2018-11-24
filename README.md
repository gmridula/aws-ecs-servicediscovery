# aws-ecs-servicediscovery
Demo for ECS Service Discovery

This provides two docker containers: backend and worker. Both run simple flask apps. We are using the ".corp" domain name.

Clean Up: Since the services created the hosted zones, they will have to be deleted first and deletion of the namespace will take care of cleaning up the route53 hosted zones.

GO TO AWS Console
Step 1: ECS >> Clusters >> Select the Cluster >> Go to Services >> Delete the Services
Step 2: Delete the cluster from the AWS console
Step 3: Get the list of services
        aws servicediscovery list-services
Step 4: Delete the services
        aws servicediscovery delete-service --id=<id>
Step 5: List the namespaces
        aws servicediscovery list-namespaces
Step 6: Delete the namespaces
        aws servicediscovery delete-namespace --id=<id>   

