---
description: '\_ \_ Перечисление Units Streams указывает типы единиц, которые будут использоваться для операций ипортабледевицеунитсстреам.'
ms.assetid: BE668696-7AF3-44AA-891A-9BFF67FB5544
title: Перечисление WPD_STREAM_UNITS (Портабледевицетипес. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_STREAM_UNITS
api_type:
- HeaderDef
api_location:
- PortableDeviceTypes.h
ms.openlocfilehash: d2419453beac6b493ddd1bbbe1281b1596ce00456599074b3872fecb003550c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119440764"
---
# <a name="wpd_stream_units-enumeration"></a>\_Перечисление единиц потоковой передачи WPD \_

Перечисление **\_ \_ Units Streams** указывает типы единиц, которые будут использоваться для операций [**ипортабледевицеунитсстреам**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceunitsstream) .

## <a name="syntax"></a>Синтаксис


```C++
typedef enum _WPD_STREAM_UNITS { 
  WPD_STREAM_UNITS_BYTES         = 0,
  WPD_STREAM_UNITS_FRAMES        = 1,
  WPD_STREAM_UNITS_ROWS          = 2,
  WPD_STREAM_UNITS_MILLISECONDS  = 3,
  WPD_STREAM_UNITS_MICROSECONDS  = 4
} WPD_STREAM_UNITS;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="WPD_STREAM_UNITS_BYTES"></span><span id="wpd_stream_units_bytes"></span>**\_число потоков потока WPD \_ \_**
</dt> <dd>

Единицы потоковой передачи указываются в байтах.

</dd> <dt>

<span id="WPD_STREAM_UNITS_FRAMES"></span><span id="wpd_stream_units_frames"></span>**\_кадры потоковых \_ единиц WPD \_**
</dt> <dd>

Единицы потоковой передачи указываются в кадрах.

</dd> <dt>

<span id="WPD_STREAM_UNITS_ROWS"></span><span id="wpd_stream_units_rows"></span>**\_ \_ число строк в ПОТОКе WPD \_**
</dt> <dd>

Единицы потоковой передачи указываются в строках.

</dd> <dt>

<span id="WPD_STREAM_UNITS_MILLISECONDS"></span><span id="wpd_stream_units_milliseconds"></span>**\_число единиц потока WPD в \_ \_ миллисекундах**
</dt> <dd>

Единицы потоковой передачи указываются в миллисекундах.

</dd> <dt>

<span id="WPD_STREAM_UNITS_MICROSECONDS"></span><span id="wpd_stream_units_microseconds"></span>**\_МИКРОсекунды потоковых \_ модулей WPD \_**
</dt> <dd>

Единицы потоковой передачи указываются в микросекундах.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                                       |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                        |
| Header<br/>                   | <dl> <dt>Портабледевицетипес. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ипортабледевицеунитсстреам**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceunitsstream)
</dt> <dt>

[**Ипортабледевицеунитсстреам:: Сикинунитс**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceunitsstream-seekinunits)
</dt> </dl>

 

 




