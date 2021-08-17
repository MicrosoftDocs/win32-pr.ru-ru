---
description: 'Дополнительные сведения: перечисление JET_DbInfo'
title: Перечисление JET_DbInfo
TOCTitle: JET_DbInfo enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_DbInfo
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbinfo(v=EXCHG.10)
ms:contentKeyID: 39516181
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Version
- Microsoft.Isam.Esent.Interop.JET_DbInfo
- Microsoft.Isam.Esent.Interop.JET_DbInfo.SpaceAvailable
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Transactions
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Filename
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Filesize
- Microsoft.Isam.Esent.Interop.JET_DbInfo.FileType
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Misc
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Options
- Microsoft.Isam.Esent.Interop.JET_DbInfo.SpaceOwned
- Microsoft.Isam.Esent.Interop.JET_DbInfo.LCID
- Microsoft.Isam.Esent.Interop.JET_DbInfo.PageSize
- Microsoft.Isam.Esent.Interop.JET_DbInfo.DBInUse
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_DbInfo.DBInUse
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Filename
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Filesize
- Microsoft.Isam.Esent.Interop.JET_DbInfo.FileType
- Microsoft.Isam.Esent.Interop.JET_DbInfo.SpaceOwned
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Misc
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Options
- Microsoft.Isam.Esent.Interop.JET_DbInfo.PageSize
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Transactions
- Microsoft.Isam.Esent.Interop.JET_DbInfo
- Microsoft.Isam.Esent.Interop.JET_DbInfo.LCID
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Version
- Microsoft.Isam.Esent.Interop.JET_DbInfo.SpaceAvailable
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c364b89ccb50542130c988a643fed594a34e370e5adb5e9d0a13f77eab5b04d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119112233"
---
# <a name="jet_dbinfo-enumeration"></a>Перечисление JET_DbInfo

Информационные уровни для получения сведений о базе данных.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Enumeration JET_DbInfo
'Usage
Dim instance As JET_DbInfo
```

``` csharp
public enum JET_DbInfo
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
<td>Имя файла</td>
<td>Возвращает путь к файлу базы данных (строка).</td>
</tr>
<tr class="even">
<td></td>
<td>LCID</td>
<td>Возвращает код локали (LCID), связанный с этой базой данных (Int32).</td>
</tr>
<tr class="odd">
<td></td>
<td>Параметры</td>
<td>Возвращает <a href="hh579532(v=exchg.10).md">опендатабасегрбит</a>. Указывает, открыта ли база данных в монопольном режиме. Если база данных находится в монопольном режиме, будет возвращен <a href="hh579532(v=exchg.10).md">монопольный</a> режим, в противном случае возвращается ноль. Другие параметры грбит базы данных для Жетаттачдатабасе и Жетопендатабасе не возвращаются.</td>
</tr>
<tr class="even">
<td></td>
<td>Transactions</td>
<td>Возвращает число, которое больше, чем максимальный уровень, до которого транзакции могут быть вложенными. Если вызывается <a href="dn292105(v=exchg.10).md">жетбегинтрансактион (JET_SESID)</a> (во вложенном режиме, то есть в том же сеансе без фиксации или отката), то при последнем вызове <a href="hh564840(v=exchg.10).md">транстудип</a> будет возвращено значение (Int32).</td>
</tr>
<tr class="odd">
<td></td>
<td>Версия</td>
<td>Возвращает основной номер версии ядра СУБД (Int32).</td>
</tr>
<tr class="even">
<td></td>
<td>Размер файла</td>
<td>Возвращает размер файла базы данных на страницах (Int32).</td>
</tr>
<tr class="odd">
<td></td>
<td>спацеовнед</td>
<td>Возвращает пространство, принадлежащее базе данных, на страницах (Int32).</td>
</tr>
<tr class="even">
<td></td>
<td>спацеаваилабле</td>
<td>Возвращает доступное пространство в базе данных на страницах (Int32).</td>
</tr>
<tr class="odd">
<td></td>
<td>Разное</td>
<td>Возвращает объект <a href="hh538867(v=exchg.10).md">JET_DBINFOMISC</a> .</td>
</tr>
<tr class="even">
<td></td>
<td>дбинусе</td>
<td>Возвращает логическое значение, указывающее, присоединена ли база данных (логический).</td>
</tr>
<tr class="odd">
<td></td>
<td>PageSize</td>
<td>Возвращает размер страницы базы данных (Int32).</td>
</tr>
<tr class="even">
<td></td>
<td>FileType</td>
<td>Возвращает тип базы данных (<a href="hh566739(v=exchg.10).md">JET_filetype</a>).</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
