---
description: Дополнительные сведения о функции JetCreateIndex3
title: Функция JetCreateIndex3
TOCTitle: JetCreateIndex3 Function
ms:assetid: bc9b940e-65c6-49d6-ad32-74434527d29f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294075(v=EXCHG.10)
ms:contentKeyID: 32765690
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateIndex3A
- JetCreateIndex3
- JetCreateIndex3W
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c4f3331a903d4885499ff6c2cd2cad0d8b8534a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346965"
---
# <a name="jetcreateindex3-function"></a>Функция JetCreateIndex3


_**Применимо к:** Windows | Windows Server_

## <a name="jetcreateindex3-function"></a>Функция JetCreateIndex3

Функция **JetCreateIndex3** создает индексы для данных в базе данных ESE, которая может быть использована для быстрого выявления конкретных данных.

**Windows 7: JetCreateIndex3** появился в операционной системе Windows 7.

```cpp
    JET_ERR JET_API JetCreateIndex3(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_INDEXCREATE2* pindexcreate,
      __in          unsigned long cIndexCreate
    );
```

### <a name="parameters"></a>Параметры

*сесид*

Контекст сеанса базы данных, используемый для вызова API.

*TableID*

Таблица, в которой будет создан индекс.

*пиндекскреате*

Массив структур [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) , каждый из которых определяет создаваемый индекс.

*Циндекскреате*

Число элементов в массиве *пиндекскреате* .

