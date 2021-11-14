# Introduction

In this part, you will learn about the main capabilities in SAP Data Intelligence Metadata Explorer, then you will get a preview about the dataset used in the hands-on.

## SAP Data Intelligence

SAP Data Intelligence allows to connect, discover, enrich, and orchestrate disjointed data assets into actionable business insights at enterprise scale.

It's core capabilities are:
* Data Integration
* Data Processing
* Data Cataloging

<br>![](/exercises/ex0/images/Ex00_DataIntelligence_01.png)

1.	Click here.
<br>![](/exercises/ex0/images/00_00_0010.png)

2.	Insert this code.
``` abap
 DATA(params) = request->get_form_fields(  ).
 READ TABLE params REFERENCE INTO DATA(param) WITH KEY name = 'cmd'.
  IF sy-subrc <> 0.
    response->set_status( i_code = 400
                     i_reason = 'Bad request').
    RETURN.
  ENDIF.
```

## SAP Data Intelligence Metadata Explorer

## Hands-on

## Summary

Now that you have ... 
Continue to - [Exercise 1 - Exercise 1 Description](../ex1/README.md)
