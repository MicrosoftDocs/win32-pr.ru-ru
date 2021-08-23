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
ms.openlocfilehash: 8ca712a758d23f70d2a1f8760272b821adeec548a1d719c9564cdc8cf17cdeb4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119657424"
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

## <a name="remarks"></a>Remarks

Это перечисление используется в свойстве [ \_ \_ \_ \_ режима эффектов для изображения WPD](still-image-properties.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Портабледевице. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Структуры и типы перечислений**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




