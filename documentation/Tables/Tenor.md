#### 



# ![Tables](../../../Images/Table32.png) [dbo].[Tenor]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |
| Row Count (~) | 5 |
| Created | 16:47:21 21 May 2015 |
| Last Modified | 14:32:02 30 March 2017 |


---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Max Length (Bytes) | Allow Nulls | Identity |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_Tenor_ID: ID](../../../Images/pkcluster.png)](#indexes) | ID | int | 4 | NO | 1 - 1 |
|  | Name | nvarchar(10) | 20 | YES |  |
|  | AssumedDays | int | 4 | NO |  |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_Tenor_ID: ID](../../../Images/pkcluster.png)](#indexes) | PK_Tenor_ID | ID | YES |


---

## <a name="#triggers"></a>Triggers

| Name | ANSI Nulls On | Quoted Identifier On | On | Description |
|---|---|---|---|---|
| tr_TenorInsert | YES | YES | After Insert | _[Audit Critical]_ |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE TABLE [dbo].[Tenor]
(
[ID] [int] NOT NULL IDENTITY(1, 1),
[Name] [nvarchar] (10) COLLATE Latin1_General_CI_AS NULL,
[AssumedDays] [int] NOT NULL
) ON [PRIMARY]
GO
CREATE TRIGGER [dbo].[tr_TenorInsert] ON [dbo].[Tenor] FOR INSERT
AS
BEGIN
	PRINT 'you inserted something';
END
GO
ALTER TABLE [dbo].[Tenor] ADD CONSTRAINT [PK_Tenor_ID] PRIMARY KEY CLUSTERED  ([ID]) ON [PRIMARY]
GO
EXEC sp_addextendedproperty N'MS_Description', N'[Audit Critical]', 'SCHEMA', N'dbo', 'TABLE', N'Tenor', 'TRIGGER', N'tr_TenorInsert'
GO

```


---

## <a name="#usedby"></a>Used By

* [[dbo].[ExchangeRate]](ExchangeRate.md)
* [[dbo].[myView]](../Views/myView.md)
* [[dbo].[v_ExchangeRates]](../Views/v_ExchangeRates.md)
* [[dbo].[ExchangeRates_ListAll]](../Programmability/Stored_Procedures/ExchangeRates_ListAll.md)
* [[dbo].[LatestSpotRate_GetByISO]](../Programmability/Stored_Procedures/LatestSpotRate_GetByISO.md)


---

###### Author:  Richard Macaskill

###### Copyright 2018 - All Rights Reserved

###### Created: 03 October 2018 15:24:06

