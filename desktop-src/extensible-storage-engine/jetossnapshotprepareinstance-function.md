---
description: Дополнительные сведения о функции Жетосснапшотпрепареинстанце
title: Функция Жетосснапшотпрепареинстанце
TOCTitle: JetOSSnapshotPrepareInstance Function
ms:assetid: b4f06342-633f-47c6-be32-64ec058920fe
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294064(v=EXCHG.10)
ms:contentKeyID: 32765679
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotPrepareInstance
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4997be8f268d676fbd4a164281061b488e948168
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474390"
---
# <a name="jetossnapshotprepareinstance-function"></a>Функция Жетосснапшотпрепареинстанце


_**Применимо к:** Windows | Windows Сервером_

## <a name="jetossnapshotprepareinstance-function"></a>Функция Жетосснапшотпрепареинстанце

Функция **жетосснапшотпрепареинстанце** выбирает конкретный экземпляр, который должен быть частью сеанса моментального снимка.

**Windows Vista:** **жетосснапшотпрепареинстанце** был введен в Windows Vista.

```cpp
JET_ERR JET_API JetOSSnapshotPrepareInstance(
  __in          JET_OSSNAPID snapId,
  __in          JET_INSTANCE instance,
  __in          const JET_GRBIT grbit
);
```

### <a name="parameters"></a>Параметры

*снапид*

Идентификатор сеанса моментального снимка.

*вхождение*

Экземпляр, который будет использоваться для этого вызова.

*грбит*

Параметры для этого вызова. Этот параметр зарезервирован для использования в будущем. Единственное допустимое значение — 0 (ноль).

### <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата. дополнительные сведения о возможных ошибках подсистемы ESE см. в разделе [ошибки расширенных служба хранилища Engine](./extensible-storage-engine-errors.md) и [параметры обработки ошибок](./error-handling-parameters.md).


| <p>Код возврата</p> | <p>Описание</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Операция выполнена успешно.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Указатель идентификатора моментального снимка имеет <strong>значение NULL</strong> , или параметр <em>грбит</em> является недопустимым.</p> | 
| <p>JET_errOSSnapshotInvalidSequence</p> | <p>Сеанс моментального снимка уже выполняется.</p> | 
| <p>JET_errOSSnapshotInvalidSnapId</p> | <p>Недопустимый идентификатор сеанса моментального снимка.</p> | 



Если эта функция выполнена, указанный экземпляр будет частью сеанса моментального снимка.

Если эта функция завершается неудачно, изменение состояния модуля не происходит.

#### <a name="remarks"></a>Комментарии

Стандартный вызов последовательности API: [жетосснапшотпрепаре](./jetossnapshotprepare-function.md), при необходимости за одним или несколькими вызовами **жетосснапшотпрепареинстанце**, после которого следует [жетосснапшотфризе](./jetossnapshotfreeze-function.md). После запуска замораживания его можно завершить с помощью [жетосснапшотсав](./jetossnapshotthaw-function.md). В любое время после подготовки сеанс моментального снимка может внезапно завершиться с помощью [жетосснапшотаборт](./jetossnapshotabort-function.md). Записи журнала событий будут созданы для различных этапов создания моментального снимка.

Если **жетосснапшотпрепареинстанце** не вызывается между началом сеанса ([жетосснапшотпрепаре](./jetossnapshotprepare-function.md)) и закреплением ([жетосснапшотфризе](./jetossnapshotfreeze-function.md)), все запущенные экземпляры в ядре будут закрепляться и становиться частью сеанса моментального снимка. Это происходит по двум причинам.

  - Он упрощает код для пользователей, которым требуются все экземпляры.

  - Он обеспечивает обратную совместимость для вызывающих объектов API моментальных снимков.

#### <a name="requirements"></a>Требования


| | | <p><strong>Клиент</strong></p> | <p>требуется Windows Vista.</p> | | <p><strong>Сервер</strong></p> | <p>требуется Windows Server 2008.</p> | | <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | | <p><strong>Библиотека</strong></p> | <p>Используйте ESENT. lib.</p> | | <p><strong>КОМПОНОВКИ</strong></p> | <p>Требуется ESENT.dll.</p> | 



#### <a name="see-also"></a>См. также:

[Параметры обработки ошибок](./error-handling-parameters.md)  
[ошибки расширенного обработчика служба хранилища](./extensible-storage-engine-errors.md)  
[JET_ERR](./jet-err.md)  
[жетосснапшотаборт](./jetossnapshotabort-function.md)  
[жетосснапшотенд](./jetossnapshotend-function.md)  
[жетосснапшотфризе](./jetossnapshotfreeze-function.md)  
[жетосснапшотпрепаре](./jetossnapshotprepare-function.md)  
[жетосснапшотсав](./jetossnapshotthaw-function.md)
