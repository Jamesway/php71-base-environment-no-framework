# php71 environment without laravel
Installs router, dependency injection container (DIC), data mapper ORM, logger, and a BDD test framework

```


docker run --rm -itv $(pwd):/app jamesway/php71-cli-dev composer nikic/fast-route \
                                                              && php-di/php-di \
                                                              && ramsey/uuid \
                                                              && doctrine/orm \
                                                              monolog/monolog

# dev
docker run --rm -itv $(pwd):/app jamesway/php71-cli-dev composer require --dev phpspec/phpspec

# optional\*
docker run --rm -itv $(pwd):/app jamesway/php71-cli-dev composer require --dev php-console/php-console
```

\*From packagist: PHP Console allows you to handle PHP errors & exceptions, dump variables, execute PHP code remotely and many other things using Google Chrome extension PHP Console and PhpConsole server library.

Google Chrome extension PHP Console https://chrome.google.com/webstore/detail/php-console/nfhmhhlpfleoednkpnnnkolmclajemef
PhpConsole server library https://github.com/barbushin/php-console