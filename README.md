# django

Create a Django project🔗 with postgresql

##  Inatalling and deploy the  Django/PostgreSQL Webapplication:


Second Question:

An application is running in AWS with Load balancer. Currently the backend instances (instances behind load balancer) are static. that is they are not in any auto scaling group. Currently they are deploying the application into backend instances via Jenkins and some custom scripts. 

Now the client decided to switch to autoscaling for cost saving. But as you know the existing continuous deployment(CD) won't work since the instances in autoscaling groups are dynamic and they keep changing on the basis of work loads. How will you address this issue? Please provide an architecture to improve the deployment logic. You have the freedom to use any services or tools.

   
We can use the code deploy service in aws to deploy the codes to autoscaling group. we can create s3 bucket as source and we can create deployment group as well.

The deployment consider the instance autoscaling. The code deplaoy service keep the bulded code in s3 bucket .according the instance availablity, the code deploy deploying he content to the instance based on some scripts.  Also, we can install deploy plugin in the jenkins. we can trigger the plugin once build completed  that copy content s3 bucket and it will distrubte the content to the sinatance as well.