### <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает [JET_ERR](./jet-err.md) тип данных с одним из следующих кодов возврата. Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).

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
<td><p>JET_errCannotIndex</p></td>
<td><p>Предпринята попытка индексирования по столбцу с использованием типа "условно-Update" или "SLV" (Обратите внимание, что столбцы SLV устарели).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnNotFound</p></td>
<td><p>Предпринята попытка индексировать несуществующий столбец. Эта ошибка также может возникнуть при попытке условного индексирования по несуществующему столбцу.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDensityInvalid</p></td>
<td><p>Эта ошибка будет возвращена, если элементу <strong>улденсити</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> присвоено число меньше 20 или больше 100.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexDuplicate</p></td>
<td><p>Была выполнена попытка определить два одинаковых индекса.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexHasPrimary</p></td>
<td><p>Предпринята попытка указать более одного первичного индекса для таблицы. У таблицы должен быть ровно один первичный индекс. Если первичный индекс не указан, ядро СУБД будет прозрачно создавать его.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexInvalidDef</p></td>
<td><p>Указано недопустимое определение индекса. Ниже приведены некоторые возможные причины получения этой ошибки.</p>
<ul>
<li><p>Первичный индекс является условным (<strong>грбит</strong> член <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> имеет JET_bitIndexPrimary набор, а элемент <strong>ккондитионалколумн</strong> <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> больше нуля).</p></li>
<li><p>Windows Server 2003 и более поздние версии Windows. Попытка создать индекс кортежа с ограничениями кортежей, но без передачи сведений в элемент <strong>птуплелимитс</strong> в <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> (то есть <em>грбит</em> имеет набор JET_bitIndexTupleLimits, но указатель <strong>птуплелимитс</strong> имеет значение null).</p></li>
<li><p>Передача недопустимого определения ключа в элемент <strong>сзкэй</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> . Описание допустимых определений см. в разделе <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</p></li>
<li><p>Установка для элемента <strong>кбварсегмак</strong> в <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> значение больше JET_cbPrimaryKeyMost (для первичного индекса) или больше JET_cbSecondaryKeyMost (для вторичного индекса).</p></li>
<li><p>Передача недопустимого сочетания для определяемого пользователем индекса в Юникоде (одна из которых имеет бит JET_bitIndexUnicode, заданный в элементе <strong>грбит</strong> в <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>). Некоторые распространенные причины могут быть вызваны тем, что поле пидксуникоде структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> имеет значение null или код LCID, указанный в структуре пидксуникоде, является недопустимым.</p></li>
<li><p>Указание столбца с несколькими значениями для первичного индекса.</p></li>
<li><p>Попытка индексировать слишком много условных столбцов. Элемент <strong>ккондитионалколумн</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> не должен быть больше JET_ccolKeyMost.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesInvalidLimits</p></td>
<td><p>Windows XP и более поздние версии Windows. Указана структура <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> , а ее ограничения не поддерживаются. См. раздел "Примечания" структуры <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> .</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesNonUniqueOnly</p></td>
<td><p>Windows XP и более поздние версии Windows. Индекс кортежа не может быть уникальным (<em>грбит</em> не должен содержать как JET_bitIndexTuples, так JET_bitIndexUnique Set).</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesOneColumnOnly</p></td>
<td><p>Windows XP и более поздние версии Windows. Индекс кортежа может находиться только в одном столбце (то есть элемент <strong>грбит</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> имеет JET_bitIndexTuples набор, а элемент <strong>сзкэй</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> указывает более одного столбца).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesSecondaryIndexOnly</p></td>
<td><p>Windows XP и более поздние версии Windows. Индекс кортежа не может быть первичным индексом (т. е. элемент <strong>грбит</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> не должен иметь одновременно JET_bitIndexPrimary и JET_bitIndexTuples).</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesTextColumnsOnly</p></td>
<td><p>Windows XP и более поздние версии Windows. Индекс кортежа может находиться только в тексте или столбце Юникода. Попытка индексировать другие столбцы (например, двоичные столбцы) приведет к JET_errIndexTuplesTextColumnsOnly.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesVarSegMacNotAllowed</p></td>
<td><p>Windows XP и более поздние версии Windows. Индекс кортежа не позволяет установить элемент <strong>кбварсегмак</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</p></td>
</tr>
<tr class="even">
<td><p>JET_errInTransaction</p></td>
<td><p>Предпринята попытка создать индекс без сведений о версии во время транзакции.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>Определение индекса недопустимо, так как элемент <strong>грбит</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> содержит неправильные значения. Ниже приведены некоторые возможные причины.</p>
<ul>
<li><p>В первичном индексе указан бит игнорирования (JET_bitIndexPrimary был передан с одним из JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull или JET_bitIndexIgnoreFirstNull).</p></li>
<li><p>Пустой индекс не игнорирует какие-либо поля NULL (т. е. элемент <strong>грбит</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> JET_bitIndexEmpty задан, но не имеет набора JET_bitIndexIgnoreAnyNull).</p></li>
<li><p>Передача структуры <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> с недопустимым элементом <strong>грбит</strong> . См. <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a>.</p></li>
</ul>
<p>При создании нескольких индексов одновременно (то есть если параметр <em>Циндекскреате</em> больше единицы) ни один из индексов не может содержать следующие биты:</p>
<ul>
<li><p>JET_bitIndexPrimary</p></li>
<li><p>JET_bitIndexUnversioned</p></li>
<li><p>JET_bitIndexEmpty</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidLanguageId</p></td>
<td><p>Передан недопустимый код локали (LCID) (с помощью элемента <strong>LCID</strong> в структуре <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> , которой элемент <strong>пидксуникоде</strong> в структуре <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> содержит указатель на или с помощью элемента <strong>LCID</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidName</p></td>
<td><p>Указано недопустимое имя индекса. Дополнительные сведения см. в разделе <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>В API передан недопустимый параметр. Ниже приведены некоторые причины, по которым может быть возвращена эта ошибка:</p>
<ul>
<li><p>Поле <strong>cbKey</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> имеет значение 0.</p></li>
<li><p>Элементу <strong>кбструкт</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> не присвоено значение sizeof ( <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ).</p></li>
</ul></td>
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

Возвращаемое значение JET_errSuccess при успешном завершении всех указанных индексов.

**JetCreateIndex3** перебирает индексы, заданные в **пиндекскреате**, и иногда прерываются при первом сбое. Любые индексы после первого индекса с ошибкой могут не попытаться, несмотря на то, что элемент **Err** структуры [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) содержит JET_errSuccess.

#### <a name="requirements"></a>Требования

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
<tr class="even">
<td><p><strong>Библиотека</strong></p></td>
<td><p>Используйте ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>КОМПОНОВКИ</strong></p></td>
<td><p>Требуется ESENT.dll.</p></td>
</tr>
<tr class="even">
<td><p><strong>Юникод</strong></p></td>
<td><p>Реализуется как <strong>JetCreateIndex3W</strong> (Юникод) и <strong>JetCreateIndex3A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>См. также:

[JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_INDEXCREATE2](./jet-indexcreate2-structure.md)  
[жеткреатеиндекс](./jetcreateindex-function.md)  
[жеткреатетаблеколумниндекс](./jetcreatetablecolumnindex-function.md)  
[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)  
[JET_SPACEHINTS](./jet-spacehints-structure.md)
