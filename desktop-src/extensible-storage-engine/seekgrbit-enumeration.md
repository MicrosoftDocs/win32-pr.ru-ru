---
description: Дополнительные сведения о перечислении Сикгрбит
title: Перечисление Сикгрбит
TOCTitle: SeekGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.SeekGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.seekgrbit(v=EXCHG.10)
ms:contentKeyID: 39515862
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SeekGrbit
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekEQ
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekGE
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekGT
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekLE
- Microsoft.Isam.Esent.Interop.SeekGrbit.SetIndexRange
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekLT
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekGT
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekLT
- Microsoft.Isam.Esent.Interop.SeekGrbit.SetIndexRange
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekGE
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekLE
- Microsoft.Isam.Esent.Interop.SeekGrbit
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekEQ
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 12a65021d8c224d2a0ed50082b3120c94fc8c83f25c9aaf3eaf6e71d3f3f45f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118978594"
---
# <a name="seekgrbit-enumeration"></a>Перечисление Сикгрбит

Параметры для Жетсик.

Это перечисление имеет атрибут [FlagsAttribute](/dotnet/api/system.flagsattribute), который разрешает побитовое сочетание значений его элементов.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration SeekGrbit
'Usage
Dim instance As SeekGrbit
```

``` csharp
[FlagsAttribute]
public enum SeekGrbit
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
<td>сикек</td>
<td>Курсор будет располагаться на записи индекса, ближайшей к началу индекса, точно совпадающему с ключом поиска.</td>
</tr>
<tr class="even">
<td></td>
<td>сиклт</td>
<td>Курсор будет расположен в позиции индекса, ближайшей к концу индекса, который меньше, чем элемент индекса, который в точности соответствует условиям поиска.</td>
</tr>
<tr class="odd">
<td></td>
<td>сикле</td>
<td>Курсор будет расположен на позиции индекса, ближайшей к концу индекса, который меньше или равен элементу индекса, который в точности соответствует условиям поиска.</td>
</tr>
<tr class="even">
<td></td>
<td>сикже</td>
<td>Курсор будет расположен на позиции индекса, ближайшей к началу индекса, который больше или равен элементу индекса, который в точности соответствует условиям поиска.</td>
</tr>
<tr class="odd">
<td></td>
<td>сикгт</td>
<td>Курсор будет расположен на позиции индекса, ближайшей к началу индекса, который больше, чем элемент индекса, который точно соответствует условиям поиска.</td>
</tr>
<tr class="even">
<td></td>
<td>сетиндексранже</td>
<td>Диапазон индексов будет автоматически настроен для всех ключей, точно соответствующих ключу поиска.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>См. также

#### <a name="reference"></a>Справочник

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
