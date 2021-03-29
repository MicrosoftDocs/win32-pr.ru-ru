---
description: Дополнительные сведения о функции Жетготопоситион
title: Функция Жетготопоситион
TOCTitle: JetGotoPosition Function
ms:assetid: 77b099f1-4a21-4ddb-b269-83ca74219b4d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269300(v=EXCHG.10)
ms:contentKeyID: 32765592
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGotoPosition
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: aae5148431ad46c5a75bbd804f2c0d777b279561
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808440"
---
# <a name="jetgotoposition-function"></a>Функция Жетготопоситион


_**Применимо к:** Windows | Windows Server_

## <a name="jetgotoposition-function"></a>Функция Жетготопоситион

Функция **жетготопоситион** перемещает курсор на новое место, которое представляет собой часть пути по текущему индексу. Дробная часть приблизительно равна следующей:

прекпос- \> центриеслт/прекпос- \> центриестотал

Эта операция выполняется в ответ на ввод поля полосы прокрутки пользователя, полученного при попытке пользователя отобразить данные, которые начинаются с помощью набора данных.

```cpp
    JET_ERR JET_API JetGotoPosition(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_RECPOS* precpos
    );
```

### <a name="parameters"></a>Параметры

*сесид*

Сеанс, используемый для этого вызова.

*TableID*

Курсор, используемый для этого вызова.

*прекпос*

Описание доли, используемой при размещении курсора в текущем индексе.

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
<td><p>Не удалось выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Не удалось выполнить операцию, так как экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</p>
<p><strong>Windows XP:</strong>  Это возвращаемое значение введено в Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Заданный прекпос- &gt; кбструкт не является допустимым размером для структуры <a href="gg269308(v=exchg.10).md">JET_RECPOS</a> , или прекпос- &gt; центриеслт больше прекпос- &gt; центриестотал.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Операция не может быть завершена, так как экземпляр, связанный с сеансом, еще не инициализирован.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRecordNotFound</p></td>
<td><p>Эта ошибка будет возвращена, если индекс пуст.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Операция не может быть завершена, так как выполняется операция восстановления на экземпляре, связанном с сеансом.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Один и тот же сеанс нельзя использовать одновременно для нескольких потоков.</p>
<p><strong>Windows XP:</strong>  Это возвращаемое значение введено в Windows XP.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Не удается выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</p></td>
</tr>
</tbody>
</table>


Если эта функция завершилась с ошибкой, курсор перемещается на текущую запись, которая является долей пути, где дробь прекпос- \> центриеслт делится на прекпос- \> центриестотал.

Если эта функция завершается ошибкой, расположение курсора остается без изменений.

#### <a name="remarks"></a>Комментарии

Эта операция перемещает курсор через таблицу в позицию в следующей приблизительной точке: прекпос- \> центриеслт, деленную на прекпос- \> центриестотал.

При постоянном обновлении таблицы Последующие вызовы с тем же [JET_RECPOS](./jet-recpos-structure.md) могут перемещать курсор на разные позиции в индексе до и после предыдущей позиции. Изоляция транзакций не применяется к размещению по [JET_RECPOS](./jet-recpos-structure.md) , поскольку она зависит от физических свойств индекса, которые не изолированы от транзакции.

[JET_RECPOS](./jet-recpos-structure.md) не следует использовать для описания записи в таблице или перемещения записи, близкой к существующей записи. Вместо этого закладки для существующей записи должны быть получены после первоначального **жетготопоситион** , а затем использоваться для перемещения той же записи.

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

[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_RECPOS](./jet-recpos-structure.md)  
[JET_SETINFO](./jet-setinfo-structure.md)
