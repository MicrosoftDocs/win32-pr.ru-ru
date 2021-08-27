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
ms.openlocfilehash: a2f035a15c0f0f2861c7c6698878e0782feb35ce
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476540"
---
# <a name="jet_objectlist-structure"></a>Структура JET_OBJECTLIST


_**Применимо к:** Windows | Windows Сервером_

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


| | | <p><strong>Клиент</strong></p> | <p>требуется Windows Vista, Windows XP или Windows 2000 Professional.</p> | | <p><strong>Сервер</strong></p> | <p>требуется Windows server 2008, Windows server 2003 или сервер Windows 2000.</p> | | <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | 



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
