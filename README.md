This buildpack enables support for multiple buildpacks when deploying to Heroku. Yep.

## Usage

First, specify this repository as the buildpack for your Heroku app:

```shell
heroku config:add BUILDPACK_URL=https://github.com/SolarCS/heroku-buildpack-multi.git
```

Then, create a `.buildpacks` file in your project root and populate it with the URLs of the buildpacks you'd like to include, one for each line. If you're deploying a Ruby app, you'll need to add Heroku's [heroku-buildpack-ruby](https://github.com/heroku/heroku-buildpack-ruby) at the end. Below is a sample `.buildpacks` file.

```shell
https://github.com/SolarCS/image-optim-buildpack.git
https://github.com/heroku/heroku-buildpack-ruby.git
```