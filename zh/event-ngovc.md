## Database > RDS for PostgreSQL > Event

## Event

Event refers to RDS for PostgreSQL or a significant event that is caused by a user. Event consists of event category , the date and time of occurrence, the source and the message. Event can be viewed on the console, and the category of events and possible events are as follows.

| Event Code              | Event Category    | Description                                                                   |
|-------------------------|-------------------|-------------------------------------------------------------------------------|
| BACKUP_01_00            | BACKUP            | Backup of DB instance started                                                 |
| BACKUP_01_01            | BACKUP            | Backup of DB instance completed                                               |
| BACKUP_01_04            | BACKUP            | Backup of DB instance failed                                                  |
| BACKUP_02_01            | BACKUP            | Backup deleted                                                                |
| BACKUP_04_00            | BACKUP            | Object storage upload started                                                 |
| BACKUP_04_01            | BACKUP            | Object storage upload completed                                               |
| BACKUP_04_04            | BACKUP            | Object storage upload failed                                                  |
| BACKUP_05_00            | BACKUP            | Backup export started                                                         |
| BACKUP_05_01            | BACKUP            | Backup exported                                                               |
| BACKUP_05_04            | BACKUP            | Backup export failed                                                          |
| BACKUP_06_01            | BACKUP            | Backup of DB instance failed (Known cause)                                    |
| DB_INSTANCE_01_00       | DB_INSTANCE       | Creating DB instance started                                                  |
| DB_INSTANCE_01_01       | DB_INSTANCE       | Creating DB instance completed                                                |
| DB_INSTANCE_01_04       | DB_INSTANCE       | Creating DB instance failed                                                   |
| DB_INSTANCE_02_01       | DB_INSTANCE       | DB instance started                                                           |
| DB_INSTANCE_03_00       | DB_INSTANCE       | DB instance force restart                                                     |
| DB_INSTANCE_04_00       | DB_INSTANCE       | Stopping DB instance started                                                  |
| DB_INSTANCE_04_01       | DB_INSTANCE       | Stopping DB instance completed                                                |
| DB_INSTANCE_04_04       | DB_INSTANCE       | Stopping DB instance failed                                                   |
| DB_INSTANCE_05_01       | DB_INSTANCE       | DB instanced ended                                                            |
| DB_INSTANCE_06_00       | DB_INSTANCE       | Deleting DB instance started                                                  |
| DB_INSTANCE_06_01       | DB_INSTANCE       | Deleting DB instance completed                                                |
| DB_INSTANCE_06_04       | DB_INSTANCE       | Deleting DB instance failed                                                   |
| DB_INSTANCE_07_00       | DB_INSTANCE       | Backup of DB instance started                                                 |
| DB_INSTANCE_07_01       | DB_INSTANCE       | Backup of DB instance completed                                               |
| DB_INSTANCE_07_04       | DB_INSTANCE       | Backup of DB instance failed                                                  |
| DB_INSTANCE_08_00       | DB_INSTANCE       | Restoring DB instance started                                                 |
| DB_INSTANCE_08_01       | DB_INSTANCE       | Restoring DB instance completed                                               |
| DB_INSTANCE_08_04       | DB_INSTANCE       | Restoring DB instance failed                                                  |
| DB_INSTANCE_09_00       | DB_INSTANCE       | Modifying detailed settings started                                           |
| DB_INSTANCE_09_01       | DB_INSTANCE       | Detailed settings modified                                                    |
| DB_INSTANCE_09_04       | DB_INSTANCE       | Detailed settings modification failed                                         |
| DB_INSTANCE_10_01       | DB_INSTANCE       | Automated backup setting enabled                                              |
| DB_INSTANCE_11_01       | DB_INSTANCE       | Automated backup setting disabled                                             |
| DB_INSTANCE_12_00       | DB_INSTANCE       | Changing DB instance type started                                             |
| DB_INSTANCE_12_01       | DB_INSTANCE       | Changing DB instance type completed                                           |
| DB_INSTANCE_12_04       | DB_INSTANCE       | Changing DB instance type failed                                              |
| DB_INSTANCE_13_00       | DB_INSTANCE       | Storage expansion started                                                     |
| DB_INSTANCE_13_01       | DB_INSTANCE       | Storage expanded                                                              |
| DB_INSTANCE_13_04       | DB_INSTANCE       | Storage expansion failed                                                      |
| DB_INSTANCE_14_01       | DB_INSTANCE       | Associate Floating IP                                                         |
| DB_INSTANCE_15_01       | DB_INSTANCE       | Disconnected to floating IP                                                   |
| DB_INSTANCE_16_01       | DB_INSTANCE       | DB instance storage secured                                                   |
| DB_INSTANCE_16_04       | DB_INSTANCE       | Securing DB instance storage failed                                           |
| DB_INSTANCE_17_01       | DB_INSTANCE       | Create a user                                                                 |
| DB_INSTANCE_17_04       | DB_INSTANCE       | Creating user failed                                                          |
| DB_INSTANCE_18_01       | DB_INSTANCE       | Changing user                                                                 |
| DB_INSTANCE_18_04       | DB_INSTANCE       | Changing user failed                                                          |
| DB_INSTANCE_19_01       | DB_INSTANCE       | Deleting a user                                                               |
| DB_INSTANCE_20_01       | DB_INSTANCE       | Create Database                                                               |
| DB_INSTANCE_20_04       | DB_INSTANCE       | Creating database failed                                                      |
| DB_INSTANCE_21_01       | DB_INSTANCE       | Changing database                                                             |
| DB_INSTANCE_21_04       | DB_INSTANCE       | Changing database failed                                                      |
| DB_INSTANCE_22_01       | DB_INSTANCE       | Deleting Database                                                             |
| DB_INSTANCE_23_00       | DB_INSTANCE       | Changing parameter group started                                              |
| DB_INSTANCE_23_01       | DB_INSTANCE       | Changing parameter group completed                                            |
| DB_INSTANCE_23_04       | DB_INSTANCE       | Changing parameter group failed                                               |
| DB_INSTANCE_24_00       | DB_INSTANCE       | Applying parameter group changes started                                      |
| DB_INSTANCE_24_01       | DB_INSTANCE       | Applying parameter group changes completed                                    |
| DB_INSTANCE_24_04       | DB_INSTANCE       | Applying parameter group changes failed                                       |
| DB_INSTANCE_25_00       | DB_INSTANCE       | Changing DB instance security group started                                   |
| DB_INSTANCE_25_01       | DB_INSTANCE       | Changing DB instance security group completed                                 |
| DB_INSTANCE_25_04       | DB_INSTANCE       | Changing DB instance security group failed                                    |
| DB_INSTANCE_26_00       | DB_INSTANCE       | DB instance migration started                                                 |
| DB_INSTANCE_26_01       | DB_INSTANCE       | DB instance migration completed                                               |
| DB_INSTANCE_26_04       | DB_INSTANCE       | DB instance migration failed                                                  |
| DB_INSTANCE_27_00       | DB_INSTANCE       | Changing access control settings started                                      |
| DB_INSTANCE_27_01       | DB_INSTANCE       | Changing access control settings completed                                    |
| DB_INSTANCE_27_04       | DB_INSTANCE       | Changing access control settings failed                                       |
| DB_INSTANCE_28_01       | DB_INSTANCE       | DB instance normalized                                                        |
| DB_INSTANCE_29_01       | DB_INSTANCE       | Not enough DB instance storage                                                |
| DB_INSTANCE_30_01       | DB_INSTANCE       | Connecting DB instance failed                                                 |
| DB_INSTANCE_31_00       | DB_INSTANCE       | Replicating DB instance started                                               |
| DB_INSTANCE_31_01       | DB_INSTANCE       | Replicating DB instance completed                                             |
| DB_INSTANCE_31_04       | DB_INSTANCE       | Replicating DB instance failed                                                |
| DB_INSTANCE_32_00       | DB_INSTANCE       | Promoting DB instance started                                                 |
| DB_INSTANCE_32_01       | DB_INSTANCE       | Promoting DB instance completed                                               |
| DB_INSTANCE_32_04       | DB_INSTANCE       | Promoting DB instance failed                                                  |
| DB_INSTANCE_33_00       | DB_INSTANCE       | Force promoting DB instance started                                           |
| DB_INSTANCE_33_01       | DB_INSTANCE       | DB instance force promotion completed                                         |
| DB_INSTANCE_33_04       | DB_INSTANCE       | DB instance force promotion failed                                            |
| DB_INSTANCE_34_00       | DB_INSTANCE       | DB instance replication rebuilding started                                    |
| DB_INSTANCE_34_01       | DB_INSTANCE       | DB instance replication rebuilding started                                    |
| DB_INSTANCE_34_04       | DB_INSTANCE       | DB instance replication rebuilding started                                    |
| DB_INSTANCE_35_00       | DB_INSTANCE       | DB instance replication latency                                               |
| DB_INSTANCE_35_01       | DB_INSTANCE       | End DB instance replication latency                                           |
| DB_INSTANCE_36_00       | DB_INSTANCE       | Stop DB instance replication                                                  |
| DB_INSTANCE_37_00       | DB_INSTANCE       | Modifying detailed settings started                                           |
| DB_INSTANCE_37_01       | DB_INSTANCE       | Detailed settings modified                                                    |
| DB_INSTANCE_37_04       | DB_INSTANCE       | Detailed settings modification failed                                         |
| DB_INSTANCE_38_01       | DB_INSTANCE       | High Availability DB Instance started                                         |
| DB_INSTANCE_39_01       | DB_INSTANCE       | High Availability DB Instance ended                                           |
| DB_INSTANCE_40_00       | DB_INSTANCE       | Runnig DB instance failover                                                   |
| DB_INSTANCE_40_01       | DB_INSTANCE       | DB instance failover completed                                                |
| DB_INSTANCE_40_04       | DB_INSTANCE       | DB instance failover failed                                                   |
| DB_INSTANCE_41_01       | DB_INSTANCE       | Instance restart using failover                                               |
| DB_INSTANCE_41_04       | DB_INSTANCE       | Instance restart using failover failed                                        |
| DB_INSTANCE_42_00       | DB_INSTANCE       | Waiting for Manual Control of Failover                                        |
| DB_INSTANCE_42_01       | DB_INSTANCE       | Manual Control of Failover Succeeded                                          |
| DB_INSTANCE_42_04       | DB_INSTANCE       | Failover manual control timeout                                               |
| DB_INSTANCE_43_01       | DB_INSTANCE       | High availability suspended                                                   |
| DB_INSTANCE_43_04       | DB_INSTANCE       | High availability suspension failed                                           |
| DB_INSTANCE_44_01       | DB_INSTANCE       | High availability restarted                                                   |
| DB_INSTANCE_44_04       | DB_INSTANCE       | High availability restart failed                                              |
| DB_INSTANCE_45_00       | DB_INSTANCE       | High availability recovery of DB instance with a completed failover started   |
| DB_INSTANCE_45_01       | DB_INSTANCE       | High availability recovery of DB instance with a completed failover completed |
| DB_INSTANCE_45_04       | DB_INSTANCE       | High availability recovery of DB instance with a completed failover failed    |
| DB_INSTANCE_46_00       | DB_INSTANCE       | High availability rebuilding DB instance with a completed failover started    |
| DB_INSTANCE_46_01       | DB_INSTANCE       | High availability rebuilding DB instance with a completed failover completed  |
| DB_INSTANCE_46_04       | DB_INSTANCE       | High availability rebuilding DB instance with a completed failover failed     |
| DB_INSTANCE_47_00       | DB_INSTANCE       | Changing DB instance with a completed failover to normal instance started     |
| DB_INSTANCE_47_01       | DB_INSTANCE       | Changing DB instance with a completed failover to normal instance completed   |
| DB_INSTANCE_47_04       | DB_INSTANCE       | Changing DB instance with a completed failover to normal instance failed      |
| DB_INSTANCE_48_01       | DB_INSTANCE       | High availability normalized                                                  |
| DB_INSTANCE_49_01       | DB_INSTANCE       | High availability stopped                                                     |
| DB_INSTANCE_50_00       | DB_INSTANCE       | Candidate master rebuilding started                                           |
| DB_INSTANCE_50_01       | DB_INSTANCE       | Candidate master rebuilding completed                                         |
| DB_INSTANCE_50_04       | DB_INSTANCE       | Candidate master rebuilding failed                                            |
| DB_INSTANCE_51_01       | DB_INSTANCE       | Backup of DB instance failed (Known cause)                                    |
| DB_INSTANCE_52_00       | DB_INSTANCE       | Exporting backup file after backing up DB instance started                    |
| DB_INSTANCE_52_01       | DB_INSTANCE       | Exporting backup file after backing up DB instance completed                  |
| DB_INSTANCE_52_04       | DB_INSTANCE       | Exporting backup file after backing up DB instance failed                     |
| DB_INSTANCE_53_01       | DB_INSTANCE       | Exporting backup file after backing up DB instance failed (known cause)       |
| DB_INSTANCE_54_00       | DB_INSTANCE       | Exporting DB instance backup started                                          |
| DB_INSTANCE_54_01       | DB_INSTANCE       | Exporting DB instance backup completed                                        |
| DB_INSTANCE_54_04       | DB_INSTANCE       | Exporting DB instance backup failed                                           |
| DB_INSTANCE_55_00       | DB_INSTANCE       | DB instance restoration using backup from the object storage started          |
| DB_INSTANCE_55_01       | DB_INSTANCE       | DB instance using backup from the object storage restored                     |
| DB_INSTANCE_55_04       | DB_INSTANCE       | DB instance restoration using backup from the object storage failed           |
| DB_INSTANCE_56_00       | DB_INSTANCE       | DB instance version upgrade started                                           |
| DB_INSTANCE_56_01       | DB_INSTANCE       | DB instance version upgrade completed                                         |
| DB_INSTANCE_56_04       | DB_INSTANCE       | DB instance version upgrade failed                                            |
| DB_INSTANCE_57_00       | DB_INSTANCE       | Applying extension changes started                                            |
| DB_INSTANCE_57_01       | DB_INSTANCE       | Applying extension changes completed                                          |
| DB_INSTANCE_57_04       | DB_INSTANCE       | Applying extension changes failed                                             |
| DB_SECURITY_GROUP_01_01 | DB_SECURITY_GROUP | DB security group created                                                     |
| DB_SECURITY_GROUP_02_00 | DB_SECURITY_GROUP | Changing DB security group started                                            |
| DB_SECURITY_GROUP_02_01 | DB_SECURITY_GROUP | Changing DB security group completed                                          |
| DB_SECURITY_GROUP_02_04 | DB_SECURITY_GROUP | Changing DB security group failed                                             |
| DB_SECURITY_GROUP_03_01 | DB_SECURITY_GROUP | DB security group deleted                                                     |
| TENANT_01_04            | TENANT            | CPU cores limit                                                               |
| TENANT_02_04            | TENANT            | RAM capacity limit	                                                           |
| TENANT_03_04            | TENANT            | Individual volume limit                                                       |
| TENANT_04_04            | TENANT            | Total project volume limit                                                    |
| TENANT_05_04            | TENANT            | Limit read replica creation                                                   |
| JOB_01_04               | JOB               | Job execution failed                                                          |

### Subscribe to Events

If subscribed to an event, a notification will be received via email and SMS when the event occurs. Notifications are sent to users of the user group subscribed to the event. Subscription can be subdivided by event type, event code, and event source. In order to temporarily stop the notifications, modify the enabled event subscription. If disabled, notifications are not sent.

![event-subscription](https://static.toastoven.net/prod_rds_postgres/20240813/event-subscription-en.png)

* ❶ Click **Register Event Subscription**and a pop-up window will appear where you can sign up for an event subscription.
* ❷ Select the type of event you want to subscribe to. The event type changes the event codes you can select.
* ❸ Select the event code to subscribe.
* ❹ Select the event source to subscribe.
* ❺ Select a user group to receive event notifications.
* ❻ Select whether to enable or disable. If you select **No**, you will not send notifications when an event occurs.
