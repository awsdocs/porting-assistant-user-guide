# Prerequisites<a name="porting-assistant-prerequisites"></a>

The following prerequisites must be verified in order to successfully port your existing \.NET applications to \.NET Core using the Porting Assistant for \.NET tool\.

**Topics**
+ [Prerequisites](#porting-assistant-prereq-versions-dependencies)
+ [Memory requirements for the Porting Assistant for \.NET Visual Studio for \.NET IDE extension\.](#porting-assistant-vs-ide-memory-requirements)
+ [AWS Identity and Access Management \(IAM\)](#porting-assistant-iam)

## Prerequisites<a name="porting-assistant-prereq-versions-dependencies"></a>

The Porting Assistant for \.NET tool requires the following prerequisites for installation and usage\.
+ **\.NET Core SDK 3\.1**: [Download \.NET Core](https://dotnet.microsoft.com/download/dotnet-core)\.
+ **AWS CLI**: You must have a valid AWS CLI profile in order for Porting Assistant for \.NET to collect compatibility information on the public NuGet packages and the APIs within the packages that are in use by your application\. To view the type of application data collected by Porting Assistant for \.NET , see [Data collected by Porting Assistant for \.NETData collected](data-protection.md#porting-assistant-data-collected)\. Information about public NuGet packages is collected to help AWS prioritize work to address \.NET Core incompatibilities on the NuGet packages, if any\. For instructions on how to configure an AWS CLI profile, see [AWS Identity and Access Management \(IAM\)](#porting-assistant-iam) \. 
+ Windows 7 or later
+ Internet connectivity on the machine running the assessment
+ If your machine is behind a proxy with restricted internet access, you must permit access to the following: 
  + **Amazon S3 Datastore** — `https://s3.us-west-2.amazonaws.com/aws.portingassistant.dotnet.datastore/`
  + **Amazon S3 Datastore authenticaiton endpoint** — `https://encore-telemetry.us-east-1.amazonaws.com/`
  + **GitHub datastore** — `hhttps://github.com/aws/porting-assistant-dotnet-datastore/tree/master/data`
  + **GitHub user content** — `http://raw.githubusercontent.com/` 
  + **NuGet or additional package addresses** — any addresses required to restore your project packages \(the most common one being `api.nuget.com`\)
+ Administrator access
+ Processor with 1\.8 GHz or above processing speed
+ 4 GB minimum of available memory
+ 5 GB minimum of free disk space

## Memory requirements for the Porting Assistant for \.NET Visual Studio for \.NET IDE extension\.<a name="porting-assistant-vs-ide-memory-requirements"></a>

The following memory requirements must be met to use the Porting Assistant for \.NET Visual Studio for \.NET IDE extension\.


| Solution size | Minimum memory requirements | 
| --- | --- | 
|  Small solutions \(1,000 to 50,000 lines of code\)  |  4 GB  | 
|  Medium solutions \(50,000 to 400,000 lines of code\)  |  8 GB  | 
| Large solutions \(400,000 or more lines of code\) | 16 GB or more, depending on size of source code | 

**Note**  
These requirements are provided as estimates\. Individual solutions can vary for memory usage\.

## AWS Identity and Access Management \(IAM\)<a name="porting-assistant-iam"></a>

You must create an IAM user and attach a policy to your IAM user in order to grant permissions to the Porting Assistant for \.NET service\. Follow the steps in this section to create the user and attach the policy\.

**Topics**
+ [Create the IAM user](#porting-assistant-iam-create-user)
+ [Attach required policy to the IAM user](#porting-assistant-iam-attach-policy)
+ [Create access keys for your IAM user](#porting-assistant-iam-access-key)
+ [Configure your AWS profile](#porting-assistant-iam-profile)

### Create the IAM user<a name="porting-assistant-iam-create-user"></a>

1. Sign in to the [AWS Management Console](https://console.aws.amazon.com/console) and navigate to the [IAM console](https://console.aws.amazon.com/iam)\.

1. Choose **Users** from the left navigation pane\.

1. Choose **Add user**\.

1. Enter the user name for the new user\. This is the sign\-in name for AWS\.

1. Under **Select AWS access type**, select **Programmatic access**\.

1. Choose **Next: Permissions**\.

1. Choose **Next: Tags**\.

1. Choose **Next: Review** to view your configuration\. After you have verified your selections, choose **Create user**\.

1. Save the user access key IDs and secret access keys\. You will use these to create AWS profiles\. To view the user access keys \(access key and secret access keys\), choose **Show** next to each password and access key that you want to see\. To save the access keys, choose **Download\.csv** and save the file to a secure location\.
**Important**  
You will not have access to the secret keys again after this step\.

For more information about creating IAM users, see [Creating an IAM user in your AWS account](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_users_create.html)\.

### Attach required policy to the IAM user<a name="porting-assistant-iam-attach-policy"></a>

To grant the required permissions to use Porting Assistant for \.NET, you must attach the following IAM policy to your IAM user\.

1. Sign in to the [AWS Management Console](https://console.aws.amazon.com/console) and navigate to the [IAM console](https://console.aws.amazon.com/iam)\.

1. Choose **Policies** from the left navigation pane\.

1. Choose **Create policy**\.

1. Choose the **JSON** tab and copy and paste the following policy into the text field\.

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

1. Choose **Next: Tags**\.

1. Choose **Review Policy** and enter a **Name** and **Description** for the policy\.

1. Choose **Create Policy**\.

1. Filter the list of policies with the name of the policy you just created\.

1. Select the bullet next to your new policy, and from the **Policy actions** dropdown, select **Attach**\.

1. Select the **User name** of the IAM user created in [Create the IAM user](#porting-assistant-iam-create-user)\.

1. Choose **Attach policy**\.

### Create access keys for your IAM user<a name="porting-assistant-iam-access-key"></a>

If you are unable to locate the access keys for the IAM user to which the required policy is attached, perform the following steps\.

1. Sign in to the [AWS Management Console](https://console.aws.amazon.com/console) and navigate to the [IAM console](https://console.aws.amazon.com/iam)\.

1. Choose **Users** from the left navigation pane\.

1. Choose the name of the user to which the policy is attached, and then choose the **Security credentials** tab\.

1. In the **Access keys** section, chose **Create access key**\.
**Note**  
If you already have an access key but cannot access your secret access key, make the old key inactive and create a new one\. 

1. To view the new access key, choose **Show**\. You will not have access to the secret access key again after this dialogue box is closed\. Your credentials will look something like the following example ID and access key:

   `Access key ID: AKIAIOSFODNN7EXAMPLE`

   `Secret access key: wJalrXUtnFEMI/K7MDENG/bPxRfiCYEXAMPLEKEY`

1. To download the key pair, choose **Download \.csv file**\. Store the keys in a secure location\. You will not have access to the secret access key again after this dialogue box is closed\.

   Keep the keys confidential to protect your AWS account and never email them\. Do not share them outside of your organizaiton, even if an inquiry appars to come from AWS or www\.amazon\.com\. No one who legitimatley represents Amazon will ever ask you for your secret key\.

For more information about creating an access key ID and secret access key, see [Access key ID and secret access key](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-quickstart.html#cli-configure-quickstart-creds)\.

### Configure your AWS profile<a name="porting-assistant-iam-profile"></a>

After you have created an IAM user, you can configure your AWS named profile to apply settings and credentials to be applied when you run commands\.

**Configure AWS profile in the assessment tool**

1. In the Porting Assistant for \.NET assessment tool, navigate to **Set up Porting Assistant for \.NET**\.

1. Choose **Add a profile** under **AWS named profile**\.

1. Enter your new **Profile name**, **AWS access key ID**, and **AWS secret access key**\. 

1. Choose **Add**\.

**Configure AWS profile using the AWS CLI**

1. Run the following AWS CLI command to create a profile for Porting Assistant for \.NET\. The profile is named `default` in the credentials file\.

   ```
   aws configure
   ```

1. For each prompt, enter the corresponding information\.
   + `AWS Access Key ID`
   + `AWS Secret Access Key`
   + `Default region name` \(For example, `us-west-2`\)
   + `Default output format`

1. After you configure the profile using the AWS CLI, Porting Assistant for \.NET will display the `default` profile under **AWS named profile** on the **Set up Porting Assistant for \.NET** page of the assesment tool\.

For more information about configuring the AWS CLI, see [Configuring the AWS CLI ](https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-configure.html)\.