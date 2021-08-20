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
ms.openlocfilehash: 4a19d7098266857f8a17e395ad749b216e45ce101278812f67c032943933955a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843965"
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

## <a name="remarks"></a>Remarks

Эта структура используется методом [**ивмдрмлиценсе:: жетаутпутпротектионлевелс**](iwmdrmlicense-getoutputprotectionlevels.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Вмдрмсдк. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Структуры**](drm-structures.md)
</dt> </dl>

 

 





