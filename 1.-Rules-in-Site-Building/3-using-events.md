# Using events

Rules provides a number of **events** – places in a Drupal page load that can be used to fire off actions. Rules that trigger on events are called **reaction rules** (in contrast to stand-alone rule components that must be triggered by other means – see the section about components).

Each event may provide some associated variables, which can be used in the rule configuration. For example, the event **After saving new content** provides the saved content as a node variable while **After updating existing content** provides both the updated and original content as variables – thereby allowing comparison between the two.

A reaction rule may have more than one triggering event. If they provide different variables, only the variables provided by **all** events may be used in the configuration, assuring that the rule may be evaluated properly regardless of which of the events is acting as trigger.