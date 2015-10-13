# :mailbox: Homebrew Mailhog
## How do I install thee formula?
`brew install maijs/mailhog/mailhog`

Or `brew tap maijs/mailhog` and then `brew install mailhog`.

Or install via URL (which will not receive updates):

```
brew install https://raw.githubusercontent.com/maijs/homebrew-mailhog/master/mailhog.rb
```

## Usage
There are couple of ways to start `MailHog`:

1. Run `brew services start mailhog` if you have [`homebrew-services`](https://github.com/Homebrew/homebrew-services) tap installed.
2. Run `$(brew --prefix)/bin/MailHog &` if you want to start it manually.

Open `http://127.0.0.1:8025` and start using. (Give it couple of seconds to boot.)

## Configuration
If you want to run MailHog manually, you can use [command line options](https://github.com/mailhog/MailHog/blob/master/docs/CONFIG.md) to configure MailHog.

# MailHog as sendmail replacement
To use MailHog as a sendmail replacement for PHP, add the following line to your `php.ini` file:
```
sendmail_path = (HOMEBREW_PREFIX)/bin/MailHog sendmail test@test
```
Restart PHP process after you make the change to `php.ini` file. Refer to `brew info mailhog` to see the full path to MailHog on your system.

## Please note
This repository is for my own testing only and it can be removed at any time. The goal is to have `mailhog.rb` formula available in official Homebrew repo.