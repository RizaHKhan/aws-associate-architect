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

A log id called a **ClouldTrail** event_.

Provides 90 days of event history.

To customise the service create 1 or more _Trails_

**Management** Events and **Data** Events.

Logs can be stored in **S3** and are **JSON** formatted.

You can also create **Organization Trail**.

Exam Powerup

- Enabled by default, but 90 days no s3
- Trails are how you configure S3 and CWLogs
- Management events only by default
- IAM, STS, CloudFront => Global Service Events (Trail will need to be enabled to gather that data).
- **NOT REALTIME** - There is a delay


