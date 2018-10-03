#### 



# ![Users](../../../../Images/User32.png) RED-GATE\\Product Managers

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Type | WindowsUser |
| Login Name | RED-GATE\\Product Managers |


---

## <a name="#databaselevelpermissions"></a>Database Level Permissions

| Type | Action |
|---|---|
| CONNECT | Grant |


---

## <a name="#sqlscript"></a>SQL Script

```sql
IF NOT EXISTS (SELECT * FROM master.dbo.syslogins WHERE loginname = N'RED-GATE\\Product Managers')
CREATE LOGIN [RED-GATE\\Product Managers] FROM WINDOWS
GO
CREATE USER [RED-GATE\\Product Managers] FOR LOGIN [RED-GATE\\Product Managers]
GO

```


---

## <a name="#usedby"></a>Used By

* [GetLatestRate](../Roles/Database_Roles/GetLatestRate.md)


---

###### Author:  Richard Macaskill

###### Copyright 2018 - All Rights Reserved

###### Created: 03 October 2018 15:24:06

