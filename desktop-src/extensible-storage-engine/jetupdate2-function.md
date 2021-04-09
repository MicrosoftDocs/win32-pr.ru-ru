---
description: Дополнительные сведения о функции JetUpdate2
title: Функция JetUpdate2
TOCTitle: JetUpdate2 Function
ms:assetid: 125f372c-9c4c-4be8-b0df-bbf53d79e90b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269190(v=EXCHG.10)
ms:contentKeyID: 32765493
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetUpdate2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cc08b26ebff33a68654ed33a2cb0539af1fa2a91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809005"
---
# <a name="jetupdate2-function"></a>Функция JetUpdate2


_**Применимо к:** Windows | Windows Server_

## <a name="jetupdate2-function"></a>Функция JetUpdate2

Функция **JetUpdate2** выполняет операцию обновления, включая вставку новой строки в таблицу или обновление существующей строки. Эта функция содержит список параметров *грбит* , которые можно задать при выполнении обновления. Удаление строки таблицы выполняется путем вызова [жетделете](./jetdelete-function.md).

**Windows server 2003: JetUpdate2** появился в windows Server 2003.

**JetUpdate2** является последним шагом в выполнении вставки или обновления. Обновление начинается с вызова [жетпрепареупдате](./jetprepareupdate-function.md) , а затем путем вызова [жетсетколумн](./jetsetcolumn-function.md) или [жетсетколумнс](./jetsetcolumns-function.md) один или несколько раз для задания состояния записи. Наконец, для завершения операции обновления вызывается **JetUpdate2** . Индексы обновляются только в [жетупдате](./jetupdate-function.md) или **JetUpdate2**, а не во время [жетсетколумн](./jetsetcolumn-function.md) или [жетсетколумнс](./jetsetcolumns-function.md).

