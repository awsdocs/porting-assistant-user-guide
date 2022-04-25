# Porting Assistant for \.NET Visual Studio IDE extension<a name="porting-assistant-vs-ide"></a>

The Porting Assistant for \.NET Visual Studio IDE extension makes it possible to use Porting Assistant for \.NET functionality seamlessly from within Visual Studio\. Once installed, the Porting Assistant for \.NET extension provides prescriptive guidance to assist you with assessing and porting your Windows \.NET Framework applications to \.NET Core on Linux\. This extension facilitates collaboration with other developers who are analyzing, debugging, testing, and refactoring the same application code\. 

You can access the Porting Assistant for \.NET Visual Studio IDE extension from the [Visual Studio Extensions Marketplace](https://marketplace.visualstudio.com/)\. Search for "Porting Assistant for \.NET"\. After you download and install the extension, you can assess any solution in your portfolio\. 

**Topics**
+ [Supported versions](#porting-assistant-vs-ide-versions)
+ [Prerequisites for using the Porting Assistant for \.NET Visual Studio IDE extension](#porting-assistant-vs-ide-prerequisites)
+ [Memory requirements](#porting-assistant-vs-ide-memory)
+ [Pricing for the Porting Assistant for \.NET Visual Studio IDE extension](#porting-assistant-vs-ide-pricing)
+ [How Porting Assistant for \.NET Visual Studio IDE extension works](porting-assistant-vs-ide-how-it-works.md)
+ [Install Porting Assistant for \.NET Visual Studio IDE extension](porting-assistant-vs-ide-installation.md)
+ [Assess and analyze solution using Porting Assistant for \.NET Visual Studio IDE extension](porting-assistant-vs-ide-solution-assessment.md)
+ [Port solution using Porting Assistant for \.NET Visual Studio IDE extension](porting-assistant-vs-ide-port-solution.md)
+ [Transition from standalone tool to Porting Assistant for \.NET Visual Studio IDE extension](porting-assistant-vs-ide-transition.md)
+ [Troubleshoot the Porting Assistant for \.NET Visual Studio IDE extension](porting-assistant-vs-ide-troubleshooting.md)
+ [Porting Assistant for \.NET Visual Studio IDE extension version history](porting-assistant-vs-ide-versions.md)

## Supported versions<a name="porting-assistant-vs-ide-versions"></a>

The Porting Assistant for \.NET Visual Studio IDE extension supports the following \.NET versions:
+ Source versions: \.NET Framework 3\.5 and later
+ Target versions: \.NET Core 3\.1 and 5 

For assessments and porting, both Windows services and ASP\.NET applications are supported\.

The Porting Assistant for \.NET Visual Studio IDE extension supports the following versions of Visual Studio and Visual Studio Code:
+ Visual Studio 2019 and later
**Note**  
If you have Visual Studio IntelliCode installed, you must change the C\# suggestions to **Disabled**\. Select **Tools** > **Options** > **IntelliCode** > **Suggestions** > **C\#**, then select **Disabled** from the dropdown\.

## Prerequisites for using the Porting Assistant for \.NET Visual Studio IDE extension<a name="porting-assistant-vs-ide-prerequisites"></a>

To use the Porting Assistant for \.NET IDE extension, ensure the following prerequisites:
+ Installation of \.NET Core 3\.1 or 5\. [Download \.NET Core](https://dotnet.microsoft.com/download/dotnet-core)\.
+ **AWS CLI**: You must have a valid AWS CLI profile in order for Porting Assistant for \.NET to collect compatibility information on the public NuGet packages and the APIs within the packages that are in use by your application\. To view the type of application data collected by Porting Assistant for \.NET , see [Data collected by Porting Assistant for \.NETData collected](data-protection.md#porting-assistant-data-collected)\. Information about public NuGet packages is collected to help AWS prioritize work to address \.NET Core incompatibilities on the NuGet packages, if any\. For instructions on how to configure an AWS CLI profile, see [Configuring the AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-configure.html)\. 
+ Visual Studio 2019 version 16\.9 and later\.
+ Installation of any \.NET Framework versions currently in use by your application\.

## Memory requirements<a name="porting-assistant-vs-ide-memory"></a>

The following memory requirements must be met to use the Porting Assistant for \.NET Visual Studio for \.NET IDE Extension\.


| Solution size | Minimum memory requirements | 
| --- | --- | 
|  Small solutions \(1,000 to 50,000 lines of code\)  |  4 GB  | 
|  Medium solutions \(50,000 to 400,000 lines of code\)  |  8 GB  | 
| Large solutions \(400,000 or more lines of code\) | 16 GB or more, depending on size of source code | 

**Note**  
These requirements are provided as estimates\. Individual solutions can vary for memory usage\.

## Pricing for the Porting Assistant for \.NET Visual Studio IDE extension<a name="porting-assistant-vs-ide-pricing"></a>

The Porting Assistant for \.NET Visual Studio IDE extension is available for use at no cost\.

**Topics**