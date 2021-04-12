---
description: 'Дополнительные сведения: структура JET_OBJECTLIST'
title: Структура JET_OBJECTLIST
TOCTitle: JET_OBJECTLIST Structure
ms:assetid: 95f12f2a-13da-48d4-a254-fc0cb718b17d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269348(v=EXCHG.10)
ms:contentKeyID: 32765635
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a7a66bb3b7f7dfbbfd1087d1fe0ce32c4144a8bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347515"
---
# <a name="jet_objectlist-structure"></a>Структура JET_OBJECTLIST


_**Применимо к:** Windows | Windows Server_

## <a name="jet_objectlist-structure"></a>Структура JET_OBJECTLIST

Структура **JET_OBJECTLIST** проходит по временной таблице, созданной с помощью [жетжетобжектинфо](./jetgetobjectinfo-function.md). Каждая строка во временной таблице описывает объект в базе данных.

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_TABLEID tableid;
      unsigned long cRecord;
      JET_COLUMNID columnidcontainername;
      JET_COLUMNID columnidobjectname;
      JET_COLUMNID columnidobjtyp;
      JET_COLUMNID columniddtCreate;
      JET_COLUMNID columniddtUpdate;
      JET_COLUMNID columnidgrbit;
      JET_COLUMNID columnidflags;
      JET_COLUMNID columnidcRecord;
      JET_COLUMNID columnidcPage;
    } JET_OBJECTLIST;
```

### <a name="members"></a>Элементы

**кбструкт**

Размер структуры в байтах. Вызов API обновит это поле, поэтому вызывающий должен убедиться, что это значение соответствует sizeof (JET_INDEXLIST).

**TableID**

Идентификатор созданной временной таблицы. Вызывающий объект должен содержать код, который будет закрывать таблицу.

**крекорд**

Количество записей во временной таблице, которые были созданы.

**колумнидконтаинернаме**

Идентификатор столбца имени типа контейнера.

Единственными поддерживаемыми в настоящее время контейнерами являются таблицы. Этот столбец является [JET_coltypTextом](./jet-coltyp.md).

**колумнидобжектнаме**

Идентификатор столбца имени объекта.

Этот столбец является [JET_coltypTextом](./jet-coltyp.md).

**колумнидобжтип**

Идентификатор столбца типа объекта. Единственными поддерживаемыми в настоящее время контейнерами являются таблицы, поэтому это поле будет JET_objtypTable.

Этот столбец является [JET_coltypLongом](./jet-coltyp.md).

**колумниддткреате**

Является устаревшей. Не используйте.

**колумниддтупдате**

Является устаревшей. Не используйте.

**колумнидгрбит**

Идентификатор столбца **грбитс** , который применим к объекту. Список применимых **грбитс** см. в разделе [JET_TABLECREATE](./jet-tablecreate-structure.md).

Этот столбец является [JET_coltypLongом](./jet-coltyp.md).

**колумнидфлагс**

Идентификатор столбца флагов, применимых к объекту. Список применимых флагов см. в разделе [JET_OBJECTINFO](./jet-objectinfo-structure.md).

Этот столбец является [JET_coltypLongом](./jet-coltyp.md).

**колумнидкрекорд**

Идентификатор столбца количества записей, имеющихся в таблице с именем в **колумнидобжектнаме**.

Этот столбец является [JET_coltypLongом](./jet-coltyp.md).

**колумнидкпаже**

Идентификатор столбца числа страниц, используемых объектом.

Этот столбец является [JET_coltypLongом](./jet-coltyp.md).

### <a name="remarks"></a>Комментарии

Каждая строка во временной таблице соответствует объекту в базе данных.

При создании временной таблицы с параметром *инфолевел* в функции [жетжетобжектинфо](./jetgetobjectinfo-function.md) , для которой задано значение JET_ObjInfoListNoStats, столбцы, идентифицируемые **колумнидкрекорд** и **колумнидкпаже** , не будут содержать осмысленной информации.

Сейчас в временной таблице будут только сведения о таблицах.

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

[JET_COLTYP](./jet-coltyp.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_OBJECTINFO](./jet-objectinfo-structure.md)  
[JET_TABLECREATE](./jet-tablecreate-structure.md)  
[жетжетобжектинфо](./jetgetobjectinfo-function.md)
