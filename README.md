# php-wechaty-getting-started [![PHP Version](https://img.shields.io/packagist/v/wechaty/php-wechaty)](https://packagist.org/packages/wechaty/php-wechaty) [![PHP CI](https://github.com/wechaty/php-wechaty-getting-started/workflows/PHP%20CI/badge.svg)](https://github.com/wechaty/php-wechaty-getting-started/actions?query=workflow%3A%22PHP+CI%22)

[![PHP Wechaty](https://wechaty.github.io/php-wechaty/images/php-wechaty.png)](https://github.com/wechaty/php-wechaty-getting-started)

PHP Wechaty Starter Project Template that Works Out-of-the-Box
 
[![Wechaty in PHP](https://img.shields.io/badge/Wechaty-PHP-blue)](https://github.com/wechaty/php-wechaty)

## Connecting Chatbots

[![Powered by Wechaty](https://img.shields.io/badge/Powered%20By-Wechaty-brightgreen.svg)](https://github.com/Wechaty/wechaty)
[![PHP Version](https://img.shields.io/packagist/v/wechaty/php-wechaty)](https://packagist.org/packages/wechaty/php-wechaty)

Wechaty is a RPA SDK for Wechat **Individual** Account that can help you create a chatbot in 8 lines of PHP.

## The World's Shortest PHP ChatBot: 8 lines of Code

```php
$wechaty = \IO\Github\Wechaty\Wechaty::getInstance($token, $endPoint);
$wechaty->onScan(function($qrcode, $status, $data) {
    $qr = \IO\Github\Wechaty\Util\QrcodeUtils::getQr($qrcode);
    echo "$qr\n\nOnline Image: https://wechaty.github.io/qrcode/$qrcode\n";
})->onLogin(function(\IO\Github\Wechaty\User\ContactSelf $user) {
})->onMessage(function(\IO\Github\Wechaty\User\Message $message) {
    $message->say("hello from PHP7.4");
})->start();
```

## Usage

### Install

```sh
# Install make sure php is 7.4+
sudo yum install php-pecl-grpc
sudo yum install php-pecl-protobuf
sudo yum install php-xml
# curl -sS https://getcomposer.org/installer | php
php -r "copy('https://install.phpcomposer.com/installer', 'composer-setup.php');"
php composer-setup.php
php -r "unlink('composer-setup.php');"
mv composer.phar /usr/local/bin/composer

make install
```

### Run

```sh
export WECHATY_PUPPET_HOSTIE_TOKEN=your_token_at_here

make bot
```

## Wechaty Getting Started in Multiple Languages

- [TypeScript Wechaty Getting Started](https://github.com/wechaty/wechaty-getting-started)
- [Python Wechaty Getting Started](https://github.com/wechaty/python-wechaty-getting-started)
- [Java Wechaty Getting Started](https://github.com/wechaty/java-wechaty-getting-started)
- [Go Wechaty Getting Started](https://github.com/wechaty/go-wechaty-getting-started)
- [PHP Wechaty Getting Started](https://github.com/wechaty/php-wechaty-getting-started)
- [.NET(C#) Wechaty Getting Started](https://github.com/wechaty/dotnet-wechaty-getting-started)

## Badge

[![Wechaty in PHP](https://img.shields.io/badge/Wechaty-PHP-blue)](https://github.com/wechaty/php-wechaty)

```md
[![Wechaty in PHP](https://img.shields.io/badge/Wechaty-PHP-blue)](https://github.com/wechaty/php-wechaty)
```

## Maintainers

[@wechaty/php](https://github.com/orgs/wechaty/teams/php/members)

## Copyright & License

- Code & Docs © 2020 Wechaty Contributors <https://github.com/wechaty>
- Code released under the Apache-2.0 License
- Docs released under Creative Commons
