---
title: Структура DRM_PLAY_OPL (Вмдрмсдк. h)
description: Структура DRM \_ Play \_ ОПЛ содержит сведения об уровнях защиты выходных данных (оплс), указанных в лицензии на действия воспроизведения.
ms.assetid: 10703893-630c-4cbe-a0b0-d2890905daba
keywords:
- Формат DRM_PLAY_OPL структуры Windows Media
- структура формат мультимедиа Windows
topic_type:
- apiref
api_name:
- DRM_PLAY_OPL
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a40d8fe4e8b3c820f9d7bcb405b5c0806040182
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699232"
---
# <a name="drm_play_opl-structure"></a>\_Структура DRM Play \_ ОПЛ

Структура **DRM \_ Play \_ ОПЛ** содержит сведения об уровнях защиты выходных данных (оплс), указанных в лицензии на действия воспроизведения.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct DRM_PLAY_OPL {
  DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS minOPL;
  DRM_OPL_OUTPUT_IDS                   oplIdReserved;
  DRM_VIDEO_OUTPUT_PROTECTION_IDS      vopi;
} ;
```



## <a name="members"></a>Члены

<dl> <dt>

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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Вмдрмсдк. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_ОПЛ копирования \_ DRM**](drmdrm-copy-opl.md)
</dt> <dt>

[**DRM \_ Play \_ ОПЛ \_ ex**](drm-play-opl-ex.md)
</dt> <dt>

[**Структуры**](drm-structures.md)
</dt> </dl>

 

 





