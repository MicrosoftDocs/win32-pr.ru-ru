---
description: Дополнительные сведения о перечислении Сеткуррентиндексгрбит
title: Перечисление Сеткуррентиндексгрбит
TOCTitle: SetCurrentIndexGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.setcurrentindexgrbit(v=EXCHG.10)
ms:contentKeyID: 39515072
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit.MoveFirst
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit.NoMove
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit.None
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit.NoMove
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit.MoveFirst
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2391715332989bf20aae3d0a666c1cef2ce2e135
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711225"
---
# <a name="setcurrentindexgrbit-enumeration"></a>Перечисление Сеткуррентиндексгрбит

Параметры для [JetSetCurrentIndex2 (JET_SESID, JET_TABLEID, String, сеткуррентиндексгрбит)](./api.jetsetcurrentindex2-method.md) и [JetSetCurrentIndex3 (JET_SESID, JET_TABLEID, String, сеткуррентиндексгрбит, Int32)](./api.jetsetcurrentindex3-method.md).

Это перечисление имеет атрибут [FlagsAttribute](/dotnet/api/system.flagsattribute), который разрешает побитовое сочетание значений его элементов.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration SetCurrentIndexGrbit
'Usage
Dim instance As SetCurrentIndexGrbit
```

``` csharp
[FlagsAttribute]
public enum SetCurrentIndexGrbit
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
<td>Параметры по умолчанию. Это то же самое, что и MoveFirst.</td>
</tr>
<tr class="even">
<td></td>
<td>MoveFirst</td>
<td>Указывает, что курсор должен располагаться на первой записи указанного индекса. Если текущий индекс выбран, этот параметр игнорируется.</td>
</tr>
<tr class="odd">
<td></td>
<td>Не перемещать</td>
<td>Указывает, что курсор должен располагаться на записи индекса нового индекса, который соответствует записи, связанной с записью индекса, в текущей позиции курсора по старому индексу.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
