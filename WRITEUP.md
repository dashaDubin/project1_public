# Write-up Template

### Analyze, choose, and justify the appropriate resource option for deploying the app.

*For **both** a VM or App Service solution for the CMS app:*
- *Analyze costs, scalability, availability, and workflow*
- *Choose the appropriate solution (VM or App Service) for deploying the app*
- *Justify your choice*
I am choosing the app service because I think it is not 
a sophisticated app and it will not require a lot of resources so creating a dedicated VM is an overkill. 
Besides I think the set up will be much simpler with an app service, and i don't want to spend time tuning a VM. Hipothetically, if this would be a prod app i would need to maintain OS up-to-date, and i think the task is fully covered for a service, so really no need for a VM.
Also a considerable argument towards using an app service is the cost, since im using a free trial account it will be cheaper than setting up a VM.
The only valid argument for the Vm for this task i see is that i had troubles deploying apps from github, 
escpecially the one with the sql database and blob storage. I managed build the project form like 5th or 6th attempt and i spent
couple of hours redeploying the app on no aparent reason. So lets see how this works, maybe i just had some bad luck.

### Re-submission
On comparison of scalability, availability and workflow
The choice of the platform, App services vs VM depends on the problem a user needs to solve in a particular situation. VM offers a full freedom of choice of the environment a user can create and maintain for the application. It also provides a user with an opportunity to control webservers, traffic and your application's configuration. However that comes at a cost of maintaining the whole VM and app by yourself, monitor the security and OS updates etc... Whereas if you don't need such a full control of your application, you can go ahead and use an app service. It gives you an advantage of seemless deployment and integrated github, you can maintain prod and dev environments simultaneously. But your app has to be constant throughtout its lifetime, the resources it needs, tha bandwidth etc.  

### Re-submission #2
I was asked to add about availability and scalability of VMs vs app services (sorry it had to take two attempts, i thought it has to apply to our concrete case, and since im on a free tier for app services and i was rather certain i didn't want to set up a VM for this task, i didnt really try to discuss the topic...).
So, as for the availablity, App Services come with a high SLA, that guarantee the same availability as VMs with two instances, which is kind of a premium service. However, since we are using the Free Tier there is no SLA for the App service there, so it loses its advantage over the VM for our purposes. 
Scalability for app services depends on the tier as well. To scale up or out you need to purchase higher tier for your service plan. Then, depending on your purpose you can either increase the properties of the service (like cpu or memory etc) or increase the number of instances that run your app. For VMs you have load balancer and scale sets for autoscaling that allows to create a group of load-balanced VM that can increase or decrease on demand or according to a schedule. This requires some DevOps knowledge as well... :) Again, since we operate on a free tier scalability was not under consideration :) 


### Assess app changes that would change your decision.
If it will work badly with an app service in terms of app deployment i will switch to VM. 
I would consider switching to a VM as well if i would need a complete control over the OS,
would need a specific OS for my application or would need high availability for my app. 
So far i think we are good to go with an app service
*Detail how the app and any other needs would have to change for you to change your decision in the last section.* 

PS
Finally I had problems deploying the app again. I opened an item in the Knowledge, and i googled the issue. Apparently its not that uncommon. I finally managed to deploy - another hint something is wrong that i didn't do any changes in deployment or code - and from the 5th or 6th attempt it worked. I don't know if i am doing something wrong, but since the issue was reported before - maybe a bug report is due, but since im very new to the platform i can't judge yet. 