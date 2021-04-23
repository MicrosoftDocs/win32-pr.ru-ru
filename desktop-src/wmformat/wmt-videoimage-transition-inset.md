---
title: WMT_VIDEOIMAGE_TRANSITION_INSET (Вмсдкидл. h)
description: Переход вставки показывает новый рисунок в прямоугольнике, который начинается с одного угла рамки.
ms.assetid: fd8bc4b7-0546-4897-ab7b-a320bbd126ef
keywords:
- WMT_VIDEOIMAGE_TRANSITION_INSET формат Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_INSET
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddd41887fafaae2756e2dafe3d57d4f1a86edf46
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648125"
---
# <a name="wmt_videoimage_transition_inset"></a><span data-ttu-id="a08f4-104">ВМТ \_ видеоимаже \_ перехода \_</span><span class="sxs-lookup"><span data-stu-id="a08f4-104">WMT\_VIDEOIMAGE\_TRANSITION\_INSET</span></span>

<span data-ttu-id="a08f4-105">Переход вставки показывает новый рисунок в прямоугольнике, который начинается с одного угла рамки.</span><span class="sxs-lookup"><span data-stu-id="a08f4-105">The inset transition reveals the new image in a rectangle originating from one corner of the frame.</span></span>

## <a name="parameters"></a><span data-ttu-id="a08f4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a08f4-106">Parameters</span></span>

<span data-ttu-id="a08f4-107">В следующей таблице описаны параметры, используемые этим переходом, и перечислены члены структуры [**ВМТ \_ видеоимаже \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) , которой они назначены.</span><span class="sxs-lookup"><span data-stu-id="a08f4-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a08f4-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="a08f4-108">Parameter</span></span></th>
<th><span data-ttu-id="a08f4-109">Член структуры</span><span class="sxs-lookup"><span data-stu-id="a08f4-109">Structure member</span></span></th>
<th><span data-ttu-id="a08f4-110">Описание</span><span class="sxs-lookup"><span data-stu-id="a08f4-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a08f4-111">Ширина</span><span class="sxs-lookup"><span data-stu-id="a08f4-111">Width</span></span></td>
<td><span data-ttu-id="a08f4-112"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="a08f4-112"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="a08f4-113">Ширина отступа в пикселях.</span><span class="sxs-lookup"><span data-stu-id="a08f4-113">Width of the inset in pixels.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a08f4-114">Высота</span><span class="sxs-lookup"><span data-stu-id="a08f4-114">Height</span></span></td>
<td><span data-ttu-id="a08f4-115"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="a08f4-115"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="a08f4-116">Высота отступа в пикселях.</span><span class="sxs-lookup"><span data-stu-id="a08f4-116">Height of the inset in pixels.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a08f4-117">Направление</span><span class="sxs-lookup"><span data-stu-id="a08f4-117">Direction</span></span></td>
<td><span data-ttu-id="a08f4-118"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="a08f4-118"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="a08f4-119">Угол, с которого начинается вставка. Задайте одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="a08f4-119">Corner from which the inset originates.Set to one of the following values:</span></span><br/>
<ul>
<li><span data-ttu-id="a08f4-120">0-вниз слева</span><span class="sxs-lookup"><span data-stu-id="a08f4-120">0 - Lower left</span></span></li>
<li><span data-ttu-id="a08f4-121">1 — нижний правый</span><span class="sxs-lookup"><span data-stu-id="a08f4-121">1 - Lower right</span></span></li>
<li><span data-ttu-id="a08f4-122">2-верхний левый</span><span class="sxs-lookup"><span data-stu-id="a08f4-122">2 - Upper left</span></span></li>
<li><span data-ttu-id="a08f4-123">3 — верхний правый</span><span class="sxs-lookup"><span data-stu-id="a08f4-123">3 - Upper right</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a08f4-124">Композиция</span><span class="sxs-lookup"><span data-stu-id="a08f4-124">Composition</span></span></td>
<td><span data-ttu-id="a08f4-125"><strong>fEffectPara3</strong></span><span class="sxs-lookup"><span data-stu-id="a08f4-125"><strong>fEffectPara3</strong></span></span></td>
<td><span data-ttu-id="a08f4-126">Задайте одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="a08f4-126">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="a08f4-127">0 — задает нормальную композицию, в которой предыдущее изображение является фоном, а текущее изображение — передним планом.</span><span class="sxs-lookup"><span data-stu-id="a08f4-127">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="a08f4-128">1 — указывает обратную композицию, в которой текущий рисунок является фоновым изображением, а предыдущее изображение — передний план.</span><span class="sxs-lookup"><span data-stu-id="a08f4-128">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="a08f4-129">Требования</span><span class="sxs-lookup"><span data-stu-id="a08f4-129">Requirements</span></span>



| <span data-ttu-id="a08f4-130">Требование</span><span class="sxs-lookup"><span data-stu-id="a08f4-130">Requirement</span></span> | <span data-ttu-id="a08f4-131">Значение</span><span class="sxs-lookup"><span data-stu-id="a08f4-131">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a08f4-132">Header</span><span class="sxs-lookup"><span data-stu-id="a08f4-132">Header</span></span><br/> | <dl> <span data-ttu-id="a08f4-133"><dt>Вмсдкидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="a08f4-133"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a08f4-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a08f4-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a08f4-135">**Переходы по изображениям видео**</span><span class="sxs-lookup"><span data-stu-id="a08f4-135">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





