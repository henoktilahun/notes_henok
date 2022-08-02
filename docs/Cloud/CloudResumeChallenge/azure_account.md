# Azure Account

## Create an Azure Account ([Azure Docs](https://docs.microsoft.com/en-us/learn/modules/create-an-azure-account/3-exercise-create-an-azure-account))
- Go to [Azure](https://azure.microsoft.com/free)
- Click 'Start Free'
- Sign in or create a new account (can use github account)
- Follow the prompts to complete creating an account

## Create Management Groups ([Azure Docs](https://docs.microsoft.com/en-us/azure/governance/management-groups/create-management-group-portal))

__Prerequisites__

- Azure subscription

__Create in Portal__

- Log into azure
- All Service > Management + governance.
- Select Management Groups.
- Select + Add management group.
- Create New
    - Might have to select "start using managment groups"
- Enter maagment group ID - can't be changed
- Enter managment group display name
    - Devleopment (DEV)
    - Production (PROD)

__Add subs to mgmt groups__

- Go to all services
- Click on subscriptions
- Click "+"
- Enter a sub name (crc_dev)
- Select billing account, billing profile, invoice section (default)
- Plan = Microsoft Azure Plan
    - this is at pay as you go rate but not sure if it's the same??
- Under 'Advanced', choose the mgmt group you want
- Click review and create
- click create 
- Do the same for crc_prod
Click on mgmt group (DEV)
- Select 'Add subscription'
- 

