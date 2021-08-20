---
description: '\_Тип перечисления "счетчики раскрытия" WPD \_ \_ описывает режим измерения, который будет использоваться при оценке экспозиции для записи образа на устройстве.'
ms.assetid: 5e92013c-600d-4128-ab59-1cfa8953db67
title: Перечисление WPD_EXPOSURE_METERING_MODES (Портабледевице. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_EXPOSURE_METERING_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 2a165493142fc25ea64adc2678e8bc4ccbeace32e245422f0fcea419063a26ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117842284"
---
# <a name="wpd_exposure_metering_modes-enumeration"></a>\_ \_ Перечисление режимов измерения экспозиции для WPD \_

Тип перечисления " **\_ \_ счетчики \_ раскрытия" WPD** описывает режим измерения, который будет использоваться при оценке экспозиции для записи образа на устройстве.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum WPD_EXPOSURE_METERING_MODES { 
  WPD_EXPOSURE_METERING_MODE_UNDEFINED                = 0,
  WPD_EXPOSURE_METERING_MODE_AVERAGE                  = 1,
  WPD_EXPOSURE_METERING_MODE_CENTER_WEIGHTED_AVERAGE  = 2,
  WPD_EXPOSURE_METERING_MODE_MULTI_SPOT               = 3,
  WPD_EXPOSURE_METERING_MODE_CENTER_SPOT              = 4
} ;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="WPD_EXPOSURE_METERING_MODE_UNDEFINED"></span><span id="wpd_exposure_metering_mode_undefined"></span>**\_неопределенный \_ режим отслеживания \_ \_ вероятности WPD**
</dt> <dd>

Режим измерения не определен.

</dd> <dt>

<span id="WPD_EXPOSURE_METERING_MODE_AVERAGE"></span><span id="wpd_exposure_metering_mode_average"></span>**\_ \_ \_ среднее значение режима метрик ВЫдержки от WPD \_**
</dt> <dd>

Использовать среднее значение раскрытия в полном образе.

</dd> <dt>

<span id="WPD_EXPOSURE_METERING_MODE_CENTER_WEIGHTED_AVERAGE"></span><span id="wpd_exposure_metering_mode_center_weighted_average"></span>**\_ \_ \_ \_ \_ средневзвешенное значение в центре режима измерения экспозиции \_**
</dt> <dd>

Используйте среднюю раскрытие, когда центр изображения заданный дополнительный вес.

</dd> <dt>

<span id="WPD_EXPOSURE_METERING_MODE_MULTI_SPOT"></span><span id="wpd_exposure_metering_mode_multi_spot"></span>**\_ \_ \_ \_ множественная разкраска в режиме метрик экспозиции WPD \_**
</dt> <dd>

Используйте многоуровневый метод усреднения.

</dd> <dt>

<span id="WPD_EXPOSURE_METERING_MODE_CENTER_SPOT"></span><span id="wpd_exposure_metering_mode_center_spot"></span>**\_ \_ геометрическое \_ \_ место центра режима \_ отслеживания вероятности WPD**
</dt> <dd>

Используйте метод усреднения по центру.

</dd> </dl>

## <a name="remarks"></a>Remarks

Указывает режим измерения для устройства. Это перечисление используется свойством "режим оценки вероятности" для [ \_ неподвижных \_ изображений \_ \_ \_ WPD](still-image-properties.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Портабледевице. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Структуры и типы перечислений**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




