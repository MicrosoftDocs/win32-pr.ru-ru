---
description: Дополнительные сведения о функции Жетжеткурсоринфо
title: Функция Жетжеткурсоринфо
TOCTitle: JetGetCursorInfo Function
ms:assetid: e779fa5d-1d7e-46f1-80c9-f7c819279188
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294126(v=EXCHG.10)
ms:contentKeyID: 32765740
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetCursorInfo
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7201c37f79f68deead837cdcdd90402e4b2bf1e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105656714"
---
# <a name="jetgetcursorinfo-function"></a>Функция Жетжеткурсоринфо


_**Применимо к:** Windows | Windows Server_

## <a name="jetgetcursorinfo-function"></a>Функция Жетжеткурсоринфо

Функция **жетжеткурсоринфо** используется для определения того, что обновление текущей записи курсора приведет к конфликту записи, в зависимости от текущего состояния обновления записи. Возможно, конфликт записи будет возвращен, даже если **жетжеткурсоринфо** возвращает JET_errSuccess, так как другой сеанс может обновить запись, прежде чем текущий сеанс сможет обновить ту же запись.

```cpp
    JET_ERR JET_API JetGetCursorInfo(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a>Параметры

*сесид*

Сеанс, который будет использоваться для этого вызова.

*TableID*

Курсор, который будет использоваться для этого вызова.

*пвресулт*

Зарезервировано для последующего использования.

*кбмакс*

Значение должно быть равно 0 (нулю); в противном случае — неиспользуемое. Он имеется для будущих функций.

*инфолевел*

Значение должно быть равно 0 (нулю); в противном случае — неиспользуемое. Он имеется для будущих функций.

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
<td><p>JET_errInvalidParameter</p></td>
<td><p>Значение <em>кбмакс</em> не равно 0 (ноль) или <em>инфолевел</em> не равно 0 (нулю).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>Курсор в настоящий момент не находится в записи, и данные логической записи не могут быть возвращены в результате.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</p></td>
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
<td><p>JET_errWriteConflict</p></td>
<td><p>Текущая запись курсора была обновлена другим сеансом, и обновление этой записи на этом сеансе приведет к конфликту записи.</p></td>
</tr>
</tbody>
</table>


При успешном выполнении эта операция не оказывает влияния на расположение курсора, но только указывает на то, что ни один другой сеанс не обновил эту запись в настоящее время.

При сбое, если возвращается отрицательный код ошибки, в курсор или базу данных ничего не происходит.

#### <a name="remarks"></a>Комментарии

Эта операция не влияет на состояние курсора или данных. Он возвращает только код ошибки, описывающий, является ли обновление текущей записи вызывающим сеансом результатом JET_errWriteConflict или неизвестное значение для возвращения JET_errWriteConflict. Если другой сеанс уже обновил эту запись для использования, убедитесь, что обновление этой записи в этом сеансе приведет к конфликту записи. Это будет иметь значение true, пока этот сеанс не зафиксирует или не произведет откат своих транзакций до уровня транзакций 0 (ноль). Однако если **жетжеткурсоринфо** возвращает JET_errSuccess, другой сеанс по-прежнему может обновить эту запись до текущего сеанса, и поэтому по-прежнему возможно, что обновление текущей записи на этом сеансе в текущей транзакции приведет к конфликту записи.

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
[жетжетлокк](./jetgetlock-function.md)  
[жетпрепареупдате](./jetprepareupdate-function.md)  
[жетстопсервице](./jetstopservice-function.md)  
[жетупдате](./jetupdate-function.md)
