# Identity and Access Management for Porting Assistant for \.NET<a name="security-iam"></a>

AWS Identity and Access Management \(IAM\) is an AWS service that helps an administrator securely control access to AWS resources\. Porting Assistant for \.NET is a standalone application that does not require IAM access control to use resources\. 

To use Porting Assistant for \.NET, you must attach the following IAM policy as an inline policy to your IAM user\. Then, configure a profile on your server with the IAM credentials of this user\. For steps on how to attach this policy, see [AWS Identity and Access Management \(IAM\)](porting-assistant-prerequisites.md#porting-assistant-iam)\.

```
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "EnCorePermission",
            "Effect": "Allow",
            "Action": [
                "execute-api:invoke",
                "s3:GetObject",
                "s3:ListBucket"
            ],
            "Resource": [
                "arn:aws:execute-api:us-east-1:492443789615:3dmmp07yx6/*",
                "arn:aws:execute-api:us-east-1:547614552430:8q2itpfg51/*",
                "arn:aws:s3:::aws.portingassistant.dotnet.datastore",
                "arn:aws:s3:::aws.portingassistant.dotnet.datastore/*"
            ]
        }
    ]
}
```