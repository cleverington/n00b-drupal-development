# {{ book.sections.new_users.scaffolding }}

I'm glad you asked.  (I was going to talk about it anyway.) Each Drupal installation from Drupal 6 onwards has the same file structure, files & infrastructure.

This means work which should be quickly and easily predictable and repeatable via scripting (through Drush, Gulp, or Grunt, for example) and version control (such as Git).

No matter which version of Drupal you might be using, your directory will look something like this:
```
# Drupal-6.x-dev (2016-April)

includes/
misc/
modules/
profiles/
scripts/
sites/
themes/
.htaccess
CHANGELOG
COPYRIGHT
cron.php
index.php
install.php
INSTALL.txt
INSTALL.mysql.txt
INSTALL.pgsql.txt
LICENSE.txt
MAINTAINERS.txt
robots.txt
upgrade.php
UPGRADE.txt
xmlrpc.php
```
Advanced users, being quite smarmy and up with the hip provisioning, might even have something like this:
```
# Drupal-7.x-dev (2016-April)

includes/
misc/
modules/
profiles/
scripts/
sites/
themes/
.htaccess
authorize.php
CHANGELOG
COPYRIGHT
cron.php
index.php
install.php
INSTALL.txt
INSTALL.mysql.txt
INSTALL.pgsql.txt
INSTALL.sqlite.txt
LICENSE.txt
MAINTAINERS.txt
README.txt
robots.txt
upgrade.php
UPGRADE.txt
web.xml
xmlrpc.php
```
and people **way** over your head (and someimtes mine) have something like this:
```
# Drupal-8.4.x-dev (2017-Oct) https://github.com/drupal/drupal

core/
modules/
profiles/
sites/
themes/
vendors/
.csslintrc
.editorconfig
.eslintignore
.eslintrc.json
.gitattributes
.htaccess
README.txt
autoload.php
composer.json
composer.lock
example.gitignore
index.php
robots.txt
update.php
web.config
```
Notice the similarities? From Drupal 6 to Drupal 7, the file structure barely changed at all.

In Drupal 8 it got to be **awesome** because the *reversed* the setup and moved all of the Drupal Core files into the `core/` folder. Instead of being locked **only** within the `sites/` folder for changes and Development, Site Owners instead get to make all of their changes in the folders *outside* of the `core/` folder. 

> To reiterate, Dont' Hack Core

The `sites/` and `profiles/` folders are maintained through *all* installations. In Drupal 6 and Drupal 7, all Development work happens within either of these two folders. In Drupal 8, as I mentioned, custom/contrib work is done outside of the `core/` folder.

### Drupal 7 Directory Structure

When using standardized Drupal 7 Best Practices, the `sites/` folder will generally have the same directory structure between installations as well, such as:
```
all/
  - files/
  - modules/
    - contrib/
    - custom/
  - themes/
default/
  - files/
  - modules/ (This should only be used when using Drupal Multisite)
  - themes/ (This should only be used when using Drupal Multisite)
  - default.settings.php
  - settings.php
  - local-settings.php
```
*Note - Your installation may not have a local-settings.php file, but you should before moving into production. We can get into that later.*

### Drupal 8 Directory Stucture
Drupal 8 adopted [Composer](https://getcomposer.org/ "Composer Homepage") in a very heavy way, so you'll want to get used to seeing Composer *everywhere* in Drupal. Everywhere.

In addition, we've seen a **very** heavy upshoot in Composer integrations using 'Continuous Integration', to keep codebases itty-bitty-tiny for the fastest deployments.

```
core/
drush/
modules/
  - files/
  - modules/
    - contrib/
    - custom/
  - themes/
sites/
  default/
    - files/    
    - default.settings.php
    - settings.php
    - local.settings.php
```

*Note - In Drupal 8, it does not really give SIte Builders a **choice** in using local.settings.php, even including content within settings.php by default to support it.