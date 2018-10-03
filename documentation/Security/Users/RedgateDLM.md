#### 



# ![Users](../../../../Images/User32.png) RedgateDLM

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Type | SqlUser |
| Login Name | RedgateDLM |
| Default Schema | dbo |


---

## <a name="#databaselevelpermissions"></a>Database Level Permissions

| Type | Action |
|---|---|
| CONNECT | Grant |


---

## <a name="#sqlscript"></a>SQL Script

```sql
IF NOT EXISTS (SELECT * FROM master.dbo.syslogins WHERE loginname = N'RedgateDLM')
CREATE LOGIN [RedgateDLM] WITH PASSWORD = 'p@ssw0rd'
GO
CREATE USER [RedgateDLM] FOR LOGIN [RedgateDLM]
GO

```


---

## <a name="#usedby"></a>Used By

* [RatesService](../Roles/Database_Roles/RatesService.md)


---

###### Author:  Richard Macaskill

###### Copyright 2018 - All Rights Reserved

###### Created: 03 October 2018 15:24:06

