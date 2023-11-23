# WooCommerce Coding Standard Check

This repository focuses on ensuring your WordPress/WooCommerce plugin complies with WooCommerce, WooCommerce-Core, WordPress, WordPress-Core, PHPcs, and PHPcf standards.

## Documentation

Find detailed documentation on WooCommerce PHP linting [here](https://developer.woocommerce.com/testing-extensions-and-maintaining-quality-code/setting-up-linting/).

## Installation with Composer

Before requiring [Composer](https://getcomposer.org/doc/00-intro.md) in your project, ensure you have it [installed globally](https://getcomposer.org/doc/00-intro.md). To install Composer in your project folder for PHPcs, run:

```bash
cd my-project
composer require woocommerce/woocommerce-sniffs
After Composer is installed in your local project, use the following commands to check PHPcs according to WooCommerce core:

bash

./vendor/bin/phpcs --standard=WooCommerce {Your-project-file-name}
./vendor/bin/phpcs --standard=WooCommerce-core {Your-project-file-name}
./vendor/bin/phpcs --standard=WordPress {Your-project-file-name}
./vendor/bin/phpcs --standard=WordPress-core {Your-project-file-name}
Correct your code by indenting lines and functions using:

bash

./vendor/bin/phpcbf --standard=WooCommerce-core {plugin-path-or-dir-path}
To see only errors (notices/warnings), use:

bash

./vendor/bin/phpcs --warning-severity=0 --ignore-annotations --extensions=php,html --standard=WooCommerce-core {Your-project-file-name}
Generate error files with:

bash

./vendor/bin/phpcs --warning-severity=0 --ignore-annotations --extensions=php,html --standard=WooCommerce-core,WooCommerce,WordPress,WordPress-core --report-file={Error-file-location} {Targeted-file-for-Phpcs-report}
WooCommerce Linter Testing Tip
Products on the WooCommerce Marketplace adhere to WooCommerce linter rules. Test your product before submitting it for Marketplace consideration:

Install PHP and Composer on your computer or in a Docker environment.
Inside wp-content, install woocommerce-sniffs with composer install woocommerce/woocommerce-sniffs.
Add a file named pbs-rules-set.xml with this content.
Inside wp-content, run the following (replace "productname" with your product's directory):
bash

php ./vendor/bin/phpcs --standard=pbs-rules-set.xml --warning-severity=0 --report-source --report-full=phpcs-report.txt --ignore-annotations --extensions=php,html themes/themename
The report will be created in a file called phpcs-report.txt.

Authors
@ambikesh-cedcommerce
Contributing
Contributions are always welcome! See contributing.md for ways to get started. Please adhere to this project's code of conduct. If there is anything missing or you want to add more, we would appreciate it. Thank you!


Make sure to replace the placeholder link in the `pbs-rules-set.xml` section with the actual content or link you want to provide for that file.
