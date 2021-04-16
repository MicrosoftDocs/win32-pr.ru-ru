---
description: Дополнительные сведения о функции Жетдупкурсор
title: Функция JetDupCursor
TOCTitle: JetDupCursor Function
ms:assetid: 154b7d2d-4656-46b3-873c-2e194a9059b4
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269193(v=EXCHG.10)
ms:contentKeyID: 32765496
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDupCursor
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 590b9b08c5386aaf1cd2dd541ac496a5fa0871d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712727"
---
# <a name="jetdupcursor-function"></a>Функция JetDupCursor


_**Применимо к:** Windows | Windows Server_

## <a name="jetdupcursor-function"></a>Функция JetDupCursor

Функция **жетдупкурсор** дублирует открытый курсор и возвращает указатель на дублирующийся курсор. Если курсор, который был продублирован, был курсором только для чтения, то дубликат курсора также является курсором только для чтения. Любое состояние, связанное с построением ключа поиска или обновлением записи, не копируется в дублирующийся курсор. Кроме того, положение исходного курсора не дублируется в повторяющемся курсоре. Дубликат курсора всегда открывается в кластеризованном индексе, и его расположение всегда находится в первой строке таблицы.

```cpp
    JET_ERR JET_API JetDupCursor(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_TABLEID* ptableid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Параметры

*сесид*

Сеанс, используемый для этого вызова.

*TableID*

Курсор, используемый для этого вызова.

*pTableID*

Указатель на *tableid*.

*грбит*

Зарезервировано для последующего использования.

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
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных. Эта ошибка будет возвращена только Windows XP и более поздних версий.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfCursors</p></td>
<td><p>Нет доступных ресурсов курсора.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Один и тот же сеанс нельзя использовать одновременно для нескольких потоков. Эта ошибка будет возвращена только Windows XP и более поздних версий.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</p></td>
</tr>
</tbody>
</table>


При успешном выполнении *pTableID* задается дубликат курсора.

В случае сбоя изменения не вносятся. Состояние *tableid* не изменяется.

#### <a name="remarks"></a>Комментарии

Для повторяющегося курсора не скопировано полное состояние курсора. Расположение повторяющегося курсора, включая текущий индекс, обычно отличается от указанного курсора. Дубликат курсора всегда возвращается в кластеризованном индексе и в первой строке таблицы. Если таблица пуста, то дублирующийся курсор не находится ни в одной строке.

Таблицы, открытые с помощью **жетдупкурсор** , обычно должны быть закрыты с помощью [жетклосетабле](./jetclosetable-function.md). Исключение из этого правила происходит при вызове **жетдупкурсор** в транзакции и откате транзакции (WITH [жетроллбакк](./jetrollback-function.md)). При откате транзакции курсор автоматически закрывается. В этом случае возникает ошибка при закрытии таблицы с помощью [жетклосетабле](./jetclosetable-function.md).

Количество таблиц, которые могут быть открыты одновременно, повлияет непосредственно на [JET_paramMaxOpenTables](./resource-parameters.md). Дополнительные сведения см. в разделе [системные параметры](./extensible-storage-engine-system-parameters.md) .

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

[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[жетклосетабле](./jetclosetable-function.md)  
[жетроллбакк](./jetrollback-function.md)  
[жетстопсервице](./jetstopservice-function.md)  
[Системные параметры](./extensible-storage-engine-system-parameters.md)
