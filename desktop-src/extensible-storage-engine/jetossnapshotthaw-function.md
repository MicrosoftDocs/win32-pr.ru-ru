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
ms.openlocfilehash: da7d5037cfc6b9a5f001dede57581127e4de60b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913559"
---
# <a name="jetossnapshotthaw-function"></a>Функция Жетосснапшотсав


_**Применимо к:** Windows | Windows Server_

## <a name="jetossnapshotthaw-function"></a>Функция Жетосснапшотсав

Функция **жетосснапшотсав** уведомляет модуль о том, что он может возобновить нормальную операцию ввода-вывода после точки фиксации и успешного создания моментального снимка.

**Windows XP:**  **Жетосснапшотсав** появился в Windows XP.

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

Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата. Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).

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
<td><p>JET_errInvalidParameter</p></td>
<td><p>Недопустимый сеанс моментального снимка, или параметр <em>грбит</em> недопустим.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOSSnapshotTimeOut</p></td>
<td><p>Время сеанса моментального снимка истекло до возникновения этого вызова. Следовательно, перед совершением этого вызова операции ввода-вывода возвращены в нормальный режим.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOSSnapshotInvalidSnapId</p></td>
<td><p>Недопустимый идентификатор сеанса моментального снимка.</p></td>
</tr>
</tbody>
</table>


Если эта функция завершается, то сеанс моментального снимка завершается, а нормальное поведение ядра возобновляется. Новый сеанс моментального снимка можно запустить позже.

Если эта функция завершается ошибкой, текущий сеанс моментального снимка завершается, но замораживание IOs в течение периода моментального снимка не учитывается внутренне.

#### <a name="remarks"></a>Комментарии

Записи журнала событий будут созданы для различных этапов создания моментального снимка.

#### <a name="requirements"></a>Требования

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Клиент</strong></p></td>
<td><p>Требуется Windows Vista или Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Требуется Windows Server 2008 или Windows Server 2003.</p></td>
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


#### <a name="see-also"></a>См. также:

[JET_ERR](./jet-err.md)  
[JET_OSSNAPID](./jet-ossnapid.md)  
[жетосснапшотаборт](./jetossnapshotabort-function.md)  
[жетосснапшотфризе](./jetossnapshotfreeze-function.md)  
[жетосснапшотпрепаре](./jetossnapshotprepare-function.md)
