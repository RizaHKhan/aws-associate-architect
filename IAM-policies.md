# IAM Policies

An identity needs to prove to AWS who it is via authentication.

Multiple statements can be in a policy.

``` json
{
 "version": 'Foo',

}

```
Parts of a statement: 
1. Sid: What the statement does. Arbitrary name
2. Effect: Allow/Deny. Deny takes precedence over any other effect.
3. Action: One or more action and can be specific such as adding an image to an S3 bucket.
4. Resource: Can be lists of AWS Resources

Explicit Deny -> Explicit Allow -> Default Deny (implicit)

Two types of policies:  Inline Policies
Creating a policy and applying it to specific account(s). Unique to each identity, therefore not scalable.

Managed Policy
Create a policy (JSON like the others) and identifies are added to it. 

They are reusable and low management overhead.

