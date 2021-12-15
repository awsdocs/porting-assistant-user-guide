# Port solution using Porting Assistant for \.NET Visual Studio IDE extension<a name="porting-assistant-vs-ide-port-solution"></a>

The following functionality is available when you port your solution using the IDE extension\.

**Guided assistance**  
You can fix all of the code recommendations at one time by porting the project, or you can go through each issue within the source code by viewing the code next to each light bulb\. When you select to port a project or solution, Porting Assistant for \.NET opens a dialog box that prompts you to choose whether to apply recommended source code changes\. If you do not select this option, you can go through each issue within the source code\. When you make a code change, you must save your updates to view the updated recommendations for your changes\.

When you port your solution to \.NET Core, the Porting Assistant for \.NET Visual Studio IDE extension provides guided assistance in the source editor throughout the process\. You can choose to **Port Solution to \.NET Core** \(all projects\) or **Port Project to \.NET Core** \(single project\) from either the **Project** tab, the **Extensions** tab, or the **Solution Explorer** pane to the right of the source file\. When the source file is open with a source editor, porting options are provided to assist you, and to automate the porting of each source file\. Automated porting involves running the source code through code translation assistant rules for porting\. This can be performed at the solution level when you select **Port to \.NET Core ** and choose to apply recommended source code changes\.

**View incompatibilities**  
You can view the list of incompatibilities, suggestions, and more from the **Error list** pane at the bottom of the page\. Select an error in the list to go to the section in the source editor where the error is located\. The source file will be annotated with the error message, details about the compatibility issue in the annotated line of code, and a recommended solution\. These details are included in the code comments\. If you have already completed automated porting, an annotation at each \(denoted by a light bulb\) line is modified to describe the change\. The source file also highlights each line of source code with compatibility issues\. This helps you to visualize the magnitude of the issues in the file and to begin to address them\. The highlighting is removed when the compatibility issues are addressed\. 

**Suggestions**  
The source editor provides a replacement suggestion for each incompatibility in the source file\. If a direct replacement exists, you are given a choice to select and replace it\. If there is no direct replacement, references or contextual help on how to proceed are provided\.

**Run code**  
When all of the source files are updated, you can compile, test, and run your code\. If you have the AWS Toolkit for Visual Studio plug\-in installed on your IDE, you can deploy your application on Amazon Web Services\. To install, see [AWS Toolkit for Visual Studio Code](http://aws.amazon.com/visualstudiocode)\.