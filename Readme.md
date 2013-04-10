Heroku buildpack: Python with Scikit-Learn from HEAD 
========================

This is a [Heroku buildpack](http://devcenter.heroku.com/articles/buildpacks) for Python apps.
It uses [virtualenv](http://www.virtualenv.org/) and [pip](http://www.pip-installer.org/).

Usage
-----

Example usage:

    $ ls
    Procfile  requirements.txt  web.py
 
Make sure to use this repo URL:

    $ heroku create --stack cedar --buildpack git@github.com:everysignalinc/heroku-buildpack-python-scikit-learn-git.git

    $ git push heroku master
    ...
    -----> Heroku receiving push
    -----> Fetching custom build pack... done
    -----> Python app detected
    -----> Preparing virtualenv version 1.6.4
           New python executable in ./bin/python
           Installing setuptools............done.
           Installing pip...............done.
    -----> HUGE numpy compile output

           Cleaning up...

The buildpack will detect your app as Python if it has the file `requirements.txt` in the root. 

