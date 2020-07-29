# Strapi MongoDB Atlas Cloudinary Heroku Template

Template for using the Strapi CMS with MongoDB Atlas, Cloudinary for image uploading, and Heroku for hosting.

Bootstrapped with `yarn create strapi-app app-name`

# Setup

Fill in your Cloudinary details in:

`extensions/upload/config/settings.json`

See instructions for using other upload providers [here](https://medium.com/@kwinten.yc.li/strapi-set-default-file-upload-provider-to-s3-cloudinary-rackspace-5b8ef6f61daa)

Fill in MongoDB Atlas details in:

`config/database.js`

Can be hosted on Heroku for easy deployment:

```
$ heroku login
$ heroku create
$ heroku git:remote -a your-heroku-app-name
$ git add .
$ git commit -m "Update database config"
$ git push heroku master
$ heroku open
```

Don't forget to set Heroku environment variables:

```
$ heroku config:set DATABASE_URI="mongodb+srv://<username>:<password>@host/<dbname>?retryWrites=true&w=majority"

$ heroku config:set DATABASE_NAME="my-database-name"
```