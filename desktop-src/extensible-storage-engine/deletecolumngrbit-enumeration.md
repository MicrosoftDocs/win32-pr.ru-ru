---
description: Дополнительные сведения о перечислении Делетеколумнгрбит
title: Перечисление Делетеколумнгрбит
TOCTitle: DeleteColumnGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.DeleteColumnGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.deletecolumngrbit(v=EXCHG.10)
ms:contentKeyID: 39512792
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.DeleteColumnGrbit
- Microsoft.Isam.Esent.Interop.DeleteColumnGrbit.IgnoreTemplateColumns
- Microsoft.Isam.Esent.Interop.DeleteColumnGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.DeleteColumnGrbit
- Microsoft.Isam.Esent.Interop.DeleteColumnGrbit.None
- Microsoft.Isam.Esent.Interop.DeleteColumnGrbit.IgnoreTemplateColumns
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3191d3c73883d0bd27b4944718f2a0b3423e2c8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719400"
---
# <a name="deletecolumngrbit-enumeration"></a>Перечисление Делетеколумнгрбит

Параметры для [JetDeleteColumn2 (JET_SESID, JET_TABLEID, String, делетеколумнгрбит)](./api.jetdeletecolumn2-method.md).

Это перечисление имеет атрибут [FlagsAttribute](/dotnet/api/system.flagsattribute), который разрешает побитовое сочетание значений его элементов.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration DeleteColumnGrbit
'Usage
Dim instance As DeleteColumnGrbit
```

``` csharp
[FlagsAttribute]
public enum DeleteColumnGrbit
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
<td>Нет</td>
<td>Параметры по умолчанию.</td>
</tr>
<tr class="even">
<td></td>
<td>игноретемплатеколумнс</td>
<td>API должен попытаться удалить только столбцы из производной таблицы. Если столбец с таким именем существует в базовой таблице, он будет проигнорирован.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
