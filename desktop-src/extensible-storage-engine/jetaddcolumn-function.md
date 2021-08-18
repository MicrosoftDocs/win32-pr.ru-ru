---
description: Дополнительные сведения о функции Жетаддколумн
title: Функция JetAddColumn
TOCTitle: JetAddColumn Function
ms:assetid: e146f784-2cbd-42c0-bf64-b37dc6f9ee43
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294122(v=EXCHG.10)
ms:contentKeyID: 32765736
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetAddColumnW
- JetAddColumnA
- JetAddColumn
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2c1c70ab6510d2e63cc1b59e94ae058565937e854968b7ba05e2710ba22aa6af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118979054"
---
# <a name="jetaddcolumn-function"></a>Функция JetAddColumn


_**Применимо к:** Windows | Windows Сервером_

## <a name="jetaddcolumn-function"></a>Функция JetAddColumn

Функция **жетаддколумн** добавляет новый столбец в существующую таблицу в базе данных ESE.

```cpp
    JET_ERR JET_API JetAddColumn(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_PCSTR szColumnName,
      __in          const JET_COLUMNDEF* pcolumndef,
      __in_opt      const void* pvDefault,
      __in          unsigned long cbDefault,
      __out_opt     JET_COLUMNID* pcolumnid
    );
```

### <a name="parameters"></a>Параметры

*сесид*

Контекст сеанса базы данных, используемый для вызова API.

*TableID*

Таблица, в которую добавляется столбец.

*сзколумннаме*

Имя добавляемого столбца. Имя должно соответствовать следующим критериям:

  - Длина должна быть меньше JET_cbNameMost символов, не включая завершающее **значение NULL**.

  - Он должен содержать только символы из следующих наборов: от 0 до 9, от A до Z, от a до z и всех остальных знаков препинания, за исключением восклицательного знака ( \! ), запятой (,), открывающей квадратной скобки ( \[ ) и закрывающей квадратной скобки ( \] ), т. е. символов ASCII 0x20, 0x22 до 0x7F

  - Оно не может начинаться с пробела.

  - Он должен содержать по крайней мере один символ, не являющийся пробелом.

*пколумндеф*

Указатель на структуру [JET_COLUMNDEF](./jet-columndef-structure.md) , которая определяет данные, которые могут храниться в столбце.

*пвдефаулт*

Указатель на буфер, содержащий значение по умолчанию для столбца. Длина буфера равна **кбдефаулт**. Если значение по умолчанию отсутствует, установите **пвдефаулт** в **значение NULL** и **кбдефаулт** в ноль. Значения по умолчанию не могут превышать JET_cbColumnMost байты для фиксированных столбцов или JET_cbLVDefaultValueMost байты для длинных значений. Если значение по умолчанию больше этого значения, оно будет обрезано без уведомления.

Если *грбит* имеет JET_bitColumnUserDefinedDefault, **пвдефаулт** будет интерпретироваться как указатель на структуру [JET_USERDEFINEDDEFAULT](./jet-userdefineddefault-structure.md) .

*кбдефаулт*

Размер (в байтах) буфера, указанного в **пвдефаулт**.

*пколумнид*

Указатель на структуру [JET_COLUMNID](./jet-columnid.md) , которая, в случае успеха, получит идентификатор только что созданного столбца. При сбое значение не определено.

