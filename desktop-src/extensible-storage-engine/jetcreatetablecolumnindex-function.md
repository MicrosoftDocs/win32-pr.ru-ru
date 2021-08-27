---
description: Дополнительные сведения о функции Жеткреатетаблеколумниндекс
title: Функция Жеткреатетаблеколумниндекс
TOCTitle: JetCreateTableColumnIndex Function
ms:assetid: 9192614b-20a6-40fb-906a-51fc057e7483
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269343(v=EXCHG.10)
ms:contentKeyID: 32765632
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateTableColumnIndexA
- JetCreateTableColumnIndexW
- JetCreateTableColumnIndex
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b17fea6bc4ee4856c3cae653eb8f138156ce9927
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122986017"
---
# <a name="jetcreatetablecolumnindex-function"></a>Функция Жеткреатетаблеколумниндекс


_**Применимо к:** Windows | Windows Сервером_

## <a name="jetcreatetablecolumnindex-function"></a>Функция Жеткреатетаблеколумниндекс

Функция **жеткреатетаблеколумниндекс** создает таблицу в базе данных ESE с начальным набором индексов и начальным набором столбцов из массива структур [JET_TABLECREATE](./jet-tablecreate-structure.md) . Имя **жеткреатетаблеколумниндекс** поступает из порядка создания объектов. Сначала он создает таблицу, столбцы и, наконец, индексы.

```cpp
    JET_ERR JET_API JetCreateTableColumnIndex(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in_out      JET_TABLECREATE* ptablecreate
    );
```

### <a name="parameters"></a>Параметры

*сесид*

Контекст сеанса базы данных, используемый для вызова API.

*DBID*

Идентификатор базы данных, используемый для вызова API.

*птаблекреате*

Указатель на структуру [JET_TABLECREATE](./jet-tablecreate-structure.md) , которая определяет создаваемую таблицу. Дополнительные сведения см. в разделе [JET_TABLECREATE](./jet-tablecreate-structure.md) .

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
| <p>JET_errDensityInvalid</p> | <p>Эта ошибка будет возвращена, если элементу <strong>улденсити</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> присвоено число меньше 20 или больше 100.</p> | 
| <p>JET_errDDLNotInheritable</p> | <p>Означает, что таблица, указанная в элементе <strong>сзтемплатетабленаме</strong> структуры <a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a> , не была помечена как таблица шаблона (т. е. в таблице не задан JET_bitTableCreateTemplateTable).</p> | 
| <p>JET_errIndexDuplicate</p> | <p>Была выполнена попытка определить два одинаковых индекса.</p> | 
| <p>JET_errIndexHasPrimary</p> | <p>Предпринята попытка указать более одного первичного индекса для таблицы. У таблицы должен быть ровно один первичный индекс. Если первичный индекс не указан, ядро СУБД будет прозрачно создавать его.</p> | 
| <p>JET_errIndexInvalidDef</p> | <p>Указано недопустимое определение индекса. Ниже приведены некоторые возможные причины получения этой ошибки:</p><ul><li><p>Первичный индекс является условным (т. е. элемент <strong>грбит</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> имеет JET_bitIndexPrimary Set, а член <strong>ккондитионалколумн</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> больше нуля).</p></li><li><p>Windows Сервер 2003 и более поздней версии. Попытка создать индекс кортежа с ограничениями кортежей, но без передачи элемента <strong>птуплелимитс</strong> в структуре <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> (т. е. элемент <strong>грбит</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> имеет JET_bitIndexTupleLimits установлен, но указатель <strong>птуплелимитс</strong> имеет значение null).</p></li><li><p>Передача недопустимого определения ключа в элемент <strong>сзкэй</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> . Описание допустимых определений см. в разделе <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</p></li><li><p>Установка для элемента <strong>кбварсегмак</strong> в <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> значение больше JET_cbPrimaryKeyMost (для первичного индекса) или больше JET_cbSecondaryKeyMost (для вторичного индекса).</p></li><li><p>Передача недопустимого сочетания для определяемого пользователем индекса в Юникоде (одна из которых имеет бит JET_bitIndexUnicode, заданный в элементе <strong>грбит</strong> в <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>). Некоторые распространенные причины: элемент <strong>пидксуникоде</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> имеет значение null, или код LCID, указанный в структуре <strong>пидксуникоде</strong> , является недопустимым.</p></li><li><p>Указание столбца с несколькими значениями для первичного индекса.</p></li><li><p>Попытка индексировать слишком много условных столбцов. Элемент <strong>ккондитионалколумн</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> не должен быть больше JET_ccolKeyMost.</p></li></ul> | 
| <p>JET_errIndexTuplesInvalidLimits</p> | <p>Windows XP и более поздних версий. Указана структура <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> , а ее ограничения не поддерживаются. См. раздел "Примечания" структуры <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> .</p> | 
| <p>JET_errIndexTuplesNonUniqueOnly</p> | <p>Windows XP и более поздних версий. Индекс кортежа не может быть уникальным (т. е. элемент <em>грбит</em> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> не должен иметь одновременно JET_bitIndexPrimary и JET_bitIndexUnique).</p> | 
| <p>JET_errIndexTuplesOneColumnOnly</p> | <p>Windows XP и более поздних версий. Индекс кортежа может находиться только в одном столбце (т. е. Если элемент <strong>грбит</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> JET_bitIndexTuples задан, а элемент <strong>сзкэй</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> указывает более одного столбца).</p> | 
| <p>JET_errIndexTuplesSecondaryIndexOnly</p> | <p>Windows XP и более поздних версий. Индекс кортежа не может быть первичным индексом (т. е. элемент <strong>грбит</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> не должен иметь одновременно JET_bitIndexPrimary и JET_bitIndexTuples).</p> | 
| <p>JET_errIndexTuplesTextColumnsOnly</p> | <p>Windows XP и более поздних версий. Индекс кортежа может находиться только в тексте или столбце Юникода. Попытка индексировать другие столбцы (например, двоичные столбцы) приведет к JET_errIndexTuplesTextColumnsOnly.</p> | 
| <p>JET_errIndexTuplesVarSegMacNotAllowed</p> | <p>Windows XP и более поздних версий. Индекс кортежа не позволяет установить элемент <strong>кбварсегмак</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</p> | 
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

