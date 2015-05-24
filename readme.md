# Docker RethinkDB Python Driver

Docker container for RethinkDB Python driver, for backup/restore.

Has the following commands:

- rethinkdb-dump
- rethinkdb-export
- rethinkdb-import
- rethinkdb-index-rebuild
- rethinkdb-restore


Backup
```
docker run --rm --link rethinkdb:rethinkdb -v $(pwd):/backup petecoop/rethinkdb-driver rethinkdb-dump -c rethinkdb -f /backup/rdb_dump.tar.gz
```

Restore
```
docker run --rm --link rethinkdb:rethinkdb -v $(pwd):/backup petecoop/rethinkdb-driver rethinkdb-restore -c rethinkdb /backup/rdb_dump.tar.gz
```