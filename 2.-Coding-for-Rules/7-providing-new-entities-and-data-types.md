# Providing new entities and data types

Just as existing data types can be altered, new ones can be added. This is done by implementing `hook_rules_data_info()`. An example of this is displayed below, where views are being introduced as a data type in Rules.

```php
Function mymodule_rules_data_info() {
  $data_types = array(
    'mymodule_view' => array(
      'label' => t('view object'),
      'wrap' => TRUE,
      'property info' => array(
        'machine_name' => array(
          'type' => 'text',
          'label' => t('Machine name'),
        ),
        'args' => array(
          'type' => 'list<text>',
          'label' => t('Arguments'),
          'setter callback' => 'entity_property_verbatim_set',
        ),
      ),
    ),
  );
}
```

Especially note the **wrap** property, which makes Rules wrap the passed object and make it available for data selection. It is required for any complex data type. Two properties are declared in the **property info** array, which will make it possible to read these properties in Rules. Also, the **args** property has a setter callback – meaning that Rules cannot only read but also write the arguments of the view object.

It so happens that the properties’ machine names correspond directly to properties in the view object. If this wasn’t the case, a **getter callback** would have been required to tell Rules how to read the property, just as it works for entity properties. Now the default callback `entity_property_verbatim_get()` is used, which like its setter sibling simply writes to the data object using the declared machine name as property name.

New entity types are declared using `hook_entity_info`. Its usage is not documented here, but if your entities are declared properly for the Entity API modules, Rules will know about them too.
