# Import and export workflows in usegalaxy.no

Galaxy offers a simple way to download a workflow as a single file which can be imported into another Galaxy instance and run there. 

!!! note

     Different Galaxy instances may have different versions of the same tool installed. This may cause the Galaxy instance you import the workflow into to throw a warning. In order for the imported and exported workflows to give identical results, the tool versions must be identical 

	There might be individual tool parameter settings that are pre-set in the exported workflow that for some reason are not carried over properly during the import. In order for the imported and exported workflows to give identical results, the individual tool parameter settings must be identical 

	A tool may not be installed in the Galaxy instance you are importing the workflow. In order for the workflow to run, the tool must be installed 

	A tool may be dependent on a pre-indexed reference. In order for the workflow to run, the reference must be available 

## Exporting a workflow:
Select the **"Workflow"** menu [1]

A list of the workflows you have created or imported into your user in usegalaxy.no will be displayed

From the menu that appear by clicking on the name of the workflow you want to export [2], select **"Download"** [3] and save the workflow (single .ga file) to your local machine

![](images/usegalaxy_export_workflow.png)

## Importing a workflow
Select the **"Workflow"** menu [1]

A list of workflows that you have created or imported (if you have any) will be displayed

Pressing **"Import"** [2] and a pop-up window with import options will appear. If you have the workflow stored locally, press **"Browse"** [3] and select the .ga file and press **"Import workflow"** [4]

!!! note

     Is is possible to import publicly available workflows directly via the URL

The imported workflow will appear in the list of workflows

![](images/usegalaxy_import_workflow1.png)

Different tool versions on exporting and importing Galaxy servers may cause the workflow to throw a warning. Click on the name of the workflow and select the **"Edit"** [1] to view potential issues, then press **"Continue"** [2]

You should now be able to run the workflow

![](images/usegalaxy_import_workflow2.png)

