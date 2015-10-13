# Homebrew Mailhog
## How do I install thee formula?
`brew install maijs/mailhog/mailhog`

Or `brew tap maijs/mailhog` and then `brew install mailhog`.

Or install via URL (which will not receive updates):

```
brew install https://raw.githubusercontent.com/maijs/homebrew-mailhog/master/mailhog.rb
```

## Configuration
If you want to run MailHog manually, you can use [command line options](https://github.com/mailhog/MailHog/blob/master/docs/CONFIG.md) to configure MailHog.

# MailHog as sendmail replacement
To use MailHog as a sendmail replacement for PHP, add the following line to your `php.ini` file:
```
sendmail_path = (HOMEBREW_PREFIX)/bin/MailHog sendmail test@test
```

Refer to `brew info mailhog` to see the full path to MailHog on your system.

## Please note
This repository is for my own testing only and it can be removed at any time. The goal is to have `mailhog.rb` formula available in official Homebrew repo.