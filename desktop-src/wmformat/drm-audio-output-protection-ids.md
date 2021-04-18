---
title: Структура DRM_AUDIO_OUTPUT_PROTECTION_IDS (Вмдрмсдк. h)
description: '\_ \_ \_ Структура идентификаторов защиты звукового выхода DRM \_ содержит список идентификаторов защиты звука.'
ms.assetid: 21972b18-334b-4a4d-812d-21cbfaf7cc58
keywords:
- Формат DRM_AUDIO_OUTPUT_PROTECTION_IDS структуры Windows Media
- структура формат мультимедиа Windows
topic_type:
- apiref
api_name:
- DRM_AUDIO_OUTPUT_PROTECTION_IDS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d3c7142f5f575413f72885aa60a0ccb826ecfab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718113"
---
# <a name="drm_audio_output_protection_ids-structure"></a>\_ \_ \_ Структура идентификаторов защиты ЗВУКового выхода DRM \_

Структура **\_ \_ \_ \_ идентификаторов защиты звукового выхода DRM** содержит список идентификаторов защиты звука.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct DRM_AUDIO_OUTPUT_PROTECTION_IDS {
  WORD                        cEntries;
  DRM_AUDIO_OUTPUT_PROTECTION *rgAop;
} ;
```



## <a name="members"></a>Члены

<dl> <dt>

**центриес**
</dt> <dd>

Число записей в массиве **ргаоп** .

</dd> <dt>

**ргаоп**
</dt> <dd>

Массив структур **\_ \_ \_ защиты выходного звука DRM** . **DRM \_ \_ \_ Защита звука** — это тип, определенный как [**\_ \_ Защита выходных данных DRM**](drm-output-protection.md).

</dd> </dl>

## <a name="remarks"></a>Комментарии

Нет.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Вмдрмсдк. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_ \_ \_ идентификаторы защиты аудио вывода DRM \_ \_ ex**](drm-audio-output-protection-ids-ex.md)
</dt> <dt>

[**\_ \_ \_ идентификаторы защиты вывода видео DRM \_**](drmdrm-video-output-protection-ids.md)
</dt> <dt>

[**Структуры**](drm-structures.md)
</dt> </dl>

 

 





