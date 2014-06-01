# Extending and altering data types

Rules relies on information from the Entity API module to declare data types for each entity on your site. These are complemented by a number of other data types, which are (with machine names in parenthesis): date, decimal number (`decimal`), duration, formatted text (`text_formatted`), integer, text (`text`), text token (`token`), truth value (`boolean`), URI (`uri`) and watchdog log entry (`log_entry`). As previously mentioned, all data types and known entity types are also represented by lists being arrays of the data values.

The formatted text, watchdog log entry and all entities are complex data types, having a number of properties – each property being one
of the declared data types. These properties can be altered and extended by modifying the **properties** array for the data type with help of `hook_entity_property_info_alter()` and `hook_rules_data_info_alter()`.

It should be noted that the globally available data is made available under the key site found in `hook_entity_property()`. The following example shows how a site-wide list of blacklisted words can be added to the site variable, to be used in Rules configuration.

```php
function mymodule_entity_property_info_ alter(&$info) {
  $info['site']['properties']['mymodule_blacklisted'] = array(
    'type' => 'list<text>',
    'label' => t('Blacklisted words'),
    'description' => t('Disallowed words on the site'),
    'getter callback' => 'mymodule_get_blacklisted_words',
  );
}

function mymodule_get_blacklisted_words() {
  return variable_get('mymodule_blacklisted', array());
}
```
