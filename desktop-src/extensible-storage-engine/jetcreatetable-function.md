---
description: Дополнительные сведения о функции Жеткреатетабле
title: Функция JetCreateTable
TOCTitle: JetCreateTable Function
ms:assetid: 28455b8b-0000-4bd5-a3ca-e1ef0446ee07
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269210(v=EXCHG.10)
ms:contentKeyID: 32765513
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateTableW
- JetCreateTable
- JetCreateTableA
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6ad510b4718ac3f81a77dd16aa5562d22af49de3
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466188"
---
# <a name="jetcreatetable-function"></a>Функция JetCreateTable


_**Применимо к:** Windows | Windows Сервером_

## <a name="jetcreatetable-function"></a>Функция JetCreateTable

Функция **жеткреатетабле** создает пустую таблицу в базе данных ESE.

```cpp
    JET_ERR JET_API JetCreateTable(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szTableName,
      __in          unsigned long lPages,
      __in          unsigned long lDensity,
      __out         JET_TABLEID* ptableid
    );
```

### <a name="parameters"></a>Параметры

*сесид*

Используемый контекст сеанса базы данных.

*DBID*

Используемый идентификатор базы данных.

*сзтабленаме*

Имя создаваемого индекса.

Имя должно быть отформатировано в соответствии со следующими правилами:

  - Должно быть меньше JET_cbNameMost, не включая завершающее значение NULL.

  - Должен состоять из следующего набора символов: от 0 до 9, от A до Z, от a до z и всех остальных знаков препинания, кроме " \! " (восклицательный знак), "," (запятая), " \[ " (открывающая скобка) и " \] " (закрывающая скобка), т. е. символы ASCII 0x20, 0x22 до 0x2D, 0x2F через 0x5A, 0x5c, 0x5d до 0x7F.

  - Не должно начинаться с пробела.

  - Состоять по крайней мере из одного символа, не являющегося пробелом.

*лпажес*

Начальное число страниц базы данных, выделяемых для таблицы. Указание числа больше единицы может сократить фрагментацию, если в эту таблицу вставлено много строк.

*лденсити*

Плотность таблицы в процентных точках. Число должно быть либо 0, либо находиться в диапазоне от 20 до 100. Передача значения 0 означает, что должно использоваться значение по умолчанию. Значение по умолчанию — 80.

*pTableID*

При успешном выполнении в этом поле возвращается идентификатор таблицы. Значение не определено, если API не возвращает JET_errSuccess.

### <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата. дополнительные сведения о возможных ошибках подсистемы ESE см. в разделе [ошибки расширенных служба хранилища Engine](./extensible-storage-engine-errors.md) и [параметры обработки ошибок](./error-handling-parameters.md).


