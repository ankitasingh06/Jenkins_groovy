# Jenkins_groovy

Hello reader!!

Deploying webserver , with the help of Jenkins is very much time efficient and It's very good to do each and evey task automatically. 

But there is still one thing manual, is to "creating Jobs in Jenkins". And for this purpose the developer team is dependent on the Operation guys.As Developer uploaded the code on SCM , now its the work of Operation team starts and it depends on Operation team, that when they will start Jenkins job and obviously creating job is manual thing, As developers have their hands strong in Coding . Developer can themselves create a code to configure jobs automatically , So here is a way by which using the DSL(Domain specific language) for Jenkins ie. GROOVY, this manual thing can be automated.

•Project Aim :-
4.  Job2 ( Seed Job ) : Pull  the Github repo automatically when some developers push repo to Github.
5. Further on jobs should be pipeline using written code  using Groovy language by the developer
6. Job1 :  
    1. By looking at the code or program file, Jenkins should automatically start the respective language interpreter installed image container to deploy code on top of Kubernetes ( eg. If code is of  PHP, then Jenkins should start the container that has PHP already installed )
    2.  Expose your pod so that testing team could perform the testing on the pod
    3. Make the data to remain persistent using PVC ( If server collects some data like logs, other user information )
7.  Job3 : Test your app if it  is working or not.
8.  Job4 : if app is not working , then send email to developer with error messages and redeploy the application after code is being edited by the developer

•Solution :-Code of Seed Job:-
   


Only one job, we have to create which will start the pipeline and job chaining is known as "Seed Job". The seed job is a Jenkins job which runs a DSL scripts, and then generates a new job.  
