---
title: WMT_VIDEOIMAGE_TRANSITION_FLIP (Вмсдкидл. h)
description: Переход «Перелистывание» поворачивает старое изображение на оси y через центр фрейма. Новый образ будет отображен в качестве обратной стороны старого образа.
ms.assetid: ff9990ef-962c-4dbb-b2bc-3bee070d2044
keywords:
- WMT_VIDEOIMAGE_TRANSITION_FLIP формат Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_FLIP
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc92ad1dfffd945b89293dd9207289aa47645d4f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649102"
---
# <a name="wmt_videoimage_transition_flip"></a><span data-ttu-id="f1e5c-105">\_отразить \_ Переход ВМТ видеоимаже \_</span><span class="sxs-lookup"><span data-stu-id="f1e5c-105">WMT\_VIDEOIMAGE\_TRANSITION\_FLIP</span></span>

<span data-ttu-id="f1e5c-106">Переход «Перелистывание» поворачивает старое изображение на оси y через центр фрейма.</span><span class="sxs-lookup"><span data-stu-id="f1e5c-106">The flip transition rotates the old image on a y-axis through the center of the frame.</span></span> <span data-ttu-id="f1e5c-107">Новый образ будет отображен в качестве обратной стороны старого образа.</span><span class="sxs-lookup"><span data-stu-id="f1e5c-107">The new image is revealed as the back of the old image.</span></span>

## <a name="parameters"></a><span data-ttu-id="f1e5c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f1e5c-108">Parameters</span></span>

<span data-ttu-id="f1e5c-109">В следующей таблице описаны параметры, используемые этим переходом, и перечислены члены структуры [**ВМТ \_ видеоимаже \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) , которой они назначены.</span><span class="sxs-lookup"><span data-stu-id="f1e5c-109">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f1e5c-110">Параметр</span><span class="sxs-lookup"><span data-stu-id="f1e5c-110">Parameter</span></span></th>
<th><span data-ttu-id="f1e5c-111">Член структуры</span><span class="sxs-lookup"><span data-stu-id="f1e5c-111">Structure member</span></span></th>
<th><span data-ttu-id="f1e5c-112">Описание</span><span class="sxs-lookup"><span data-stu-id="f1e5c-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f1e5c-113">Angle</span><span class="sxs-lookup"><span data-stu-id="f1e5c-113">Angle</span></span></td>
<td><span data-ttu-id="f1e5c-114"><strong>fEffectPara0</strong></span><span class="sxs-lookup"><span data-stu-id="f1e5c-114"><strong>fEffectPara0</strong></span></span></td>
<td><span data-ttu-id="f1e5c-115">Угол поворота (от 0,0 до 180,0 градусов).</span><span class="sxs-lookup"><span data-stu-id="f1e5c-115">Angle of the rotation, from 0.0 to 180.0 degrees.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f1e5c-116">Композиция</span><span class="sxs-lookup"><span data-stu-id="f1e5c-116">Composition</span></span></td>
<td><span data-ttu-id="f1e5c-117"><strong>fEffectPara1</strong></span><span class="sxs-lookup"><span data-stu-id="f1e5c-117"><strong>fEffectPara1</strong></span></span></td>
<td><span data-ttu-id="f1e5c-118">Задайте одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="f1e5c-118">Set to one of the following values:</span></span>
<ul>
<li><span data-ttu-id="f1e5c-119">0 — задает нормальную композицию, в которой предыдущее изображение является фоном, а текущее изображение — передним планом.</span><span class="sxs-lookup"><span data-stu-id="f1e5c-119">0 - Specifies normal composition, in which the previous image is the background, and the current image is the foreground.</span></span></li>
<li><span data-ttu-id="f1e5c-120">1 — указывает обратную композицию, в которой текущий рисунок является фоновым изображением, а предыдущее изображение — передний план.</span><span class="sxs-lookup"><span data-stu-id="f1e5c-120">1 - Specifies reversed composition, in which the current image is the background image, and the previous image is the foreground</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="f1e5c-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f1e5c-121">Remarks</span></span>

<span data-ttu-id="f1e5c-122">Вы можете визуализировать результат этого перехода, как если бы оба изображения были связаны между собой физическими фотографиями.</span><span class="sxs-lookup"><span data-stu-id="f1e5c-122">You can visualize the effect of this transition as if both images were physical photographs glued together back-to-back.</span></span> <span data-ttu-id="f1e5c-123">Переход имеет тот же результат, что и удержание двух таких фотографий в центре нижнего края и поворот их на 180 градусов.</span><span class="sxs-lookup"><span data-stu-id="f1e5c-123">The transition has the same effect as holding two such photographs at the center of the bottom edge and rotating them 180 degrees.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1e5c-124">Требования</span><span class="sxs-lookup"><span data-stu-id="f1e5c-124">Requirements</span></span>



| <span data-ttu-id="f1e5c-125">Требование</span><span class="sxs-lookup"><span data-stu-id="f1e5c-125">Requirement</span></span> | <span data-ttu-id="f1e5c-126">Значение</span><span class="sxs-lookup"><span data-stu-id="f1e5c-126">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f1e5c-127">Header</span><span class="sxs-lookup"><span data-stu-id="f1e5c-127">Header</span></span><br/> | <dl> <span data-ttu-id="f1e5c-128"><dt>Вмсдкидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1e5c-128"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1e5c-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f1e5c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1e5c-130">**Переходы по изображениям видео**</span><span class="sxs-lookup"><span data-stu-id="f1e5c-130">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





