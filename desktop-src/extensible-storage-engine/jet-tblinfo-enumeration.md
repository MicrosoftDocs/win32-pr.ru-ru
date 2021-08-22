---
description: 'Дополнительные сведения: перечисление JET_TblInfo'
title: Перечисление JET_TblInfo
TOCTitle: JET_TblInfo enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_TblInfo
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_tblinfo(v=EXCHG.10)
ms:contentKeyID: 39512198
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_TblInfo
- Microsoft.Isam.Esent.Interop.JET_TblInfo.Dbid
- Microsoft.Isam.Esent.Interop.JET_TblInfo.TemplateTableName
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceUsage
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceAlloc
- Microsoft.Isam.Esent.Interop.JET_TblInfo.Name
- Microsoft.Isam.Esent.Interop.JET_TblInfo.Default
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceAvailable
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceOwned
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_TblInfo
- Microsoft.Isam.Esent.Interop.JET_TblInfo.Dbid
- Microsoft.Isam.Esent.Interop.JET_TblInfo.Default
- Microsoft.Isam.Esent.Interop.JET_TblInfo.TemplateTableName
- Microsoft.Isam.Esent.Interop.JET_TblInfo.Name
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceAvailable
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceOwned
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceUsage
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceAlloc
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0b2af9bfd69f81b518eba42f435a457c9baaa0d0ce8ddbac1424b997329a3ef0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119832684"
---
# <a name="jet_tblinfo-enumeration"></a>Перечисление JET_TblInfo

Информационные уровни для получения сведений о таблице с помощью Жетжеттаблеинфо.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Enumeration JET_TblInfo
'Usage
Dim instance As JET_TblInfo
```

``` csharp
public enum JET_TblInfo
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
<td>По умолчанию</td>
<td>Параметр по умолчанию. Извлекает <a href="dn335219(v=exchg.10).md">JET_OBJECTINFO</a> , содержащий сведения о таблице. Используйте этот параметр с <a href="dn292198(v=exchg.10).md">жетжеттаблеинфо (JET_SESID, JET_TABLEID, JET_OBJECTINFO, JET_TblInfo)</a>.</td>
</tr>
<tr class="even">
<td></td>
<td>Имя</td>
<td>Возвращает имя таблицы. Используйте этот параметр с <a href="dn292204(v=exchg.10).md">жетжеттаблеинфо (JET_SESID, JET_TABLEID, String, JET_TblInfo)</a>.</td>
</tr>
<tr class="odd">
<td></td>
<td>Dbid</td>
<td>Возвращает <a href="hh596176(v=exchg.10).md">JET_DBID</a> базы данных, содержащей таблицу. Используйте этот параметр с <a href="dn292197(v=exchg.10).md">жетжеттаблеинфо (JET_SESID, JET_TABLEID, JET_DBID, JET_TblInfo)</a>.</td>
</tr>
<tr class="even">
<td></td>
<td>спацеусаже</td>
<td>Поведение метода зависит от того, насколько велик массив, передаваемый в метод. Массив должен содержать по крайней мере две записи. Первая запись будет содержать число принадлежащих ей экстентов в таблице. Вторая запись будет содержать количество доступных экстентов в таблице. Если массив содержит более двух записей, остальные байты буфера будут состоять из массива структур, представляющих список экстентов. Эта структура содержит два члена: номер последней страницы в экстенте и количество страниц в экстенте. Используйте этот параметр с <a href="dn292202(v=exchg.10).md">жетжеттаблеинфо (JET_SESID, JET_TABLEID, [], JET_TblInfo)</a>.</td>
</tr>
<tr class="odd">
<td></td>
<td>спацеаллок</td>
<td>Массив, переданный в Жетжеттаблеинфо, должен содержать две записи. В первой записи будет задано количество страниц в таблице. Для второй записи будет задана Целевая плотность страниц таблицы. Используйте этот параметр с <a href="dn292202(v=exchg.10).md">жетжеттаблеинфо (JET_SESID, JET_TABLEID, [], JET_TblInfo)</a>.</td>
</tr>
<tr class="even">
<td></td>
<td>спацеовнед</td>
<td>Возвращает число принадлежащих страниц в таблице. Используйте этот параметр с <a href="dn292201(v=exchg.10).md">жетжеттаблеинфо (JET_SESID, JET_TABLEID, Int32, JET_TblInfo)</a>.</td>
</tr>
<tr class="odd">
<td></td>
<td>спацеаваилабле</td>
<td>Возвращает количество доступных страниц в таблице. Используйте этот параметр с <a href="dn292201(v=exchg.10).md">жетжеттаблеинфо (JET_SESID, JET_TABLEID, Int32, JET_TblInfo)</a>.</td>
</tr>
<tr class="even">
<td></td>
<td>темплатетабленаме</td>
<td>Если таблица является производной, то результат будет заполняться именем таблицы, из которой производная таблица наследовала ее DDL. Если таблица не является производной, буфер будет пустой строкой. Используйте этот параметр с <a href="dn292204(v=exchg.10).md">жетжеттаблеинфо (JET_SESID, JET_TABLEID, String, JET_TblInfo)</a>.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>См. также

#### <a name="reference"></a>Справочник

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
