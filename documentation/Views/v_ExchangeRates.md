#### 



# ![Views](../../../Images/View32.png) [dbo].[v_ExchangeRates]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 14:28:26 07 October 2015 |
| Last Modified | 14:28:26 07 October 2015 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| ISO | nchar(3) | 6 |
| Name | nvarchar(10) | 20 |
| OutrightRate | decimal(22,10) | 13 |
| AsOfDateTime | datetime | 8 |
| SettlementDate | datetime | 8 |
| ValidFrom | datetime | 8 |
| ValidTo | datetime | 8 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[v_ExchangeRates]
as

SELECT
   er.ISO
,   t.Name
,   er.OutrightRate
,   er.AsOfDateTime
,   er.SettlementDate
,   er.ValidFrom
,   er.ValidTo
FROM
    dbo.ExchangeRate AS er
INNER JOIN dbo.Currency AS c
    ON c.ISO = er.ISO
INNER JOIN dbo.Tenor AS t
    ON t.ID = er.TenorId;


	
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Currency]](../Tables/Currency.md)
* [[dbo].[ExchangeRate]](../Tables/ExchangeRate.md)
* [[dbo].[Tenor]](../Tables/Tenor.md)


---

###### Author:  Richard Macaskill

###### Copyright 2018 - All Rights Reserved

###### Created: 03 October 2018 15:24:06

