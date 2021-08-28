---
description: 'Дополнительные сведения: структура JET_COLUMNDEF'
title: Структура JET_COLUMNDEF
TOCTitle: JET_COLUMNDEF Structure
ms:assetid: ee1fc473-bff5-438e-98ae-247de12e76f9
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294130(v=EXCHG.10)
ms:contentKeyID: 32765744
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
ms.openlocfilehash: fccf3b076b71e8923366a95810d1f3009d4fe1c4
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471140"
---
# <a name="jet_columndef-structure"></a>Структура JET_COLUMNDEF


_**Применимо к:** Windows | Windows Сервером_

## <a name="jet_columndef-structure"></a>Структура JET_COLUMNDEF

Структура **JET_COLUMNDEF** определяет данные, которые могут храниться в столбце.

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_COLUMNID columnid;
      JET_COLTYP coltyp;
      unsigned short wCountry;
      unsigned short langid;
      unsigned short cp;
      unsigned short wCollate;
      unsigned long cbMax;
      JET_GRBIT grbit;
    } JET_COLUMNDEF;
```

### <a name="members"></a>Элементы

**кбструкт**

Размер структуры в байтах. Он должен иметь значение sizeof (JET_COLUMNDEF).

**columnid**

Зарезервировано. значение **columnid** должно быть равно 0 (нулю).

**колтип**

Тип столбца (например, текст, двоичный или числовой). Дополнительные сведения см. в разделе [JET_COLTYP](./jet-coltyp.md).

**вкаунтри**

Зарезервировано. **вкаунтри** должно иметь значение 0 (ноль).

**langid**

Является устаревшей. значение **LangID** должно быть равно 0 (нулю).

**cp**

Кодовая страница для столбца. Единственными допустимыми значениями для текстовых столбцов являются английский (1252) и Unicode (1200). Нулевое значение означает, что будет использоваться по умолчанию (английский, 1252). Если столбец не является текстовым столбцом, кодовая страница автоматически получает значение 0.

**вколлате**

Зарезервировано. **вколлате** должно иметь значение 0 (ноль).

**кбмакс**

Максимальная длина (в байтах) столбца переменной длины или длина столбца фиксированной длины.

**грбит**

Группа битов, содержащая параметры, которые должны использоваться для этого вызова, включая ноль или более следующих значений.


| <p>Значение</p> | <p>Значение</p> | 
|--------------|----------------|
| <p>JET_bitColumnFixed</p> | <p>Столбец будет исправлен. Он всегда будет использовать один и тот же объем пространства в строке независимо от объема данных, сохраняемых в столбце. JET_bitColumnFixed нельзя использовать с JET_bitColumnTagged. Этот бит не может использоваться с длинными значениями ( <strong>JET_coltypLongText</strong> и <strong>JET_coltypLongBinary</strong>).</p> | 
| <p>JET_bitColumnTagged</p> | <p>Столбец будет помечен как. Помеченные столбцы не занимают место в базе данных, если они не содержат данных. Этот бит не может использоваться с JET_bitColumnFixed.</p> | 
| <p>JET_bitColumnNotNULL</p> | <p>Для этого столбца никогда не должно быть задано значение NULL.</p> | 
| <p>JET_bitColumnVersion</p> | <p>Столбец представляет собой столбец версии, указывающий версию строки. Значение этого столбца начинается с нуля и будет автоматически увеличиваться для каждого обновления в строке.</p><p>Этот бит можно применить только к <strong>JET_coltypLong</strong> столбцам. Этот бит не может использоваться с JET_bitColumnAutoincrement, JET_bitColumnEscrowUpdate или JET_bitColumnTagged.</p> | 
| <p>JET_bitColumnAutoincrement</p> | <p>Столбец будет автоматически увеличиваться. Число является увеличивающимся числом и гарантированно уникально в пределах таблицы. Однако числа могут не быть непрерывными. Например, если в таблицу вставляются пять строк, столбец «AutoIncrement» может содержать значения {1, 2, 6, 7, 8}. Этот бит можно использовать только для столбцов типа <strong>JET_coltypLong</strong> или <strong>JET_coltypCurrency</strong>.</p><p><strong>Windows 2000:</strong> в Windows 2000 этот бит можно использовать только для столбцов типа <strong>JET_coltypLong</strong>.</p> | 
| <p>JET_bitColumnUpdatable</p> | <p>Этот бит допустим только для вызовов <a href="gg269215(v=exchg.10).md">жетжетколумнинфо</a>.</p> | 
| <p>JET_bitColumnTTKey</p> | <p>Этот бит допустим только для вызовов <a href="gg294118(v=exchg.10).md">жетопентабле</a>.</p> | 
| <p>JET_bitColumnTTDescending</p> | <p>Этот бит допустим только для вызовов <a href="gg269211(v=exchg.10).md">жетопентемптабле</a>.</p> | 
| <p>JET_bitColumnMultiValued</p> | <p>Столбец может иметь несколько значений. Столбец с несколькими значениями может иметь ноль, одно или несколько связанных с ним значений. Различные значения в столбце с несколькими значениями идентифицируются по числу, называемому элементом <strong>итагсекуенце</strong> , который относится к различным структурам, включая: <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>, <a href="gg294090(v=exchg.10).md">JET_SETINFO</a>, <a href="gg269233(v=exchg.10).md">JET_SETCOLUMN</a>, <a href="gg269334(v=exchg.10).md">JET_RETRIEVECOLUMN</a>и <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>. Столбцы с несколькими значениями должны быть помечены как столбцы. Это значит, что они не могут быть столбцами фиксированной длины или переменной длины.</p> | 
| <p>JET_bitColumnEscrowUpdate</p> | <p>Указывает, что столбец является столбцом депонирования обновлений. Столбец депонированного обновления может обновляться параллельно разными сеансами с <a href="gg294125(v=exchg.10).md">жетескровупдате</a> и поддерживать согласованность транзакций. Столбец депонированного обновления также должен соответствовать следующим условиям.</p><ul><li><p>Столбец депонированного обновления может быть создан только в том случае, если таблица пуста.</p></li></ul><ul><li><p>Столбец депонированного обновления должен иметь тип <strong>JET_coltypLong</strong>.</p></li></ul><ul><li><p>Столбец депонированного обновления должен иметь значение по умолчанию ( <strong>кбдефаулт</strong> должно быть положительным).</p></li></ul><ul><li><p>JET_bitColumnEscrowUpdate нельзя использовать в сочетании с JET_bitColumnTagged, JET_bitColumnVersion или JET_bitColumnAutoincrement.</p></li></ul> | 
| <p>JET_bitColumnUnversioned</p> | <p>Столбец будет создан в без сведений о версии. Это означает, что другие транзакции, пытающиеся добавить столбец с тем же именем, завершатся ошибкой. Этот бит удобен только для <a href="gg294122(v=exchg.10).md">жетаддколумн</a>. Его нельзя использовать в транзакции.</p> | 
| <p>JET_bitColumnMaybeNull</p> | <p>Зарезервировано для последующего использования.</p> | 
| <p>JET_bitColumnFinalize</p> | <p>Вместо JET_bitColumnFinalize используйте JET_bitColumnDeleteOnZero. JET_bitColumnFinalize, что столбец может быть завершен. Если столбец, который может быть завершен, имеет столбец депонированного обновления, который достигает нуля, строка будет удалена. В будущих версиях вместо этого могут вызываться функции обратного вызова (Дополнительные сведения см. в разделе <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>). Столбец, который может быть завершен, должен быть столбцом типа "условно Update". JET_bitColumnFinalize нельзя использовать с JET_bitColumnUserDefinedDefault.</p> | 
| <p>JET_bitColumnUserDefinedDefault</p> | <p>Значение по умолчанию для столбца будет предоставлено функцией обратного вызова. См. <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>. Столбец, содержащий определяемое пользователем значение по умолчанию, должен быть столбцом с тегами. Указание JET_bitColumnUserDefinedDefault означает, что <strong>пвдефаулт</strong> должен указывать на структуру <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> , а для <strong>кбдефаулт</strong> должно быть задано значение sizeof ( <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> ).</p><ul><li><p>JET_bitColumnUserDefinedDefault нельзя использовать в сочетании с JET_bitColumnFixed, JET_bitColumnNotNULL, JET_bitColumnVersion, JET_bitColumnAutoincrement, JET_bitColumnUpdatable, JET_bitColumnEscrowUpdate, JET_bitColumnFinalize, JET_bitColumnDeleteOnZero или JET_bitColumnMaybeNull.</p></li></ul> | 
| <p>JET_bitColumnDeleteOnZero</p> | <p>Столбец является столбцом депонированного обновления, и когда он достигает нуля, запись будет удалена. Обычно для столбца, который может быть завершен, можно использовать его как поле счетчика ссылок, а когда поле достигает нуля, запись удаляется. JET_bitColumnDeleteOnZero связана с JET_bitColumnFinalize. Столбец Deleted-on-Zero должен быть столбцом депонированного обновления. JET_bitColumnDeleteOnZero нельзя использовать с JET_bitColumnFinalize. JET_bitColumnDeleteOnZero нельзя использовать с пользовательскими столбцами по умолчанию.</p> | 



### <a name="requirements"></a>Требования


| | | <p><strong>Клиент</strong></p> | <p>требуется Windows Vista, Windows XP или Windows 2000 Professional.</p> | | <p><strong>Сервер</strong></p> | <p>требуется Windows server 2008, Windows server 2003 или сервер Windows 2000.</p> | | <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | 



### <a name="see-also"></a>См. также:

[JET_CALLBACK](./jet-callback-callback-function.md)  
[JET_COLTYP](./jet-coltyp.md)  
[JET_COLUMNCREATE](./jet-columncreate-structure.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_USERDEFINEDDEFAULT](./jet-userdefineddefault-structure.md)  
[жетаддколумн](./jetaddcolumn-function.md)  
[жетескровупдате](./jetescrowupdate-function.md)  
[жетжеттаблеколумнинфо](./jetgettablecolumninfo-function.md)  
[жетопентемптабле](./jetopentemptable-function.md)  
[JetOpenTempTable2](./jetopentemptable2-function.md)  
[JetOpenTempTable3](./jetopentemptable3-function.md)  
[жетренамеколумн](./jetrenamecolumn-function.md)
