---
description: 'Дополнительные сведения: структура JET_COLUMNCREATE'
title: Структура JET_COLUMNCREATE
TOCTitle: JET_COLUMNCREATE Structure
ms:assetid: 553263a9-7d2c-4bd7-ad77-1dfb6d21ef2c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269252(v=EXCHG.10)
ms:contentKeyID: 32765554
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
ms.openlocfilehash: ffe79dde0f24e82aa7ca9457604ea76b587e9b29
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984027"
---
# <a name="jet_columncreate-structure"></a>Структура JET_COLUMNCREATE


_**Применимо к:** Windows | Windows Сервером_

## <a name="jet_columncreate-structure"></a>Структура JET_COLUMNCREATE

Структура **JET_COLUMNCREATE** описывает столбец, который создается в базе данных.

```cpp
    typedef struct tag_JET_COLUMNCREATE {
      unsigned long cbStruct;
      tchar* szColumnName;
      JET_COLTYP coltyp;
      unsigned long cbMax;
      JET_GRBIT grbit;
      void* pvDefault;
      unsigned long cbDefault;
      unsigned long cp;
      JET_COLUMNID columnid;
      JET_ERR err;
    } JET_COLUMNCREATE;
```

### <a name="members"></a>Элементы

**кбструкт**

Размер структуры в байтах. Это поле должно быть инициализировано в **sizeof (JET_COLUMNCREATE)**.

**сзколумннаме**

Имя создаваемого столбца. Имя должно соответствовать следующим критериям:

  - Длина должна быть меньше JET_cbNameMost символов, не включая завершающее значение NULL.

<!-- end list -->

  - Он должен содержать только символы из следующих наборов: от 0 до 9, от A до Z, от a до z и всех остальных знаков препинания, за исключением восклицательного знака ( \! ), запятой (,), открывающей квадратной скобки ( \[ ) и закрывающей квадратной скобки ( \] ), т. е. символов ASCII 0x20, 0x22 до 0x7F.

<!-- end list -->

  - Оно не может начинаться с пробела.

<!-- end list -->

  - Он должен содержать по крайней мере один символ, не являющийся пробелом.

**колтип**

Тип столбца (например, текст, двоичный или числовой). Дополнительные сведения см. в разделе [JET_COLTYP](./jet-coltyp.md).

**кбмакс**

Максимальная длина (в байтах) столбца переменной длины. Длина столбца для столбцов фиксированной длины.

**грбит**

Группа битов, содержащая параметры для этой структуры, которые содержат ноль или более следующих значений.


