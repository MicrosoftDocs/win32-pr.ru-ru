---
description: '\_Тип перечисления «режимы отслеживания фокуса» для WPD \_ описывает, \_ как устройство должно решить, какую часть кадра использовать для установки фокуса.'
ms.assetid: 0e68d0e8-2ce3-4994-99c2-2ff2293d8a20
title: Перечисление WPD_FOCUS_METERING_MODES (Портабледевице. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_FOCUS_METERING_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: f59d6a2f1cabbbe7b072a87caa3e5d74d012fc49
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668682"
---
# <a name="wpd_focus_metering_modes-enumeration"></a>\_ \_ Перечисление режимов метрик ФОКУСа WPD \_

Тип перечисления « **\_ \_ \_ режимы отслеживания фокуса** » для WPD описывает, как устройство должно решить, какую часть кадра использовать для установки фокуса.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum WPD_FOCUS_METERING_MODES { 
  WPD_FOCUS_METERING_MODE_UNDEFINED    = 0,
  WPD_FOCUS_METERING_MODE_CENTER_SPOT  = 1,
  WPD_FOCUS_METERING_MODE_MULTI_SPOT   = 2
} ;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="WPD_FOCUS_METERING_MODE_UNDEFINED"></span><span id="wpd_focus_metering_mode_undefined"></span>**\_режим метрик фокуса WPD не \_ \_ \_ определен**
</dt> <dd>

Указывает, что режим фокусировки не указан.

</dd> <dt>

<span id="WPD_FOCUS_METERING_MODE_CENTER_SPOT"></span><span id="wpd_focus_metering_mode_center_spot"></span>**\_ \_ \_ \_ центр отслеживания фокусирований для WPD \_**
</dt> <dd>

Фокусируется на центре области с рамками.

</dd> <dt>

<span id="WPD_FOCUS_METERING_MODE_MULTI_SPOT"></span><span id="wpd_focus_metering_mode_multi_spot"></span>**\_ \_ \_ \_ множественная разкраска в режиме метрик фокуса WPD \_**
</dt> <dd>

Определение фокуса путем анализа нескольких частей области в рамке.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Это перечисление задается свойством " [ \_ \_ \_ \_ \_ режим отслеживания фокуса" для неподвижных изображений WPD](still-image-properties.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Портабледевице. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Структуры и типы перечислений**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




