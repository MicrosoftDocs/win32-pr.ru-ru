---
description: Дополнительные сведения о функции Жетстопбаккуп
title: Функция Жетстопбаккуп
TOCTitle: JetStopBackup Function
ms:assetid: b7545284-2fdb-4470-8466-fc2109ad63c5
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294067(v=EXCHG.10)
ms:contentKeyID: 32765682
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetStopBackup
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fd5f7fe7096b0562aa9fc4ce8d15f77a4ccf205f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469701"
---
# <a name="jetstopbackup-function"></a>Функция Жетстопбаккуп


_**Применимо к:** Windows | Windows Сервером_

## <a name="jetstopbackup-function"></a>Функция Жетстопбаккуп

Функция **жетстопбаккуп** предотвращает продолжение любых операций потоковой архивации на определенном работающем экземпляре, тем самым завершая потоковую архивацию предсказуемым образом.

**Windows XP:**  эта функция появилась в Windows XP.

[Жетстопсервице](./jetstopservice-function.md) — это устаревший вызов, если разрешен только один экземпляр. В этом случае единственным активным экземпляром является тот, который подготавливается к завершению.

```cpp
JET_ERR JET_API JetStopBackup(void);
```

### <a name="parameters"></a>Параметры

У этой функции нет параметров.

### <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата. дополнительные сведения о возможных ошибках подсистемы ESE см. в разделе [ошибки расширенных служба хранилища Engine](./extensible-storage-engine-errors.md) и [параметры обработки ошибок](./error-handling-parameters.md).


| <p>Код возврата</p> | <p>Описание</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Операция выполнена успешно.</p> | 
| <p>JET_errRunningInMultiInstanceMode</p> | <p>Не ясно, какой экземпляр подготавливается к завершению при использовании <a href="gg269240(v=exchg.10).md">жетстопсервице</a> в режиме с несколькими экземплярами.</p><p><strong>Windows XP:</strong>  это возвращаемое значение вводится в Windows XP.</p> | 



Если эта функция завершается успешно, экземпляр начнет работать с ошибками новых интерфейсов API потоковой архивации.

Если эта функция завершается ошибкой, то не будет выполнено никаких действий для подготовки к завершению резервного копирования на экземпляре, и изменение состояния экземпляра не будет выполнено.

#### <a name="remarks"></a>Комментарии

Резервное копирование обычно запускается событием за пределами механизма обработки и с помощью этого API, а само приложение ESENT делает все последующие вызовы интерфейсов API потоковой архивации неудачными. Большинство API-интерфейсов потоковой архивации начнут завершаться сбоем с JET_errBackupAbortByServer. Таким образом, любое выполнение потоковой архивации (например, [жетреадфилеинстанце](./jetreadfileinstance-function.md)) вернет ошибку. Операции резервного копирования, которые являются частью завершения резервного копирования (например, [жетендекстерналбаккупинстанце](./jetendexternalbackupinstance-function.md)), по-прежнему будут разрешены.

#### <a name="requirements"></a>Требования


| | | <p><strong>Клиент</strong></p> | <p>требуется Windows Vista, Windows XP или Windows 2000 Professional.</p> | | <p><strong>Сервер</strong></p> | <p>требуется Windows server 2008, Windows server 2003 или сервер Windows 2000.</p> | | <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | | <p><strong>Библиотека</strong></p> | <p>Используйте ESENT. lib.</p> | | <p><strong>КОМПОНОВКИ</strong></p> | <p>Требуется ESENT.dll.</p> | 



#### <a name="see-also"></a>См. также:

[жетендекстерналбаккупинстанце](./jetendexternalbackupinstance-function.md)  
[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[жетреадфилеинстанце](./jetreadfileinstance-function.md)  
[жетстопсервице](./jetstopservice-function.md)