| <p>Значение</p> | <p>Значение</p> | 
|--------------|----------------|
| <p>JET_bitColumnFixed</p> | <p>Столбец является фиксированным. Он всегда будет использовать один и тот же объем пространства в строке независимо от объема данных, сохраняемых в столбце. JET_bitColumnFixed нельзя использовать с JET_bitColumnTagged. Этот бит не может использоваться с длинными значениями, такими как <strong>JET_coltypLongText</strong> и <strong>JET_coltypLongBinary</strong>.</p> | 
| <p>JET_bitColumnTagged</p> | <p>Столбец помечен как тег. Помеченные столбцы не занимают место в базе данных, если они не содержат данных. Этот бит не может использоваться с JET_bitColumnFixed.</p> | 
| <p>JET_bitColumnNotNULL</p> | <p>Для этого столбца никогда не должно быть задано значение NULL.</p> | 
| <p>JET_bitColumnAutoincrement</p> | <p>Столбец автоматически увеличивается. Число является увеличивающимся числом и гарантированно уникально в пределах таблицы. Однако это число может не быть непрерывным. Например, если в таблицу вставляются пять строк, столбец AutoIncrement может содержать значения {1, 2, 6, 7, 8}.</p><p><strong>Windows 2000:</strong> Этот бит можно использовать только для столбцов типа <strong>JET_coltypLong</strong>.</p><p><strong>Windows Server 2003 и более поздних версий:</strong> Этот бит можно использовать только для столбцов типа <strong>JET_coltypLong</strong> или <strong>JET_coltypCurrency</strong>.</p> | 
| <p>JET_bitColumnUpdatable</p> | <p>Этот бит допустим только для вызовов <a href="gg269215(v=exchg.10).md">жетжетколумнинфо</a>.</p> | 
| <p>JET_bitColumnTTKey</p> | <p>Этот бит допустим только для вызовов <a href="gg269211(v=exchg.10).md">жетопентемптабле</a>.</p> | 
| <p>JET_bitColumnTTDescending</p> | <p>Этот бит допустим только для вызовов <a href="gg269211(v=exchg.10).md">жетопентемптабле</a>.</p> | 
| <p>JET_bitColumnMultiValued</p> | <p>Столбец может иметь несколько значений. Столбец с несколькими значениями может иметь ноль, одно или несколько связанных с ним значений. Различные значения в столбце с несколькими значениями определяются элементом <strong>итагсекуенце</strong> в различных структурах, например <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>, <a href="gg294090(v=exchg.10).md">JET_SETINFO</a>, <a href="gg269233(v=exchg.10).md">JET_SETCOLUMN</a>, <a href="gg269334(v=exchg.10).md">JET_RETRIEVECOLUMN</a>, <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>. Столбцы с несколькими значениями должны быть помечены как столбцы. Это значит, что они не могут быть столбцами фиксированной длины или переменной длины.</p> | 
| <p>JET_bitColumnEscrowUpdate</p> | <p>Столбец является столбцом депонированного обновления. Столбец депонированного обновления может обновляться параллельно разными сеансами с <a href="gg294125(v=exchg.10).md">жетескровупдате</a> и поддерживать согласованность транзакций.</p><ul><li><p>Столбец депонированного обновления может быть создан только в том случае, если таблица пуста.</p></li><li><p>Столбец депонированного обновления должен иметь тип <strong>JET_coltypLong.</strong></p></li><li><p>Столбец депонированного обновления должен иметь значение по умолчанию ( <strong>кбдефаулт</strong> должно быть положительным).</p></li><li><p>JET_bitColumnEscrowUpdate нельзя использовать в сочетании со следующими константами:</p><ul><li><p>JET_bitColumnTagged</p></li><li><p>JET_bitColumnVersion</p></li><li><p>JET_bitColumnAutoincrement</p></li></ul></li></ul> | 
| <p>JET_bitColumnUnversioned</p> | <p>Столбец создается без версии. Другие транзакции, пытающиеся добавить столбец с тем же именем, завершатся ошибкой. Этот бит удобен только для <a href="gg294122(v=exchg.10).md">жетаддколумн</a>. Его нельзя использовать в транзакции.</p> | 
| <p>JET_bitColumnMaybeNull</p> | <p>Зарезервировано для последующего использования.</p> | 
| <p>JET_bitColumnFinalize</p> | <p>Вместо JET_bitColumnFinalize используйте JET_bitColumnDeleteOnZero. JET_bitColumnFinalize указывает, что столбец может быть завершен. Если столбец, который может быть завершен, имеет столбец депонированного обновления, который достигает нуля, строка будет удалена. В будущих версиях вместо этого можно вызвать функцию обратного вызова. Дополнительные сведения см. в разделе <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>. Столбец, который может быть завершен, должен быть столбцом типа "условно Update". JET_bitColumnFinalize нельзя использовать с JET_bitColumnUserDefinedDefault.</p> | 
| <p>JET_bitColumnUserDefinedDefault</p> | <p>Значение по умолчанию для столбца предоставляется функцией обратного вызова <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>. Столбец, содержащий определяемое пользователем значение по умолчанию, должен быть столбцом с тегами. <strong>пвдефаулт</strong> должен указывать на структуру <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> , а для <strong>кбдефаулт</strong> должно быть задано значение sizeof (<a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a>).</p><p>JET_bitColumnUserDefinedDefault нельзя использовать в сочетании со следующими константами:</p><ul><li><p>JET_bitColumnFixed</p></li><li><p>JET_bitColumnNotNULL</p></li><li><p>JET_bitColumnVersion</p></li><li><p>JET_bitColumnAutoincrement</p></li><li><p>JET_bitColumnUpdatable</p></li><li><p>JET_bitColumnEscrowUpdate</p></li><li><p>JET_bitColumnFinalize</p></li><li><p>JET_bitColumnDeleteOnZero</p></li><li><p>JET_bitColumnMaybeNull</p></li></ul> | 
| <p>JET_bitColumnDeleteOnZero</p> | <p>Столбец является столбцом депонированного обновления, и когда он достигает нуля, запись будет удалена. Обычно для столбца, который может быть завершен, можно использовать его как поле счетчика ссылок, а когда поле достигает нуля, запись удаляется. JET_bitColumnDeleteOnZero связана с JET_bitColumnFinalize. Столбец Deleted-on-Zero должен быть столбцом депонированного обновления. JET_bitColumnDeleteOnZero нельзя использовать с JET_bitColumnFinalize. JET_bitColumnDeleteOnZero нельзя использовать с пользовательскими столбцами по умолчанию.</p> | 



