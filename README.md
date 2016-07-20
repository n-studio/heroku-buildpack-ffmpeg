Heroku buildpack: FFMpeg
=======================

This is a [Heroku buildpack](http://devcenter.heroku.com/articles/buildpacks) for using [ffmpeg](http://www.ffmpeg.org/) in your project.  
It doesn't do anything else, so to actually compile your app you should combine it with a real buildpack.

Usage
-----
To use this buildpack, you should prepare .buildpacks file that contains this buildpack url and your real buildpack url.  

    $ heroku buildpacks:add --index 1 heroku/ruby
    $ heroku buildpacks:add --index 2 https://github.com/akomic/heroku-buildpack-ffmpeg.git

You can verify installing ffmpeg by following command.

    $ heroku run "ffmpeg -version"
