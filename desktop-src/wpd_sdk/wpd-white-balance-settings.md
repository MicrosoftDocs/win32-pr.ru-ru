---
description: '\_ \_ Тип перечисления «параметры белого баланса» \_ содержит сведения о том, как видеоролики и видеоизображения выводят цветовые каналы для достижения правильного баланса белого.'
ms.assetid: 7bc173dd-4fdd-4b03-994e-f0711c910618
title: Перечисление WPD_WHITE_BALANCE_SETTINGS (Портабледевице. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_WHITE_BALANCE_SETTINGS
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 1b596dd6d8fbcc2b2a875b70d80e8eb4040c966590642a004c551ec159c9f5d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117842051"
---
# <a name="wpd_white_balance_settings-enumeration"></a>\_ \_ Перечисление параметров белого баланса WPD \_

Тип перечисления « **\_ \_ \_ Параметры белого баланса** » содержит сведения о том, как видеоролики и видеоизображения выводят цветовые каналы для достижения правильного баланса белого.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum WPD_WHITE_BALANCE_SETTINGS { 
  WPD_WHITE_BALANCE_UNDEFINED           = 0,
  WPD_WHITE_BALANCE_MANUAL              = 1,
  WPD_WHITE_BALANCE_AUTOMATIC           = 2,
  WPD_WHITE_BALANCE_ONE_PUSH_AUTOMATIC  = 3,
  WPD_WHITE_BALANCE_DAYLIGHT            = 4,
  WPD_WHITE_BALANCE_TUNGSTEN            = 5,
  WPD_WHITE_BALANCE_FLASH               = 6
} ;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="WPD_WHITE_BALANCE_UNDEFINED"></span><span id="wpd_white_balance_undefined"></span>**\_неопределенный \_ баланс белого WPD \_**
</dt> <dd>

Это значение не было определено.

</dd> <dt>

<span id="WPD_WHITE_BALANCE_MANUAL"></span><span id="wpd_white_balance_manual"></span>**\_ \_ Ручное баланс белого по \_**
</dt> <dd>

Баланс белого задается явным образом с помощью [свойства \_ \_ \_ \_ коэффициента по прежнему RGB-изображения WPD](still-image-properties.md) и не изменяется самим собой.

</dd> <dt>

<span id="WPD_WHITE_BALANCE_AUTOMATIC"></span><span id="wpd_white_balance_automatic"></span>**\_белый баланс белого, \_ \_ Автоматический**
</dt> <dd>

Устройство будет устанавливать баланс белого цвета.

</dd> <dt>

<span id="WPD_WHITE_BALANCE_ONE_PUSH_AUTOMATIC"></span><span id="wpd_white_balance_one_push_automatic"></span>**\_белый баланс по белого \_ регулятора для \_ \_ \_ автоматической отправки**
</dt> <dd>

Устройство задаст баланс белого, но только когда пользователь отправит кнопку захвата устройства при надежде устройства в белом поле.

</dd> <dt>

<span id="WPD_WHITE_BALANCE_DAYLIGHT"></span><span id="wpd_white_balance_daylight"></span>**\_белый \_ баланс на \_ летнее время**
</dt> <dd>

Устройство будет использовать баланс белого цвета, подходящий для использования в большинстве параметров перехода на летнее время.

</dd> <dt>

<span id="WPD_WHITE_BALANCE_TUNGSTEN"></span><span id="wpd_white_balance_tungsten"></span>**\_тунгстен белого \_ баланса \_ WPD**
</dt> <dd>

Устройство будет использовать баланс белого цвета, подходящий для использования в большинстве инкандесцент параметров освещения.

</dd> <dt>

<span id="WPD_WHITE_BALANCE_FLASH"></span><span id="wpd_white_balance_flash"></span>**\_ \_ вспышка белого баланса WPD \_**
</dt> <dd>

Устройство будет использовать номера белого баланса, которые подходят для использования с Flash.

</dd> </dl>

## <a name="remarks"></a>Remarks

Это перечисление используется свойством " [ \_ неподвижный \_ \_ \_ баланс изображения WPD](still-image-properties.md) ".

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Портабледевице. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Структуры и типы перечислений**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




