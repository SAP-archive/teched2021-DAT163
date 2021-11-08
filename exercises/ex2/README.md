# Exercise 2 - Exercise 2 Description

In this exercise, we will create...

## Modify Preparation

After completing these steps you will have created...

1. Click 'View Preparation'
<br>![](/exercises/ex2/images/Ex02_Part01_01.png)

2. Click 'DRUG_01'
<br>![](/exercises/ex2/images/Ex02_Part01_02.png)

3. This opens your preparation
<br>![](/exercises/ex2/images/Ex02_Part01_03.png)

4. Click 'Recipe'
<br>![](/exercises/ex2/images/Ex02_Part01_04.png)

5. Edit the 'Enrich' action
<br>![](/exercises/ex2/images/Ex02_Part01_05.png)

6. This opens the Enrich window with the defined Enrich action
<br>![](/exercises/ex2/images/Ex02_Part01_06.png)

7. Click the 'Join' icon
<br>![](/exercises/ex2/images/Ex02_Part01_07.png)

8. the join definition window opens. Scroll down
<br>![](/exercises/ex2/images/Ex02_Part01_08.png)

9. Check 'POTENCY'
<br>![](/exercises/ex2/images/Ex02_Part01_09.png)

10. Click 'Apply'
<br>![](/exercises/ex2/images/Ex02_Part01_10.png)

11. 'POTENCY' is now added in the output columns
<br>![](/exercises/ex2/images/Ex02_Part01_11.png)

12. Click 'Apply Enrichment'
<br>![](/exercises/ex2/images/Ex02_Part01_12.png)

13. The daset is now enriched with the additional selected column
<br>![](/exercises/ex2/images/Ex02_Part01_13.png)

14. Click 'Recipe'
<br>![](/exercises/ex2/images/Ex02_Part01_14.png)

15. Edit the 'Add Column' action
<br>![](/exercises/ex2/images/Ex02_Part01_15.png)

16. Change the 'Column Name' from ValidClaim to VALID_DRUG
<br>![](/exercises/ex2/images/Ex02_Part01_16.png)

17. Click 'Save'
<br>![](/exercises/ex2/images/Ex02_Part01_17.png)

18. The column name has changed
<br>![](/exercises/ex2/images/Ex02_Part01_18.png)

19. Click 'Add Filter'
<br>![](/exercises/ex2/images/Ex02_Part01_19.png)

20. Select 'VALID_DRUG'
<br>![](/exercises/ex2/images/Ex02_Part01_20.png)

21. Type 'NO' in the associated filter text field.
<br>![](/exercises/ex2/images/Ex02_Part01_21.png)

22. Type enter to validate the filter
<br>![](/exercises/ex2/images/Ex02_Part01_22.png)

23. This filters the data with only claims containing an invalid drug
<br>![](/exercises/ex2/images/Ex02_Part01_23.png)

24. Click the 'DRUG_NAME' Column Header, and sort acending
<br>![](/exercises/ex2/images/Ex02_Part01_24.png)

25. The data are sorted by 'DRUG_NAME' by ascending order, but the first records contains null values
<br>![](/exercises/ex2/images/Ex02_Part01_25.png)

26. Click 'Add Filter' and Select 'DRUG_NAME'
<br>![](/exercises/ex2/images/Ex02_Part01_26.png)

27. Click the '=' icon associated to the 'DRUG_NAME' filter
<br>![](/exercises/ex2/images/Ex02_Part01_27.png)

28. Select 'Not Null'
<br>![](/exercises/ex2/images/Ex02_Part01_28.png)

29. This shows only the claims with unknown drugs which are not null
<br>![](/exercises/ex2/images/Ex02_Part01_29.png)

30. CLick '<' to come back to the list of available actions
<br>![](/exercises/ex2/images/Ex02_Part01_30.png)

31. Click 'Aggregate Preparation'
<br>![](/exercises/ex2/images/Ex02_Part01_31.png)

32. The aggregate window shows up. The filter defined in the main data preparation room are automatically pre-defined in the aggregation window
<br>![](/exercises/ex2/images/Ex02_Part01_32.png)

33. Double-click or Drag and drop 'DRUG_NAME' in the 'Output Columns' area
<br>![](/exercises/ex2/images/Ex02_Part01_33.png)

34. This defines the aggregation with a preview of the result.
<br>![](/exercises/ex2/images/Ex02_Part01_34.png)

