
# Woocommerce #Coding Standard Check

This blog is about to make your WordPress/Woocommerce plugin with Woocommerce,Woocommerce-Core,WordPress,WordPress-Core,PHPcs, PHPcf Standard.


## Documentation
Now you'll see here.

[Woocommerce PHP Link Documentation](https://developer.woocommerce.com/testing-extensions-and-maintaining-quality-code/setting-up-linting/)


## Installation of Composer

Before requiring [composer](https://getcomposer.org/doc/00-intro.md) in your project you must have [installed](https://getcomposer.org/doc/00-intro.md) the composer globally
|| To Install composer in the project folder to run for the PHPcs

```bash
  cd my-project
  composer require woocommerce/woocommerce-sniffs
```
    
## After once you installed the composer in you local project

You will need to run following commands to check for the phpcs accroding to woocommerce core

```bash
  ./vendor/bin/phpcs --standard=Woocommerce {Your-project-file-name}
  ./vendor/bin/phpcs --standard=Woocommerce-core {Your-project-file-name}
  ./vendor/bin/phpcs --standard=WordPress {Your-project-file-name}
  ./vendor/bin/phpcs --standard=WordPress-core {Your-project-file-name}
```

Correct code | ( Indent the code lines and function ) you can use below commands 

```bash
    ./vendor/bin/phpcbf --standard=Woocommerce-core {plugin-path-or-dir-path}

```
This above command will show you the Error,Warnning,Notice etc for PHPcs,
Now if you only want to see the error not notice/warning then you have to use this below commands.

```bash
  ./vendor/bin/phpcs --warning-severity=0 --ignore-annotations --extensions=php,html --standard=Woocommerce-core {Your-project-file-name}
```

If you want to generate errors of the file with the following above coammnad then try use this command to get error generated file 

```bash
    ./vendor/bin/phpcs --warning-severity=0 --ignore-annotations --extensions=php,html --standard=Woocommerce-core,Woocommerce,WordPress,WordPress-core --report-file={Where you want to generate files with Errors } { The targeted file on which you want PHPcs report }

```
## Authors

- [@ambikesh-cedcommerce](https://www.github.com/ambikesh-cedcommerce)


## Contributing

Contributions are always welcome!

See `contributing.md` for ways to get started.

Please adhere to this project's `code of conduct`. If there is anything missing or you can to add more I would love that thanks.
