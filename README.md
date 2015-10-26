# :mailbox: Homebrew Mailhog

## Don't use this tap, use official repo!
Mailhog formula is now available in official Homebrew repository (see the [PR](https://github.com/Homebrew/homebrew/pull/44884)). This tap is obsolete now and formula file is removed, but installation instructions are updated to guide you through the setup.

## How do I install the formula?
`brew install mailhog`

Or install via URL (which will not receive updates):

```
brew install https://raw.githubusercontent.com/Homebrew/homebrew/master/Library/Formula/mailhog.rb
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
sendmail_path = $HOMEBREW_PREFIX/bin/MailHog sendmail test@test
```

Replace `$HOMEBREW_PREFIX` with the path where your Homebrew is installed. Restart PHP process after you make the change to `php.ini` file. Refer to `brew info mailhog` to see the full path to MailHog on your system.
