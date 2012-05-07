Munin plugin for monitoring ElasticInbox nodes and Cassandra cluster.

## Installation

Copy `jmx2munin*` to plugins directory (usually `/usr/share/munin/plugins/`). Copy `plugin-conf.d/cassandra` to `/etc/munin/plugin-conf.d/`.

On Cassandra and ElasticInbox nodes create required symlinks using following snippet:
```
for i in `\ls -A jmx2munin`; do echo "ln -s /usr/share/munin/plugins/jmx2munin_ /etc/munin/plugins/$i"; done;
```