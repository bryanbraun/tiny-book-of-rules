# Useful additional modules

There are a number of modules taking advantage of Rules as a framework, or providing new actions, conditions and plugins. The most notable are:

* Rules Scheduler. This module is included in the Rules project, and allows scheduling components to be evaluated at a future point in time. The module can for example be used to schedule content deletion, upgrading of user accounts, or managing recurring e-mails.
* Views Bulk Operations (VBO). This module extends Views and allows users to perform actions on selected rows. Apart from some base-level actions, Rules components may be used as actions by VBO. An equally useful feature of VBO is that it allows calling Views from Rules configuration, to load a list of entities listed by Views.
* Rules Bonus Pack. This module serves as an experimental lab for new Rules functionality, and provides a number of new actions and conditions. It also allows using condition components as CTools access plugins, as well as providing a new component type used for validating and modifying arguments (contextual filter values) in Views.
* Rules Link. This module can be used to attach links to entities, and firing rule sets when these links are clicked. Links can also be rendered using Views, and link visibility can be controlled by condition sets.