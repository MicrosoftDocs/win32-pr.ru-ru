---
title: Структура DRM_PLAY_OPL_EX (Вмдрмсдк. h)
description: Структура DRM \_ Play \_ ОПЛ \_ ex содержит сведения об уровнях защиты выходных данных (оплс), указанных в лицензии на действия воспроизведения.
ms.assetid: 287f6681-f12e-4ef3-b802-24ee7b94bc7f
keywords:
- Формат DRM_PLAY_OPL_EX структуры Windows Media
- структура формат мультимедиа Windows
topic_type:
- apiref
api_name:
- DRM_PLAY_OPL_EX
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a89ca0c6b1cf33a422265fb177e1b1432a52fbd12b3f9fda658125682f3888ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117848443"
---
# <a name="drm_play_opl_ex-structure"></a>\_Структура DRM Play \_ ОПЛ \_ ex

Структура **DRM \_ Play \_ ОПЛ \_ ex** содержит сведения об уровнях защиты выходных данных (оплс), указанных в лицензии на действия воспроизведения.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct DRM_PLAY_OPL_EX {
  DWORD                                dwVersion;
  DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS minOPL;
  DRM_OPL_OUTPUT_IDS                   oplIdReserved;
  DRM_VIDEO_OUTPUT_PROTECTION_IDS_EX   vopi;
} ;
```



## <a name="members"></a>Члены

<dl> <dt>

**двверсион**
</dt> <dd>

Номер версии.

</dd> <dt>

**минопл**
</dt> <dd>

[**DRM \_ Минимальная \_ Структура \_ \_ уровней защиты выходных данных**](drmdrm-minimum-output-protection-levels.md) , содержащая минимум ОПЛ, необходимый для воспроизведения содержимого в различных форматах.

</dd> <dt>

**оплидресервед**
</dt> <dd>

Зарезервировано для последующего использования.

</dd> <dt>

**вопи**
</dt> <dd>

[**DRM \_ Структура \_ \_ \_ идентификаторов защиты видео**](drmdrm-video-output-protection-ids.md) , содержащая идентификаторы защиты видео, которые применяются к воспроизведению содержимого.

</dd> </dl>

## <a name="remarks"></a>Remarks

Эта структура идентична структуре **DRM \_ Play \_ ОПЛ** , за исключением того, что она включает номер версии.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Вмдрмсдк. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**DRM \_ Play \_ ОПЛ**](drmdrm-play-opl.md)
</dt> <dt>

[**Структуры**](drm-structures.md)
</dt> </dl>

 

 





