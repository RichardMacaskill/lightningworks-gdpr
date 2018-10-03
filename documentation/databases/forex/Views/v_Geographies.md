#### 



# ![Views](../../../Images/View32.png) [dbo].[v_Geographies]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |
| Created | 09:10:23 23 November 2015 |
| Last Modified | 09:10:23 23 November 2015 |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| ID | int | 4 |
| CurrencyZoneName | nvarchar(20) | 40 |
| ISO | nchar(3) | 6 |
| CurrencyZoneID | int | 4 |
| CountryId | int | 4 |
| StandardPrecision | int | 4 |
| HasSubUnits | bit | 1 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE VIEW [dbo].[v_Geographies] AS
SELECT cz.ID
    ,  cz.CurrencyZoneName
    ,  czmc.ISO
    ,  czmc.CurrencyZoneID
    ,  c.CountryId
    ,  c.StandardPrecision
    ,  c.HasSubUnits FROM dbo.CurrencyZone AS cz
INNER JOIN dbo.CurrencyZoneMemberCurrency AS czmc 
ON czmc.CurrencyZoneID	=	cz.ID
INNER JOIN dbo.Currency AS c
ON	czmc.ISO	=	c.ISO
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Currency]](../Tables/Currency.md)
* [[dbo].[CurrencyZone]](../Tables/CurrencyZone.md)
* [[dbo].[CurrencyZoneMemberCurrency]](../Tables/CurrencyZoneMemberCurrency.md)


---

###### Author:  Richard Macaskill

###### Copyright 2018 - All Rights Reserved

###### Created: 03 October 2018 15:24:06

