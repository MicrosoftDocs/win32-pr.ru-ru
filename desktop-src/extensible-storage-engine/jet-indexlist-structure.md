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
ms.openlocfilehash: a696d1c52a42cad2b3b67b047984b48d77637a1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346995"
---
# <a name="jet_indexlist-structure"></a>Структура JET_INDEXLIST


_**Применимо к:** Windows | Windows Server_

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
<td><p>Циндексинфоколс<br />
15</p></td>
<td><p>Указывает, что разрешены 15 столбцов.</p></td>
</tr>
<tr class="even">
<td><p>кколумнинфоколс<br />
14</p></td>
<td><p>Указывает, что разрешены 14 столбцов.</p></td>
</tr>
<tr class="odd">
<td><p>кобжектинфоколс<br />
9</p></td>
<td><p>Указывает, что разрешены 9 столбцов.</p></td>
</tr>
</tbody>
</table>


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
<td><p>JET_bitKeyAscending</p></td>
<td><p>Сегмент индекса в возрастающем порядке.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitKeyDescending</p></td>
<td><p>Сегмент индекса в порядке убывания.</p></td>
</tr>
</tbody>
</table>


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

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Ключ</p></th>
<th><p>Ввод</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>100</p></td>
<td><p>&quot;this&quot;</p></td>
</tr>
<tr class="even">
<td><p>100</p></td>
<td><p>&quot;is&quot;</p></td>
</tr>
<tr class="odd">
<td><p>200</p></td>
<td><p>&quot;ранне&quot;</p></td>
</tr>
<tr class="even">
<td><p>500</p></td>
<td><p>&quot;example&quot;</p></td>
</tr>
</tbody>
</table>


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
