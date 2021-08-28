---
description: Дополнительные сведения о функции Жетосснапшотсав
title: Функция Жетосснапшотсав
TOCTitle: JetOSSnapshotThaw Function
ms:assetid: 3b001113-6299-4082-ab15-461f2e33e996
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269229(v=EXCHG.10)
ms:contentKeyID: 32765531
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotThaw
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 445fa1d2370f13ae39615d4228b245899173ad8d
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122986687"
---
# <a name="jetossnapshotthaw-function"></a>Функция Жетосснапшотсав


_**Применимо к:** Windows | Windows Сервером_

## <a name="jetossnapshotthaw-function"></a>Функция Жетосснапшотсав

Функция **жетосснапшотсав** уведомляет модуль о том, что он может возобновить нормальную операцию ввода-вывода после точки фиксации и успешного создания моментального снимка.

**Windows xp:****жетосснапшотсав** появился в Windows XP.  

```cpp
    JET_ERR JET_API JetOSSnapshotThaw(
      __in          const JET_OSSNAPID snapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Параметры

*снапид*

Идентификатор сеанса моментального снимка.

*грбит*

Этот параметр зарезервирован для будущего использования, и поддерживается только допустимое значение 0.

### <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата. дополнительные сведения о возможных ошибках подсистемы ESE см. в разделе [ошибки расширенных служба хранилища Engine](./extensible-storage-engine-errors.md) и [параметры обработки ошибок](./error-handling-parameters.md).


| <p>Код возврата</p> | <p>Описание</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Операция выполнена успешно.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Недопустимый сеанс моментального снимка, или параметр <em>грбит</em> недопустим.</p> | 
| <p>JET_errOSSnapshotTimeOut</p> | <p>Время сеанса моментального снимка истекло до возникновения этого вызова. Следовательно, перед совершением этого вызова операции ввода-вывода возвращены в нормальный режим.</p> | 
| <p>JET_errOSSnapshotInvalidSnapId</p> | <p>Недопустимый идентификатор сеанса моментального снимка.</p> | 



Если эта функция завершается, то сеанс моментального снимка завершается, а нормальное поведение ядра возобновляется. Новый сеанс моментального снимка можно запустить позже.

Если эта функция завершается ошибкой, текущий сеанс моментального снимка завершается, но замораживание IOs в течение периода моментального снимка не учитывается внутренне.

#### <a name="remarks"></a>Комментарии

Записи журнала событий будут созданы для различных этапов создания моментального снимка.

#### <a name="requirements"></a>Требования


| Требование | Применение |
|------------|----------|
| <p><strong>Клиент</strong></p> | <p>требуется Windows Vista или Windows XP.</p> | 
| <p><strong>Server</strong></p> | <p>требуется Windows server 2008 или Windows server 2003.</p> | 
| <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | 
| <p><strong>Библиотека</strong></p> | <p>Используйте ESENT. lib.</p> | 
| <p><strong>КОМПОНОВКИ</strong></p> | <p>Требуется ESENT.dll.</p> | 



#### <a name="see-also"></a>См. также:

[JET_ERR](./jet-err.md)  
[JET_OSSNAPID](./jet-ossnapid.md)  
[жетосснапшотаборт](./jetossnapshotabort-function.md)  
[жетосснапшотфризе](./jetossnapshotfreeze-function.md)  
[жетосснапшотпрепаре](./jetossnapshotprepare-function.md)
