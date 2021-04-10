---
description: Дополнительные сведения о функции Жетсетколумнс
title: Функция JetSetColumns
TOCTitle: JetSetColumns Function
ms:assetid: a5b011dc-0da6-44bf-aaf5-352d8a57e5bf
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294050(v=EXCHG.10)
ms:contentKeyID: 32765649
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetColumns
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cfd4535b66064c19257f4bb7b51b059453660916
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143516"
---
# <a name="jetsetcolumns-function"></a>Функция JetSetColumns


_**Применимо к:** Windows | Windows Server_

## <a name="jetsetcolumns-function"></a>Функция JetSetColumns

Функция **жетсетколумнс** похожа на поведение [жетсетколумн](./jetsetcolumn-function.md) , но позволяет приложению задавать несколько значений столбцов в одной операции. Массив структур [JET_SETCOLUMN](./jet-setcolumn-structure.md) используется для описания набора значений столбцов, которые необходимо задать, а также для описания входных буферов для каждого устанавливаемого значения столбца.

```cpp
    JET_ERR JET_API JetSetColumns(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in_out_opt  JET_SETCOLUMN* psetcolumn,
      __in          unsigned long csetcolumn
    );
```

### <a name="parameters"></a>Параметры

*сесид*

Сеанс, используемый для этого вызова.

*TableID*

Курсор, используемый для этого вызова.

*псетколумн*

Указатель на массив из одной или нескольких структур [JET_SETCOLUMN](./jet-setcolumn-structure.md) . Каждая структура включает в себя описания того, какое значение столбца следует задать и откуда получать данные о столбцах для задания.

*ксетколумн*

Число структур [JET_SETCOLUMN](./jet-setcolumn-structure.md) в массиве, заданном параметром *псетколумн*.

### <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата. Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).

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
<td><p>JET_errBadColumnId</p></td>
<td><p>Указанный идентификатор столбца находится за пределами допустимых ограничений идентификатора столбца.</p></td>
</tr>
<tr class="even">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnIllegalNull</p></td>
<td><p>То же, что и JET_errNullInvalid.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnNotFound</p></td>
<td><p>Столбец, описываемый данным <em>columnid</em> , не существует в таблице.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnNotUpdatable</p></td>
<td><p>Предпринята недопустимая попытка обновить значение Long во время операции вставки копирования удаление исходного обновления.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnTooBig</p></td>
<td><p>Данные значений столбцов, заданных во входном буфере, превышают ограничение по размеру либо естественным для столбца фиксированной длины, либо настроены для текстовых или двоичных столбцов фиксированной длины. Эта ошибка также возвращается при передаче более 1024 байт данных для длинного столбца и установке флага JET_bitSetIntrinsicLV.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных. Эта ошибка будет возвращена только Windows XP и более поздних версий.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBufferSize</p></td>
<td><p>Заданный размер данных значения столбца не соответствует типу данных фиксированной длины, который является естественным.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidColumnType</p></td>
<td><p>Предпринята недопустимая попытка обновить столбец автоинкремента во время операции вставки или обновления либо обновить столбец версии во время операции замены.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>Указанные параметры неизвестны или являются недопустимым сочетанием известных битовых параметров.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Заданный псетинфо- &gt; кбструкт не является допустимым размером для структуры <a href="gg294090(v=exchg.10).md">JET_SETINFO</a> .</p></td>
</tr>
<tr class="even">
<td><p>JET_errMultiValuedDuplicate</p></td>
<td><p>Операция задания столбца попыталась создать повторяющееся значение и указать либо JET_bitSetUniqueMultiValues, либо JET_bitSetUniqueNormalizedMultiValues.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInTransaction</p></td>
<td><p>Предпринята недопустимая попытка обновить значение длинного столбца, если вызывающий сеанс не был в транзакции.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNullInvalid</p></td>
<td><p>Предпринята недопустимая попытка установить ненулевое значение NULL для столбца.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRecordTooBig</p></td>
<td><p>Значение столбца не может быть присвоено значению во входном буфере, так как оно привело к превышению ограничения на размер страницы. Столбцы типа <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> или <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> можно хранить отдельно от оставшихся данных записи. Однако другие столбцы должны храниться вместе с записью, что может привести к превышению ограничения на размер записи. Даже для длинных столбцов требуется 5-байтное пространство внутри записи в качестве компоновки, что также может привести к возвращению JET_errRecordTooBig.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Один и тот же сеанс нельзя использовать одновременно для нескольких потоков. Эта ошибка будет возвращена только Windows XP и более поздних версий.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</p></td>
</tr>
<tr class="even">
<td><p>JET_errUpdateNotPrepared</p></td>
<td><p>Курсор в настоящее время не находится в процессе вставки новой записи или обновления существующей записи.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnMaxTruncated</p></td>
<td><p>Значение столбца во входном буфере превысило максимальную заданную длину для столбца переменной длины и было усечено.</p></td>
</tr>
</tbody>
</table>


При успешном выполнении для каждого столбца, описанного в псетколумнс, требуемая часть значения столбца задается данными, скопированными из входного буфера. Набор данных столбца мог быть усечен, если превышена максимальная длина, указанная для столбца переменной длины.

В случае сбоя положение курсора остается неизменным, и данные значения столбца не обновляются в буфере копирования.

#### <a name="remarks"></a>Комментарии

Если любая отдельная операция с набором столбцов возвращает ошибку, то вся операция **жетсетколумнс** возвратит ошибку. Обычно предупреждения возвращаются в псетколумнс- \> Error, а не в коде возврата этой функции. Однако если в последнем наборе столбцов есть предупреждение, это предупреждение будет возвращаться из самого **жетсетколумнс** .

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
</tbody>
</table>


#### <a name="see-also"></a>См. также:

[JET_COLTYP](./jet-coltyp.md)  
[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_SETCOLUMN](./jet-setcolumn-structure.md)  
[жетретриевеколумнс](./jetretrievecolumns-function.md)  
[жетсетколумн](./jetsetcolumn-function.md)
