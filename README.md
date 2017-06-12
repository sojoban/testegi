Test EGI
=========

Get Started
-----------

### Requirements

To run this application on your machine, you need at least:

* Apache Web Server with `mod_rewrite enabled`, and `AllowOverride Options` (or `All`) in your `httpd.conf` or Nginx Web Server
* MySQL >= 5.7
* PHP 5.6
* PHP mcrypt
* PHP mbstring
* PHP intl
* PHP curl -- otherwise crawling goes **very slow**
* Phalcon 3.0. Phalcon is a web framework delivered as a C extension providing high performance and lower resource consumption.

```bash
brew tap homebrew/homebrew-php
brew install php56-mcrypt
brew install php56-mbstring
brew install php56-intl
brew install php56-phalcon
brew install php56-curl
```

### Database Setup

```bash
./install_database.sh <mysql-host> <mysql-root-password>
```

## Installing Dependencies via Composer

*NOTE*: Dependencies are currently pushed into the git repository, then you should not really
need to use Composer unless you need to include a new dependency or update current versions.

Test EGI's dependencies must be installed using Composer. Install composer in a common location or in your project:

```bash
curl -s http://getcomposer.org/installer | php
```

Run the composer installer:

```bash
cd lab
php composer.phar install
```

## Preparing the Dev environment

Rename the files on `app/config/*.renameme` to `.php` to have
those values override the standard configuration.