**пвдефаулт**

Указывает на буфер, который будет значением по умолчанию для столбца. Длина буфера равна **кбдефаулт**. Если значение по умолчанию отсутствует, **пвдефаулт** должно иметь значение null, а **кбдефаулт** — нулевое значение. Если *грбит* имеет JET_bitColumnUserDefinedDefault, **пвдефаулт** будет интерпретироваться как указатель на структуру JET_USERDEFINEDDEFAULT. Значения по умолчанию не могут быть больше 255 байт. Если значение по умолчанию превышает 255 байт, оно будет обрезано без уведомления.

**кбдефаулт**

Размер (в байтах) буфера, заданного параметром **пвдефаулт**.

**cp**

Кодовая страница для столбца. Единственными допустимыми значениями для текстовых столбцов являются английский (1252) и Unicode (1200). Нулевое значение означает, что будет использоваться по умолчанию (английский, 1252). Если столбец не является текстовым столбцом, кодовая страница автоматически получает значение 0.

**columnid**

При успешном завершении идентификатор столбца вновь созданного столбца будет передан обратно в это поле. При сбое значение не определено.

**Err**

Поле **Err** будет содержать состояние создания этого столбца. Список вероятных возвращаемых значений см. в разделе [жетаддколумн](./jetaddcolumn-function.md) .

### <a name="requirements"></a>Требования


| Требование | Применение |
|------------|----------|
| <p><strong>Клиент</strong></p> | <p>требуется Windows Vista, Windows XP или Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>требуется Windows server 2008, Windows server 2003 или сервер Windows 2000.</p> | 
| <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | 
| <p><strong>Юникод</strong></p> | <p>Реализуется как <strong>JET_COLUMNCREATE_W</strong> (Юникод) и <strong>JET_COLUMNCREATE_A</strong> (ANSI).</p> | 



### <a name="see-also"></a>См. также:

[JET_COLTYP](./jet-coltyp.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_RETINFO](./jet-retinfo-structure.md)  
[JET_SETINFO](./jet-setinfo-structure.md)  
[JET_SETCOLUMN](./jet-setcolumn-structure.md)  
[JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md)  
[JET_ENUMCOLUMNVALUE](./jet-enumcolumnvalue-structure.md)  
[жетаддколумн](./jetaddcolumn-function.md)  
[жеткреатетаблеколумниндекс](./jetcreatetablecolumnindex-function.md)  
[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)  
[жетескровупдате](./jetescrowupdate-function.md)  
[жетренамеколумн](./jetrenamecolumn-function.md)  
[жетсетколумнс](./jetsetcolumns-function.md)
