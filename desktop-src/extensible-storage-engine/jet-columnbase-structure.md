---
description: 'Дополнительные сведения: структура JET_COLUMNBASE'
title: Структура JET_COLUMNBASE
TOCTitle: JET_COLUMNBASE Structure
ms:assetid: 171275c3-966d-409d-ad20-a8f240f7500d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269194(v=EXCHG.10)
ms:contentKeyID: 32765497
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
ms.openlocfilehash: 603025166eed7c92d98148a43d26046308235777
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983597"
---
# <a name="jet_columnbase-structure"></a>Структура JET_COLUMNBASE


_**Применимо к:** Windows | Windows Сервером_

## <a name="jet_columnbase-structure"></a>Структура JET_COLUMNBASE

Структура **JET_COLUMNBASE** описывает параметры базового столбца. Функции [жетжетколумнинфо](./jetgetcolumninfo-function.md) и [жетжеттаблеколумнинфо](./jetgettablecolumninfo-function.md) используют структуру **JET_COLUMNBASE** .

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_COLUMNID columnid;
      JET_COLTYP coltyp;
      unsigned short wCountry;
      unsigned short langid;
      unsigned short cp;
      unsigned short wFiller;
      unsigned long cbMax;
      JET_GRBIT grbit;
      tchar szBaseTableName[256];
      tchar szBaseColumnName[256];
    } JET_COLUMNBASE;
