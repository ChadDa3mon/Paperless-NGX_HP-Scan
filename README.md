# Paperless-NGX_HP-Scan
This is a simple docker-compose I wanted to share, which combines the super useful [node-hp-scan-to](https://github.com/manuc66/node-hp-scan-to) with Paperless-NGX and a postgres DB. 

# Usage
Simply download the docker-compose file to your local system and place it in a folder where you want your data stored. 

## Customizing
I'm not smart enough (and too lazy) to implement proper variables here. There's a few things you'll want to change:
- **hostname:** (Line 22) - This is the name that will show up in your printer as the computer you can send your scans to
- **IP:** This is the IP address of your printer
- **POSTGRES_PASSWORD:** Put something better than `paperless` here. 
- **PAPERLESS_SECRET_KEY:** This should be a very long (32+ characters) random string of alpha numeric characters

**Note:** For full details on the configuration options, I suggest checking out the [official github repo](https://github.com/paperless-ngx/paperless-ngx).

## Running
Once you have your docker-compose setup the way you want, run `docker-compose up -d` from within the directory where your docker-compose file is. 
