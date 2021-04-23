---
title: WMT_VIDEOIMAGE_TRANSITION_IRIS (Вмсдкидл. h)
description: Переход IRI раскрывает новый образ вдоль оси x и оси y. Визуальный результат этого перехода заключается в том, что новый образ отображается в расширяющемся перекрестном переходе на все стороны фрейма.
ms.assetid: 7390d959-a566-43e7-937d-1e617bc98a6e
keywords:
- WMT_VIDEOIMAGE_TRANSITION_IRIS формат Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_IRIS
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd216c7387f850f317417717c50216dd63449843
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648849"
---
# <a name="wmt_videoimage_transition_iris"></a><span data-ttu-id="c963a-105">ВМТ \_ видеоимаже \_ 1-2-3 \_</span><span class="sxs-lookup"><span data-stu-id="c963a-105">WMT\_VIDEOIMAGE\_TRANSITION\_IRIS</span></span>

<span data-ttu-id="c963a-106">Переход IRI раскрывает новый образ вдоль оси x и оси y.</span><span class="sxs-lookup"><span data-stu-id="c963a-106">The iris transition reveals the new image along an x-axis and a y-axis.</span></span> <span data-ttu-id="c963a-107">Визуальный результат этого перехода заключается в том, что новый образ отображается в расширяющемся перекрестном переходе на все стороны фрейма.</span><span class="sxs-lookup"><span data-stu-id="c963a-107">The visual effect of this transition is that the new image appears in a widening cross reaching to all sides of the frame.</span></span>

## <a name="parameters"></a><span data-ttu-id="c963a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c963a-108">Parameters</span></span>

<span data-ttu-id="c963a-109">В следующей таблице описаны параметры, используемые этим переходом, и перечислены члены структуры [**ВМТ \_ видеоимаже \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) , которой они назначены.</span><span class="sxs-lookup"><span data-stu-id="c963a-109">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c963a-110">Параметр</span><span class="sxs-lookup"><span data-stu-id="c963a-110">Parameter</span></span></th>
<th><span data-ttu-id="c963a-111">Член структуры</span><span class="sxs-lookup"><span data-stu-id="c963a-111">Structure member</span></span></th>
<th><span data-ttu-id="c963a-112">Описание</span><span class="sxs-lookup"><span data-stu-id="c963a-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c963a-113">Центр по оси X</span><span class="sxs-lookup"><span data-stu-id="c963a-113">Center X</span></span></td>
<td><span data-ttu-id="c963a-114"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="c963a-114"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="c963a-115">Координата по оси X относительно видеокадра центра результатов диафрагмы.</span><span class="sxs-lookup"><span data-stu-id="c963a-115">X-coordinate, relative to the video frame, of the center of the iris effect.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c963a-116">Центр по оси Y</span><span class="sxs-lookup"><span data-stu-id="c963a-116">Center Y</span></span></td>
<td><span data-ttu-id="c963a-117"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="c963a-117"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="c963a-118">Координата по оси Y относительно видеокадра центра результатов диафрагмы.</span><span class="sxs-lookup"><span data-stu-id="c963a-118">Y-coordinate, relative to the video frame, of the center of the iris effect.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c963a-119">Ширина</span><span class="sxs-lookup"><span data-stu-id="c963a-119">Width</span></span></td>
<td><span data-ttu-id="c963a-120"><strong>fEffectPara2</strong></span><span class="sxs-lookup"><span data-stu-id="c963a-120"><strong>fEffectPara2</strong></span></span></td>
<td><span data-ttu-id="c963a-121">Ширина вертикальной линии, в пикселях которой отображается новое изображение.</span><span class="sxs-lookup"><span data-stu-id="c963a-121">Width of the vertical line revealing the new image, in pixels.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c963a-122">Высота</span><span class="sxs-lookup"><span data-stu-id="c963a-122">Height</span></span></td>
<td><span data-ttu-id="c963a-123"><strong>fEffectPara3</strong></span><span class="sxs-lookup"><span data-stu-id="c963a-123"><strong>fEffectPara3</strong></span></span></td>
<td><span data-ttu-id="c963a-124">Высота горизонтальной линии, которая отображает новое изображение (в пикселях).</span><span class="sxs-lookup"><span data-stu-id="c963a-124">Height of the horizontal line revealing the new image, in pixels.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c963a-125">Композиция</span><span class="sxs-lookup"><span data-stu-id="c963a-125">Composition</span></span></td>
<td><span data-ttu-id="c963a-126"><strong>fEffectPara4</strong></span><span class="sxs-lookup"><span data-stu-id="c963a-126"><strong>fEffectPara4</strong></span></span></td>
<td><span data-ttu-id="c963a-127">Задайте одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="c963a-127">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="c963a-128">0 — задает нормальную композицию, в которой предыдущее изображение является фоном, а текущее изображение — передним планом.</span><span class="sxs-lookup"><span data-stu-id="c963a-128">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="c963a-129">1 — указывает обратную композицию, в которой текущий рисунок является фоновым изображением, а предыдущее изображение — передний план.</span><span class="sxs-lookup"><span data-stu-id="c963a-129">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="c963a-130">Требования</span><span class="sxs-lookup"><span data-stu-id="c963a-130">Requirements</span></span>



| <span data-ttu-id="c963a-131">Требование</span><span class="sxs-lookup"><span data-stu-id="c963a-131">Requirement</span></span> | <span data-ttu-id="c963a-132">Значение</span><span class="sxs-lookup"><span data-stu-id="c963a-132">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c963a-133">Header</span><span class="sxs-lookup"><span data-stu-id="c963a-133">Header</span></span><br/> | <dl> <span data-ttu-id="c963a-134"><dt>Вмсдкидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="c963a-134"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c963a-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c963a-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c963a-136">**Переходы по изображениям видео**</span><span class="sxs-lookup"><span data-stu-id="c963a-136">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





