# Introduction

In this part, you will learn about the main capabilities in SAP Data Intelligence Metadata Explorer, then you will get a preview about the dataset used in the hands-on.

## SAP Data Intelligence - Overview

SAP Data Intelligence allows to connect, discover, enrich, and orchestrate disjointed data assets into actionable business insights at enterprise scale.

It's core capabilities are:
* Data Integration
* Data Processing
* Data Cataloging

<br>![](/exercises/ex0/images/Ex00_DataIntelligence_01.png)

### Data Integration

With SAP Data Intelligence, you can integrate any kind of data (structured, unstructured or streaming), with any pattern (real-time, near-real-time, batch), enrich it, refine it and feed process it.

SAP Data Intelligence Modeler is a flow-based application that allows to build powerful pipelines using drag-and-drop operators.
There are over 250 operators (data integration, connectivity, processing, data quality, ML ...) that allows to combine and switch between integration styles (streaming, batch, replication, virtualization, migration, ...).

<br>![](/exercises/ex0/images/Ex00_DataIntelligence_02.png)

The operators are extensible and the application supports custom and partner operators.

The data pipelines also support data workflows for cross-system orchestration (trigger execution of SAP BW Process chains, execute remote SAP Data Services jobs, submit Spark jobs to Hadoop clusters, ...).

SAP Data Intelligence modeler enables to create complex, multistep, reusable data pipelines and operators.

### Data Processing



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
