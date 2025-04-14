## Database > RDS for PostgreSQL > DB拡張機能

## DB拡張機能
あらかじめビルドされた拡張機能をPostgreSQLにインストールして機能を拡張することができます。NHN CloudのRDS for PostgreSQLでサポートする拡張機能は次のとおりです。

### PostgreSQL基本提供機能

`auto_explain`モジュールはパラメータグループの`shared_preload_libraries`パラメータに追加して全体セッションに適用したり、`LOAD`構文でセッションごとに個別に適用できます。残りの拡張機能は[CREATE EXTENSION](https://www.postgresql.org/docs/14/sql-createextension.html)構文で必要な拡張機能をインストールできます。

| 拡張機能名         | バージョン | SUPERUSER権限 | 備考                          | Webサイト                                                   |
|--------------------|-----|--------------|-------------------------------|----------------------------------------------------------|
| auto_explain       | -   | O            | `LOAD`構文実行時にSUPERUSER権限必要 | https://www.postgresql.org/docs/14/auto-explain.html     |
| citext             | 1.6 |              |                               | https://www.postgresql.org/docs/14/citext.html           |
| cube               | 1.5 |              |                               | https://www.postgresql.org/docs/14/cube.html             |
| dblink             | 1.2 | O            |                               | https://www.postgresql.org/docs/14/dblink.html           |
| earthdistance      | 1.1 | O            | cubeインストール必要                  | https://www.postgresql.org/docs/14/earthdistance.html    |
| fuzzystrmatch      | 1.1 |              |                               | https://www.postgresql.org/docs/14/fuzzystrmatch.html    |
| hstore             | 1.8 |              |                               | https://www.postgresql.org/docs/14/hstore.html           |
| intarray           | 1.5 |              |                               | https://www.postgresql.org/docs/14/intarray.html         |
| isn                | 1.2 |              |                               | https://www.postgresql.org/docs/14/isn.html              |
| lo                 | 1.1 |              |                               | https://www.postgresql.org/docs/14/lo.html               |
| ltree              | 1.2 |              |                               | https://www.postgresql.org/docs/14/ltree.html            |
| pg_stat_statements | 1.9 | O            |                               | https://www.postgresql.org/docs/14/pgstatstatements.html |
| pg_visibility      | 1.2 | O            |                               | https://www.postgresql.org/docs/14/pgvisibility.html     |
| pgcrypto           | 1.3 |              |                               | https://www.postgresql.org/docs/14/pgcrypto.html         |
| pgrowlocks         | 1.2 | O            |                               | https://www.postgresql.org/docs/14/pgrowlocks.html       |
| postgres_fdw       | 1.1 | O            |                               | https://www.postgresql.org/docs/14/postgres-fdw.html     |
| tablefunc          | 1.0 |              |                               | https://www.postgresql.org/docs/14/tablefunc.html        |

### RDS追加提供機能

追加提供される拡張機能をインストールするには、必要に応じてパラメータグループの`shared_preload_libraries`パラメータに設定を追加した後、DBエンジン再起動が必要です。再起動が完了したら[CREATE EXTENSION](https://www.postgresql.org/docs/14/sql-createextension.html)構文で必要な拡張機能をインストールできます。

| 拡張機能名                   | バージョン  | SUPERUSER権限 | パラメータ設定 | 備考                         | Webサイト                             |
|------------------------------|-------|--------------|---------|------------------------------|------------------------------------|
| pgAudit                      | 1.6.2 | O            | 追加必要 |                              | https://www.pgaudit.org/           |
| pgrouting                    | 3.6.2 | O            |         | postgisインストール必要              | https://pgrouting.org/             |
| postgis                      | 3.4.1 | O            | 追加必要 |                              | https://postgis.net/               |
| postgis_raster               | 3.4.1 | O            |         | postgisインストール必要              |                                    |
| postgis_sfcgal               | 3.4.1 | O            |         | postgisインストール必要              |                                    |
| postgis_tiger_geocoder       | 3.4.1 | O            |         | fuzzystrmatch, postgisインストール必要 |                                    |
| postgis_topology             | 3.4.1 | O            |         | postgisインストール必要              |                                    |
| address_standardizer         | 3.4.1 | O            |         | postgisインストール必要              |                                    |
| address_standardizer_data_us | 3.4.1 | O            |         | postgisインストール必要              |                                    |
