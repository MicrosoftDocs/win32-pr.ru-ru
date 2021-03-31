---
description: 'Дополнительные сведения: структура JET_RECSIZE'
title: Структура JET_RECSIZE
TOCTitle: JET_RECSIZE Structure
ms:assetid: bb2a63bb-7956-46c2-9791-0d0678a6c366
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294072(v=EXCHG.10)
ms:contentKeyID: 32765687
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e4e6b2f313a5411ba5bfeea73db3b01afe007612
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808542"
---
# <a name="jet_recsize-structure"></a>Структура JET_RECSIZE


_**Применимо к:** Windows | Windows Server_

## <a name="jet_recsize-structure"></a>Структура JET_RECSIZE

Структура **JET_RECSIZE** используется [жетжетрекордсизе](./jetgetrecordsize-function.md) для получения сведений о требованиях к использованию записи в пространстве данных пользователя, количестве столбцов набора, количестве значений и служебной нагрузке на структуру записи ESE.

**Windows Vista:** Структура **JET_RECSIZE** появилась в Windows Vista.

```cpp
    typedef struct {
      unsigned __int64 cbData;
      unsigned __int64 cbLongValueData;
      unsigned __int64 cbOverhead;
      unsigned __int64 cbLongValueOverhead;
      unsigned __int64 cNonTaggedColumns;
      unsigned __int64 cTaggedColumns;
      unsigned __int64 cLongValues;
      unsigned __int64 cMultiValues;
    } JET_RECSIZE;
```

### <a name="members"></a>Элементы

**cbData**

Пользовательский набор данных в записи.

**Примечание**  .  Размер ключа не включен в этот раздел.

**кблонгвалуедата**

Данные пользователя, связанные с записью, но хранимые в дереве длинных значений.

**Примечание**  .  Это не учитывает внутренние значения long.

**кбоверхеад**

Издержки структуры записи ESE для этой записи. Сюда входит размер ключа записи.

**кблонгвалуеоверхеад**

Затраты на данные длинных значений.

**Примечание**  .  Это не учитывает внутренние значения long.

**кнонтагжедколумнс**

Общее число фиксированных и переменных столбцов, заданных в этой записи.

**ктагжедколумнс**

Общее число столбцов с тегами, заданных в этой записи.

**клонгвалуес**

Общее число значений long, хранящихся в дереве Long-Value для этой записи.

**Примечание**  .  Это не учитывает внутренние значения long.

**кмултивалуес**

Совокупность общего количества значений, находящихся за первым для всех столбцов в записи.

### <a name="remarks"></a>Комментарии

Общее число значений в записи будет **кмултивалуес**  +  **кнонтагжедколумнс**  +  **ктагжедколумнс**.

### <a name="requirements"></a>Требования

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
</tbody>
</table>


### <a name="see-also"></a>См. также:

[жетжетрекордсизе](./jetgetrecordsize-function.md)
