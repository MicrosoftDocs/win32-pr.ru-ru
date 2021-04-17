---
title: WMT_VIDEOIMAGE_TRANSITION_DIAMOND (Вмсдкидл. h)
description: Переход ромба открывает новый образ в ромбе.
ms.assetid: ff36a64d-62f7-424d-acc9-a7902926a90c
keywords:
- WMT_VIDEOIMAGE_TRANSITION_DIAMOND формат Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_DIAMOND
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e3abfa337edd58fc536e530eb0ff6473c9a9d28
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694569"
---
# <a name="wmt_videoimage_transition_diamond"></a><span data-ttu-id="91269-104">ВМТ \_ видеоимаже \_ Переход \_ ромб</span><span class="sxs-lookup"><span data-stu-id="91269-104">WMT\_VIDEOIMAGE\_TRANSITION\_DIAMOND</span></span>

<span data-ttu-id="91269-105">Переход ромба открывает новый образ в ромбе.</span><span class="sxs-lookup"><span data-stu-id="91269-105">The diamond transition reveals the new image in a diamond.</span></span>

## <a name="parameters"></a><span data-ttu-id="91269-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="91269-106">Parameters</span></span>

<span data-ttu-id="91269-107">В следующей таблице описаны параметры, используемые этим переходом, и перечислены члены структуры [**ВМТ \_ видеоимаже \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) , которой они назначены.</span><span class="sxs-lookup"><span data-stu-id="91269-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="91269-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="91269-108">Parameter</span></span></th>
<th><span data-ttu-id="91269-109">Член структуры</span><span class="sxs-lookup"><span data-stu-id="91269-109">Structure member</span></span></th>
<th><span data-ttu-id="91269-110">Описание</span><span class="sxs-lookup"><span data-stu-id="91269-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="91269-111">Центр по оси X</span><span class="sxs-lookup"><span data-stu-id="91269-111">Center X</span></span></td>
<td><span data-ttu-id="91269-112"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="91269-112"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="91269-113">Координата по оси X относительно видеокадра центра ромба.</span><span class="sxs-lookup"><span data-stu-id="91269-113">X-coordinate, relative to the video frame, of the center of the diamond.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="91269-114">Центр по оси Y</span><span class="sxs-lookup"><span data-stu-id="91269-114">Center Y</span></span></td>
<td><span data-ttu-id="91269-115"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="91269-115"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="91269-116">Координата по оси Y относительно видеокадра центра ромба.</span><span class="sxs-lookup"><span data-stu-id="91269-116">Y-coordinate, relative to the video frame, of the center of the diamond.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="91269-117">Ширина</span><span class="sxs-lookup"><span data-stu-id="91269-117">Width</span></span></td>
<td><span data-ttu-id="91269-118"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="91269-118"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="91269-119">Ширина ромба в пикселях.</span><span class="sxs-lookup"><span data-stu-id="91269-119">Width of the diamond in pixels.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="91269-120">Высота</span><span class="sxs-lookup"><span data-stu-id="91269-120">Height</span></span></td>
<td><span data-ttu-id="91269-121"><strong>fEffectPara3</strong></span><span class="sxs-lookup"><span data-stu-id="91269-121"><strong>fEffectPara3</strong></span></span></td>
<td><span data-ttu-id="91269-122">Высота ромба в пикселях.</span><span class="sxs-lookup"><span data-stu-id="91269-122">Height of the diamond in pixels.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="91269-123">Композиция</span><span class="sxs-lookup"><span data-stu-id="91269-123">Composition</span></span></td>
<td><span data-ttu-id="91269-124"><strong>fEffectPara4</strong></span><span class="sxs-lookup"><span data-stu-id="91269-124"><strong>fEffectPara4</strong></span></span></td>
<td><span data-ttu-id="91269-125">Задайте одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="91269-125">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="91269-126">0 — задает нормальную композицию, в которой предыдущее изображение является фоном, а текущее изображение — передним планом.</span><span class="sxs-lookup"><span data-stu-id="91269-126">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="91269-127">1 — указывает обратную композицию, в которой текущий рисунок является фоновым изображением, а предыдущее изображение — передний план.</span><span class="sxs-lookup"><span data-stu-id="91269-127">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="91269-128">Требования</span><span class="sxs-lookup"><span data-stu-id="91269-128">Requirements</span></span>



| <span data-ttu-id="91269-129">Требование</span><span class="sxs-lookup"><span data-stu-id="91269-129">Requirement</span></span> | <span data-ttu-id="91269-130">Значение</span><span class="sxs-lookup"><span data-stu-id="91269-130">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="91269-131">Header</span><span class="sxs-lookup"><span data-stu-id="91269-131">Header</span></span><br/> | <dl> <span data-ttu-id="91269-132"><dt>Вмсдкидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="91269-132"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91269-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="91269-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91269-134">**Переходы по изображениям видео**</span><span class="sxs-lookup"><span data-stu-id="91269-134">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





