---
title: Структура DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS (Вмдрмсдк. h)
description: '\_ \_ \_ Структура уровней минимальной защиты от DRM \_ содержит минимальные уровни защиты выходных данных (оплс) для воспроизведения содержимого различных типов. Устройство должно поддерживать минимальный ОПЛ для типа данных, чтобы получить данные этого типа из модуля чтения.'
ms.assetid: 6232ecd4-9829-4de3-9810-70e3d3c129a9
keywords:
- Формат DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS структуры Windows Media
- структура формат мультимедиа Windows
topic_type:
- apiref
api_name:
- DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5559527507f0399a09661dfe380f51d11e10750eddf7d996b38d110e4f38e37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119708924"
---
# <a name="drm_minimum_output_protection_levels-structure"></a>\_Минимальная \_ \_ \_ Структура уровней защиты выходных данных DRM

Структура **\_ уровней минимальной \_ \_ защиты от \_ DRM** содержит минимальные уровни защиты выходных данных (оплс) для воспроизведения содержимого различных типов. Устройство должно поддерживать минимальный ОПЛ для типа данных, чтобы получить данные этого типа из модуля чтения.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS {
  WORD wCompressedDigitalVideo;
  WORD wUncompressedDigitalVideo;
  WORD wAnalogVideo;
  WORD wCompressedDigitalAudio;
  WORD wUncompressedDigitalAudio;
} ;
```



## <a name="members"></a>Члены

<dl> <dt>

**вкомпресседдигиталвидео**
</dt> <dd>

Минимальный ОПЛ, необходимый для получения сжатого цифрового видео.

</dd> <dt>

**вункомпресседдигиталвидео**
</dt> <dd>

Минимальный ОПЛ, необходимый для получения несжатого цифрового видео.

</dd> <dt>

**ваналогвидео**
</dt> <dd>

Минимальный ОПЛ, необходимый для получения аналогового видео.

</dd> <dt>

**вкомпресседдигиталаудио**
</dt> <dd>

Для получения сжатого цифрового аудио требуется минимум ОПЛ.

</dd> <dt>

**вункомпресседдигиталаудио**
</dt> <dd>

Минимальный ОПЛ, необходимый для получения несжатого цифрового аудио.

</dd> </dl>

## <a name="remarks"></a>Remarks

Эта структура используется в качестве члена структуры [**DRM \_ Play \_ ОПЛ**](drmdrm-play-opl.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Вмдрмсдк. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Структуры**](drm-structures.md)
</dt> </dl>

 

 





