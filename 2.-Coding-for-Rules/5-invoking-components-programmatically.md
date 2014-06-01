# Invoking components programmatically

Rules components are handy tools for allowing site builders to customize their own actions and conditions. If you are writing a module that allows site builders to set custom conditions (or actions), you can let them set these up as Rules components and then evaluate selected components programmatically. This works in a way analogous to invoking events, by using `rules_invoke_component()`.

The first argument is the (machine) name of the component, and any subsequent arguments are variables sent to the component.

```php
// Included somewhere in your custom module.
$component_name = $settings['rules_component_name'];
// Any variables provided from the component are returned from its evaluation.
$result = rules_invoke_component($component_ name, $var_1, $var_2);
```
