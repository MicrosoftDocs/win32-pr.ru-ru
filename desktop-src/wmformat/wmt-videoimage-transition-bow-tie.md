---
title: WMT_VIDEOIMAGE_TRANSITION_BOW_TIE (Вмсдкидл. h)
description: Переход «линия бабочки» раскрывает новый образ в наборе треугольников на противоположных сторонах рамки.
ms.assetid: d98da767-eea7-460c-ae5f-6bef9d93ad9d
keywords:
- WMT_VIDEOIMAGE_TRANSITION_BOW_TIE формат Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_BOW_TIE
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dd4d426c335a30853085a2501206ccd6e7efc7e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674859"
---
# <a name="wmt_videoimage_transition_bow_tie"></a><span data-ttu-id="6f934-104">ВМТ \_ видеоимаже \_ Переход на \_ бабочку \_</span><span class="sxs-lookup"><span data-stu-id="6f934-104">WMT\_VIDEOIMAGE\_TRANSITION\_BOW\_TIE</span></span>

<span data-ttu-id="6f934-105">Переход «линия бабочки» раскрывает новый образ в наборе треугольников на противоположных сторонах рамки.</span><span class="sxs-lookup"><span data-stu-id="6f934-105">The bow tie transition reveals the new image in a set of triangles on opposite sides of the frame.</span></span>

## <a name="parameters"></a><span data-ttu-id="6f934-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6f934-106">Parameters</span></span>

<span data-ttu-id="6f934-107">В следующей таблице описаны параметры, используемые этим переходом, и перечислены члены структуры [**ВМТ \_ видеоимаже \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) , которой они назначены.</span><span class="sxs-lookup"><span data-stu-id="6f934-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6f934-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="6f934-108">Parameter</span></span></th>
<th><span data-ttu-id="6f934-109">Член структуры</span><span class="sxs-lookup"><span data-stu-id="6f934-109">Structure member</span></span></th>
<th><span data-ttu-id="6f934-110">Описание</span><span class="sxs-lookup"><span data-stu-id="6f934-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6f934-111">Ширина</span><span class="sxs-lookup"><span data-stu-id="6f934-111">Width</span></span></td>
<td><span data-ttu-id="6f934-112"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="6f934-112"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="6f934-113">Ширина каждой треугольной стороны для привязки бабочки.</span><span class="sxs-lookup"><span data-stu-id="6f934-113">Width of each triangular side of the bow tie.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6f934-114">Высота</span><span class="sxs-lookup"><span data-stu-id="6f934-114">Height</span></span></td>
<td><span data-ttu-id="6f934-115"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="6f934-115"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="6f934-116">Высота каждой треугольной стороны привязку к бабочке.</span><span class="sxs-lookup"><span data-stu-id="6f934-116">Height of each triangular side of the bow tie.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6f934-117">Направление</span><span class="sxs-lookup"><span data-stu-id="6f934-117">Direction</span></span></td>
<td><span data-ttu-id="6f934-118"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="6f934-118"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="6f934-119">Задайте одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="6f934-119">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="6f934-120">0 — задает результат горизонтальной бабочки, в котором треугольники вводятся справа и слева от рамки.</span><span class="sxs-lookup"><span data-stu-id="6f934-120">0 - Specifies horizontal bow tie effect, in which the triangles enter from the right and left sides of the frame.</span></span></li>
<li><span data-ttu-id="6f934-121">1 — задает действие по вертикали, при котором треугольники вводятся сверху и снизу рамки.</span><span class="sxs-lookup"><span data-stu-id="6f934-121">1 - Specifies vertical bow tie effect, in which the triangles enter from the top and bottom of the frame.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6f934-122">Композиция</span><span class="sxs-lookup"><span data-stu-id="6f934-122">Composition</span></span></td>
<td><span data-ttu-id="6f934-123"><strong>fEffectPara3</strong></span><span class="sxs-lookup"><span data-stu-id="6f934-123"><strong>fEffectPara3</strong></span></span></td>
<td><span data-ttu-id="6f934-124">Задайте одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="6f934-124">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="6f934-125">0 — задает нормальную композицию, в которой предыдущее изображение является фоном, а текущее изображение — передним планом.</span><span class="sxs-lookup"><span data-stu-id="6f934-125">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="6f934-126">1 — задает обратную композицию, в которой текущий рисунок является фоновым изображением, а предыдущее изображение — передний план.</span><span class="sxs-lookup"><span data-stu-id="6f934-126">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="6f934-127">Требования</span><span class="sxs-lookup"><span data-stu-id="6f934-127">Requirements</span></span>



| <span data-ttu-id="6f934-128">Требование</span><span class="sxs-lookup"><span data-stu-id="6f934-128">Requirement</span></span> | <span data-ttu-id="6f934-129">Значение</span><span class="sxs-lookup"><span data-stu-id="6f934-129">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6f934-130">Header</span><span class="sxs-lookup"><span data-stu-id="6f934-130">Header</span></span><br/> | <dl> <span data-ttu-id="6f934-131"><dt>Вмсдкидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f934-131"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f934-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6f934-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f934-133">**Переходы по изображениям видео**</span><span class="sxs-lookup"><span data-stu-id="6f934-133">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





