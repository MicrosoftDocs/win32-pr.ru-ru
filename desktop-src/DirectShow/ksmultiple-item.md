---
description: '\_Структура элемента ксмултипле описывает размер и число свойств переменной длины в ПИН-кодах в режиме ядра.'
ms.assetid: aedbf7bc-393d-4ab5-afcd-d8822b925f07
title: Структура KSMULTIPLE_ITEM (KS. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KSMULTIPLE_ITEM
api_type:
- HeaderDef
api_location:
- ks.h
ms.openlocfilehash: 2e1cdf3d8edcea88fbcfb260d87d3e79d62eb2aebc57144ae38defb018065f1a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119823314"
---
# <a name="ksmultiple_item-structure"></a>\_Структура элемента ксмултипле

`KSMULTIPLE_ITEM`Структура описывает размер и число свойств переменной длины ПИН-кодов в режиме ядра.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct {
  ULONG Size;
  ULONG Count;
} KSMULTIPLE_ITEM, *PKSMULTIPLE_ITEM;
```



## <a name="members"></a>Члены

<dl> <dt>

**Размер**
</dt> <dd>

Размер возвращенного блока памяти в байтах. Размер включает структуру **\_ элемента ксмултипле** и элементы, которые следуют за ней.

</dd> <dt>

**Количество**
</dt> <dd>

Указывает общее число элементов, которые следуют за этой структурой.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>KS. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[DirectShow Сотрудник](directshow-structures.md)
</dt> <dt>

[**Икспин:: Кскуеримедиумс**](ikspin-ksquerymediums.md)
</dt> <dt>

[**регпинмедиум**](/windows/desktop/api/strmif/ns-strmif-regpinmedium)
</dt> </dl>

 

 




