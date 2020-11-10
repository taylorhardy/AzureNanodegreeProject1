# Write-up Template

### Analyze, choose, and justify the appropriate resource option for deploying the app.

*For **both** a VM or App Service solution for the CMS app:*
- *Analyze costs, scalability, availability, and workflow*
- *Choose the appropriate solution (VM or App Service) for deploying the app*
- *Justify your choice*

App Service: Being that this is a small application, it does not require a lot of compute resources. Due to this, even with paying for constant usage, the cost for the basic tier (at 730 hours) would be $13.14 per instance. Should the app scale rapidly it would hit about the same costs as 1 VM with 6 instances, However, the premise of this application is simple and probably would not be an issue. Being that the basic teir at 730 hours will still be cheaper, I would be able to have multiple instances for higher availability for less than the price of the single VM (standard tier), allowing for this option to be more available. The workflow for this option is much simpilier, as CI/CD setup is far easier to get started using App Services, through the deployment center. With this option I would able to connect to my GitHub account and use GitHub actions to build and deploy the project over to the App Service. 

VM: This option allows for more customization and scalability. This would also be a good opiton if the application was built using a language not supported by App Services. Because of the abilty to customize the VM, you would be able to optimize performance more with a VM. However, for smaller development teams this would be more overhead to manage. With the pricing for a standard tier D2 VM with a Linux OS being about $80 a month, horizontal scaling would be more costly and invite additional complexity for the application team, however, with more compute power I would be able to have multiple instances of the application running on a VM and use a reverse proxy to load balance between them. By doing this I would have higher availability, but there is still a single point of failure given that it is running on a single VM. The workflow would largely depend on the CI/CD solution that is developed, as it could be as basic as logging into the server via ssh and using Git to pull down the code, or creating a more robust solution using technologies like Jenkins and Docker.

Deployment Choice: I chose to deploy the application using App Services, as the application is very simple and will not require the compute power to justify mantaining a VM. Since App Services supported Python, it was much quicker to deploy the application and setup a CI/CD pipeline as well. 

### Assess app changes that would change your decision.

*Detail how the app and any other needs would have to change for you to change your decision in the last section.* 

App Service: If the application was written in a language that App Services does not support, this would require me to make a different decision. Also, if there was a requriement that increased the compute power needed by a lot, this would no longer be a cost effecitve solution as increasing the instance type doubles the price at each step. 

VM: If the project needed more compute power, I would have went with using a VM. Also, if the project had a dependency that was not a supported language, or requried OS customization, a VM would have been a more viable option. 