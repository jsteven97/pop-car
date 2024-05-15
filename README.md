# How to run this project in local

## Run the following commands
 - `git clone <repo>`
 - `ddev start`
 - `ddev composer install`
 - `ddev drush config:set system.site uuid 09aa893d-74c2-47d3-9aa2-e1f81313a6e6 -y`
 - `ddev drush entity:delete shortcut`
 - `ddev drush entity:delete shortcut_set default`
 - `ddev drush cim -y && ddev drush cr`
 - `ddev drush uli`

