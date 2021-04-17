---
description: Дополнительные сведения о функции Жетделете
title: Функция JetDelete
TOCTitle: JetDelete Function
ms:assetid: 807de5ba-2f4b-4779-ab29-a1f094beecc1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269315(v=EXCHG.10)
ms:contentKeyID: 32765605
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDelete
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9f3422bc623bbd4f0cc99365df51bb797100811c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647515"
---
# <a name="jetdelete-function"></a>Функция JetDelete


_**Применимо к:** Windows | Windows Server_

## <a name="jetdelete-function"></a>Функция JetDelete

Функция **жетделете** удаляет текущую запись в таблице базы данных.

```cpp
    JET_ERR JET_API JetDelete(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid
    );
```

### <a name="parameters"></a>Параметры

*сесид*

Контекст сеанса базы данных, который будет использоваться для вызова API.

*TableID*

Курсор в таблице базы данных. Текущая строка будет удалена.

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
<td><p>JET_errCallbackFailed</p></td>
<td><p>Ошибка функции обратного вызова. Например, нарушения прав доступа в функциях обратного вызова перехватываются и преобразуются в JET_errCallbackFailed. Эта ошибка будет возвращена только Windows XP и более поздних версий.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIllegalOperation</p></td>
<td><p>Курсор, указанный функцией <em>tableid</em> , не поддерживает удаление. См. раздел «Примечания».</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных. Эта ошибка будет возвращена только Windows XP и более поздних версий.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>Курсор, заданный параметром <em>tableid</em> , не находится в записи.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errPermissionDenied</p></td>
<td><p>Ядро СУБД не имеет достаточных разрешений для удаления записи. Это может произойти, если файл базы данных был открыт с доступом только для чтения.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRollbackError</p></td>
<td><p>Буфер обновления (см. <a href="gg269339(v=exchg.10).md">жетпрепареупдате</a>) существует, но не все изменения, внесенные в столбцы типа JET_coltypLongText и (или) столбцы типа JET_coltypLongBinary, могут быть отменены.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Нельзя одновременно использовать один сеанс из нескольких потоков. Эта ошибка будет возвращена только Windows XP и более поздних версий.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTransReadOnly</p></td>
<td><p>Транзакция является транзакцией только для чтения и не поддерживает удаления.</p></td>
</tr>
<tr class="even">
<td><p>JET_errVersionStoreOutOfMemory</p></td>
<td><p>Не удалось выполнить операцию, так как недостаточно памяти для удержания транзакционных сведений об обновлении.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errWriteConflict</p></td>
<td><p>Другой сеанс ранее заблокировал запись для обновления. Обновление, которое попыталось этот сеанс, завершится ошибкой.</p></td>
</tr>
</tbody>
</table>


В случае успеха валюта остается непосредственно перед следующей записью. Если удаленная запись была последней в таблице, то валюта остается в конце таблицы (то есть после новой записи). Если удаленная запись была единственной записью в таблице, то в качестве валюты устанавливается начало.

Соответствующие индексы обновляются автоматически.

Если обновление подготовлено (с помощью [жетпрепареупдате](./jetprepareupdate-function.md)), оно будет отменено. Буфер обновления будет сброшен.

В случае сбоя валюта остается неизменной. Если обновление подготовлено (см. [жетпрепареупдате](./jetprepareupdate-function.md)), буфер обновления может быть сброшен.

#### <a name="remarks"></a>Комментарии

Не все таблицы поддерживают удаление строк. Как правило, временная таблица не поддерживает удаление строк. Удаление записей может быть включено во временных таблицах по многим причинам:

  - JET_bitTTUpdatable был указан во время создания.

  - Большие временные таблицы могут поддерживать удаление, если они были созданы с помощью JET_bitTTScrollable или JET_bitTTIndexed. Пороговое значение, при достижении которого временная таблица становится "большим", в настоящее время составляет 64 килобайт, но может быть изменено в будущих выпусках.

Windows XP и более поздние версии. Функции обратного вызова могут вызываться **жетделете**, включая JET_cbtypBeforeDelete и JET_cbtypAfterDelete.

Важно понимать влияние выполнения большого количества операций обновления в рамках одной транзакции. Каждое обновление базы данных должно быть отслеживанием ядра СУБД в хранилище версий. Хранилище версий содержит активную запись всех различных версий каждой записи или записи индекса в базе данных, которые могут быть видны всем активным транзакциям. Эти версии используются для поддержки управления параллелизмом с несколькими версиями, используемого ядром СУБД для поддержки транзакций с использованием изоляции моментальных снимков. После того, как ядро СУБД исчерпало ресурсы, используемые для хранения этих версий, оно больше не сможет принять дальнейшие изменения до тех пор, пока некоторые транзакции не разрешают высвободить эти ресурсы. Если обработчик находится в этом состоянии, все обновления будут завершаться с JET_errVersionStoreOutOfMemory. Ресурсы, доступные ядру СУБД для хранения этих версий, можно контролировать с помощью [жетсетсистемпараметер](./jetsetsystemparameter-function.md) с *JET_paramMaxVerPages* и *JET_paramGlobalMinVerPages*.

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

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[жетопентемптабле](./jetopentemptable-function.md)  
[жетпрепареупдате](./jetprepareupdate-function.md)  
[Системные параметры](./extensible-storage-engine-system-parameters.md)
