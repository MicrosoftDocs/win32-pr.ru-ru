---
description: Дополнительные сведения о функции Жетосснапшоттрункателогинстанце
title: Функция Жетосснапшоттрункателогинстанце
TOCTitle: JetOSSnapshotTruncateLogInstance Function
ms:assetid: ddc51957-5b89-4abf-9193-c34ef626a63e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294115(v=EXCHG.10)
ms:contentKeyID: 32765729
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotTruncateLogInstance
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cef30d012c28c809bb35d59a82fd596ba69bd175
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808428"
---
# <a name="jetossnapshottruncateloginstance-function"></a>Функция Жетосснапшоттрункателогинстанце


_**Применимо к:** Windows | Windows Server_

## <a name="jetossnapshottruncateloginstance-function"></a>Функция Жетосснапшоттрункателогинстанце

Функция **жетосснапшоттрункателогинстанце** усекает журнал для указанного экземпляра во время сеанса моментального снимка.

**Windows Vista:**  **Жетосснапшоттрункателогинстанце** появился в Windows Vista.

```cpp
    JET_ERR JET_API JetOSSnapshotTruncateLogInstance(
      __in          const JET_OSSNAPID snapId,
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

Параметры для этого вызова. Этот параметр может иметь сочетание следующих значений.

*грбит* может иметь одно из следующих значений:

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
<li><p>Вызов завершается после истечения времени ожидания сеанса моментального снимка.</p></li>
<li><p>Сеанс был указан в качестве моментального снимка копии.</p></li>
</ul></td>
</tr>
</tbody>
</table>


Если эта функция выполнена, файлы журнала для одного или всех экземпляров, которые являются частью сеанса моментального снимка, будут обрезаны, если это возможно.

#### <a name="remarks"></a>Комментарии

Эта функция должна вызываться только в том случае, если моментальный снимок был создан с помощью параметра JET_bitContinueAfterThaw. В противном случае сеанс моментального снимка завершается после вызова [жетосснапшотсав](./jetossnapshotthaw-function.md).

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
