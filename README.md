maintains a cache of user login data gleaned from minecraft
logs... cache data is maintained even as logs are deleted, so it only
needs occasionally updated (before logs that haven't been analyzed are
deleted).

quick and dirty:

* edit config.sh to reflect your paths
* run update_lastlog to build the cache
* use listuser to see results

You can set up update_lastlog to run from cron.  It will not duplicate
data when you feed it logs it has seen before.  As long as you run it
before logs it hasn't seen are rotated out of existence, the cache
will be accurate.


[needs more formal treatment]
