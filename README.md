Convenient_SetupScriptsDisabler
====================

Disables the automatic application of setup scripts in Magento.

n98-magerun sys:setup:run is my preferred method of running setup scripts. 

Just pop it in your composer.json and it's all ready to go.

```
{
    "require": {
        "magento-hackathon/magento-composer-installer": "~3.0@alpha",
        "convenient/setupscriptsdisabler":"~0.1"
    },
    "repositories": [
        {
            "type": "composer",
            "url": "http://packages.firegento.com"
        }
    ],
    "extra": {
        "magento-root-dir":"./",
        "magento-deploystrategy":"copy"
    }
}

```
