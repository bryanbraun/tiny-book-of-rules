# Lists and loops

Each data type declared to Rules automatically gets a sibling data type, being a list of this particular data. Thus, Rules cannot only handle nodes, text strings and dates, but also lists of nodes, strings and dates. This is very useful when working with multiple-value fields, but also for a few multiple-value entity properties, such as the roles of a user.

Rules provides a few actions and conditions that are handy when working with lists: **List contains item**, **Add a value to a list** and **Remove a value from a list**. The latter two can for example be used to add/remove a user from a multiple-value user reference field.

The most useful thing with lists, though, is the ability to **loop** through them. By adding a loop to your set of actions, you have each action inside the loop being evaluated once for every item in the list you select. This can for example be used to send an e-mail to all users in a multiple-value user reference field.

It is possible to use loops within loops, though you should be aware that evaluation may become performance heavy if there are many items to loop over.