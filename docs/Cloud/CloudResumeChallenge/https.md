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


Configure HTTPS on an Azure CDN custom domain
- 