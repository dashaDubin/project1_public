# Write-up Template

### Analyze, choose, and justify the appropriate resource option for deploying the app.

*For **both** a VM or App Service solution for the CMS app:*
- *Analyze costs, scalability, availability, and workflow*
- *Choose the appropriate solution (VM or App Service) for deploying the app*
- *Justify your choice*
I am choosing the app service because hipothetically if this app would be a prod app 
i would not want to spend my time on maintaining the OS of a VM up-to-date. I think it is not 
a sophisticated app and it will not require a lot of resources so creating a dedicated VM is an overkill. 
Besides I think the set up will be much simpler with an app service. And im lazy to administer a whole VM for this :) 
Also a considerable argument towards using an app service is the cost, since im using a free trial account it will be cheaper than setting up a VM.
The only valid argument for the Vm for this task i see is that i had troubles deploying apps from github for all the exersices, 
escpecially the one with the sql database and blob storage. I managed build the project form like 5th or 6th attempt and i spent
couple of hours redeploying the app on no aparent reason. So lets see how this works, maybe i just had some bad luck.

### Assess app changes that would change your decision.
If it will work badly with an app service in terms of app deployment i will switch to VM. 
I would consider switching to a VM as well if i would need a complete control over the OS,
would need a specific OS for my application or would need high availability for my app. 
So far i think we are good to go with an app service
*Detail how the app and any other needs would have to change for you to change your decision in the last section.* 