# OS2Web builder Drupal compose project.

Drupal environment is base on [Composer template for Drupal projects](https://github.com/drupal-composer/drupal-project)
See information about how to install and use it on Drupal-composer README page.

It supposed to use [Docksal](https://docksal.io/) as development environment.
See [Docksal documentation](https://docs.docksal.io) to setup project on your local environment 
and start work with it. 

## Builder usage

### `fin cex` command

This command will export Drupal configuration and remove `uuid` and `core` from
all config files inside `./web/modules/custom/*/config` path.

To get your files split to `./web/modules/custom/[your-module]/config` folder,
you should have proper config_split config activated to this project. See 

In case there is no split config for your project, feel free to add it and
commit to project. So other developers could use it during development also.

See command script `.docksal/commands/cex` 

### `fin clean-config [your-config-directory]` command

Command that removes `uuid` and `core` keys from files inside directiry your
will specify as parameter. You will find this command userful if you have
submodules.

To get your files split to `./web/modules/custom/[your-module]/config` folder,
you should have proper config_split config activated to this project. See 

In case there is no split config for your project, feel free to add it and
commit to project. So other developers could use it during development also.

### `fin rebuild` command

You can use this command to get fresh Drupal installation based on standard
profile. After running command you can enable required modules and develop
your modules.

See command script `.docksal/commands/rebuild` 


### `fin rebuild-test` command

This command could be used for testing purposes where all unused modules such
as: Field UI, Config Management, is deactivated.

See command script `.docksal/commands/rebuild-test` 
