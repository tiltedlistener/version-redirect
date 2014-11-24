# Version Redirect

Allows Drupal sites to redirect all previous aliases of a node to the current node alias. This is intended to allow site and content administrators to update URL aliases with Pathauto to whatever is more fitting to their content or to do bulk updates without fear of breaking old links from internal and external sources.

Aliases are versioned every time an URL alias changes for a node for any number of changes. This includes bulk updates and pattern updates with Pathauto.


## Edge Case Considerations

**Versioned alias is used on another node**

In this case, the standard Drupal routing will direct the user to the correct page. This module only activates when a 404 occurs, so for a versioned alias to be routed successfully, the alias must not exist in the pathauto url_alias table.

**Two nodes end up with the same URL alias in versioning**

The module will present a 302 redirect to a generate page that lists links to all the pages that have that alias. 


## Dependencies 

- Pathauto
- Global Redirect