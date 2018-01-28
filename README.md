# [PLSQL.INFO](http://plsql.info) SOURCE CODES

[![Build Status](https://travis-ci.org/plsql/plsql.info.svg?branch=gh-pages)](https://travis-ci.org/plsql/plsql.info)



Инсталлируете docker, далее:

    $ docker pull marley/centos6-for-jekyll:latest
    $ docker run -i -t -p 80:8080 --name plsql_info marley/centos6-for-jekyll:latest /bin/bash

Далее уже в контейнере docker:

    $ source ~/.bash_profile
    $ cd /projects
    $ git clone --depth=1 https://bitbucket.org/plsql/plsql.info .
    $ bundle
    $ JEKYLL_ENV=production bundle exec jekyll serve --host 0.0.0.0 --port 8080

Остается подключиться браузером к локалхосту.
