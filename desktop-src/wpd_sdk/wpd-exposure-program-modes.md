---
description: '\_Тип ПЕРЕЧИСЛЕНИЯ WPD экспозиции \_ \_ mode описывает режим экспозиции, используемый при записи образов с помощью устройства.'
ms.assetid: 68b76294-6ad3-4f4a-bf02-bc31c9e8ac62
title: Перечисление WPD_EXPOSURE_PROGRAM_MODES (Портабледевице. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_EXPOSURE_PROGRAM_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: dc64012c4f13f84abef55d2426c856b931eb447e61df4f04c69781c089857930
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083278"
---
# <a name="wpd_exposure_program_modes-enumeration"></a>\_ \_ Перечисление режимов программы "ЭКСПОЗИЦИя WPD" \_

Тип перечисления **WPD \_ экспозиции \_ \_** Mode описывает режим экспозиции, используемый при записи образов с помощью устройства.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum WPD_EXPOSURE_PROGRAM_MODES { 
  WPD_EXPOSURE_PROGRAM_MODE_UNDEFINED          = 0,
  WPD_EXPOSURE_PROGRAM_MODE_MANUAL             = 1,
  WPD_EXPOSURE_PROGRAM_MODE_AUTO               = 2,
  WPD_EXPOSURE_PROGRAM_MODE_APERTURE_PRIORITY  = 3,
  WPD_EXPOSURE_PROGRAM_MODE_SHUTTER_PRIORITY   = 4,
  WPD_EXPOSURE_PROGRAM_MODE_CREATIVE           = 5,
  WPD_EXPOSURE_PROGRAM_MODE_ACTION             = 6,
  WPD_EXPOSURE_PROGRAM_MODE_PORTRAIT           = 7
} ;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_UNDEFINED"></span><span id="wpd_exposure_program_mode_undefined"></span>**\_режим программы экспозиции WPD не \_ \_ \_ определен**
</dt> <dd>

Не указан режим экспозиции.

</dd> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_MANUAL"></span><span id="wpd_exposure_program_mode_manual"></span>**\_руководство по \_ \_ режиму \_ программы для WPD**
</dt> <dd>

Приложение должно указать все параметры экспозиции.

</dd> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_AUTO"></span><span id="wpd_exposure_program_mode_auto"></span>**\_ \_ режим автоматической экспозиции программы WPD \_ \_ Auto**
</dt> <dd>

Использовать режим автоматической экспозиции, определяемый устройством.

</dd> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_APERTURE_PRIORITY"></span><span id="wpd_exposure_program_mode_aperture_priority"></span>**\_ \_ \_ \_ приоритет режима АПЕРТУРы для \_ программы WPD**
</dt> <dd>

Автоматический режим экспозиции, указывающий, что значение апертуры линзы должно оставаться фиксированным, но скорость затвора должна быть определена устройством.

</dd> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_SHUTTER_PRIORITY"></span><span id="wpd_exposure_program_mode_shutter_priority"></span>**\_ \_ \_ \_ приоритет выдержкы в режиме \_ программы**
</dt> <dd>

Автоматический режим экспозиции, который указывает, что скорость затвора должна оставаться фиксированной, но этот Апертура должен быть определен устройством.

</dd> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_CREATIVE"></span><span id="wpd_exposure_program_mode_creative"></span>**\_ \_ \_ творческий режим программы, подверженной атаке WPD \_**
</dt> <dd>

Автоматический режим экспозиции, который пытается максимально увеличить глубину поля.

</dd> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_ACTION"></span><span id="wpd_exposure_program_mode_action"></span>**\_ \_ \_ действие режима программы экспозиции WPD \_**
</dt> <dd>

Автоматический режим экспозиции, который пытается максимально увеличить скорость затвора.

</dd> <dt>

<span id="WPD_EXPOSURE_PROGRAM_MODE_PORTRAIT"></span><span id="wpd_exposure_program_mode_portrait"></span>**режим программы "экспозиция" (WPD) \_ \_ \_ \_ Книжная**
</dt> <dd>

Автоматический режим экспозиции, указывающий относительно полную глубину поля.

</dd> </dl>

## <a name="remarks"></a>Remarks

Указывает режим программы экспозиции устройства. Это перечисление используется в свойстве " [ \_ режим программы" в \_ \_ \_ \_ режиме уязвимости с образом WPD](still-image-properties.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Портабледевице. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Структуры и типы перечислений**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




