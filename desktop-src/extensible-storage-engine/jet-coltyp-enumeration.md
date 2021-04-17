---
description: 'Дополнительные сведения: перечисление JET_coltyp'
title: Перечисление JET_coltyp
TOCTitle: JET_coltyp enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_coltyp
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_coltyp(v=EXCHG.10)
ms:contentKeyID: 39511169
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_coltyp.Nil
- Microsoft.Isam.Esent.Interop.JET_coltyp.IEEEDouble
- Microsoft.Isam.Esent.Interop.JET_coltyp.LongBinary
- Microsoft.Isam.Esent.Interop.JET_coltyp.LongText
- Microsoft.Isam.Esent.Interop.JET_coltyp.Text
- Microsoft.Isam.Esent.Interop.JET_coltyp.IEEESingle
- Microsoft.Isam.Esent.Interop.JET_coltyp.DateTime
- Microsoft.Isam.Esent.Interop.JET_coltyp.Binary
- Microsoft.Isam.Esent.Interop.JET_coltyp.UnsignedByte
- Microsoft.Isam.Esent.Interop.JET_coltyp.Currency
- Microsoft.Isam.Esent.Interop.JET_coltyp.Bit
- Microsoft.Isam.Esent.Interop.JET_coltyp.Long
- Microsoft.Isam.Esent.Interop.JET_coltyp
- Microsoft.Isam.Esent.Interop.JET_coltyp.Short
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_coltyp.Binary
- Microsoft.Isam.Esent.Interop.JET_coltyp.Short
- Microsoft.Isam.Esent.Interop.JET_coltyp.Bit
- Microsoft.Isam.Esent.Interop.JET_coltyp.UnsignedByte
- Microsoft.Isam.Esent.Interop.JET_coltyp.IEEEDouble
- Microsoft.Isam.Esent.Interop.JET_coltyp.IEEESingle
- Microsoft.Isam.Esent.Interop.JET_coltyp
- Microsoft.Isam.Esent.Interop.JET_coltyp.Currency
- Microsoft.Isam.Esent.Interop.JET_coltyp.Nil
- Microsoft.Isam.Esent.Interop.JET_coltyp.DateTime
- Microsoft.Isam.Esent.Interop.JET_coltyp.LongBinary
- Microsoft.Isam.Esent.Interop.JET_coltyp.Long
- Microsoft.Isam.Esent.Interop.JET_coltyp.LongText
- Microsoft.Isam.Esent.Interop.JET_coltyp.Text
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 616dc80d835e22502b6781355a2eff35a6375e05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674231"
---
# <a name="jet_coltyp-enumeration"></a>Перечисление JET_coltyp

Типы столбцов ESENT.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Enumeration JET_coltyp
'Usage
Dim instance As JET_coltyp
```

``` csharp
public enum JET_coltyp
```

## <a name="members"></a>Члены

<table>
<thead>
<tr class="header">
<th></th>
<th>Имя участника</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td>Указатель</td>
<td>Тип столбца NULL. Недопустимый для создания столбца.</td>
</tr>
<tr class="even">
<td></td>
<td>bit</td>
<td>True, false или NULL.</td>
</tr>
<tr class="odd">
<td></td>
<td>UnsignedByte</td>
<td>1-байтовое целое число без знака.</td>
</tr>
<tr class="even">
<td></td>
<td>Short</td>
<td>2-байтовое целое число со знаком.</td>
</tr>
<tr class="odd">
<td></td>
<td>Long</td>
<td>4-байтовое целое число со знаком.</td>
</tr>
<tr class="even">
<td></td>
<td>Валюта</td>
<td>8-байтовое целое число со знаком.</td>
</tr>
<tr class="odd">
<td></td>
<td>ииесингле</td>
<td>4-байтовые одиночные точности с стандартом IEEE.</td>
</tr>
<tr class="even">
<td></td>
<td>ииедаубле</td>
<td>8-байтная двойная точность IEEE.</td>
</tr>
<tr class="odd">
<td></td>
<td>Дата/время</td>
<td>Целочисленная Дата, дробная часть времени.</td>
</tr>
<tr class="even">
<td></td>
<td>Двоичные данные</td>
<td>Двоичные данные размером до 255 байт.</td>
</tr>
<tr class="odd">
<td></td>
<td>Текст</td>
<td>Текстовые данные размером до 255 байт.</td>
</tr>
<tr class="even">
<td></td>
<td>LongBinary</td>
<td>Двоичные данные, до 2 ГБ.</td>
</tr>
<tr class="odd">
<td></td>
<td>LongText</td>
<td>Текстовые данные, до 2 ГБ.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
