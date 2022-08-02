# Azure Environments


__Azure Management Groups__

- A way to manage subscriptions
- It's a layer above subscriptions so all subs wition a managmeent group will automatically get the conditions applied to that group
- Can be hierarcal, so can have parent to child relationship
- Can be created via cli 
- `az account management-group create --name 'management group name' `

__Subscriptions__

- Just a way to group resources under your billing account
- Can have multiple subscriptions
- User accounts stored in Azure Active Directory (Azure AD)

To create a subscription:

- Log in to your account
- Select the subscription you want and add it
- Most common is 'Pay As You Go'

__Resource groups__

- Groups to organize related rerouces into
- Can have as many resrouce groups as you want for each subs

__Hierarchy__ 

Tenant/Azure AD -> Root Tenant Group -> Management group or subs or both -> child managment groups -> subs -> resource groups

__Diff Env. with Management Groups__

- Can have different Managment groups for Dev, QA, Prod
- Each managment grups has it's own subs
- Each sub has it's own resource group
- Each rsource group has the resources under it. 

![](https://miro.medium.com/max/700/1%2AEKZ0Jni6S_0hEJg0QnqlWA.png)

- Can also do the same thing swith subs. bypassing the management groups
- subs (dev, qa, prod) -> resource group -> Resrouces
- Can also do the same thing with Resrouce groups
- One sub -> Resrouce groups (dev, qa, prod) -> Resources
- Can also have mixed approaches of all three 