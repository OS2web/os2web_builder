## Remove uuid and _core from configs
Run the following from the root of Drupal inside your terminal.

```
cd [drupal-root]
drush cex -y
find ./modules/custom/*/config -type f -exec sed -i -e '/^uuid: /d' {} \;"
find ./modules/custom/*/config -type f -exec sed -i -e '/_core:/,+1d' {} \;"
```

### For Mac OSX
```
cd [drupal-root]
drush cex -y
find /path/to/PROFILE_NAME/config/install/ -type f -exec sed -i '' '/^uuid: /d' {} \;
find /path/to/PROFILE_NAME/config/install/ -type f -exec sed -i '' '/_core:/{N;d;}' {} \;
```
