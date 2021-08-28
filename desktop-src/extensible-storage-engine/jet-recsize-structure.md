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
ms.openlocfilehash: 4fd0f59c821fa80d8de46f97e05aa1944354018e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475950"
---
# <a name="jet_recsize-structure"></a>Структура JET_RECSIZE


_**Применимо к:** Windows | Windows Сервером_

## <a name="jet_recsize-structure"></a>Структура JET_RECSIZE

Структура **JET_RECSIZE** используется [жетжетрекордсизе](./jetgetrecordsize-function.md) для получения сведений о требованиях к использованию записи в пространстве данных пользователя, количестве столбцов набора, количестве значений и служебной нагрузке на структуру записи ESE.

**Windows Vista:** структура **JET_RECSIZE** появилась в Windows Vista.

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


| | | <p><strong>Клиент</strong></p> | <p>требуется Windows Vista.</p> | | <p><strong>Сервер</strong></p> | <p>требуется Windows Server 2008.</p> | | <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | 



### <a name="see-also"></a>См. также:

[жетжетрекордсизе](./jetgetrecordsize-function.md)
