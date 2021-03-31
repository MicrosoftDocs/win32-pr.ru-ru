---
title: Переходы по изображениям видео
description: Переходы по изображениям видео
ms.assetid: 201ddbfb-567b-4893-b754-569f1e7d8466
keywords:
- Windows Media Format SDK, переходы по изображениям видео
- Улучшенный системный формат (ASF), переходы по изображениям видео
- ASF (расширенный формат систем), переходы к видеоизображениям
- переходы по изображениям видео
- Кодек Windows Media Video 9 (образ 2)
- кодеки, кодек Windows Media Video 9 Image v2
- видеопотоки, кодек Windows Media Video 9 Image v2
- видеопотоки, переходы изображений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbfd02628a78196a73750c2c0ff6b9e9c3d6729c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067782"
---
# <a name="video-image-transitions"></a><span data-ttu-id="d456b-111">Переходы по изображениям видео</span><span class="sxs-lookup"><span data-stu-id="d456b-111">Video Image Transitions</span></span>

<span data-ttu-id="d456b-112">Кодек Windows Media Video 9 Image v2 анимирует ряд изображений, что приводит к потоку видео.</span><span class="sxs-lookup"><span data-stu-id="d456b-112">The Windows Media Video 9 Image v2 codec animates a series of images, resulting in a video stream.</span></span> <span data-ttu-id="d456b-113">Кодек может обрабатывать два изображения одновременно, объединяя их вместе и создавая переходы друг от друга в соответствии с предоставленной конфигурацией.</span><span class="sxs-lookup"><span data-stu-id="d456b-113">The codec can manipulate two images at once, blending them together and creating a transition from one to the other according to the configuration you supply.</span></span> <span data-ttu-id="d456b-114">В этом разделе описаны поддерживаемые переходы и необходимые параметры.</span><span class="sxs-lookup"><span data-stu-id="d456b-114">This section describes the supported transitions and the parameters they require.</span></span>

<span data-ttu-id="d456b-115">Переходы перечислены в следующей таблице по их глобальным идентификаторам.</span><span class="sxs-lookup"><span data-stu-id="d456b-115">The transitions are listed in the following table by their global identifiers.</span></span>



