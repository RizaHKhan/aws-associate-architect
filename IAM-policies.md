# IAM Policies

An identity needs to prove to AWS who it is via authentication.

Multiple statements can be in a policy.

```json
{
  "version": "foo",
  "statements": [{}, {}]
}
```

Parts of a statement:

1. `Sid`: What the statement does. Arbitrary name
2. `Effect`: Allow/Deny. Deny takes precedence over any other effect.
3. `Action`: One or more action and can be specific such as adding an image to an S3 bucket.
4. `Resource`: Can be lists of AWS Resources

Explicit Deny -> Explicit Allow -> Default Deny (implicit)

Two types of policies:  Inline Policies
Creating a policy and applying it to specific account(s). Unique to each identity, therefore not scalable.

Managed Policy
Create a policy (JSON like the others) and identifies are added to it.

They are reusable and low management overhead.

## IAM Users

Are an identity used for anything requiring long-term AWS access e.g Humans, Applications or service accounts

#### Authentication

Principal proves to AWS it is indeed that principal. Access/keys or username/password are methods to authenticate.

If authenticated -> _Authenticated Identity_ and can start interacting with AWS.

## Amazon Resource Name (ARN)

Uniquely identify resources within any AWS accounts

Structure:

```
arn:partition:service:region:account-id:resouce-id
arn:partition:service:region:account-id:resouce-type/resource-id
```

Example:

```
arn:aws:s3:::catgifs
arn:aws:s3:::catgifs/*
```

- Bucket and objects inside that bucket are not the same thing.

### Exam Powerup

- 5,000 IAM Users per account
- IAM User can be a member of 10 groups
- This has systems design impacts...
- Internet-scale applications
- Large orgs & org merges
- IAM Roles & Identity Federation fix this (more later)

