# Using actions

Rules actions are reactions that Rules may perform. Some actions return new data that Rules can work with – such as loading the most recent comment written by a user – but most actions only deal with the data already available to Rules.

Some common actions are:

* Add a variable: This adds a new variable into your configuration, which then can be manipulated and used.
* Calculate a value: This allows you to perform basic arithmetics with numbers.
* Create a new entity: This asks for required data for an entity, and then creates it.
* Fetch entity by id: This allows for fetching nodes and other entities by id.
* Fetch entity by property: This allows for fetching all entities matching selected criteria, for example a selected field value.
* Show a message on the site: This displays an on-site message.
* Publish/unpublish content.
* Create or delete any URL alias.
* Send an e-mail.
* Set a data value (described below).

Actions can be combined in chains, which allows for rules loading new objects and then acting on them. Contributed modules may provide more actions to Rules.