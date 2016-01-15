# Little Node App

Deployed to Heroku.

To set the Mongo URL:

```
$ heroku config:add MONGODB_URL=<some_username>:<some_password>!@ds123456.mongolab.com:45795/little_node
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
