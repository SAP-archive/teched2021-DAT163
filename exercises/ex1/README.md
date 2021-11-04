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

8. Select 'DEMO'
<br>![](/exercises/ex1/images/Ex01_Part03_08.png)

9. Click 'View FactSheet'
<br>![](/exercises/ex1/images/Ex01_Part03_09.png)

10. Click 'Start Profiling'
<br>![](/exercises/ex1/images/Ex01_Part03_10.png)

9. Click 'Notification'

10. Wait and Click 'Refresh'

11. Click 'Columns'

12. Select the Line for 'DRUG_NAME'

13. Click 'Data Intelligence Metadata Explorer'

14. Click 'Home'

We have...


## Upload your Dataset

After completing these steps you will have uploaded and published datasets in SAP Data Intellegence

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

