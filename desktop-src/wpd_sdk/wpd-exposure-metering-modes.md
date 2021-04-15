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
ms.openlocfilehash: 76c2594339c6fa4997e4d646fc89e8c30dcdf8fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675701"
---
# <a name="wpd_exposure_metering_modes-enumeration"></a><span data-ttu-id="2e22f-103">\_ \_ Перечисление режимов измерения экспозиции для WPD \_</span><span class="sxs-lookup"><span data-stu-id="2e22f-103">WPD\_EXPOSURE\_METERING\_MODES enumeration</span></span>

<span data-ttu-id="2e22f-104">Тип перечисления " **\_ \_ счетчики \_ раскрытия" WPD** описывает режим измерения, который будет использоваться при оценке экспозиции для записи образа на устройстве.</span><span class="sxs-lookup"><span data-stu-id="2e22f-104">The **WPD\_EXPOSURE\_METERING\_MODES** enumeration type describes the metering mode to use when estimating exposure for still image capture by a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e22f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2e22f-105">Syntax</span></span>


```C++
typedef enum WPD_EXPOSURE_METERING_MODES { 
  WPD_EXPOSURE_METERING_MODE_UNDEFINED                = 0,
  WPD_EXPOSURE_METERING_MODE_AVERAGE                  = 1,
  WPD_EXPOSURE_METERING_MODE_CENTER_WEIGHTED_AVERAGE  = 2,
  WPD_EXPOSURE_METERING_MODE_MULTI_SPOT               = 3,
  WPD_EXPOSURE_METERING_MODE_CENTER_SPOT              = 4
} ;
```



## <a name="constants"></a><span data-ttu-id="2e22f-106">Константы</span><span class="sxs-lookup"><span data-stu-id="2e22f-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="2e22f-107"><span id="WPD_EXPOSURE_METERING_MODE_UNDEFINED"></span><span id="wpd_exposure_metering_mode_undefined"></span>**\_неопределенный \_ режим отслеживания \_ \_ вероятности WPD**</span><span class="sxs-lookup"><span data-stu-id="2e22f-107"><span id="WPD_EXPOSURE_METERING_MODE_UNDEFINED"></span><span id="wpd_exposure_metering_mode_undefined"></span>**WPD\_EXPOSURE\_METERING\_MODE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="2e22f-108">Режим измерения не определен.</span><span class="sxs-lookup"><span data-stu-id="2e22f-108">The metering mode is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="2e22f-109"><span id="WPD_EXPOSURE_METERING_MODE_AVERAGE"></span><span id="wpd_exposure_metering_mode_average"></span>**\_ \_ \_ среднее значение режима метрик ВЫдержки от WPD \_**</span><span class="sxs-lookup"><span data-stu-id="2e22f-109"><span id="WPD_EXPOSURE_METERING_MODE_AVERAGE"></span><span id="wpd_exposure_metering_mode_average"></span>**WPD\_EXPOSURE\_METERING\_MODE\_AVERAGE**</span></span>
</dt> <dd>

<span data-ttu-id="2e22f-110">Использовать среднее значение раскрытия в полном образе.</span><span class="sxs-lookup"><span data-stu-id="2e22f-110">Use averaged exposure across the full image.</span></span>

</dd> <dt>

<span data-ttu-id="2e22f-111"><span id="WPD_EXPOSURE_METERING_MODE_CENTER_WEIGHTED_AVERAGE"></span><span id="wpd_exposure_metering_mode_center_weighted_average"></span>**\_ \_ \_ \_ \_ средневзвешенное значение в центре режима измерения экспозиции \_**</span><span class="sxs-lookup"><span data-stu-id="2e22f-111"><span id="WPD_EXPOSURE_METERING_MODE_CENTER_WEIGHTED_AVERAGE"></span><span id="wpd_exposure_metering_mode_center_weighted_average"></span>**WPD\_EXPOSURE\_METERING\_MODE\_CENTER\_WEIGHTED\_AVERAGE**</span></span>
</dt> <dd>

<span data-ttu-id="2e22f-112">Используйте среднюю раскрытие, когда центр изображения заданный дополнительный вес.</span><span class="sxs-lookup"><span data-stu-id="2e22f-112">Use an averaged exposure, with the center of the image given more weight.</span></span>

</dd> <dt>

<span data-ttu-id="2e22f-113"><span id="WPD_EXPOSURE_METERING_MODE_MULTI_SPOT"></span><span id="wpd_exposure_metering_mode_multi_spot"></span>**\_ \_ \_ \_ множественная разкраска в режиме метрик экспозиции WPD \_**</span><span class="sxs-lookup"><span data-stu-id="2e22f-113"><span id="WPD_EXPOSURE_METERING_MODE_MULTI_SPOT"></span><span id="wpd_exposure_metering_mode_multi_spot"></span>**WPD\_EXPOSURE\_METERING\_MODE\_MULTI\_SPOT**</span></span>
</dt> <dd>

<span data-ttu-id="2e22f-114">Используйте многоуровневый метод усреднения.</span><span class="sxs-lookup"><span data-stu-id="2e22f-114">Use a multi-spot averaging technique.</span></span>

</dd> <dt>

<span data-ttu-id="2e22f-115"><span id="WPD_EXPOSURE_METERING_MODE_CENTER_SPOT"></span><span id="wpd_exposure_metering_mode_center_spot"></span>**\_ \_ геометрическое \_ \_ место центра режима \_ отслеживания вероятности WPD**</span><span class="sxs-lookup"><span data-stu-id="2e22f-115"><span id="WPD_EXPOSURE_METERING_MODE_CENTER_SPOT"></span><span id="wpd_exposure_metering_mode_center_spot"></span>**WPD\_EXPOSURE\_METERING\_MODE\_CENTER\_SPOT**</span></span>
</dt> <dd>

<span data-ttu-id="2e22f-116">Используйте метод усреднения по центру.</span><span class="sxs-lookup"><span data-stu-id="2e22f-116">Use a center-spot averaging technique.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2e22f-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2e22f-117">Remarks</span></span>

<span data-ttu-id="2e22f-118">Указывает режим измерения для устройства.</span><span class="sxs-lookup"><span data-stu-id="2e22f-118">Indicates the metering mode of the device.</span></span> <span data-ttu-id="2e22f-119">Это перечисление используется свойством "режим оценки вероятности" для [ \_ неподвижных \_ изображений \_ \_ \_ WPD](still-image-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="2e22f-119">This enumeration is used by the [WPD\_STILL\_IMAGE\_EXPOSURE\_METERING\_MODE](still-image-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e22f-120">Требования</span><span class="sxs-lookup"><span data-stu-id="2e22f-120">Requirements</span></span>



| <span data-ttu-id="2e22f-121">Требование</span><span class="sxs-lookup"><span data-stu-id="2e22f-121">Requirement</span></span> | <span data-ttu-id="2e22f-122">Значение</span><span class="sxs-lookup"><span data-stu-id="2e22f-122">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e22f-123">Header</span><span class="sxs-lookup"><span data-stu-id="2e22f-123">Header</span></span><br/> | <dl> <span data-ttu-id="2e22f-124"><dt>Портабледевице. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e22f-124"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e22f-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2e22f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e22f-126">**Структуры и типы перечислений**</span><span class="sxs-lookup"><span data-stu-id="2e22f-126">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




