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
ms.openlocfilehash: 62e26b1aa8804514588e66c1d02e1f0643e97bcb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675927"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>KS. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры DirectShow](directshow-structures.md)
</dt> <dt>

[**Икспин:: Кскуеримедиумс**](ikspin-ksquerymediums.md)
</dt> <dt>

[**регпинмедиум**](/windows/desktop/api/strmif/ns-strmif-regpinmedium)
</dt> </dl>

 

 




