About Us
--------
* Developing on Drupal for about 2 years
* Mix of government and private sites (MLKday.gov, VISTA Campus, Bankers Without Borders)
* Baltimore | Austin | Jackson 

Overview
========
* PHP & MySQL (standard LAMP stack).
* Drupal Pros (Modularity, Flexibility, Stability, Community).
* Drupal Cons (Bare bones, Steep learning curve, modules not always plug and play, Hard for lay users, lack of decent themes).
* What it's good for: Large custom sites, Enterprise level sites, Gov sites, multiple content heavy sites.
* Some examples: [data.gov.uk](http://data.gov.uk), [The Economist](https://drupal.org/node/915102), [The Whitehouse](http://www.whitehouse.gov/), [Smithsonian Institution Transcriptions](http://transcription.si.edu/), [Harvard.edu](http://www.harvard.edu/), [NASA](http://www.nasa.gov/), [Fast Company](http://www.fastcompany.com/), and [Amnesty International](http://www.amnesty.org/).

Whats Now
-------
* Drupal 7.
* 26,110 contributed modules.
* Over 1,047,545 Community users on D.O.

What's Cool
==========

Distributions
----------
Generally speaking, Distributions combine core Drupal, contributed modules, themes, and pre-defined configuration into one download.
* Also can create your own distro/configure your own custom Installation Profile. (public or Private). We have a base Distro we created with basic modules/settings we re-use for most builds.
* Distros are great for standing up a complete (ish) site (saves time for quick builds, beginers). Also, sometimes it can be helpful to deconstruct operations you may wish to mimic/modify.
* A word of warning on Distros, watch out for those with custom Modules.
* Some good examples: [Commerce Kickstart](https://drupal.org/project/commerce_kickstart), [OpenPublic](https://drupal.org/project/openpublic), [OpenChurch](https://drupal.org/project/openchurch).

Sub Themes
----------
Like WordPress, Drupal allows you to utilize sub themes. This is especially awesome if you utilize either your own, or a public distro.
* Overwrite any core, or parent theme file, without hacking core, or the parent distro theme.
* Overwrite any module files without hacking contrib modules. (Super important if handing it off to a client).
* Overwrite Views templates, either generally, or for a specific view only.

Views
----------
[Views](https://drupal.org/project/views), simply put, is a game changer. It alows custom cultivation, filtering, and display of any content on your site. It is one of the most powerful site building tools in any CMS I have dealt with.

Views is that it is a tool to build queries. You can even inspect the query as you build it, if you like. It then stores that query in the DB, and can be accessed in any number of ways. You can create custom blocks, custom pages, hardcode a view into a PHP template, sky's the limit.

The real power of Views comes when you start exploring relationships with content. Any CMS can display a list of related content, but it gets trickier when you want to pull in seperate content types. Views makes it easy to spin up complicated displays of inter-related content, as well as make it filterable to the end user if desired.

* Think of queries within queries, displaying sub/related content via passing along things like node or taxonomy ID's.
* One blessing and curse of Views is that the queries are stored in the DB. This makes it easier for non programers to use/modify, but has the obvious drawback of being lost if the DB gets corrupted. So back it up! You can also export Views as PHP queries, if you prefer to hardcode/etc.
* Be sure to "disable" the Views UI module on live sites, this will ensure company admins can't mess things up, unless the have permissions to enable modules, or are smart enough to know what they are doing if they are a super user.

Services
----------
[Services](https://drupal.org/project/services) provides a standard way of integrating external applications with Drupal sites. Service callbacks may be used with multiple interfaces like REST, XMLRPC, JSON, and more.
* Interface with node/user/taxonomy/etc.
* You can also integrate with Views via [Views Services](https://drupal.org/project/services_views). Awaesome!
* Need [oAuth](https://drupal.org/project/oauth) on that? No problem.

Drush
----------
[Drush](http://www.drush.org/) is a Drupal specific command line tool (shell and Unix scripting interface) for either local, or remote.
* Downloading and activating modules is now as simple as this: drush en module_name -y
* Can also update core,clear cache, run cron, run SQL operations, spin up core (or Distro) instances, create users, and a whole, whole lot more.

Devel
---------
A suite of modules containing fun for module developers and themers.
* Pretty Print arrays of nodes/views/etc for debugging/custom theming.
* Generate dummy users, nodes, and taxonomy terms for sandboxing/building.

Whats Next
-------
* Drupal 8 (Feature freeze, release goal mid 2014)
* Views integration out of the box
* Web services out of the box (including views, also see Symphony note below)
* Drush out of the box.
* New field types to core (Date, Link, Phone, etc)
* Multi Lingual Improvements
* More object oriented code (classes, inheritance, interfaces, etc)
* Admin UX improvments, Mobile optimization
* [Symphony Framework](http://symfony.com/) Components. An underlying framework that is a first-class REST citizen.
* Templates will utilize [TWIG](http://twig.sensiolabs.org/) library! Embrace the brace. No need to know $node->foo vs. $node['foo'] vs. print $foo vs. print render($foo) anymore!
* More industry standard external libraries ([Composer]
(https://getcomposer.org/), [PHPUnit](http://phpunit.de/), [Guzzle](http://guzzle.readthedocs.org/en/latest/#), [Assetic](http://symfony.com/doc/current/cookbook/assetic/asset_management.html) and more)
* Configuration Management support (Dev > Stage > Prod)