### <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата. дополнительные сведения о возможных ошибках подсистемы ESE см. в разделе [ошибки расширенных служба хранилища Engine](./extensible-storage-engine-errors.md) и [параметры обработки ошибок](./error-handling-parameters.md).

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
<td><p>JET_errFixedDDL</p></td>
<td><p>Была предпринята попытка изменить определение данных для фиксированной таблицы DDL. Примером таблицы с фиксированной DDL-таблицей является таблица шаблонов.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>В API передан недопустимый параметр. Ниже приведены некоторые примеры недопустимых параметров.</p>
<ul>
<li><p>Передача неправильного размера структуры <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> в ее члене <em>кбструкт</em> .</p></li>
<li><p>Передача JET_bitColumnUserDefinedDefault, но не установка <strong>кбдефаулт</strong> в sizeof (<a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a>).</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errInTransaction</p></td>
<td><p>Предпринята попытка добавить столбец с установленным битом JET_bitColumnUnversioned, но сеанс в данный момент находится в транзакции.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnDuplicate</p></td>
<td><p>Столбец уже существует. Предпринята попытка добавить столбец без сведений о версии, и этот столбец уже существует.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTableNotEmpty</p></td>
<td><p>Таблица содержит данные. Столбец депонированного обновления можно добавить только в пустую таблицу.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRecordTooBig</p></td>
<td><p>Запись слишком велика. Сумма параметра <strong>кбмакс</strong> для фиксированных столбцов не должна превышать определенное значение.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyColumns</p></td>
<td><p>Предпринята попытка добавить в таблицу слишком много столбцов. Таблица может содержать не более JET_ccolFixedMost фиксированных столбцов, не более JET_ccolVarMost столбцов переменной длины и не более JET_ccolTaggedMost столбцов с тегами.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnRedundant</p></td>
<td><p>Была предпринята попытка добавить избыточный столбец. Не должно быть более одного столбца автоинкремента и не более одного столбца версий для каждой таблицы.</p></td>
</tr>
<tr class="even">
<td><p>JET_errCallbackNotResolved</p></td>
<td><p>Не удалось разрешить функцию обратного вызова. Возможно, Библиотека DLL не найдена или не найдена функция в библиотеке DLL. В журнале событий будут предоставлены дополнительные сведения, если включено достаточное протоколирование.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnMaxTruncated</p></td>
<td><p>Предупреждение, указывающее, что максимальная длина (<strong>кбмакс</strong>) фиксированного или переменного столбца превышает JET_cbColumnMost. Это ограничение не применяется к длинным значениям ( <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> и <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>).</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidName</p></td>
<td><p>Недопустимое имя передано в качестве <strong>сзколумннаме</strong>. Дополнительные сведения об ограничениях см. в разделе критерии для <strong>сзколумннаме</strong>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidColumnType</p></td>
<td><p>Поле <strong>колтип</strong> не было задано как допустимый тип столбца.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidCodePage</p></td>
<td><p>Параметр <strong>CP</strong> структуры <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> не был задан как действительная кодовая страница. Единственными допустимыми значениями для текстовых столбцов являются английский (1252) и Unicode (1200). Значение 0 означает, что будет использоваться по умолчанию (английский, 1252).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTaggedNotNULL</p></td>
<td><p>JET_bitColumnNotNULL не может использоваться с тегами, длинными значениями или столбцами SLV.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>Указано недопустимое сочетание <em>грбитс</em> . Вот некоторые из причин возникновения этой ошибки:</p>
<ul>
<li><p>JET_bitColumnFixed использовался для столбца с тегом, длинным значением или в столбце SLV.</p></li>
<li><p>JET_bitColumnEscrowUpdate был использован для столбца, который не был типа <a href="gg269213(v=exchg.10).md">JET_coltypLong</a>.</p></li>
<li><p>JET_bitColumnEscrowUpdate использовался в столбце версии (JET_bitColumnVersion).</p></li>
<li><p>JET_bitColumnEscrowUpdate использовался в столбце Аутоинкремемнт (JET_bitColumnAutoincrement).</p></li>
<li><p>JET_bitColumnEscrowUpdate использовался для столбца, не имеющего значения по умолчанию (<strong>кбдефаулт</strong> равен нулю).</p></li>
<li><p>JET_bitColumnFinalize использовался для столбца, который не является столбцом условно-обновления (JET_bitColumnEscrowUpdate не был задан).</p></li>
<li><p>JET_bitColumnDeleteOnZero использовался для столбца, который не является столбцом условно-обновления (JET_bitColumnEscrowUpdate не был задан).</p></li>
<li><p>JET_bitColumnAutoincrement использовался для столбца, который не был <a href="gg269213(v=exchg.10).md">JET_coltypLong</a>.</p>
<p><strong>Windows 2000:</strong> эта причина для кода ошибки используется только в Windows 2000.</p>
<p>JET_bitColumnAutoincrement использовался для столбца, который не был ни <a href="gg269213(v=exchg.10).md">JET_coltypLong</a> , ни <a href="gg269213(v=exchg.10).md">JET_coltypCurrency</a>.</p>
<p><strong>Windows XP:</strong> по этой причине код ошибки используется в операционных системах Windows XP и более поздних версий.</p></li>
<li><p>JET_bitColumnVersion использовался для столбца, который не был <a href="gg269213(v=exchg.10).md">JET_coltypLong</a>.</p></li>
<li><p>JET_bitColumnVersion использовался в столбце AutoIncrement.</p></li>
<li><p>JET_bitColumnUserDefinedDefault использовался в сочетании с JET_bitColumnFixed.</p></li>
<li><p>JET_bitColumnUserDefinedDefault использовался в сочетании с JET_bitColumnNotNULL.</p></li>
<li><p>JET_bitColumnUserDefinedDefault использовался в сочетании с JET_bitColumnVersion.</p></li>
<li><p>JET_bitColumnUserDefinedDefault использовался в сочетании с JET_bitColumnAutoincrement.</p></li>
<li><p>JET_bitColumnUserDefinedDefault использовался в сочетании с JET_bitColumnUpdatable.</p></li>
<li><p>JET_bitColumnUserDefinedDefault использовался в сочетании с JET_bitColumnEscrowUpdate.</p></li>
<li><p>JET_bitColumnUserDefinedDefault использовался в сочетании с JET_bitColumnFinalize.</p></li>
<li><p>JET_bitColumnUserDefinedDefault использовался в сочетании с JET_bitColumnDeleteOnZero.</p></li>
<li><p>JET_bitColumnUserDefinedDefault использовался в сочетании с JET_bitColumnMaybeNull.</p></li>
<li><p>JET_bitColumnUserDefinedDefault использовался для столбца без тегов (с фиксированным или переменным).</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errMultiValuedColumnMustBeTagged</p></td>
<td><p>Столбец с несколькими значениями (JET_bitColumnMultiValued) может использоваться только для столбца с тегом или длинным значением (<a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> или <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>).</p></td>
</tr>
<tr class="even">
<td><p>JET_errCannotBeTagged</p></td>
<td><p>Предпринята попытка использовать столбец с тегами, если столбец не может быть помечен. Ниже перечислены некоторые ограничения, позволяющие разрешать столбцы с тегами.</p>
<ul>
<li><p>Столбец депонированного обновления (JET_bitColumnEscrowUpdate) не может использоваться для столбца с тегом или длинным значением (<a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> или <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>).</p></li>
<li><p>Столбец с автоувеличением может не помечаться тегами.</p></li>
<li><p>Столбец версии не может быть помечен.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errExclusiveTableLockRequired</p></td>
<td><p>Для этой операции требуется монопольная блокировка таблицы.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnColumnMaxTruncated</p></td>
<td><p>Предупреждение, указывающее, что максимальная длина (<em>кбмакс</em>) фиксированного или переменного столбца превышает JET_cbColumnMost. Это ограничение не применяется к длинным значениям ( <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> и <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>).</p></td>
</tr>
</tbody>
</table>


#### <a name="requirements"></a>Требования

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Клиент</strong></p></td>
<td><p>требуется Windows Vista, Windows XP или Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Сервер</strong></p></td>
<td><p>требуется Windows server 2008, Windows server 2003 или сервер Windows 2000.</p></td>
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
<td><p>Реализуется как <strong>жетаддколумнв</strong> (Юникод) и <strong>жетаддколумна</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>См. также

[JET_COLTYP](./jet-coltyp.md)  
[JET_COLUMNCREATE](./jet-columncreate-structure.md)  
[JET_COLUMNDEF](./jet-columndef-structure.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[жеткреатетаблеколумниндекс](./jetcreatetablecolumnindex-function.md)  
[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)
