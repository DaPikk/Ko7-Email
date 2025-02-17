# Email Module For Koseven (Ported from Leemo Studios Kohana 3.3 Swiwtmailer Emailer)

__Attention!__ This module is very different from the original module. The structure
of this module has been heavily reworked to be more in line with the principles
used in Kohana.

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
