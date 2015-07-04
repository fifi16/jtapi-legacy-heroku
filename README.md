# jtapi-legacy-heroku
Heroku Twitter API based on Java, a fork of mariotaku:jtapi-legacy

How to deploy
=====

###Heroku

Deployment to heroku is a bit more complicated than OpenShift, but still easier than any other api proxies.

1. Fork this repo
2. Create an application in **Heroku Dashboard**, you will be redirected to **Settings** of your newly created application.
3. Change ````OVERRIDE_APP_HOST```` to your domain (like ````jtapi.herokuapp.com````) in ````jtapi-legacy-heroku/heroku/res/config/jtapi.properties````, commit and push.
4. Find **Config Variables** in **Settings** segment, click **Reveal Config Vars**, then press **Edit**
5. Add a new variable, the **key** is ````BUILDPACK_URL````, and the **value** is ````https://github.com/heroku/heroku-buildpack-java````, click **Save**.
6. Find **Connect to Github** in **Deploy** segment, gives Heroku your Github access, then type **the repo name that you've forked**, click **Connect**.
7. Find **Manual deploy**, click **Deploy Branch**.
8. Done!