```cpp
    JET_ERR JET_API JetUpdate2(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out_opt     void* pvBookmark,
      __in          unsigned long cbBookmark,
      __out_opt     unsigned long* pcbActual,
      __in            const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Параметры

*сесид*

Сеанс, используемый для этого вызова.

*TableID*

Курсор, используемый для этого вызова.

*пвбукмарк*

Указатель на возвращаемую закладку для вставленной строки.

*кббукмарк*

Размер буфера, на который указывает *пвбукмарк*.

*пкбактуал*

Возвращаемый размер закладки для вставляемой строки, возвращенной в *пвбукмарк*.

*грбит*

Группа битов, содержащая параметры, которые должны использоваться для этого вызова, включая ноль или более следующих значений.

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
<td><p>JET_bitUpdateCheckESE97Compatibility</p></td>
<td><p>Этот флаг приводит к тому, что обновление возвращает ошибку, если в версии ESE для Windows 2000 не было возможно, что применяет меньшее максимальное число экземпляров столбцов с несколькими значениями в каждой записи, чем в более поздних версиях ESE. Это важно только для приложений, которые хотят реплицировать данные между приложениями, размещенными в Windows 2000, и приложениями, размещенными на Windows Server 2003 или более поздних версиях ESE. Это не должно быть необходимо для большинства приложений.</p></td>
</tr>
</tbody>
</table>


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
<td><p>JET_errSuccess</p></td>
<td><p>Операция выполнена успешно.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBufferTooSmall</p></td>
<td><p>Заданный буфер для закладки записи недостаточно велик для хранения закладки записи.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDiskFull</p></td>
<td><p>Операция обновления требует увеличения размера файла базы данных или выделения файла журнала, но диск, на котором находится файл базы данных или ряд журналов, заполнен. Кроме того, файл базы данных находится на томе в формате FAT32, а файл базы данных уже 4GBytes, ограничение на количество файлов для FAT32.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</p>
<p><strong>Windows XP:</strong>  Эта ошибка будет возвращена только Windows XP и более поздних версий.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Данный параметр <em>подготовки</em> в функции <a href="gg269339(v=exchg.10).md">жетпрепареупдате</a> не является допустимым флагом.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errKeyDuplicate</p></td>
<td><p>Ключ индекса для этой записи является дубликатом другого ключа индекса для другой записи, уже наданнымся в таблице, и индекс не допускает дублирования.</p></td>
</tr>
<tr class="even">
<td><p>JET_errKeyTruncated</p></td>
<td><p>Вставленная или обновленная запись имеет один или несколько индексов, для которых созданный ключ превысил максимально допустимый размер. В результате операция не смогла предотвратить усечение ключа.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errMultiValuedIndexViolation</p></td>
<td><p>Вставленная или обновленная запись имеет индексируемый многозначный столбец с двумя или более значениями, идентичными в пределах ключа максимальной длины, установленного для индекса. В результате запись содержит две идентичные записи в индексе, что недопустимо.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNullInvalid</p></td>
<td><p>Один или несколько столбцов вставляемой записи или в обновленном состоянии заменяемой записи имеют <strong>значение NULL</strong> , что нарушает определенное ограничение для этих столбцов.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNullKeyDisallowed</p></td>
<td><p>Один или несколько индексов не позволяют разрешить ключ <strong>null</strong> , а вставленное или обновленное состояние заменяемой записи нарушает это заданное ограничение.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRecordPrimaryChanged</p></td>
<td><p>Операция замены записи обновила первичный ключ. Обновления первичных ключевых столбцов должны выполняться путем удаления существующей записи и вставки новой записи с нужными данными.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Один и тот же сеанс нельзя использовать одновременно для нескольких потоков.</p>
<p><strong>Windows XP:</strong>  Эта ошибка будет возвращена только Windows XP и более поздних версий.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errUpdateNotPrepared</p></td>
<td><p><a href="gg269339(v=exchg.10).md">Жетпрепареупдате</a> был вызван с JET_prepCancel, но курсор не был в подготовленном состоянии.</p></td>
</tr>
<tr class="even">
<td><p>JET_errWriteConflict</p></td>
<td><p>Операция замены записи, для которой не была выделена блокировка записи, может столкнуться с конфликтом записи во время обновления.</p></td>
</tr>
</tbody>
</table>


При успешном выполнении операция открытия обновления курсора завершается. Если для таблицы определен автоматически увеличивающийся столбец, то это значение устанавливается для вставленных записей. Если для таблицы определен столбец версии, то его значение инициализируется для вновь вставленных записей или увеличивается каждый раз при замене записи. Обновляются все индексы, включая кластеризованные и некластеризованные индексы.

В случае сбоя изменения какого либо типа не вносятся в базу данных. Перед вставкой и до замены функции обратного вызова могут быть вызваны, но после вызовов INSERT и After replace не будут вызываться, так как Последнее не может привести к сбою обновления. Буфер копирования курсора остается в подготовленном состоянии, чтобы можно было постепенно устранить проблемы, вызвавшие ошибки, и повторить операцию обновления.

#### <a name="remarks"></a>Комментарии

Ограничения размера записи применяются [жетсетколумн](./jetsetcolumn-function.md), а не в общем [жетупдате](./jetupdate-function.md). Единственным исключением является использование флага совместимости JET_bitUpdateCheckESE97Compatibility. В этом случае проверяется вся запись, так как отдельная операция [жетсетколумн](./jetsetcolumn-function.md) , которая превышает это ограничение, может быть компенсироваться последующим вызовом [жетсетколумн](./jetsetcolumn-function.md).

Дополнительные сведения см. в разделе "Примечания" в [жетупдате](./jetupdate-function.md) .

#### <a name="requirements"></a>Требования

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Клиент</strong></p></td>
<td><p>Требуется Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Требуется Windows Server 2008 или Windows Server 2003.</p></td>
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

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[жетделете](./jetdelete-function.md)  
[жетпрепареупдате](./jetprepareupdate-function.md)  
[жетрегистеркаллбакк](./jetregistercallback-function.md)  
[жетретриевеколумн](./jetretrievecolumn-function.md)  
[жетретриевеколумнс](./jetretrievecolumns-function.md)  
[жетсетколумн](./jetsetcolumn-function.md)  
[жетсетколумнс](./jetsetcolumns-function.md)
