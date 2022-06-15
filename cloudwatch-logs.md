# CloudWatch Logs

- Public Service - usable from AWS or on-premises
- Store, Monitor and access logging data
- AWS Integrations - EC2, VPC Flow Logs, Lambda, CloudTrail, R53 and more...
- Can generate metrics based on logs - metric filter

Regional service (ie, `us-east-1`).

Logging Sources(ie, AWS, EC2, API etc) inject data into CloudWatch called `log events` which are stored inside `log-streams`.

Collected metrics can be used to trigger alarms.

## CloudTrail

Logs API actions that affect AWS account. Almost any action is logged by CloudTrail.

A log id called a _ClouldTrail event_.

Provides 90 days of event history.

To customise the service create 1 or more _Trails_

_Management_ Events and _Data_ Events.