35. Double-click or Drag and drop 'DRUG_NAME' in the 'Output Columns' area
<br>![](/exercises/ex2/images/Ex02_Part01_35.png)

36. Change the Aggregation function from 'No Aggregation' to 'Count'
<br>![](/exercises/ex2/images/Ex02_Part01_36.png)

37. This shows the preview of the aggregation that contains the distinct values of drug names with their respective count
<br>![](/exercises/ex2/images/Ex02_Part01_37.png)

38. Click 'Apply Aggregation'
<br>![](/exercises/ex2/images/Ex02_Part01_38.png)

39. The main data preparation room now contains the aggregated data. The data could be exported as-is (as this is based only on a sample of the data) for further study and analysis. We can see already some simple data quality issues in the name of the drugs which we will curate later on.
<br>![](/exercises/ex2/images/Ex02_Part01_39.png)

40. For now, we can disable this aggregation (but still keep it's definition). Click 'Recipe'
<br>![](/exercises/ex2/images/Ex02_Part01_40.png)

41. Click 'More Actions' for the 'Aggregate' action in the recipe
<br>![](/exercises/ex2/images/Ex02_Part01_41.png)

42. Click 'Disable'
<br>![](/exercises/ex2/images/Ex02_Part01_42.png)

43. The aggregation action is now disabled. The data preparation room shows the data prior executing the aggregation. The filters that were defined were automatically removed (but are still embedded in the definition of the aggregation). At any point of time, we can come back to this data preparation recipe and reactive this action.
<br>![](/exercises/ex2/images/Ex02_Part01_43.png)

44. Click 'Actions'
<br>![](/exercises/ex2/images/Ex02_Part01_44.png)

45. Click 'Run Preparation'
<br>![](/exercises/ex2/images/Ex02_Part01_45.png)

46. Click the 'Container' icon
<br>![](/exercises/ex2/images/Ex02_Part01_46.png)

47. Select 'PHARMA-CLAIMS_ENRICHED_#' (where # is your user number)
<br>![](/exercises/ex2/images/Ex02_Part01_47.png)

48. Click 'Apply'
<br>![](/exercises/ex2/images/Ex02_Part01_48.png)

49. This defines it will overwrite the content of the data with this new definition
<br>![](/exercises/ex2/images/Ex02_Part01_49.png)

50. Click 'Apply'
<br>![](/exercises/ex2/images/Ex02_Part01_50.png)

51. Click 'Yes'
<br>![](/exercises/ex2/images/Ex02_Part01_51.png)

52. Wait until you see a notification for the task being completed
<br>![](/exercises/ex2/images/Ex02_Part01_52.png)

53. Click 'Data Intelligence Metadata Explorer'. Click 'Browse Connections'.
<br>![](/exercises/ex2/images/Ex02_Part01_53.png)

54. Click 'DI_DATA_LAKE'
<br>![](/exercises/ex2/images/Ex02_Part01_54.png)

55. Click 'shared'
<br>![](/exercises/ex2/images/Ex02_Part01_55.png)

56. Filter the data with 'TechEd_DAT163_#' (where # is your user number)
<br>![](/exercises/ex2/images/Ex02_Part01_56.png)

57. Click 'TechEd_DAT163_#' (where # is your user number)
<br>![](/exercises/ex2/images/Ex02_Part01_57.png)

58. Click 'View Factsheet' for the file 'PHARMA_CLAIMS_ENRICH_#' (where # is your user number)
<br>![](/exercises/ex2/images/Ex02_Part01_58.png)

59. The application shows the factsheet associated to the selected dataset.
<br>![](/exercises/ex2/images/Ex02_Part01_59.png)

60. Click 'Column'
<br>![](/exercises/ex2/images/Ex02_Part01_60.png)

61. Thte columns are not profiled anymore. This is because the structure of the data changed when we modified the definition in the recipe associated to the preparation task (added the column POTENCY, changed one column name)
<br>![](/exercises/ex2/images/Ex02_Part01_61.png)

62. Click 'Profile Data'
<br>![](/exercises/ex2/images/Ex02_Part01_62.png)

63. Click 'Yes'
<br>![](/exercises/ex2/images/Ex02_Part01_63.png)

64. Wait to receive both notification that signify that the profiling task started and finished successfully.
<br>![](/exercises/ex2/images/Ex02_Part01_64.png)

65. Click 'Refresh'
<br>![](/exercises/ex2/images/Ex02_Part01_65.png)

66. The data are profiled again, there is a new version of the profiling information available. Previous information of the profiling metadata stays available. Click 'Columns'
<br>![](/exercises/ex2/images/Ex02_Part01_66.png)

67. All the new profiling information are available.
<br>![](/exercises/ex2/images/Ex02_Part01_67.png)

68. Click 'Data Intelligence Metadata Explorer'. Click 'Home'.
<br>![](/exercises/ex2/images/Ex02_Part01_68.png)

69. Click 'scheduled tasks' to create a new scheduled task.
<br>![](/exercises/ex2/images/Ex02_Part01_69.png)

70. Click 'Add' to add a new task.
<br>![](/exercises/ex2/images/Ex02_Part01_70.png)

71. Click the 'Name' field to select the publication name to schedule.
<br>![](/exercises/ex2/images/Ex02_Part01_71.png)

72. Type 'Pharma Claims Publication #' in the 'Filter Publications' text field. (Where # is your user number)
<br>![](/exercises/ex2/images/Ex02_Part01_72.png)

73. Select your publication (for example if you are user 01, select Pharma Claims Publication 01).
<br>![](/exercises/ex2/images/Ex02_Part01_73.png)

74. Click 'OK'
<br>![](/exercises/ex2/images/Ex02_Part01_74.png)

75. Open the 'Picker' icon to give you few more minutes for the first schedule of the selected publication.
<br>![](/exercises/ex2/images/Ex02_Part01_75.png)

76. add 5 more minutes to the original value. For example, if the value was 06:45, set it to 06:50. Click 'OK'
<br>![](/exercises/ex2/images/Ex02_Part01_76.png)

77. Click 'Save'
<br>![](/exercises/ex2/images/Ex02_Part01_77.png)

78. Wait until the scheduled publication task is executed.
<br>![](/exercises/ex2/images/Ex02_Part01_78.png)

79. Once done, the status will change to 'completed'
<br>![](/exercises/ex2/images/Ex02_Part01_79.png)

80. Click on the scheduled task to see the details.
<br>![](/exercises/ex2/images/Ex02_Part01_80.png)

81. Click 'Data Intelligence Metadata Explorer'. Click 'Home'.
<br>![](/exercises/ex2/images/Ex02_Part01_81.png)

82. You are back to the solution home page.
<br>![](/exercises/ex2/images/Ex02_Part01_82.png)

## Business Glossary

1. Click 'glossaries' to access or create a new glossary
<br>![](/exercises/ex2/images/Ex02_Part02_01.png)

2. You can access or create glossaries
<br>![](/exercises/ex2/images/Ex02_Part02_02.png)

3. Click '+'
<br>![](/exercises/ex2/images/Ex02_Part02_03.png)

4. Type 'DRUGS_GLOSSARY_01' in the 'Name' text field.
<br>![](/exercises/ex2/images/Ex02_Part02_04.png)

5. Select the 'GLOSSARY' Template.
<br>![](/exercises/ex2/images/Ex02_Part02_05.png)

6. Type the following description: 'Glossary for pharmaceutical drugs'.
<br>![](/exercises/ex2/images/Ex02_Part02_07.png)

7. Your can create your glossary
<br>![](/exercises/ex2/images/Ex02_Part02_07.png)

8. Click 'Save'.
<br>![](/exercises/ex2/images/Ex02_Part02_08.png)

9. You created a glossary, and now can start enriching it with new terms.
<br>![](/exercises/ex2/images/Ex02_Part02_09.png)

10. Click '+' to create a new term.
<br>![](/exercises/ex2/images/Ex02_Part02_10.png)

11. The term creation windows shows up.
<br>![](/exercises/ex2/images/Ex02_Part02_11.png)

12. Type 'Potency' in the 'Name' text field.
<br>![](/exercises/ex2/images/Ex02_Part02_12.png)

13. Type the following definition for the term: 'Measure of drug activity expressed in terms of the amount required to produce an effect of given intensity.
<br>![](/exercises/ex2/images/Ex02_Part02_13.png)

14. Click 'Save'
<br>![](/exercises/ex2/images/Ex02_Part02_14.png)

15. Click '<' to come back to the list of terms.
<br>![](/exercises/ex2/images/Ex02_Part02_15.png)

16. The term is created and part of the glossary definitions. Click 'Potency'.
<br>![](/exercises/ex2/images/Ex02_Part02_16.png)

17. the term window shows up.
<br>![](/exercises/ex2/images/Ex02_Part02_17.png)

18. Click 'Edit'
<br>![](/exercises/ex2/images/Ex02_Part02_18.png)

19. Click 'Relationships'
<br>![](/exercises/ex2/images/Ex02_Part02_19.png)

20. Click 'Edit Related Objects'.
<br>![](/exercises/ex2/images/Ex02_Part02_20.png)

21. Click 'Datasets/Columns'.
<br>![](/exercises/ex2/images/Ex02_Part02_21.png)

22. Click 'DI_DATA_LAKE'
<br>![](/exercises/ex2/images/Ex02_Part02_22.png)

23. Search 'CLAIMS_*_##' *(where # is your user number)
<br>![](/exercises/ex2/images/Ex02_Part02_23.png)

24. Check your dataset (for example PHARMA_CLAIMS_ENRICHED_01 if your user number is 01).
<br>![](/exercises/ex2/images/Ex02_Part02_24.png)

25.  Click 'View Columns'.
<br>![](/exercises/ex2/images/Ex02_Part02_25.png)

26. Check 'Potency'. Click 'Save Related Objects'.
<br>![](/exercises/ex2/images/Ex02_Part02_26.png)

27. The term is now associated to a dataset and a column in this dataset.
<br>![](/exercises/ex2/images/Ex02_Part02_27.png)

28. Click 'Data Intelligence Metadata Explorer'. Click 'Home'.
<br>![](/exercises/ex2/images/Ex02_Part02_28.png)

29. Type 'CLAIMS' in the search bar.
<br>![](/exercises/ex2/images/Ex02_Part02_29.png)

30. Type enter key.
<br>![](/exercises/ex2/images/Ex02_Part02_30.png)

31. The Catalog shows the results of the dataset that matches the search pattern.
<br>![](/exercises/ex2/images/Ex02_Part02_31.png)

32. Click the 'Filter' icon.
<br>![](/exercises/ex2/images/Ex02_Part02_32.png)

33. Change the Search string to 'CLAIMS_*_##' *(where ## is your user number)
<br>![](/exercises/ex2/images/Ex02_Part02_33.png)

34. Click 'Apply'.
<br>![](/exercises/ex2/images/Ex02_Part02_34.png)

35. Click 'More Actions'.
<br>![](/exercises/ex2/images/Ex02_Part02_35.png)

36. Click 'View Factsheet'.
<br>![](/exercises/ex2/images/Ex02_Part02_36.png)

37. Click 'Overview'.
<br>![](/exercises/ex2/images/Ex02_Part02_37.png)
 
38. Click 'Relationships'.
<br>![](/exercises/ex2/images/Ex02_Part02_38.png)

39. Click 'Terms and Tags'.
<br>![](/exercises/ex2/images/Ex02_Part02_39.png)

40. The glossary term 'Potency' is associated to the dataset. Click 'Columns'.
<br>![](/exercises/ex2/images/Ex02_Part02_40.png)

41. Click 'POTENCY'.
<br>![](/exercises/ex2/images/Ex02_Part02_41.png)

42. The glossary term 'Potency' is associated to the 'POTENCY' column of the dataset.
<br>![](/exercises/ex2/images/Ex02_Part02_42.png)

43. Click 'Data Intelligence Metadata Explorer'. Click 'Home'.
<br>![](/exercises/ex2/images/Ex02_Part02_43.png)

44. You are back to the Data Intellience Metadata Explorer Home page.
<br>![](/exercises/ex2/images/Ex02_Part02_44.png)

## Rules

1. Click 'rules' to access existing or create new rules.
<br>![](/exercises/ex2/images/Ex02_Part03_01.png)

## Exercise 2.1 Sub Exercise 1 Description

After completing these steps you will have created...

1. Click here.
<br>![](/exercises/ex2/images/02_01_0010.png)

2.	Insert this line of code.
```abap
response->set_text( |Hello ABAP World! | ). 
```



## Exercise 2.2 Sub Exercise 2 Description

After completing these steps you will have...

1.	Enter this code.
```abap
DATA(lt_params) = request->get_form_fields(  ).
READ TABLE lt_params REFERENCE INTO DATA(lr_params) WITH KEY name = 'cmd'.
  IF sy-subrc = 0.
    response->set_status( i_code = 200
                     i_reason = 'Everything is fine').
    RETURN.
  ENDIF.

```

2.	Click here.
<br>![](/exercises/ex2/images/02_02_0010.png)

## Summary

You've now ...

Continue to - [Exercise 3 - Excercise 3 ](../ex3/README.md)
