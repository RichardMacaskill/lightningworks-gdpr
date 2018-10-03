#### 



# ![Views](../../../Images/View32.png) [dbo].[myView]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 11:08:10 01 December 2015 |
| Last Modified | 15:56:21 05 February 2016 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Identity |
|---|---|---|---|
| ID | int | 4 | 0 - 0 |
| Name | nvarchar(10) | 20 |  |
| AssumedDays | int | 4 |  |


---

## <a name="#sqlscript"></a>SQL Script

```sql

CREATE VIEW [dbo].[myView] AS 
SELECT * FROM dbo.Tenor;

GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Tenor]](../Tables/Tenor.md)


---

###### Author:  Richard Macaskill

###### Copyright 2018 - All Rights Reserved

###### Created: 03 October 2018 15:24:06

