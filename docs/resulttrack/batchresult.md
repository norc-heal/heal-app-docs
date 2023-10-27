# Advanced
## Batch Add Result(s) to Tracker

If you try to save a result while you have the corresponding Results Tracker open, you will receive an error. The annotated result file will save as a .txt file within the dsc-pkg folder, but it will not be added to the Results Tracker. You will need to do this manually using the "Batch add existing result(s) to tracker" option.

1. Ensure that none of your Results Trackers are open before attempting to batch add results.
1. Navigate to the "Add Result" tab and select "Batch add existing result(s) to tracker" under "Advanced."

    <figure markdown>
        ![](../app-screenshots/batch-add-result-1.PNG)
        <figcaption></figcaption>
    </figure>

3. Select the results that you want to add.
    1. It may be easiest to select all existing annotated result files when using this feature. The tool will scan the result files you select and only add those that are not already included in within the Results Tracker, so selecting a file that has already been included in the Results Tracker will not produce an error here.
    2. Note: These files follow the naming convention "result-trk-result-"

    <figure markdown>
        ![](../app-screenshots/select-results-batch.PNG)
        <figcaption></figcaption>
    </figure>

4. If your files are successfully added to the appropriate Results Trackers, the User Status Message Box will provide a confirmation message:

    <figure markdown>
        ![](../app-screenshots/usmb-batch-add.PNG)
        <figcaption></figcaption>
    </figure>