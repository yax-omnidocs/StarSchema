# Chap.1 - Analytic Databases and Dimensional Design

The techniques for the design of analytics databases unleash business analytics in a very simple way: **they model the measurement of business processes**

## Dimensional Design

**Core**: A set of business metrics that captures how a process is evaluated, and a description of the context of every measurement.

**Purpose**: Different from an operational system that supports the *execution* of a business process, an analytic system supports the evaluation of the process

> An operational system directly supports the execution of a business process. By capturing details about significant events or transactions, it constructs a record of activities. (Row population). 
> 
> The activities recorded by these systems are sometimes known as transactions,e.g., </br>
> - [orders,shipments,returns] in a sales system, </br>
> - [assets, liabilities, equities] in a accounting system. </br>
>
> The systems themselves are sometimes called online transaction process (OLTP) systems, or transaction systems for short.

**Operational system vs. Analytic system**:

| | Operational System | Analytic System |
| --- | ------ | --------|
|**Purpose**|Execution of a business process| Measurement of a  business process|
|**Primary  Interaction Style**| Insert, Update,  Query, Delete| Query|
|**Scope of  Interaction**| Individual  transaction| Aggregated transactions|
|**Query Patterns**| Predictable  and stable | Unpredictable  and changing|
|**Temporal Focus**| Current | Current and historic|
|**Design Optimization**| Update concurrency| High-performance query|
|**Design Principe**| Entity-relationship (ER) design </br> in third normal form (3NF)| Dimensional design </br> (Star Schema or Cube)|
|**Alias**| Transaction System </br> Online Transaction Processing </br> System (OLTP) </br> Source System | Data Warehouse System </br> Data Mart| 

**Measurement and Context**:These two concepts are the foundation of dimensional design. Every dimensional solution describes a process by capturing what is measured and the context in which the measurements are evaluated.