---
title: WMT_VIDEOIMAGE_TRANSITION_SPLIT (Вмсдкидл. h)
description: Переход с разбиением раскрывает новый образ, разделив старый образ. Разбиение отображается вдоль прямой горизонтальной или вертикальной линии, которая начинается внутри рамки.
ms.assetid: ad777bfb-29a7-441f-8399-e462639450eb
keywords:
- WMT_VIDEOIMAGE_TRANSITION_SPLIT формат Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_SPLIT
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05df253c730b85c4bef8cf18d05ed98fcbd78f35
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648704"
---
# <a name="wmt_videoimage_transition_split"></a><span data-ttu-id="5b721-105">ВМТ \_ видеоимаже \_ Переход на \_ разбиение</span><span class="sxs-lookup"><span data-stu-id="5b721-105">WMT\_VIDEOIMAGE\_TRANSITION\_SPLIT</span></span>

<span data-ttu-id="5b721-106">Переход с разбиением раскрывает новый образ, разделив старый образ.</span><span class="sxs-lookup"><span data-stu-id="5b721-106">The split transition reveals the new image by splitting the old image.</span></span> <span data-ttu-id="5b721-107">Разбиение отображается вдоль прямой горизонтальной или вертикальной линии, которая начинается внутри рамки.</span><span class="sxs-lookup"><span data-stu-id="5b721-107">The split appears along a straight horizontal or vertical line starting inside the frame.</span></span>

## <a name="parameters"></a><span data-ttu-id="5b721-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="5b721-108">Parameters</span></span>

<span data-ttu-id="5b721-109">В следующей таблице описаны параметры, используемые этим переходом, и перечислены члены структуры [**ВМТ \_ видеоимаже \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) , которой они назначены.</span><span class="sxs-lookup"><span data-stu-id="5b721-109">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5b721-110">Параметр</span><span class="sxs-lookup"><span data-stu-id="5b721-110">Parameter</span></span></th>
<th><span data-ttu-id="5b721-111">Член структуры</span><span class="sxs-lookup"><span data-stu-id="5b721-111">Structure member</span></span></th>
<th><span data-ttu-id="5b721-112">Описание</span><span class="sxs-lookup"><span data-stu-id="5b721-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5b721-113">Центр по оси X</span><span class="sxs-lookup"><span data-stu-id="5b721-113">Center X</span></span></td>
<td><span data-ttu-id="5b721-114"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="5b721-114"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="5b721-115">Координата X относительно видеокадра исходной строки разбиения.</span><span class="sxs-lookup"><span data-stu-id="5b721-115">X-coordinate, relative to the video frame, of the origin line of the split.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b721-116">Центр по оси Y</span><span class="sxs-lookup"><span data-stu-id="5b721-116">Center Y</span></span></td>
<td><span data-ttu-id="5b721-117"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="5b721-117"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="5b721-118">Координата по оси Y относительно видеокадра исходной строки разбиения.</span><span class="sxs-lookup"><span data-stu-id="5b721-118">Y-coordinate, relative to the video frame, of the origin line of the split.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b721-119">расстояние;</span><span class="sxs-lookup"><span data-stu-id="5b721-119">Distance</span></span></td>
<td><span data-ttu-id="5b721-120"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="5b721-120"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="5b721-121">Ширина разбиения в пикселях.</span><span class="sxs-lookup"><span data-stu-id="5b721-121">Width of the split in pixels.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b721-122">Направление</span><span class="sxs-lookup"><span data-stu-id="5b721-122">Direction</span></span></td>
<td><span data-ttu-id="5b721-123"><strong>fEffectPara3</strong></span><span class="sxs-lookup"><span data-stu-id="5b721-123"><strong>fEffectPara3</strong></span></span></td>
<td><span data-ttu-id="5b721-124">Ориентация разбиения. Задайте одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="5b721-124">Orientation of the split.Set to one of the following values:</span></span><br/>
<ul>
<li><span data-ttu-id="5b721-125">0 — разделяется вдоль горизонтальной линии.</span><span class="sxs-lookup"><span data-stu-id="5b721-125">0 - Splits along a horizontal line.</span></span></li>
<li><span data-ttu-id="5b721-126">1 — разбивается вдоль вертикальной линии.</span><span class="sxs-lookup"><span data-stu-id="5b721-126">1 - Splits along a vertical line.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b721-127">Композиция</span><span class="sxs-lookup"><span data-stu-id="5b721-127">Composition</span></span></td>
<td><span data-ttu-id="5b721-128"><strong>fEffectPara4</strong></span><span class="sxs-lookup"><span data-stu-id="5b721-128"><strong>fEffectPara4</strong></span></span></td>
<td><span data-ttu-id="5b721-129">Задайте одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="5b721-129">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="5b721-130">0 — задает нормальную композицию, в которой предыдущее изображение является фоном, а текущее изображение — передним планом.</span><span class="sxs-lookup"><span data-stu-id="5b721-130">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="5b721-131">1 — указывает обратную композицию, в которой текущий рисунок является фоновым изображением, а предыдущее изображение — передний план.</span><span class="sxs-lookup"><span data-stu-id="5b721-131">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="5b721-132">Требования</span><span class="sxs-lookup"><span data-stu-id="5b721-132">Requirements</span></span>



| <span data-ttu-id="5b721-133">Требование</span><span class="sxs-lookup"><span data-stu-id="5b721-133">Requirement</span></span> | <span data-ttu-id="5b721-134">Значение</span><span class="sxs-lookup"><span data-stu-id="5b721-134">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5b721-135">Header</span><span class="sxs-lookup"><span data-stu-id="5b721-135">Header</span></span><br/> | <dl> <span data-ttu-id="5b721-136"><dt>Вмсдкидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b721-136"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b721-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5b721-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b721-138">**Переходы по изображениям видео**</span><span class="sxs-lookup"><span data-stu-id="5b721-138">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





