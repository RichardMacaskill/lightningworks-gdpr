#### 



# ![Views](../../../Images/View32.png) [dbo].[v_Exrates_Currency]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 14:50:16 24 November 2015 |
| Last Modified | 15:22:09 24 November 2015 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| ID | int | 4 |
| ISO | nchar(3) | 6 |
| TenorId | int | 4 |
| OutrightRate | decimal(22,10) | 13 |
| AsOfDateTime | datetime | 8 |
| ValidFrom | datetime | 8 |
| ValidTo | datetime | 8 |
| CountryId | int | 4 |
| StandardPrecision | int | 4 |
| HasSubUnits | bit | 1 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[v_Exrates_Currency]
AS

SELECT er.ID
    ,  er.ISO
    ,  er.TenorId
    ,  er.OutrightRate
    ,  er.AsOfDateTime
        ,  er.ValidFrom
    ,  er.ValidTo
        ,  c.CountryId
    ,  c.StandardPrecision
    ,  c.HasSubUnits FROM dbo.ExchangeRate AS er INNER JOIN dbo.Currency AS c ON c.ISO = er.ISO
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Currency]](../Tables/Currency.md)
* [[dbo].[ExchangeRate]](../Tables/ExchangeRate.md)


---

###### Author:  Richard Macaskill

###### Copyright 2018 - All Rights Reserved

###### Created: 03 October 2018 15:24:06

