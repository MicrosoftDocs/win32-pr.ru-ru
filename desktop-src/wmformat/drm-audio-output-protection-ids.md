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
ms.openlocfilehash: 7e31589a229dcd5e32a0198cf7f3679846574bdb605e25a8df272b1793704b92
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119659014"
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

## <a name="remarks"></a>Remarks

Отсутствует.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Вмдрмсдк. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_ \_ \_ идентификаторы защиты аудио вывода DRM \_ \_ ex**](drm-audio-output-protection-ids-ex.md)
</dt> <dt>

[**\_ \_ \_ идентификаторы защиты вывода видео DRM \_**](drmdrm-video-output-protection-ids.md)
</dt> <dt>

[**Структуры**](drm-structures.md)
</dt> </dl>

 

 





