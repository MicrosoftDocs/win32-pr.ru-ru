---
description: Дополнительные сведения о функции Жетосснапшотенд
title: Функция Жетосснапшотенд
TOCTitle: JetOSSnapshotEnd Function
ms:assetid: f7f4db8b-8e40-48d7-bc7b-0c80d0d0f77f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294136(v=EXCHG.10)
ms:contentKeyID: 32765750
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotEnd
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: de1237de9af0b1b75f645346fc30a128a1b8e907
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143531"
---
# <a name="jetossnapshotend-function"></a>Функция Жетосснапшотенд


_**Применимо к:** Windows | Windows Server_

## <a name="jetossnapshotend-function"></a>Функция Жетосснапшотенд

Функция **жетосснапшотенд** уведомляет модуль о завершении сеанса моментального снимка.

**Windows Vista:**  **Жетосснапшотенд** появился в Windows Vista:.

```cpp
    JET_ERR JET_API JetOSSnapshotEnd(
      __in          const JET_OSSNAPID snapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Параметры

*снапид*

Идентификатор сеанса моментального снимка.

*грбит*

Параметры для этого вызова. Этот параметр может иметь сочетание следующих значений.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Значение</p></th>
<th><p>Значение</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>0</p></td>
<td><p>Успешное завершение сеанса моментального снимка.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitAbortSnapshot</p></td>
<td><p>Сеанс моментального снимка прерван.</p></td>
</tr>
</tbody>
</table>


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
<td><p>JET_errInvalidGrbit</p></td>
<td><p>Один из запрошенных параметров недопустим, используется неправильно или не реализован.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOSSnapshotInvalidSequence</p></td>
<td><p>Сеанс моментального снимка уже выполняется. Это не допускается.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOSSnapshotInvalidSnapId</p></td>
<td><p>Недопустимый идентификатор сеанса моментального снимка.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOSSnapshotTimeOut</p></td>
<td><p>Время сеанса моментального снимка истекло до возникновения этого вызова. В результате операции ввода-вывода, возвращенные в нормальный режим до того, как был выполнен этот вызов.</p></td>
</tr>
</tbody>
</table>


Если эта функция завершается, то сеанс моментального снимка будет завершен и будет возобновлено нормальное поведение ядра. Новый сеанс моментального снимка можно запустить позже.

Если эта функция завершается ошибкой, возвращается код возврата JET_errOSSnapshotTimeOut и текущий сеанс моментального снимка завершается, но замораживание IOs в течение периода моментального снимка не учитывается внутренне. Для всех остальных ошибок состояние сеанса моментального снимка не изменится.

#### <a name="remarks"></a>Комментарии

Эта функция вызывается, только если [жетосснапшотсав](./jetossnapshotthaw-function.md) был вызван с JET_bitContinueAfterThaw.

Сеанс моментального снимка должен быть завершен для проверки моментальных снимков и усечения журнала. Записи журнала событий будут созданы для различных этапов создания моментального снимка.

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
[жетосснапшотсав](./jetossnapshotthaw-function.md)
