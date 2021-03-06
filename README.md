# TRON API
A PHP API for interacting with the Tron Protocol

[![Latest Stable Version](https://poser.pugx.org/iexbase/tron-api/version)](https://packagist.org/packages/iexbase/tron-api)
[![Software License](https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square)](LICENSE)
[![Build Status](https://api.travis-ci.com/iexbase/tron-api.svg?branch=master)](https://travis-ci.com/iexbase/tron-api)
[![Issues](https://img.shields.io/github/issues/iexbase/tron-api.svg)](https://github.com/iexbase/tron-api/issues)
[![Pull Requests](https://img.shields.io/github/issues-pr/iexbase/tron-api.svg)](https://github.com/iexbase/tron-api/pulls)
[![Contributors](https://img.shields.io/github/contributors/iexbase/tron-api.svg)](https://github.com/iexbase/tron-api/graphs/contributors)

## Install

```bash
> composer require iexbase/tron-api
```
## Requirements

The following versions of PHP are supported by this version.

* PHP 7.1
* PHP 7.2

## Example Usage

```php
use IEXBase\TronAPI\Tron;

$tron = new Tron();

//Change node address
$fullNode = new HttpProvider('https://api.trongrid.io:8090');
$solidityNode = new HttpProvider('https://api.trongrid.io:8091');
$tron - new Tron($fullNode, $solidityNode);

//alternative way to enter a private key
$tron->setPrivateKey('private_key');

//Balance
$tron->fromTron($tron->getBalance());

// Transfer Trx
var_dump($tron->sendTransaction('from', 'to', 'amount'));

//Generate Address
var_dump($tron->generateAddress());

//Get Last Blocks
var_dump($tron->getLatestBlocks(2));

//Change account name (only once)
var_dump($tron->changeAccountName('address', 'NewName'));
```

## Testing

``` bash
$ vendor/bin/phpunit
```

## Donations
**Tron(TRX)**: TRWBqiqoFZysoAeyR1J35ibuyc8EvhUAoY
