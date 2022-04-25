# Data protection in Porting Assistant for \.NET<a name="data-protection"></a>

The AWS [shared responsibility model](http://aws.amazon.com/compliance/shared-responsibility-model/) applies to data protection in Porting Assistant for \.NET\. As described in this model, AWS is responsible for protecting the global infrastructure that runs all of the AWS Cloud\. You are responsible for maintaining control over your content that is hosted on this infrastructure\. This content includes the security configuration and management tasks for the AWS services that you use\. For more information about data privacy, see the [Data Privacy FAQ](http://aws.amazon.com/compliance/data-privacy-faq)\. For information about data protection in Europe, see the [AWS Shared Responsibility Model and GDPR](http://aws.amazon.com\blogs/security/the-aws-shared-responsibility-model-and-gdpr/) blog post on the *AWS Security Blog*\.

For data protection purposes, we recommend that you protect AWS account credentials and set up individual user accounts with AWS Identity and Access Management \(IAM\)\. That way each user is given only the permissions necessary to fulfill their job duties\. We also recommend that you secure your data in the following ways:
+ Use multi\-factor authentication \(MFA\) with each account\.
+ Use SSL/TLS to communicate with AWS resources\. We recommend TLS 1\.2 or later\.
+ Set up API and user activity logging with AWS CloudTrail\.
+ Use AWS encryption solutions, along with all default security controls within AWS services\.
+ Use advanced managed security services such as Amazon Macie, which assists in discovering and securing personal data that is stored in Amazon S3\.
+ If you require FIPS 140\-2 validated cryptographic modules when accessing AWS through a command line interface or an API, use a FIPS endpoint\. For more information about the available FIPS endpoints, see [Federal Information Processing Standard \(FIPS\) 140\-2](http://aws.amazon.com/compliance/fips/)\.

We strongly recommend that you never put confidential or sensitive information, such as your customers' email addresses, into tags or free\-form fields such as a **Name** field\. This includes when you work with Porting Assistant or other AWS services using the console, API, AWS CLI, or AWS SDKs\. Any data that you enter into tags or free\-form fields used for names may be used for billing or diagnostic logs\. If you provide a URL to an external server, we strongly recommend that you do not include credentials information in the URL to validate your request to that server\.

**Topics**
+ [Data collected by Porting Assistant for \.NET](#porting-assistant-data-collected)

## Data collected by Porting Assistant for \.NET<a name="porting-assistant-data-collected"></a>

If you accept the data collection option in the **Settings** menu of the Porting Assistant for \.NET tool, the following application data is collected:

1. Application errors generated when running assessments, porting, or when performing other functions provided by the Porting Assistant for \.NET tool\.

1. Names and versions of public NuGet packages assessed by the Porting Assistant for \.NET tool\.

1. Metrics for assessments run by the Porting Assistant for \.NET tool on public NuGet packages, such as the number of packages and solutions, and the amount of time taken to create a solution\.

You can change your data collection settings at any time in the **Settings** menu of the Porting Assistant for \.NET tool\. 

**Encryption at rest**  
All data within Porting Assistant for \.NET is encrypted at rest in accordance with industry standards\.

**Encryption in transit**  
All requests to Porting Assistant for \.NET must be made over the Transport Layer Security protocol \(TLS\)\. We recommend TLS 1\.2 or later\.