# Components

Reaction rules are the simplest and usually most common Rules configurations. But you can also create Rules **components** – reusable condition sets, action sets, single rules or sets of rules. These components can then be called by reaction rules, saving you the work of repeating the same conditions in three different reaction rules.
Apart from avoiding repetitive work, components may also be invoked by other modules. Views Bulk Operations, for example, can make use of Rules components as actions; Rules

Scheduler can schedule the evaluation of any component for a future point in time; and with the help of Rules Bonus Pack, CTools can use condition components as access plugins in modules like Page manager and Panels.

Components are mainly created and edited like reaction rules – but they have no triggers. They also have configurable variables that are either **parameters** or **provided** (or both). Parameters are required input data for the component – variables that have to be specified when calling the component. Provided variables are returned to the caller after evaluation.

Components are very useful both in site building and coding.