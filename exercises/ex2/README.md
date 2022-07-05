# Hands-on - Part 2 (Govern and Monitor Data Quality)

In this exercise, you will continue to interact with the enriched dataset you created in the previous part.
You will first modify the recipe you used to create that dataset, schedule a publication so it can take into account potential metadata changes in the future.
Then you will create rules and a rulebook to visually track the data quality issues that were found.
Finally you will curate the data.

## Modify Preparation

After completing these steps you will have modified your data preparation recipe to further isolate the data quality issues on a specific column.
Then you will schedule a publication of this dataset to take into account potantial metadata changes in the future.

1. Click 'View Preparation'.
<br>![](/exercises/ex2/images/Ex02_Part01_01.png)

2. Click 'DRUG_##' (where ## is your user number).
<br>![](/exercises/ex2/images/Ex02_Part01_02.png)

3. This opens your preparation.
<br>![](/exercises/ex2/images/Ex02_Part01_03.png)

4. Click 'Recipe'.
<br>![](/exercises/ex2/images/Ex02_Part01_04.png)

5. Edit the 'Enrich' action.
<br>![](/exercises/ex2/images/Ex02_Part01_05.png)

6. This opens the Enrich window with the defined Enrich action.
<br>![](/exercises/ex2/images/Ex02_Part01_06.png)

7. Click the 'Join' icon.
<br>![](/exercises/ex2/images/Ex02_Part01_07.png)

8. The join definition window opens. Scroll down.
<br>![](/exercises/ex2/images/Ex02_Part01_08.png)

9. Check 'POTENCY'.
<br>![](/exercises/ex2/images/Ex02_Part01_09.png)

10. Click 'Apply'.
<br>![](/exercises/ex2/images/Ex02_Part01_10.png)

11. 'POTENCY' is now added in the output columns.
<br>![](/exercises/ex2/images/Ex02_Part01_11.png)

12. Click 'Apply Enrichment'.
<br>![](/exercises/ex2/images/Ex02_Part01_12.png)

13. The daset is now enriched with the additional selected column.
<br>![](/exercises/ex2/images/Ex02_Part01_13.png)

14. Click 'Recipe'.
<br>![](/exercises/ex2/images/Ex02_Part01_14.png)

15. Edit the 'Add Column' action.
<br>![](/exercises/ex2/images/Ex02_Part01_15.png)

16. Change the 'Column Name' from ValidClaim to VALID_DRUG.
<br>![](/exercises/ex2/images/Ex02_Part01_16.png)

17. Click 'Save'.
<br>![](/exercises/ex2/images/Ex02_Part01_17.png)

18. The column name has changed.
<br>![](/exercises/ex2/images/Ex02_Part01_18.png)

19. Click 'Add Filter'.
<br>![](/exercises/ex2/images/Ex02_Part01_19.png)

20. Select 'VALID_DRUG'.
<br>![](/exercises/ex2/images/Ex02_Part01_20.png)

21. Type 'NO' in the associated filter text field.
<br>![](/exercises/ex2/images/Ex02_Part01_21.png)

22. Press Enter key to validate the filter.
<br>![](/exercises/ex2/images/Ex02_Part01_22.png)

23. This filters the data with only claims containing an invalid drug.
<br>![](/exercises/ex2/images/Ex02_Part01_23.png)

24. Click the 'DRUG_NAME' Column Header, and sort acending.
<br>![](/exercises/ex2/images/Ex02_Part01_24.png)

25. The data are sorted by 'DRUG_NAME' by ascending order, but the first records contains null values.
<br>![](/exercises/ex2/images/Ex02_Part01_25.png)

26. Click 'Add Filter' and Select 'DRUG_NAME'.
<br>![](/exercises/ex2/images/Ex02_Part01_26.png)

27. Click the '=' icon associated to the 'DRUG_NAME' filter.
<br>![](/exercises/ex2/images/Ex02_Part01_27.png)

28. Select 'Not Null'.
<br>![](/exercises/ex2/images/Ex02_Part01_28.png)

29. This shows only the claims with unknown drugs which are not null.
<br>![](/exercises/ex2/images/Ex02_Part01_29.png)

30. Click '<' to come back to the 'Run Preparation' menu.
<br>![](/exercises/ex2/images/Ex02_Part01_30.png)

30. Click once again '<' to come back to the list of available actions.
<br>![](/exercises/ex2/images/Ex02_Part01_30b.png)

31. Click 'Aggregate Preparation'.
<br>![](/exercises/ex2/images/Ex02_Part01_31.png)

32. The aggregate window shows up. The filter defined in the main data preparation room are automatically pre-defined in the aggregation window.
<br>![](/exercises/ex2/images/Ex02_Part01_32.png)

33. Drag and drop 'DRUG_NAME' in the 'Output Columns' area.
<br>![](/exercises/ex2/images/Ex02_Part01_33.png)

34. This defines the aggregation with a preview of the result.
<br>![](/exercises/ex2/images/Ex02_Part01_34.png)

35. Drag and drop 'DRUG_NAME' in the 'Output Columns' area.
<br>![](/exercises/ex2/images/Ex02_Part01_35.png)

36. This will generate an expected error message as right now the system considers we are trying to aggregate data twice on the same column.
<br>![](/exercises/ex2/images/Ex02_Part01_36.png)

37. Change the Aggregation function from 'No Aggregation' to 'Count'.
<br>![](/exercises/ex2/images/Ex02_Part01_37.png)

38. This shows the preview of the aggregation that contains the distinct values of drug names with their respective count.
<br>![](/exercises/ex2/images/Ex02_Part01_38.png)

39. Click 'Apply Aggregation'.
<br>![](/exercises/ex2/images/Ex02_Part01_39.png)

40. The main data preparation room now contains the aggregated data. The data could be exported as-is (as this is based only on a sample of the data) for further study and analysis. We can see already some simple data quality issues in the name of the drugs which we will curate later on.
<br>![](/exercises/ex2/images/Ex02_Part01_40.png)

41. For now, we can disable this aggregation (but still keep it's definition). Click 'Recipe'.
<br>![](/exercises/ex2/images/Ex02_Part01_41.png)

42. Click 'More Actions' for the 'Aggregate' action in the recipe.
<br>![](/exercises/ex2/images/Ex02_Part01_42.png)

43. Click 'Disable'.
<br>![](/exercises/ex2/images/Ex02_Part01_43.png)

44. The aggregation action is now disabled. The data preparation room shows the data prior executing the aggregation. The filters that were defined were automatically removed (but are still embedded in the definition of the aggregation). At any point of time, we can come back to this data preparation recipe and reactivate this action.
<br>![](/exercises/ex2/images/Ex02_Part01_44.png)

45. Click 'Actions'.
<br>![](/exercises/ex2/images/Ex02_Part01_45.png)

46. Click 'Run Preparation'.
<br>![](/exercises/ex2/images/Ex02_Part01_46.png)

47. Click the 'Container' icon.
<br>![](/exercises/ex2/images/Ex02_Part01_47.png)

48. Select 'PHARMA-CLAIMS_ENRICHED_##' (where ## is your user number).
<br>![](/exercises/ex2/images/Ex02_Part01_48.png)

49. Click 'Apply'.
<br>![](/exercises/ex2/images/Ex02_Part01_49.png)

50. This defines it will overwrite the content of the data with this new definition.
<br>![](/exercises/ex2/images/Ex02_Part01_50.png)

51. Click 'Apply'.
<br>![](/exercises/ex2/images/Ex02_Part01_51.png)

52. Click 'Yes'.
<br>![](/exercises/ex2/images/Ex02_Part01_52.png)

53. Wait until you see a notification for the task being completed.
<br>![](/exercises/ex2/images/Ex02_Part01_53.png)

54. Click 'Data Intelligence Metadata Explorer'. Click 'Browse Connections'.
<br>![](/exercises/ex2/images/Ex02_Part01_54.png)

55. Click 'DI_DATA_LAKE'.
<br>![](/exercises/ex2/images/Ex02_Part01_55.png)

56. Click 'shared'.
<br>![](/exercises/ex2/images/Ex02_Part01_56.png)

57. Filter the data with 'TechEd_DAT163_##' (where ## is your user number).
<br>![](/exercises/ex2/images/Ex02_Part01_57.png)

58. Click 'TechEd_DAT163_##' (where ## is your user number).
<br>![](/exercises/ex2/images/Ex02_Part01_58.png)

59. Click 'View Factsheet' for the file 'PHARMA_CLAIMS_ENRICH_##' (where ## is your user number).
<br>![](/exercises/ex2/images/Ex02_Part01_59.png)

60. The application shows the factsheet associated to the selected dataset.
<br>![](/exercises/ex2/images/Ex02_Part01_60.png)

61. Click 'Column'.
<br>![](/exercises/ex2/images/Ex02_Part01_61.png)

62. The columns are not profiled anymore. This is because the structure of the data changed when we modified the definition in the recipe associated to the preparation task (added the column POTENCY, changed one column name).
<br>![](/exercises/ex2/images/Ex02_Part01_62.png)

63. Click 'Profile Data'.
<br>![](/exercises/ex2/images/Ex02_Part01_63.png)

64. Click 'Yes'.
<br>![](/exercises/ex2/images/Ex02_Part01_64.png)

65. Wait to receive both notification that signify that the profiling task started and finished successfully.
<br>![](/exercises/ex2/images/Ex02_Part01_65.png)

66. Click 'Refresh'.
<br>![](/exercises/ex2/images/Ex02_Part01_66.png)

67. The data are profiled again, there is a new version of the profiling information available. Previous information of the profiling metadata stays available. Click 'Columns'.
<br>![](/exercises/ex2/images/Ex02_Part01_67.png)

68. All the new profiling information are available.
<br>![](/exercises/ex2/images/Ex02_Part01_68.png)

69. Click 'Data Intelligence Metadata Explorer'. Click 'Home'.
<br>![](/exercises/ex2/images/Ex02_Part01_69.png)

Because you changed the structure of the dataset, you would also need to publish the dataset once again to the catalog.
However, instead of repeating this operation, you can schedule the publication of the dataset instead of doing it manually every time the structure of the data changes.

70. Click 'scheduled tasks' to create a new scheduled task.
<br>![](/exercises/ex2/images/Ex02_Part01_70.png)

71. Click 'Add' to add a new task.
<br>![](/exercises/ex2/images/Ex02_Part01_71.png)

72. Click the 'Name' field to select the publication name to schedule.
<br>![](/exercises/ex2/images/Ex02_Part01_72.png)

73. Type 'Pharma Claims Publication ##' in the 'Filter Publications' text field. (Where ## is your user number).
<br>![](/exercises/ex2/images/Ex02_Part01_73.png)

74. Select your publication (for example if you are user 01, select Pharma Claims Publication 01).
<br>![](/exercises/ex2/images/Ex02_Part01_74.png)

75. Click 'OK'.
<br>![](/exercises/ex2/images/Ex02_Part01_75.png)

76. Open the 'Picker' icon to give you few more minutes for the first schedule of the selected publication.
<br>![](/exercises/ex2/images/Ex02_Part01_76.png)

77. Add 5 more minutes to the original value. For example, if the value was 06:45, set it to 06:50. Click 'OK'.
<br>![](/exercises/ex2/images/Ex02_Part01_77.png)

78. Click 'Save'.
<br>![](/exercises/ex2/images/Ex02_Part01_78.png)

79. Wait until the scheduled publication task is executed.
<br>![](/exercises/ex2/images/Ex02_Part01_79.png)

80. Once done, the status will change to 'completed'.
<br>![](/exercises/ex2/images/Ex02_Part01_80.png)

81. Click on the scheduled task to see the details.
<br>![](/exercises/ex2/images/Ex02_Part01_81.png)

82. Click 'Data Intelligence Metadata Explorer'. Click 'Home'.
<br>![](/exercises/ex2/images/Ex02_Part01_82.png)

83. You are back to the solution home page.
<br>![](/exercises/ex2/images/Ex02_Part01_83.png)

You have now modified your data preparation recipe to further isolate the data quality issues on a specific column.
You also have scheduled a publication of this dataset to take into account potantial metadata changes in the future.

## Business Glossary

After completing these steps you will have created a glossary and business terms and associated them to your enriched dataset.

1. Click 'glossaries' to access or create a new glossary.
<br>![](/exercises/ex2/images/Ex02_Part02_01.png)

2. You can access or create glossaries.
<br>![](/exercises/ex2/images/Ex02_Part02_02.png)

3. Click '+'.
<br>![](/exercises/ex2/images/Ex02_Part02_03.png)

4. Type 'DRUGS_GLOSSARY_##' in the 'Name' text field (where ## is your user number).
<br>![](/exercises/ex2/images/Ex02_Part02_04.png)

5. Select the 'GLOSSARY' Template.
<br>![](/exercises/ex2/images/Ex02_Part02_05.png)

6. Type the following description: 'Glossary for pharmaceutical drugs'.
<br>![](/exercises/ex2/images/Ex02_Part02_06.png)

7. You can create your glossary.
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

13. Type the following definition for the term: 'Measure of drug activity expressed in terms of the amount required to produce an effect of given intensity'.
<br>![](/exercises/ex2/images/Ex02_Part02_13.png)

14. Click 'Save'.
<br>![](/exercises/ex2/images/Ex02_Part02_14.png)

15. Click the 'Go back to term list' icon.
<br>![](/exercises/ex2/images/Ex02_Part02_15.png)

16. The 'Term' is created and part of the glossary definitions. Click 'Potency'.
<br>![](/exercises/ex2/images/Ex02_Part02_16.png)

17. the term window shows up.
<br>![](/exercises/ex2/images/Ex02_Part02_17.png)

18. Click 'Edit'.
<br>![](/exercises/ex2/images/Ex02_Part02_18.png)

19. Click 'Relationships'.
<br>![](/exercises/ex2/images/Ex02_Part02_19.png)

20. Click 'Manage Relationships'.
<br>![](/exercises/ex2/images/Ex02_Part02_20.png)

21. Click 'Datasets or Columns'.
<br>![](/exercises/ex2/images/Ex02_Part02_21.png)

22. Click 'DI_DATA_LAKE'.
<br>![](/exercises/ex2/images/Ex02_Part02_22.png)

23. Click 'shared'.
<br>![](/exercises/ex2/images/Ex02_Part02_23.png)

24. Search 'DAT163_##' (where ## is your user number).
<br>![](/exercises/ex2/images/Ex02_Part02_24.png)

25. Check your dataset (for example PHARMA_CLAIMS_ENRICHED_01 if your user number is 01).
<br>![](/exercises/ex2/images/Ex02_Part02_25.png)

26.  Click 'View Columns'.
<br>![](/exercises/ex2/images/Ex02_Part02_26.png)

27. Check 'Potency'. Click 'Save Related Objects'.
<br>![](/exercises/ex2/images/Ex02_Part02_27.png)

28. The term is now associated to a dataset and a column in this dataset.
<br>![](/exercises/ex2/images/Ex02_Part02_28.png)

29. Click 'Data Intelligence Metadata Explorer'. Click 'Home'.
<br>![](/exercises/ex2/images/Ex02_Part02_29.png)

30. Type 'CLAIMS' in the search bar.
<br>![](/exercises/ex2/images/Ex02_Part02_30.png)

31. Press Enter key.
<br>![](/exercises/ex2/images/Ex02_Part02_31.png)

32. The Catalog shows the results of the dataset that matches the search pattern.
<br>![](/exercises/ex2/images/Ex02_Part02_32.png)

33. Click the 'Filter' icon.
<br>![](/exercises/ex2/images/Ex02_Part02_33.png)

34. Change the Search string to 'CLAIMS_*_##' *(where ## is your user number).
<br>![](/exercises/ex2/images/Ex02_Part02_34.png)

35. Click 'Apply'.
<br>![](/exercises/ex2/images/Ex02_Part02_35.png)

36. Click 'More Actions'.
<br>![](/exercises/ex2/images/Ex02_Part02_36.png)

37. Click 'View Factsheet'.
<br>![](/exercises/ex2/images/Ex02_Part02_37.png)

38. Click 'Overview'.
<br>![](/exercises/ex2/images/Ex02_Part02_38.png)
 
39. Click 'Relationships'.
<br>![](/exercises/ex2/images/Ex02_Part02_39.png)

40. Click 'Terms and Tags'.
<br>![](/exercises/ex2/images/Ex02_Part02_40.png)

41. The glossary term 'Potency' is associated to the dataset. Click 'Columns'.
<br>![](/exercises/ex2/images/Ex02_Part02_41.png)

42. Click 'POTENCY'.
<br>![](/exercises/ex2/images/Ex02_Part02_42.png)

43. The glossary term 'Potency' is associated to the 'POTENCY' column of the dataset.
<br>![](/exercises/ex2/images/Ex02_Part02_43.png)

44. Click 'Data Intelligence Metadata Explorer'. Click 'Home'.
<br>![](/exercises/ex2/images/Ex02_Part02_44.png)

45. You are back to the Data Intellience Metadata Explorer Home page.
<br>![](/exercises/ex2/images/Ex02_Part02_45.png)

You have now created a glossary and business terms and associated them to your enriched dataset.

## Rules

After completing these steps you will have created rules and a rulebook that is evaluating the data quality of your enriched dataset.

1. Click 'rules' to access existing or create new rules.
<br>![](/exercises/ex2/images/Ex02_Part03_01.png)

2. Click '+' to create a new 'Completeness' rule.
<br>![](/exercises/ex2/images/Ex02_Part03_02.png)

3. Type 'DRUG_NAME_EXISTS_##' for both the 'Rule ID' and the 'Name' (where ## is your user id).
<br>![](/exercises/ex2/images/Ex02_Part03_03.png)
 
4. Type the following 'Description': Drug Name must not be null.
<br>![](/exercises/ex2/images/Ex02_Part03_04.png)

5. Click 'Save'.
<br>![](/exercises/ex2/images/Ex02_Part03_05.png)

6. The main rule editor window shows up.
<br>![](/exercises/ex2/images/Ex02_Part03_06.png)

7. Click '+'.
<br>![](/exercises/ex2/images/Ex02_Part03_07.png)

8. Type 'DRUG_NAME' for the 'Name' of the parameter for the rule.
<br>![](/exercises/ex2/images/Ex02_Part03_08.png)

9. Select the 'Type'.
<br>![](/exercises/ex2/images/Ex02_Part03_09.png)

10. Select 'String'.
<br>![](/exercises/ex2/images/Ex02_Part03_10.png)

11. Click 'Save'.
<br>![](/exercises/ex2/images/Ex02_Part03_11.png)

12. The parameter is created.
<br>![](/exercises/ex2/images/Ex02_Part03_12.png)

13. Click '+' to define the condition.
<br>![](/exercises/ex2/images/Ex02_Part03_13.png)

14. Type 'DRUG_NAME_NOT_NULL' for the 'Condition Name'.
<br>![](/exercises/ex2/images/Ex02_Part03_14.png)

15. Select 'DRUG_NAME' for the parameter.
<br>![](/exercises/ex2/images/Ex02_Part03_15.png)

16. Click 'Save'.
<br>![](/exercises/ex2/images/Ex02_Part03_16.png)

17. Click '<' to go back to the list of categories.
<br>![](/exercises/ex2/images/Ex02_Part03_17.png)

18. Click 'More Actions' to create a new 'Accuracy' rule.
<br>![](/exercises/ex2/images/Ex02_Part03_18.png)

19. Click 'Create Rule'.
<br>![](/exercises/ex2/images/Ex02_Part03_19.png)

20. Type 'DRUG_NAME_VALID_##' for both the 'Rule ID' and the 'Name' (where ## is your user id).
<br>![](/exercises/ex2/images/Ex02_Part03_20.png)
 
21. Type the following 'Description': The drug name is valid.
<br>![](/exercises/ex2/images/Ex02_Part03_21.png)

22. Click 'Save'.
<br>![](/exercises/ex2/images/Ex02_Part03_22.png)

23. Click '+'.
<br>![](/exercises/ex2/images/Ex02_Part03_23.png)

24. Type 'DRUG_NAME_VALID' for the parameter 'Name'.
<br>![](/exercises/ex2/images/Ex02_Part03_24.png)

25. Click the 'Save' icon.
<br>![](/exercises/ex2/images/Ex02_Part03_25.png)

26. Click '+' on the 'Conditions'.
<br>![](/exercises/ex2/images/Ex02_Part03_26.png)

27. Type 'DRUG_NAME_VALID' for the 'Condition Name', select 'DRUG_NAME_VALID' for the 'Parameter Name', select 'equals' for the 'Operator', and Type 'YES' for the 'Value or Format'.
<br>![](/exercises/ex2/images/Ex02_Part03_27.png)

28. Click 'Save'.
<br>![](/exercises/ex2/images/Ex02_Part03_28.png)

29. Click '<' to navigate back to the list of rule categories.
<br>![](/exercises/ex2/images/Ex02_Part03_29.png)

30. You have created two different rules, now you can create a rulebook and associate these rules with a dataset.
<br>![](/exercises/ex2/images/Ex02_Part03_30.png)

31. Click 'Data Intelligence Metadata Explorer'.
<br>![](/exercises/ex2/images/Ex02_Part03_31.png)

32. Click 'Rules'. Click 'View Rulebooks'.
<br>![](/exercises/ex2/images/Ex02_Part03_32.png)

33. The rulebooks overview window shows up.
<br>![](/exercises/ex2/images/Ex02_Part03_33.png)

34. Click '+' to create a new rulebook.
<br>![](/exercises/ex2/images/Ex02_Part03_34.png)

35. Type 'PHARMA_CLAIMS_##' for the rulebook 'Name' (where ## is your user number).
<br>![](/exercises/ex2/images/Ex02_Part03_35.png)

36. Type the following 'Description': 'Set of rules to evaluate the quality of dataset used to track pharma claims'.
<br>![](/exercises/ex2/images/Ex02_Part03_36.png)

37. Click 'Save'.
<br>![](/exercises/ex2/images/Ex02_Part03_37.png)

38. The empty rule book is created.
<br>![](/exercises/ex2/images/Ex02_Part03_38.png)

39. Click 'Add Rule'.
<br>![](/exercises/ex2/images/Ex02_Part03_39.png)

40. Expand 'Accuracy'.
<br>![](/exercises/ex2/images/Ex02_Part03_40.png)

41. Check your rule named 'DRUG_NAME_VALID_##' (For example if your user number is 01, check the rule named 'DRUG_NAME_VALID_01).
<br>![](/exercises/ex2/images/Ex02_Part03_41.png)

42. Collapse 'Accuracy'.
<br>![](/exercises/ex2/images/Ex02_Part03_42.png)

43. Expand 'Completeness'.
<br>![](/exercises/ex2/images/Ex02_Part03_43.png)

44. Check your rule named 'DRUG_NAME_EXISTS_##' (For example if your user number is 01, check the rule named 'DRUG_NAME_EXISTS_01).
<br>![](/exercises/ex2/images/Ex02_Part03_44.png)

45. Click 'Save'.
<br>![](/exercises/ex2/images/Ex02_Part03_45.png)

46. The rules are now imported, you need to associate them with a dataset to be run against.
<br>![](/exercises/ex2/images/Ex02_Part03_46.png)
 
47. Click 'Create Rule Binding' to bind the rule with a dataset.
<br>![](/exercises/ex2/images/Ex02_Part03_47.png)

48. Click 'Step 2'.
<br>![](/exercises/ex2/images/Ex02_Part03_48.png)

49. Click 'Select a Connection'.
<br>![](/exercises/ex2/images/Ex02_Part03_49.png)

50. Select 'DI_DATA_LAKE'.
<br>![](/exercises/ex2/images/Ex02_Part03_50.png)

51. The 'DI_DATA_LAKE' connection is selected.
<br>![](/exercises/ex2/images/Ex02_Part03_51.png)
 
52. Click 'shared'.
<br>![](/exercises/ex2/images/Ex02_Part03_52.png)

53. Search 'TechEd_DAT163_##' (where ## is your user number). Click your folder.
<br>![](/exercises/ex2/images/Ex02_Part03_53.png)

54. Select 'PHARMA_CLAIMS_ENRICHED_##' (where ## is your user number).
<br>![](/exercises/ex2/images/Ex02_Part03_54.png)

55. The dataset is selected.
<br>![](/exercises/ex2/images/Ex02_Part03_55.png)

56. Click 'Step 3'.
<br>![](/exercises/ex2/images/Ex02_Part03_56.png)

57. Select a new associated mapping.
<br>![](/exercises/ex2/images/Ex02_Part03_57.png)

58. Select 'VALID_DRUG'.
<br>![](/exercises/ex2/images/Ex02_Part03_58.png)

59. Click 'Create Binding'.
<br>![](/exercises/ex2/images/Ex02_Part03_59.png)

60. Click 'Close'.
<br>![](/exercises/ex2/images/Ex02_Part03_60.png)

61. You created the binding for the first rule. Expand the second rule to create it's binding.
<br>![](/exercises/ex2/images/Ex02_Part03_61.png)

62. Click 'Create Rule Binding'.
<br>![](/exercises/ex2/images/Ex02_Part03_62.png)

63. Click 'Step 2'.
<br>![](/exercises/ex2/images/Ex02_Part03_63.png)

64. Select 'DI_DATA_LAKE'.
<br>![](/exercises/ex2/images/Ex02_Part03_64.png)

65. Click 'Step 3'.
<br>![](/exercises/ex2/images/Ex02_Part03_65.png)

66. Select a new associated mapping.
<br>![](/exercises/ex2/images/Ex02_Part03_66.png)

67. Select 'DRUG_NAME'.
<br>![](/exercises/ex2/images/Ex02_Part03_67.png)

68. Click 'Create Binding'.
<br>![](/exercises/ex2/images/Ex02_Part03_68.png)

69. Click 'Close'.
<br>![](/exercises/ex2/images/Ex02_Part03_69.png)

70. Both rules are now bound to a dataset. Click 'Run All'.
<br>![](/exercises/ex2/images/Ex02_Part03_70.png)

71. Enable 'Save All'.
<br>![](/exercises/ex2/images/Ex02_Part03_71.png)

72. Select 'Replace'.
<br>![](/exercises/ex2/images/Ex02_Part03_72.png)

73. Enable 'Create Linked Preparation'.
<br>![](/exercises/ex2/images/Ex02_Part03_73.png)

74. Click 'Run'.
<br>![](/exercises/ex2/images/Ex02_Part03_74.png)

75. The rules are being evaluated. Wait until the disabled 'View Results' is enabled.
<br>![](/exercises/ex2/images/Ex02_Part03_75.png)

76. Click 'View Results'.
<br>![](/exercises/ex2/images/Ex02_Part03_76.png)

77. The rules execution debriefing window shows up. Expand the results.
<br>![](/exercises/ex2/images/Ex02_Part03_77.png)

78. Click 'Details'.
<br>![](/exercises/ex2/images/Ex02_Part03_78.png)

79. You can see the failing records which are not valid drug names.
<br>![](/exercises/ex2/images/Ex02_Part03_79.png)

80. Expand the failed records window.
<br>![](/exercises/ex2/images/Ex02_Part03_80.png)

81. Click 'Failed Rows'.
<br>![](/exercises/ex2/images/Ex02_Part03_81.png)

82. You can see the details of the failed records for the selected rule.
<br>![](/exercises/ex2/images/Ex02_Part03_82.png)

83. Click 'Data Intelligence Metadata Explorer'. Click 'Home'.
<br>![](/exercises/ex2/images/Ex02_Part03_83.png)

84. You are back to the Data Intelligence Metadata Explorer home page.
<br>![](/exercises/ex2/images/Ex02_Part03_84.png)

You have now created rules and a rulebook that is evaluating the data quality of your enriched dataset.

## Data Remediation

After completing these steps you will have fixed data quality issues using the data remediation preparation.

1. Click 'View Preparations'.
<br>![](/exercises/ex2/images/Ex02_Part04_01.png)

2. Click 'Preparation for PHARMA_CLAIMS_ENRICHED_##.csv' (where ## is your user number).
<br>![](/exercises/ex2/images/Ex02_Part04_02.png)

3. Click the header for the column named 'DRUG_NAME'.
<br>![](/exercises/ex2/images/Ex02_Part04_03.png)

4. Click 'Replace'.
<br>![](/exercises/ex2/images/Ex02_Part04_04.png)

5. Type 'Nystatine' for the search string and type 'Nystatin' for the 'Replace by'.
<br>![](/exercises/ex2/images/Ex02_Part04_05.png)

6. Click 'Apply'.
<br>![](/exercises/ex2/images/Ex02_Part04_06.png)

7. The value 'Nystatine' was replaced by 'Nystatin'.
<br>![](/exercises/ex2/images/Ex02_Part04_07.png)

8. Click 'Replace'.
<br>![](/exercises/ex2/images/Ex02_Part04_08.png)

9. Type 'Acetaminofen' for the search string and type 'Acetaminophen' for the 'Replace by'.
<br>![](/exercises/ex2/images/Ex02_Part04_09.png)

10. Click 'Apply'.
<br>![](/exercises/ex2/images/Ex02_Part04_10.png)

11. The value 'Acetaminofen' was replaced by 'Acetaminophen'.
<br>![](/exercises/ex2/images/Ex02_Part04_11.png)

12. Click '<' to go back to the 'Rulebook Dataset Results'.
<br>![](/exercises/ex2/images/Ex02_Part04_12.png)

13. Click '<' to go back to the 'Run Preparation'.
<br>![](/exercises/ex2/images/Ex02_Part04_13.png)

14. Type 'REMEDIATED_DATA_##' for the 'Dataset Name' (where ## is your user number).
<br>![](/exercises/ex2/images/Ex02_Part04_14.png)

15. Click 'Apply'.
<br>![](/exercises/ex2/images/Ex02_Part04_15.png)

16. Click 'Data Intelligence Metadata Explorer'. Click 'Home'.
<br>![](/exercises/ex2/images/Ex02_Part04_16.png)

You fixed data quality issues using the data preparation recipe that was automatically generated with the execution of the rulebook.
In a normal process, the output dataset resulting of that data remediation process would be used in order to update the original table that contains the data quality issues using workflow and approovals.
For this hands-on, you can use the data preparation recipe you created to simulate the update process of the data and see the results in the rulebook.

17. Click 'View Preparations'.
<br>![](/exercises/ex2/images/Ex02_Part04_17.png)

18. Click 'DRUG_##' (where ## is your user number).
<br>![](/exercises/ex2/images/Ex02_Part04_18.png)

19. Click 'Recipe'.
<br>![](/exercises/ex2/images/Ex02_Part04_19.png)

20. Edit the 'Enrich' action.
<br>![](/exercises/ex2/images/Ex02_Part04_20.png)

21. Click '+' to add a new source.
<br>![](/exercises/ex2/images/Ex02_Part04_21.png)

22. Click 'Browse'.
<br>![](/exercises/ex2/images/Ex02_Part04_22.png)

23. Select the connection 'DI_DATA_LAKE'.
<br>![](/exercises/ex2/images/Ex02_Part04_23.png)

24. Click 'shared'.
<br>![](/exercises/ex2/images/Ex02_Part04_24.png)

25. Type 'TechEd_DAT163_##' in the 'Filter items' to search for your folder (where ## is your user number).
<br>![](/exercises/ex2/images/Ex02_Part04_25.png)

26. Click 'TechEd_DAT163_##' (where ## is your user number).
<br>![](/exercises/ex2/images/Ex02_Part04_26.png)

27. Click 'REMEDIATED_DATA_##' (where ## is your user number).
<br>![](/exercises/ex2/images/Ex02_Part04_27.png)

28. Click 'OK'.
<br>![](/exercises/ex2/images/Ex02_Part04_28.png)

29. The remediated dataset was added to the source.
<br>![](/exercises/ex2/images/Ex02_Part04_29.png)

30. Click 'X' to delete the join with the dataset 'D1'.
<br>![](/exercises/ex2/images/Ex02_Part04_30.png)

31. Drag and drop the 'REMEDIATED_DATA_##' datasource to the left side of 'P1' (where 3 is your user number).
<br>![](/exercises/ex2/images/Ex02_Part04_31.png)

32. Select 'Left Join'.
<br>![](/exercises/ex2/images/Ex02_Part04_32.png)

33. Scroll down and uncheck 'VALID_DRUG' and 'POTENCY' under the 'left source' list of columns.
<br>![](/exercises/ex2/images/Ex02_Part04_33.png)

34. Scroll down and uncheck 'ORIG_PRODUCT', 'DOSAGE', 'ROUTE_ADMINISTERED', and 'NOTES' from the right source list of columns.
<br>![](/exercises/ex2/images/Ex02_Part04_34.png)

35. Click 'Apply'.
<br>![](/exercises/ex2/images/Ex02_Part04_35.png)

36. Click 'Apply Enrichment'.
<br>![](/exercises/ex2/images/Ex02_Part04_36.png)

37. Click 'POTENCY_0'.
<br>![](/exercises/ex2/images/Ex02_Part04_37.png)

38. Click 'Rename'.
<br>![](/exercises/ex2/images/Ex02_Part04_38.png)

39. Type 'POTENCY' for the 'New Column Name'.
<br>![](/exercises/ex2/images/Ex02_Part04_39.png)

40. Click 'Apply'.
<br>![](/exercises/ex2/images/Ex02_Part04_40.png)

41. Click '<' to come back to the 'Run Preparation' menu.
<br>![](/exercises/ex2/images/Ex02_Part04_41.png)

42. You can now run your preparation to create a new curated dataset.
<br>![](/exercises/ex2/images/Ex02_Part04_42.png)

43. Type 'PHARMA_CLAIMS_CURATED_##' for the 'Dataset Name' (Where ## is your user number).
<br>![](/exercises/ex2/images/Ex02_Part04_43.png)

44. Click 'Apply'.
<br>![](/exercises/ex2/images/Ex02_Part04_44.png)

45. Click 'Data Intelligence Metadata Explorer'. Click 'Home'.
<br>![](/exercises/ex2/images/Ex02_Part04_45.png)

46. Click 'rulebooks'.
<br>![](/exercises/ex2/images/Ex02_Part04_46.png)

47. Type 'PHARMA_CLAIMS_##' in the 'Filter rulebook names' text field (where ## is your user number).
<br>![](/exercises/ex2/images/Ex02_Part04_47.png)

48. Click 'PHARMA_CLAIMS_##' (where ## is your user number).
<br>![](/exercises/ex2/images/Ex02_Part04_48.png)

49. Expand both 'Accuracy' and 'Completeness' set of rules.
<br>![](/exercises/ex2/images/Ex02_Part04_49.png)

50. Edit the rules binding associated to the first rule: 'DRUG_NAME_VALID_##' (where ## is your user number).
<br>![](/exercises/ex2/images/Ex02_Part04_50.png)

51. Delete the rule binding.
<br>![](/exercises/ex2/images/Ex02_Part04_51.png)

52. Click 'Save'.
<br>![](/exercises/ex2/images/Ex02_Part04_52.png)

53. Click 'Close'.
<br>![](/exercises/ex2/images/Ex02_Part04_53.png)

54. Expand 'Accuracy'.
<br>![](/exercises/ex2/images/Ex02_Part04_54.png)

55. Click 'Create Rule Binding'.
<br>![](/exercises/ex2/images/Ex02_Part04_55.png)

56. Click 'Step 2'.
<br>![](/exercises/ex2/images/Ex02_Part04_56.png)

57. Click 'Browse'.
<br>![](/exercises/ex2/images/Ex02_Part04_57.png)

58. Select 'DI_DATA_LAKE' for the 'Connection'.
<br>![](/exercises/ex2/images/Ex02_Part04_58.png)

59. Click 'shared'.
<br>![](/exercises/ex2/images/Ex02_Part04_59.png)

60. Filter 'TechEd_DAT163_##' and select your folder (where ## is your user number).
<br>![](/exercises/ex2/images/Ex02_Part04_60.png)

61. Select 'PHARMA_CLAIMS_CURATED_##' (where ## is your user number). Then click 'Step 3'.
<br>![](/exercises/ex2/images/Ex02_Part04_61.png)

62. Select 'VALID_DRUG' for the mapping. Then click 'Create Binding'.
<br>![](/exercises/ex2/images/Ex02_Part04_62.png)

63. Click 'Close'.
<br>![](/exercises/ex2/images/Ex02_Part04_63.png)

64. Expand 'Completeness', then edit the rule binding.
<br>![](/exercises/ex2/images/Ex02_Part04_64.png)

65. Delete the column mapping for 'DRUG_NAME'. Then click 'Save'.
<br>![](/exercises/ex2/images/Ex02_Part04_65.png)

66. Click 'Close'.
<br>![](/exercises/ex2/images/Ex02_Part04_66.png)

67. Expand 'Completeness', then click 'Create Rule Binding'.
<br>![](/exercises/ex2/images/Ex02_Part04_67.png)

68. Click 'Step 2'.
<br>![](/exercises/ex2/images/Ex02_Part04_68.png)

69. Select the existing 'Connection ID' for 'PHARMA_CLAIMS_CURATED_##', then click 'Step 3' (where ## is your user number).
<br>![](/exercises/ex2/images/Ex02_Part04_69.png)

70. Click 'Create Binding'.
<br>![](/exercises/ex2/images/Ex02_Part04_70.png)

71. Click 'Close'.
<br>![](/exercises/ex2/images/Ex02_Part04_71.png)

72. Click 'Run All'.
<br>![](/exercises/ex2/images/Ex02_Part04_72.png)

73. Click 'Run'.
<br>![](/exercises/ex2/images/Ex02_Part04_73.png)

74. Wait for the rulebook execution to finish.
<br>![](/exercises/ex2/images/Ex02_Part04_74.png)

75. You can check the execution completion status with the notification.
<br>![](/exercises/ex2/images/Ex02_Part04_75.png)

76. Click 'View Results'.
<br>![](/exercises/ex2/images/Ex02_Part04_76.png)

77. Click 'Yes'.
<br>![](/exercises/ex2/images/Ex02_Part04_77.png)

78. Expand the dataset.
<br>![](/exercises/ex2/images/Ex02_Part04_78.png)

79. The quality of the data improved.
<br>![](/exercises/ex2/images/Ex02_Part04_79.png)

80. Click 'Data Intelligence Metadata Explorer'. Click 'Home'.
<br>![](/exercises/ex2/images/Ex02_Part04_80.png)

81. You are back to the home page of the Metadata Explorer.
<br>![](/exercises/ex2/images/Ex02_Part04_81.png)

You have now fixed data quality issues using the data remediation preparation.

## Conclusion

In this hands-on you:
* Accessed and discovered several data repositories (Database, Cloud Data Lake, Local File System)
* Profiled and published dataset to the catalog
* Found data quality issues
* Created your own enriched dataset
* Created a glossary and terms and associated them with your data
* Assessed the quality of a dataset using rules and a rulebook
* Improved the data with data remediation and witness the results

For more information about SAP Data Intelligence, you can have a look at the following ressources:
* Product Home Page: https://www.sap.com/products/data-intelligence/features.html
* Help Portal: https://help.sap.com/viewer/product/SAP_DATA_INTELLIGENCE/Cloud/en-US

Thanks!
