# Website skeleton

## Folderstructure:
- bin folder (for commandline scripts / cronjobs)
- cache folder (for all temporary or caching files, this should be the only directory that needs to be writable)
- config folder (for all the configuration settings)
- public folder (like d'uh, how else are you going to show people stuff?)
    - assets
        - css (for all the compiled css files, make sure you have a filewatcher running)
        - js (for all the javascript files)
        - img (for all images)
- scss (for all the scss files that need to be compiled)
- templates (for all the twig templates)
- tests (for all the unit tests)

## Included packages:
- scssphp/scssphp 
- twig/twig
- squizlabs/php_codesniffer version 3.5+ (dev only)
- phpunit/phpunit version 7 (dev only)

Note:
I have included the codesniffer package, so you can check on PSR12 standards. 

## Autoloading:
This skeleton will have the App namespace, therefor the autoloading maps the src file to the App namespace.

Also included in the package is a config.php.template file, 
this will be the template for the config.php file located in the config folder.
This config.php file is also fitted with the App namespace, and included in the composer autoloading.

## Automated Github testing:
To make sure the codebase is properly compliant, i've added a github workflow action. 
This action will do a codesniffer check on every pull request. 
