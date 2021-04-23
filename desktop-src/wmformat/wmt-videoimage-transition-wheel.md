---
title: WMT_VIDEOIMAGE_TRANSITION_WHEEL (Вмсдкидл. h)
description: Переход колесика показывает новый образ, поворачивая четыре линии вокруг общей точки вращения, например звезды колеса.
ms.assetid: 426217be-789b-4b78-b0ea-de9629ecd46c
keywords:
- WMT_VIDEOIMAGE_TRANSITION_WHEEL формат Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_WHEEL
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42f39d3355cfce3397c379bf7edafaae77ccfafe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649121"
---
# <a name="wmt_videoimage_transition_wheel"></a><span data-ttu-id="4d1e6-104">\_ \_ колесо перехода ВМТ \_ видеоимаже</span><span class="sxs-lookup"><span data-stu-id="4d1e6-104">WMT\_VIDEOIMAGE\_TRANSITION\_WHEEL</span></span>

<span data-ttu-id="4d1e6-105">Переход колесика показывает новый образ, поворачивая четыре линии вокруг общей точки вращения, например звезды колеса.</span><span class="sxs-lookup"><span data-stu-id="4d1e6-105">The wheel transition reveals the new image by rotating four lines around a common pivot point, like the spokes of a wheel.</span></span>

## <a name="parameters"></a><span data-ttu-id="4d1e6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4d1e6-106">Parameters</span></span>

<span data-ttu-id="4d1e6-107">В следующей таблице описаны параметры, используемые этим переходом, и перечислены члены структуры [**ВМТ \_ видеоимаже \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) , которой они назначены.</span><span class="sxs-lookup"><span data-stu-id="4d1e6-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4d1e6-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="4d1e6-108">Parameter</span></span></th>
<th><span data-ttu-id="4d1e6-109">Член структуры</span><span class="sxs-lookup"><span data-stu-id="4d1e6-109">Structure member</span></span></th>
<th><span data-ttu-id="4d1e6-110">Описание</span><span class="sxs-lookup"><span data-stu-id="4d1e6-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4d1e6-111">Центр по оси X</span><span class="sxs-lookup"><span data-stu-id="4d1e6-111">Center X</span></span></td>
<td><span data-ttu-id="4d1e6-112"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="4d1e6-112"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="4d1e6-113">Координата по оси X относительно видеокадра центра воздействия колесика.</span><span class="sxs-lookup"><span data-stu-id="4d1e6-113">X-coordinate, relative to the video frame, of the center of the wheel effect.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d1e6-114">Центр по оси Y</span><span class="sxs-lookup"><span data-stu-id="4d1e6-114">Center Y</span></span></td>
<td><span data-ttu-id="4d1e6-115"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="4d1e6-115"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="4d1e6-116">Координата по оси Y относительно видеокадра центра воздействия колесика.</span><span class="sxs-lookup"><span data-stu-id="4d1e6-116">Y-coordinate, relative to the video frame, of the center of the wheel effect.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4d1e6-117">Angle</span><span class="sxs-lookup"><span data-stu-id="4d1e6-117">Angle</span></span></td>
<td><span data-ttu-id="4d1e6-118"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="4d1e6-118"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="4d1e6-119">Угол поворота (в градусах) периферийных элементов этого угла.</span><span class="sxs-lookup"><span data-stu-id="4d1e6-119">Angle of rotation, in degrees, of the spokes of the wheel effect.</span></span> <span data-ttu-id="4d1e6-120">Значение 0,0 указывает на старое изображение без выявила новый образ.</span><span class="sxs-lookup"><span data-stu-id="4d1e6-120">A value of 0.0 indicates the old image without any of the new image revealed.</span></span> <span data-ttu-id="4d1e6-121">Значение 90,0 указывает, что новый образ полностью отображен. Перемещение с 0,0 на 90,0 отображается с поворотом по часовой стрелке.</span><span class="sxs-lookup"><span data-stu-id="4d1e6-121">A value of 90.0 indicates the new image fully revealed.Movement from 0.0 to 90.0 appears as clockwise rotation of the spokes.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d1e6-122">Композиция</span><span class="sxs-lookup"><span data-stu-id="4d1e6-122">Composition</span></span></td>
<td><span data-ttu-id="4d1e6-123"><strong>fEffectPara3</strong></span><span class="sxs-lookup"><span data-stu-id="4d1e6-123"><strong>fEffectPara3</strong></span></span></td>
<td><span data-ttu-id="4d1e6-124">Задайте одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="4d1e6-124">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="4d1e6-125">0 — задает нормальную композицию, в которой предыдущее изображение является фоном, а текущее изображение — передним планом.</span><span class="sxs-lookup"><span data-stu-id="4d1e6-125">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="4d1e6-126">1 — указывает обратную композицию, в которой текущий рисунок является фоновым изображением, а предыдущее изображение — передний план.</span><span class="sxs-lookup"><span data-stu-id="4d1e6-126">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="4d1e6-127">Требования</span><span class="sxs-lookup"><span data-stu-id="4d1e6-127">Requirements</span></span>



| <span data-ttu-id="4d1e6-128">Требование</span><span class="sxs-lookup"><span data-stu-id="4d1e6-128">Requirement</span></span> | <span data-ttu-id="4d1e6-129">Значение</span><span class="sxs-lookup"><span data-stu-id="4d1e6-129">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4d1e6-130">Header</span><span class="sxs-lookup"><span data-stu-id="4d1e6-130">Header</span></span><br/> | <dl> <span data-ttu-id="4d1e6-131"><dt>Вмсдкидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="4d1e6-131"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d1e6-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4d1e6-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d1e6-133">**Переходы по изображениям видео**</span><span class="sxs-lookup"><span data-stu-id="4d1e6-133">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





