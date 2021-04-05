---
description: Дополнительные сведения о функции Жетсетсессионпараметер
title: Функция Жетсетсессионпараметер
TOCTitle: JetSetSessionParameter Function
ms:assetid: 11aecf42-22ef-4bea-a3d7-961a7bdc85aa
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835038(v=EXCHG.10)
ms:contentKeyID: 49894660
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetSetSessionParameter
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 926ae0db2e47ce571f441ab5836c4ddbe6f8bcc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990980"
---
# <a name="jetsetsessionparameter-function"></a>Функция Жетсетсессионпараметер


_**Применимо к:** Windows | Windows Server_

Функция **жетсетсессионпараметер** настраивает ядро СУБД.

``` c++
JET_ERR JET_API JetSetSessionParameter (
  __in_opt      JET_SESID sesid,
  __in          unsigned long sesparamid,
  __in_read_bytes_opt_(cbParam)  void* pvParam,
  __in          unsigned long cbParam
);
```

### <a name="parameters"></a>Параметры

*сесид*

Указывает сеанс, используемый для этого вызова.

Если этот параметр указан, то указанный экземпляр игнорируется, и будет использоваться экземпляр, связанный с сеансом.

*сеспарамид*

ИДЕНТИФИКАТОР устанавливаемого параметра сеанса.

*пвпарам*

Данные, которые необходимо задать в этом параметре сеанса.

*кбпарам*

Размер предоставленных данных.

### <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает [JET_ERR](./jet-err.md) тип данных с одним из кодов возврата, перечисленных в следующей таблице. Дополнительные сведения о возможных ошибках ESE см. в разделе [Расширенные ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).

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
<td><p>JET_errAlreadyInitialized</p></td>
<td><p>Экземпляр был инициализирован с помощью вызова функции <a href="gg294068(v=exchg.10).md">жетинит</a> , и эта операция не может быть выполнена в результате. Это может произойти при попытке настроить системный параметр после изменения значения параметра, которое больше не может повлиять на состояние ядра СУБД.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова функции <a href="gg269240(v=exchg.10).md">жетстопсервице</a> .</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesInvalidLimits</p></td>
<td><p>Указаны недопустимые параметры индекса кортежа. Эта ошибка возвращается только в том случае, если для параметра <em>JET_paramIndexTuplesLengthMin</em>, <em>JET_paramIndexTuplesLengthMax</em>или <em>JET_paramIndexTuplesToIndexMax</em> задано недопустимое значение. Дополнительные сведения об этих параметрах см. в разделе <a href="gg294119(v=exchg.10).md">Параметры индекса</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInitInProgress</p></td>
<td><p>Невозможно выполнить операцию, так как инициализируется экземпляр, связанный с сеансом.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Один из указанных параметров содержит непредвиденное значение или содержит значение, которое не имеет смысла при объединении со значением другого параметра. Это может произойти, если происходит следующее:</p>
<ul>
<li><p>Указанный идентификатор системного параметра является недопустимым или не поддерживается.</p></li>
<li><p>Предпринята попытка установить системный параметр с строковыми значениями, длина которого находилась вне допустимого диапазона для параметра.</p></li>
<li><p>Предпринята попытка установить системный параметр с символьным значением, где длина его абсолютного пути находилась вне допустимого диапазона для этого параметра.</p></li>
<li><p>Предпринята попытка установить системный параметр с целочисленными значениями, который находится за пределами допустимого диапазона для параметра.</p></li>
<li><p>Предпринята попытка задать JET_paramUnicodeIndexDefault с нулевым указателем <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> , недопустимым LCID или неподдерживаемым набором флагов <strong>LCMapString завершилось ошибкой</strong> .</p></li>
<li><p>Невозможно задать указанный системный параметр, так как он доступен только для чтения.</p></li>
<li><p>Предпринята попытка установить системный параметр после вызова функции <a href="gg294068(v=exchg.10).md">жетинит</a> , ядро СУБД находится в режиме с одним экземпляром, а сеанс не был указан.</p></li>
<li><p>Указанный системный параметр является глобальным, и предпринята попытка задать для этого системного параметра значение конкретного экземпляра.</p></li>
<li><p>Указанный системный параметр доступен только для одного экземпляра, и предпринята попытка установить глобальное значение для этого системного параметра.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidPath</p></td>
<td><p>Указан недопустимый путь к файловой системе. Эта ошибка может возвращаться <strong>жетсетсессионпараметер</strong> только при задании системных параметров, представляющих пути файловой системы. Например, параметр <em>JET_paramSystemPath</em> может возвращать эту ошибку. Дополнительные сведения об этом параметре см. в разделе <a href="gg269235(v=exchg.10).md">Параметры журнала транзакций</a>.</p></td>
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
<td><p>JET_errTermInProgress</p></td>
<td><p>Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidSesid</p></td>
<td><p>Недопустимый обработчик сеанса или ссылается на закрытый сеанс.</p>
<p>Эта ошибка не возвращается при всех обстоятельствах. Дескрипторы проверяются только на основе наилучшей силы.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidInstance</p></td>
<td><p>Недопустимый указатель экземпляра или ссылка на экземпляр, который был закрыт.</p>
<p>Эта ошибка не возвращается при всех обстоятельствах. Дескрипторы проверяются только на основе наилучшей силы.</p></td>
</tr>
</tbody>
</table>


При успешном выполнении параметру System будет присвоено указанное значение.

При сбое значение системного параметра останется неизменным.

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

[JET_API_PTR](./jet-api-ptr.md)  
[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_SESID](./jet-sesid.md)  
[жеткреатеинстанце](./jetcreateinstance-function.md)  
[жетжетсистемпараметер](./jetgetsystemparameter-function.md)  
[жетинит](./jetinit-function.md)  
[Системные параметры](./extensible-storage-engine-system-parameters.md)
