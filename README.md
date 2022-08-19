# `heroku-buildpack-gifski`

### Install

This buildpack installs [gifski](https://github.com/ImageOptim/gifski/issues) on your dynos.

In your project root:

```sh-session
$ heroku buildpacks:add https://github.com/voxable/heroku-buildpack-gifski --app HEROKU_APP_NAME
```

### Set gifski version

You can set a `GIFSKI_VERSION` config variable to control the installed version:

```sh-session
$ heroku config:set GIFSKI_VERSION=1.7.1 --app HEROKU_APP_NAME
```

### Clear cache
Since the installation is cached you might want to clean it out due to config changes.

 ```sh-session
$ heroku plugins:install heroku-repo
$ heroku repo:purge_cache -app HEROKU_APP_NAME
```
> _Note : Replace `HEROKU_APP_NAME` With Your App Name Ex. sticker-bot1_
