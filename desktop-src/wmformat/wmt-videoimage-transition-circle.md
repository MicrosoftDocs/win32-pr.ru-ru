---
title: WMT_VIDEOIMAGE_TRANSITION_CIRCLE (Вмсдкидл. h)
description: Переход круга показывает новое изображение в круге.
ms.assetid: ba3bcf46-1254-4aad-a958-0f9ddb2f40dc
keywords:
- WMT_VIDEOIMAGE_TRANSITION_CIRCLE формат Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_CIRCLE
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ccf3a8eff2ca5a5069fa01c4e61bc0735808fd4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699238"
---
# <a name="wmt_videoimage_transition_circle"></a><span data-ttu-id="557d5-104">ВМТ \_ видеоимаженый \_ \_ круг</span><span class="sxs-lookup"><span data-stu-id="557d5-104">WMT\_VIDEOIMAGE\_TRANSITION\_CIRCLE</span></span>

<span data-ttu-id="557d5-105">Переход круга показывает новое изображение в круге.</span><span class="sxs-lookup"><span data-stu-id="557d5-105">The circle transition reveals the new image in a circle.</span></span>

## <a name="parameters"></a><span data-ttu-id="557d5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="557d5-106">Parameters</span></span>

<span data-ttu-id="557d5-107">В следующей таблице описаны параметры, используемые этим переходом, и перечислены члены структуры [**ВМТ \_ видеоимаже \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) , которой они назначены.</span><span class="sxs-lookup"><span data-stu-id="557d5-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="557d5-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="557d5-108">Parameter</span></span></th>
<th><span data-ttu-id="557d5-109">Член структуры</span><span class="sxs-lookup"><span data-stu-id="557d5-109">Structure member</span></span></th>
<th><span data-ttu-id="557d5-110">Описание</span><span class="sxs-lookup"><span data-stu-id="557d5-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="557d5-111">Центр по оси X</span><span class="sxs-lookup"><span data-stu-id="557d5-111">Center X</span></span></td>
<td><span data-ttu-id="557d5-112"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="557d5-112"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="557d5-113">Координата по оси X относительно видеокадра центра окружности.</span><span class="sxs-lookup"><span data-stu-id="557d5-113">X-coordinate, relative to the video frame, of the center of the circle.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="557d5-114">Центр по оси Y</span><span class="sxs-lookup"><span data-stu-id="557d5-114">Center Y</span></span></td>
<td><span data-ttu-id="557d5-115"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="557d5-115"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="557d5-116">Координата по оси Y относительно видеокадра центра окружности.</span><span class="sxs-lookup"><span data-stu-id="557d5-116">Y-coordinate, relative to the video frame, of center of the circle.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="557d5-117">Радиус.</span><span class="sxs-lookup"><span data-stu-id="557d5-117">Radius</span></span></td>
<td><span data-ttu-id="557d5-118"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="557d5-118"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="557d5-119">Радиус (в пикселях) круга.</span><span class="sxs-lookup"><span data-stu-id="557d5-119">Radius, in pixels, of the circle.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="557d5-120">Композиция</span><span class="sxs-lookup"><span data-stu-id="557d5-120">Composition</span></span></td>
<td><span data-ttu-id="557d5-121"><strong>fEffectPara3</strong></span><span class="sxs-lookup"><span data-stu-id="557d5-121"><strong>fEffectPara3</strong></span></span></td>
<td><span data-ttu-id="557d5-122">Задайте одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="557d5-122">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="557d5-123">0 — задает нормальную композицию, в которой предыдущее изображение является фоном, а текущее изображение — передним планом.</span><span class="sxs-lookup"><span data-stu-id="557d5-123">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="557d5-124">1 — задает обратную композицию, в которой текущий рисунок является фоновым изображением, а предыдущее изображение — передний план.</span><span class="sxs-lookup"><span data-stu-id="557d5-124">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="557d5-125">Требования</span><span class="sxs-lookup"><span data-stu-id="557d5-125">Requirements</span></span>



| <span data-ttu-id="557d5-126">Требование</span><span class="sxs-lookup"><span data-stu-id="557d5-126">Requirement</span></span> | <span data-ttu-id="557d5-127">Значение</span><span class="sxs-lookup"><span data-stu-id="557d5-127">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="557d5-128">Header</span><span class="sxs-lookup"><span data-stu-id="557d5-128">Header</span></span><br/> | <dl> <span data-ttu-id="557d5-129"><dt>Вмсдкидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="557d5-129"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="557d5-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="557d5-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="557d5-131">**Переходы по изображениям видео**</span><span class="sxs-lookup"><span data-stu-id="557d5-131">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





