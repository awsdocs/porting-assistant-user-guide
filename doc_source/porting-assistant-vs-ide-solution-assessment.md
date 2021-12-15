# Assess and analyze solution using Porting Assistant for \.NET Visual Studio IDE extension<a name="porting-assistant-vs-ide-solution-assessment"></a>

To assess your solution and analyze the results from the Porting Assistant for \.NET Visual Studio IDE extension, perform the following steps:

1. Open a solution file, then open a \.cs file within the solution\.

1. From the Porting Assistant for \.NET Visual Studio IDE Extension, select the **Analyze** tab\. In the drop\-down menu, you can choose to **Enable Incremental Assessments** or **Run Full Assessment**\.

   1. **Enable Incremental Assessments**\. When you select this option, Porting Assistant for \.NET automatically runs a continuous assessment as you make changes to the source code\. Compatibility errors are displayed when encountered\. 

   1. **Run Full Assessment**\. When you select this option, Porting Assistant for \.NET runs a one\-time, full assessment for the compatibility solution loaded in the IDE\.

1. The **Error List** pane at the bottom of the screen displays all of the incompatibilities discovered in the source files associated with the solution\. You can select each entry in the list of incompatibilities to view the incompatibility in the source code, which is highlighted\.