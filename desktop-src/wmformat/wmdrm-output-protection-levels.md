---
title: Структура WMDRM_OUTPUT_PROTECTION_LEVELS (Вмдрмсдк. h)
description: '\_ \_ Структура уровней защиты WMDRM OUTPUT \_ содержит уровни защиты выходных данных (оплс), необходимые для выполнения различных действий в лицензии.'
ms.assetid: 6b284180-1033-4c57-b010-6d4ab4bc593a
keywords:
- Формат WMDRM_OUTPUT_PROTECTION_LEVELS структуры Windows Media
- структура формат мультимедиа Windows
topic_type:
- apiref
api_name:
- WMDRM_OUTPUT_PROTECTION_LEVELS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d720a8aef42178da188b71a1635d97031b138397
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717864"
---
# <a name="wmdrm_output_protection_levels-structure"></a>\_ \_ Структура уровней защиты данных WMDRM \_

Структура **\_ \_ \_ уровней защиты WMDRM Output** содержит уровни защиты выходных данных (оплс), необходимые для выполнения различных действий в лицензии.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct WMDRM_OUTPUT_PROTECTION_LEVELS {
  WORD wCompressedDigitalVideo;
  WORD wUncompressedDigitalVideo;
  WORD wAnalogVideo;
  WORD wCompressedDigitalAudio;
  WORD wUncompressedDigitalAudio;
  WORD wMinimumCopyProtectionLevel;
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

</dd> <dt>

**вминимумкопипротектионлевел**
</dt> <dd>

Для копирования содержимого требуется минимум ОПЛ.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Эта структура используется методом [**ивмдрмлиценсе:: жетаутпутпротектионлевелс**](iwmdrmlicense-getoutputprotectionlevels.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Вмдрмсдк. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Структуры**](drm-structures.md)
</dt> </dl>

 

 





