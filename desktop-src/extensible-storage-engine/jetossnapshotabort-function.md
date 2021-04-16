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
ms.openlocfilehash: d976f027a940bcf0199016d0e617d515273183ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712509"
---
# <a name="jetossnapshotabort-function"></a>Функция Жетосснапшотаборт


_**Применимо к:** Windows | Windows Server_

## <a name="jetossnapshotabort-function"></a>Функция Жетосснапшотаборт

Функция **жетосснапшотаборт** уведомляет модуль о том, что он может возобновить нормальные операции ввода-вывода после завершения периода фиксации с неудачным снимком.

**Windows server 2003:**  **Жетосснапшотаборт** появился в Windows Server 2003.

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
<td><p>Недопустимый сеанс моментального снимка, или параметр грбит недопустим.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOSSnapshotInvalidSnapId</p></td>
<td><p>Недопустимый идентификатор сеанса моментального снимка.</p></td>
</tr>
</tbody>
</table>


Если эта функция завершается, то сеанс моментального снимка завершится, и поведение нормального обработчика будет возобновлено. Новый сеанс моментального снимка можно запустить позже.

Если эта функция завершается ошибкой, сеанс моментального снимка не будет прерван.

#### <a name="remarks"></a>Комментарии

Эта функция должна вызываться вместо [жетосснапшотсав](./jetossnapshotthaw-function.md) , чтобы информировать механизм о том, что моментальный снимок был прерван по причинам, не связанным с ядром. Эти сведения можно использовать позже для выведения сообщений журнала событий о сеансе моментальных снимков или для определения других соответствующих действий.

#### <a name="requirements"></a>Требования

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Клиент</strong></p></td>
<td><p>Требуется Windows Vista.</p></td>
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
[жетосснапшотфризе](./jetossnapshotfreeze-function.md)  
[жетосснапшотпрепаре](./jetossnapshotprepare-function.md)  
[жетосснапшотсав](./jetossnapshotthaw-function.md)
