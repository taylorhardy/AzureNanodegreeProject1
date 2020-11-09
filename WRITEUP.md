# Write-up Template

### Analyze, choose, and justify the appropriate resource option for deploying the app.

*For **both** a VM or App Service solution for the CMS app:*
- *Analyze costs, scalability, availability, and workflow*
- *Choose the appropriate solution (VM or App Service) for deploying the app*
- *Justify your choice*

App Service: Being that this is a small application, it does not require a lot of compute resources. Due to this, even with paying for constant usage, the cost would still be smaller/equal to using a VM that is not running all the time. While scaling could be costly, the premise of this application is simple and probably would not be an issue. CI/CD setup is far easier to get started using App Services, through the deployment center. 

VM: This option allows for more customization and scalability. This would also be a good opiton if the application was built using a language not supported by App Services. Because of the abilty to customize the VM, you would be able to optimize performance more with a VM. However, for smaller development teams this would be more overhead to manage. 

Deployment Choice: I chose to deploy the application using App Services, as the application is very simple and will not require the compute power to justify mantaining a VM. Since App Services supported Python, it was much quicker to deploy the application and setup a CI/CD pipeline as well. 

### Assess app changes that would change your decision.

*Detail how the app and any other needs would have to change for you to change your decision in the last section.* 

App Service: If the application was written in a language that App Services does not support, this would require me to make a different decision. Also, if there was a requriement that increased the compute power needed by a lot, this would no longer be a cost effecitve solution. 

VM: If the project needed more compute power, I would have went with using a VM. Also, if the project had a dependency that was not a supported language, or requried OS customization, a VM would have been a more viable option. 