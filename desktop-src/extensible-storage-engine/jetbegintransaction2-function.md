---
description: Дополнительные сведения о функции JetBeginTransaction2
title: Функция JetBeginTransaction2
TOCTitle: JetBeginTransaction2 Function
ms:assetid: 638af3f1-b342-46bd-9fd0-dc281936355c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269268(v=EXCHG.10)
ms:contentKeyID: 32765570
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBeginTransaction
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d2d62a5d39f82771aa72b74aab5af14c617ffa90
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985107"
---
# <a name="jetbegintransaction2-function"></a>Функция JetBeginTransaction2


_**Применимо к:** Windows | Windows Сервером_

## <a name="jetbegintransaction2-function"></a>Функция JetBeginTransaction2

Функция **JetBeginTransaction2** заставляет сеанс войти в транзакцию и создать новую точку сохранения. Эту функцию можно вызвать несколько раз в одном сеансе, чтобы создать дополнительные точки сохранения. Эти точки сохранения можно использовать для выборочного сохранения или отмены изменений в базе данных.

```cpp
    JET_ERR JET_API JetBeginTransaction2(
      __in          JET_SESID sesid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Параметры

*сесид*

Сеанс, используемый для этого вызова.

*грбит*

Группа битов, содержащая параметры, которые должны использоваться для этого вызова, включая ноль или более следующих значений.


| <p>Значение</p> | <p>Значение</p> | 
|--------------|----------------|
| <p>JET_bitTransactionReadOnly</p> | <p>Транзакция не изменит базу данных. При попытке обновления эта операция завершится ошибкой с JET_errTransReadOnly. Этот параметр игнорируется, если он не запрашивается, если данный сеанс еще не находится в транзакции. этот параметр доступен только для Windows XP.</p> | 



### <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата. дополнительные сведения о возможных ошибках подсистемы ESE см. в разделе [ошибки расширенных служба хранилища Engine](./extensible-storage-engine-errors.md) и [параметры обработки ошибок](./error-handling-parameters.md).


| <p>Код возврата</p> | <p>Описание</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Операция выполнена успешно.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</p><p>эта ошибка будет возвращена только Windows XP и более поздних выпусках.</p> | 
| <p>JET_errNotInitialized</p> | <p>Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>Один и тот же сеанс нельзя использовать одновременно для нескольких потоков. эта ошибка будет возвращена только Windows XP и более поздних выпусках.</p> | 
| <p>JET_errTermInProgress</p> | <p>Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</p> | 
| <p>JET_errTransTooDeep</p> | <p>Не удается запустить новую транзакцию, так как сеанс уже находится в максимально допустимой глубины точки сохранения в ядре СУБД.</p> | 



При успешном выполнении указанный сеанс будет находиться внутри транзакции. Если сеанс был ранее внутри транзакции, будет создана новая точка сохранения.

В случае сбоя состояние транзакции сеанса останется неизменным. Изменение состояния базы данных не выполняется.

#### <a name="remarks"></a>Комментарии

Дополнительные сведения о работе транзакций см. в разделе [жетбегинтрансактион](./jetbegintransaction-function.md).

#### <a name="requirements"></a>Требования


| Требование | Применение |
|------------|----------|
| <p><strong>Клиент</strong></p> | <p>требуется Windows Vista, Windows XP или Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>требуется Windows server 2008, Windows server 2003 или сервер Windows 2000.</p> | 
| <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | 
| <p><strong>Библиотека</strong></p> | <p>Используйте ESENT. lib.</p> | 
| <p><strong>КОМПОНОВКИ</strong></p> | <p>Требуется ESENT.dll.</p> | 



#### <a name="see-also"></a>См. также:

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[жетбегинтрансактион](./jetbegintransaction-function.md)  
[жеткоммиттрансактион](./jetcommittransaction-function.md)  
[жетжетсистемпараметер](./jetgetsystemparameter-function.md)  
[жетресетсессионконтекст](./jetresetsessioncontext-function.md)  
[жетроллбакк](./jetrollback-function.md)  
[жетсетсессионконтекст](./jetsetsessioncontext-function.md)  
[Системные параметры](./extensible-storage-engine-system-parameters.md)
