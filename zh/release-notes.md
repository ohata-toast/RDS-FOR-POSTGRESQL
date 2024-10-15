## Database > RDS for PostgreSQL > Release Notes

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