| <span data-ttu-id="d456b-116">Идентификатор перехода</span><span class="sxs-lookup"><span data-stu-id="d456b-116">Transition identifier</span></span>                                                                           | <span data-ttu-id="d456b-117">Описание</span><span class="sxs-lookup"><span data-stu-id="d456b-117">Description</span></span>                                                                                                                                  |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d456b-118">**ВМТ \_ видеоимаже \_ Переход на \_ бабочку \_**</span><span class="sxs-lookup"><span data-stu-id="d456b-118">**WMT\_VIDEOIMAGE\_TRANSITION\_BOW\_TIE**</span></span>](wmt-videoimage-transition-bow-tie.md)              | <span data-ttu-id="d456b-119">Новый образ отображается в наборе треугольников на противоположных сторонах рамки.</span><span class="sxs-lookup"><span data-stu-id="d456b-119">New image is revealed in a set of triangles on opposite sides of the frame.</span></span>                                                                  |
| [<span data-ttu-id="d456b-120">**ВМТ \_ видеоимаженый \_ \_ круг**</span><span class="sxs-lookup"><span data-stu-id="d456b-120">**WMT\_VIDEOIMAGE\_TRANSITION\_CIRCLE**</span></span>](wmt-videoimage-transition-circle.md)                 | <span data-ttu-id="d456b-121">Новый образ отображается в круге.</span><span class="sxs-lookup"><span data-stu-id="d456b-121">New image is revealed in a circle.</span></span>                                                                                                           |
| [<span data-ttu-id="d456b-122">**\_ \_ \_ перекрестное выцветание перехода ВМТ видеоимаже \_**</span><span class="sxs-lookup"><span data-stu-id="d456b-122">**WMT\_VIDEOIMAGE\_TRANSITION\_CROSS\_FADE**</span></span>](wmt-videoimage-transition-cross-fade.md)        | <span data-ttu-id="d456b-123">Без специального перехода Коэффициенты смешения двух изображений определяют перекрестное выцветание (растворение).</span><span class="sxs-lookup"><span data-stu-id="d456b-123">No special transition, the blend coefficients of the two images determine the cross-fade (dissolve).</span></span>                                         |
| [<span data-ttu-id="d456b-124">**ВМТ \_ видеоимаже \_ Переход по \_ диагонали**</span><span class="sxs-lookup"><span data-stu-id="d456b-124">**WMT\_VIDEOIMAGE\_TRANSITION\_DIAGONAL**</span></span>](wmt-videoimage-transition-diagonal.md)             | <span data-ttu-id="d456b-125">Новый образ раскрывается по диагональной линии, порожденной в одном углу рамки.</span><span class="sxs-lookup"><span data-stu-id="d456b-125">New image is revealed along a diagonal line originating in one corner of the frame.</span></span>                                                          |
| [<span data-ttu-id="d456b-126">**ВМТ \_ видеоимаже \_ Переход \_ ромб**</span><span class="sxs-lookup"><span data-stu-id="d456b-126">**WMT\_VIDEOIMAGE\_TRANSITION\_DIAMOND**</span></span>](wmt-videoimage-transition-diamond.md)               | <span data-ttu-id="d456b-127">Новый образ отображается в виде ромба.</span><span class="sxs-lookup"><span data-stu-id="d456b-127">New image is revealed in a diamond.</span></span>                                                                                                          |
| [<span data-ttu-id="d456b-128">**ВМТ \_ видеоимаже \_ Переход \_ \_ к \_ цвету**</span><span class="sxs-lookup"><span data-stu-id="d456b-128">**WMT\_VIDEOIMAGE\_TRANSITION\_FADE\_TO\_COLOR**</span></span>](wmt-videoimage-transition-fade-to-color.md) | <span data-ttu-id="d456b-129">Разрешается из изображения в кадр сплошного цвета.</span><span class="sxs-lookup"><span data-stu-id="d456b-129">Dissolves from the image to a frame of solid color.</span></span>                                                                                          |
| [<span data-ttu-id="d456b-130">**ВМТ \_ видеоимаже \_ Переход \_ заполнен \_ V**</span><span class="sxs-lookup"><span data-stu-id="d456b-130">**WMT\_VIDEOIMAGE\_TRANSITION\_FILLED\_V**</span></span>](wmt-videoimage-transition-filled-v.md)            | <span data-ttu-id="d456b-131">Новый образ отображается в треугольнике, который начинается с одной стороны рамки.</span><span class="sxs-lookup"><span data-stu-id="d456b-131">New image is revealed in a triangle originating from one side of the frame.</span></span>                                                                  |
| [<span data-ttu-id="d456b-132">**\_отразить \_ Переход ВМТ видеоимаже \_**</span><span class="sxs-lookup"><span data-stu-id="d456b-132">**WMT\_VIDEOIMAGE\_TRANSITION\_FLIP**</span></span>](wmt-videoimage-transition-flip.md)                     | <span data-ttu-id="d456b-133">Старое изображение поворачивается на оси y через центр рамки.</span><span class="sxs-lookup"><span data-stu-id="d456b-133">Old image is rotated on a y-axis through the center of the frame.</span></span> <span data-ttu-id="d456b-134">Новый образ будет отображен в качестве обратной стороны старого образа.</span><span class="sxs-lookup"><span data-stu-id="d456b-134">The new image is revealed as the back of the old image.</span></span>                    |
| [<span data-ttu-id="d456b-135">**ВМТ \_ видеоимаже \_ перехода \_**</span><span class="sxs-lookup"><span data-stu-id="d456b-135">**WMT\_VIDEOIMAGE\_TRANSITION\_INSET**</span></span>](wmt-videoimage-transition-inset.md)                   | <span data-ttu-id="d456b-136">Новый образ раскрывается прямоугольником, который начинается с одного угла рамки.</span><span class="sxs-lookup"><span data-stu-id="d456b-136">New image is revealed by a rectangle originating from one corner of the frame.</span></span>                                                               |
| [<span data-ttu-id="d456b-137">**ВМТ \_ видеоимаже \_ 1-2-3 \_**</span><span class="sxs-lookup"><span data-stu-id="d456b-137">**WMT\_VIDEOIMAGE\_TRANSITION\_IRIS**</span></span>](wmt-videoimage-transition-iris.md)                     | <span data-ttu-id="d456b-138">Новое изображение раскрывается вдоль оси x и оси y.</span><span class="sxs-lookup"><span data-stu-id="d456b-138">New image is revealed along an x-axis and a y-axis.</span></span>                                                                                          |
| [<span data-ttu-id="d456b-139">**ВМТ \_ видеоимаже \_ Переход \_ на \_ пробную страницу**</span><span class="sxs-lookup"><span data-stu-id="d456b-139">**WMT\_VIDEOIMAGE\_TRANSITION\_PAGE\_ROLL**</span></span>](wmt-videoimage-transition-page-roll.md)          | <span data-ttu-id="d456b-140">Старое изображение преобразуется в результате зеркального отображения страницы, что приводит к раскрытию нового изображения под.</span><span class="sxs-lookup"><span data-stu-id="d456b-140">Old image is transformed in a page-flipping effect, revealing the new image underneath.</span></span>                                                      |
| [<span data-ttu-id="d456b-141">**\_ \_ прямоугольник перехода ВМТ \_ видеоимаже**</span><span class="sxs-lookup"><span data-stu-id="d456b-141">**WMT\_VIDEOIMAGE\_TRANSITION\_RECTANGLE**</span></span>](wmt-videoimage-transition-rectangle.md)           | <span data-ttu-id="d456b-142">Новый образ раскрывается прямоугольником внутри рамки.</span><span class="sxs-lookup"><span data-stu-id="d456b-142">New image is revealed by a rectangle within the frame.</span></span>                                                                                       |
| [<span data-ttu-id="d456b-143">**ВМТ \_ видеоимаже \_ Переход \_**</span><span class="sxs-lookup"><span data-stu-id="d456b-143">**WMT\_VIDEOIMAGE\_TRANSITION\_REVEAL**</span></span>](wmt-videoimage-transition-reveal.md)                 | <span data-ttu-id="d456b-144">Новый образ раскрывается по прямой линии, полученной с одной стороны рамки.</span><span class="sxs-lookup"><span data-stu-id="d456b-144">New image is revealed along a straight line originating from one side of the frame.</span></span>                                                          |
| [<span data-ttu-id="d456b-145">**\_ \_ слайд перехода ВМТ \_ видеоимаже**</span><span class="sxs-lookup"><span data-stu-id="d456b-145">**WMT\_VIDEOIMAGE\_TRANSITION\_SLIDE**</span></span>](wmt-videoimage-transition-slide.md)                   | <span data-ttu-id="d456b-146">Старые слайды изображения выходят за пределы кадра, раскрывая новый рисунок под ним.</span><span class="sxs-lookup"><span data-stu-id="d456b-146">Old image slides out of the frame, revealing the new image underneath.</span></span>                                                                       |
| [<span data-ttu-id="d456b-147">**ВМТ \_ видеоимаже \_ Переход на \_ разбиение**</span><span class="sxs-lookup"><span data-stu-id="d456b-147">**WMT\_VIDEOIMAGE\_TRANSITION\_SPLIT**</span></span>](wmt-videoimage-transition-split.md)                   | <span data-ttu-id="d456b-148">Новый образ раскрывается по горизонтали или вертикали в старом изображении.</span><span class="sxs-lookup"><span data-stu-id="d456b-148">New image is revealed by a horizontal or vertical split in the old image.</span></span> <span data-ttu-id="d456b-149">Разбиение отображается вдоль прямой линии, которая начинается внутри рамки.</span><span class="sxs-lookup"><span data-stu-id="d456b-149">The split appears along a straight line starting inside the frame.</span></span> |
| [<span data-ttu-id="d456b-150">**ВМТ \_ видеоимаже \_ 1-2-3 \_**</span><span class="sxs-lookup"><span data-stu-id="d456b-150">**WMT\_VIDEOIMAGE\_TRANSITION\_STAR**</span></span>](wmt-videoimage-transition-star.md)                     | <span data-ttu-id="d456b-151">Новый образ отображается в рамке с пятью символами звездочки.</span><span class="sxs-lookup"><span data-stu-id="d456b-151">New image is revealed by a five-pointed star inside the frame.</span></span>                                                                               |
| [<span data-ttu-id="d456b-152">**\_ \_ колесо перехода ВМТ \_ видеоимаже**</span><span class="sxs-lookup"><span data-stu-id="d456b-152">**WMT\_VIDEOIMAGE\_TRANSITION\_WHEEL**</span></span>](wmt-videoimage-transition-wheel.md)                   | <span data-ttu-id="d456b-153">Новый образ раскрывается четырьмя вращающимися периферийными точками с общей точкой вращения.</span><span class="sxs-lookup"><span data-stu-id="d456b-153">New image is revealed by four rotating spokes with a common pivot point.</span></span>                                                                     |



 

<span data-ttu-id="d456b-154">Каждый переход полностью описывается в своем разделе.</span><span class="sxs-lookup"><span data-stu-id="d456b-154">Each transition is fully described in its own topic.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d456b-155">См. также</span><span class="sxs-lookup"><span data-stu-id="d456b-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d456b-156">**Справочник по программированию**</span><span class="sxs-lookup"><span data-stu-id="d456b-156">**Programming Reference**</span></span>](programming-reference.md)
</dt> <dt>

[<span data-ttu-id="d456b-157">**ВМТ \_ видеоимаже \_ SAMPLE2**</span><span class="sxs-lookup"><span data-stu-id="d456b-157">**WMT\_VIDEOIMAGE\_SAMPLE2**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2)
</dt> </dl>

 

 




