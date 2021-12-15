# Port a solution<a name="porting-assistant-port"></a>

You can port a project using the assessment tool or the CLI console application\. 

## Port a solution using the assessment tool<a name="porting-assistant-port-tool"></a>

To port a solution using the assessment tool, perform the following steps:

1. From the main page of Porting Assistant for \.NET, choose **Get started**\. 

1. On the **Edit settings** page, choose the target \.NET framework and AWS named profile to allow Porting Assistant to assess your solution\. You can also add the AWS named profile using the [ AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-files.html)\.

1. From the main page of the assessment tool, select **Assessed solutions** from the left navigation pane\. 

1. On the **Assessed Solutions** page, select a solutions file\. You will be directed to the**Assessment overview** page\.

1. Under the **Projects** tab, select the project you want to port\. Choose **Port project**\. The Porting Assistant will ask how you want to save your ported project\. Select whether you want to copy the ported project to a new location or modify the project in place\. 
**Note**  
The project is ported to the version used in the assessment\. If you want to port to a different version, you must reassess the project after changing the version in your settings\.

   After you select the destination folder and choose **Save**, or select to modify the project file in place, you will be directed to the **Port projects** page\.

1. Porting Assistant begins to port the new solution, and you are directed to the **Assessment overview** page\. The status of the port appears at the top of the page\. You can view the port status of a package by selecting it on the **Assessment overview** page and looking at the **Port status** in the overview section\.

**Important**  
When you port a solution, your project files and code are modified\. Your project file is modified to include compatible packages you selected and other packages detected by the assessment\. In addition, Porting Assistant adds or backs up code files based on the type of projects detected\. Some code files are changed to make them more compatible with \.NET Core\. The result is not a completely ported project\. The project may not build, and additional source code changes may be required\. Any added or modified code must be verified and tested before it can be considered production ready\. 

## Port a solution using the Porting Assistant CLI console application<a name="porting-assistant-port-cli"></a>

The following steps guide you through the process of porting a solution using the Porting Assistant CLI console application\. The CLI is packaged with the Porting Assistant for \.NET tool\. After you install the Porting Assistant for \.NET tool, the CLI can be found in the following location: `C:\Users\<user_name>\AppData\Local\Programs\Porting Assistant for .NET\resources\netcore_build\PortingAssistant.Client.CLI.exe`\.

To port a solution using the Porting Assistant CLI console application, run the following commands\.

1. `--solution-path (-s)`

   **Definition**: The path to your solution file

   **Required**: Yes

1. `--output-path (-o)`

   **Definition**: The path where the assessment JSON file is stored\.

   **Required**: Yes

1. `--target-version (-t)` 

   **Definition**: The \.NET version to use for the assessment\.

   **Required**: No

   **Options**: 
   + `netcore3.1`
   + `net5.0`
   + `net6.0` \(default\)

1. `--ignore-projects (-i)`

   **Definition**: Projects that are not assessed\.

   **Required**: No

   **Value**: 

   Comma separated project names\. For example `project1, project2`\.

1. `--porting-projects (-p)`

   **Definition**: Projects to port\.

   **Required**: No

   **Value**: 

   Comma separated project names\. For example `project1, project2`\.

**Example**

You have a solution with five projects, named `project1`, `project2`, `project3`, `project4`, and `project5`, and you want to port `project1` and `project2`\.

```
& 'C:\Users\<username>\AppData\Local\Programs\Porting Assistant for .NET\resources\netcore_build\PortingAssistant.Client.CLI.exe' assess --solution-path "<path_to_solution/example_solution.sln>" --output-path "<path_to_output_dir>” --target “net5.0” --porting-projects “project1,project2”
```