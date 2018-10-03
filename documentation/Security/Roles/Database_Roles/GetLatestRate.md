#### 



# ![Database Roles](../../../../../Images/Role_Database32.png) GetLatestRate

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Owner | dbo |


---

## <a name="#members"></a>Members

* [GetLatestRatesUser](../../Users/GetLatestRatesUser.md)
* [RatesServiceUser](../../Users/RatesServiceUser.md)
* [RED-GATE\\Product Managers](../../Users/RED-GATE_Product_Managers.md)


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE ROLE [GetLatestRate]
AUTHORIZATION [dbo]
GO
EXEC sp_addrolemember N'GetLatestRate', N'GetLatestRatesUser'
GO
EXEC sp_addrolemember N'GetLatestRate', N'RatesServiceUser'
GO
EXEC sp_addrolemember N'GetLatestRate', N'RED-GATE\\Product Managers'
GO

```


---

## <a name="#uses"></a>Uses

* [GetLatestRatesUser](../../Users/GetLatestRatesUser.md)
* [RatesServiceUser](../../Users/RatesServiceUser.md)
* [RED-GATE\\Product Managers](../../Users/RED-GATE_Product_Managers.md)


---

###### Author:  Richard Macaskill

###### Copyright 2018 - All Rights Reserved

###### Created: 03 October 2018 15:24:06

