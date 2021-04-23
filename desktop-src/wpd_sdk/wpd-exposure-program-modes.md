---
description: '\_Тип ПЕРЕЧИСЛЕНИЯ WPD экспозиции \_ \_ mode описывает режим экспозиции, используемый при записи образов с помощью устройства.'
ms.assetid: 68b76294-6ad3-4f4a-bf02-bc31c9e8ac62
title: Перечисление WPD_EXPOSURE_PROGRAM_MODES (Портабледевице. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_EXPOSURE_PROGRAM_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: a88ce90bb9e776cd45245b32a363635c2ccf0560
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675699"
---
# <a name="wpd_exposure_program_modes-enumeration"></a><span data-ttu-id="5e08c-103">\_ \_ Перечисление режимов программы "ЭКСПОЗИЦИя WPD" \_</span><span class="sxs-lookup"><span data-stu-id="5e08c-103">WPD\_EXPOSURE\_PROGRAM\_MODES enumeration</span></span>

<span data-ttu-id="5e08c-104">Тип перечисления **WPD \_ экспозиции \_ \_** Mode описывает режим экспозиции, используемый при записи образов с помощью устройства.</span><span class="sxs-lookup"><span data-stu-id="5e08c-104">The **WPD\_EXPOSURE\_PROGRAM\_MODES** enumeration type describes an exposure mode to use when capturing images with a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e08c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5e08c-105">Syntax</span></span>


```C++
typedef enum WPD_EXPOSURE_PROGRAM_MODES { 
  WPD_EXPOSURE_PROGRAM_MODE_UNDEFINED          = 0,
  WPD_EXPOSURE_PROGRAM_MODE_MANUAL             = 1,
  WPD_EXPOSURE_PROGRAM_MODE_AUTO               = 2,
  WPD_EXPOSURE_PROGRAM_MODE_APERTURE_PRIORITY  = 3,
  WPD_EXPOSURE_PROGRAM_MODE_SHUTTER_PRIORITY   = 4,
  WPD_EXPOSURE_PROGRAM_MODE_CREATIVE           = 5,
  WPD_EXPOSURE_PROGRAM_MODE_ACTION             = 6,
  WPD_EXPOSURE_PROGRAM_MODE_PORTRAIT           = 7
} ;
```



## <a name="constants"></a><span data-ttu-id="5e08c-106">Константы</span><span class="sxs-lookup"><span data-stu-id="5e08c-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="5e08c-107"><span id="WPD_EXPOSURE_PROGRAM_MODE_UNDEFINED"></span><span id="wpd_exposure_program_mode_undefined"></span>**\_режим программы экспозиции WPD не \_ \_ \_ определен**</span><span class="sxs-lookup"><span data-stu-id="5e08c-107"><span id="WPD_EXPOSURE_PROGRAM_MODE_UNDEFINED"></span><span id="wpd_exposure_program_mode_undefined"></span>**WPD\_EXPOSURE\_PROGRAM\_MODE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="5e08c-108">Не указан режим экспозиции.</span><span class="sxs-lookup"><span data-stu-id="5e08c-108">The exposure mode has not been specified.</span></span>

</dd> <dt>

<span data-ttu-id="5e08c-109"><span id="WPD_EXPOSURE_PROGRAM_MODE_MANUAL"></span><span id="wpd_exposure_program_mode_manual"></span>**\_руководство по \_ \_ режиму \_ программы для WPD**</span><span class="sxs-lookup"><span data-stu-id="5e08c-109"><span id="WPD_EXPOSURE_PROGRAM_MODE_MANUAL"></span><span id="wpd_exposure_program_mode_manual"></span>**WPD\_EXPOSURE\_PROGRAM\_MODE\_MANUAL**</span></span>
</dt> <dd>

<span data-ttu-id="5e08c-110">Приложение должно указать все параметры экспозиции.</span><span class="sxs-lookup"><span data-stu-id="5e08c-110">The application should specify all exposure settings.</span></span>

</dd> <dt>

<span data-ttu-id="5e08c-111"><span id="WPD_EXPOSURE_PROGRAM_MODE_AUTO"></span><span id="wpd_exposure_program_mode_auto"></span>**\_ \_ режим автоматической экспозиции программы WPD \_ \_ Auto**</span><span class="sxs-lookup"><span data-stu-id="5e08c-111"><span id="WPD_EXPOSURE_PROGRAM_MODE_AUTO"></span><span id="wpd_exposure_program_mode_auto"></span>**WPD\_EXPOSURE\_PROGRAM\_MODE\_AUTO**</span></span>
</dt> <dd>

<span data-ttu-id="5e08c-112">Использовать режим автоматической экспозиции, определяемый устройством.</span><span class="sxs-lookup"><span data-stu-id="5e08c-112">Use a device-defined automatic exposure mode.</span></span>

</dd> <dt>

<span data-ttu-id="5e08c-113"><span id="WPD_EXPOSURE_PROGRAM_MODE_APERTURE_PRIORITY"></span><span id="wpd_exposure_program_mode_aperture_priority"></span>**\_ \_ \_ \_ приоритет режима АПЕРТУРы для \_ программы WPD**</span><span class="sxs-lookup"><span data-stu-id="5e08c-113"><span id="WPD_EXPOSURE_PROGRAM_MODE_APERTURE_PRIORITY"></span><span id="wpd_exposure_program_mode_aperture_priority"></span>**WPD\_EXPOSURE\_PROGRAM\_MODE\_APERTURE\_PRIORITY**</span></span>
</dt> <dd>

<span data-ttu-id="5e08c-114">Автоматический режим экспозиции, указывающий, что значение апертуры линзы должно оставаться фиксированным, но скорость затвора должна быть определена устройством.</span><span class="sxs-lookup"><span data-stu-id="5e08c-114">An automated exposure mode that indicates that the lens aperture value should remain fixed, but shutter speed should be determined by the device.</span></span>

</dd> <dt>

<span data-ttu-id="5e08c-115"><span id="WPD_EXPOSURE_PROGRAM_MODE_SHUTTER_PRIORITY"></span><span id="wpd_exposure_program_mode_shutter_priority"></span>**\_ \_ \_ \_ приоритет выдержкы в режиме \_ программы**</span><span class="sxs-lookup"><span data-stu-id="5e08c-115"><span id="WPD_EXPOSURE_PROGRAM_MODE_SHUTTER_PRIORITY"></span><span id="wpd_exposure_program_mode_shutter_priority"></span>**WPD\_EXPOSURE\_PROGRAM\_MODE\_SHUTTER\_PRIORITY**</span></span>
</dt> <dd>

<span data-ttu-id="5e08c-116">Автоматический режим экспозиции, который указывает, что скорость затвора должна оставаться фиксированной, но этот Апертура должен быть определен устройством.</span><span class="sxs-lookup"><span data-stu-id="5e08c-116">An automated exposure mode that indicates that the shutter speed should remain fixed, but that lens aperture should be determined by the device.</span></span>

</dd> <dt>

<span data-ttu-id="5e08c-117"><span id="WPD_EXPOSURE_PROGRAM_MODE_CREATIVE"></span><span id="wpd_exposure_program_mode_creative"></span>**\_ \_ \_ творческий режим программы, подверженной атаке WPD \_**</span><span class="sxs-lookup"><span data-stu-id="5e08c-117"><span id="WPD_EXPOSURE_PROGRAM_MODE_CREATIVE"></span><span id="wpd_exposure_program_mode_creative"></span>**WPD\_EXPOSURE\_PROGRAM\_MODE\_CREATIVE**</span></span>
</dt> <dd>

<span data-ttu-id="5e08c-118">Автоматический режим экспозиции, который пытается максимально увеличить глубину поля.</span><span class="sxs-lookup"><span data-stu-id="5e08c-118">An automated exposure mode that tries to maximize the depth of field.</span></span>

</dd> <dt>

<span data-ttu-id="5e08c-119"><span id="WPD_EXPOSURE_PROGRAM_MODE_ACTION"></span><span id="wpd_exposure_program_mode_action"></span>**\_ \_ \_ действие режима программы экспозиции WPD \_**</span><span class="sxs-lookup"><span data-stu-id="5e08c-119"><span id="WPD_EXPOSURE_PROGRAM_MODE_ACTION"></span><span id="wpd_exposure_program_mode_action"></span>**WPD\_EXPOSURE\_PROGRAM\_MODE\_ACTION**</span></span>
</dt> <dd>

<span data-ttu-id="5e08c-120">Автоматический режим экспозиции, который пытается максимально увеличить скорость затвора.</span><span class="sxs-lookup"><span data-stu-id="5e08c-120">An automated exposure mode that tries to maximize the shutter speed.</span></span>

</dd> <dt>

<span data-ttu-id="5e08c-121"><span id="WPD_EXPOSURE_PROGRAM_MODE_PORTRAIT"></span><span id="wpd_exposure_program_mode_portrait"></span>**режим программы "экспозиция" (WPD) \_ \_ \_ \_ Книжная**</span><span class="sxs-lookup"><span data-stu-id="5e08c-121"><span id="WPD_EXPOSURE_PROGRAM_MODE_PORTRAIT"></span><span id="wpd_exposure_program_mode_portrait"></span>**WPD\_EXPOSURE\_PROGRAM\_MODE\_PORTRAIT**</span></span>
</dt> <dd>

<span data-ttu-id="5e08c-122">Автоматический режим экспозиции, указывающий относительно полную глубину поля.</span><span class="sxs-lookup"><span data-stu-id="5e08c-122">An automated exposure mode that specifies a relatively shallow depth of field.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5e08c-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5e08c-123">Remarks</span></span>

<span data-ttu-id="5e08c-124">Указывает режим программы экспозиции устройства.</span><span class="sxs-lookup"><span data-stu-id="5e08c-124">Indicates the exposure program mode of the device.</span></span> <span data-ttu-id="5e08c-125">Это перечисление используется в свойстве " [ \_ режим программы" в \_ \_ \_ \_ режиме уязвимости с образом WPD](still-image-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="5e08c-125">This enumeration is used by the [WPD\_STILL\_IMAGE\_EXPOSURE\_PROGRAM\_MODE](still-image-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e08c-126">Требования</span><span class="sxs-lookup"><span data-stu-id="5e08c-126">Requirements</span></span>



| <span data-ttu-id="5e08c-127">Требование</span><span class="sxs-lookup"><span data-stu-id="5e08c-127">Requirement</span></span> | <span data-ttu-id="5e08c-128">Значение</span><span class="sxs-lookup"><span data-stu-id="5e08c-128">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e08c-129">Header</span><span class="sxs-lookup"><span data-stu-id="5e08c-129">Header</span></span><br/> | <dl> <span data-ttu-id="5e08c-130"><dt>Портабледевице. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e08c-130"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e08c-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5e08c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e08c-132">**Структуры и типы перечислений**</span><span class="sxs-lookup"><span data-stu-id="5e08c-132">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




