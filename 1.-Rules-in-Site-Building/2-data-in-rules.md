# Data in Rules

Actions, and other plugins in Rules, act on specified data types. These data can be simple, such as text, integers and dates; or complex like nodes – which in turn have properties represented by data, such as node id (integer), title (text), or creation date (date). Complex data types may have properties which are complex, too – each node has, for example, an author represented by a user account (which in turn has a number of properties).

Some properties are writable, which means that you can alter these with Rules actions. The action **Set a data value** is particularly useful, and can be used to set any writable data.

For most action parameters, it is possible to switch between **direct input**, meaning manually written input, and **data selection**, a tool for drilling down into the nested properties of complex data types.

The data object site is always available in Rules, containing global site data such as the account for the acting user, the site name, and some other information.

Finally, it should be noted that field values are read- and writable **only if Rules can be certain that the relevant entity has that field**. If working with a node, for example, a field will only appear if conditions have been set that limits the rule to selected content types (see [using conditions](4-using-conditions.md) for more information). If the entity doesn’t have separate bundles – such as users – Rules can access the fields right away.
