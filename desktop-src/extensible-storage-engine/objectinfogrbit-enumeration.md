---
description: Дополнительные сведения о перечислении Обжектинфогрбит
title: Перечисление Обжектинфогрбит
TOCTitle: ObjectInfoGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.ObjectInfoGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.objectinfogrbit(v=EXCHG.10)
ms:contentKeyID: 39516208
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ObjectInfoGrbit
- Microsoft.Isam.Esent.Interop.ObjectInfoGrbit.Bookmark
- Microsoft.Isam.Esent.Interop.ObjectInfoGrbit.Rollback
- Microsoft.Isam.Esent.Interop.ObjectInfoGrbit.Updatable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ObjectInfoGrbit.Bookmark
- Microsoft.Isam.Esent.Interop.ObjectInfoGrbit.Rollback
- Microsoft.Isam.Esent.Interop.ObjectInfoGrbit.Updatable
- Microsoft.Isam.Esent.Interop.ObjectInfoGrbit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4028a2a337b32394029960e45bb0e485c2b6b705
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712065"
---
# <a name="objectinfogrbit-enumeration"></a>Перечисление Обжектинфогрбит

Параметры таблицы, используемые в [JET_OBJECTINFO](./jet-objectinfo-class.md).

Это перечисление имеет атрибут [FlagsAttribute](/dotnet/api/system.flagsattribute), который разрешает побитовое сочетание значений его элементов.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration ObjectInfoGrbit
'Usage
Dim instance As ObjectInfoGrbit
```

``` csharp
[FlagsAttribute]
public enum ObjectInfoGrbit
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
<td>Закладка</td>
<td>В таблице могут быть закладки.</td>
</tr>
<tr class="even">
<td></td>
<td>Откат</td>
<td>Можно выполнить откат таблицы.</td>
</tr>
<tr class="odd">
<td></td>
<td>Обновляется</td>
<td>Таблицу можно обновить.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
