---
title: WMT_VIDEOIMAGE_TRANSITION_PAGE_ROLL (Вмсдкидл. h)
description: Переход на страницу преобразует старое изображение с помощью отражения страницы и раскрывает новый рисунок под ним.
ms.assetid: 50efa4e9-0d3a-4b85-96b0-6d5cd637ca98
keywords:
- WMT_VIDEOIMAGE_TRANSITION_PAGE_ROLL формат Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_PAGE_ROLL
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4167395dbe00242af42f30713438f33e88f2dda
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648009"
---
# <a name="wmt_videoimage_transition_page_roll"></a><span data-ttu-id="b5838-104">ВМТ \_ видеоимаже \_ Переход \_ на \_ пробную страницу</span><span class="sxs-lookup"><span data-stu-id="b5838-104">WMT\_VIDEOIMAGE\_TRANSITION\_PAGE\_ROLL</span></span>

<span data-ttu-id="b5838-105">Переход на страницу преобразует старое изображение с помощью отражения страницы и раскрывает новый рисунок под ним.</span><span class="sxs-lookup"><span data-stu-id="b5838-105">The page roll transition transforms the old image with a page-flipping effect, revealing the new image underneath.</span></span>

## <a name="parameters"></a><span data-ttu-id="b5838-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b5838-106">Parameters</span></span>

<span data-ttu-id="b5838-107">В следующей таблице описаны параметры, используемые этим переходом, и перечислены члены структуры [**ВМТ \_ видеоимаже \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) , которой они назначены.</span><span class="sxs-lookup"><span data-stu-id="b5838-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b5838-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="b5838-108">Parameter</span></span></th>
<th><span data-ttu-id="b5838-109">Член структуры</span><span class="sxs-lookup"><span data-stu-id="b5838-109">Structure member</span></span></th>
<th><span data-ttu-id="b5838-110">Описание</span><span class="sxs-lookup"><span data-stu-id="b5838-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b5838-111">Радиус.</span><span class="sxs-lookup"><span data-stu-id="b5838-111">Radius</span></span></td>
<td><span data-ttu-id="b5838-112"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="b5838-112"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="b5838-113">Радиус рулона на странице.</span><span class="sxs-lookup"><span data-stu-id="b5838-113">Radius of the roll in the page roll effect.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b5838-114">расстояние;</span><span class="sxs-lookup"><span data-stu-id="b5838-114">Distance</span></span></td>
<td><span data-ttu-id="b5838-115"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="b5838-115"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="b5838-116">Объем нового изображения, отображаемого в пикселях в виде постраничного развертывания.</span><span class="sxs-lookup"><span data-stu-id="b5838-116">Amount of the new image that is revealed by the page roll effect, in pixels.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b5838-117">Направление</span><span class="sxs-lookup"><span data-stu-id="b5838-117">Direction</span></span></td>
<td><span data-ttu-id="b5838-118"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="b5838-118"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="b5838-119">Угол или сторона видеокадра, из которого поступает страница. Задайте одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="b5838-119">Corner or side of the video frame, from which the page roll originates.Set to one of the following values:</span></span><br/>
<ul>
<li><span data-ttu-id="b5838-120">0 слева</span><span class="sxs-lookup"><span data-stu-id="b5838-120">0 - Left side</span></span></li>
<li><span data-ttu-id="b5838-121">1-правая сторона</span><span class="sxs-lookup"><span data-stu-id="b5838-121">1 - Right side</span></span></li>
<li><span data-ttu-id="b5838-122">2 — снизу</span><span class="sxs-lookup"><span data-stu-id="b5838-122">2 - Bottom</span></span></li>
<li><span data-ttu-id="b5838-123">3 — сверху</span><span class="sxs-lookup"><span data-stu-id="b5838-123">3 - Top</span></span></li>
<li><span data-ttu-id="b5838-124">4. левый нижний угол</span><span class="sxs-lookup"><span data-stu-id="b5838-124">4 - Bottom left corner</span></span></li>
<li><span data-ttu-id="b5838-125">5-нижний правый угол</span><span class="sxs-lookup"><span data-stu-id="b5838-125">5 - Bottom right corner</span></span></li>
<li><span data-ttu-id="b5838-126">6-верхний левый угол</span><span class="sxs-lookup"><span data-stu-id="b5838-126">6 - Upper left corner</span></span></li>
<li><span data-ttu-id="b5838-127">7-верхний правый угол</span><span class="sxs-lookup"><span data-stu-id="b5838-127">7 - Upper right corner</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b5838-128">Композиция</span><span class="sxs-lookup"><span data-stu-id="b5838-128">Composition</span></span></td>
<td><span data-ttu-id="b5838-129"><strong>fEffectPara3</strong></span><span class="sxs-lookup"><span data-stu-id="b5838-129"><strong>fEffectPara3</strong></span></span></td>
<td><span data-ttu-id="b5838-130">Задайте одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="b5838-130">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="b5838-131">0 — задает нормальную композицию, в которой предыдущее изображение является фоном, а текущее изображение — передним планом.</span><span class="sxs-lookup"><span data-stu-id="b5838-131">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="b5838-132">1 — указывает обратную композицию, в которой текущий рисунок является фоновым изображением, а предыдущее изображение — передний план.</span><span class="sxs-lookup"><span data-stu-id="b5838-132">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="b5838-133">Требования</span><span class="sxs-lookup"><span data-stu-id="b5838-133">Requirements</span></span>



| <span data-ttu-id="b5838-134">Требование</span><span class="sxs-lookup"><span data-stu-id="b5838-134">Requirement</span></span> | <span data-ttu-id="b5838-135">Значение</span><span class="sxs-lookup"><span data-stu-id="b5838-135">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b5838-136">Header</span><span class="sxs-lookup"><span data-stu-id="b5838-136">Header</span></span><br/> | <dl> <span data-ttu-id="b5838-137"><dt>Вмсдкидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5838-137"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5838-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b5838-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5838-139">**Переходы по изображениям видео**</span><span class="sxs-lookup"><span data-stu-id="b5838-139">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





