---
title: WMT_VIDEOIMAGE_TRANSITION_STAR (Вмсдкидл. h)
description: При переходе типа "звезда" новый образ отображается на пять звездочек внутри рамки.
ms.assetid: d16f73ce-0fa8-47b4-8146-32f276e6d16c
keywords:
- WMT_VIDEOIMAGE_TRANSITION_STAR формат Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_STAR
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af064682c4488153823164433bd432a9080336fd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704399"
---
# <a name="wmt_videoimage_transition_star"></a><span data-ttu-id="8cca7-104">ВМТ \_ видеоимаже \_ 1-2-3 \_</span><span class="sxs-lookup"><span data-stu-id="8cca7-104">WMT\_VIDEOIMAGE\_TRANSITION\_STAR</span></span>

<span data-ttu-id="8cca7-105">При переходе типа "звезда" новый образ отображается на пять звездочек внутри рамки.</span><span class="sxs-lookup"><span data-stu-id="8cca7-105">The star transition reveals the new image in a five-pointed star inside the frame.</span></span>

## <a name="parameters"></a><span data-ttu-id="8cca7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8cca7-106">Parameters</span></span>

<span data-ttu-id="8cca7-107">В следующей таблице описаны параметры, используемые этим переходом, и перечислены члены структуры [**ВМТ \_ видеоимаже \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) , которой они назначены.</span><span class="sxs-lookup"><span data-stu-id="8cca7-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8cca7-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="8cca7-108">Parameter</span></span></th>
<th><span data-ttu-id="8cca7-109">Член структуры</span><span class="sxs-lookup"><span data-stu-id="8cca7-109">Structure member</span></span></th>
<th><span data-ttu-id="8cca7-110">Описание</span><span class="sxs-lookup"><span data-stu-id="8cca7-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8cca7-111">Центр по оси X</span><span class="sxs-lookup"><span data-stu-id="8cca7-111">Center X</span></span></td>
<td><span data-ttu-id="8cca7-112"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="8cca7-112"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="8cca7-113">Координата по оси X относительно видеокадра центра звезды.</span><span class="sxs-lookup"><span data-stu-id="8cca7-113">X-coordinate, relative to the video frame, of the center of the star.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8cca7-114">Центр по оси Y</span><span class="sxs-lookup"><span data-stu-id="8cca7-114">Center Y</span></span></td>
<td><span data-ttu-id="8cca7-115"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="8cca7-115"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="8cca7-116">Координата по оси Y относительно видеокадра центра звезды.</span><span class="sxs-lookup"><span data-stu-id="8cca7-116">Y-coordinate, relative to the video frame, of the center of the star.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8cca7-117">Радиус.</span><span class="sxs-lookup"><span data-stu-id="8cca7-117">Radius</span></span></td>
<td><span data-ttu-id="8cca7-118"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="8cca7-118"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="8cca7-119">Радиус (в пикселях) круга, определяемый точками звезды.</span><span class="sxs-lookup"><span data-stu-id="8cca7-119">Radius, in pixels, of the circle defined by the points of the star.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8cca7-120">Композиция</span><span class="sxs-lookup"><span data-stu-id="8cca7-120">Composition</span></span></td>
<td><span data-ttu-id="8cca7-121"><strong>fEffectPara3</strong></span><span class="sxs-lookup"><span data-stu-id="8cca7-121"><strong>fEffectPara3</strong></span></span></td>
<td><span data-ttu-id="8cca7-122">Задайте одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="8cca7-122">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="8cca7-123">0 — задает нормальную композицию, в которой предыдущее изображение является фоном, а текущее изображение — передним планом.</span><span class="sxs-lookup"><span data-stu-id="8cca7-123">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="8cca7-124">1 — задает обратную композицию, в которой текущий рисунок является фоновым изображением, а предыдущее изображение — передний план.</span><span class="sxs-lookup"><span data-stu-id="8cca7-124">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="8cca7-125">Требования</span><span class="sxs-lookup"><span data-stu-id="8cca7-125">Requirements</span></span>



| <span data-ttu-id="8cca7-126">Требование</span><span class="sxs-lookup"><span data-stu-id="8cca7-126">Requirement</span></span> | <span data-ttu-id="8cca7-127">Значение</span><span class="sxs-lookup"><span data-stu-id="8cca7-127">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8cca7-128">Header</span><span class="sxs-lookup"><span data-stu-id="8cca7-128">Header</span></span><br/> | <dl> <span data-ttu-id="8cca7-129"><dt>Вмсдкидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="8cca7-129"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8cca7-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8cca7-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cca7-131">**Переходы по изображениям видео**</span><span class="sxs-lookup"><span data-stu-id="8cca7-131">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





