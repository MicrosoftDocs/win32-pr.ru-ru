---
title: Цель рендеринга
description: Международный консорциум по цветам (ICC) определил четыре разных значения, называемые механизмами рендеринга.
ms.assetid: c980f3ea-daff-491a-a10a-03ba446d383e
keywords:
- Цветовая система Windows (WCS), изображения
- WCS (цветовая система Windows), изображения
- Управление цветом изображений, намерения рендеринга
- Управление цветом, изображения
- цвета, изображения для подготовки к просмотру
- изображения
- Международный консорциум по цвету (ICC)
- ИИК (Международный цветовой консорциум)
- Цель изображения
- Цель графики
- Цель подтверждения
- Цель соответствия
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72df148cf4c439c8081e41f3eb8089c5588e7fe2
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105720819"
---
# <a name="rendering-intents"></a><span data-ttu-id="7580f-115">Цель рендеринга</span><span class="sxs-lookup"><span data-stu-id="7580f-115">Rendering Intents</span></span>

<span data-ttu-id="7580f-116">Международный консорциум по цветам (ICC) определил четыре разных значения, называемые механизмами *рендеринга*.</span><span class="sxs-lookup"><span data-stu-id="7580f-116">The International Color Consortium (ICC) has defined four different values called *rendering intents*.</span></span> <span data-ttu-id="7580f-117">Они представляют четыре различных подхода к созданию цветовой отрисовки.</span><span class="sxs-lookup"><span data-stu-id="7580f-117">These represent four different approaches to creating a color rendering.</span></span> <span data-ttu-id="7580f-118">Эти четыре способа и константы, используемые для ссылки на них в коде, выглядят следующим образом.</span><span class="sxs-lookup"><span data-stu-id="7580f-118">These four intents, and the constants used to refer to them in code are as follows.</span></span>



| <span data-ttu-id="7580f-119">Блокировка с намерением</span><span class="sxs-lookup"><span data-stu-id="7580f-119">Intent</span></span>                            | <span data-ttu-id="7580f-120">Имя ICC</span><span class="sxs-lookup"><span data-stu-id="7580f-120">ICC Name</span></span>              | <span data-ttu-id="7580f-121">Описание</span><span class="sxs-lookup"><span data-stu-id="7580f-121">Description</span></span>                    |
|-----------------------------------|-----------------------|--------------------------------|
| <span data-ttu-id="7580f-122">Picture</span><span class="sxs-lookup"><span data-stu-id="7580f-122">Picture</span></span> | <span data-ttu-id="7580f-123">Искусственного</span><span class="sxs-lookup"><span data-stu-id="7580f-123">Perceptual</span></span>            | <span data-ttu-id="7580f-124">\_искусственного намерения</span><span class="sxs-lookup"><span data-stu-id="7580f-124">INTENT\_PERCEPTUAL</span></span>             |
| <span data-ttu-id="7580f-125">GRAPHIC</span><span class="sxs-lookup"><span data-stu-id="7580f-125">Graphic</span></span> | <span data-ttu-id="7580f-126">Насыщенность</span><span class="sxs-lookup"><span data-stu-id="7580f-126">Saturation</span></span>            | <span data-ttu-id="7580f-127">\_насыщенность намерения</span><span class="sxs-lookup"><span data-stu-id="7580f-127">INTENT\_SATURATION</span></span>             |
| <span data-ttu-id="7580f-128">Подтверждение</span><span class="sxs-lookup"><span data-stu-id="7580f-128">Proof</span></span>     | <span data-ttu-id="7580f-129">Относительно + +</span><span class="sxs-lookup"><span data-stu-id="7580f-129">Relative Colorimetric</span></span> | <span data-ttu-id="7580f-130">относительное НАМЕРЕНие + + \_ \_</span><span class="sxs-lookup"><span data-stu-id="7580f-130">INTENT\_RELATIVE\_COLORIMETRIC</span></span> |
| <span data-ttu-id="7580f-131">Соответствует</span><span class="sxs-lookup"><span data-stu-id="7580f-131">Match</span></span>     | <span data-ttu-id="7580f-132">Абсолютно + +</span><span class="sxs-lookup"><span data-stu-id="7580f-132">Absolute Colorimetric</span></span> | <span data-ttu-id="7580f-133">НАМЕРЕНие абсолютно + + \_ \_</span><span class="sxs-lookup"><span data-stu-id="7580f-133">INTENT\_ABSOLUTE\_COLORIMETRIC</span></span> |




 

