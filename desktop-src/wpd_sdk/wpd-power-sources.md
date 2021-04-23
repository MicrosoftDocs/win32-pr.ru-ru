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
# <a name="wpd_power_sources-enumeration"></a><span data-ttu-id="6c590-103">\_ \_ Перечисление источников питания WPD</span><span class="sxs-lookup"><span data-stu-id="6c590-103">WPD\_POWER\_SOURCES enumeration</span></span>

<span data-ttu-id="6c590-104">Тип перечисления **WPD \_ Power \_ Sources** описывает источник питания, который использует устройство.</span><span class="sxs-lookup"><span data-stu-id="6c590-104">The **WPD\_POWER\_SOURCES** enumeration type describes the power source that a device is using.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c590-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6c590-105">Syntax</span></span>


```C++
typedef enum WPD_POWER_SOURCES { 
  WPD_POWER_SOURCE_BATTERY   = 0,
  WPD_POWER_SOURCE_EXTERNAL  = 1
} ;
```



## <a name="constants"></a><span data-ttu-id="6c590-106">Константы</span><span class="sxs-lookup"><span data-stu-id="6c590-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="6c590-107"><span id="WPD_POWER_SOURCE_BATTERY"></span><span id="wpd_power_source_battery"></span>**\_питание источника питания (WPD) \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6c590-107"><span id="WPD_POWER_SOURCE_BATTERY"></span><span id="wpd_power_source_battery"></span>**WPD\_POWER\_SOURCE\_BATTERY**</span></span>
</dt> <dd>

<span data-ttu-id="6c590-108">Источник питания устройства — батарея.</span><span class="sxs-lookup"><span data-stu-id="6c590-108">The device power source is a battery.</span></span>

</dd> <dt>

<span data-ttu-id="6c590-109"><span id="WPD_POWER_SOURCE_EXTERNAL"></span><span id="wpd_power_source_external"></span>**\_ \_ внешний источник питания \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="6c590-109"><span id="WPD_POWER_SOURCE_EXTERNAL"></span><span id="wpd_power_source_external"></span>**WPD\_POWER\_SOURCE\_EXTERNAL**</span></span>
</dt> <dd>

<span data-ttu-id="6c590-110">Устройство использует внешний источник питания.</span><span class="sxs-lookup"><span data-stu-id="6c590-110">The device uses an external power source.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6c590-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6c590-111">Remarks</span></span>

<span data-ttu-id="6c590-112">Это перечисление используется свойством [ \_ \_ \_ источник питания устройства WPD](device-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="6c590-112">This enumeration is used by the [WPD\_DEVICE\_POWER\_SOURCE](device-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c590-113">Требования</span><span class="sxs-lookup"><span data-stu-id="6c590-113">Requirements</span></span>



| <span data-ttu-id="6c590-114">Требование</span><span class="sxs-lookup"><span data-stu-id="6c590-114">Requirement</span></span> | <span data-ttu-id="6c590-115">Значение</span><span class="sxs-lookup"><span data-stu-id="6c590-115">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c590-116">Header</span><span class="sxs-lookup"><span data-stu-id="6c590-116">Header</span></span><br/> | <dl> <span data-ttu-id="6c590-117"><dt>Портабледевице. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c590-117"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c590-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6c590-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c590-119">**Структуры и типы перечислений**</span><span class="sxs-lookup"><span data-stu-id="6c590-119">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