| <p>Код возврата</p> | <p>Описание</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Операция выполнена успешно.</p> | 
| <p>JET_errCallbackNotResolved</p> | <p>Не удалось разрешить функцию обратного вызова. Возможно, Библиотека DLL не найдена или не найдена функция в библиотеке DLL. Если ведение журнала включено, в журнале событий будут представлены дополнительные сведения.</p> | 
| <p>JET_errCannotIndex</p> | <p>Предпринята попытка индексирования по столбцу с использованием типа "условно-Update" или "SLV" (Обратите внимание, что столбцы SLV устарели).</p> | 
| <p>JET_errCannotNestDDL</p> | <p>Если птаблекреате- &gt; грбит указывает JET_bitTableCreateTemplateTable, но птаблекреате- &gt; сзтемплатетабленаме имеет значение null.</p> | 
| <p>JET_errColumnDuplicate</p> | <p>Столбец уже существует.</p> | 
| <p>JET_errColumnNotFound</p> | <p>Предпринята попытка индексировать несуществующий столбец. Эта ошибка также может возникнуть при попытке условного индексирования по несуществующему столбцу.</p> | 
| <p>JET_errColumnRedundant</p> | <p>Была предпринята попытка добавить избыточный столбец. Не должно быть более одного столбца автоинкремента и не более одного столбца версий для каждой таблицы.</p> | 
| <p>JET_errDensityInvalid</p> | <p>В элементе <em>улденсити</em> в структуре <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> или <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> передана недопустимая плотность.</p> | 
| <p>JET_errDDLNotInheritable</p> | <p>Означает, что таблица, указанная в элементе <strong>сзтемплатетабленаме</strong> структуры <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> , не была помечена как таблица шаблона (т. е. в таблице не был установлен JET_bitTableCreateTemplateTable).</p> | 
| <p>JET_errIndexDuplicate</p> | <p>Предпринята попытка определить два одинаковых индекса.</p> | 
| <p>JET_errIndexHasPrimary</p> | <p>Предпринята попытка указать более одного первичного индекса для таблицы. У таблицы должен быть ровно один первичный индекс. Если первичный индекс не указан, ядро СУБД будет прозрачно создавать его.</p> | 
| <p>JET_errIndexInvalidDef</p> | <p>Указано недопустимое определение индекса. Ниже приведены некоторые возможные причины получения этой ошибки:</p><ul><li><p>Первичный индекс является условным (т. е. элемент <strong>грбит</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> имеет JET_bitIndexPrimary Set, а член <strong>ккондитионалколумн</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> больше нуля).</p></li><li><p>Windows Сервер 2003 и более поздней версии. Попытка создать индекс кортежа с ограничениями кортежей, но без передачи элемента <strong>птуплелимитс</strong> в структуре <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> (т. е. элемент <strong>грбит</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> имеет JET_bitIndexTupleLimits установлен, но указатель <strong>птуплелимитс</strong> имеет значение null).</p></li><li><p>Передача недопустимого определения ключа в элемент <strong>сзкэй</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> . Описание допустимых определений см. в разделе <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</p></li><li><p>Установка для элемента <strong>кбварсегмак</strong> в <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> значение больше JET_cbPrimaryKeyMost (для первичного индекса) или больше JET_cbSecondaryKeyMost (для вторичного индекса).</p></li><li><p>Передача недопустимого сочетания для определяемого пользователем индекса в Юникоде (одна из которых имеет бит JET_bitIndexUnicode, заданный в элементе <strong>грбит</strong> в <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>). Некоторые распространенные причины: элемент <strong>пидксуникоде</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> имеет значение null, или код LCID, указанный в структуре <strong>пидксуникоде</strong> , является недопустимым.</p></li><li><p>Указание столбца с несколькими значениями для первичного индекса.</p></li><li><p>Попытка индексировать слишком много условных столбцов. Элемент <strong>ккондитионалколумн</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> не должен быть больше JET_ccolKeyMost.</p></li></ul> | 
| <p>JET_errIndexTuplesInvalidLimits</p> | <p>Windows XP и более поздних версий. Указана структура <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> , а ее ограничения не поддерживаются. См. раздел "Примечания" структуры <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> .</p> | 
| <p>JET_errIndexTuplesNonUniqueOnly</p> | <p>Windows XP и более поздних версий. Индекс кортежа не может быть уникальным (т. е. элемент <em>грбит</em> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> не должен иметь одновременно JET_bitIndexPrimary и JET_bitIndexUnique).</p> | 
| <p>JET_errIndexTuplesOneColumnOnly</p> | <p>Windows XP и более поздних версий. Индекс кортежа может находиться только в одном столбце (т. е. Если элемент <strong>грбит</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> JET_bitIndexTuples задан, а элемент <strong>сзкэй</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> указывает более одного столбца).</p> | 
| <p>JET_errIndexTuplesSecondaryIndexOnly</p> | <p>Windows XP и более поздних версий. Индекс кортежа не может быть первичным индексом (т. е. элемент <strong>грбит</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> не должен иметь одновременно JET_bitIndexPrimary и JET_bitIndexTuples).</p> | 
| <p>JET_errIndexTuplesVarSegMacNotAllowed</p> | <p>Windows XP и более поздних версий. Индекс кортежа не позволяет установить элемент <strong>кбварсегмак</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</p> | 
| <p>JET_errIndexTuplesTextColumnsOnly</p> | <p>Windows XP и более поздних версий. Индекс кортежа может находиться только в тексте или столбце Юникода. Попытка индексировать другие столбцы (например, двоичные столбцы) приведет к JET_errIndexTuplesTextColumnsOnly.</p> | 
| <p>JET_errInTransaction</p> | <p>Предпринята попытка создать индекс без сведений о версии во время транзакции.</p> | 
| <p>JET_errInvalidCodePage</p> | <p>Элементу <strong>CP</strong> структуры <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> не задана допустимая кодовая страница. Единственными допустимыми значениями для текстовых столбцов являются английский (1252) и Unicode (1200). Значение 0 означает, что будет использоваться по умолчанию (английский, 1252).</p> | 
| <p>JET_errInvalidColumnType</p> | <p>Элементу <strong>колтип</strong> структуры <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> не был задан допустимый тип столбца.</p> | 
| <p>JET_errInvalidCreateIndex</p> | <p>Некоторые причины этой ошибки могут возникнуть:</p><ul><li><p>Элементу <strong>ргиндекскреате</strong> структуры <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> присвоено значение null.</p></li><li><p>Элементу <strong>ргколумнкреате</strong> структуры <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> присвоено значение null.</p></li><li><p>Элементу <strong>кбструкт</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> не было присвоено допустимое значение.</p></li></ul> | 
| <p>JET_errInvalidgrbit</p> | <p>В <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> или <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a>указано недопустимое сочетание элементов <strong>грбит</strong> .</p><p>Определение индекса недопустимо, так как элемент <strong>грбит</strong> содержит неправильные значения. Возможные причины:</p><ul><li><p>Для первичного индекса задан бит игнорирования (то есть JET_bitIndexPrimary передан с JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull или JET_bitIndexIgnoreFirstNull).</p></li><li><p>Пустой индекс не игнорирует все элементы NULL (т. е. элемент <strong>грбит</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> JET_bitIndexEmpty установлен, но не имеет JET_bitIndexIgnoreAnyNull).</p></li><li><p>Передача структуры <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> с недопустимым элементом <strong>грбит</strong> .</p></li></ul> | 
| <p>JET_errInvalidLanguageId</p> | <p>Передан недопустимый код локали (LCID) (либо с помощью элемента <strong>LCID</strong> структуры <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> , на который указывает элемент <strong>пидксуникоде</strong> в структуре <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> , либо с помощью поля <strong>LCID</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ).</p> | 
| <p>JET_errInvalidParameter</p> | <p>Указан недопустимый параметр. Возможные причины:</p><ul><li><p>Элемент <strong>ргколумнкреате</strong> структуры <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> имеет значение null.</p></li><li><p>Элемент <strong>кбструкт</strong> одной из структур <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> , указанных в элементе <strong>ргколумнкреате</strong> структуры <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> , не был задан как sizeof (JET_COLUMNCREATE).</p></li><li><p>Элемент <strong>cbKey</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> имеет значение 0.</p></li><li><p>Элементу <strong>кбструкт</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> не присвоено значение sizeof (JET_INDEXCREATE).</p></li></ul> | 
| <p>JET_errRecordTooBig</p> | <p>Запись слишком велика. Сумма элемента <strong>кбмакс</strong> структуры <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> для всех фиксированных столбцов не должна превышать определенное значение.</p> | 
| <p>JET_errTableDuplicate</p> | <p>Таблица уже существует.</p> | 
| <p>JET_errTooManyColumns</p> | <p>Предпринята попытка добавить в таблицу слишком много столбцов. Таблица может содержать не более JET_ccolFixedMost фиксированных столбцов, не более JET_ccolVarMost столбцов переменной длины и не более JET_ccolTaggedMost столбцов с тегами.</p> | 
| <p>JET_errUnicodeTranslationFail</p> | <p>Произошла ошибка при попытке нормализовать столбец в Юникоде. Это может быть вызвано недостатком системных ресурсов.</p> | 



