# Using Conditions

When a reaction rule is fired, or in other occasions where rules are used, you have the options to check a number of **conditions** and abort any actions if the conditions aren’t met. Conditions can be pretty specific, such as **Content is promoted to front page, Data value is empty** or the comparison between two text strings – but the most used condition is called **Data comparison**. This one is used to compare two variables available to Rules, or to compare a data variable to a manually entered value
– for example to check if a field has a certain value or if the node author is the same as the acting user.

Conditions can be logically grouped to create **and** and **or** groups. These groups may in turn contain other logical groups.

There are two conditions that are particularly important when working with fields: **Content is of type** and **Entity has field**. These conditions allows Rules to know that an entity has a particular field, and subsequently makes the field data available in configuration. The condition **Entity is of type** has a similar role to provide entity-specific data, but is used much less frequently. (You can also use the **Data comparison** condition to check the entity bundle.)