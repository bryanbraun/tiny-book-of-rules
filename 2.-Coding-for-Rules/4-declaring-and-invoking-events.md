# Declaring and invoking events

Events are declared with an info hook – `hook_rules_event_info()` – very similar to the previous ones. An important difference is the key used to declare event variables:

```php
$events = array(
  'mymodule_rules_event_id' => array(
    'group' => t('My module'),
    'label' => t('My event'),
    'variables' => array(
      'var_1' => array(
        'type' => 'node',
        'label' => t('Node provided by the event'),
      ),
    ),
  ),
);

return $events;
```

Events are not invoked by their own callbacks. Rather, they are invoked by adding the `rules_invoke_event()` function somewhere in the execution cycle. The first parameter used with this function is the name of the event to call, and any subsequent parameters are being passed as variables to the Rules event:

```php
// Placed in your custom module to react in the execution cycle
rules_invoke_event('mymodule_rules_event_id', $node);
```

An alternative to `rules_invoke_event` is the `rules_invoke_event_by_args()` function. It takes two parameters only, the first being the name of the event and the second being an array of variables to pass to the event.
