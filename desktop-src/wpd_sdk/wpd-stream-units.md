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
ms.openlocfilehash: 8e70455402a49673b574a0c696b6dda30cc6a884
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816808"
---
# <a name="wpd_stream_units-enumeration"></a><span data-ttu-id="f7e59-103">\_Перечисление единиц потоковой передачи WPD \_</span><span class="sxs-lookup"><span data-stu-id="f7e59-103">WPD\_STREAM\_UNITS enumeration</span></span>

<span data-ttu-id="f7e59-104">Перечисление **\_ \_ Units Streams** указывает типы единиц, которые будут использоваться для операций [**ипортабледевицеунитсстреам**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceunitsstream) .</span><span class="sxs-lookup"><span data-stu-id="f7e59-104">The **WPD\_STREAM\_UNITS** enumeration specifies the unit types to be used for [**IPortableDeviceUnitsStream**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceunitsstream) operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7e59-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f7e59-105">Syntax</span></span>


```C++
typedef enum _WPD_STREAM_UNITS { 
  WPD_STREAM_UNITS_BYTES         = 0,
  WPD_STREAM_UNITS_FRAMES        = 1,
  WPD_STREAM_UNITS_ROWS          = 2,
  WPD_STREAM_UNITS_MILLISECONDS  = 3,
  WPD_STREAM_UNITS_MICROSECONDS  = 4
} WPD_STREAM_UNITS;
```



## <a name="constants"></a><span data-ttu-id="f7e59-106">Константы</span><span class="sxs-lookup"><span data-stu-id="f7e59-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="f7e59-107"><span id="WPD_STREAM_UNITS_BYTES"></span><span id="wpd_stream_units_bytes"></span>**\_число потоков потока WPD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f7e59-107"><span id="WPD_STREAM_UNITS_BYTES"></span><span id="wpd_stream_units_bytes"></span>**WPD\_STREAM\_UNITS\_BYTES**</span></span>
</dt> <dd>

<span data-ttu-id="f7e59-108">Единицы потоковой передачи указываются в байтах.</span><span class="sxs-lookup"><span data-stu-id="f7e59-108">The stream units are specified in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="f7e59-109"><span id="WPD_STREAM_UNITS_FRAMES"></span><span id="wpd_stream_units_frames"></span>**\_кадры потоковых \_ единиц WPD \_**</span><span class="sxs-lookup"><span data-stu-id="f7e59-109"><span id="WPD_STREAM_UNITS_FRAMES"></span><span id="wpd_stream_units_frames"></span>**WPD\_STREAM\_UNITS\_FRAMES**</span></span>
</dt> <dd>

<span data-ttu-id="f7e59-110">Единицы потоковой передачи указываются в кадрах.</span><span class="sxs-lookup"><span data-stu-id="f7e59-110">The stream units are specified in frames.</span></span>

</dd> <dt>

<span data-ttu-id="f7e59-111"><span id="WPD_STREAM_UNITS_ROWS"></span><span id="wpd_stream_units_rows"></span>**\_ \_ число строк в ПОТОКе WPD \_**</span><span class="sxs-lookup"><span data-stu-id="f7e59-111"><span id="WPD_STREAM_UNITS_ROWS"></span><span id="wpd_stream_units_rows"></span>**WPD\_STREAM\_UNITS\_ROWS**</span></span>
</dt> <dd>

<span data-ttu-id="f7e59-112">Единицы потоковой передачи указываются в строках.</span><span class="sxs-lookup"><span data-stu-id="f7e59-112">The stream units are specified in rows.</span></span>

</dd> <dt>

<span data-ttu-id="f7e59-113"><span id="WPD_STREAM_UNITS_MILLISECONDS"></span><span id="wpd_stream_units_milliseconds"></span>**\_число единиц потока WPD в \_ \_ миллисекундах**</span><span class="sxs-lookup"><span data-stu-id="f7e59-113"><span id="WPD_STREAM_UNITS_MILLISECONDS"></span><span id="wpd_stream_units_milliseconds"></span>**WPD\_STREAM\_UNITS\_MILLISECONDS**</span></span>
</dt> <dd>

<span data-ttu-id="f7e59-114">Единицы потоковой передачи указываются в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="f7e59-114">The stream units are specified in milliseconds.</span></span>

</dd> <dt>

<span data-ttu-id="f7e59-115"><span id="WPD_STREAM_UNITS_MICROSECONDS"></span><span id="wpd_stream_units_microseconds"></span>**\_МИКРОсекунды потоковых \_ модулей WPD \_**</span><span class="sxs-lookup"><span data-stu-id="f7e59-115"><span id="WPD_STREAM_UNITS_MICROSECONDS"></span><span id="wpd_stream_units_microseconds"></span>**WPD\_STREAM\_UNITS\_MICROSECONDS**</span></span>
</dt> <dd>

<span data-ttu-id="f7e59-116">Единицы потоковой передачи указываются в микросекундах.</span><span class="sxs-lookup"><span data-stu-id="f7e59-116">The stream units are specified in microseconds.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f7e59-117">Требования</span><span class="sxs-lookup"><span data-stu-id="f7e59-117">Requirements</span></span>



| <span data-ttu-id="f7e59-118">Требование</span><span class="sxs-lookup"><span data-stu-id="f7e59-118">Requirement</span></span> | <span data-ttu-id="f7e59-119">Значение</span><span class="sxs-lookup"><span data-stu-id="f7e59-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7e59-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f7e59-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f7e59-121">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="f7e59-121">Windows 8 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="f7e59-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f7e59-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f7e59-123">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f7e59-123">None supported</span></span><br/>                                                                        |
| <span data-ttu-id="f7e59-124">Header</span><span class="sxs-lookup"><span data-stu-id="f7e59-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7e59-125"><dt>Портабледевицетипес. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7e59-125"><dt>PortableDeviceTypes.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7e59-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f7e59-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7e59-127">**ипортабледевицеунитсстреам**</span><span class="sxs-lookup"><span data-stu-id="f7e59-127">**IPortableDeviceUnitsStream**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceunitsstream)
</dt> <dt>

[<span data-ttu-id="f7e59-128">**Ипортабледевицеунитсстреам:: Сикинунитс**</span><span class="sxs-lookup"><span data-stu-id="f7e59-128">**IPortableDeviceUnitsStream::SeekInUnits**</span></span>](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceunitsstream-seekinunits)
</dt> </dl>

 

 




