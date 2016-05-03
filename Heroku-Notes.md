[Back to README](README.md)
#### Heroku

Get herohu cli (follow instructions on website)
```
wget -O- https://toolbelt.heroku.com/install-ubuntu.sh | sh
```
<hr>
create your app (https://devcenter.heroku.com/articles/getting-started-with-nodejs#deploy-the-app)
```
heroku create
```
<hr>
push your app
```
git push heroku master
```
<hr>
ensure at least 1 instance running
```
heroku ps:scale web=1
```
Heroku CLI submits usage information back to Heroku. If you would like to disable this, set `skip_analytics: true` in /homefolder/.heroku/config.json
<hr>
visit the app by the name generated of from terminal
```
heroku open
```
<hr>
Run the app locally
https://devcenter.heroku.com/articles/getting-started-with-nodejs#run-the-app-locally
```
heroku local web
```
browse http://localhost:5000/
<hr>
View logs https://devcenter.heroku.com/articles/getting-started-with-nodejs#view-logs
```
heroku logs --tail
```
<hr>
#### New Heroku app.
```
heroku login
```
```
heroku create soap-add
  Creating ⬢ soap-add... done
  https://soap-add.herokuapp.com/ | https://git.heroku.com/soap-add.git
```
```
git push heroku master
```
<hr>
https://devcenter.heroku.com/articles/nodejs-support
<hr>
<hr>
<hr>
