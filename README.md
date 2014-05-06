This is a fork of stomita/heroku-buildpack-phantomjs, which points to a different file location for the Phantom JS binaries, as the original location is currently not accessible. This fork will be discontinued, when the original binaries are accessible again!

Below see original readme: 


Heroku buildpack: PhantomJS
=======================

This is a [Heroku buildpack](http://devcenter.heroku.com/articles/buildpacks) of PhantomJS(http://phantomjs.org).

Usage
-----

Example usage:

```shell
$ heroku create --stack cedar --buildpack https://github.com/stomita/heroku-buildpack-phantomjs.git

# or if your app is already created:
$ heroku config:add BUILDPACK_URL=https://github.com/stomita/heroku-buildpack-phantomjs.git

$ git push heroku master
```

Note
-----

If you're using [heroku-buildpack-multi](https://github.com/ddollar/heroku-buildpack-multi) to include other buildpacks, you should set environment variable by your own to include following paths.

    PATH="/usr/local/bin:/usr/bin:/bin:/app/vendor/phantomjs/bin"
    LD_LIBRARY_PATH="/usr/local/lib:/usr/lib:/lib:/app/vendor/phantomjs/lib"



