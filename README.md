# speedtestmail

This command line script sends out an email with your current internet connection bandwidth. It is basically a very simple wrapper around [speedtest-cli](https://github.com/sivel/speedtest-cli) and mail. I run it from cron to keep track of my varying internet bandwidth.

# Prerequisites
1. Make sure you have [speedtest-cli](https://github.com/sivel/speedtest-cli) installed and operational.
2. Also make sure you can send emails from your command line as follows:
```
$ echo "42" | mail -s "The answer to life the universe and everything" someone@gmail.com
```

# Install
```
curl -sSL https://raw.github.com/roubles/speedtestmail/master/webinstall.sh | bash
```

# Usage
```
$ speedtestmail someone@gmail.com,someoneelse@gmail.com
```

# Cron usage
I run it once every hour as follows:
```
0 * * * * speedtestmail someone@gmail.com,someoneelse@gmail.com
```

# Uninstall
```
curl -sSL https://raw.github.com/roubles/speedtestmail/master/webuninstall.sh | bash
```
