# Extending rules

Normally, extensions of Rules are put into the file mymodule.rules.inc. This way, the file is only loaded when Rules is actually used on a page load, which is good for performance. In this section of the book, all code examples assume that your module is called mymodule.

The following sections only contain the very basics of extending Rules. More detailed documentation can be found at the online documentation ([http://www.drupal.org/node/878720](http://www.drupal.org/node/878720)) and in `rules.api.php` included in the Rules project.