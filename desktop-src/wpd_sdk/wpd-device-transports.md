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
# <a name="wpd_device_transports-enumeration"></a><span data-ttu-id="7c612-104">\_ \_ Перечисление перетранспорта устройств WPD</span><span class="sxs-lookup"><span data-stu-id="7c612-104">WPD\_DEVICE\_TRANSPORTS enumeration</span></span>

<span data-ttu-id="7c612-105">Тип [**ПЕРЕЧИСЛЕНИЯ \_ \_ транспорта устройства WPD**](/windows/desktop/wpd_sdk/wpd-device-transports) указывает отношение наследования для службы.</span><span class="sxs-lookup"><span data-stu-id="7c612-105">The [**WPD\_DEVICE\_TRANSPORTS**](/windows/desktop/wpd_sdk/wpd-device-transports) enumeration type specifies the inheritance relationship for a service.</span></span> <span data-ttu-id="7c612-106">Это перечисление используется свойством **\_ \_ транспорта устройства WPD** .</span><span class="sxs-lookup"><span data-stu-id="7c612-106">This enumeration is used by the **WPD\_DEVICE\_TRANSPORT** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c612-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7c612-107">Syntax</span></span>


```C++
typedef enum tagWPD_DEVICE_TRANSPORTS { 
  WPD_DEVICE_TRANSPORT_UNSPECIFIED  = 0,
  WPD_DEVICE_TRANSPORT_USB          = 1,
  WPD_DEVICE_TRANSPORT_IP           = 2,
  WPD_DEVICE_TRANSPORT_BLUETOOTH    = 3
} WPD_DEVICE_TRANSPORTS;
```



## <a name="constants"></a><span data-ttu-id="7c612-108">Константы</span><span class="sxs-lookup"><span data-stu-id="7c612-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="7c612-109"><span id="WPD_DEVICE_TRANSPORT_UNSPECIFIED"></span><span id="wpd_device_transport_unspecified"></span>**не \_ \_ указан транспорт \_ устройства WPD**</span><span class="sxs-lookup"><span data-stu-id="7c612-109"><span id="WPD_DEVICE_TRANSPORT_UNSPECIFIED"></span><span id="wpd_device_transport_unspecified"></span>**WPD\_DEVICE\_TRANSPORT\_UNSPECIFIED**</span></span>
</dt> <dd>

<span data-ttu-id="7c612-110">Тип транспорта не указан.</span><span class="sxs-lookup"><span data-stu-id="7c612-110">The transport type was not specified.</span></span>

</dd> <dt>

<span data-ttu-id="7c612-111"><span id="WPD_DEVICE_TRANSPORT_USB"></span><span id="wpd_device_transport_usb"></span>**\_транспорт устройства \_ WPD \_ USB**</span><span class="sxs-lookup"><span data-stu-id="7c612-111"><span id="WPD_DEVICE_TRANSPORT_USB"></span><span id="wpd_device_transport_usb"></span>**WPD\_DEVICE\_TRANSPORT\_USB**</span></span>
</dt> <dd>

<span data-ttu-id="7c612-112">Устройство подключено через USB.</span><span class="sxs-lookup"><span data-stu-id="7c612-112">The device is connected through USB.</span></span>

</dd> <dt>

<span data-ttu-id="7c612-113"><span id="WPD_DEVICE_TRANSPORT_IP"></span><span id="wpd_device_transport_ip"></span>**\_ \_ \_ IP-адрес транспорта устройства WPD**</span><span class="sxs-lookup"><span data-stu-id="7c612-113"><span id="WPD_DEVICE_TRANSPORT_IP"></span><span id="wpd_device_transport_ip"></span>**WPD\_DEVICE\_TRANSPORT\_IP**</span></span>
</dt> <dd>

<span data-ttu-id="7c612-114">Устройство подключается по протоколу IP.</span><span class="sxs-lookup"><span data-stu-id="7c612-114">The device is connected through Internet Protocol (IP).</span></span>

</dd> <dt>

<span data-ttu-id="7c612-115"><span id="WPD_DEVICE_TRANSPORT_BLUETOOTH"></span><span id="wpd_device_transport_bluetooth"></span>**\_транспорт устройства \_ WPD \_ Bluetooth**</span><span class="sxs-lookup"><span data-stu-id="7c612-115"><span id="WPD_DEVICE_TRANSPORT_BLUETOOTH"></span><span id="wpd_device_transport_bluetooth"></span>**WPD\_DEVICE\_TRANSPORT\_BLUETOOTH**</span></span>
</dt> <dd>

<span data-ttu-id="7c612-116">Устройство подключено через Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="7c612-116">The device is connected through Bluetooth.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7c612-117">Требования</span><span class="sxs-lookup"><span data-stu-id="7c612-117">Requirements</span></span>



| <span data-ttu-id="7c612-118">Требование</span><span class="sxs-lookup"><span data-stu-id="7c612-118">Requirement</span></span> | <span data-ttu-id="7c612-119">Значение</span><span class="sxs-lookup"><span data-stu-id="7c612-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c612-120">Header</span><span class="sxs-lookup"><span data-stu-id="7c612-120">Header</span></span><br/> | <dl> <span data-ttu-id="7c612-121"><dt>Портабледевице. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c612-121"><dt>PortableDevice.h</dt></span></span> </dl> |



 

