Convenient_SetupScriptsDisabler
====================

Disables the automatic application of setup scripts in Magento, this is cool because

1. It's a little performance boost, we don't need to be checking for setup scripts every time Mage::run is called as setup scripts should be run during the deployment process
2. It is safer. If you went wild and deployed to a busy server it is possible that setup scripts could be initiated multiple times by multiple processes. This could cause your database to get into unexpected or corrupted states.

`n98-magerun sys:setup:run` is my preferred method of running setup scripts. 

Just pop it (and your preferred composer installer / autoloader) in your composer.json and it's all ready to go.

```
{
    "require": {
        "magento-hackathon/magento-composer-installer": "~2.0",
        "convenient/setupscriptsdisabler":"~0.2"
    },
    "repositories": [
        {
            "type": "composer",
            "url": "http://packages.firegento.com"
        }
    ],
    "extra": {
        "magento-root-dir":"./",
        "magento-force":"override"
    }
}

```
