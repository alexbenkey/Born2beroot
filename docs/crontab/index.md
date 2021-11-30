# Crontab & Cronjobs

Crontab is a scheduling service that can automate certain tasks for you like creating backups or in our case annoy us every 10 minutes with a shitty popup!

## Adding a cronjob

Simply run ```crontab -e``` as root and you will be see something like this:
![cron](/images/cron.png)

I highly recommend [this site!](https://crontab.guru/#*/10_*_*_*_*)

The way it works is that you got timers for every minute, hour, day, month and year which you can specify to a specific value. Now the subject requires us to run the script every 10 minutes. We can do so like this:

```bash
#Runs every 10th minute of the hour
*/10 * * * * bash /etc/monitoring.sh
```

## Starting and stopping the service

One requirement is to start and stop cron without touching anything, except the command line.

### Start
```bash
#Starts the service...
/etc/init.d/cron start
```

### Stop
```bash
#Stops the service...
/etc/init.d/cron stop
```

This is actually it, yeah theres not much to it.
