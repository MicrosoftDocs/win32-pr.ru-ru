---
description: '\_ \_ Тип перечисления транспорта устройства WPD указывает отношение наследования для службы. Это перечисление используется \_ \_ свойством транспорта устройства WPD.'
ms.assetid: a9d48034-3588-4e48-a03a-91cbe679cbc9
title: Перечисление WPD_DEVICE_TRANSPORTS (Портабледевице. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_DEVICE_TRANSPORTS
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 574c6b0b00980d110f2374e7426dd101c9122854
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704067"
---
# <a name="wpd_device_transports-enumeration"></a>\_ \_ Перечисление перетранспорта устройств WPD

Тип [**ПЕРЕЧИСЛЕНИЯ \_ \_ транспорта устройства WPD**](/windows/desktop/wpd_sdk/wpd-device-transports) указывает отношение наследования для службы. Это перечисление используется свойством **\_ \_ транспорта устройства WPD** .

## <a name="syntax"></a>Синтаксис


```C++
typedef enum tagWPD_DEVICE_TRANSPORTS { 
  WPD_DEVICE_TRANSPORT_UNSPECIFIED  = 0,
  WPD_DEVICE_TRANSPORT_USB          = 1,
  WPD_DEVICE_TRANSPORT_IP           = 2,
  WPD_DEVICE_TRANSPORT_BLUETOOTH    = 3
} WPD_DEVICE_TRANSPORTS;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="WPD_DEVICE_TRANSPORT_UNSPECIFIED"></span><span id="wpd_device_transport_unspecified"></span>**не \_ \_ указан транспорт \_ устройства WPD**
</dt> <dd>

Тип транспорта не указан.

</dd> <dt>

<span id="WPD_DEVICE_TRANSPORT_USB"></span><span id="wpd_device_transport_usb"></span>**\_транспорт устройства \_ WPD \_ USB**
</dt> <dd>

Устройство подключено через USB.

</dd> <dt>

<span id="WPD_DEVICE_TRANSPORT_IP"></span><span id="wpd_device_transport_ip"></span>**\_ \_ \_ IP-адрес транспорта устройства WPD**
</dt> <dd>

Устройство подключается по протоколу IP.

</dd> <dt>

<span id="WPD_DEVICE_TRANSPORT_BLUETOOTH"></span><span id="wpd_device_transport_bluetooth"></span>**\_транспорт устройства \_ WPD \_ Bluetooth**
</dt> <dd>

Устройство подключено через Bluetooth.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Портабледевице. h</dt> </dl> |



 