<span data-ttu-id="7580f-134">Спецификация формата ICC версии 3,4, которая описывает эти способы, может быть скачана из color.org.</span><span class="sxs-lookup"><span data-stu-id="7580f-134">The ICC Profile Format Specification Version 3.4, which describes these intents, can be downloaded from color.org.</span></span>

## <a name="picture-intent"></a><span data-ttu-id="7580f-135">Цель изображения</span><span class="sxs-lookup"><span data-stu-id="7580f-135">Picture Intent</span></span>

<span data-ttu-id="7580f-136">Назначение «искусственного» в предложении спецификации ICC 4,9, цель изображения приводит к тому, что весь [цветовой охват](./g.md) изображения сжимается или расширяется для заполнения палитры целевого устройства, так что серый баланс сохраняется, но точность изображения может не сохраняться.</span><span class="sxs-lookup"><span data-stu-id="7580f-136">Called perceptual intent in the ICC specification clause 4.9, a Picture intent causes the full [gamut](./g.md) of the image to be compressed or expanded to fill the gamut of the destination device, so that gray balance is preserved but colorimetric accuracy may not be preserved.</span></span>

<span data-ttu-id="7580f-137">Иными словами, если определенные цвета в изображении выходят за пределы диапазона цветов, которые может визуализировать выходное устройство, цель изображения приведет к корректировке всех цветов в изображении, чтобы каждый цвет в изображении находился в диапазоне, который может быть визуализирован, и чтобы связь между цветами сохранялась насколько возможно.</span><span class="sxs-lookup"><span data-stu-id="7580f-137">In other words, if certain colors in an image fall outside of the range of colors that the output device can render, the picture intent will cause all the colors in the image to be adjusted so that the every color in the image falls within the range that can be rendered and so that the relationship between colors is preserved as much as possible.</span></span>

<span data-ttu-id="7580f-138">Эта цель наиболее подходит для показа фотографий и изображений, и обычно является намерением по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7580f-138">This intent is most suitable for display of photographs and images, and is generally the default intent.</span></span>

## <a name="graphic-intent"></a><span data-ttu-id="7580f-139">Цель графики</span><span class="sxs-lookup"><span data-stu-id="7580f-139">Graphic Intent</span></span>

<span data-ttu-id="7580f-140">В предложении спецификации ICC 4,12 вызывается график намерением [насыщенности](s.md) .</span><span class="sxs-lookup"><span data-stu-id="7580f-140">The ICC specification clause 4.12 calls the Graphic intent a [saturation](s.md) intent.</span></span> <span data-ttu-id="7580f-141">Он сохраняет чрома цветов в изображении за счет возможных расходов на [оттенок](h.md) и [освещение](l.md).</span><span class="sxs-lookup"><span data-stu-id="7580f-141">It preserves the chroma of colors in the image at the possible expense of [hue](h.md) and [lightness](l.md).</span></span>

<span data-ttu-id="7580f-142">Реализация этой цели остается довольно проблематичной, и ICC по-прежнему работает над методами для достижения желаемых эффектов.</span><span class="sxs-lookup"><span data-stu-id="7580f-142">Implementation of this intent remains somewhat problematic, and the ICC is still working on methods to achieve the desired effects.</span></span>

<span data-ttu-id="7580f-143">Эта цель наиболее подходит для бизнес-графики, таких как диаграммы, где более важно, чтобы цвета были ярче и точно соответствовать друг другу, а не конкретному цвету.</span><span class="sxs-lookup"><span data-stu-id="7580f-143">This intent is most suitable for business graphics such as charts, where it is more important that the colors be vivid and contrast well with each other rather than a specific color.</span></span>

## <a name="proof-intent"></a><span data-ttu-id="7580f-144">Цель подтверждения</span><span class="sxs-lookup"><span data-stu-id="7580f-144">Proof Intent</span></span>

<span data-ttu-id="7580f-145">Цель эксперимента, называемая «+ +» в спецификации ICC, определяется таким образом, что все цвета, которые выходят за пределы диапазона, который может визуализировать выходное устройство, настраиваются на ближайший к просмотру цвет, в то время как все остальные цвета остаются без изменений.</span><span class="sxs-lookup"><span data-stu-id="7580f-145">The Proof intent, called the colorimetric intent in the ICC specification, is defined such that any colors that fall outside the range that the output device can render are adjusted to the closest color that can be rendered, while all other colors are left unchanged.</span></span>

