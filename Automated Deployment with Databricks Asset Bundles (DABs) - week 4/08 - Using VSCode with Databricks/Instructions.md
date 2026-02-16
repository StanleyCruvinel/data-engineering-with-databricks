Visual Studio Code (VSCode) and Databricks Introduction
Databricks CLI in VSCode
Select the menu icon (three lines in the navigation bar).

Select Terminal, then New Terminal.

In the terminal, type cd work to navigate to the work folder, where you have write access in this lab.

Type the command databricks -v to view the version of the Databricks CLI. You should see that Databricks CLI version V0.258.0 has already been installed.

NOTE: View the Install or update the Databricks CLI for more information.

Next, confirm the clipboard is enabled on the website. In the Chrome browser to the left of the URL select View site information icon. Make sure the clipboard is enabled.

Clipboard Settings Image
Complete the following steps to authenticate to your lab Databricks Workspace. We will create a Databricks configuration profile with the name DEFAULT.

a. Use the Databricks CLI to run the following command: databricks configure.

b. For the "Databricks Host" prompt, paste your Databricks workspace instance URL from your text editor.

NOTE: To paste on a mac use COMMAND + SHIFT + V. If you use COMMAND + V a pasting error will occur.
NOTE: To paste on a windows try SHIFT + INSERT. If you use COMMAND + V a pasting error will occur.
NOTE: If pasting does not work for you, just press enter.
c. For the "Personal Access Token" prompt, paste the Databricks personal access token for your workspace.

NOTE: To paste on a mac use COMMAND + SHIFT + V. If you use COMMAND + V a pasting error will occur.
NOTE: To paste on a windows try SHIFT + INSERT. If you use COMMAND + V a pasting error will occur.
NOTE: If pasting does not work for you, just press enter. Then go to the work folder and find the .cfg text file and paste your values in there.
d. After you enter your Databricks personal access token, a corresponding configuration profile will be added to your databricks.cfg file.

NOTE: View the Authentication for the Databricks CLI documentation for more information on authentication methods.

Run the CLI command databricks catalogs list to view the catalogs in your Databricks Workspace.

Run the command databricks bundle init to use the default DAB template.

a. Select default-python.

b. Press Enter to use the default project name my_project.

c. Select "Yes" for the remaining prompts to use the default project.

d. Expand the work folder in the left navigation and notice that all the required files were added to your local environment.

NOTE: In a terminal, the templates provide a series of prompts that can be used to customize the DAB template. The course uses shell commands in notebook cells for the Databricks CLI, and this method does display the prompts.

Run the command cd my_project to navigate within your project directory.

Run the command ls to confirm you see your DAB project and the databricks.yml file.

Validate the default DAB project using databricks bundle validate.

Deploy the default DAB project using databricks bundle deploy.

Navigate back to your Databricks Lab Workspace. Go to Workflows and notice that you deployed the DAB using your local VSCode IDE.

Databricks VSCode Extension (Quick High-Level Introduction)
After your DAB project has been created, let's quickly explore how you can use DABs with the Databricks VSCode extension. This will be a quick introduction.

For a deeper dive into the Databricks VSCode extension, refer to the What is the Databricks extension for Visual Studio Code? documentation.

Select the Databricks Icon from the left navigation pane.

Click on Choose a project / Select a Project. This will use the default authentication we set with the Databricks CLI.

In the dropdown, choose the project you created with the Databricks CLI, named my_project.

The Databricks extension will display your project, with additional features on the left.

Clipboard Settings Image
Under CONFIGURATION, you will see various details to assist with your CI/CD process.

Under CONFIGURATION, select Cluster. A pop-up at the top of the screen will appear, allowing you to select a Compute cluster from your Workspace.

Under BUNDLE RESOURCE EXPLORER, you can see information about your DAB.

Under BUNDLE VARIABLES, you will be able to view the bundle variables you created.

That’s a quick introduction to the Databricks VSCode Extension for DABs. The extension provides additional features locally when working with DABs.

Note: Databricks Connect has not been set up for this demo environment. This is outside the scope of this course.
