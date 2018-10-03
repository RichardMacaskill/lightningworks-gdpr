#### 



# ![Users](../../../../Images/User32.png) RatesServiceUser

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Type | WindowsUser |
| Login Name | TESTNET\\RatesServiceUser |
| Default Schema | dbo |


---

## <a name="#databaselevelpermissions"></a>Database Level Permissions

| Type | Action |
|---|---|
| CONNECT | Grant |


---

## <a name="#sqlscript"></a>SQL Script

```sql
IF NOT EXISTS (SELECT * FROM master.dbo.syslogins WHERE loginname = N'TESTNET\\RatesServiceUser')
CREATE LOGIN [TESTNET\\RatesServiceUser] FROM WINDOWS
GO
CREATE USER [RatesServiceUser] FOR LOGIN [TESTNET\\RatesServiceUser]
GO

```


---

## <a name="#usedby"></a>Used By

* [GetLatestRate](../Roles/Database_Roles/GetLatestRate.md)


---

###### Author:  Richard Macaskill

###### Copyright 2018 - All Rights Reserved

###### Created: 03 October 2018 15:24:06