<span data-ttu-id="7580f-146">Цель подтверждения не сохраняет [белую точку](w.md).</span><span class="sxs-lookup"><span data-stu-id="7580f-146">Proof intent does not preserve the [white point](w.md).</span></span>

<span data-ttu-id="7580f-147">Например, белый цвет бумаги больше желтого, чем белый в мониторе компьютера.</span><span class="sxs-lookup"><span data-stu-id="7580f-147">For example, the whitest white of a paper is more yellow than the whitest white of a computer monitor.</span></span> <span data-ttu-id="7580f-148">Изображение, преобразованное в цветовой охват принтера с использованием относительных намерений, приведет к тому, что все цвета станут желтыми.</span><span class="sxs-lookup"><span data-stu-id="7580f-148">An image converted into the gamut of the printer using relative colorimetric intent would result in all colors becoming more yellow.</span></span> <span data-ttu-id="7580f-149">Белая точка изображения перемещается в соответствии с белой точкой принтера.</span><span class="sxs-lookup"><span data-stu-id="7580f-149">The white point of the image is moved to match the white point of the printer.</span></span> <span data-ttu-id="7580f-150">Все остальные цвета в изображении сохраняют свое расположение относительно белого пункта.</span><span class="sxs-lookup"><span data-stu-id="7580f-150">All other colors in the image keep their position relative to the white point.</span></span> <span data-ttu-id="7580f-151">При этом создается изображение, которое более точно отражает то, как будет выглядеть напечатанное изображение.</span><span class="sxs-lookup"><span data-stu-id="7580f-151">This produces an image that more accurately reflects what the printed image will look like.</span></span> <span data-ttu-id="7580f-152">Однако пользователь может найти его визуально.</span><span class="sxs-lookup"><span data-stu-id="7580f-152">However, the user may find it visually disconcerting.</span></span>

## <a name="match-intent"></a><span data-ttu-id="7580f-153">Цель соответствия</span><span class="sxs-lookup"><span data-stu-id="7580f-153">Match Intent</span></span>

<span data-ttu-id="7580f-154">При совпадении все цвета, находящиеся за пределами диапазона, который может визуализировать выходное устройство, настраиваются на ближайший цвет, который может быть визуализирован, в то время как все остальные цвета остаются без изменений.</span><span class="sxs-lookup"><span data-stu-id="7580f-154">In a Match intent, any colors that fall outside the range that the output device can render are adjusted to the closest color that can be rendered, while all other colors are left unchanged.</span></span> <span data-ttu-id="7580f-155">Спецификация ICC вызывает абсолютное намерение соответствия.</span><span class="sxs-lookup"><span data-stu-id="7580f-155">The ICC specification calls the match intent absolute colorimetric intent.</span></span>

<span data-ttu-id="7580f-156">Цель соответствия сохраняет белую точку.</span><span class="sxs-lookup"><span data-stu-id="7580f-156">Match intent preserves the white point.</span></span>

<span data-ttu-id="7580f-157">Например, белый цвет бумаги больше желтого, чем белый в мониторе компьютера.</span><span class="sxs-lookup"><span data-stu-id="7580f-157">For example, the whitest white of a paper is more yellow than the whitest white of a computer monitor.</span></span> <span data-ttu-id="7580f-158">Изображение, преобразованное в [цветовой охват](./g.md) принтера с применением соответствия, приведет к преобразованию всех цветов и их сопоставлению с охватом принтера.</span><span class="sxs-lookup"><span data-stu-id="7580f-158">An image converted into the [gamut](./g.md) of the printer using match intent would result in all colors being converted and matched into the gamut of the printer.</span></span> <span data-ttu-id="7580f-159">Белая точка изображения не перемещается в соответствии с белой точкой принтера.</span><span class="sxs-lookup"><span data-stu-id="7580f-159">The white point of the image is not moved to match the white point of the printer.</span></span> <span data-ttu-id="7580f-160">Таким образом, расстояние от цветов до белой точки может измениться.</span><span class="sxs-lookup"><span data-stu-id="7580f-160">Therefore, the distance of the colors to the white point may change.</span></span> <span data-ttu-id="7580f-161">Это создает изображение, которое менее наглядно разрабатывается для пользователя, но также является менее точным представлением вывода принтера.</span><span class="sxs-lookup"><span data-stu-id="7580f-161">This produces an image that is less visually disconcerting to the user, but is also a less accurate rendition of printer output.</span></span>

 

 