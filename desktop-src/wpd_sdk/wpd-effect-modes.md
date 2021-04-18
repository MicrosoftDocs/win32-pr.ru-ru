---
description: '\_Тип перечисления «режимы влияния WPD» \_ описывает различные визуальные эффекты, которые могут быть применены к изображению.'
ms.assetid: 7624fccb-e416-4db4-978e-410c4c236328
title: Перечисление WPD_EFFECT_MODES (Портабледевице. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_EFFECT_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 7e29f89207a74d335fbe1c2561f8dcf9cec3e923
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694431"
---
# <a name="wpd_effect_modes-enumeration"></a>\_ \_ Перечисление режимов влияния WPD

Тип перечисления « **\_ \_ режимы влияния WPD** » описывает различные визуальные эффекты, которые могут быть применены к изображению.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum WPD_EFFECT_MODES { 
  WPD_EFFECT_MODE_UNDEFINED        = 0,
  WPD_EFFECT_MODE_COLOR            = 1,
  WPD_EFFECT_MODE_BLACK_AND_WHITE  = 2,
  WPD_EFFECT_MODE_SEPIA            = 3
} ;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="WPD_EFFECT_MODE_UNDEFINED"></span><span id="wpd_effect_mode_undefined"></span>**\_режим влияния WPD не \_ \_ определен**
</dt> <dd>

Не указан ни один результат.

</dd> <dt>

<span id="WPD_EFFECT_MODE_COLOR"></span><span id="wpd_effect_mode_color"></span>**\_ \_ Цвет режима влияния \_ WPD**
</dt> <dd>

Изображение должно иметь цвет.

</dd> <dt>

<span id="WPD_EFFECT_MODE_BLACK_AND_WHITE"></span><span id="wpd_effect_mode_black_and_white"></span>**\_режим влияния WPD — \_ \_ черный \_ и \_ белый**
</dt> <dd>

Изображение должно быть черно-белым.

</dd> <dt>

<span id="WPD_EFFECT_MODE_SEPIA"></span><span id="wpd_effect_mode_sepia"></span>**\_режим влияния \_ WPD \_ выцветшей**
</dt> <dd>

Образ должен быть выцветшей.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Это перечисление используется в свойстве [ \_ \_ \_ \_ режима эффектов для изображения WPD](still-image-properties.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Портабледевице. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Структуры и типы перечислений**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




