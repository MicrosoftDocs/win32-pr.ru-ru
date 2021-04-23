---
title: WMT_VIDEOIMAGE_TRANSITION_DIAGONAL (Вмсдкидл. h)
description: Диагональный переход показывает новый рисунок вдоль диагональной линии, порожденной в одном углу рамки.
ms.assetid: 1aaaf9e8-bbb8-4289-948e-5d352798e831
keywords:
- WMT_VIDEOIMAGE_TRANSITION_DIAGONAL формат Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_DIAGONAL
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6affa3e0727972e66e1ab6584c94ec233a11655
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685267"
---
# <a name="wmt_videoimage_transition_diagonal"></a><span data-ttu-id="9ccd3-104">ВМТ \_ видеоимаже \_ Переход по \_ диагонали</span><span class="sxs-lookup"><span data-stu-id="9ccd3-104">WMT\_VIDEOIMAGE\_TRANSITION\_DIAGONAL</span></span>

<span data-ttu-id="9ccd3-105">Диагональный переход показывает новый рисунок вдоль диагональной линии, порожденной в одном углу рамки.</span><span class="sxs-lookup"><span data-stu-id="9ccd3-105">The diagonal transition reveals the new image along a diagonal line originating in one corner of the frame.</span></span>

## <a name="parameters"></a><span data-ttu-id="9ccd3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9ccd3-106">Parameters</span></span>

<span data-ttu-id="9ccd3-107">В следующей таблице описаны параметры, используемые этим переходом, и перечислены члены структуры [**ВМТ \_ видеоимаже \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) , которой они назначены.</span><span class="sxs-lookup"><span data-stu-id="9ccd3-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9ccd3-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="9ccd3-108">Parameter</span></span></th>
<th><span data-ttu-id="9ccd3-109">Член структуры</span><span class="sxs-lookup"><span data-stu-id="9ccd3-109">Structure member</span></span></th>
<th><span data-ttu-id="9ccd3-110">Описание</span><span class="sxs-lookup"><span data-stu-id="9ccd3-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9ccd3-111">Ширина</span><span class="sxs-lookup"><span data-stu-id="9ccd3-111">Width</span></span></td>
<td><span data-ttu-id="9ccd3-112"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="9ccd3-112"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="9ccd3-113">Ширина диагональной секции в пикселях.</span><span class="sxs-lookup"><span data-stu-id="9ccd3-113">Width of the diagonal section in pixels.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ccd3-114">Высота</span><span class="sxs-lookup"><span data-stu-id="9ccd3-114">Height</span></span></td>
<td><span data-ttu-id="9ccd3-115"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="9ccd3-115"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="9ccd3-116">Высота диагональной секции в пикселях.</span><span class="sxs-lookup"><span data-stu-id="9ccd3-116">Height of the diagonal section in pixels.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ccd3-117">Направление</span><span class="sxs-lookup"><span data-stu-id="9ccd3-117">Direction</span></span></td>
<td><span data-ttu-id="9ccd3-118"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="9ccd3-118"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="9ccd3-119">Определяет угол, с которого исходит переход. Задайте один из следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="9ccd3-119">Determines the corner from which the transition originates.Set to one of the following:</span></span><br/>
<ul>
<li><span data-ttu-id="9ccd3-120">0-верхний правый</span><span class="sxs-lookup"><span data-stu-id="9ccd3-120">0 - Upper right</span></span></li>
<li><span data-ttu-id="9ccd3-121">1-верхний левый</span><span class="sxs-lookup"><span data-stu-id="9ccd3-121">1 - Upper left</span></span></li>
<li><span data-ttu-id="9ccd3-122">2-вниз справа</span><span class="sxs-lookup"><span data-stu-id="9ccd3-122">2 - Lower right</span></span></li>
<li><span data-ttu-id="9ccd3-123">3-вниз слева</span><span class="sxs-lookup"><span data-stu-id="9ccd3-123">3 - Lower left</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ccd3-124">Композиция</span><span class="sxs-lookup"><span data-stu-id="9ccd3-124">Composition</span></span></td>
<td><span data-ttu-id="9ccd3-125"><strong>fEffectPara3</strong></span><span class="sxs-lookup"><span data-stu-id="9ccd3-125"><strong>fEffectPara3</strong></span></span></td>
<td><span data-ttu-id="9ccd3-126">Задайте одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="9ccd3-126">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="9ccd3-127">0 — задает нормальную композицию, в которой предыдущее изображение является фоном, а текущее изображение — передним планом.</span><span class="sxs-lookup"><span data-stu-id="9ccd3-127">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="9ccd3-128">1 — задает обратную композицию, в которой текущий рисунок является фоновым изображением, а предыдущее изображение — передний план.</span><span class="sxs-lookup"><span data-stu-id="9ccd3-128">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="9ccd3-129">Требования</span><span class="sxs-lookup"><span data-stu-id="9ccd3-129">Requirements</span></span>



| <span data-ttu-id="9ccd3-130">Требование</span><span class="sxs-lookup"><span data-stu-id="9ccd3-130">Requirement</span></span> | <span data-ttu-id="9ccd3-131">Значение</span><span class="sxs-lookup"><span data-stu-id="9ccd3-131">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9ccd3-132">Header</span><span class="sxs-lookup"><span data-stu-id="9ccd3-132">Header</span></span><br/> | <dl> <span data-ttu-id="9ccd3-133"><dt>Вмсдкидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ccd3-133"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ccd3-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9ccd3-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ccd3-135">**Переходы по изображениям видео**</span><span class="sxs-lookup"><span data-stu-id="9ccd3-135">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





