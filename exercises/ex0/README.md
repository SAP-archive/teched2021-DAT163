# Product Overview

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

With SAP Data Intelligence, you can explore your data assets, create and validate your models, and orchestrate any mix of data processing engines, seamlessly within the data pipelines that feed them.

SAP Data Intelligence Machine Learning Manager seamlessly accelerate machine learning models deployment and operation. This is a one single interface that allows you to see and orchestrate all data-driven applications and data flows across the organization with tools to help manage governance, auditability, and transparency.

<br>![](/exercises/ex0/images/Ex00_DataIntelligence_03.png)

It comes with an interactive development environment to work with notebooks, code, and data including text editors, terminals, data file viewers, and other custom components side by side with notebooks in a tabbed work area.

You can harness the usage of Jupyter notebooks in data-driven applications by benefitting from the seamless integration of the JupyterLab environment and the pipeline modeler application.

### Data Cataloging

SAP Data Intelligence enables a unified data catalog to easily discover, organize, and curate your data.

<br>![](/exercises/ex0/images/Ex00_DataIntelligence_04.png)

SAP Data Intelligence Metadata Explorer enables to:
* Discover data (crawl, profile, organize, link, and enrich) and make data accessible (browse, search)
* Classify and organize data (ML-driven auto-tag) and understand it (location, attributes, quality, lineage, sensitivity)
* Enforce centralized authorization and security for data orchestration, and control data quality standards

## SAP Data Intelligence Metadata Explorer - Main Capabilities

SAP Data Intelligence three main capabilities are:
* Data Governance and Discovery
* Data Quality Monitoring
* Data Preparation and Enrichment

### Data Governance and Discovery

Easily connect and browse data repository by searching and filtering across auto-discovered data assets.

<br>![](/exercises/ex0/images/Ex00_DataIntelligence_05.png)

Link data to information-rich business terms with common properties and definitions, leverage custom attributes to extend business terms and add value, define, maintain and explore relationships of terms and technical artifacts.

<br>![](/exercises/ex0/images/Ex00_DataIntelligence_06.png)

Profile data and get insights via the 'Fact Sheet' with overview from columns, metadata, lineage and reviews. 

<br>![](/exercises/ex0/images/Ex00_DataIntelligence_07.png)

### Data Quality Monitoring

Easily create, update, and manage data quality rules.

Rules support one or more parameters and one or more conditions for each parameter. The parameter might be the name of a frequently used column in your dataset. A condition you set shows the criteria of what might cause the record to pass or fail.

You can also specify logical expressions for your conditions.
After the rule is created, you can test the rule with some sample data to see if the results meet your expectations.

<br>![](/exercises/ex0/images/Ex00_DataIntelligence_08.png)

Visualize data quality in easy-to-consume rulebooks and dashboards

Rulebooks contain a group of rules. Rather than running a single rule, you run a rulebook that can contain many rules. These rules can come from one or more rule categories, and the rules may be bound to one or more datasets.

Grouping the rules into a rulebook helps to gain an understanding of the individual rules that have passed or failed within a larger context.

<br>![](/exercises/ex0/images/Ex00_DataIntelligence_09.png)

Create a dashboard with custom tiles showing the results of the datasets, categories, and rulebooks that matter to you. You can have several dashboards, and you can have groups within the dashboard, which helps you organize your scorecards in a way that makes sense to you.

### Data Preparation and Enrichment

Discover, prepare and cleanse, and share data with a visual, interactive interface intended for less complex tasks.

Business users and data scientists can access, transform, and enrich datasets using a spreadsheet-like user interface in Metadata Explorer.

Use data preparation to find data quality issues, correct and standardize data, and then output the data for analysis. This process improves efficiency and gains better business insights.

<br>![](/exercises/ex0/images/Ex00_DataIntelligence_10.png)

Use the Data Preparation user interface to view a set of data and create a recipe of actions to shape the data. After processing the preparation, the transformed data is output into a target data set that other downstream applications can use.

## Summary

Now that you have learned about SAP Data Intelligence and Metadata Explorer. 
Continue to - [Hands-on - Part 1](../ex1/README.md)
