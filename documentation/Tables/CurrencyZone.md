#### 



# ![Tables](../../../Images/Table32.png) [dbo].[CurrencyZone]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |
| Row Count (~) | 0 |
| Created | 14:03:18 25 June 2015 |
| Last Modified | 14:03:18 25 June 2015 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Allow Nulls | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_CurrencyZone_ID: ID](../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NO | 1 - 1 |
|  | CurrencyZoneName | nvarchar(20) | 40 | YES |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_CurrencyZone_ID: ID](../../../Images/pkcluster.png)](#indexes) | PK_CurrencyZone_ID | ID | YES |


---

## <a name="#extendedproperties"></a>Extended Properties

| Name | Level 2 Type | Level 2 Name | Value |
|---|---|---|---|
| sys_information_type_id | COLUMN | CurrencyZoneName | C44193E1-0E58-4B2A-9001-F7D6E7BC1373 |
| sys_information_type_name | COLUMN | CurrencyZoneName | Financial |
| sys_sensitivity_label_id | COLUMN | CurrencyZoneName | 1866ca45-1973-4c28-9d12-04d407f147ad |
| sys_sensitivity_label_name | COLUMN | CurrencyZoneName | Public |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[CurrencyZone]
(
[ID] [int] NOT NULL IDENTITY(1, 1),
[CurrencyZoneName] [nvarchar] (20) COLLATE Latin1_General_CI_AS NULL
) ON [PRIMARY]
GO
ALTER TABLE [dbo].[CurrencyZone] ADD CONSTRAINT [PK_CurrencyZone_ID] PRIMARY KEY CLUSTERED  ([ID]) ON [PRIMARY]
GO
EXEC sp_addextendedproperty N'sys_information_type_id', N'C44193E1-0E58-4B2A-9001-F7D6E7BC1373', 'SCHEMA', N'dbo', 'TABLE', N'CurrencyZone', 'COLUMN', N'CurrencyZoneName'
GO
EXEC sp_addextendedproperty N'sys_information_type_name', N'Financial', 'SCHEMA', N'dbo', 'TABLE', N'CurrencyZone', 'COLUMN', N'CurrencyZoneName'
GO
EXEC sp_addextendedproperty N'sys_sensitivity_label_id', N'1866ca45-1973-4c28-9d12-04d407f147ad', 'SCHEMA', N'dbo', 'TABLE', N'CurrencyZone', 'COLUMN', N'CurrencyZoneName'
GO
EXEC sp_addextendedproperty N'sys_sensitivity_label_name', N'Public', 'SCHEMA', N'dbo', 'TABLE', N'CurrencyZone', 'COLUMN', N'CurrencyZoneName'
GO

```


---

## <a name="#usedby"></a>Used By

* [[dbo].[v_Geographies]](../Views/v_Geographies.md)


---

###### Author:  Richard Macaskill

###### Copyright 2018 - All Rights Reserved

###### Created: 03 October 2018 15:24:06

