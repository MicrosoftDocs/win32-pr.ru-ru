---
description: 'Дополнительные сведения: структура JET_COLUMNLIST'
title: Структура JET_COLUMNLIST
TOCTitle: JET_COLUMNLIST Structure
ms:assetid: 3899676f-c96e-4f15-9089-4faea6808bc2
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269228(v=EXCHG.10)
ms:contentKeyID: 32765530
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
ms.openlocfilehash: c61f3492a9f92700fc51b7e51e13f8c3c3febc69
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985267"
---
# <a name="jet_columnlist-structure"></a>Структура JET_COLUMNLIST


_**Применимо к:** Windows | Windows Сервером_

## <a name="jet_columnlist-structure"></a>Структура JET_COLUMNLIST

Структура **JET_COLUMNLIST** содержит сведения, необходимые для прохода по временной таблице, созданной функциями [жетжетколумнинфо](./jetgetcolumninfo-function.md) и [жетжеттаблеколумнинфо](./jetgettablecolumninfo-function.md) . Каждая строка во временной таблице описывает столбец в таблице, указанной в вызове API. Эта структура используется только с [жетжетколумнинфо](./jetgetcolumninfo-function.md) и [жетжеттаблеколумнинфо](./jetgettablecolumninfo-function.md).

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_TABLEID tableid;
      unsigned long cRecord;
      JET_COLUMNID columnidPresentationOrder;
      JET_COLUMNID columnidcolumnname;
      JET_COLUMNID columnidcolumnid;
      JET_COLUMNID columnidcoltyp;
      JET_COLUMNID columnidCountry;
      JET_COLUMNID columnidLangid;
      JET_COLUMNID columnidCp;
      JET_COLUMNID columnidCollate;
      JET_COLUMNID columnidcbMax;
      JET_COLUMNID columnidgrbit;
      JET_COLUMNID columnidDefault;
      JET_COLUMNID columnidBaseTableName;
      JET_COLUMNID columnidBaseColumnName;
      JET_COLUMNID columnidDefinitionName;
    } JET_COLUMNLIST;
```

### <a name="members"></a>Элементы

**кбструкт**

Размер структуры в байтах. Вызов API обновит это поле, поэтому вызывающий должен убедиться, что это значение соответствует sizeof (JET_COLUMNLIST).

**TableID**

Идентификатор созданной временной таблицы. За закрытие таблицы отвечает вызывающий объект.

**крекорд**

Количество записей во временной таблице, созданных вызовом API.

**колумнидпресентатионордер**

Идентификатор столбца для порядка представления.

Порядок представления используется для сортировки строк временной таблицы. Порядок представления является фиксированным [JET_coltypLong](./jet-coltyp.md). Если указанный уровень информации не является компактным, он также помечается как JET_bitColumnTTKey.

**колумнидколумннаме**

Идентификатор столбца имени столбца.

Если указанный уровень информации не является компактным, он также помечается как JET_bitColumnTTKey.

**колумнидколумнид**

Идентификатор столбца идентификатора столбца.

Идентификатор столбца является фиксированным [JET_coltypLong](./jet-coltyp.md).

**колумнидколтип**

Идентификатор столбца типа.

Тип столбца является фиксированным [JET_coltypLong](./jet-coltyp.md).

**колумнидкаунтри**

Идентификатор столбца кода страны.

Код страны является фиксированной [JET_coltypShort](./jet-coltyp.md).

**колумнидлангид**

Идентификатор столбца идентификатора языка.

Идентификатор языка является фиксированным [JET_coltypShort](./jet-coltyp.md).

**колумнидкп**

Идентификатор столбца кодовой страницы.

Кодовая страница является фиксированной [JET_coltypShort](./jet-coltyp.md).

**колумнидколлате**

Идентификатор столбца для последовательности параметров сортировки.

Последовательность параметров сортировки является фиксированной [JET_coltypShort](./jet-coltyp.md).

**колумнидкбмакс**

Идентификатор столбца поля **кбмакс** .

**Кбмакс** является фиксированной [JET_coltypLong](./jet-coltyp.md).

**колумнидгрбит**

Идентификатор столбца *грбитс* столбца. Поле *грбит* является фиксированной [JET_coltypLong](./jet-coltyp.md). Дополнительные сведения об этих битах см. в разделе [JET_COLUMNDEF](./jet-columndef-structure.md).

Ниже приведены возможные значения для **колумнидгрбит**.

JET_bitColumnTagged

JET_bitColumnFixed

JET_bitColumnUpdatable

JET_bitColumnNotNULL

JET_bitColumnAutoincrement

JET_bitColumnVersion

JET_bitColumnMultiValued

JET_bitColumnEscrowUpdate

JET_bitColumnFinalize

JET_bitColumnDeleteOnZero

JET_bitColumnUserDefinedDefault

**колумниддефаулт**

Идентификатор столбца значения по умолчанию для столбца.

Значение по умолчанию — [JET_coltypLongBinary](./jet-coltyp.md).

**колумнидбасетабленаме**

Идентификатор столбца имени таблицы, из которой была получена таблица.

Имя таблицы является [JET_coltypTextом](./jet-coltyp.md).

**колумнидбасеколумннаме**

Идентификатор столбца имени столбца, из которого был получен столбец.

Имя столбца является [JET_coltypTextом](./jet-coltyp.md).

**колумниддефинитионнаме**

Идентификатор столбца имени определения столбца.

Имя определения столбца является [JET_coltypTextом](./jet-coltyp.md).

### <a name="remarks"></a>Комментарии

По умолчанию порядок строк во временной таблице сортируется по имени столбца. Его также можно отсортировать по идентификатору столбца. Дополнительные сведения о сортировке по идентификатору столбца см. в разделе [жетжетколумнинфо](./jetgetcolumninfo-function.md) и [жетжеттаблеколумнинфо](./jetgettablecolumninfo-function.md).

Вызов [жетжетколумнинфо](./jetgetcolumninfo-function.md) или [жетжеттаблеколумнинфо](./jetgettablecolumninfo-function.md) может указывать компактную форму результатов. Если какие-либо столбцы были унаследованы из таблицы шаблонов, в результате сжатия не будут сохранены.

### <a name="requirements"></a>Требования


| Требование | Применение |
|------------|----------|
| <p><strong>Клиент</strong></p> | <p>требуется Windows Vista, Windows XP или Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>требуется Windows server 2008, Windows server 2003 или сервер Windows 2000.</p> | 
| <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | 



### <a name="see-also"></a>См. также:

[JET_COLTYP](./jet-coltyp.md)

[JET_COLUMNDEF](./jet-columndef-structure.md)

[JET_COLUMNID](./jet-columnid.md)

[JET_ERR](./jet-err.md)

[JET_GRBIT](./jet-grbit.md)

[JET_SESID](./jet-sesid.md)

[JET_TABLEID](./jet-tableid.md)

[жетжетколумнинфо](./jetgetcolumninfo-function.md)

[жетжеттаблеколумнинфо](./jetgettablecolumninfo-function.md)
