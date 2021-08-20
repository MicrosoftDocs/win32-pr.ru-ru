---
description: В следующей таблице перечислены сопоставления типов данных Variant и типов данных OLE DB.
ms.assetid: 213458bf-b847-4ced-8a92-686b4eee6d07
title: Сопоставление типов данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e25e909755c87b15526b97488285a0cf688e15dab64073fad603efc190f382b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118462598"
---
# <a name="data-type-mappings"></a>Сопоставление типов данных

В следующей таблице перечислены сопоставления типов данных Variant и типов данных OLE DB.




| Тип данных Variant | Тип данных OLE DB |
|-------------------|------------------|
| Логическое значение VT \_          | DBTYPE \_ bool     |
| VT \_ BSTR          | DBTYPE \_ BSTR     |
| VT \_ ByRef         | DBTYPE \_ ByRef    |
| VT \_ CY            | DBTYPE \_ CY       |
| \_Дата VT          | DBTYPE, \_ Дата     |
| VT \_ Decimal       | Тип DBTYPE \_ Decimal  |
| VT \_ пуст         | DBTYPE \_ Empty    |
| VT \_ fileTime      | DBTYPE \_ fileTime |
| \_идентификатор GUID VT          | DBTYPE, \_ идентификатор GUID     |
| VT \_ I1            | DBTYPE \_ I1       |
| VT \_ I2            | DBTYPE \_ I2       |
| VT \_ I4            | DBTYPE \_ I4       |
| VT \_ i8            | DBTYPE \_ i8       |
| VT \_ null          | DBTYPE \_ null     |
| VT \_ R4            | DBTYPE \_ R4       |
| VT \_ R8            | DBTYPE \_ UI8      |
| \_вектор VT        | DBTYPE \_ Vector   |
| VT \_ встр          | DBTYPE \_ встр     |



 

В следующей таблице перечислены сопоставления между типами данных XML и типами данных OLE DB.



| Тип данных Variant | Тип данных OLE DB |
|-------------------|------------------|
| Ячейки. ФОРМАТЕ        | DBTYPE \_ байт    |
| Ячейки. HEX           | DBTYPE \_ i8       |
| BOOLEAN           | DBTYPE \_ bool     |
| CHAR              | DBTYPE \_ str      |
| DATE              | DBTYPE, \_ Дата     |
| DATETIME          | DBTYPE, \_ Дата     |
| DateTime. TZ       | DBTYPE, \_ Дата     |
| ИСПРАВЛЕНо. 14,4        | DBTYPE \_ R4       |
| FLOAT             | DBTYPE \_ R8       |
| I1                | DBTYPE \_ I1       |
| I2                | DBTYPE \_ I2       |
| I4                | DBTYPE \_ I4       |
| I8                | DBTYPE \_ i8       |
| INT               | DBTYPE \_ i8       |
| LONG              | DBTYPE \_ I4       |
| NUMBER            | DBTYPE \_ R8       |
| Р4                | DBTYPE \_ R4       |
| R8                | DBTYPE \_ R8       |
| STRING            | DBTYPE \_ встр     |
| TIME              | DBTYPE \_ fileTime |
| Таймаут. TZ           | DBTYPE \_ fileTime |
| UI1               | DBTYPE \_ UI2      |
| UI2               | DBTYPE \_ UI2      |
| UI4               | DBTYPE \_ UI4      |
| UI8               | DBTYPE \_ UI8      |
| URI               | DBTYPE \_ встр     |
| UUID              | DBTYPE, \_ идентификатор GUID     |



 

Строковые данные можно привести к другим типам данных. Дополнительные сведения см. в разделе [приведение типа данных столбца](-search-sql-castingdatacolumntype.md).

 

 



