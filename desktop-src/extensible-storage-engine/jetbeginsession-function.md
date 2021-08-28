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
ms.openlocfilehash: 3e6263916211e5d21e0032ba6de8d98e46fedfa9
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122989077"
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


| <p>Код возврата</p> | <p>Описание</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Операция выполнена успешно.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</p><p>эта ошибка будет возвращена только Windows XP и более поздних выпусках.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Один из указанных параметров содержит непредвиденное значение или содержит значение, которое не имеет смысла при объединении со значением другого параметра.</p> | 
| <p>JET_errNotInitialized</p> | <p>Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</p> | 
| <p>JET_errOutOfMemory</p> | <p>Не удалось выполнить операцию, так как не удалось выделить память.</p> | 
| <p>JET_errOutOfSessions</p> | <p>Число сеансов, которые ядро позволит запустить, ограничено. Это значение можно изменить с помощью <a href="gg294044(v=exchg.10).md">жетсетсистемпараметер</a> с константой JET_paramMaxSessions. Число сеансов по умолчанию — 16. Дополнительные сведения о JET_paramMaxSessions см. в разделе <a href="gg294139(v=exchg.10).md">системные параметры</a> .</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</p> | 
| <p>JET_errTermInProgress</p> | <p>Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</p> | 



При успешном выполнении обработчик сеанса инициализируется и может использоваться для операций базы данных.

В случае сбоя отсутствуют доступные сеансы или не удалось инициализировать новый сеанс.

#### <a name="remarks"></a>Комментарии

При использовании сеансов в разных потоках необходимо тщательное внимание. Сеанс отслеживает, какой поток использовался во время [жетбегинтрансактион](./jetbegintransaction-function.md), [жеткоммиттрансактион](./jetcommittransaction-function.md)или [жетроллбакк](./jetrollback-function.md), и при использовании в нескольких потоках с открытой транзакцией возникает ошибка. [Жетресетсессионконтекст](./jetresetsessioncontext-function.md), [жетсетсессионконтекст](./jetsetsessioncontext-function.md) может изменить это поведение. Так как сеанс по-прежнему является сериализованным контекстом, и несколько операций с базой данных не могут выполняться одновременно в одном сеансе, только последовательно. Однако можно использовать несколько сеансов для достижения параллельного доступа к базе данных. Сеансы можно использовать внутри транзакции в потоках путем установки и сброса контекстов сеанса.

Обработчик сеанса должен быть закрыт с помощью [жетендсессион](./jetendsession-function.md).

#### <a name="requirements"></a>Требования


| Требование | Применение |
|------------|----------|
| <p><strong>Клиент</strong></p> | <p>требуется Windows Vista, Windows XP или Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>требуется Windows server 2008, Windows server 2003 или сервер Windows 2000.</p> | 
| <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | 
| <p><strong>Библиотека</strong></p> | <p>Используйте ESENT. lib.</p> | 
| <p><strong>КОМПОНОВКИ</strong></p> | <p>Требуется ESENT.dll.</p> | 
| <p><strong>Юникод</strong></p> | <p>Реализуется как <strong>жетбегинсессионв</strong> (Юникод) и <strong>жетбегинсессиона</strong> (ANSI).</p> | 



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
