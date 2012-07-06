studying-cakephp2
=================

**This is just my study project.**

This is an application made with CakePHP 2.2(PHP Web Application Framework).


Environment
-----------

My environment:

- CentOS 6.2 (Minimal install)
- nginx 1.2.x
- PHP 5.4.x with APC, Xdebug
- MySQL 5.1.x

Running php-fpm with nginx.
But Apache is easier to run Symfony2 because the rewrite rule is provided by CakePHP.


Getting started
---------------

1. Clone this repository.
2. Setup virtual host and configure document root to `app/webroot` directory.
3. Setup permissions. (See http://book.cakephp.org/2.0/en/installation.html#permissions)
4. Copy `app/Config/core.php.dist` to `app/Config/core.php` and set Security.salt, Security.cipherSeed.  
   You can use below command to generate random string.

        # Generate random salt.
        cat /dev/urandom | tr -dc '[:alnum:]' | head -c 40

        # Generate random cipher seed.
        cat /dev/urandom | tr -dc '[:digit:]' | head -c 29

5. Copy `app/Config/database.php.default` to `app/Config/database.php` and change parameters according to you environment.
6. Run `git submodule update --init --recursive`
7. If you want to use latest version of Twig, run `cd app/Plugin/TwigView/Vendor/Twig; git checkout master`
8. Access `http://your_server/example`
