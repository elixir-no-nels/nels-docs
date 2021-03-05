# User Documentation

## Accessing NeLS

## Upload/Download data to/from NeLS

### Upload/Download data using the Webinterface

### Upload/Download using ssh

## Exchange data with usegalaxy.no

## Midterm data storage in NeLS/SBI

## Where to deposit data long term

## Import and export Galaxy histories to and from NeLS

[usegalaxy.no](https://usegalaxy.no/) is directly connected to your data storage in [NeLS](https://nels.bioinfo.no/). This exclude the need for local copy of your data. You can simply transfer data directly between [usegalaxy.no](https://usegalaxy.no/) and [NeLS](https://nels.bioinfo.no/).

We have made a function in the [usegalaxy.no](https://usegalaxy.no/) that can export a whole history including the data sets in that history as a single compressed file to [NeLS](https://nels.bioinfo.no/). 

This file can be imported into another Galaxy instance and the analysis work can continue there. The advantage of this export is that all provenance data will be kept, meaning all commands, tool versions, database versions, etc that were used prior to the export.

!!! note

     Since usegalaxy.no is not meant for storage we encourage you to move your data when your analysis is done.

#### Before getting started

* Login to [https://usegalaxy.no/](https://usegalaxy.no/) - See how to login to usegalaxy.no [make a separate tutorial and link here]
* You need at least one history in usegalaxy.no to export

#### Exporting a history from usegalaxy.no to NeLS
Dataset and histories can also be exported from usegalaxy.no to your local system. 

!!! note

     💡If you have several histories, you would need to repeat the steps below for each history you would like to export.

* Make sure that the history you want to export is your current (active) history 
* Press the "**History options**" [1] and select "**Export History**" under the "**NeLS storage**" section [2]
* You will be redirected to the NeLS portal where you need to choose the destination folder [3] (shown here a random subfolder in the Personal folder)
* Browse to the folder you want to export the history to and press "**Use current folder**" [4].
* You should be redirected back to usegalaxy.no where you can view the transfer progress (you might need to scroll down a bit in the usegalaxy.no main window). When the transfer is complete, the progression bar will turn green [5]

![](images/usegalaxy_export1.png)

#### Importing a history from NeLS to usegalaxy.no
Both single datasets and complete histories can be imported from your NeLS storage

!!! note

    💡When importing data from NeLS, you cannot define the datatype (format). You can change datatype once the datasets are imported into usegalaxy.no

* Press the "**History options**" and select "**Import History**" under the "**NeLS storage**" section [1]
* You will be redirected to the NeLS storage. browse to the folder containing the data (example here is a random subfolder in the Project folder), select the history (or file) [2] and press "**Send to Galaxy**" [3]
*You will be redirected back to usegalaxy.no and you can monitor the progress of the import [4]. The progress bar will turn green when the import is complete [5]
* The name of the imported history will be "**imported from archive: ....**"" The history can be accessed by selecting "**Histories**" [6] under the **User**" menu. You can rename the history if you like.

![](images/usegalaxy_import_NeLS_History.png)

## Delete and permanent delete data in usegalaxy.no

Galaxy offer multiple ways to delete datasets and histories. The are two major types of deletion:

1. Delete datasets or histories - This option temporary delete data (basically just hide the data)
2. Permanently delete datasets or histories - This option permanently delete data from the disk

!!! note

     We strongly encourage that you copy your histories to NeLS and permanently delete data from usegalaxy.no when you are done with your data analysis. This will free up your personal disk space in usegalaxy.no. To backup data to NeLS see [this documentation](usegalaxy_ImportExport.md)

### Delete datasets

Select the dataset(s) you want to delete (temporary) by pressing "**X**" next to the dataset in your "**History**" panel [1]. The dataset should disappear from you history, but you still access it [2]

You have only temporary deleted the data (equal to moving it to the trash bin on you computer), and it can be undeleted (moved back from trash bin), or permanently deleted by pressing "**Permanently remove it from disk**" [3]
Press "**OK**" to confirm the permanent deletion [4]

You can still see traces of the dataset in your history [5], but the data in the file is deleted from the disk and you have freed up disk space

![](images/usegalaxy_delete_data.png)

### Delete complete histories
Similarly, you can temporary and permanently delete histories. Access the overview of your histories either by selecting "**Histories**" [1] under the **User**" menu or by pressing "**View all histories**" [2] in the "**History**" panel

From the drop-down menu of the history you want to delete (exemplified by the history named "**imported from archive: ....**""), press "**Delete Permanently**" [3] for permanent deletion. 

If you chose the other history view, from the drop-down menu of the history you want to delete press "**Purge**" [4]. Both options will ask you to confirm the deletion, and both options will erase the data from disk.

![](images/usegalaxy_delete_histories.png)


## Import and export workflows in usegalaxy.no

Galaxy offers a simple way to download a workflow as a single file which can be imported into another Galaxy instance and run there. 

!!! note

     Different Galaxy instances may have different versions of the same tool installed. This may cause the Galaxy instance you import the workflow into to throw a warning. In order for the imported and exported workflows to give identical results, the tool versions must be identical 

	There might be individual tool parameter settings that are pre-set in the exported workflow that for some reason are not carried over properly during the import. In order for the imported and exported workflows to give identical results, the individual tool parameter settings must be identical 

	A tool may not be installed in the Galaxy instance you are importing the workflow. In order for the workflow to run, the tool must be installed 

	A tool may be dependent on a pre-indexed reference. In order for the workflow to run, the reference must be available 

### Exporting a workflow:
Select the **"Workflow"** menu [1]

A list of the workflows you have created or imported into your user in usegalaxy.no will be displayed

From the menu that appear by clicking on the name of the workflow you want to export [2], select **"Download"** [3] and save the workflow (single .ga file) to your local machine

![](images/usegalaxy_export_workflow.png)

### Importing a workflow
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

## ENN DETTE?