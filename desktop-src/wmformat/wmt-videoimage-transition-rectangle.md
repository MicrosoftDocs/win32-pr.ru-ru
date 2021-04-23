---
title: WMT_VIDEOIMAGE_TRANSITION_RECTANGLE (Вмсдкидл. h)
description: Переход прямоугольника показывает новое изображение в прямоугольнике внутри фрейма.
ms.assetid: 2e238cd5-1da5-4145-a44d-b2658559fa0f
keywords:
- WMT_VIDEOIMAGE_TRANSITION_RECTANGLE формат Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_RECTANGLE
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cdcc5e5b074a07cee13a9af7f7a0f8c0f629de0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708418"
---
# <a name="wmt_videoimage_transition_rectangle"></a><span data-ttu-id="fb621-104">\_ \_ прямоугольник перехода ВМТ \_ видеоимаже</span><span class="sxs-lookup"><span data-stu-id="fb621-104">WMT\_VIDEOIMAGE\_TRANSITION\_RECTANGLE</span></span>

<span data-ttu-id="fb621-105">Переход прямоугольника показывает новое изображение в прямоугольнике внутри фрейма.</span><span class="sxs-lookup"><span data-stu-id="fb621-105">The rectangle transition reveals the new image in a rectangle within the frame.</span></span>

## <a name="parameters"></a><span data-ttu-id="fb621-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fb621-106">Parameters</span></span>

<span data-ttu-id="fb621-107">В следующей таблице описаны параметры, используемые этим переходом, и перечислены члены структуры [**ВМТ \_ видеоимаже \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) , которой они назначены.</span><span class="sxs-lookup"><span data-stu-id="fb621-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fb621-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="fb621-108">Parameter</span></span></th>
<th><span data-ttu-id="fb621-109">Член структуры</span><span class="sxs-lookup"><span data-stu-id="fb621-109">Structure member</span></span></th>
<th><span data-ttu-id="fb621-110">Описание</span><span class="sxs-lookup"><span data-stu-id="fb621-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fb621-111">Центр по оси X</span><span class="sxs-lookup"><span data-stu-id="fb621-111">Center X</span></span></td>
<td><span data-ttu-id="fb621-112"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="fb621-112"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="fb621-113">Координата по оси X относительно видеокадра центра прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="fb621-113">X-coordinate, relative to the video frame, of the center of the rectangle.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fb621-114">Центр по оси Y</span><span class="sxs-lookup"><span data-stu-id="fb621-114">Center Y</span></span></td>
<td><span data-ttu-id="fb621-115"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="fb621-115"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="fb621-116">Координата по оси Y относительно видеокадра центра прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="fb621-116">Y-coordinate, relative to the video frame, of the center of the rectangle.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fb621-117">Ширина</span><span class="sxs-lookup"><span data-stu-id="fb621-117">Width</span></span></td>
<td><span data-ttu-id="fb621-118"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="fb621-118"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="fb621-119">Ширина прямоугольника в пикселях.</span><span class="sxs-lookup"><span data-stu-id="fb621-119">Width of the rectangle in pixels.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fb621-120">Высота</span><span class="sxs-lookup"><span data-stu-id="fb621-120">Height</span></span></td>
<td><span data-ttu-id="fb621-121"><strong>fEffectPara3</strong></span><span class="sxs-lookup"><span data-stu-id="fb621-121"><strong>fEffectPara3</strong></span></span></td>
<td><span data-ttu-id="fb621-122">Высота прямоугольника в пикселях.</span><span class="sxs-lookup"><span data-stu-id="fb621-122">Height of the rectangle in pixels.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fb621-123">Композиция</span><span class="sxs-lookup"><span data-stu-id="fb621-123">Composition</span></span></td>
<td><span data-ttu-id="fb621-124"><strong>fEffectPara4</strong></span><span class="sxs-lookup"><span data-stu-id="fb621-124"><strong>fEffectPara4</strong></span></span></td>
<td><span data-ttu-id="fb621-125">Задайте одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="fb621-125">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="fb621-126">0 — задает нормальную композицию, в которой предыдущее изображение является фоном, а текущее изображение — передним планом.</span><span class="sxs-lookup"><span data-stu-id="fb621-126">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="fb621-127">1 — указывает обратную композицию, в которой текущий рисунок является фоновым изображением, а предыдущее изображение — передний план.</span><span class="sxs-lookup"><span data-stu-id="fb621-127">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="fb621-128">Требования</span><span class="sxs-lookup"><span data-stu-id="fb621-128">Requirements</span></span>



| <span data-ttu-id="fb621-129">Требование</span><span class="sxs-lookup"><span data-stu-id="fb621-129">Requirement</span></span> | <span data-ttu-id="fb621-130">Значение</span><span class="sxs-lookup"><span data-stu-id="fb621-130">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fb621-131">Header</span><span class="sxs-lookup"><span data-stu-id="fb621-131">Header</span></span><br/> | <dl> <span data-ttu-id="fb621-132"><dt>Вмсдкидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb621-132"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb621-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fb621-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb621-134">**Переходы по изображениям видео**</span><span class="sxs-lookup"><span data-stu-id="fb621-134">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





