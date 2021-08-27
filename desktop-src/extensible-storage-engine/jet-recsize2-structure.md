---
description: 'Дополнительные сведения: структура JET_RECSIZE2'
title: Структура JET_RECSIZE2
TOCTitle: JET_RECSIZE2 Structure
ms:assetid: 02a13b5b-d904-49b2-baaa-c60328d70290
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269174(v=EXCHG.10)
ms:contentKeyID: 32765477
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
ms.openlocfilehash: 0b99f5aa60f90a753a9c5d095e7a63417485b1fd
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469841"
---
# <a name="jet_recsize2-structure"></a>Структура JET_RECSIZE2


_**Применимо к:** Windows | Windows Сервером_

## <a name="jet_recsize2-structure"></a>Структура JET_RECSIZE2

Структура **JET_RECSIZE2** используется [JetGetRecordSize2](./jetgetrecordsize2-function.md) для получения сведений о требованиях к использованию записи в пространстве данных пользователя, количестве столбцов набора, количестве значений и служебной нагрузке на структуру записи ESE.

**Windows 7:** структура **JET_RECSIZE2** введена в операционной системе Windows 7.

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
      unsigned __int64 cCompressedColumns;
      unsigned __int64 cbDataCompressed;
      unsigned __int64 cbLongValueDataCompressed;
    } JET_RECSIZE2;
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

**ккомпресседколумнс**

Общее число сжатых столбцов.

**кбдатакомпрессед**

Сжатый размер данных пользователя в этой записи. Это то же самое, что и cbData, если никакие внутренние значения long не сжимаются.

**кблонгвалуедатакомпрессед**

Сжатый размер данных пользователя в дереве длинных значений. Это то же самое, что и данные Кблонгвалуе, если не сжаты отдельные длинные значения.

### <a name="remarks"></a>Комментарии

Общее число значений в записи будет **кмултивалуес**  +  **кнонтагжедколумнс**  +  **ктагжедколумнс**.

Логическими данными в записи является (cbData + Кблонгвалуедата), а физическим размером данных является (Кбдатакомпрессед + Кблонгвалуедатакомпрессед). Это можно использовать для вычисления коэффициента сжатия сохраненных данных.

### <a name="requirements"></a>Требования


| | | <p><strong>Клиент</strong></p> | <p>требуется операционная система Windows Vista.</p> | | <p><strong>Сервер</strong></p> | <p>требуется операционная система Windows Server 2008.</p> | | <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | 



### <a name="see-also"></a>См. также:

[жетжетрекордсизе](./jetgetrecordsize-function.md)  
[JetGetRecordSize2](./jetgetrecordsize2-function.md)
