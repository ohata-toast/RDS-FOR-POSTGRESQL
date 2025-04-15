## Database > RDS for PostgreSQL > Release Notes

### 2025. 4. 15.

#### 기능 추가

- DB 엔진 신규 버전 추가
    - PostgreSQL 14.17, 17.4 버전을 추가했습니다.
- 확장 관리 기능 추가
    - 콘솔에서 SUPERUSER 권한이 필요한 확장을 설치하거나 삭제하는 기능을 추가했습니다.
    - 데이터베이스 & 사용자 목록과 동일하게 확장 목록을 동기화할 수 있습니다.
- 유지보수 설정에 로그 보관 기간 추가
    - 자동 스토리지 정리 기능 사용 시 보관 기간이 지난 PostgreSQL 로그를 삭제하는 기능을 추가했습니다.

#### 기능 변경

- DB 엔진 신규 생성 제한
    - PostgreSQL 14.15, 17.2 버전에서 보안 취약점이 발견돼 최신 버전으로의 업그레이드가 [권고](https://www.postgresql.org/support/security/CVE-2025-1094/)됩니다.
    - 기존 DB 인스턴스를 고가용성으로 변경하거나 백업으로 복원하는 경우에만 제한적으로 허용합니다.

### Feb 11, 2025

#### Added Features

- Added a new DB engine version
    - Added PostgreSQL versions 14.15, 17.2.
- Added a feature to upgrade DB engine version
    - You can upgrade the DB Engine version from an existing version to the recently added version.

#### Features Updates

- Added DB engine creation limit
    - A security vulnerability has been discovered in PostgreSQL version 14.6 and an upgrade to a newer version is [recommended](https://www.postgresql.org/about/news/postgresql-171-165-159-1414-1317-and-1221-released-2955/).
    - DB engine creation is allowed for changing an existing DB instance to high availability or restoring with a backup.

### December 10, 2024

#### Added Features

- Added High Availability
    - Added the feature to create and modify high-availability DB instances.
- Added Database & User Synchronization
    - Added the feature to view databases and user lists in sync with information within the DB engine.
- Added Maintenance Settings
    - Provides the feature to periodically clean up storage to help stabilize DB instances.
- Added Backup Export
    - Added the feature to select an existing backup or start a new backup and export it to user object storage.
- Added the feature to restore to a backup in object storage
    - Added the feature to restore from a backup exported to object storage.
- Added API Feature
    - Added the feature to control RDS for PostgreSQL features via APIs.

#### Feature Updates

- Changed the DB Instance > **Backup** tab name
    - Renamed the **Backup** tab to **Backup and Maintenance** among the detail tabs of the DB instance.
    - You can additionally check the maintenance settings within your DB instance.
- Changed User Permissions in Databases
    - Expanded DDL user permissions from the `CREATE` schema permission to the `CREATE` database permission.
    - As part of the expanded permissions, changed to allow schema creation with DDL user IDs.
- Improved Database List View Feature
    - Improved the feature to view a list of schemas added as DDL users in the database list.
- Improved Backup Settings
    - Removed the backup retry expiration time entry and improved to retry backups within the backup window time range.
- Changed Feature to Free up Capacity
    - Improved the selection of WAL log files from directly selecting them to a backup time base that allows point-in-time restores.
- Changed the `shared_buffers` parameter
    - Limit the parameter to a maximum of 50% of the DB instance RAM size, as using an excessively large value can cause problems running the DB engine.

### October 15, 2024

#### Added Features

- Added auto backup settings
    - Added the feature to set whether to allow auto backups.
    - You can disallow auto backups under any circumstances.
        - If you don't have the backups required for replication, you are limited to creating read replicas.
- Added the feature to wait for replication delay on force promotion
    - Added the feature to wait for replication delays to resolve when force promoting.
- Added the feature to end replication delay queuing
    - Added the feature to end the wait for replication delays when promoting/forcing a promotion.
- Added DB extensions
    - Added pgrouting, bool, hstore, intarray, isn, lo, ltree, and more to be able to install.

#### Feature Updates

- Improved event subscription search
    - Improved so that you can search by event source name.
- Improved the feature to enter the shared_preload_libraries parameter
    - Improved the way shared_preload_libraries values are entered to a multi-select drop-down list format.

#### Bug fixes

- Fix default notification creation errors
    - Fixed default notification creation to ignore the existence of a notification group with the same name.
- Fixed an error with the log_timezone parameter
    - Fixed an issue where replication fails when the log_timezone value is applied to something other than Asia/Seoul.
- Fixed an error with the max_connections parameter
    - Fixed an issue with the order of application when changing the max_connections value with read replicas added.
    - Changed the parameter to be inapplicable if the value on the master is set to be greater than the read replica.
    - Changed the parameter to be inapplicable if the value of the read replica is set to less than the master.

### August 13, 2024

#### Added Features

- Added DB instance deletion protection feature
- Added connected notification groups, operating system information to DB instance detail view screen
- Added the feature to create read replicas
    - Added replication latency to monitoring charts and monitoring settings.
- Added the Subscribe to Events feature
    - Notifications sent when certain events occur.

#### Feature Updates

- Improved the access control feature
    - Added the option to add default access control rules when adding users.
    - Improved usability to allow drag-and-drop rule ordering.
- Improved to see which parameter items actually change when applying parameter group changes
- Improved the service activation screen
    - Modified to auto-refresh on service activation.
- Improved the parameter group detail Screen
    - Added the TIMEZONE type and improved the dropdown to search for and enter it.
    - Improved the feature to select units with a dropdown when editing parameters with units.

### June 11, 2024

#### Release of a New Service

- Relational Database Service (RDS) is a service that provides relational databases in cloud environments.
- You can use relational databases without difficult settings.
- PostgreSQL 14.6 version is provided.