#### <a name="remarks"></a>Комментарии

**Жеткреатетабле** создает таблицу, которая не содержит столбцов. Чтобы добавить столбцы, см. раздел [жетаддколумн](./jetaddcolumn-function.md).

Внутренне **жеткреатетабле** вызывает [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md), заполняя структуру [JET_TABLECREATE2](./jet-tablecreate2-structure.md) следующим:

  - JET_TABLECREATE2. Кбструкт = sizeof (JET_TABLECREATE2)

  - JET_TABLECREATE2. Сзтабленаме = Сзтабленаме

  - JET_TABLECREATE2. Улпажес = Лпаже

  - JET_TABLECREATE2. Улденсити = Лденсити

  - JET_TABLECREATE2. TableID = JET_tableidNil

Все остальные поля внутренней [JET_TABLECREATE2](./jet-tablecreate2-structure.md) структуры имеют нулевое значение или значение null. В выходных данных *pTableID* будет иметь значение JET_TABLECREATE2. TableID.

Дополнительные сведения см. в разделе [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md) .

Как и [жетопентабле](./jetopentable-function.md), когда приложение выполняется с использованием возвращенного элемента **tableid** из структуры [JET_TABLECREATE2](./jet-tablecreate2-structure.md) , оно обычно должно быть закрыто с помощью [жетклосетабле](./jetclosetable-function.md).

#### <a name="requirements"></a>Требования


| | | <p><strong>Клиент</strong></p> | <p>требуется Windows Vista, Windows XP или Windows 2000 Professional.</p> | | <p><strong>Сервер</strong></p> | <p>требуется Windows server 2008, Windows server 2003 или сервер Windows 2000.</p> | | <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | | <p><strong>Библиотека</strong></p> | <p>Используйте ESENT. lib.</p> | | <p><strong>КОМПОНОВКИ</strong></p> | <p>Требуется ESENT.dll.</p> | | <p><strong>Юникод</strong></p> | <p>Реализуется как <strong>жеткреатетаблев</strong> (Юникод) и <strong>жеткреатетаблеа</strong> (ANSI).</p> | 



#### <a name="see-also"></a>См. также:

[JET_DBID](./jet-dbid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_TABLECREATE2](./jet-tablecreate2-structure.md)  
[жетаддколумн](./jetaddcolumn-function.md)  
[жеткреатетаблеколумниндекс](./jetcreatetablecolumnindex-function.md)  
[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)
