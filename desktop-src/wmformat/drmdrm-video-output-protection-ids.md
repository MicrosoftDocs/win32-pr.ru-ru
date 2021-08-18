---
title: Структура DRM_VIDEO_OUTPUT_PROTECTION_IDS (Вмдрмсдк. h)
description: '\_ \_ \_ \_ Структура идентификаторов для защиты от видео DRM содержит массив \_ \_ структур защиты вывода видео DRM \_ .'
ms.assetid: 9f206a7e-c92b-4f29-a591-72784086d1db
keywords:
- Формат DRM_VIDEO_OUTPUT_PROTECTION_IDS структуры Windows Media
- структура формат мультимедиа Windows
topic_type:
- apiref
api_name:
- DRM_VIDEO_OUTPUT_PROTECTION_IDS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9439328ed817da40630c3a600cf7e6db553738a12799babbe9e71c48f28923b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119085876"
---
# <a name="drm_video_output_protection_ids-structure"></a>\_ \_ \_ Структура идентификаторов защиты ВИДЕОпотока DRM \_

Структура **\_ \_ \_ \_ идентификаторов для защиты от видео DRM** содержит массив структур **\_ \_ \_ защиты вывода видео DRM** .

## <a name="syntax"></a>Синтаксис


```C++
typedef struct DRM_VIDEO_OUTPUT_PROTECTION_IDS {
  WORD                        cEntries;
  DRM_VIDEO_OUTPUT_PROTECTION *rgVop;
} ;
```



## <a name="members"></a>Члены

<dl> <dt>

**центриес**
</dt> <dd>

Число элементов в массиве, на которые ссылается **ргвоп**.

</dd> <dt>

**ргвоп**
</dt> <dd>

Адрес массива структур **\_ \_ \_ защиты вывода видео DRM** . **DRM \_ \_ \_ Защита вывода видео** — это тип, определенный [**как \_ \_ Защита выходных данных DRM**](drm-output-protection.md).

</dd> </dl>

## <a name="remarks"></a>Remarks

Эта структура используется в качестве члена структуры [**DRM \_ Play \_ ОПЛ**](drmdrm-play-opl.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Вмдрмсдк. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_ \_ \_ идентификаторы защиты звука в DRM \_**](drm-audio-output-protection-ids.md)
</dt> <dt>

[**\_ \_ \_ идентификаторы защиты вывода видео DRM \_ \_ ex**](drm-video-output-protection-ids-ex.md)
</dt> <dt>

[**Структуры**](drm-structures.md)
</dt> </dl>

 

 





