#### 



# ![Database Roles](../../../../../Images/Role_Database32.png) db_datareader

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Owner | dbo |


---

## <a name="#members"></a>Members

* [RatesService](RatesService.md)


---

## <a name="#sqlscript"></a>SQL Script

```sql
EXEC sp_addrolemember N'db_datareader', N'RatesService'
GO

```


---

## <a name="#uses"></a>Uses

* [RatesService](RatesService.md)


---

###### Author:  Richard Macaskill

###### Copyright 2018 - All Rights Reserved

###### Created: 03 October 2018 15:24:06

