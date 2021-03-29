---
description: Дополнительные сведения о функции Жетосснапшоттрункателог
title: Функция Жетосснапшоттрункателог
TOCTitle: JetOSSnapshotTruncateLog Function
ms:assetid: 3df8f5b2-8083-49b7-a325-fd13187f785c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269231(v=EXCHG.10)
ms:contentKeyID: 32765533
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotTruncateLog
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f0a3cebd743a3c8cd9a3d86f1f637dcb5b2c9c91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647565"
---
# <a name="jetossnapshottruncatelog-function"></a>Функция Жетосснапшоттрункателог


_**Применимо к:** Windows | Windows Server_

## <a name="jetossnapshottruncatelog-function"></a>Функция Жетосснапшоттрункателог

Функция **жетосснапшоттрункателог** включает усечение журнала для всех экземпляров, которые являются частью сеанса моментальных снимков.

**Windows Vista:**  **Жетосснапшоттрункателог** появился в Windows Vista.

```cpp
    JET_ERR JET_API JetOSSnapshotTruncateLog(
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
<td><p>JET_bitAllDatabasesSnapshot</p></td>
<td><p>Все базы данных подключены, поэтому подсистема хранилища может вычислять и выполнять усечение журнала.</p></td>
</tr>
<tr class="even">
<td><p>Ноль (0)</p></td>
<td><p>Усечение не выполняется.</p></td>
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
<td><p>Недопустимый параметр <em>грбит</em> .</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOSSnapshotInvalidSequence</p></td>
<td><p>Сеанс моментального снимка не находится в состоянии, в котором может произойти усечение. Возможные причины:</p>
<ul>
<li><p>вызов выполняется по истечении времени ожидания сеанса моментальных снимков</p></li>
<li><p>сеанс был указан в качестве моментального снимка копии</p></li>
</ul></td>
</tr>
</tbody>
</table>


При успешном выполнении файлы журнала для одной или всех экземпляров сеанса моментальных снимков будут обрезаны, если это возможно.

#### <a name="remarks"></a>Комментарии

Эта функция должна вызываться только в том случае, если моментальный снимок был создан с помощью параметра JET_bitContinueAfterThaw. В противном случае сеанс моментального снимка был бы завершен после вызова [жетосснапшотсав](./jetossnapshotthaw-function.md) .

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
[жетосснапшотенд](./jetossnapshotend-function.md)  
[жетосснапшотфризе](./jetossnapshotfreeze-function.md)  
[жетосснапшотпрепаре](./jetossnapshotprepare-function.md)  
[жетосснапшотсав](./jetossnapshotthaw-function.md)
