---
description: '\_Тип перечисления «режимы записи WPD» \_ описывает режим сбора данных о времени записи образа.'
ms.assetid: bfe96176-d018-4b39-a938-035757111784
title: Перечисление WPD_CAPTURE_MODES (Портабледевице. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_CAPTURE_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: e56e3e66cd20abaeb1daf0a674633a36b57a9575
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717857"
---
# <a name="wpd_capture_modes-enumeration"></a><span data-ttu-id="fd0b3-103">\_ \_ Перечисление режимов захвата WPD</span><span class="sxs-lookup"><span data-stu-id="fd0b3-103">WPD\_CAPTURE\_MODES enumeration</span></span>

<span data-ttu-id="fd0b3-104">Тип перечисления « **\_ \_ режимы записи WPD** » описывает режим сбора данных о времени записи образа.</span><span class="sxs-lookup"><span data-stu-id="fd0b3-104">The **WPD\_CAPTURE\_MODES** enumeration type describes the capture timing mode of a still image capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd0b3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fd0b3-105">Syntax</span></span>


```C++
typedef enum WPD_CAPTURE_MODES { 
  WPD_CAPTURE_MODE_UNDEFINED  = 0,
  WPD_CAPTURE_MODE_NORMAL     = 1,
  WPD_CAPTURE_MODE_BURST      = 2,
  WPD_CAPTURE_MODE_TIMELAPSE  = 3
} ;
```



## <a name="constants"></a><span data-ttu-id="fd0b3-106">Константы</span><span class="sxs-lookup"><span data-stu-id="fd0b3-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="fd0b3-107"><span id="WPD_CAPTURE_MODE_UNDEFINED"></span><span id="wpd_capture_mode_undefined"></span>**\_режим записи WPD не \_ \_ определен**</span><span class="sxs-lookup"><span data-stu-id="fd0b3-107"><span id="WPD_CAPTURE_MODE_UNDEFINED"></span><span id="wpd_capture_mode_undefined"></span>**WPD\_CAPTURE\_MODE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="fd0b3-108">Режим записи не определен.</span><span class="sxs-lookup"><span data-stu-id="fd0b3-108">The capture mode has not been defined.</span></span>

</dd> <dt>

<span data-ttu-id="fd0b3-109"><span id="WPD_CAPTURE_MODE_NORMAL"></span><span id="wpd_capture_mode_normal"></span>**\_режим записи WPD " \_ \_ нормальный"**</span><span class="sxs-lookup"><span data-stu-id="fd0b3-109"><span id="WPD_CAPTURE_MODE_NORMAL"></span><span id="wpd_capture_mode_normal"></span>**WPD\_CAPTURE\_MODE\_NORMAL**</span></span>
</dt> <dd>

<span data-ttu-id="fd0b3-110">Не следует использовать задержки или пакетный режим.</span><span class="sxs-lookup"><span data-stu-id="fd0b3-110">No delay or burst mode should be used.</span></span>

</dd> <dt>

<span data-ttu-id="fd0b3-111"><span id="WPD_CAPTURE_MODE_BURST"></span><span id="wpd_capture_mode_burst"></span>**\_ \_ ускоренный режим записи WPD \_**</span><span class="sxs-lookup"><span data-stu-id="fd0b3-111"><span id="WPD_CAPTURE_MODE_BURST"></span><span id="wpd_capture_mode_burst"></span>**WPD\_CAPTURE\_MODE\_BURST**</span></span>
</dt> <dd>

<span data-ttu-id="fd0b3-112">Указывает, что определенное количество образов должно быть захвачено с определенным интервалом между ними.</span><span class="sxs-lookup"><span data-stu-id="fd0b3-112">Specifies that a defined number of images should be captured with a defined interval between them.</span></span> <span data-ttu-id="fd0b3-113">Количество образов для захвата и временной задержки между ними задается с помощью [ \_ \_ \_ \_ счетчика "число неподвижных](still-image-properties.md) [образов \_ " \_ \_ \_ ](still-image-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="fd0b3-113">The number of images to capture and time delay between them are specified by the [WPD\_STILL\_IMAGE\_BURST\_NUMBER](still-image-properties.md) and [WPD\_STILL\_IMAGE\_BURST\_INTERVAL](still-image-properties.md) properties.</span></span>

</dd> <dt>

<span data-ttu-id="fd0b3-114"><span id="WPD_CAPTURE_MODE_TIMELAPSE"></span><span id="wpd_capture_mode_timelapse"></span>**\_ \_ тимелапсе режим записи \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="fd0b3-114"><span id="WPD_CAPTURE_MODE_TIMELAPSE"></span><span id="wpd_capture_mode_timelapse"></span>**WPD\_CAPTURE\_MODE\_TIMELAPSE**</span></span>
</dt> <dd>

<span data-ttu-id="fd0b3-115">Для записи образов следует использовать фотографию времени.</span><span class="sxs-lookup"><span data-stu-id="fd0b3-115">Image capture should use time lapse photography.</span></span> <span data-ttu-id="fd0b3-116">Число образов и интервал между ними описывается в разделе [ \_ \_ \_ тимелапсе \_ Number](still-image-properties.md) и [WPD, \_ все равно Image \_ \_ тимелапсе \_ Interval](still-image-properties.md) Properties.</span><span class="sxs-lookup"><span data-stu-id="fd0b3-116">The number of images and interval between them are described by the [WPD\_STILL\_IMAGE\_TIMELAPSE\_NUMBER](still-image-properties.md) and [WPD\_STILL\_IMAGE\_TIMELAPSE\_INTERVAL](still-image-properties.md) properties.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fd0b3-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fd0b3-117">Remarks</span></span>

<span data-ttu-id="fd0b3-118">Это перечисление используется в свойстве " [ \_ \_ \_ \_ режим захвата WPD-образа](still-image-properties.md) ".</span><span class="sxs-lookup"><span data-stu-id="fd0b3-118">This enumeration is used by the [WPD\_STILL\_IMAGE\_CAPTURE\_MODE](still-image-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd0b3-119">Требования</span><span class="sxs-lookup"><span data-stu-id="fd0b3-119">Requirements</span></span>



| <span data-ttu-id="fd0b3-120">Требование</span><span class="sxs-lookup"><span data-stu-id="fd0b3-120">Requirement</span></span> | <span data-ttu-id="fd0b3-121">Значение</span><span class="sxs-lookup"><span data-stu-id="fd0b3-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd0b3-122">Header</span><span class="sxs-lookup"><span data-stu-id="fd0b3-122">Header</span></span><br/> | <dl> <span data-ttu-id="fd0b3-123"><dt>Портабледевице. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd0b3-123"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd0b3-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fd0b3-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd0b3-125">**Свойства и атрибуты WPD**</span><span class="sxs-lookup"><span data-stu-id="fd0b3-125">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> <dt>

[<span data-ttu-id="fd0b3-126">**Структуры и типы перечислений**</span><span class="sxs-lookup"><span data-stu-id="fd0b3-126">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




