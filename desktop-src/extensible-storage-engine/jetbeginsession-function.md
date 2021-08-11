---
description: Дополнительные сведения о функции Жетбегинсессион
title: Функция JetBeginSession
TOCTitle: JetBeginSession Function
ms:assetid: f1c33b78-f2d1-44ea-8ec9-94b729b94e24
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294131(v=EXCHG.10)
ms:contentKeyID: 32765745
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBeginSessionA
- JetBeginSession
- JetBeginSessionW
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0852de04f3969e3e30debc7ba7ff4f3aedf7ac4084b17f91feed8984fe4e1467
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118251618"
---
# <a name="jetbeginsession-function"></a>Функция JetBeginSession


_**Применимо к:** Windows | Windows Сервером_

## <a name="jetbeginsession-function"></a>Функция JetBeginSession

Функция **жетбегинсессион** запускает сеанс и инициализирует и возвращает обработчик сеанса ESE ([JET_SESID](./jet-sesid.md)). Сеансы управляют всем доступом к базе данных и используются для управления областью транзакций. Сеанс можно использовать для начала, фиксации или прерывания транзакций. Сеанс также используется для присоединения, создания или открытия базы данных. Сеанс используется в качестве контекста для всех операций DDL и DML. Чтобы увеличить параллелизм и параллельный доступ к базе данных, можно приступило к нескольким сеансам.

```cpp
    JET_ERR JET_API JetBeginSession(
      __in          JET_INSTANCE instance,
      __out         JET_SESID* psesid,
      __in_opt      JET_PCSTR szUserName,
      __in_opt      JET_PCSTR szPassword
    );
```

### <a name="parameters"></a>Параметры

*вхождение*

Экземпляр базы данных, используемый для этого вызова.

*псесид*

Указатель на переменную, которую обработчик сеанса инициализирует при успешном возвращении.

*сзусернаме*

Этот параметр зарезервирован.

*сзпассворд*

Этот параметр зарезервирован.

### <a name="return-value"></a>Возвращаемое значение

Эта функция позволяет возвратить любые [JET_ERR](./jet-err.md)s, определенные в этом API. дополнительные сведения об ошибках Jet см. в разделе [расширенные ошибки служба хранилища Engine](./extensible-storage-engine-errors.md) и [параметры обработки ошибок](./error-handling-parameters.md).

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
<td><p>Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</p>
<p>эта ошибка будет возвращена только Windows XP и более поздних выпусках.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Один из указанных параметров содержит непредвиденное значение или содержит значение, которое не имеет смысла при объединении со значением другого параметра.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfMemory</p></td>
<td><p>Не удалось выполнить операцию, так как не удалось выделить память.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfSessions</p></td>
<td><p>Число сеансов, которые ядро позволит запустить, ограничено. Это значение можно изменить с помощью <a href="gg294044(v=exchg.10).md">жетсетсистемпараметер</a> с константой JET_paramMaxSessions. Число сеансов по умолчанию — 16. Дополнительные сведения о JET_paramMaxSessions см. в разделе <a href="gg294139(v=exchg.10).md">системные параметры</a> .</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</p></td>
</tr>
</tbody>
</table>


При успешном выполнении обработчик сеанса инициализируется и может использоваться для операций базы данных.

В случае сбоя отсутствуют доступные сеансы или не удалось инициализировать новый сеанс.

#### <a name="remarks"></a>Remarks

При использовании сеансов в разных потоках необходимо тщательное внимание. Сеанс отслеживает, какой поток использовался во время [жетбегинтрансактион](./jetbegintransaction-function.md), [жеткоммиттрансактион](./jetcommittransaction-function.md)или [жетроллбакк](./jetrollback-function.md), и при использовании в нескольких потоках с открытой транзакцией возникает ошибка. [Жетресетсессионконтекст](./jetresetsessioncontext-function.md), [жетсетсессионконтекст](./jetsetsessioncontext-function.md) может изменить это поведение. Так как сеанс по-прежнему является сериализованным контекстом, и несколько операций с базой данных не могут выполняться одновременно в одном сеансе, только последовательно. Однако можно использовать несколько сеансов для достижения параллельного доступа к базе данных. Сеансы можно использовать внутри транзакции в потоках путем установки и сброса контекстов сеанса.

Обработчик сеанса должен быть закрыт с помощью [жетендсессион](./jetendsession-function.md).

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
<td><p><strong>Server</strong></p></td>
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
<td><p>Реализуется как <strong>жетбегинсессионв</strong> (Юникод) и <strong>жетбегинсессиона</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>См. также:

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_SESID](./jet-sesid.md)  
[жетбегинтрансактион](./jetbegintransaction-function.md)  
[жеткоммиттрансактион](./jetcommittransaction-function.md)  
[жетдупсессион](./jetdupsession-function.md)  
[жетендсессион](./jetendsession-function.md)  
[жетресетсессионконтекст](./jetresetsessioncontext-function.md)  
[жетроллбакк](./jetrollback-function.md)  
[жетсетсессионконтекст](./jetsetsessioncontext-function.md)  
[жетстопсервице](./jetstopservice-function.md)  
[Системные параметры](./extensible-storage-engine-system-parameters.md)