```

### <a name="members"></a>Элементы

**кбструкт**

Размер этой структуры в байтах. Задайте для **кбструкт** значение sizeof (JET_COLUMNBASE).

**columnid**

Зарезервировано. Установите значение **columnid** равным 0 (нулю).

**колтип**

Тип столбца (например, текст, двоичный или числовой). Дополнительные сведения см. в разделе [JET_COLTYP](./jet-coltyp.md).

**вкаунтри**

Зарезервировано. Задайте значение 0 (ноль).

**langid**

Зарезервировано. Задайте значение 0 (ноль).

**cp**

Кодовая страница для столбца. Единственными допустимыми значениями для текстовых столбцов являются английский (1252) и Unicode (1200). Нулевое значение означает, что будет использоваться по умолчанию (английский, 1252). Если столбец не является текстовым столбцом, кодовая страница автоматически устанавливается в нулевое значение.

**вфиллер**

Зарезервировано. Задайте значение 0 (ноль).

**кбмакс**

Максимальная длина (в байтах) столбца переменной длины или фактической длины в байтах для столбца фиксированной длины.

**грбит**

Параметры для столбца, включая ноль или более следующих значений.


| <p>Значение</p> | <p>Значение</p> | 
|--------------|----------------|
| <p>JET_bitColumnFixed</p> | <p>Столбец является фиксированным и занимает один и тот же объем пространства в строке независимо от объема содержащихся в ней данных. JET_bitColumnFixed нельзя сочетать с JET_bitColumnTagged и не может использоваться, если для элемента <strong>колтип</strong> задано значение <strong>JET_coltypLongText</strong> или <strong>JET_coltypLongBinary</strong>.</p> | 
| <p>JET_bitColumnTagged</p> | <p>Столбец помечается и занимает место в базе данных только в том случае, если содержит данные. JET_bitColumnTagged нельзя сочетать с JET_bitColumnFixed, JET_bitColumnVersion или JET_bitColumnEscrowUpdate.</p> | 
| <p>JET_bitColumnNotNULL</p> | <p>Для этого столбца не должно быть задано значение <strong>null</strong> .</p><p>JET_bitColumnNotNULL нельзя сочетать с JET_bitColumnUserDefinedDefault.</p> | 
| <p>JET_bitColumnVersion</p> | <p>Столбец представляет собой столбец версии, указывающий версию строки. Значение этого столбца начинается с нуля и автоматически увеличивается на единицу при каждом обновлении строки.</p><p>JET_bitColumnVersion можно использовать только в том случае, если элемент <strong>колтип</strong> имеет значение <strong>JET_coltypLong</strong> и не может сочетаться с JET_bitColumnAutoincrement, JET_bitColumnEscrowUpdate, JET_bitColumnTagged или JET_bitColumnUserDefinedDefault.</p> | 
| <p>JET_bitColumnAutoincrement</p> | <p>Столбец автоматически увеличивается. Число является увеличивающимся числом и гарантированно уникально в пределах таблицы. Однако числа могут не быть последовательными. Например, если в таблицу вставляются пять строк, то автоматически увеличивающийся столбец может содержать значения {1, 2, 6, 7, 8}.</p><p>JET_bitColumnAutoincrement можно использовать только в том случае, если элемент <strong>колтип</strong> имеет значение <strong>JET_coltypLong</strong> или <strong>JET_coltypCurrency</strong> и не может сочетаться с JET_bitColumnEscrowUpdate, JET_bitColumnUserDefinedDefault или JET_bitColumnVersion.</p><p><strong>Windows 2000:</strong> JET_bitColumnVersion можно использовать, только если для элемента <strong>колтип</strong> задано значение <strong>JET_coltypLong</strong>.</p> | 
| <p>JET_bitColumnUpdatable</p> | <p>Допустимо только для вызовов <a href="gg269215(v=exchg.10).md">жетжетколумнинфо</a>. JET_bitColumnUpdatable нельзя сочетать с JET_bitColumnUserDefinedDefault.</p> | 
| <p>JET_bitColumnTTKey</p> | <p>Допускается только для вызовов <a href="gg294118(v=exchg.10).md">жетопентабле</a>.</p> | 
| <p>JET_bitColumnTTDescending</p> | <p>Допускается только для вызовов <a href="gg269211(v=exchg.10).md">жетопентемптабле</a>.</p> | 
| <p>JET_bitColumnMultiValued</p> | <p>Столбец может иметь несколько значений. Столбец с несколькими значениями может иметь ноль, одно или несколько связанных с ним значений. Различные значения в столбце с несколькими значениями идентифицируются по числу в элементе <strong>итагсекуенце</strong> различных структур, например <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>, <a href="gg294090(v=exchg.10).md">JET_SETINFO</a>, <a href="gg269233(v=exchg.10).md">JET_SETCOLUMN</a>, <a href="gg269334(v=exchg.10).md">JET_RETRIEVECOLUMN</a>, <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>. Столбцы с несколькими значениями должны быть помечены как столбцы. Это значит, что они не могут быть столбцами фиксированной или переменной длины.</p> | 
| <p>JET_bitColumnEscrowUpdate</p> | <p>Указывает, что столбец является столбцом депонированного обновления, который может обновляться параллельно различными сеансами с <a href="gg294125(v=exchg.10).md">жетескровупдате</a> и будет иметь согласованность транзакций.</p><ul><li><p>Столбец депонированного обновления может быть создан только в том случае, если таблица пуста.</p></li></ul><ul><li><p>Для столбца депонированного обновления элемент <strong>колтип</strong> должен иметь значение <strong>JET_coltypLong.</strong></p></li></ul><ul><li><p>Столбец депонированного обновления должен иметь значение по умолчанию ( <strong>кбдефаулт</strong> должно быть положительным).</p></li></ul><ul><li><p>JET_bitColumnEscrowUpdate нельзя сочетать с JET_bitColumnTagged, JET_bitColumnVersion или JET_bitColumnAutoincrement.</p></li></ul> | 
| <p>JET_bitColumnUnversioned</p> | <p>Столбец создается без номера версии. Это означает, что другие транзакции, пытающиеся добавить столбец с тем же именем, завершатся ошибкой. JET_bitColumnUnversioned используется только с <a href="gg294122(v=exchg.10).md">жетаддколумн</a>. Его нельзя использовать в транзакции.</p> | 
| <p>JET_bitColumnMaybeNull</p> | <p>Зарезервировано для последующего использования.</p><p>JET_bitColumnMaybeNull нельзя сочетать с JET_bitColumnUserDefinedDefault.</p> | 
| <p>JET_bitColumnFinalize</p> | <p>Не используйте. Вместо этого используйте JET_bitColumnDeleteOnZero.</p><p>Столбец может быть завершен. Столбец, который может быть завершен, — это столбец депонированного обновления, который приводит к удалению строки, когда столбец достигает нуля. В будущих версиях вместо этого могут вызываться функции обратного вызова (см. <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>). Столбец, который может быть завершен, должен быть столбцом типа "условно Update". JET_bitColumnFinalize нельзя сочетать с JET_bitColumnUserDefinedDefault.</p> | 
| <p>JET_bitColumnUserDefinedDefault</p> | <p>Значение по умолчанию для столбца будет предоставлено функцией обратного вызова. См. <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>. Столбец, содержащий определяемое пользователем значение по умолчанию, должен быть столбцом с тегами. Если указано JET_bitColumnUserDefinedDefault, <strong>пвдефаулт</strong> должен указывать на структуру <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> , а для <strong>кбдефаулт</strong> должно быть задано значение sizeof (JET_USERDEFINEDDEFAULT).</p><p>JET_bitColumnUserDefinedDefault не могут сочетаться с JET_bitColumnFixed, JET_bitColumnNotNULL, JET_bitColumnVersion, JET_bitColumnAutoincrement, JET_bitColumnUpdatable, JET_bitColumnEscrowUpdate, JET_bitColumnFinalize, JET_bitColumnDeleteOnZero или JET_bitColumnMaybeNull.</p> | 
| <p>JET_bitColumnDeleteOnZero</p> | <p>Столбец является столбцом депонированного обновления, и когда он достигает нуля, запись будет удалена. Как правило, при удалении столбцов с удалением на нуль используются поля счетчика ссылок. Когда число ссылок становится равным нулю, запись удаляется. Столбец Deleted-on-Zero должен быть столбцом депонированного обновления.</p><p>JET_bitColumnDeleteOnZero заменяет JET_bitColumnFinalize.</p><p>JET_bitColumnDeleteOnZero нельзя сочетать с JET_bitColumnFinalize или JET_bitColumnUserDefinedDefault и не может использоваться с пользовательскими столбцами по умолчанию.</p> | 



**сзбасетабленаме**

Таблица, из которой текущая таблица наследует свою DDL.

**сзбасеколумннаме**

Имя столбца в таблице шаблонов.

### <a name="remarks"></a>Комментарии

**JET_COLUMNBASE** содержит большую часть тех же сведений, что и [JET_COLUMNDEF](./jet-columndef-structure.md), но добавляет строковые поля для описания базовой таблицы (если использовалась иерархическая DDL).

### <a name="requirements"></a>Требования


| Требование | Применение |
|------------|----------|
| <p><strong>Клиент</strong></p> | <p>требуется Windows Vista, Windows XP или Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>требуется Windows server 2008, Windows server 2003 или сервер Windows 2000.</p> | 
| <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | 
| <p><strong>Юникод</strong></p> | <p>Реализуется как <strong>JET_COLUMNBASE_W</strong> (Юникод) и <strong>JET_COLUMNBASE_A</strong> (ANSI).</p> | 



### <a name="see-also"></a>См. также:

[JET_CALLBACK](./jet-callback-callback-function.md)  
[JET_COLTYP](./jet-coltyp.md)  
[JET_COLUMNDEF](./jet-columndef-structure.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_USERDEFINEDDEFAULT](./jet-userdefineddefault-structure.md)  
[жетжетколумнинфо](./jetgetcolumninfo-function.md)  
[жетжеттаблеколумнинфо](./jetgettablecolumninfo-function.md)  
[жетренамеколумн](./jetrenamecolumn-function.md)
