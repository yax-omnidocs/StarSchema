## What is Normalization?

Normalization is a database design technique that reduces data redundancy and eliminates undesirable characteristics like Insertion, Update and Deletion Anomalies.

Normalization will divide a wide table into smaller tables and link them using relationships.

## Database Normal Forms

There are many normal forms existing in relational database, such as

- 1NF
- 2NF
- 3NF
- BCNF
- ...
- 6NF

In most practical applications, normalization achieves its best in 3NF.

> Database Normalization with an example </br>
> |Name|ZIPCode|Item|
> |-----|-----|----|
> |Lidl|2100|Tofu,Milk|
> |Netto|2300|Pizza,Chili|
> |Netto|2450|Mushroom|

## 1NF Rules

In the above example, `Item` column having multiple values breaks the 1NF rule, of which essence are

- Each table cell should contain a single value
- Each record (row) needs to be unique

According to 1NF rules, the table would be like

> |Name|ZIPCode|Item|
> |-----|-----|----|
> |Lidl|2100|Tofu|
> |Lidl|2100|Milk|
> |Netto|2300|Pizza|
> |Netto|2300|Chili|
> |Netto|2450|Mushroom|