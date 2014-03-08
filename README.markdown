## Hyperic HQ CouchDB plugin

This project is a Hyperic HQ plugin for monitoring [CouchDB](http://couchdb.apache.org/)
derived from [github.com/hyperic/hq-couchdb](http://github.com/hyperic/hq-couchdb) and ported
to hyperic 5.7.x

### Auto-Discovery

The CouchDB server process is auto-discovered and monitoring properties are configured
using the couch .ini files.  The Database service discovery creates an instance for each
database list in *_all_dbs*

### Metrics

Server process metrics are collectd via SIGAR.

The runtime metrics available in 0.9+ are collected via the *_stats* module,
see: <http://wiki.apache.org/couchdb/Runtime_Statistics>

The Database service collects status metrics via */dbname*,
see: <http://wiki.apache.org/couchdb/HTTP_database_API>

### Log File Tracking

Messages are optionally reported from couchdb.log and can be filtered by severity level
and/or regex include/exclude.

### Config File Tracking

Each .ini file can be watched for changes.

### Control Actions

None yet.

### Dependencies

[jcouchdb](http://code.google.com/p/jcouchdb/) - see LICENSES file for details.

### CouchDB version support

Tested versions on Linux:

### Hyperic HQ version support

Tested with [vFabric Hyperic EE](https://www.vmware.com/support/pubs/hyperic-pubs.html) version 5.7.1

