# {{ book.sections.drupal_learning.drupal_learning_sections.installing_drush }}

## Role
- ALL

## Rank
- ALL

## Prerequisites
- Basics of Composer

## Drupal 8 Drush

Installation of Drush changed **permanently** in Drupal 8.4. 

Using previous versions of Drush and previous versions of Drupal, Drush could be installed globally (via `composer require -global drush/drush` or similar) and then used within any Drupal Project (though this ended badly) or creating in a directory all alone (see method below) and used via an alias.

With the addition of the Composer and the greater portions of the Symfony Framework, maintaining Drush as a project dependancy was the next logical evolution.

### Steps to Install Drush 8.x or Drush 9.x

*All of this information can be found at http://docs.drush.org/en/master/install/*

To start, the gang at Drush highly recommends installing the [Drush Launcher](https://github.com/drush-ops/drush-launcher "Drush Launcher"), which allows the `drush` command to be used globally, even though `composer require -global` cannot be performed.

```bash
$ cd ~/some-drupal-site
$ composer require drush/drush
```

Most general options for requiring `drush` are:
```bash
$ composer require drush/drush:9.x
$ composer require drush/drush:8.x
```
Drush 7.x can *technically* be installed via `composer require`, but only Drupal 7 and Drupal 8 support Composer. If *using* Composer within a Drupal 8 project, you're better off with drush 8.x.

## Older Versions of Drush

*These methods do not work for Drush 9.x and support will degrate for Drush 8.x starting October 2017.*

Sometimes it is prudent to maintain multiple versions of Drush, especially when maintaining multiple Drupal sites with different versions of Drupal installed.

**For Example:**
- Drupal 6 will not work with Drush 8.x or Drush 9.x
- Drupal 7 will work with both Drush 7.x and Drush 8.x
- Drupal 8 will work with both Drush 8.x and Drush 9.x
- The local version of Drush used to connect must be the same as the remote server (7.x, 8.x, etc.)
- The local version of Drush used to connect must be a *greater* release than the remote server (8.11, 7.1.8, etc.)

### Steps to Keep Older Versions of Drush Available

This method is basically just exploiting Composer to keep a version of Drush 'at the ready' when needing to use Drush for Maintenance and upkeep of older Drupal installations.

#### Install drush 7.x
- `mkdir ~/drush7`
- `cd ~/drush7`
- `composer require "drush/drush:7.*"

#### Install drush 8.x
- `mkdir ~/drush8`
- `cd ~/drush8`
- `composer require "drush/drush:8.*"

#### Create Aliases
Add the following lines to your `~/.bashrc` or `~/.bash_profile`:
- `alias drush7='~/drush7/vendor/bin/drush'`
- `alias drush7='~/drush8/vendor/bin/drush'`


Credit to ccjjmartin for the tips on multiple versions of Drush, compliments of https://github.com/ccjjmartin/setup.environment. 