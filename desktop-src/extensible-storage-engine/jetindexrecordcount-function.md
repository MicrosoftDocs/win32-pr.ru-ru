---
description: Дополнительные сведения о функции Жетиндексрекордкаунт
title: Функция Жетиндексрекордкаунт
TOCTitle: JetIndexRecordCount Function
ms:assetid: 62d39738-cd91-4cfb-9483-f4a2dd845d9a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269267(v=EXCHG.10)
ms:contentKeyID: 32765569
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetIndexRecordCount
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3324ad2fe68d106c7f4d2dcdcd1c3dd6ddefd608
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539978"
---
# <a name="jetindexrecordcount-function"></a>Функция Жетиндексрекордкаунт


_**Применимо к:** Windows | Windows Server_

## <a name="jetindexrecordcount-function"></a>Функция Жетиндексрекордкаунт

Функция **жетиндексрекордкаунт** подсчитывает количество записей в текущем индексе до текущей позиции вперед. Текущая позицией включается в число. Число может быть больше, чем общее число записей в таблице, если текущий индекс находится над многозначным столбцом, а экземпляры столбца имеют несколько значений. Если таблица пуста, для счетчика будет возвращено значение 0.

```cpp
    JET_ERR JET_API JetIndexRecordCount(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         unsigned long* pcrec,
      __in          unsigned long crecMax
    );
```

### <a name="parameters"></a>Параметры

*сесид*

Сеанс, используемый для этого вызова.

*TableID*

Курсор, используемый для этого вызова.

*пкрек*

Указатель на длинное значение без знака для получения счетчика.

*крекмакс*

Максимальное число записей для подсчета. Значение *крекмакс* , равное 0, указывает на то, что число не ограничено.

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
<td><p>Операция не может быть завершена, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Операция не может быть завершена, так как экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</p>
<p><strong>Windows XP:</strong>  Это возвращаемое значение введено в Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>Курсор в настоящий момент не находится в записи, и таблица не пуста.</p>
<p><strong>Windows XP, Windows Server 2003, windows 2000 Server и windows 2000 Professional:</strong>  Если курсор располагается на пустом индексе или диапазоне индекса, <strong>жетиндексрекордкаунт</strong> ошибочно возвращает JET_errNoCurrentRecord.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Операция не может быть завершена, так как экземпляр, связанный с сеансом, еще не инициализирован.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Операция не может быть завершена, так как выполняется операция восстановления на экземпляре, связанном с сеансом.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Один и тот же сеанс нельзя использовать одновременно для нескольких потоков.</p>
<p><strong>Windows XP:</strong>  Это возвращаемое значение введено в Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Не удается выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</p></td>
</tr>
</tbody>
</table>


Если эта функция выполнена, точное число записей индекса, включая текущую и до *крекмакс* (если оно не равно 0), возвращается в неподписанном длинном виде, на который указывает *пкрек*.

Если эта функция завершается ошибкой, в память, выделенную в *прекпос*, не вносятся изменения.

#### <a name="remarks"></a>Комментарии

Если таблица не пуста, то курсор должен быть размещен на записи, с которой начинается подсчет. Количество будет включать эту запись и подсчитывать до заданного предела в *крекмакс*. Если значение *крекмакс* равно 0, операция будет продолжать подсчета до конца индекса.

Диапазоны индексов можно использовать для создания искусственных ограничений на конец индекса для счетчика. Таким образом, поддиапазоны индекса можно полностью подсчитать. Курсор должен располагаться в первой строке диапазона. Должен быть выполнен конец ключа диапазона, а затем [жетсетиндексранже](./jetsetindexrange-function.md) должен использоваться для задания верхнего диапазона, включающего или исключительного. Наконец, **жетиндексрекордкаунт** должен быть вызван для точного подсчета диапазона.

**Жетиндексрекордкаунт** подчиняется семантике транзакции и возвращает счетчик, который является точным для этого конкретного сеанса в текущем состоянии транзакции.

**Жетиндексрекордкаунт** обращается к конечным страницам индекса для точного подсчета записей. Следовательно, она может выполнять большую часть операций ввода-вывода и может быть достаточно высокой. Для предотвращения чрезмерной нагрузки следует использовать ограничение *крекмакс* . Если диапазон большой, то можно будет подсчитать диапазон приблизительным способом с помощью [жетжетрекордпоситион](./jetgetrecordposition-function.md).

**Windows XP, Windows Server 2003, windows 2000 Server и windows 2000 Professional:**  Если курсор располагается на пустом индексе или диапазоне индекса, **жетиндексрекордкаунт** возвращает JET_errNoCurrentRecord, а не возвращается число записей, равное нулю. Приложение должно проверить, пуст ли индекс или диапазон индекса в этом случае.

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
[жетжетрекордпоситион](./jetgetrecordposition-function.md)  
[жетсетиндексранже](./jetsetindexrange-function.md)  
[жетстопсервице](./jetstopservice-function.md)
