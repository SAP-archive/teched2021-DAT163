# Objective

As a Business Analyst or Data Steward, you need to understand and gain insight into your data. After accessing various data, profiling them and reviewing the profiling results you will be able to add a glossary term to a column in your dataset as well as provide a rating and comment on the dataset.

In this exercise, you will discover and interact with various connected systems, upload a dataset, profile the data, rate dataset, create a relationship with data and a glossary term

## Log Into SAP Data Intelligence

After completing these steps, you will have logged into SAP Data Intelligence.

1. Open Chrome and go to the SAP Data Intelligence url you were provided
<br>![](/exercises/ex1/images/Ex01_Part01_01.png)

2. Enter 'Default' for Tenant Name and click 'Proceed'
<br>![](/exercises/ex1/images/Ex01_Part01_02.png)

3. Enter the Username that was assigned to you (e.g. 'TA#'), for Tenant Name
Note: where # is the number assigned to you
Enter the Password that was assigned to you, for your Password
Click 'Sign In'
<br>![](/exercises/ex1/images/Ex01_Part01_03.png)

4. You are now signed in the application.
<br>![](/exercises/ex1/images/Ex01_Part01_04.png)

You have now logged into SAP Data Intelligence.

## Browse data in a Connected System (Database)

After completing these steps you will have discovered dataset stored in a database.

1. Click on 'Metadata Explorer'
<br>![](/exercises/ex1/images/Ex01_Part03_01.png)

2. Click on 'Browse Connections'
<br>![](/exercises/ex1/images/Ex01_Part03_02.png)

3. Click 'List View'
<br>![](/exercises/ex1/images/Ex01_Part03_03.png)

4. This allows to show the list of connections as a list.
<br>![](/exercises/ex1/images/Ex01_Part03_04.png)

5. Select 'View Capabilities'
<br>![](/exercises/ex1/images/Ex01_Part03_05.png)

6. This lists all the features supported for a given connected system.
<br>![](/exercises/ex1/images/Ex01_Part03_06.png)

7. Click 'Grid View' to come back to tiles.
<br>![](/exercises/ex1/images/Ex01_Part03_07.png)

8. Click on the 'HANA_DEMO' tile
<br>![](/exercises/ex1/images/Ex01_Part03_08.png)

9. Select 'DEMO'
<br>![](/exercises/ex1/images/Ex01_Part03_09.png)

10. Click 'View FactSheet' on the 'PHARMA_CLAIM' database table tile
<br>![](/exercises/ex1/images/Ex01_Part03_10.png)

11. This shows the factsheet (DETAILS)
<br>![](/exercises/ex1/images/Ex01_Part03_11.png)

12. Click 'Start Profiling'
<br>![](/exercises/ex1/images/Ex01_Part03_12.png)

13. Click 'Notification'
<br>![](/exercises/ex1/images/Ex01_Part03_13.png)

14. This shows the details of the notifications. Click anywhere outside the notification window to continue interacting with the application
<br>![](/exercises/ex1/images/Ex01_Part03_14.png)

15. Wait for the profiling task to finish, and Click 'Refresh'
<br>![](/exercises/ex1/images/Ex01_Part03_15.png)

16. The factsheet was updated with the profiling information once the task is done.
<br>![](/exercises/ex1/images/Ex01_Part03_16.png)

17. Click 'Columns'
<br>![](/exercises/ex1/images/Ex01_Part03_17.png)

18. Select the Line for 'DRUG_NAME'
<br>![](/exercises/ex1/images/Ex01_Part03_18.png)

19. Observe Data Preview and the 'Top 10 Distinct Values'
<br>![](/exercises/ex1/images/Ex01_Part03_19.png)

20. We can see there are data quality issues such as spelling mistakes on the drug names
<br>![](/exercises/ex1/images/Ex01_Part03_20.png)

21. We can also see there is an important number of null values
<br>![](/exercises/ex1/images/Ex01_Part03_21.png)

22. Click 'Data Intelligence Metadata Explorer'
<br>![](/exercises/ex1/images/Ex01_Part03_22.png)

23. Click 'Home'
<br>![](/exercises/ex1/images/Ex01_Part03_23.png)

You have now discovered a table in a database, profiled the data and found some data quality issues.

## Upload your Dataset

After completing these steps you will have uploaded and published datasets in SAP Data Intellegence.

1. Click on 'Metadata Explorer'
<br>![](/exercises/ex1/images/Ex01_Part02_01.png)

2. Click on 'Browse Connections'
<br>![](/exercises/ex1/images/Ex01_Part02_02.png)

3. Click on the 'DI_DATA_LAKE' tile
<br>![](/exercises/ex1/images/Ex01_Part02_03.png)

4. Click on the 'shared' tile
<br>![](/exercises/ex1/images/Ex01_Part02_04.png)

5. Click on the New Folder icon (folder with a +)
<br>![](/exercises/ex1/images/Ex01_Part02_05.png)

