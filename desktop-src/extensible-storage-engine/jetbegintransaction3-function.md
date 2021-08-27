---
description: Дополнительные сведения о функции JetBeginTransaction3
title: Функция JetBeginTransaction3
TOCTitle: JetBeginTransaction3 Function
ms:assetid: 7f8ed059-0b97-46fa-9925-e46cdcbee6ea
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835043(v=EXCHG.10)
ms:contentKeyID: 49894665
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetBeginTransaction3
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ed7c963da40f72fb7ea54c5614836a1de81a0b3d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479240"
---
# <a name="jetbegintransaction3-function"></a>Функция JetBeginTransaction3


_**Применимо к:** Windows | Windows Сервером_

Функция **JetBeginTransaction3** заставляет сеанс войти в транзакцию и создать новую точку сохранения. Эту функцию можно вызвать несколько раз в одном сеансе, чтобы создать дополнительные точки сохранения. Эти точки сохранения можно использовать для выборочного сохранения или отмены изменений в базе данных.

функция **JetBeginTransaction3** была введена в операционной системе Windows 8.

``` c++
JET_ERR JET_API JetBeginTransaction3(
  __in          JET_SESID sesid,
  __in          int64 trxid,
  __in          JET_GRBIT grbit
);
```

### <a name="parameters"></a>Параметры

*сесид*

Сеанс, используемый для этого вызова.

*трксид*

Необязательный идентификатор, предоставленный пользователем для идентификации транзакции.

*грбит*

Группа битов, которая указывает ноль или более значений параметров вызова, перечисленных в следующей таблице.


| <p>Значение</p> | <p>Значение</p> | 
|--------------|----------------|
| <p>JET_bitTransactionReadOnly</p> | <p>Транзакция не изменит базу данных. При попытке обновления эта операция завершится ошибкой с JET_errTransReadOnly кодом ответа. Этот параметр игнорируется, если он не запрашивается, если данный сеанс еще не находится в транзакции. этот параметр доступен в версиях операционной системы Windows, начиная с Windows XP.</p> | 



### <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает [JET_ERR](./jet-err.md) тип данных с одним из кодов возврата, перечисленных в следующей таблице. дополнительные сведения о служба хранилища возможных ошибках ESE см. в разделе [ошибки расширяемых](./extensible-storage-engine-errors.md) подсистемы служба хранилища и [параметры обработки ошибок](./error-handling-parameters.md).


| <p>Код возврата</p> | <p>Описание</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Операция выполнена успешно.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова функции <a href="gg269240(v=exchg.10).md">жетстопсервице</a> .</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</p><p>этот код возврата возвращается версиями Windows начиная с Windows XP.</p> | 
| <p>JET_errNotInitialized</p> | <p>Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>Один и тот же сеанс нельзя использовать одновременно для нескольких потоков. эта ошибка возвращается версиями Windows начиная с Windows XP.</p> | 
| <p>JET_errTermInProgress</p> | <p>Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</p> | 
| <p>JET_errTransTooDeep</p> | <p>Не удается запустить новую транзакцию, так как сеанс уже находится в максимально допустимой глубины точки сохранения в ядре СУБД.</p> | 



При успешном выполнении указанный сеанс будет находиться внутри транзакции. Если сеанс был ранее в рамках транзакции, будет создана новая точка сохранения.

В случае сбоя состояние транзакции сеанса останется неизменным. Изменение состояния базы данных не выполняется.

#### <a name="remarks"></a>Комментарии

Дополнительные сведения о работе транзакций см. в разделе [жетбегинтрансактион](./jetbegintransaction-function.md).

#### <a name="requirements"></a>Требования


| | | <p><strong>Клиент</strong></p> | <p>Требуется Windows 8.</p> | | <p><strong>Сервер</strong></p> | <p>Требуется Windows Server 2012.</p> | | <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | | <p><strong>Библиотека</strong></p> | <p>Используйте ESENT. lib.</p> | | <p><strong>КОМПОНОВКИ</strong></p> | <p>Требуется ESENT.dll.</p> | 



#### <a name="see-also"></a>См. также

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
