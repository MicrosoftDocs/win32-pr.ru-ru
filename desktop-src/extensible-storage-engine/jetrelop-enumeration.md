---
description: Дополнительные сведения о перечислении Жетрелоп
title: Перечисление Жетрелоп (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: JetRelop enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Windows8.JetRelop
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.jetrelop(v=EXCHG.10)
ms:contentKeyID: 55104456
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.BitmaskEqualsZero
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.BitmaskNotEqualsZero
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.Equals
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.GreaterThan
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.GreaterThanOrEqual
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.LessThan
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.LessThanOrEqual
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.NotEquals
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.PrefixEquals
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.GreaterThan
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.GreaterThanOrEqual
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.PrefixEquals
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.BitmaskNotEqualsZero
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.LessThanOrEqual
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.LessThan
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.NotEquals
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.BitmaskEqualsZero
- Microsoft.Isam.Esent.Interop.Windows8.JetRelop.Equals
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7839e0223eb9dd773ca9a5d10b5210b10b0a944a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350415"
---
# <a name="jetrelop-enumeration"></a>Перечисление Жетрелоп

Операция сравнения для фильтра, определенного как [JET_INDEX_COLUMN](./jet-index-column-class.md).

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Enumeration JetRelop
'Usage
Dim instance As JetRelop
```

``` csharp
public enum JetRelop
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
<td>Равно</td>
<td>Принимать только строки, имеющие значение столбца, равное заданному значению.</td>
</tr>
<tr class="even">
<td></td>
<td>префиксекуалс</td>
<td>Принимать только строки со столбцами, префикс которых соответствует заданному значению.</td>
</tr>
<tr class="odd">
<td></td>
<td>NotEquals</td>
<td>Принимать только строки, значения столбца которых не равны заданному значению.</td>
</tr>
<tr class="even">
<td></td>
<td>LessThanOrEqual;</td>
<td>Принимать только строки, для которых значение столбца меньше или равно заданному значению.</td>
</tr>
<tr class="odd">
<td></td>
<td>LessThan;</td>
<td>Принимать только строки, значения столбцов которых меньше заданного значения.</td>
</tr>
<tr class="even">
<td></td>
<td>GreaterThanOrEqual;</td>
<td>Принимать только строки, имеющие значение столбца больше или равное заданному значению.</td>
</tr>
<tr class="odd">
<td></td>
<td>GreaterThan</td>
<td>Принимать только строки, значения столбцов которых больше заданного значения.</td>
</tr>
<tr class="even">
<td></td>
<td>битмаскекуалсзеро</td>
<td>Принимать только строки, имеющие значение столбца and с заданной битовой маской, возвращающей ноль.</td>
</tr>
<tr class="odd">
<td></td>
<td>битмаскнотекуалсзеро</td>
<td>Принимать только строки, имеющие значение столбца and с заданной битовой маской, что приводит к ненулевому значению.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Пространство имен Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)
