---
description: Дополнительные сведения о функции Жетосснапшотаборт
title: Функция Жетосснапшотаборт
TOCTitle: JetOSSnapshotAbort Function
ms:assetid: 629455af-b526-4366-9b9a-112757f72c32
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269265(v=EXCHG.10)
ms:contentKeyID: 32765567
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotAbort
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7767a1c7e9dc9182fe521d2d903b52d3b88dadb3
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983357"
---
# <a name="jetossnapshotabort-function"></a>Функция Жетосснапшотаборт


_**Применимо к:** Windows | Windows Сервером_

## <a name="jetossnapshotabort-function"></a>Функция Жетосснапшотаборт

Функция **жетосснапшотаборт** уведомляет модуль о том, что он может возобновить нормальные операции ввода-вывода после завершения периода фиксации с неудачным снимком.

**Windows server 2003:****жетосснапшотаборт** появился в Windows Server 2003.  

```cpp
    JET_ERR JET_API JetOSSnapshotAbort(
      __in          const JET_OSSNAPID snapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Параметры

*снапид*

Идентификатор сеанса моментального снимка.

*грбит*

Параметры для этого вызова. Этот параметр зарезервирован для будущего использования, и поддерживается только допустимое значение 0 (ноль).

### <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата. дополнительные сведения о возможных ошибках подсистемы ESE см. в разделе [ошибки расширенных служба хранилища Engine](./extensible-storage-engine-errors.md) и [параметры обработки ошибок](./error-handling-parameters.md).


| <p>Код возврата</p> | <p>Описание</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Операция выполнена успешно.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Недопустимый сеанс моментального снимка, или параметр грбит недопустим.</p> | 
| <p>JET_errOSSnapshotInvalidSnapId</p> | <p>Недопустимый идентификатор сеанса моментального снимка.</p> | 



Если эта функция завершается, то сеанс моментального снимка завершится, и поведение нормального обработчика будет возобновлено. Новый сеанс моментального снимка можно запустить позже.

Если эта функция завершается ошибкой, сеанс моментального снимка не будет прерван.

#### <a name="remarks"></a>Комментарии

Эта функция должна вызываться вместо [жетосснапшотсав](./jetossnapshotthaw-function.md) , чтобы информировать механизм о том, что моментальный снимок был прерван по причинам, не связанным с ядром. Эти сведения можно использовать позже для выведения сообщений журнала событий о сеансе моментальных снимков или для определения других соответствующих действий.

#### <a name="requirements"></a>Требования


| Требование | Применение |
|------------|----------|
| <p><strong>Клиент</strong></p> | <p>требуется Windows Vista.</p> | 
| <p><strong>Server</strong></p> | <p>требуется Windows server 2008 или Windows server 2003.</p> | 
| <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | 
| <p><strong>Библиотека</strong></p> | <p>Используйте ESENT. lib.</p> | 
| <p><strong>КОМПОНОВКИ</strong></p> | <p>Требуется ESENT.dll.</p> | 



#### <a name="see-also"></a>См. также:

[JET_ERR](./jet-err.md)  
[JET_OSSNAPID](./jet-ossnapid.md)  
[жетосснапшотфризе](./jetossnapshotfreeze-function.md)  
[жетосснапшотпрепаре](./jetossnapshotprepare-function.md)  
[жетосснапшотсав](./jetossnapshotthaw-function.md)
