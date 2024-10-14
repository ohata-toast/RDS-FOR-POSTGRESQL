## Database > RDS for PostgreSQL > DB Extensions

## DB Extensions
You can extend functionality by installing pre-built extensions into PostgreSQL. The following extensions are supported by RDS for PostgreSQL on NHN Cloud.

### PostgreSQL Built-in Features

The auto_explain module can be applied to the entire session by adding it to the shared_preload_libraries parameter in the parameter group, or separately for each session with the LOAD syntax. For the remaining extensions, you can install the required extensions with the CREATE EXTENSION syntax.

| Extension name           | Version  | Remarks         | Homepage                                                     |
|--------------------|-----|------------|----------------------------------------------------------|
| auto_explain       | -   |            | https://www.postgresql.org/docs/14/auto-explain.html     |
| citext             | 1.6 |            | https://www.postgresql.org/docs/14/citext.html           |
| cube               | 1.5 |            | https://www.postgresql.org/docs/14/cube.html             |
| dblink             | 1.2 |            | https://www.postgresql.org/docs/14/dblink.html           |
| earthdistance      | 1.1 | Requires cube installation | https://www.postgresql.org/docs/14/earthdistance.html    |
| fuzzystrmatch      | 1.1 |            | https://www.postgresql.org/docs/14/fuzzystrmatch.html    |
| hstore             | 1.8 |            | https://www.postgresql.org/docs/14/hstore.html           |
| intarray           | 1.5 |            | https://www.postgresql.org/docs/14/intarray.html         |
| isn                | 1.2 |            | https://www.postgresql.org/docs/14/isn.html              |
| lo                 | 1.1 |            | https://www.postgresql.org/docs/14/lo.html               |
| ltree              | 1.2 |            | https://www.postgresql.org/docs/14/ltree.html            |
| pg_stat_statements | 1.9 |            | https://www.postgresql.org/docs/14/pgstatstatements.html |
| pg_visibility      | 1.2 |            | https://www.postgresql.org/docs/14/pgvisibility.html     |
| pgcrypto           | 1.3 |            | https://www.postgresql.org/docs/14/pgcrypto.html         |
| pgrowlocks         | 1.2 |            | https://www.postgresql.org/docs/14/pgrowlocks.html       |
| postgres_fdw       | 1.1 |            | https://www.postgresql.org/docs/14/postgres-fdw.html     |
| tablefunc          | 1.0 |            | https://www.postgresql.org/docs/14/tablefunc.html        |

### RDS Additional Features

Installing the additional offered extensions requires a DB engine restart, if necessary, after adding the setting to the shared_preload_libraries parameter in the parameter group. Once the restart is complete, you can install the required extensions with the CREATE EXTENSION syntax.

| Extension name                     | Version    | Setting parameters | Remarks                           | Homepage                               |
|------------------------------|-------|---------|------------------------------|------------------------------------|
| pg_repack                    | 1.4.8 |         |                              | https://reorg.github.io/pg_repack/ |
| pgAudit                      | 1.6.2 | Additional required   |                              | https://www.pgaudit.org/           |
| pgrouting                    | 3.6.2 |         | Requires postgis installation                | https://pgrouting.org/             |
| postgis                      | 3.4.1 | Additional required   |                              | https://postgis.net/               |
| postgis_raster               | 3.4.1 |         | Requires postgis installation                |                                    |
| postgis_sfcgal               | 3.4.1 |         | Requires postgis installation                |                                    |
| postgis_tiger_geocoder       | 3.4.1 |         | fuzzystrmatch, requires postgis installation |                                    |
| postgis_topology             | 3.4.1 |         | Requires postgis installation                |                                    |
| address_standardizer         | 3.4.1 |         | Requires postgis installation                |                                    |
| address_standardizer_data_us | 3.4.1 |         | Requires postgis installation                |                                    |
