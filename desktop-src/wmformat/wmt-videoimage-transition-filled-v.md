---
title: WMT_VIDEOIMAGE_TRANSITION_FILLED_V (Вмсдкидл. h)
description: При заполнении V новый рисунок отображается в треугольнике, который начинается с одной стороны рамки.
ms.assetid: d256178f-cb1d-4d36-9d30-e6dd6b3b23ec
keywords:
- WMT_VIDEOIMAGE_TRANSITION_FILLED_V формат Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_FILLED_V
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfe229657dfd29d3cb9d83a8a4853e2e89a7a6fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694568"
---
# <a name="wmt_videoimage_transition_filled_v"></a><span data-ttu-id="2cc32-104">ВМТ \_ видеоимаже \_ Переход \_ заполнен \_ V</span><span class="sxs-lookup"><span data-stu-id="2cc32-104">WMT\_VIDEOIMAGE\_TRANSITION\_FILLED\_V</span></span>

<span data-ttu-id="2cc32-105">При заполнении V новый рисунок отображается в треугольнике, который начинается с одной стороны рамки.</span><span class="sxs-lookup"><span data-stu-id="2cc32-105">The filled V transition reveals the new image in a triangle originating from one side of the frame.</span></span>

## <a name="parameters"></a><span data-ttu-id="2cc32-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2cc32-106">Parameters</span></span>

<span data-ttu-id="2cc32-107">В следующей таблице описаны параметры, используемые этим переходом, и перечислены члены структуры [**ВМТ \_ видеоимаже \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) , которой они назначены.</span><span class="sxs-lookup"><span data-stu-id="2cc32-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2cc32-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="2cc32-108">Parameter</span></span></th>
<th><span data-ttu-id="2cc32-109">Член структуры</span><span class="sxs-lookup"><span data-stu-id="2cc32-109">Structure member</span></span></th>
<th><span data-ttu-id="2cc32-110">Описание</span><span class="sxs-lookup"><span data-stu-id="2cc32-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2cc32-111">Ширина</span><span class="sxs-lookup"><span data-stu-id="2cc32-111">Width</span></span></td>
<td><span data-ttu-id="2cc32-112"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="2cc32-112"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="2cc32-113">Ширина заполненной V в пикселях.</span><span class="sxs-lookup"><span data-stu-id="2cc32-113">Width of the filled V in pixels.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2cc32-114">Высота</span><span class="sxs-lookup"><span data-stu-id="2cc32-114">Height</span></span></td>
<td><span data-ttu-id="2cc32-115"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="2cc32-115"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="2cc32-116">Высота заполненной V в пикселях.</span><span class="sxs-lookup"><span data-stu-id="2cc32-116">Height of the filled V in pixels.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2cc32-117">Направление</span><span class="sxs-lookup"><span data-stu-id="2cc32-117">Direction</span></span></td>
<td><span data-ttu-id="2cc32-118"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="2cc32-118"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="2cc32-119">Направление, с которого происходит заполнение V. Задайте одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="2cc32-119">Direction from which the filled V originates.Set to one of the following values:</span></span><br/>
<ul>
<li><span data-ttu-id="2cc32-120">0 — переход с левой стороны рамки.</span><span class="sxs-lookup"><span data-stu-id="2cc32-120">0 - Enters from the left side of the frame.</span></span></li>
<li><span data-ttu-id="2cc32-121">1 — переход с правой стороны рамки.</span><span class="sxs-lookup"><span data-stu-id="2cc32-121">1 - Enters from the right side of the frame.</span></span></li>
<li><span data-ttu-id="2cc32-122">2 — переходит от нижней части рамки.</span><span class="sxs-lookup"><span data-stu-id="2cc32-122">2 - Enters from the bottom of the frame.</span></span></li>
<li><span data-ttu-id="2cc32-123">3 — переходит от верхней части рамки.</span><span class="sxs-lookup"><span data-stu-id="2cc32-123">3 - Enters from the top of the frame.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2cc32-124">Композиция</span><span class="sxs-lookup"><span data-stu-id="2cc32-124">Composition</span></span></td>
<td><span data-ttu-id="2cc32-125"><strong>fEffectPara3</strong></span><span class="sxs-lookup"><span data-stu-id="2cc32-125"><strong>fEffectPara3</strong></span></span></td>
<td><span data-ttu-id="2cc32-126">Задайте одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="2cc32-126">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="2cc32-127">0 — задает нормальную композицию, в которой предыдущее изображение является фоном, а текущее изображение — передним планом.</span><span class="sxs-lookup"><span data-stu-id="2cc32-127">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="2cc32-128">1 — указывает обратную композицию, в которой текущий рисунок является фоновым изображением, а предыдущее изображение — передний план.</span><span class="sxs-lookup"><span data-stu-id="2cc32-128">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="2cc32-129">Требования</span><span class="sxs-lookup"><span data-stu-id="2cc32-129">Requirements</span></span>



| <span data-ttu-id="2cc32-130">Требование</span><span class="sxs-lookup"><span data-stu-id="2cc32-130">Requirement</span></span> | <span data-ttu-id="2cc32-131">Значение</span><span class="sxs-lookup"><span data-stu-id="2cc32-131">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2cc32-132">Header</span><span class="sxs-lookup"><span data-stu-id="2cc32-132">Header</span></span><br/> | <dl> <span data-ttu-id="2cc32-133"><dt>Вмсдкидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="2cc32-133"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2cc32-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2cc32-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cc32-135">**Переходы по изображениям видео**</span><span class="sxs-lookup"><span data-stu-id="2cc32-135">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





