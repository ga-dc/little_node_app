# Little Node App

Node and Mongoose, deployed to Heroku.

1. Sign up for a *free* [MongoLab database](http://mongolab.com).
2. Create a new user in the *database*. This is *different* from your MongoLab user account. Don't bother with crazy password security. You'll need the username and password for step 5.
3. `$ heroku create`
4. `$ git push heroku master`
5. Set an environment variable with the appropriate information from your MongoLab database. The variable here has been called `MONGODB_URL`, but it can be anything as long as it matches the place the URL is referenced in your `index.js`.
```

$ heroku config:add MONGODB_URL=NAME_OF_USER_YOU_CREATED:PASSWORD_OF_USER_YOU_CREATED!@ds123456.mongolab.com:45795/little_node
```

If you get errors:

```
$ heroku logs --tail
```

If the error says something about `ENOENT` or `ERRCONNECTION`, make sure you set the Mongo URL correctly.

Check with:

```
$ heroku config -s
```
