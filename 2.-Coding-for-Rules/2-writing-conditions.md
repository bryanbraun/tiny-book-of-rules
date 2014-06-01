# Writing conditions

Conditions are the least complex Rules extension. To provide new conditions to Rules, you need two things – a function returning TRUE or FALSE, and an implementation of `hook_rules_condition_info()` to tell Rules about your condition. The info hook should return an array on the following form:

```php
$conditions = array('mymodule_rules_condition_check_a_node_value' => array(
  'group' => t('My module'),
  'label' => t('My condition'),
  'parameter' => array(
    'var_1' => array(
    'type' => 'node',
    'label' => t('Condition parameter 1 (node)'),
  ),
  'var_2' => array(
    'type' => 'text',
    'label' => t('Condition parameter 2 (text)'),
  ),),
);),
return $conditions;
```

The outermost key in the array above is by default the name of the callback function for the condition – more than one condition can be declared by adding more keys. As usual, make sure to prefix your functions with your module name. Especially note the property **parameter**, used for telling Rules which type of data the condition uses as input. There can be any number of parameters – including none – for a condition callback. These are used by the callback function, which returns TRUE or FALSE:

```php
function mymodule_rules_condition_check_a_ node_value($var_1, $var_2) {
// Condition logic goes here...
  return $result;
}
```
