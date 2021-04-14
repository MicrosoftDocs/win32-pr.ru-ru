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
ms.openlocfilehash: 8cc5179a55aabfa3324e3caab7005f4abe437a6d
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "104424550"
---
# <a name="jetossnapshotprepareinstance-function"></a>Функция Жетосснапшотпрепареинстанце


_**Применимо к:** Windows | Windows Server_

## <a name="jetossnapshotprepareinstance-function"></a>Функция Жетосснапшотпрепареинстанце

Функция **жетосснапшотпрепареинстанце** выбирает конкретный экземпляр, который должен быть частью сеанса моментального снимка.

**Windows Vista:** **жетосснапшотпрепареинстанце** был впервые появился в Windows Vista.

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
<td><p>Указатель идентификатора моментального снимка имеет <strong>значение NULL</strong> , или параметр <em>грбит</em> является недопустимым.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOSSnapshotInvalidSequence</p></td>
<td><p>Сеанс моментального снимка уже выполняется.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOSSnapshotInvalidSnapId</p></td>
<td><p>Недопустимый идентификатор сеанса моментального снимка.</p></td>
</tr>
</tbody>
</table>


Если эта функция выполнена, указанный экземпляр будет частью сеанса моментального снимка.

Если эта функция завершается неудачно, изменение состояния модуля не происходит.

#### <a name="remarks"></a>Комментарии

Стандартный вызов последовательности API: [жетосснапшотпрепаре](./jetossnapshotprepare-function.md), при необходимости за одним или несколькими вызовами **жетосснапшотпрепареинстанце**, после которого следует [жетосснапшотфризе](./jetossnapshotfreeze-function.md). После запуска замораживания его можно завершить с помощью [жетосснапшотсав](./jetossnapshotthaw-function.md). В любое время после подготовки сеанс моментального снимка может внезапно завершиться с помощью [жетосснапшотаборт](./jetossnapshotabort-function.md). Записи журнала событий будут созданы для различных этапов создания моментального снимка.

Если **жетосснапшотпрепареинстанце** не вызывается между началом сеанса ([жетосснапшотпрепаре](./jetossnapshotprepare-function.md)) и закреплением ([жетосснапшотфризе](./jetossnapshotfreeze-function.md)), все запущенные экземпляры в ядре будут закрепляться и становиться частью сеанса моментального снимка. Это происходит по двум причинам.

  - Он упрощает код для пользователей, которым требуются все экземпляры.

  - Он обеспечивает обратную совместимость для вызывающих объектов API моментальных снимков.

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
<td><p>Требуется Windows Server 2008.</p></td>
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

[Параметры обработки ошибок](./error-handling-parameters.md)  
[Ошибки расширяемого подсистемы хранилища](./extensible-storage-engine-errors.md)  
[JET_ERR](./jet-err.md)  
[жетосснапшотаборт](./jetossnapshotabort-function.md)  
[жетосснапшотенд](./jetossnapshotend-function.md)  
[жетосснапшотфризе](./jetossnapshotfreeze-function.md)  
[жетосснапшотпрепаре](./jetossnapshotprepare-function.md)  
[жетосснапшотсав](./jetossnapshotthaw-function.md)
