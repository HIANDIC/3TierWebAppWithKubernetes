## 3 tier web application (frontend, backend and database)

- In this project I will create a 3 tier web application (frontend, backend and database). In other words our architecture will be created as presentation tier, application tier and data tier. In order to create this architecture these steps will be done:

#

1. First of all the images of our app must be created
2. These app's images are pushed to docker hub
3. Now we begin the K8s part:

    - PV
    - PVC
    - Database Deployment
    - Database Service
    - Webserver Deployment
    - Webserver Service
    - Resultserver Deployment
    - Resultserver Service
    
4. We go on K8s and make some additional configuration to make our infrastructure more flexible and secure. Therefore we will create secret and configmap objects.
    
    -   For credentials and sensitive data we will use secret object
    -   For other nonsensitive data we will use configmap
5. At the end all config files will be created as charts by using helm. After that deployment/release will be done via using helm.


Note: In the Webserver Deployment secret and configmap objects are not be used. I want to show the differences between hardcoding/hard configuration and flexibility. Do not forget that it is not a best practice. Best practice is to use secret and configmap and store these data in our cluster not in a version control system. But for learning purpose I put these config files in my repo. You can see using secret and configmap ensure our app to be more secure and flexible. It is a very convenient way to manage our config files.