# {{ book.sections.new_users.you_need_drush }}

If you are a Mac or Linux user, you really, *really* need [Drush](http://docs.drush.org/en/master/install/).

Even if you are a beginner, Drush is a tool **every** Drupalist and Drupalista should use.

This is because Drush, like Drupal, is a multifaceted tool useful for beginners and experts alike.

> It is important to note that many of the **tools** listed are just that, **tools**.
>
> Some will function with your workflow, some will not.

When installing your first site in Drupal on the last page, we walked through many steps, did we not?

Once installed, Drush allows for this:
```bash
user@machine:~/ | => cd /your-project/
user@machine:~/public_html/drupal/ | master
=> drush site-install --acount-name=admin --account-pass=admin
```

Drush also allows for this:
```bash
drush @site.env cc all (Drupal 7)
drush @site.env cache-rebuild (Drupal 8)
```

With the correct database information and an understanding of your own project Drush saves lots of time.

Drush is not the only tool for Site Maintenance and Admininistration (see the next page).

Drush **is** the must-have tool, however.

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

