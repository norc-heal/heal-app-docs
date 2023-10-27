---
hide:
  - toc
full-width: true
---

# Editing an Experiment

If you want to edit an experiment annotation after you have created it, you can do so in the tool using the "Edit an existing experiment" feature. 

!!! Info
    We encourage you to use the form to edit your experiments rather than entering/editing information manually into the Experiment Tracker CSV, as the tool will automatically put your information into the correct formatting and structure. Manual edits will not necessarily be in the correct format.


1. Select "Edit an existing experiment" in the "Add Experiment" tab.

    <figure markdown>
        ![](../app-screenshots/edit-exp-select.PNG)
        <figcaption></figcaption>
    </figure>

2. Navigate to your dsc-pkg folder and select the annotated experiment .txt file that you want to edit.

    *For example:*

    <figure markdown>
        ![](../app-screenshots/exp-track-output.PNG)
        <figcaption></figcaption>
    </figure>

3. The information on your annotated experiment will populate in the "Annotate Experiment" window.

    <figure markdown>
        ![](../app-screenshots/edit-exp-pop.PNG)
        <figcaption></figcaption>
    </figure>

    1. When you edit your first experiment, the tool will create an "archive" folder and will archive the original version of your result annotation (.txt) file there, so there are no issues with duplicate file naming. The User Status Message Box will also display a message providing information on the location of the original annotation file.

        <figure markdown>
            ![](../app-screenshots/edit-result-archive.PNG)
            <figcaption></figcaption>
        </figure>
    
        !!! Note
    
            Currently, you can only edit an experiment once within the tool, due to an issue of duplicate files in the archive folder. This will be addressed in later releases of the tool. 
            
            For a temporary fix, if you need to make second or third edits to the same experiment file, you should go into the archive folder and change the name of the experiment txt file saved there (for example, you can change the name from "exp-trk-exp-1" to "exp-trk-exp-1-1"). This will allow the tool to archive your current experiment annotation without returning an error.
        

4. Make any necessary edits to your experiment file, and then select "Save experiment."