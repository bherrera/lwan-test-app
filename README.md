Heroku lwan test application
=======================

Running [lwan.ws](https://lwan.ws) test application at Heroku using [heroku-buildpack-lwan](https://github.com/bherrera/heroku-buildpack-lwan)

    $ls -R
    Aptfile   README.md conf      test.lua  wwwroot

    ./conf:
    lwan.conf.erb

    ./wwwroot:
    100.html   icons      index.html zero

    ./wwwroot/icons:
    back.png   file.png   folder.png


    $cat .buildpacks
    https://github.com/ddollar/heroku-buildpack-apt
    https://github.com/bherrera/heroku-buildpack-lwan

    $cat Aptfile
    cmake

    $heroku create --buildpack https://github.com/ddollar/heroku-buildpack-multi

    $git push heroku master

