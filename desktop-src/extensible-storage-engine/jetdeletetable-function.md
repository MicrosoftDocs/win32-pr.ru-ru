---
description: Дополнительные сведения о функции Жетделететабле
title: Функция Жетделететабле
TOCTitle: JetDeleteTable Function
ms:assetid: e8a4131f-a69b-41f3-94c6-a1607fc23c1f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294128(v=EXCHG.10)
ms:contentKeyID: 32765742
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDeleteTable
- JetDeleteTableA
- JetDeleteTableW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c432f8e09ad706b6632e4e5ca49a89a263a84dbb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105713141"
---
# <a name="jetdeletetable-function"></a>Функция Жетделететабле


_**Применимо к:** Windows | Windows Server_

## <a name="jetdeletetable-function"></a>Функция Жетделететабле

Функция **жетделететабле** удаляет таблицу в базе данных ESE.

```cpp
    JET_ERR JET_API JetDeleteTable(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szTableName
    );
```

### <a name="parameters"></a>Параметры

*сесид*

Контекст сеанса базы данных, используемый для вызова API.

*DBID*

Идентификатор базы данных, используемый для вызова API.

*сзтабленаме*

Имя таблицы для удаления.

### <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата. Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Код возврата</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>Операция выполнена успешно.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTableInUse</p></td>
<td><p>Предпринята попытка удалить таблицу, в то время как другой сеанс имеет идентификатор открытой таблицы (<a href="gg269182(v=exchg.10).md">JET_TABLEID</a>) с <a href="gg294118(v=exchg.10).md">жетопентабле</a> или <a href="gg269193(v=exchg.10).md">жетдупкурсор</a>.</p></td>
</tr>
<tr class="odd">
<td><p>Таблица JET_errCannotDeletetemporary</p></td>
<td><p>Была предпринята попытка удалить временную таблицу. Временная таблица автоматически удаляется, когда она закрывается с помощью <a href="gg294087(v=exchg.10).md">жетклосетабле</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCannotDeleteTemplateTable</p></td>
<td><p>Предпринята попытка удалить таблицу шаблонов, то есть таблицу, из которой может быть унаследована инструкция DDL.</p></td>
</tr>
</tbody>
</table>


#### <a name="requirements"></a>Требования

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Клиент</strong></p></td>
<td><p>Требуется Windows Vista, Windows XP или Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Объявлено в ESENT. h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Библиотека</strong></p></td>
<td><p>Используйте ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>КОМПОНОВКИ</strong></p></td>
<td><p>Требуется ESENT.dll.</p></td>
</tr>
<tr class="even">
<td><p><strong>Юникод</strong></p></td>
<td><p>Реализуется как <strong>жетделететаблев</strong> (Юникод) и <strong>жетделететаблеа</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>См. также:

[JET_DBID](./jet-dbid.md)  
[JET_SESID](./jet-sesid.md)  
[жетклосетабле](./jetclosetable-function.md)
