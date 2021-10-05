# pool

A miner pool for Gaman Blockchain. Gaman is an Blockchain which containing GAN Coin as the main cryptocurrency. This blockchain is forked from Arionum (ARO) Blockchain.

Live version: https://pool1.gaman.web.id

The pool requires a full node running on the same server (on a different subdomain) as it uses it's libraries and db connection.

## Install

The requirements are the same as for the Gaman node:

- php 7.2 (with argon2)
- php-openssl
- php-gmp
- php-bcmath
- composer

## Usage

1. Create a new database for the pool (separate from the node one).
2. Edit the `config.php` and follow the instructions inside.
3. Import the `contrib/pool.sql` to your NEW mysql database.
4. Chmod the cache directory using `chmod 777 cache -R`.
5. Run composer install or composer update. If any problems with required dependency, please try to run sudo composer install --ignore-platform-reqs or sudo composer update --ignore-platform-reqs
6. Create a cron entry using the following format:
   ```bash
   */10 * * * * user php /path/to/pool/payments.php
   ```

Start the poolsanity by running:

```bash
php /path/to/pool/poolsanity.php &>/dev/null &
```

## Notes

For the template system, we use [raintpl3].

Please use a new name instead of [pool1] to avoid user confusion!

This project is early alpha, bugs may be found, functions might not work properly etc.

[pool1]: https://pool1.gaman.web.id
[raintpl3]: https://github.com/feulf/raintpl3

## Development Fund

Coin | Address
---- | --------
[ARO]: | UnhhKyFdmdRrHDFxEyLJ76Q1JSxYfGptjj3W2hTJDkDpv2j9prUEsC6EwaGDMgHF4DA8QvR7vKCy4sKpE8tLfqa
[LTC]: | 
[BTC]: | 
[ETH]: | 
[BCH]: | 

If you'd like to support the Gaman Blockchain development, you can donate to the addresses listed above.

[aro]: https://arionum.com
[ltc]: https://litecoin.org
[btc]: https://bitcoin.org
[eth]: https://ethereum.org
[bch]: https://www.bitcoincash.org