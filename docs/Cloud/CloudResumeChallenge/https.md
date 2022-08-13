# HTTPS

 - Need azure CDN for this
 - Azure CDN = Azure content delivery network
    - distributed network of servers that can efficiently eliver web contnet to users
    - CDNs store cached content on edge server and are in locations closer to users
    - Benefits of suing Azure CDN
        - Performance + bertter user experience
        - better handling of sudden high loads (i.e. product launcs)
        - Less traffic on origin server + user distribution

- To enable Azure CDN for storage account:
    - go to storage account
    - On the left side, select Azure CDN
    - Values for Create new endpoint:
        - CDN profile: 'create new' 
        - Pick a name (i.e. cdn-crc-profile)
        - Pricing tier: Microsoft CDN (classic)
        - CDN endpoint name: cdn-crc-endpoint
        - Origin hostname: defualt
    - Select 'Create' and it should create an Azure CDN 


## Add custom domain to endpoint

### Create CNAME DNS record
- For google dns
    - go to domains.google
    - find your custom domain or get one
    - Click manage
    - Under 'DNS', select 'Manage custom records'
    - add:
        - Host Name: www
        - Type: CNAME
        - Data: _Azure Endpoint_
- Note: in google DNS, you have to point your A/root record to an IP address to you won't be able to point example.com to your end point. The workaround for me was to use forwarding - so example.com forwards to www.example.com which was set up in the previous instructions. 

### Add a custom domain to your CDN endpoint
- In your portal, go to the CDN you created
- Click '+ Custom Domain'
- Endpoint should be prefilled
- Add your custom hostname. i.e. www.example.com 
    - You'll need to already have create your dns record before this
- That's it!
- According to AZURE, it should take around 10 minutse for everything to propagate and you should be able to navigate to your custom domain and access your content


## Configure HTTPS on Azure CDN

### TLS/SSL certs - CDN managed
- 