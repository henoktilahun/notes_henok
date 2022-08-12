# Azure Storage Acccount

- Before you can create an azure static website, you'll need to create a storage account where you can host your site
- Got to Azure portal, make sure you have an account and an azure subscription
- Got to 'All Resrouces'
- Select Storage account
- Select + to create a container
- Pick default options?? not really sure lol


## Static website

- under the new or exiting storage account
- Go to the 'Capabilities' tab under overveiw
- Click Static website
- Select enabled
    - index document name: index.html
    - error document path: 404.html
    - save
- Should give you a primary and secondary endpoint

- Under storage account > containers > $web:
    - click upload and select files

    - To upload folders:
        - go to storage account
        - storage browser > blob containers > $web 
        - Click add directory
        - give it a name and hit 'ok'
            - while you're still on that page upload the files - upload, browse and select

- Once you have all your files uploaded - you should have a webpage you can access publicly 
