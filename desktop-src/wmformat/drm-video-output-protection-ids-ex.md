---
title: Структура DRM_VIDEO_OUTPUT_PROTECTION_IDS_EX (Вмдрмсдк. h)
description: В \_ \_ \_ \_ структуре идентификаторов защиты видео DRM \_ содержится массив \_ \_ структур защиты вывода видео DRM \_ .
ms.assetid: 89de0ade-fa86-4081-b65b-9c84fb68cf3d
keywords:
- Формат DRM_VIDEO_OUTPUT_PROTECTION_IDS_EX структуры Windows Media
- структура формат мультимедиа Windows
topic_type:
- apiref
api_name:
- DRM_VIDEO_OUTPUT_PROTECTION_IDS_EX
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2e7cc5ec0b4b14d88deb317e62e3e1cd4f92b57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704048"
---
# <a name="drm_video_output_protection_ids_ex-structure"></a>\_ \_ Идентификатор защиты вывода видео DRM — \_ \_ \_ Структура ex

В **структуре \_ \_ \_ \_ \_ идентификаторов защиты видео DRM** содержится массив структур **\_ \_ \_ защиты вывода видео DRM** .

## <a name="syntax"></a>Синтаксис


```C++
typedef struct DRM_VIDEO_OUTPUT_PROTECTION_IDS_EX {
  DWORD                          dwVersion;
  WORD                           cEntries;
  DRM_VIDEO_OUTPUT_PROTECTION_EX *rgVop;
} ;
```



## <a name="members"></a>Члены

<dl> <dt>

**двверсион**
</dt> <dd>

Номер версии.

</dd> <dt>

**центриес**
</dt> <dd>

Число элементов в массиве, на которые ссылается **ргвоп**.

</dd> <dt>

**ргвоп**
</dt> <dd>

Адрес массива структур для **\_ \_ \_ \_ защиты вывода видео DRM** . **DRM \_ \_ \_ Защита от вывода видео \_ ex** — это тип, определенный как [**\_ \_ Защита \_ выходных данных DRM**](drm-output-protection-ex.md), например.

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

 

 





