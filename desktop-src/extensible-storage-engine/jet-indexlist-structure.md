---
description: 'Дополнительные сведения: структура JET_INDEXLIST'
title: Структура JET_INDEXLIST
TOCTitle: JET_INDEXLIST Structure
ms:assetid: 0c092b48-e583-49f3-8f5e-1428a84d9265
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269185(v=EXCHG.10)
ms:contentKeyID: 32765488
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
ms.openlocfilehash: c57fda6eaea161839cdaa758c41f13749d4c5eda
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480050"
---
# <a name="jet_indexlist-structure"></a>Структура JET_INDEXLIST


_**Применимо к:** Windows | Windows Сервером_

## <a name="jet_indexlist-structure"></a>Структура JET_INDEXLIST

Структура **JET_INDEXLIST** содержит необходимые сведения для прохода по временной таблице, созданной функциями [жетжетиндексинфо](./jetgetindexinfo-function.md) или [жетжеттаблеиндексинфо](./jetgettableindexinfo-function.md) . Каждая строка во временной таблице описывает столбец индекса.

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_TABLEID tableid;
      gned long cRecord;
      JET_COLUMNID columnidindexname;
      JET_COLUMNID columnidgrbitIndex;
      JET_COLUMNID columnidcKey;
      JET_COLUMNID columnidcEntry;
      JET_COLUMNID columnidcPage;
      JET_COLUMNID columnidcColumn;
      JET_COLUMNID columnidiColumn;
      JET_COLUMNID columnidcolumnid;
      JET_COLUMNID columnidcoltyp;
      JET_COLUMNID columnidCountry;
      JET_COLUMNID columnidLangid;
      JET_COLUMNID columnidCp;
      JET_COLUMNID columnidCollate;
      JET_COLUMNID columnidgrbitColumn;
      JET_COLUMNID columnidcolumnname;
      JET_COLUMNID columnidLCMapFlags;
    } JET_INDEXLIST;