Вызов **жеткреатетаблеколумниндекс** идентичен вызову [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md), при этом каждое поле в структуре [JET_TABLECREATE2](./jet-tablecreate2-structure.md) содержит значение соответствующего поля [JET_TABLECREATE](./jet-tablecreate-structure.md)со следующими исключениями:

  - JET_TABLECREATE2. Кбструкт задано значение sizeof (JET_TABLECREATE2)

  - JET_TABLECREATE2. Сзкаллбакк имеет значение NULL

  - JET_TABLECREATE2. кбтип имеет значение 0

Дополнительные сведения см. в разделе [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md) .

Как и [жетопентабле](./jetopentable-function.md), когда приложение выполняется с помощью возвращенного *TableID*, оно обычно должно быть закрыто с помощью [жетклосетабле](./jetclosetable-function.md).

#### <a name="requirements"></a>Требования


| Требование | Применение |
|------------|----------|
| <p><strong>Клиент</strong></p> | <p>требуется Windows Vista, Windows XP или Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>требуется Windows server 2008, Windows server 2003 или сервер Windows 2000.</p> | 
| <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | 
| <p><strong>Библиотека</strong></p> | <p>Используйте ESENT. lib.</p> | 
| <p><strong>КОМПОНОВКИ</strong></p> | <p>Требуется ESENT.dll.</p> | 
| <p><strong>Юникод</strong></p> | <p>Реализуется как <strong>жеткреатетаблеколумниндексв</strong> (Юникод) и <strong>жеткреатетаблеколумниндекса</strong> (ANSI).</p> | 



#### <a name="see-also"></a>См. также:

[JET_DBID](./jet-dbid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_TABLECREATE](./jet-tablecreate-structure.md)  
[JET_TABLECREATE2](./jet-tablecreate2-structure.md)  
[жетаддколумн](./jetaddcolumn-function.md)  
[жеткреатетаблеколумниндекс]()  
[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)
