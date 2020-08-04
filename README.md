# Jenkins_groovy

Hello reader!!

Deploying webserver , with the help of Jenkins is very much time efficient and It's very good to do each and evey task automatically. 

But there is still one thing manual, is to "creating Jobs in Jenkins". And for this purpose the developer team is dependent on the Operation guys.As Developer uploaded the code on SCM , now its the work of Operation team starts and it depends on Operation team, that when they will start Jenkins job and obviously creating job is manual thing, As developers have their hands strong in Coding . Developer can themselves create a code to configure jobs automatically , So here is a way by which using the DSL(Domain specific language) for Jenkins ie. GROOVY, this manual thing can be automated.

   ![images](https://user-images.githubusercontent.com/60088271/89330205-8b1f6c00-d6ad-11ea-8ab5-cf9504292d97.png)

•Project Aim :-
-> Seed Job :- Pull  the Github repo automatically when some developers push repo to Github.
-> Further on jobs should be pipeline using written code  using Groovy language by the developer
* Job1 :- Program to download/pull all program files pushed/updated by developer into github.
* Job2 :-  
    1. By looking at the code or program file, Jenkins should automatically start the respective language interpreter installed image container to deploy code on top of Kubernetes     ( eg. If code is of  PHP, then Jenkins should start the container that has PHP already installed )
    2.  Expose your pod so that testing team could perform the testing on the pod
    3. Make the data to remain persistent using PVC ( If server collects some data like logs, other user information )
* Job3 : Test your app if it  is working or not.
* Job4 : if app is not working , then send email to developer with error messages and redeploy the application after code is being edited by the developer

•Solution :-Code of Seed Job:-
   
   ![Screenshot (764)](https://user-images.githubusercontent.com/60088271/89328783-85288b80-d6ab-11ea-8637-ae28bed3ff70.png)
   
   
   ![Screenshot (770)](https://user-images.githubusercontent.com/60088271/89329764-e13fdf80-d6ac-11ea-9a76-9458d84ed5ac.png)


Only one job, we have to create which will start the pipeline and job chaining is known as "Seed Job". The seed job is a Jenkins job which runs a DSL scripts, and then generates a new job.  

-> After running seed job,Job1 is created and configured automatically :-

   ![Screenshot (766)](https://user-images.githubusercontent.com/60088271/89328991-d33d8f00-d6ab-11ea-833d-18651008e2e5.png)
   
   ![Screenshot (767)](https://user-images.githubusercontent.com/60088271/89329025-e18bab00-d6ab-11ea-8cfb-0e5cdafc1de5.png)

  ![Screenshot (768)](https://user-images.githubusercontent.com/60088271/89329881-13514180-d6ad-11ea-85f9-582a6cc365f2.png)

   ![Screenshot (769)](https://user-images.githubusercontent.com/60088271/89329998-3bd93b80-d6ad-11ea-9279-d065e883a1d4.png)
