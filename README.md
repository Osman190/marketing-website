# DCI marketing website

[![Build Status](https://travis-ci.org/DigitalCareerInstitute/marketing-website.svg?branch=master)](https://travis-ci.org/DigitalCareerInstitute/marketing-website)

![Screenshot](screenshot.png)

### Architecture:

NodeJs/Express/Passport/Pug/Redis, React in the backend

[Live version](https://digitalcareerinstitute.org)  

## Installation:
1. Install `NodeJS/npm`
1. Install `MongoDB`
1. Install caching `Redis`. [Install info](https://redis.io/download#installation)
1. copy the `.env.example` to `.env` and fill in the neccessary secret keys (you get them from an admin): ``
1. It can happend that it complains about a missing global `webpack` and `webpack-cli`. Just install them global: `npm i webpack webpack-cli -g`


#### Example .env:
```
PORT=3000
MONGOURL=mongodb://localhost:27017/marketing-website
DOMAIN=localhost
EVENTBRIDE_API_KEY=XXXXXXXXXXXXXXXXXXXX
MAILHOST=XXXXXX.XXXXXXXXXX.com
MAILUSER=XXXXXXXXXXXX
MAILPW=XXXXXXXXXXXXXX
MAILPORT=587
MAILRECEIVER=developer@digitalcareerinstitute.org
TOURMAILRECEIVER=developer@digitalcareerinstitute.org
IMAGE_UPLOAD_DIR=uploads/images/
USE_REDIS=true
AUTHORIZATION='auth xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx-us14'
URL='https://us14.api.mailchimp.com/3.0/lists/xxxxxxxxxx'
CRONINTERVAL="0 0 * * *"
CLIENT_ID="XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX"
CLIENT_SECRET="XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX"
SESSION_KEY=digitalcareerinstitute
SESSION_SECRET=XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
HUBSPOT_API_KEY=XXXXXXXX-00XX-0000-0000-XXXXXXXXXXXX

```

### Run the app

Start normal: `npm start`  
Start development: `npm run dev`

### Insert example data in database

##### Create a few Stories and Menulocations in the selected DB.

Insert example data:  
`npm run seed`

Remove all seeds from database:  
`npm run seed:delete`

### Contribution
- Check out the [Issues](https://github.com/DigitalCareerInstitute/marketing-website/issues) for a `good first issue` and let yourself invite to Trello by [@spielhoelle](mailto:thomas.kuhnert@digitalcareerinstitute.org)
- And read  the [Contribution Guidelines](CONTRIBUTING.md)
- Be nice to each other and follow the [Code of Conduct](https://github.com/digitalcareerinstitute/marketing-website/CODE_OF_CONDUCT.md)


### Run in docker dev environment  
`docker-compose up`

### Deployment
In the private [infrastructure repo](https://github.com/DigitalCareerInstitute/infrastructure) we manage the deployment and the server provision per [Ansible](https://www.ansible.com/). If you need to deploy, require ssh access to the live environment from an admin.


## Features

For some actions you need a superadmin account, for some a normal admin role is enought. Contact [@spielhoelle](mailto:thomas.kuhnert@digitalcareerinstitute.org) or [@LeandroDCI](https://github.com/LeandroDCI) for extended access rights.

### Events from eventbrite

Events will be automatically fetched once a night per a automated task. It is possible to  manually delete all of them and refetch in case of urgent update. Go on [/admin/events](https://digitalcareerinstitute.org/admin/events) and use the appropriate interface action for just refetch, or first purge all.
![Events screenshot](/docs/events.png)

### Multilang
Todo

### Usermanagement
Todo

### Partners
Todo

### Employees
Todo

### Pages
Todo

### Stories
Todo

### Locations/Campuses
Todo

### Menu + menulocations
Todo

### Pages
Todo

### Contacts
Todo

### Courses
Todo

### Add an item
Todo

