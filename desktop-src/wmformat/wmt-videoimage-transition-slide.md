---
title: WMT_VIDEOIMAGE_TRANSITION_SLIDE (Вмсдкидл. h)
description: Переход на слайд показывает новое изображение путем перемещения старого изображения из рамки.
ms.assetid: 925bcf92-5608-48ca-9bdc-dd08bcd8b8d5
keywords:
- WMT_VIDEOIMAGE_TRANSITION_SLIDE формат Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_SLIDE
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26caaadc268e823734c2bcf4a7899e6bb5399192
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648705"
---
# <a name="wmt_videoimage_transition_slide"></a><span data-ttu-id="3443f-104">\_ \_ слайд перехода ВМТ \_ видеоимаже</span><span class="sxs-lookup"><span data-stu-id="3443f-104">WMT\_VIDEOIMAGE\_TRANSITION\_SLIDE</span></span>

<span data-ttu-id="3443f-105">Переход на слайд показывает новое изображение путем перемещения старого изображения из рамки.</span><span class="sxs-lookup"><span data-stu-id="3443f-105">The slide transition reveals the new image by sliding the old image out of the frame.</span></span>

## <a name="parameters"></a><span data-ttu-id="3443f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3443f-106">Parameters</span></span>

<span data-ttu-id="3443f-107">В следующей таблице описаны параметры, используемые этим переходом, и перечислены члены структуры [**ВМТ \_ видеоимаже \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) , которой они назначены.</span><span class="sxs-lookup"><span data-stu-id="3443f-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3443f-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="3443f-108">Parameter</span></span></th>
<th><span data-ttu-id="3443f-109">Член структуры</span><span class="sxs-lookup"><span data-stu-id="3443f-109">Structure member</span></span></th>
<th><span data-ttu-id="3443f-110">Описание</span><span class="sxs-lookup"><span data-stu-id="3443f-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3443f-111">расстояние;</span><span class="sxs-lookup"><span data-stu-id="3443f-111">Distance</span></span></td>
<td><span data-ttu-id="3443f-112"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="3443f-112"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="3443f-113">Расстояние (в пикселях), в котором старое изображение слайдов выходит за пределы рамки.</span><span class="sxs-lookup"><span data-stu-id="3443f-113">Distance, in pixels, that the old image slides out of the frame.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3443f-114">Направление</span><span class="sxs-lookup"><span data-stu-id="3443f-114">Direction</span></span></td>
<td><span data-ttu-id="3443f-115"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="3443f-115"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="3443f-116">Направление, в котором слайды старого изображения. Задайте одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="3443f-116">Direction in which the old image slides.Set to one of the following values:</span></span><br/>
<ul>
<li><span data-ttu-id="3443f-117">0 — слайд справа.</span><span class="sxs-lookup"><span data-stu-id="3443f-117">0 - Slide to the right.</span></span></li>
<li><span data-ttu-id="3443f-118">1 — слайд слева.</span><span class="sxs-lookup"><span data-stu-id="3443f-118">1 - Slide to the left.</span></span></li>
<li><span data-ttu-id="3443f-119">2. Проведите вверх.</span><span class="sxs-lookup"><span data-stu-id="3443f-119">2 - Slide upward.</span></span></li>
<li><span data-ttu-id="3443f-120">3. Проведите вниз.</span><span class="sxs-lookup"><span data-stu-id="3443f-120">3 - Slide downward.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3443f-121">Композиция</span><span class="sxs-lookup"><span data-stu-id="3443f-121">Composition</span></span></td>
<td><span data-ttu-id="3443f-122"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="3443f-122"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="3443f-123">Задайте одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="3443f-123">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="3443f-124">0 — задает нормальную композицию, в которой предыдущее изображение является фоном, а текущее изображение — передним планом.</span><span class="sxs-lookup"><span data-stu-id="3443f-124">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="3443f-125">1 — указывает обратную композицию, в которой текущий рисунок является фоновым изображением, а предыдущее изображение — передний план.</span><span class="sxs-lookup"><span data-stu-id="3443f-125">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="3443f-126">Требования</span><span class="sxs-lookup"><span data-stu-id="3443f-126">Requirements</span></span>



| <span data-ttu-id="3443f-127">Требование</span><span class="sxs-lookup"><span data-stu-id="3443f-127">Requirement</span></span> | <span data-ttu-id="3443f-128">Значение</span><span class="sxs-lookup"><span data-stu-id="3443f-128">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3443f-129">Header</span><span class="sxs-lookup"><span data-stu-id="3443f-129">Header</span></span><br/> | <dl> <span data-ttu-id="3443f-130"><dt>Вмсдкидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="3443f-130"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3443f-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3443f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3443f-132">**Переходы по изображениям видео**</span><span class="sxs-lookup"><span data-stu-id="3443f-132">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





