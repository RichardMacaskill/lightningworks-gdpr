#### 



# ![Stored Procedures](../../../../Images/StoredProcedure32.png) [dbo].[ExchangeRates_ListAll]

---

## <a name="#description"></a>MS_Description

Lists values for exchange rats

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE PROCEDURE [dbo].[ExchangeRates_ListAll]
AS
SET NOCOUNT ON
BEGIN
SELECT  er.ID ,
        er.ISO ,
        er.TenorId ,
        er.OutrightRate ,
        er.AsOfDateTime ,
        er.SettlementDate ,
        er.ValidFrom ,
        er.ValidTo ,
        t.ID ,
        t.Name ,
        t.AssumedDays ,
        c.ISO ,
        c.CountryId ,
        c.StandardPrecision ,
        c.HasSubUnits
FROM    dbo.ExchangeRate AS er
        INNER JOIN dbo.Tenor AS t ON t.ID = er.TenorId
        INNER JOIN dbo.Currency AS c ON c.ISO = er.ISO;
END	



GO
EXEC sp_addextendedproperty N'MS_Description', N'Lists values for exchange rats', 'SCHEMA', N'dbo', 'PROCEDURE', N'ExchangeRates_ListAll', NULL, NULL
GO

```


---

## <a name="#uses"></a>Uses

* [[dbo].[Currency]](../../Tables/Currency.md)
* [[dbo].[ExchangeRate]](../../Tables/ExchangeRate.md)
* [[dbo].[Tenor]](../../Tables/Tenor.md)


---

###### Author:  Richard Macaskill

###### Copyright 2018 - All Rights Reserved

###### Created: 03 October 2018 15:24:06

