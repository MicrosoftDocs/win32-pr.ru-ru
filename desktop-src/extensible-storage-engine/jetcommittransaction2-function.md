---
description: Дополнительные сведения о функции JetCommitTransaction2
title: Функция JetCommitTransaction2
TOCTitle: JetCommitTransaction2 Function
ms:assetid: 55b89f8e-7073-4fc2-bf97-103b4bc45e1c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835041(v=EXCHG.10)
ms:contentKeyID: 49894663
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetCommitTransaction2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 24dfecd091de027f51ed8f69c0441fbc7cbd57af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712870"
---
# <a name="jetcommittransaction2-function"></a>Функция JetCommitTransaction2


_**Применимо к:** Windows | Windows Server_

Функция **JetCommitTransaction2** фиксирует изменения, внесенные в состояние базы данных во время текущей точки сохранения, и переносит их в предыдущую точку сохранения. При фиксации самой внешней точки сохранения изменения, внесенные во время этой точки сохранения, будут зафиксированы в состоянии базы данных, и сеанс завершит транзакцию.

Функция **JetCommitTransaction2** была введена в операционной системе Windows 8.

``` c++
JET_ERR JET_API JetCommitTransaction2(
  __in          JET_SESID sesid,
  __in          JET_GRBIT grbit,
  __in          DWORD cmsecDurableCommit,
  __out         JET_COMMIT_ID pCommitID
);
```

### <a name="parameters"></a>Параметры

*сесид*

Сеанс, используемый для этого вызова.

*грбит*

Группа битов, задающих ноль или более значений, перечисленных в следующей таблице.

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
<td><p>JET_bitCommitLazyFlush</p></td>
<td><p>Транзакция фиксируется обычным образом, но этот API не ждет сброса транзакции в файл журнала транзакций перед возвратом вызывающему объекту. Это радикально сокращает продолжительность операции фиксации за счет устойчивости. Любая транзакция, которая не записывается в журнал до сбоя, будет автоматически прервана во время восстановления после сбоя во время следующего вызова функции <a href="gg294068(v=exchg.10).md">жетинит</a> .</p>
<p>Если указаны JET_bitWaitLastLevel0Commit или JET_bitWaitAllLevel0Commit, этот параметр игнорируется.</p>
<p>Если этот вызов к <strong>JetCommitTransaction2</strong> не соответствует первому вызову функции <a href="gg294083(v=exchg.10).md">жетбегинтрансактион</a> для этого сеанса, этот параметр игнорируется. Это связано с тем, что последнее действие, выполняемое на самой внешней точке сохранения, является определяющим фактором в том, фиксируется ли вся транзакция на диске.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitWaitAllLevel0Commit</p></td>
<td><p>Все транзакции, ранее зафиксированные любым сеансом, которые еще не были сброшены в файл журнала транзакций, будут сброшены немедленно. Этот API будет ожидать, пока транзакции не будут сброшены перед возвратом в вызывающий объект.</p>
<p>Этот параметр может использоваться, даже если сеанс в данный момент не находится в транзакции.</p>
<p>Этот параметр нельзя использовать в сочетании с любым другим параметром.</p>
<p>Этот параметр доступен в версиях операционной системы Windows Server, начиная с Windows Server 2003.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitWaitLastLevel0Commit</p></td>
<td><p>Если в сеансе ранее зафиксированы транзакции и они еще не были записаны в файл журнала транзакций, они должны быть сброшены немедленно. Этот API будет ожидать, пока транзакции не будут сброшены перед возвратом в вызывающий объект. Это полезно, если приложение ранее зафиксировало несколько транзакций с помощью JET_bitCommitLazyFlush и теперь хочет сбросить все эти транзакции на диск.</p>
<p>Этот параметр может использоваться, даже если сеанс в данный момент не находится в транзакции.</p>
<p>Этот параметр нельзя использовать в сочетании с любым другим параметром.</p></td>
</tr>
</tbody>
</table>


*кмсекдураблекоммит*

Продолжительность фиксации отложенной транзакции.

*пкоммитид*

Идентификатор фиксации, связанный с этой записью фиксации.

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
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова функции <a href="gg269240(v=exchg.10).md">жетстопсервице</a> .</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</p>
<p>Эта ошибка будет возвращена только версиями операционной системы Windows, начиная с Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>Один из запрошенных параметров недопустим или не реализован. Эта ошибка будет возвращена функцией <strong>JetCommitTransaction2</strong> , когда происходит следующее:</p>
<ul>
<li><p>Указан недопустимый <em>грбит</em> .</p></li>
<li><p>JET_bitWaitLastLevel0Commit был указан в сочетании с другой <em>грбит</em>.</p></li>
<li><p>JET_bitWaitAllLevel0Commit был указан в сочетании с другой <em>грбит</em>.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInTransaction</p></td>
<td><p>Не удалось выполнить операцию, так как данный сеанс не находится в транзакции.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Один и тот же сеанс нельзя использовать одновременно для нескольких потоков.</p>
<p>Эта ошибка будет возвращена только версиями операционной системы Windows, начиная с Windows XP.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</p></td>
</tr>
</tbody>
</table>


При успешном выполнении все изменения, внесенные в базу данных во время текущей точки сохранения для данного сеанса, будут зафиксированы, а точка сохранения будет закончена. Если последняя точка сохранения сеанса была завершена, транзакция при необходимости будет сброшена в файл журнала транзакций, и сеанс завершит транзакцию.

В случае сбоя состояние транзакции сеанса останется неизменным. Изменение состояния базы данных не выполняется. Чтобы прервать транзакцию, приложение должно вызвать функцию [жетроллбакк](./jetrollback-function.md) .

#### <a name="remarks"></a>Комментарии

Должен быть один вызов **JetCommitTransaction2** или [жетроллбакк](./jetrollback-function.md) для сопоставления каждого вызова [жетбегинтрансактион](./jetbegintransaction-function.md) для данного сеанса.

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

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[жетбегинтрансактион](./jetbegintransaction-function.md)  
[жеткоммиттрансактион](./jetcommittransaction-function.md)  
[жетроллбакк](./jetrollback-function.md)  
[жетстопсервице](./jetstopservice-function.md)
