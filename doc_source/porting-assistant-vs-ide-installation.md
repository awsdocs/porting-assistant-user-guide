# Install Porting Assistant for \.NET Visual Studio IDE extension<a name="porting-assistant-vs-ide-installation"></a>

Perform the following steps to install the Porting Assistant for \.NET Visual Studio IDE extension\.

1. Go to the [Visual Studio Extensions Marketplace](https://marketplace.visualstudio.com/)\. Search for "Porting Assistant for \.NET"\. Choose **Install** and run the installer to complete the installation\. 

1. When the installation is complete, **Close** the installer and relaunch Visual Studio\. When you relaunch Visual Studio, open the solution you want to assess, then open one of its \.cs files\. Select the **Analyze** tab to view Porting Assistant for \.NET options\. To run an assessment, select **Analyze**>**Run Full Assessment**\. The first time you run an assessment, you will see the **Getting started with Porting Assistant for \.NET for Visual Studio** screen\. Enter your AWS named profile details and consent to share telemetry to continue\. You must have a valid AWS CLI profile in order for Porting Assistant for \.NET to collect compatibility information on the public NuGet packages and the APIs within the packages that are in use by your application\. To view the type of application data collected by Porting Assistant for \.NET , see [Data collected by Porting Assistant for \.NETData collected](data-protection.md#porting-assistant-data-collected)\. Information about public NuGet packages is collected to help AWS prioritize work to address \.NET Core incompatibilities on the NuGet packages, if any\. For instructions on how to configure an AWS CLI profile, see [Configuring the AWS CLI ](https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-configure.html)\. 

1. From the **Getting Started** screen, you can choose the **Target Framework** version to which you want to port your application\.

1. **Save and close** the **Getting Started** screen\. 

   You can change the settings you entered into the **Getting Started** screen by selecting the **Tools** tab, and choosing **Options** from the dropdown menu\. Under **PortingAssistant Extension**, select **Data usage sharing** to select a different **AWS Named Profile**, **Add a named profile**, or to change your usage data selection\. Choose **General** under **PortingAssistant Extension** to update the **Target Framework**\.
