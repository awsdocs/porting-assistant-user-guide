# How Porting Assistant for \.NET Visual Studio IDE extension works<a name="porting-assistant-vs-ide-how-it-works"></a>

You can download the Porting Assistant for \.NET Visual Studio IDE extension from the [Visual Studio Extensions Marketplace](https://marketplace.visualstudio.com/)\. When you use the extensions from within a supported Visual Studio version, you can initiate one or more \.NET application assessments and port your solutions to \.NET Core for Linux\. Additional work may be required to address issues for which Porting Assistant for \.NET can't find resolution\. You can browse the source code repository to find and specify a solution file for your \.NET application, and then initiate an assessment task for the application\. From within Visual Studio, you can view and analyze the generated report\. When an assessment is complete, Porting Assistant for \.NET jump\-starts the process by converting \.csproj files from the Visual Studio 2015 to the Visual Studio 2019 format\. It converts the project file structure to match the structure expected by \.NET Core\.

You can use the updated project files to start making changes in the source code and to receive contextual help and authoritative guidance from within the editor\. The Porting Assistant for \.NET Visual Studio IDE extension supports code diagnostics\. When an application is ported, you can utilized the AWS toolkit for Visual Studio to deploy it to your choice of AWS \.NET Core\-supported execution environment\. 

You can continue to use the standalone Porting Assistant for \.NET tool to perform portfolio assessments\. You can also begin your assessment with the standalone tool and transition to the IDE environment to port your application\.

The following table compares features of the standalone tool and the IDE extension\.


| Features | Porting Assistant for \.NET standalone tool | Porting Assistant for \.NET Visual Studio IDE extension | 
| --- | --- | --- | 
|  Run assessment on all applications in a portfolio  |  Run assessments on multiple applications concurrently  | Run assessments only on currently opened applications | 
|  View list of assessed applications and compare assessments for all applications  |  Yes  | No | 
|  Load single solution to tool for assessment  |  Yes  | Yes | 
|  View list of incompatibilities for a solution  |  Yes  | Yes | 
|  View package dependency tree for a solution  |  Yes  | No | 
|  View recommendations  |  Yes  | Yes | 
|  Run automated porting  |  Yes  | Yes | 
|  Open source file for direct editing  |  No  | Yes | 
|  Contextual help with recommendations  |  No  | Yes | 
| Provide details about compatibility and steps to rectify incompatibilities |  No  | Yes | 
|  Continuous reassessment as code is modified  |  No  | Yes | 
|  Test, debug, and run code  |  No  | Yes | 
|  Deploy the application in AS runtimes, using AWS toolkit downloaded separately  |  No  | Yes | 