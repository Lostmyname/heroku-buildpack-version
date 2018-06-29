Source Version Buildpack
==================

We use commit sha's to version our assets. This buildpacks exposes the `SOURCE_VERSION` build time environment variable to the runtime as well.

## Background

Heroku provides the [SOURCE_VERSION](https://devcenter.heroku.com/changelog-items/630) environment variable as a nice SCM-agnostic way to do this. We can use a buildpack to create a [profile.d](https://devcenter.heroku.com/articles/profiled) script that will export SOURCE_VERSION into the app runtime environment.

## Usage

Add the buildpack to your app:

`heroku buildpacks:add https://github.com/Lostmyname/heroku-buildpack-version`

## Links

- [Heroku Buildpacks](http://devcenter.heroku.com/articles/buildpacks)
- [Buildpack API](https://devcenter.heroku.com/articles/buildpack-api)
- [SOURCE_VERSION](https://devcenter.heroku.com/changelog-items/630)
- [Default Config Values](https://devcenter.heroku.com/articles/buildpack-api#default-config-values)
