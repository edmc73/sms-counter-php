# Edmc73 - SMS Counter for PHP

Character counter for SMS Messages

## Usage

```php
use Edmc73\SMSCounter\SMSCounter;

$smsCounter = new SMSCounter();
$smsCounter->count('some-string-to-be-counted');
```

which returns
```
stdClass Object
(
  [encoding]    => GSM_7BIT
  [length]      => 25
  [per_message] => 160
  [remaining]   => 135
  [messages]    => 1
)
```

You can sanitize your text to be a valid GSM 03.38 charset

```php
use Edmc73\SMSCounter\SMSCounter;

$smsCounter = new SMSCounter();
$smsCounter->sanitizeToGSM('dadáó'); //return dadao
```

## Installation

`sms-counter-php` is available via [composer](http://getcomposer.org) on [packagist](https://packagist.org/packages/instasent/sms-counter-php).

```json
{
    "require": {
       "edmc73/sms-counter-php": "^0.5"
    }
}
```

## License

SMS Counter (PHP) is released under the [MIT License](LICENSE-MIT.md)

### Mentions

* Original idea : [danxexe/sms-counter](https://github.com/danxexe/sms-counter)
* Fork Idea from: [instasent/sms-counter-php](https://github.com/instasent/sms-counter-php)
