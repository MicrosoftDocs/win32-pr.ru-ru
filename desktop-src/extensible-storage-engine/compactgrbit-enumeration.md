---
description: Дополнительные сведения о перечислении Компактгрбит
title: Перечисление Компактгрбит
TOCTitle: CompactGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.CompactGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.compactgrbit(v=EXCHG.10)
ms:contentKeyID: 39509676
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.CompactGrbit
- Microsoft.Isam.Esent.Interop.CompactGrbit.None
- Microsoft.Isam.Esent.Interop.CompactGrbit.Stats
- Microsoft.Isam.Esent.Interop.CompactGrbit.Repair
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.CompactGrbit.Repair
- Microsoft.Isam.Esent.Interop.CompactGrbit.Stats
- Microsoft.Isam.Esent.Interop.CompactGrbit
- Microsoft.Isam.Esent.Interop.CompactGrbit.None
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a85f3298e4127a35acd5a39839f788fc404269f80a07463bde1417dc04f7fe16
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119976544"
---
# <a name="compactgrbit-enumeration"></a>Перечисление Компактгрбит

Параметры для [жеткомпакт (JET_SESID, String, String, JET_PFNSTATUS, JET_CONVERT, компактгрбит)](./api.jetcompact-method.md).

Это перечисление имеет атрибут [FlagsAttribute](/dotnet/api/system.flagsattribute), который разрешает побитовое сочетание значений его элементов.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration CompactGrbit
'Usage
Dim instance As CompactGrbit
```

``` csharp
[FlagsAttribute]
public enum CompactGrbit
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
<td>Статистика</td>
<td>Вызывает Жеткомпакт для дампа статистики в базе данных-источнике в файл с именем DFRGINFO.TXT. Статистика включает в себя имя каждой таблицы в базе данных источника, число строк в каждой таблице, общий размер в байтах всех строк в каждой таблице, общий размер в байтах всех столбцов типа <a href="hh577895(v=exchg.10).md">LongText</a> или <a href="hh577895(v=exchg.10).md">лонгбинари</a> , которые достаточно велики для хранения отдельно от записи, число конечных страниц кластеризованного индекса и количество конечных страниц с длинными значениями. Кроме того, сводные статистические данные, включая размер базы данных-источника, целевую базу данных, время, необходимое для сжатия базы данных, также сохраняются в дампе временной базы данных.</td>
</tr>
<tr class="odd">
<td></td>
<td>Восстановить</td>
<td><strong>Устарело.</strong> Используется, если база данных-источник повреждена. Она обеспечивает целый набор новых поведений, предназначенных для восстановления максимально возможного объема данных из базы данных-источника. Жеткомпакт с этим набором параметров может вернуть значение <a href="hh564840(v=exchg.10).md">Success</a> , но не скопировать все данные, созданные в базе данных источника. Данные, которые находятся в поврежденных частях базы данных источника, будут пропущены.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
