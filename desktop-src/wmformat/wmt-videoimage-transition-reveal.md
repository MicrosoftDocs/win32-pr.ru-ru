---
title: WMT_VIDEOIMAGE_TRANSITION_REVEAL (Вмсдкидл. h)
description: Переход «Показать» раскрывает новый образ вдоль прямой линии, полученной с одной стороны рамки.
ms.assetid: 75ff6155-6b28-474a-b5d1-c3f1b3873b8e
keywords:
- WMT_VIDEOIMAGE_TRANSITION_REVEAL формат Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_REVEAL
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9aa385912cf106955dd33e06824d0b3668fcd97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648979"
---
# <a name="wmt_videoimage_transition_reveal"></a><span data-ttu-id="e74a1-104">ВМТ \_ видеоимаже \_ Переход \_</span><span class="sxs-lookup"><span data-stu-id="e74a1-104">WMT\_VIDEOIMAGE\_TRANSITION\_REVEAL</span></span>

<span data-ttu-id="e74a1-105">Переход «Показать» раскрывает новый образ вдоль прямой линии, полученной с одной стороны рамки.</span><span class="sxs-lookup"><span data-stu-id="e74a1-105">The reveal transition reveals the new image along a straight line originating from one side of the frame.</span></span>

## <a name="parameters"></a><span data-ttu-id="e74a1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e74a1-106">Parameters</span></span>

<span data-ttu-id="e74a1-107">В следующей таблице описаны параметры, используемые этим переходом, и перечислены члены структуры [**ВМТ \_ видеоимаже \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) , которой они назначены.</span><span class="sxs-lookup"><span data-stu-id="e74a1-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e74a1-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="e74a1-108">Parameter</span></span></th>
<th><span data-ttu-id="e74a1-109">Член структуры</span><span class="sxs-lookup"><span data-stu-id="e74a1-109">Structure member</span></span></th>
<th><span data-ttu-id="e74a1-110">Описание</span><span class="sxs-lookup"><span data-stu-id="e74a1-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e74a1-111">расстояние;</span><span class="sxs-lookup"><span data-stu-id="e74a1-111">Distance</span></span></td>
<td><span data-ttu-id="e74a1-112"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="e74a1-112"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="e74a1-113">Размер нового изображения, выданного в пикселях.</span><span class="sxs-lookup"><span data-stu-id="e74a1-113">Amount of the new image revealed, in pixels.</span></span> <span data-ttu-id="e74a1-114">Это значение задается относительно исходной стороны кадра.</span><span class="sxs-lookup"><span data-stu-id="e74a1-114">This value is relative to the originating side of the frame.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e74a1-115">Направление</span><span class="sxs-lookup"><span data-stu-id="e74a1-115">Direction</span></span></td>
<td><span data-ttu-id="e74a1-116"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="e74a1-116"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="e74a1-117">Направление раскрытия. Задайте одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="e74a1-117">Direction of the revealing.Set to one of the following values:</span></span><br/>
<ul>
<li><span data-ttu-id="e74a1-118">0 — отображается справа; исходит от левой части рамки.</span><span class="sxs-lookup"><span data-stu-id="e74a1-118">0 - Reveal to the right; originate from the left side of the frame.</span></span></li>
<li><span data-ttu-id="e74a1-119">1 — раскрывается слева; исходит от правой части кадра.</span><span class="sxs-lookup"><span data-stu-id="e74a1-119">1 - Reveal to the left; originate from the right side of the frame.</span></span></li>
<li><span data-ttu-id="e74a1-120">2. Отображение вверх; исходит от нижней части рамки.</span><span class="sxs-lookup"><span data-stu-id="e74a1-120">2 - Reveal upward; originate from the bottom of the frame.</span></span></li>
<li><span data-ttu-id="e74a1-121">3 — раскрытие вниз; исходит от верхней части рамки.</span><span class="sxs-lookup"><span data-stu-id="e74a1-121">3 - Reveal downward; originate from the top of the frame.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e74a1-122">Композиция</span><span class="sxs-lookup"><span data-stu-id="e74a1-122">Composition</span></span></td>
<td><span data-ttu-id="e74a1-123"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="e74a1-123"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="e74a1-124">Задайте одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="e74a1-124">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="e74a1-125">0 — задает нормальную композицию, в которой предыдущее изображение является фоном, а текущее изображение — передним планом.</span><span class="sxs-lookup"><span data-stu-id="e74a1-125">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="e74a1-126">1 — указывает обратную композицию, в которой текущий рисунок является фоновым изображением, а предыдущее изображение — передний план.</span><span class="sxs-lookup"><span data-stu-id="e74a1-126">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="e74a1-127">Требования</span><span class="sxs-lookup"><span data-stu-id="e74a1-127">Requirements</span></span>



| <span data-ttu-id="e74a1-128">Требование</span><span class="sxs-lookup"><span data-stu-id="e74a1-128">Requirement</span></span> | <span data-ttu-id="e74a1-129">Значение</span><span class="sxs-lookup"><span data-stu-id="e74a1-129">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e74a1-130">Header</span><span class="sxs-lookup"><span data-stu-id="e74a1-130">Header</span></span><br/> | <dl> <span data-ttu-id="e74a1-131"><dt>Вмсдкидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="e74a1-131"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e74a1-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e74a1-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e74a1-133">**Переходы по изображениям видео**</span><span class="sxs-lookup"><span data-stu-id="e74a1-133">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





