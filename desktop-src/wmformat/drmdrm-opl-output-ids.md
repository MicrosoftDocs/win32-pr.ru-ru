---
title: Структура DRM_OPL_OUTPUT_IDS (Вмдрмсдк. h)
description: '\_ \_ \_ Структура выходных идентификаторов DRM ОПЛ содержит ряд выходных идентификаторов уровня защиты выходных данных (ОПЛ).'
ms.assetid: 3627f2a7-1cea-400b-82e7-678898ccc386
keywords:
- Формат DRM_OPL_OUTPUT_IDS структуры Windows Media
- структура формат мультимедиа Windows
topic_type:
- apiref
api_name:
- DRM_OPL_OUTPUT_IDS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 802787c5e373c837d639e0225bf650d80c105970
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708364"
---
# <a name="drm_opl_output_ids-structure"></a>\_ \_ Структура идентификаторов выходных данных ОПЛ DRM \_

Структура **\_ \_ выходных \_ идентификаторов DRM ОПЛ** содержит ряд выходных идентификаторов уровня защиты выходных данных (ОПЛ).

## <a name="syntax"></a>Синтаксис


```C++
typedef struct DRM_OPL_OUTPUT_IDS {
  WORD cIds;
  GUID *rgIds;
} ;
```



## <a name="members"></a>Члены

<dl> <dt>

**Идентификаторы CID**
</dt> <dd>

Количество идентификаторов в массиве, на которые ссылается **ргидс**.

</dd> <dt>

**ргидс**
</dt> <dd>

Адрес массива идентификаторов GUID. Каждый элемент массива содержит идентификатор выхода ОПЛ.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Эта структура используется в качестве члена структур [**DRM \_ Copy \_ ОПЛ**](drmdrm-copy-opl.md) и [**DRM \_ Play \_ ОПЛ**](drmdrm-play-opl.md) для идентификации групп идентификаторов выходных данных.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Вмдрмсдк. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Структуры**](drm-structures.md)
</dt> </dl>

 

 





