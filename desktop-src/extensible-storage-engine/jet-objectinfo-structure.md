---
description: 'Дополнительные сведения: структура JET_OBJECTINFO'
title: Структура JET_OBJECTINFO
TOCTitle: JET_OBJECTINFO Structure
ms:assetid: 9d348ab3-d453-4316-9233-681f165e8ef1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269353(v=EXCHG.10)
ms:contentKeyID: 32765640
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cd1f8a876153b5b457cfb153cbf35fa2d388b0f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081187"
---
# <a name="jet_objectinfo-structure"></a>Структура JET_OBJECTINFO


_**Применимо к:** Windows | Windows Server_

## <a name="jet_objectinfo-structure"></a>Структура JET_OBJECTINFO

Структура **JET_OBJECTINFO** содержит сведения об объекте. В настоящее время поддерживаются только таблицы типов объектов.

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_OBJTYP objtyp;
      JET_DATESERIAL dtCreate;
      JET_DATESERIAL dtUpdate;
      JET_GRBIT grbit;
      unsigned long flags;
      unsigned long cRecord;
      unsigned long cPage;
    } JET_OBJECTINFO;
```

### <a name="members"></a>Элементы

**кбструкт**

Размер структуры **JET_OBJECTINFO** в байтах.

**обжтип**

Содержит [JET_OBJTYP](./jet-objtyp.md) структуры. В настоящее время возвращаются только таблицы (то есть JET_objtypTable).

**дткреате**

Является устаревшей. Не используйте.

**дтупдате**

Является устаревшей. Не используйте.

**грбит**

Группа битов, содержащая параметры, доступные для данного вызова, которые включают ноль или более следующих значений.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Значение</p></th>
<th><p>Значение</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitTableInfoBookmark</p></td>
<td><p>В таблице могут быть закладки.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTableInfoRollback</p></td>
<td><p>Можно выполнить откат таблицы.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTableInfoUpdatable</p></td>
<td><p>Таблицу можно обновить.</p></td>
</tr>
</tbody>
</table>


**flags**

Битовое поле, которое содержит ноль или более следующих флагов.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Значение</p></th>
<th><p>Значение</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitObjectSystem</p></td>
<td><p>Таблица является системной таблицей и предназначена только для внутреннего использования.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitObjectTableDerived</p></td>
<td><p>Таблица, унаследованная на языке DDL из таблицы шаблонов.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitObjectTableFixedDDL</p></td>
<td><p>Невозможно изменить DDL для таблицы.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitObjectTableNoFixedVarColumnsInDerivedTables</p></td>
<td><p>Используется в сочетании с JET_bitObjectTableTemplate для запрета фиксированных или переменных столбцов в производных таблицах (чтобы в будущем можно было добавить в шаблон фиксированные или переменные столбцы).</p>
<p><strong>Windows XP:  </strong> Это значение вводится в Windows XP.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitObjectTableTemplate</p></td>
<td><p>Таблица является таблицей шаблонов.</p></td>
</tr>
</tbody>
</table>


**крекорд**

Число записей в таблице.

Это значение извлекается, только если **JET_OBJECTINFO** был передан в [жетжетобжектинфо](./jetgetobjectinfo-function.md).

**кпаже**

Количество страниц, используемых таблицей.

Это значение извлекается, только если **JET_OBJECTINFO** был передан в [жетжетобжектинфо](./jetgetobjectinfo-function.md).

### <a name="remarks"></a>Комментарии

Структура **JET_OBJECTINFO** заполняется вызовом [жетжетобжектинфо](./jetgetobjectinfo-function.md) или [жетжеттаблеинфо](./jetgettableinfo-function.md). Если вызов API не выполняется, содержимое структуры не определено.

Если применимо, статистика таблицы включает количество записей и количество страниц в кластеризованном индексе (то есть индекс, содержащий данные записи). Доступ к статистике индекса осуществляется отдельно по имени с помощью [жетжетиндексинфо](./jetgetindexinfo-function.md) или [жетжеттаблеиндексинфо](./jetgettableindexinfo-function.md).

### <a name="requirements"></a>Требования

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
</tbody>
</table>


### <a name="see-also"></a>См. также:

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_OBJTYP](./jet-objtyp.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[жетжетиндексинфо](./jetgetindexinfo-function.md)  
[жетжетобжектинфо](./jetgetobjectinfo-function.md)  
[жетжеттаблеиндексинфо](./jetgettableindexinfo-function.md)  
[жетжеттаблеинфо](./jetgettableinfo-function.md)
