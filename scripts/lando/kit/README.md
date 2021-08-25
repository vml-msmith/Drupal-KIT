# Drupal KIT Docksal Commands
The project uses [Docksal](https://docksal.io/) for local-environment development and project-building. To get these to
install correctly for your project, make sure that `".docksal/commands/kit": ["vmlyr-drupal/kit-docksal-commands"],` is
set correctly in the `extra / installer-paths` section of the project's composer.json file.

 The following is a list of the KIT-specific Docksal commands included:
 - `kit/check-url` – Runs through the collection of URLs and checks whether they appropriate match their requested
 response (default is 200). Can also count number of errors logged when pages were checked.
 - `kit/conf` – A wrapper command used in lieu of `drush cex`/`cim` which helps handle environment-specific
 configuration export and import. **Please Note: To correctly export _as_ an environment, the environment first needs to
 be imported. The changes can then be made and exported. This makes sure that there is no environment cross-polution.
 Typically, importing and exporting as "local" is the most fool-proof way of handling configuration unless an
 environment-specific change needs to be made.**
 - `kit/gulp` – Wrapper command to run the npm gulp commands inside theme source directory.
 - `kit/init-db` – To initialize or reinitialize one or multiple site's databases based on their drush alias files.
 - `kit/npm` – Wrapper command to run the npm gulp commands inside theme source directory.
 - `kit/phpcbf` – Run Code Beautifier & Fixer (`phpcbf`) against a given path.
 - `kit/phpcs` – Run Code Sniffer (`phpcs`) against a given path.
 - `kit/sync` – Sync database (and optionally files) to a local environment from an external environment. After the
 database is imported, the site runs various updates and imports configuration as a specified (default: local)
 environment.
 - `kit/theme` – Use this command to auto-create new themes based on VMLY&R's scaffolding themes.
