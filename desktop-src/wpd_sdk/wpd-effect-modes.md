---
description: '\_Тип перечисления «режимы влияния WPD» \_ описывает различные визуальные эффекты, которые могут быть применены к изображению.'
ms.assetid: 7624fccb-e416-4db4-978e-410c4c236328
title: Перечисление WPD_EFFECT_MODES (Портабледевице. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_EFFECT_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 7e29f89207a74d335fbe1c2561f8dcf9cec3e923
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694431"
---
# <a name="wpd_effect_modes-enumeration"></a><span data-ttu-id="61294-103">\_ \_ Перечисление режимов влияния WPD</span><span class="sxs-lookup"><span data-stu-id="61294-103">WPD\_EFFECT\_MODES enumeration</span></span>

<span data-ttu-id="61294-104">Тип перечисления « **\_ \_ режимы влияния WPD** » описывает различные визуальные эффекты, которые могут быть применены к изображению.</span><span class="sxs-lookup"><span data-stu-id="61294-104">The **WPD\_EFFECT\_MODES** enumeration type describes various visual effects that can be applied to an image.</span></span>

## <a name="syntax"></a><span data-ttu-id="61294-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="61294-105">Syntax</span></span>


```C++
typedef enum WPD_EFFECT_MODES { 
  WPD_EFFECT_MODE_UNDEFINED        = 0,
  WPD_EFFECT_MODE_COLOR            = 1,
  WPD_EFFECT_MODE_BLACK_AND_WHITE  = 2,
  WPD_EFFECT_MODE_SEPIA            = 3
} ;
```



## <a name="constants"></a><span data-ttu-id="61294-106">Константы</span><span class="sxs-lookup"><span data-stu-id="61294-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="61294-107"><span id="WPD_EFFECT_MODE_UNDEFINED"></span><span id="wpd_effect_mode_undefined"></span>**\_режим влияния WPD не \_ \_ определен**</span><span class="sxs-lookup"><span data-stu-id="61294-107"><span id="WPD_EFFECT_MODE_UNDEFINED"></span><span id="wpd_effect_mode_undefined"></span>**WPD\_EFFECT\_MODE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="61294-108">Не указан ни один результат.</span><span class="sxs-lookup"><span data-stu-id="61294-108">No effect has been specified.</span></span>

</dd> <dt>

<span data-ttu-id="61294-109"><span id="WPD_EFFECT_MODE_COLOR"></span><span id="wpd_effect_mode_color"></span>**\_ \_ Цвет режима влияния \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="61294-109"><span id="WPD_EFFECT_MODE_COLOR"></span><span id="wpd_effect_mode_color"></span>**WPD\_EFFECT\_MODE\_COLOR**</span></span>
</dt> <dd>

<span data-ttu-id="61294-110">Изображение должно иметь цвет.</span><span class="sxs-lookup"><span data-stu-id="61294-110">The image should be color.</span></span>

</dd> <dt>

<span data-ttu-id="61294-111"><span id="WPD_EFFECT_MODE_BLACK_AND_WHITE"></span><span id="wpd_effect_mode_black_and_white"></span>**\_режим влияния WPD — \_ \_ черный \_ и \_ белый**</span><span class="sxs-lookup"><span data-stu-id="61294-111"><span id="WPD_EFFECT_MODE_BLACK_AND_WHITE"></span><span id="wpd_effect_mode_black_and_white"></span>**WPD\_EFFECT\_MODE\_BLACK\_AND\_WHITE**</span></span>
</dt> <dd>

<span data-ttu-id="61294-112">Изображение должно быть черно-белым.</span><span class="sxs-lookup"><span data-stu-id="61294-112">The image should be black and white.</span></span>

</dd> <dt>

<span data-ttu-id="61294-113"><span id="WPD_EFFECT_MODE_SEPIA"></span><span id="wpd_effect_mode_sepia"></span>**\_режим влияния \_ WPD \_ выцветшей**</span><span class="sxs-lookup"><span data-stu-id="61294-113"><span id="WPD_EFFECT_MODE_SEPIA"></span><span id="wpd_effect_mode_sepia"></span>**WPD\_EFFECT\_MODE\_SEPIA**</span></span>
</dt> <dd>

<span data-ttu-id="61294-114">Образ должен быть выцветшей.</span><span class="sxs-lookup"><span data-stu-id="61294-114">The image should be sepia.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="61294-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="61294-115">Remarks</span></span>

<span data-ttu-id="61294-116">Это перечисление используется в свойстве [ \_ \_ \_ \_ режима эффектов для изображения WPD](still-image-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="61294-116">This enumeration is used by the [WPD\_STILL\_IMAGE\_EFFECT\_MODE](still-image-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="61294-117">Требования</span><span class="sxs-lookup"><span data-stu-id="61294-117">Requirements</span></span>



| <span data-ttu-id="61294-118">Требование</span><span class="sxs-lookup"><span data-stu-id="61294-118">Requirement</span></span> | <span data-ttu-id="61294-119">Значение</span><span class="sxs-lookup"><span data-stu-id="61294-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="61294-120">Header</span><span class="sxs-lookup"><span data-stu-id="61294-120">Header</span></span><br/> | <dl> <span data-ttu-id="61294-121"><dt>Портабледевице. h</dt></span><span class="sxs-lookup"><span data-stu-id="61294-121"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61294-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="61294-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61294-123">**Структуры и типы перечислений**</span><span class="sxs-lookup"><span data-stu-id="61294-123">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




