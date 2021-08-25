---
title: Структура WMDRM_ANALOG_VIDEO_RESTRICTIONS (Вмдрмсдк. h)
description: '\_ \_ Структура ограничений аналогового видео WMDRM \_ содержит сведения об ограничении для воспроизведения содержимого в виде аналогового видео.'
ms.assetid: 13b38115-bd18-45b9-a1d5-542e043a4bde
keywords:
- Формат WMDRM_ANALOG_VIDEO_RESTRICTIONS структуры Windows Media
- структура формат мультимедиа Windows
topic_type:
- apiref
api_name:
- WMDRM_ANALOG_VIDEO_RESTRICTIONS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8221fe325983387107f4e0c03f5672a6762502d8865e1d5895a9e48e96b99d4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928814"
---
# <a name="wmdrm_analog_video_restrictions-structure"></a>\_ \_ Структура ограничений аналогового видео WMDRM \_

Структура **\_ \_ \_ ограничений аналогового видео WMDRM** содержит сведения об ограничении для воспроизведения содержимого в виде аналогового видео.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct WMDRM_ANALOG_VIDEO_RESTRICTIONS {
  GUID  guidRestrictionID;
  DWORD dwRestrictionData;
} ;
```



## <a name="members"></a>Члены

<dl> <dt>

**гуидрестриктионид**
</dt> <dd>

Идентификатор ограничения.

</dd> <dt>

**дврестриктиондата**
</dt> <dd>

Данные ограничений.

</dd> </dl>

## <a name="remarks"></a>Remarks

Эта структура получается при вызове [**ивмдрмлиценсе:: жетаналогвидеорестриктионлевелс**](iwmdrmlicense-getanalogvideorestrictionlevels.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Вмдрмсдк. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Структуры**](drm-structures.md)
</dt> <dt>

[**\_ограничения аналогового видео WMDRM ( \_ \_ \_ пример)**](wmdrm-analog-video-restrictions-ex.md)
</dt> </dl>

 

 





