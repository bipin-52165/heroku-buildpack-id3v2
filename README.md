Heroku buildpack: id3v2
=======================

This is a [Heroku buildpack](http://devcenter.heroku.com/articles/buildpacks) for using [id3v2](http://id3v2.sourceforge.net/) in your project. 

id3v2 build is a custom vulcan build downloaded from (https://github.com/soft-dave/heroku-buildpack-id3v2/raw/master/id3v2.tar.gz)

It doesn't do anything else, so to actually compile your app you should use [buildpack-id3v2-tag](https://github.com/soft-dave/heroku-buildpack-id3v2) to combine it with a real buildpack.

Usage
-----
To use this buildpack, you should prepare .buildpacks file that contains this buildpack url and your real buildpack url.  

    $ ls
    .buildpacks
    ...
    
    $ cat .buildpacks
    https://github.com/soft-dave/buildpack-id3v2

    $ heroku create --buildpack https://github.com/soft-dave/heroku-buildpack-id3v2

    $ git push heroku master
    ...

You can verify installing ffmpeg by following command.

    $ heroku run "id3v2"
