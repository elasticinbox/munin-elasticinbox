Munin plugin for monitoring ElasticInbox nodes and Cassandra cluster.

## Installation

Plugin has to be installed in each Cassandra and ElasticInbox node.

First, copy plugin and config files:
```
mv jmx2munin* /usr/share/munin/plugins/
mv plugin-conf.d/* /etc/munin/plugin-conf.d/
```

Second, create required symlinks using following snippet:
```
for i in `\ls -A /usr/share/munin/plugins/jmx2munin`; do echo "ln -s /usr/share/munin/plugins/jmx2munin_ /etc/munin/plugins/$i"; done;
```

## Credits

Based on __jmx2munin__ plugin from https://github.com/tcurdt/jmx2munin