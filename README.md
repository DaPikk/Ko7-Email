[![CI workflow](https://github.com/DaPikk/Ko7-Email/actions/workflows/php.yml/badge.svg)]()
[![Required minimum PHP Version](https://img.shields.io/badge/PHP-7.4>8.1-blue)]()
[![Required minimum Ko7even Version](https://img.shields.io/badge/Ko7even-=>3.3.8-blue)](https://github.com/koseven/koseven)
[![Required SwiftMailer Version](https://img.shields.io/badge/SwiftMailer-6.0-blue)](https://swiftmailer.symfony.com/)
[![Github Issues](https://img.shields.io/github/issues/dapikk/ko7-email.svg)](https://github.com/dapikk/ko7-email/issues)

# Email Module For Koseven (Ported from Leemo Studios Kohana 3.3 Swiwtmailer Emailer)
[![Original code](https://img.shields.io/badge/Leemo-Kohana_swift_mailer_(2016)-red)](https://github.com/Leemo/kohana-swift-mailer)

__Attention!__ This module is very different from the original module. The structure
of this module has been heavily reworked to be more in line with the principles
used in Kohana.

## Requires
* PHP 7.4 - 8.1
* Ko7even => 3.3.8
* SwiftMailer => 6.0

## Download
![Latest release](https://github.com/DaPikk/Ko7-Email/releases/latest)

## Installation

Edit your bootstrap file `APPPATH/bootstrap.php` and enable email module:

~~~
Koseven::modules(array(
  // ...
  'email' => MODPATH.'email',
  // ...
  ));
~~~

Then copy `MODPATH/email/config/email.php` to `APPPATH/config/email.php`.

NB! If swiftmailer is not included in the vendor folder, download proper swiftmailer version as per composer.json:
"swiftmailer/swiftmailer": "^6.0"
NB! "Swift Mailer" will stop being maintained at the end of November 2021.

Well done!

## Example of usage

~~~
Email::instance()
  ->from('sender@example.com')
  ->to('recipient_1@example.com')
  ->to('recipient_2@example.com', 'Mr. Recipient')
  ->subject('Hi there!')
  ->body('Hi, guys! This is my awesome email.')
  ->send();
~~~

Enjoy!
