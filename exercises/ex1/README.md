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

## Upload your Dataset

After completing these steps you will have uploaded and published datasets in SAP Data Intellegence

1. Click on 'Metadata Explorer'

2. Click on 'Browse Connections'

3. Click on the 'DI_DATA_LAKE' tile

4. Click on the 'shared' tile

5. Click on the New Folder icon (folder with a +)

7. Enter 'TechEd_DAT163_#' for folder name
Note: where # is the number assigned to you

8. Click 'OK'

9. Search for 'TechEd_DAT163_#' to isolate your newly created folder, then click on your newly added 'TechEd_DAT163_#' folder
Note: where # is the number assigned to you

10. Upload a file, click on the 'Upload Files' icon on the toolbar

11. Click on the '+' in the upper right hand corner of the Upload Files pop-up window

12. Browse to Sample Data folder where you downloaded 'Customer_US.parquet' and 'Sales_data.csv' and select 'Customer_US_#.parquet'
Note: where # is the number assigned to you

13. Click 'Open'

14. Click on the '+' in the upper right hand corner of the Upload Files pop-up window

15. Click 'Upload'

16. After Upload is Complete, click 'Close'

17. 

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

