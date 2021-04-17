---
description: 'Дополнительные сведения: перечисление JET_IdxInfo'
title: Перечисление JET_IdxInfo
TOCTitle: JET_IdxInfo enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_IdxInfo
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_idxinfo(v=EXCHG.10)
ms:contentKeyID: 39512789
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.VarSegMac
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.KeyMost
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.IndexId
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.SysTabCursor
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.OLC
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.Default
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.ResetOLC
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.SpaceAlloc
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.Langid
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.LCID
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.List
- Microsoft.Isam.Esent.Interop.JET_IdxInfo
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.Count
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.LCID
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.IndexId
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.SpaceAlloc
- Microsoft.Isam.Esent.Interop.JET_IdxInfo
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.List
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.VarSegMac
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.KeyMost
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.OLC
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.ResetOLC
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.SysTabCursor
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.Count
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.Default
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.Langid
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e1f2cb50537ed492a428c82fd9a6f6541c5fad2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712883"
---
# <a name="jet_idxinfo-enumeration"></a>Перечисление JET_IdxInfo

Информационные уровни для получения сведений об индексе с помощью Жетжетиндексинфо. и Жетжеттаблеиндексинфо.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Enumeration JET_IdxInfo
'Usage
Dim instance As JET_IdxInfo
```

``` csharp
public enum JET_IdxInfo
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
<td>Значение по умолчанию</td>
<td>Возвращает структуру <a href="dn335123(v=exchg.10).md">JET_INDEXLIST</a> со сведениями об индексе.</td>
</tr>
<tr class="even">
<td></td>
<td>Список</td>
<td>Возвращает структуру <a href="dn335123(v=exchg.10).md">JET_INDEXLIST</a> со сведениями об индексе.</td>
</tr>
<tr class="odd">
<td></td>
<td>систабкурсор</td>
<td><strong>Устарело.</strong> Систабкурсор устарел.</td>
</tr>
<tr class="even">
<td></td>
<td>олк</td>
<td><strong>Устарело.</strong> ОЛК устарел.</td>
</tr>
<tr class="odd">
<td></td>
<td>ресетолк</td>
<td><strong>Устарело.</strong> Сброс ОЛК устарел.</td>
</tr>
<tr class="even">
<td></td>
<td>спацеаллок</td>
<td>Возвращает целое число с использованием пространства индекса.</td>
</tr>
<tr class="odd">
<td></td>
<td>LCID</td>
<td>Возвращает целое число с идентификатором LCID индекса.</td>
</tr>
<tr class="even">
<td></td>
<td>Надежно</td>
<td><strong>Устарело.</strong> LangID устарел. Вместо этого используйте LCID.</td>
</tr>
<tr class="odd">
<td></td>
<td>Count</td>
<td>Возвращает целое число с числом индексов в таблице.</td>
</tr>
<tr class="even">
<td></td>
<td>варсегмак</td>
<td>Возвращает значение ushort со значением Кбварсегмак, с которым был создан индекс.</td>
</tr>
<tr class="odd">
<td></td>
<td>IndexId</td>
<td>Возвращает <a href="hh557060(v=exchg.10).md">JET_INDEXID</a> , определяющую индекс.</td>
</tr>
<tr class="even">
<td></td>
<td>кэймост</td>
<td>Впервые появился в Windows Vista. Возвращает значение ushort со значением Кбкэймост, с которым был создан индекс.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
