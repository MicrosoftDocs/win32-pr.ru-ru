---
description: Дополнительные сведения о функции Жетосснапшотпрепаре
title: Функция JetOSSnapshotPrepare
TOCTitle: JetOSSnapshotPrepare Function
ms:assetid: 364cbcba-7ddb-4748-8417-e885a5984b0d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269224(v=EXCHG.10)
ms:contentKeyID: 32765526
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotPrepare
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 67ccf9a5b21ccb9a4f94ba5aa4f995e4bb9017bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647513"
---
# <a name="jetossnapshotprepare-function"></a>Функция JetOSSnapshotPrepare


_**Применимо к:** Windows | Windows Server_

## <a name="jetossnapshotprepare-function"></a>Функция JetOSSnapshotPrepare

Функция **жетосснапшотпрепаре** начинает подготовку сеанса моментального снимка. Сеанс моментальных снимков — это короткий интервал времени, в течение которого модуль не выполняет никаких операций записи с диска IOs на диск, чтобы подсистема могла участвовать в сеансе моментальных снимков тома (при использовании модуля записи моментальных снимков).

**Windows XP:**  **Жетосснапшотпрепаре** появился в Windows XP.

```cpp
    JET_ERR JET_API JetOSSnapshotPrepare(
      __out         JET_OSSNAPID* psnapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Параметры

*пснапид*

Идентификатор сеанса моментального снимка, который необходимо запустить.

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
<td><p>Стандартный моментальный снимок.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitIncrementalSnapshot</p></td>
<td><p>Будут предприняты только файлы журналов.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitCopySnapshot</p></td>
<td><p>Моментальный снимок копии (обычная или добавочная) без усечения журнала.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitContinueAfterThaw</p></td>
<td><p>Сеанс моментального снимка происходит после <a href="gg269229(v=exchg.10).md">жетосснапшотсав</a> и требует вызова функции <a href="gg294136(v=exchg.10).md">жетосснапшотенд</a> .</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitExplicitPrepare</p></td>
<td><p>Ни один экземпляр не будет подготовлен по умолчанию.</p>
<p><strong>Windows 7:</strong>  JET_bitExplicitPrepare введен в Windows 7.</p></td>
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
<td><p>JET_errInvalidParameter</p></td>
<td><p>Указатель идентификатора моментального снимка имеет значение NULL, или параметр <em>грбит</em> является недопустимым.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOSSnapshotInvalidSequence</p></td>
<td><p>Сеанс моментальных снимков уже выполняется, и в данный момент операция не может иметь более одного сеанса моментального снимка.</p></td>
</tr>
</tbody>
</table>


Если эта функция завершится с ошибкой, сеанс моментального снимка можно будет запустить в любое время с фазы замораживания ввода-вывода. Идентификатор сеанса будет возвращен и должен использоваться в последующих вызовах для сеанса моментального снимка.

Выполняющиеся экземпляры подсистемы теперь будут рассматриваться как часть сеанса моментального снимка.

**Windows Vista:**  Чтобы указать другое подмножество экземпляров, можно вызвать [жетосснапшотпрепареинстанце](./jetossnapshotprepareinstance-function.md) .

Стандартный вызов последовательности API: **жетосснапшотпрепаре**, при необходимости за одним или несколькими вызовами [жетосснапшотпрепареинстанце](./jetossnapshotprepareinstance-function.md), после которого следует [жетосснапшотфризе](./jetossnapshotfreeze-function.md). После запуска замораживания его можно завершить с помощью [жетосснапшотсав](./jetossnapshotthaw-function.md). В любое время после подготовки сеанс моментального снимка может внезапно завершиться с помощью [жетосснапшотаборт](./jetossnapshotabort-function.md).

Если после [жетосснапшотсав](./jetossnapshotthaw-function.md)указан JET_bitContinueAfterThaw, то сеанс моментального снимка останется (хотя операция ввода-вывода будет возобновлена). При этом будет включена проверка моментального снимка и, при необходимости, будет включено усечение журнала с помощью [жетосснапшоттрункателог](./jetossnapshottruncatelog-function.md) и потребуется вызов [жетосснапшотенд](./jetossnapshotend-function.md).

Если эта функция завершается неудачно, изменение состояния модуля не происходит.

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
[жетосснапшотенд](./jetossnapshotend-function.md)  
[жетосснапшотфризе](./jetossnapshotfreeze-function.md)  
[жетосснапшотпрепареинстанце](./jetossnapshotprepareinstance-function.md)  
[жетосснапшотсав](./jetossnapshotthaw-function.md)  
[жетосснапшоттрункателог](./jetossnapshottruncatelog-function.md)
