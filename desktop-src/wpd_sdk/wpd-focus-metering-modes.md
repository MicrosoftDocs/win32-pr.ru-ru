---
description: '\_Тип перечисления «режимы отслеживания фокуса» для WPD \_ описывает, \_ как устройство должно решить, какую часть кадра использовать для установки фокуса.'
ms.assetid: 0e68d0e8-2ce3-4994-99c2-2ff2293d8a20
title: Перечисление WPD_FOCUS_METERING_MODES (Портабледевице. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_FOCUS_METERING_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: f59d6a2f1cabbbe7b072a87caa3e5d74d012fc49
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668682"
---
# <a name="wpd_focus_metering_modes-enumeration"></a><span data-ttu-id="0b060-103">\_ \_ Перечисление режимов метрик ФОКУСа WPD \_</span><span class="sxs-lookup"><span data-stu-id="0b060-103">WPD\_FOCUS\_METERING\_MODES enumeration</span></span>

<span data-ttu-id="0b060-104">Тип перечисления « **\_ \_ \_ режимы отслеживания фокуса** » для WPD описывает, как устройство должно решить, какую часть кадра использовать для установки фокуса.</span><span class="sxs-lookup"><span data-stu-id="0b060-104">The **WPD\_FOCUS\_METERING\_MODES** enumeration type describes how a device should decide what part of a frame to use to set focus.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b060-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0b060-105">Syntax</span></span>


```C++
typedef enum WPD_FOCUS_METERING_MODES { 
  WPD_FOCUS_METERING_MODE_UNDEFINED    = 0,
  WPD_FOCUS_METERING_MODE_CENTER_SPOT  = 1,
  WPD_FOCUS_METERING_MODE_MULTI_SPOT   = 2
} ;
```



## <a name="constants"></a><span data-ttu-id="0b060-106">Константы</span><span class="sxs-lookup"><span data-stu-id="0b060-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="0b060-107"><span id="WPD_FOCUS_METERING_MODE_UNDEFINED"></span><span id="wpd_focus_metering_mode_undefined"></span>**\_режим метрик фокуса WPD не \_ \_ \_ определен**</span><span class="sxs-lookup"><span data-stu-id="0b060-107"><span id="WPD_FOCUS_METERING_MODE_UNDEFINED"></span><span id="wpd_focus_metering_mode_undefined"></span>**WPD\_FOCUS\_METERING\_MODE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="0b060-108">Указывает, что режим фокусировки не указан.</span><span class="sxs-lookup"><span data-stu-id="0b060-108">Indicates that no focusing mode has been specified.</span></span>

</dd> <dt>

<span data-ttu-id="0b060-109"><span id="WPD_FOCUS_METERING_MODE_CENTER_SPOT"></span><span id="wpd_focus_metering_mode_center_spot"></span>**\_ \_ \_ \_ центр отслеживания фокусирований для WPD \_**</span><span class="sxs-lookup"><span data-stu-id="0b060-109"><span id="WPD_FOCUS_METERING_MODE_CENTER_SPOT"></span><span id="wpd_focus_metering_mode_center_spot"></span>**WPD\_FOCUS\_METERING\_MODE\_CENTER\_SPOT**</span></span>
</dt> <dd>

<span data-ttu-id="0b060-110">Фокусируется на центре области с рамками.</span><span class="sxs-lookup"><span data-stu-id="0b060-110">Focuses on the center of the framed area.</span></span>

</dd> <dt>

<span data-ttu-id="0b060-111"><span id="WPD_FOCUS_METERING_MODE_MULTI_SPOT"></span><span id="wpd_focus_metering_mode_multi_spot"></span>**\_ \_ \_ \_ множественная разкраска в режиме метрик фокуса WPD \_**</span><span class="sxs-lookup"><span data-stu-id="0b060-111"><span id="WPD_FOCUS_METERING_MODE_MULTI_SPOT"></span><span id="wpd_focus_metering_mode_multi_spot"></span>**WPD\_FOCUS\_METERING\_MODE\_MULTI\_SPOT**</span></span>
</dt> <dd>

<span data-ttu-id="0b060-112">Определение фокуса путем анализа нескольких частей области в рамке.</span><span class="sxs-lookup"><span data-stu-id="0b060-112">Determine focus by analyzing multiple parts of the framed area.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0b060-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0b060-113">Remarks</span></span>

<span data-ttu-id="0b060-114">Это перечисление задается свойством " [ \_ \_ \_ \_ \_ режим отслеживания фокуса" для неподвижных изображений WPD](still-image-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="0b060-114">This enumeration is specified by the [WPD\_STILL\_IMAGE\_FOCUS\_METERING\_MODE](still-image-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b060-115">Требования</span><span class="sxs-lookup"><span data-stu-id="0b060-115">Requirements</span></span>



| <span data-ttu-id="0b060-116">Требование</span><span class="sxs-lookup"><span data-stu-id="0b060-116">Requirement</span></span> | <span data-ttu-id="0b060-117">Значение</span><span class="sxs-lookup"><span data-stu-id="0b060-117">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b060-118">Header</span><span class="sxs-lookup"><span data-stu-id="0b060-118">Header</span></span><br/> | <dl> <span data-ttu-id="0b060-119"><dt>Портабледевице. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b060-119"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b060-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0b060-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b060-121">**Структуры и типы перечислений**</span><span class="sxs-lookup"><span data-stu-id="0b060-121">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




