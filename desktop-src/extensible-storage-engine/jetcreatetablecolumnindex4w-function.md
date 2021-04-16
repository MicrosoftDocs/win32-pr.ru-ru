---
description: Дополнительные сведения о функции JetCreateTableColumnIndex4W
title: Функция JetCreateTableColumnIndex4W
TOCTitle: JetCreateTableColumnIndex4W Function
ms:assetid: 5a74b397-dfb4-4a1d-807b-284329239bc3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835042(v=EXCHG.10)
ms:contentKeyID: 49894664
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetCreateTableColumnIndex4W
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 26ebdb8cf62123febe2d44b5a638c285c180062c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105713071"
---
# <a name="jetcreatetablecolumnindex4w-function"></a>Функция JetCreateTableColumnIndex4W


_**Применимо к:** Windows | Windows Server_

Функция **JetCreateTableColumnIndex4W** создает таблицу в расширяемой подсистеме хранилища (ESE (база данных с начальным набором индексов и начальным набором столбцов из массива структур [JET_TABLECREATE3](./jet-tablecreate3-structure.md) . Структура [JET_TABLECREATE3](./jet-tablecreate3-structure.md) позволяет указать функцию обратного вызова.

Функция **JetCreateTableColumnIndex4W** была введена в операционной системе Windows 8.

``` c++
JET_ERR JET_API JetCreateTableColumnIndex4W(
  __in          JET_SESID sesid,
  __in          JET_DBID dbid,
  __in_out      JET_TABLECREATE3* ptablecreate
);
```

### <a name="parameters"></a>Параметры

*сесид*

Контекст сеанса базы данных, используемый для вызова API.

*DBID*

Идентификатор базы данных, используемый для вызова API.

*птаблекреате*

Указатель на структуру [JET_TABLECREATE3](./jet-tablecreate3-structure.md) , определяющую создаваемую таблицу. Дополнительные сведения см. в разделе [JET_TABLECREATE3](./jet-tablecreate3-structure.md) .

### <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из кодов возврата, перечисленных в следующей таблице. Дополнительные сведения о возможных ошибках расширенного хранилища Енгинже (ESE) см. в разделе [ошибки расширенного подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Код возврата</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>Операция выполнена успешно.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCallbackNotResolved</p></td>
<td><p>Не удалось разрешить функцию обратного вызова. Возможно, Библиотека DLL не найдена или не найдена функция в библиотеке DLL. Если ведение журнала включено, в журнале событий будут представлены дополнительные сведения.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errCannotIndex</p></td>
<td><p>Предпринята попытка индексирования по столбцу с использованием типа "условно-Update" или "SLV" (Обратите внимание, что столбцы SLV устарели).</p></td>
</tr>
<tr class="even">
<td><p>JET_errCannotNestDDL</p></td>
<td><p>Возвращается, если параметр <em>птаблекреате- &gt; грбит</em> задает JET_bitTableCreateTemplateTable значение, но параметр <em>птаблекреате- &gt; сзтемплатетабленаме</em> имеет значение null.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnDuplicate</p></td>
<td><p>Столбец уже существует.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnNotFound</p></td>
<td><p>Предпринята попытка индексировать несуществующий столбец. Эта ошибка также может возникнуть при попытке условного индексирования по несуществующему столбцу.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnRedundant</p></td>
<td><p>Была предпринята попытка добавить избыточный столбец. Должно существовать не более одного столбца автоинкремента, и для каждой таблицы должно существовать не более одного столбца версии.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDensityInvalid</p></td>
<td><p>Эта ошибка будет возвращена, если элементу <strong>улденсити</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> присвоено число меньше 20 или больше 100.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDDLNotInheritable</p></td>
<td><p>Означает, что таблица, указанная в элементе <strong>сзтемплатетабленаме</strong> структуры <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> , не была помечена как таблица шаблона (т. е. в таблице не установлено значение параметра JET_bitTableCreateTemplateTable).</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexDuplicate</p></td>
<td><p>Была выполнена попытка определить два одинаковых индекса.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexHasPrimary</p></td>
<td><p>Предпринята попытка указать более одного первичного индекса для таблицы. У таблицы должен быть ровно один первичный индекс. Если первичный индекс не указан, ядро СУБД будет прозрачно создавать его.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexInvalidDef</p></td>
<td><p>Указано недопустимое определение индекса. Ниже приведены некоторые возможные причины этой ошибки.</p>
<ul>
<li><p>Первичный индекс является условным (то есть элемент <strong>грбит</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> имеет набор значений JET_bitIndexPrimary, а элемент <strong>ккондитионалколумн</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> больше нуля).</p></li>
<li><p>Применимо к версиям операционной системы Windows Server, начиная с Windows Server 2003. Попытка создать индекс кортежа с ограничениями кортежей, но без передачи элемента <strong>птуплелимитс</strong> в структуре <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> (то есть элемент <strong>грбит</strong> структуры <strong>JET_INDEXCREATE2</strong> имеет JET_bitIndexTupleLimits набор значений, но указатель <strong>птуплелимитс</strong> имеет значение null).</p></li>
<li><p>Передача недопустимого определения ключа в элемент <strong>сзкэй</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> . Сведения о допустимых определениях см. в разделе <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>.</p></li>
<li><p>Задание для элемента <strong>кбварсегмак</strong> в <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> значение больше значения JET_cbPrimaryKeyMost (для первичного индекса) или больше значения JET_cbSecondaryKeyMost (для вторичного индекса).</p></li>
<li><p>Передача недопустимого сочетания для определяемого пользователем индекса в Юникоде (один из которых имеет бит JET_bitIndexUnicode значение, установленный в элементе <strong>грбит</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ). Некоторые распространенные причины: элемент <strong>пидксуникоде</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> имеет значение null, или код LCID, указанный в структуре <strong>пидксуникоде</strong> , является недопустимым.</p></li>
<li><p>Указание многозначного столбца для первичного индекса.</p></li>
<li><p>Попытка индексировать слишком много условных столбцов. Элемент <strong>ккондитионалколумн</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> не должен быть больше <strong>JET_ccolKeyMost</strong>.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesInvalidLimits</p></td>
<td><p>Применимо к версиям Windows, начиная с Windows XP. Указана структура <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> , а ее ограничения не поддерживаются. Дополнительные сведения см. в разделе "Примечания" структуры <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> .</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesNonUniqueOnly</p></td>
<td><p>Применимо к версиям Windows, начиная с Windows XP. Индекс кортежа не может быть уникальным (т. е. элемент <em>грбит</em> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> не должен иметь одновременно JET_bitIndexPrimary и JET_bitIndexUnique значений).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesOneColumnOnly</p></td>
<td><p>Применимо к версиям Windows, начиная с Windows XP. Индекс кортежа может находиться только в одном столбце (т. е. Если элемент <strong>грбит</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> имеет JET_bitIndexTuples набор значений, а элемент <strong>сзкэй</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> указывает более одного столбца).</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesSecondaryIndexOnly</p></td>
<td><p>Применимо к версиям Windows, начиная с Windows XP. Индекс кортежа не может быть первичным индексом (т. е. элемент <strong>грбит</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> не должен иметь одновременно JET_bitIndexPrimary и JET_bitIndexTuples).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesTextColumnsOnly</p></td>
<td><p>Применимо к версиям Windows, начиная с Windows XP. Индекс кортежа может находиться только в тексте или столбце Юникода. Попытка индексировать другие столбцы (например, двоичные столбцы) приведет к появлению JET_errIndexTuplesTextColumnsOnly кода ответа.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesVarSegMacNotAllowed</p></td>
<td><p>Применимо к версиям Windows, начиная с Windows XP. Индекс кортежа не позволяет установить элемент <strong>кбварсегмак</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInTransaction</p></td>
<td><p>Предпринята попытка создать индекс без сведений о версии во время транзакции.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidCodePage</p></td>
<td><p>Элементу <strong>CP</strong> структуры <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> не задана допустимая кодовая страница. Единственными допустимыми значениями для текстовых столбцов являются английский (1252) и Unicode (1200). Значение 0 означает, что будет использоваться по умолчанию (английский, 1252).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidColumnType</p></td>
<td><p>Элементу <strong>колтип</strong> структуры <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> не был задан допустимый тип столбца.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidCreateIndex</p></td>
<td><p>Ниже приведены некоторые причины, по которым может возникнуть Эта ошибка:</p>
<ul>
<li><p>Элементу <strong>ргиндекскреате</strong> структуры <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> присвоено значение null.</p></li>
<li><p>Элементу <strong>ргколумнкреате</strong> структуры <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> присвоено значение null.</p></li>
<li><p>Элементу <strong>кбструкт</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> не было присвоено допустимое значение.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>В структуре <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> было указано недопустимое сочетание элементов <strong>грбит</strong> .</p>
<p>Определение индекса недопустимо, так как элемент <strong>грбит</strong> содержит неправильные значения. Ниже приведены некоторые возможные причины.</p>
<ul>
<li><p>Для первичного индекса задан бит игнорирования (то есть JET_bitIndexPrimary значение было передано вместе со значениями JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull или JET_bitIndexIgnoreFirstNull).</p></li>
<li><p>Пустой индекс не игнорирует все элементы NULL (т. е. элемент <strong>грбит</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> имеет значение JET_bitIndexEmpty, но не имеет набора значений JET_bitIndexIgnoreAnyNull).</p></li>
<li><p>Передача структуры <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> с недопустимым элементом <strong>грбит</strong> .</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidLanguageId</p></td>
<td><p>Передан недопустимый код локали (LCID) (либо с помощью элемента <strong>LCID</strong> структуры <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> , на который указывает элемент <strong>пидксуникоде</strong> в структуре <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> , либо через поле <strong>LCID</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Указан недопустимый параметр. Ниже приведены некоторые возможные причины.</p>
<ul>
<li><p>Элемент <strong>ргколумнкреате</strong> структуры <a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a> имеет значение null.</p></li>
<li><p>Элемент <strong>кбструкт</strong> одной из структур <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> , указанных в элементе <strong>ргколумнкреате</strong> структуры <a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a> , не был задан как sizeof (JET_COLUMNCREATE).</p></li>
<li><p>Элемент <strong>cbKey</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> имеет значение 0.</p></li>
<li><p>Элементу <strong>кбструкт</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> не присвоено значение sizeof (JET_INDEXCREATE2).</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errRecordTooBig</p></td>
<td><p>Запись слишком велика. Сумма элемента <strong>кбмакс</strong> структуры <a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a> для всех фиксированных столбцов не должна превышать определенное значение.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTableDuplicate</p></td>
<td><p>Таблица уже существует.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyColumns</p></td>
<td><p>Предпринята попытка добавить в таблицу слишком много столбцов. Таблица может содержать не более <strong>JET_ccolFixedMost</strong> фиксированных столбцов, не более <strong>JET_ccolVarMost</strong> столбцов переменной длины и не более <strong>JET_ccolTaggedMost</strong> столбцов с тегами.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errUnicodeTranslationFail</p></td>
<td><p>Произошла ошибка при попытке нормализовать столбец в Юникоде. Это может быть вызвано недостатком системных ресурсов.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSpaceHintsInvalid</p></td>
<td><p>Неверное или неправильное действие элемента структуры подсказок пространства JET.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Комментарии

Функция **JetCreateTableColumnIndex4W** создает таблицу с начальным набором столбцов и индексов. Дополнительные столбцы и индексы можно добавлять и удалять динамически с помощью функций [жетаддколумн](./jetaddcolumn-function.md), [жетделетеколумн](./jetdeletecolumn-function.md), [JetDeleteColumn2](./jetdeletecolumn2-function.md), [жеткреатеиндекс](./jetcreateindex-function.md), [JetCreateIndex2](./jetcreateindex2-function.md), [JetCreateIndex3](./jetcreateindex3-function.md), [JetCreateIndex4W](./jetcreateindex4w-function.md)и [жетделетеиндекс](./jetdeleteindex-function.md) .

Как и в случае с функцией [жетопентабле](./jetopentable-function.md) , когда приложение выполняется с использованием возвращенного *TableID*, функция [жетклосетабле](./jetclosetable-function.md) должна закрыть приложение.

#### <a name="requirements"></a>Требования

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Клиент</strong></p></td>
<td><p>Требуется Windows 8.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Требуется Windows Server 2012.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Объявлено в ESENT. h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Библиотека</strong></p></td>
<td><p>Используйте ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>КОМПОНОВКИ</strong></p></td>
<td><p>Требуется ESENT.dll.</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>См. также раздел

[JET_CBTYP](./jet-cbtyp.md)  
[JET_DBID](./jet-dbid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JET_INDEXCREATE2](./jet-indexcreate2-structure.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_TABLECREATE2](./jet-tablecreate2-structure.md)  
[JET_TABLECREATE3](./jet-tablecreate3-structure.md)  
[JET_TUPLELIMITS](./jet-tuplelimits-structure.md)  
[жетаддколумн](./jetaddcolumn-function.md)  
[жеткреатеиндекс](./jetcreateindex-function.md)  
[JetCreateIndex2](./jetcreateindex2-function.md)  
[JetCreateIndex3](./jetcreateindex3-function.md)  
[жеткреатетабле](./jetcreatetable-function.md)  
[жеткреатетаблеколумниндекс](./jetcreatetablecolumnindex-function.md)  
[жетделетеколумн](./jetdeletecolumn-function.md)  
[JetDeleteColumn2](./jetdeletecolumn2-function.md)
