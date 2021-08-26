---
title: Структура WMDRM_ANALOG_VIDEO_RESTRICTIONS_EX (Вмдрмсдк. h)
description: '\_ \_ \_ Примерная структура ограничений аналогового видео WMDRM \_ содержит расширенные сведения об ограничении для воспроизведения содержимого в виде аналогового видео.'
ms.assetid: fe9092fe-a717-4377-9653-1cc07795319f
keywords:
- Формат WMDRM_ANALOG_VIDEO_RESTRICTIONS_EX структуры Windows Media
- структура формат мультимедиа Windows
topic_type:
- apiref
api_name:
- WMDRM_ANALOG_VIDEO_RESTRICTIONS_EX
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e9cbacff2d330c869c35eb7a3d1ca46ae6c80a030495ffec42eabc3726436c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006544"
---
# <a name="wmdrm_analog_video_restrictions_ex-structure"></a>\_Ограничения аналогового видео WMDRM — \_ \_ \_ Структура

**\_ \_ \_ \_ Примерная структура ограничений аналогового видео WMDRM** содержит расширенные сведения об ограничении для воспроизведения содержимого в виде аналогового видео.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct WMDRM_ANALOG_VIDEO_RESTRICTIONS_EX {
  DWORD dwVersion;
  GUID  guidRestrictionID;
  DWORD cbRestrictionData;
  BYTE  *pbRestrictionData;
} ;
```



## <a name="members"></a>Члены

<dl> <dt>

**двверсион**
</dt> <dd>

Номер версии.

</dd> <dt>

**гуидрестриктионид**
</dt> <dd>

Идентификатор ограничения.

</dd> <dt>

**кбрестриктиондата**
</dt> <dd>

Размер данных ограничения в байтах.

</dd> <dt>

**пбрестриктиондата**
</dt> <dd>

Данные ограничений.

</dd> </dl>

## <a name="remarks"></a>Remarks

Отсутствует.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Вмдрмсдк. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Структуры**](drm-structures.md)
</dt> <dt>

[**\_ограничения аналогового \_ видео WMDRM \_**](wmdrm-analog-video-restrictions.md)
</dt> </dl>

 

 





