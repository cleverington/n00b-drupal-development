# {{ book.sections.new_users.you_need_drush }}

If you are a Mac or Linux user, you really, *really* need [Drush](http://docs.drush.org/en/master/install/).

Even if you, as a beginner Drush is a tool every Drupalist and Drupalista should use.

This is because Drush, like Drupal, is a multifaceted tool useful for beginners and experts alike.

> It is important to note that many of the **tools** listed are just that, **tools**.
>
> Some will function with your workflow, some will not.

When installing your first site in Drupal on the last page, we walked through many steps, did we not?

Once installed, Drush allows for this:
```
user@machine:~/ | => cd /your-project/
user@machine:~/public_html/drupal/ | master
=> drush site-install --acount-name=admin --account-pass=admin
```

With the correct database information and an understanding of your own project Drush saves lots of time.

Drush is not the only tool

## Scaffolding

What is Scaffolding?

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
# Drupal-8.2.x-dev (2016-April)

core/
modules/
profiles/
sites/
themes/
vendors/
.csslintrc
.editorconfig
.eslintrc
.htaccess
autoload.php
composer.json
example.txt
index.php
LICENSE.txt
README.txt
robots.txt
update.php
web.xml
```
Notice the similarities? From Drupal 6 to Drupal 7, the file structure barely changed at all.

> To reiterate, Dont' Hack Core

The sites/ folder and profiles/ folder is maintained through *all* installations, which is where all Development work happens, whether as a Front End Developer, Back End Developer, Site Builder, or Certified n00b.

When using standardized Drupal Best Practices, the sites/ folder will generally have the same directory structure between installations as well, such as:
```
all/
  - files/
  - modules/
  - themes/
default/
  - files/
  - modules/
  - themes/
  - default.settings.php
  - settings.php
  - local-settings.php
```
*Note - Your installation may not have a local-settings.php file, but you should before moving into production. We can get into that later.*


-----

### Further Reading (Other Tools):

 + [Drupal Console](https://drupalconsole.com/ "Drupal Console"):
  + The new CLI for Drupal. The Drupal Console is a tool to generate boilerplate code, interact and debug Drupal 8.
  + The Drupal Console, while powerful, only works with Drupal 8. Careful deliberation should be made prior to starting any projects using Drupal Console.
  + If chosen, [Pantheon.io](https://pantheon.io/ "Pantheon.io") provides a great beginners tutorials on using both Drush and Drupal Console together. It is available [here](https://pantheon.io/introduction-drush-and-drupal-console "An Introduction to Drush and the Drupal Console").
 + [Gadget](https://github.com/phase2/generator-gadget "Gadget: A Generator for New Drupal Projects"):
   + In short, and taken directly from their site, "Gadget will set up a Drupal project with the site skeleton and tools to build your project and configure your build system with the Grunt Drupal Tasks kit."
   + Made by [Phase2](https://www.phase2technology.com/ "Phase 2: Open Technology, Open Minds"), Gadget uses the [Grunt](http://gruntjs.com/ "Grunt: The Javascript Task Runner") plugin ```grunt-drupal-tasks``` to scaffold Drupal 7 and Drupal 8 sites quickly, efficiently, and with full Grunt workflows!
 + [Aquifer.io](https://aquifer.io/ "")
   + The newest script-kiddy on the block, and made the the Chefs over at [Four Kitchens](https://fourkitchens.com/ "Four Kitchens"), "Aquifer is a command line interface that makes it easy to scaffold, build, test, and deploy your Drupal websites".
   + As the makers of [Pressflow](http://www.pressflow.org/ "Pressflow"), a major Drupal 6 update distribution, the guys at Four Kitchens understand the need for incorporating 'non-standard' modules and themes directly into scripting/scaffolding workflow.
   + As an opinion of this Developer, Aquifer may actually be the most logical choice (to start learning from) because it uses a [Drush make workflow](http://docs.aquifer.io/sections/what-is-a-drush-make-workflow.html "What is a Drush make workflow?").
   + In contrast, however, Aquifer is **Developer** focused