6. Enter 'TechEd_DAT163_#' for folder name (where # is the number assigned to you)
<br>![](/exercises/ex1/images/Ex01_Part02_06.png)

7. Click 'OK'
<br>![](/exercises/ex1/images/Ex01_Part02_07.png)

8. Search for 'TechEd_DAT163_#' to isolate your newly created folder, then click on your newly added 'TechEd_DAT163_#' folder (where # is the number assigned to you)
<br>![](/exercises/ex1/images/Ex01_Part02_08.png)

9. Upload a file, click on the 'Upload Files' icon on the toolbar
<br>![](/exercises/ex1/images/Ex01_Part02_09.png)

10. Click on 'Upload' in the upper right hand corner of the Upload Files pop-up window
<br>![](/exercises/ex1/images/Ex01_Part02_10.png)

11. Browse to Sample Data folder where you downloaded and extracted 'DRUG_#.csv' (where # is the number assigned to you) and select it
<br>![](/exercises/ex1/images/Ex01_Part02_11.png)

12. Click 'Open'
<br>![](/exercises/ex1/images/Ex01_Part02_12.png)

13. Click 'Upload'
<br>![](/exercises/ex1/images/Ex01_Part02_13.png)

The file will upload on the data lake.
<br>![](/exercises/ex1/images/Ex01_Part02_13_bis.png)

14. After Upload is Complete, click 'Close'
<br>![](/exercises/ex1/images/Ex01_Part02_14.png)

15. The file is now uploaded and available in the data lake.
<br>![](/exercises/ex1/images/Ex01_Part02_15.png)

## Enrich Dataset and Isolate Data Quality Issues

After completing these steps you will have created a new dataset using self-service data preparation.
This new dataset will help to easily isolate invalid claims.

1. Click 'More Actions'
<br>![](/exercises/ex1/images/Ex01_Part04_01.png)

2. Select 'Prepare Data'
<br>![](/exercises/ex1/images/Ex01_Part04_02.png)

3. The self-service data preparation room shows up
<br>![](/exercises/ex1/images/Ex01_Part04_03.png)

4. The first record of the data is actually the column header
<br>![](/exercises/ex1/images/Ex01_Part04_04.png)

5. Check 'Use first row as header'
<br>![](/exercises/ex1/images/Ex01_Part04_05.png)

6. Click 'Continue'
<br>![](/exercises/ex1/images/Ex01_Part04_06.png)

7. The application will automatically recreate a new sample with the updated metadata structure
<br>![](/exercises/ex1/images/Ex01_Part04_07.png)

8. The dataset now has the proper header
<br>![](/exercises/ex1/images/Ex01_Part04_08.png)

9. Click 'Actions'
<br>![](/exercises/ex1/images/Ex01_Part04_09.png)

10. Click 'Enrich Preparation'
<br>![](/exercises/ex1/images/Ex01_Part04_10.png)

11. the enrich preparation main user interface shows up
<br>![](/exercises/ex1/images/Ex01_Part04_11.png)

12. Click '+' to add a new source of data to merge with
<br>![](/exercises/ex1/images/Ex01_Part04_12.png)

13. Click 'Browse'
<br>![](/exercises/ex1/images/Ex01_Part04_13.png)

14. Select 'HANA_DEMO as a 'Connection'
<br>![](/exercises/ex1/images/Ex01_Part04_14.png)

15. Click 'DEMO'
<br>![](/exercises/ex1/images/Ex01_Part04_15.png)

16. Select 'PHARMA_CLAIMS'
<br>![](/exercises/ex1/images/Ex01_Part04_16.png)

17. Click 'OK'
<br>![](/exercises/ex1/images/Ex01_Part04_17.png)

18. The application is acquiring a sample of the new selected dataset
<br>![](/exercises/ex1/images/Ex01_Part04_18.png)

19. The new selected dataset can now be used to merge data
<br>![](/exercises/ex1/images/Ex01_Part04_19.png)

20. Drag and drop 'PHARMA_CLAIMS' on the cell on the left hand-side of the main dataset
<br>![](/exercises/ex1/images/Ex01_Part04_20.png)

21. Select 'Left Join'
<br>![](/exercises/ex1/images/Ex01_Part04_21.png)

22. Scroll down the list of output columns and uncheck 'ORIG_PRODUCT', 'POTENCY', 'DOSAGE', 'ROUTE_ADMINISTERED', NOTES
<br>![](/exercises/ex1/images/Ex01_Part04_22.png)

23. Click Apply
<br>![](/exercises/ex1/images/Ex01_Part04_23.png)

24. The application displays a preview of the merge data
<br>![](/exercises/ex1/images/Ex01_Part04_24.png)






## Exercise 1.1 Sub Exercise 1 Description

After completing these steps you will have created...

1. Click here.
<br>![](/exercises/ex1/images/01_01_0010.png)

2.	Insert this line of code.
```abap
response->set_text( |Hello World! | ). 
```



## Exercise 1.2 Sub Exercise 2 Description

After completing these steps you will have...

1.	Enter this code.
```abap
DATA(lt_params) = request->get_form_fields(  ).
READ TABLE lt_params REFERENCE INTO DATA(lr_params) WITH KEY name = 'cmd'.
  IF sy-subrc <> 0.
    response->set_status( i_code = 400
                     i_reason = 'Bad request').
    RETURN.
  ENDIF.

```

2.	Click here.
<br>![](/exercises/ex1/images/01_02_0010.png)


## Summary

You've now ...

Continue to - [Exercise 2 - Exercise 2 Description](../ex2/README.md)

