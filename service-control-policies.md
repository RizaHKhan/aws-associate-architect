# Service Control Policies

Are account permissions boundaries.
\*They limit what the account (including root user) can do.

JSON document can be attached to the organization as a whole or can be attached to one or more units. They can also be attached to multiple accounts.

If attached to root org (they impact all child orgs).

```json
{
  "Version": "####",
  "Statement": [
    {
      "Effect": "Allow",
      "Action": "*",
      "Resource": "*"
    },
    {
      "Effect": "Allow",
      "Action": "*",
      "Resource": "*"
    }
  ]
}
```