```

### <a name="members"></a>Элементы

**кбструкт**

Размер структуры в байтах. Вызов API обновит это поле, поэтому вызывающий должен убедиться, что это значение соответствует sizeof (JET_INDEXLIST).

**TableID**

Идентификатор созданной временной таблицы. За закрытие таблицы отвечает вызывающий объект.

**крекорд**

Количество записей во временной таблице, которые были созданы.

**колумнидиндекснаме**

Идентификатор столбца имени индекса.

Этот столбец является [JET_coltypTextом](./jet-coltyp.md).

**колумнидгрбитиндекс**

Идентификатор столбца *грбитс* , используемого в индексе. Список допустимых битов см. в разделе [JET_INDEXCREATE](./jet-indexcreate-structure.md) .

Этот столбец является [JET_coltypLongом](./jet-coltyp.md).

**колумнидккэй**

Идентификатор столбца количества ключей в индексе.

Этот столбец является [JET_coltypLongом](./jet-coltyp.md).

**колумнидцентри**

Идентификатор столбца количества записей в индексе.

Этот столбец является [JET_coltypLongом](./jet-coltyp.md).

**колумнидкпаже**

Идентификатор столбца количества страниц, используемых индексом. Этот столбец является [JET_coltypLongом](./jet-coltyp.md).

**колумнидкколумн**

Идентификатор столбца общего числа столбцов, охватываемых индексом.

Этот столбец является [JET_coltypLongом](./jet-coltyp.md).

**колумнидиколумн**

Идентификатор столбца для номера столбца в индексе. Дополнительные сведения см. в подразделе «Примечания» этого раздела.

Этот столбец является [JET_coltypLongом](./jet-coltyp.md).


| <p>Значение</p> | <p>Значение</p> | 
|--------------|----------------|
| <p>Циндексинфоколс<br />15</p> | <p>Указывает, что разрешены 15 столбцов.</p> | 
| <p>кколумнинфоколс<br />14</p> | <p>Указывает, что разрешены 14 столбцов.</p> | 
| <p>кобжектинфоколс<br />9</p> | <p>Указывает, что разрешены 9 столбцов.</p> | 



**колумнидколумнид**

Идентификатор столбца индексируемого столбца. Дополнительные сведения см. в подразделе «Примечания» этого раздела. Этот столбец является [JET_coltypLongом](./jet-coltyp.md).

**колумнидколтип**

Идентификатор столбца колтип индексируемого столбца. Дополнительные сведения см. в подразделе «Примечания» этого раздела. Этот столбец является [JET_coltypLongом](./jet-coltyp.md).

**колумнидкаунтри**

Идентификатор столбца с кодом страны индексируемого столбца. Код страны является устаревшим.

Этот столбец является [JET_coltypShortом](./jet-coltyp.md).

**колумнидлангид**

Идентификатор столбца идентификатора языка (LCID), в котором был создан индекс. Дополнительные сведения см. в разделе [JET_INDEXCREATE](./jet-indexcreate-structure.md).

Этот столбец является [JET_coltypShortом](./jet-coltyp.md).

**колумнидкп**

Идентификатор столбца кодовой страницы, под которой был создан индекс. Дополнительные сведения см. в разделе [JET_COLUMNCREATE](./jet-columncreate-structure.md).

Этот столбец является [JET_coltypShortом](./jet-coltyp.md).

**колумнидколлате**

Идентификатор столбца для последовательности параметров сортировки, в которой был создан индекс. Последовательность параметров сортировки является устаревшей.

Этот столбец является [JET_coltypShortом](./jet-coltyp.md).

**колумнидгрбитколумн**

Идентификатор столбца *грбитс* , который применяется к порядку столбца в индексе.

Данные для этого столбца можно упорядочить как JET_bitKeyAscending или JET_bitKeyDescending. Этот столбец является [JET_coltypLongом](./jet-coltyp.md). Например, индекс, определенный как "-Столбец1 \\ 0 + Столбец2 \\ 0", будет иметь JET_bitKeyDescending "Столбец1" и JET_bitKeyAscending "Столбец2".

Для этого элемента допустимы следующие параметры.


| <p>Значение</p> | <p>Значение</p> | 
|--------------|----------------|
| <p>JET_bitKeyAscending</p> | <p>Сегмент индекса в возрастающем порядке.</p> | 
| <p>JET_bitKeyDescending</p> | <p>Сегмент индекса в порядке убывания.</p> | 



**колумнидколумннаме**

Идентификатор столбца имени столбца.

Этот столбец является [JET_coltypTextом](./jet-coltyp.md).

**колумнидлкмапфлагс**

Идентификатор столбца флагов, которые используются для создания индекса. Дополнительные сведения см. в разделе **двмапфлагс** статьи [JET_UNICODEINDEX](./jet-unicodeindex-structure.md).

Этот столбец является [JET_coltypLongом](./jet-coltyp.md).

### <a name="remarks"></a>Комментарии

Каждая строка во временной таблице соответствует столбцу в определенном индексе.

Например, индекс "+ A \\ 0 + B 0 + \\ C 0 + \\ D 0 + \\ E \\ 0" больше пяти столбцов, и он займет пять строк во временной таблице. Каждая из этих пяти строк будет иметь значение 5 в столбце, идентифицируемом по столбцу columnid. Однако каждая строка будет иметь разное значение для столбца columnid, в диапазоне от 0 до 4.

Число ключей в определенном индексе соответствует числу уникальных значений, для которых вызывающий может выполнить поиск и получить точное соответствие. Число записей — это количество строк, совпадающих с индексом. Если индекс имеет ограничение уникальности, число ключей равно числу записей. Например, если таблица содержит следующие сведения и индекс создается для столбца с именем "ключ", то существует три ключа (100, 200 и 500), но есть четыре записи ("this", "-", "a" и "example").


| <p>Клавиши</p> | <p>Ввод</p> | 
|------------|--------------|
| <p>100</p> | <p>настоящего</p> | 
| <p>100</p> | <p>рекомендуется</p> | 
| <p>200</p> | <p>ранне</p> | 
| <p>500</p> | <p>Например</p> | 



### <a name="requirements"></a>Требования


| | | <p><strong>Клиент</strong></p> | <p>требуется Windows Vista, Windows XP или Windows 2000 Professional.</p> | | <p><strong>Сервер</strong></p> | <p>требуется Windows server 2008, Windows server 2003 или сервер Windows 2000.</p> | | <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | 



### <a name="see-also"></a>См. также:

[JET_COLTYP](./jet-coltyp.md)  
[JET_COLUMNCREATE](./jet-columncreate-structure.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_UNICODEINDEX](./jet-unicodeindex-structure.md)  
[жетжетиндексинфо](./jetgetindexinfo-function.md)  
[жетжеттаблеиндексинфо](./jetgettableindexinfo-function.md)
