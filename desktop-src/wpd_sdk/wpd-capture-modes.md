---
description: '\_Тип перечисления «режимы записи WPD» \_ описывает режим сбора данных о времени записи образа.'
ms.assetid: bfe96176-d018-4b39-a938-035757111784
title: Перечисление WPD_CAPTURE_MODES (Портабледевице. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_CAPTURE_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: e56e3e66cd20abaeb1daf0a674633a36b57a9575
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717857"
---
# <a name="wpd_capture_modes-enumeration"></a>\_ \_ Перечисление режимов захвата WPD

Тип перечисления « **\_ \_ режимы записи WPD** » описывает режим сбора данных о времени записи образа.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum WPD_CAPTURE_MODES { 
  WPD_CAPTURE_MODE_UNDEFINED  = 0,
  WPD_CAPTURE_MODE_NORMAL     = 1,
  WPD_CAPTURE_MODE_BURST      = 2,
  WPD_CAPTURE_MODE_TIMELAPSE  = 3
} ;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="WPD_CAPTURE_MODE_UNDEFINED"></span><span id="wpd_capture_mode_undefined"></span>**\_режим записи WPD не \_ \_ определен**
</dt> <dd>

Режим записи не определен.

</dd> <dt>

<span id="WPD_CAPTURE_MODE_NORMAL"></span><span id="wpd_capture_mode_normal"></span>**\_режим записи WPD " \_ \_ нормальный"**
</dt> <dd>

Не следует использовать задержки или пакетный режим.

</dd> <dt>

<span id="WPD_CAPTURE_MODE_BURST"></span><span id="wpd_capture_mode_burst"></span>**\_ \_ ускоренный режим записи WPD \_**
</dt> <dd>

Указывает, что определенное количество образов должно быть захвачено с определенным интервалом между ними. Количество образов для захвата и временной задержки между ними задается с помощью [ \_ \_ \_ \_ счетчика "число неподвижных](still-image-properties.md) [образов \_ " \_ \_ \_ ](still-image-properties.md) .

</dd> <dt>

<span id="WPD_CAPTURE_MODE_TIMELAPSE"></span><span id="wpd_capture_mode_timelapse"></span>**\_ \_ тимелапсе режим записи \_ WPD**
</dt> <dd>

Для записи образов следует использовать фотографию времени. Число образов и интервал между ними описывается в разделе [ \_ \_ \_ тимелапсе \_ Number](still-image-properties.md) и [WPD, \_ все равно Image \_ \_ тимелапсе \_ Interval](still-image-properties.md) Properties.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Это перечисление используется в свойстве " [ \_ \_ \_ \_ режим захвата WPD-образа](still-image-properties.md) ".

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Портабледевице. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Свойства и атрибуты WPD**](properties-and-attributes.md)
</dt> <dt>

[**Структуры и типы перечислений**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




