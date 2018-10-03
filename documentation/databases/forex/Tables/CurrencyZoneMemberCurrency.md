#### 



# ![Tables](../../../Images/Table32.png) [dbo].[CurrencyZoneMemberCurrency]

---

## <a name="#description"></a>MS_Description

Maps CurrencyZone to Currency. A Currency (e.g. GRD) can be a member of one or more Currency Zones (e.g. EuroZone). Note that Currency Zones are used for risk management and compliance exposure limits as well as being legal definitions.

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |
| Row Count (~) | 0 |
| Created | 14:03:18 25 June 2015 |
| Last Modified | 14:03:18 25 June 2015 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Allow Nulls |
|---|---|---|---|---|
| [![Cluster Primary Key PK_CurrencyZoneMemberCurrency_CMP: ISO\CurrencyZoneID](../../../Images/pkcluster.png)](#indexes) | ISO | nchar(3) | 6 | NO |
| [![Cluster Primary Key PK_CurrencyZoneMemberCurrency_CMP: ISO\CurrencyZoneID](../../../Images/pkcluster.png)](#indexes) | CurrencyZoneID | int | 4 | NO |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_CurrencyZoneMemberCurrency_CMP: ISO\CurrencyZoneID](../../../Images/pkcluster.png)](#indexes) | PK_CurrencyZoneMemberCurrency_CMP | ISO, CurrencyZoneID | YES |


---

## <a name="#extendedproperties"></a>Extended Properties

| Name | Level 2 Type | Level 2 Name | Value |
|---|---|---|---|
| sys_information_type_id | COLUMN | CurrencyZoneID | C44193E1-0E58-4B2A-9001-F7D6E7BC1373 |
| sys_information_type_name | COLUMN | CurrencyZoneID | Financial |
| sys_sensitivity_label_id | COLUMN | CurrencyZoneID | 1866ca45-1973-4c28-9d12-04d407f147ad |
| sys_sensitivity_label_name | COLUMN | CurrencyZoneID | Public |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[CurrencyZoneMemberCurrency]
(
[ISO] [nchar] (3) COLLATE Latin1_General_CI_AS NOT NULL,
[CurrencyZoneID] [int] NOT NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[CurrencyZoneMemberCurrency] ADD CONSTRAINT [PK_CurrencyZoneMemberCurrency_CMP] PRIMARY KEY CLUSTERED  ([ISO], [CurrencyZoneID]) ON [PRIMARY]
GO
EXEC sp_addextendedproperty N'MS_Description', N'Maps CurrencyZone to Currency. A Currency (e.g. GRD) can be a member of one or more Currency Zones (e.g. EuroZone). Note that Currency Zones are used for risk management and compliance exposure limits as well as being legal definitions.', 'SCHEMA', N'dbo', 'TABLE', N'CurrencyZoneMemberCurrency', NULL, NULL
GO
EXEC sp_addextendedproperty N'sys_information_type_id', N'C44193E1-0E58-4B2A-9001-F7D6E7BC1373', 'SCHEMA', N'dbo', 'TABLE', N'CurrencyZoneMemberCurrency', 'COLUMN', N'CurrencyZoneID'
GO
EXEC sp_addextendedproperty N'sys_information_type_name', N'Financial', 'SCHEMA', N'dbo', 'TABLE', N'CurrencyZoneMemberCurrency', 'COLUMN', N'CurrencyZoneID'
GO
EXEC sp_addextendedproperty N'sys_sensitivity_label_id', N'1866ca45-1973-4c28-9d12-04d407f147ad', 'SCHEMA', N'dbo', 'TABLE', N'CurrencyZoneMemberCurrency', 'COLUMN', N'CurrencyZoneID'
GO
EXEC sp_addextendedproperty N'sys_sensitivity_label_name', N'Public', 'SCHEMA', N'dbo', 'TABLE', N'CurrencyZoneMemberCurrency', 'COLUMN', N'CurrencyZoneID'
GO

```


---

## <a name="#usedby"></a>Used By

* [[dbo].[v_Geographies]](../Views/v_Geographies.md)


---

###### Author:  Richard Macaskill

###### Copyright 2018 - All Rights Reserved

###### Created: 03 October 2018 15:24:06

