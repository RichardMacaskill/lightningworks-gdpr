#### 



# ![Table-valued Functions](../../../../../Images/Function_Table32.png) [dbo].[SplitToTable]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| ANSI Nulls On | YES |
| Quoted Identifier On | YES |


---

## <a name="#parameters"></a>Parameters

| Name | Data Type | Max Length (Bytes) |
|---|---|---|
| @Delimiter | char | 1 |
| @CSV | nvarchar(4000) | 8000 |


---

## <a name="#sqlscript"></a>SQL Script

```sql
CREATE FUNCTION [dbo].[SplitToTable] (@Delimiter char(1), @CSV nvarchar(4000))
RETURNS table
AS
RETURN (
    WITH Pieces(pn, start, stop) AS (
        SELECT 1, 1, CHARINDEX(@Delimiter, @CSV)
        UNION ALL
        SELECT pn + 1, stop + 1, CHARINDEX(@Delimiter, @CSV, stop + 1)
        FROM Pieces
        WHERE stop > 0
    )
    SELECT
        pn as PartNumber,
        SUBSTRING(@CSV, start, CASE WHEN stop > 0 THEN stop-start ELSE 512 END) AS Part
        FROM Pieces
) 
GO

```


---

###### Author:  Richard Macaskill

###### Copyright 2018 - All Rights Reserved

###### Created: 03 October 2018 15:24:06

