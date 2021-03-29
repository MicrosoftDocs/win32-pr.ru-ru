---
description: '\_ \_ Тип перечисления WPD Power Sources описывает источник питания, который использует устройство.'
ms.assetid: feebf213-052d-4315-84db-2109cab5f179
title: Перечисление WPD_POWER_SOURCES (Портабледевице. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_POWER_SOURCES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: bf9a153d4d41a64b639f796ea2ba0eeb9e567a32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648036"
---
# <a name="wpd_power_sources-enumeration"></a>\_ \_ Перечисление источников питания WPD

Тип перечисления **WPD \_ Power \_ Sources** описывает источник питания, который использует устройство.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum WPD_POWER_SOURCES { 
  WPD_POWER_SOURCE_BATTERY   = 0,
  WPD_POWER_SOURCE_EXTERNAL  = 1
} ;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="WPD_POWER_SOURCE_BATTERY"></span><span id="wpd_power_source_battery"></span>**\_питание источника питания (WPD) \_ \_**
</dt> <dd>

Источник питания устройства — батарея.

</dd> <dt>

<span id="WPD_POWER_SOURCE_EXTERNAL"></span><span id="wpd_power_source_external"></span>**\_ \_ внешний источник питания \_ WPD**
</dt> <dd>

Устройство использует внешний источник питания.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Это перечисление используется свойством [ \_ \_ \_ источник питания устройства WPD](device-properties.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Портабледевице. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Структуры и типы перечислений**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




