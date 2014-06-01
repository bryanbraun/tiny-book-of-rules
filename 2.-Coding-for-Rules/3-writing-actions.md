# Writing actions

Conditions are very similar to conditions in their structure: a function carrying out the action, and an info hook implementation to tell Rules about it – in this case `hook_rules_actions_info()`. An important difference is that while conditions return TRUE or FALSE, actions may return new data objects to Rules. See example below.

```php
$actions = array(
  'mymodule_rules_action_fetch_user_recent_content' => array(
    'group' => t('My module'),
    'label' => t('My action'),
    'parameter' => array(
      'var_1' => array(
        'type' => 'user',
        'label' => t('Fetch latest content from this user'),
        'save' => TRUE,
      ),
    ),
    'provides' => array(
      'var_2' => array(
        'type' => 'node',
        'label' => t('Most recent content'),
      ),
    ),
  ),
);
return $actions;
```

Especially note the **provides** property, describing the variable(s) returned from the action. When writing the action callback, make sure it returns an array containing the variable(s) that Rules expects. The keys for the return array must match the keys in the info hook. The **save** property for the `var_1` parameter means that Rules saves the passed variable if the action was successfully executed. Rules will normally wait with saving the changed entities and other data until execution is finished, to avoid multiple saves.

```php
function mymodule_rules_action_fetch_user_recent_content ($var_1) {
  // Code to fetch a node object goes here...
  return array(
    'var_1' => $account,
    'var_2' => $node,
  );
}
```