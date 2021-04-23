---
description: Освещение в реальном мире содержит очень высокий динамический диапазон (HDR) значений светимости.
ms.assetid: 537700e2-802d-4fd1-b026-142d6f4f0559
title: Освещение HDR (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f397ccef2b1fa315e64861453b13f0f6fddfe77
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104262280"
---
# <a name="hdr-lighting-direct3d-9"></a><span data-ttu-id="0d9c2-103">Освещение HDR (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0d9c2-103">HDR Lighting (Direct3D 9)</span></span>

<span data-ttu-id="0d9c2-104">Освещение в реальном мире содержит очень высокий динамический диапазон (HDR) значений светимости.</span><span class="sxs-lookup"><span data-stu-id="0d9c2-104">Lighting in the real world contains a very high dynamic range (HDR) of luminance values.</span></span> <span data-ttu-id="0d9c2-105">Реальный мир имеет около 10 заказов динамического диапазона (DR) для значений светимости, которые распределяются по спектру оттенков по яркости.</span><span class="sxs-lookup"><span data-stu-id="0d9c2-105">The real world has about 10 orders of dynamic range (DR) for luminance values spread across the spectrum of darkness to brightness.</span></span> <span data-ttu-id="0d9c2-106">С другой стороны, экран компьютера имеет очень ограниченный цвет отображения (или диапазон значений светимости): примерно два порядка динамических диапазонов.</span><span class="sxs-lookup"><span data-stu-id="0d9c2-106">On the other hand, a computer screen has a very limited display gamut (or range of luminance values): approximately two orders of dynamic range.</span></span> <span data-ttu-id="0d9c2-107">Задача создания изображений, визуализированных в режиме HDR, заключается в сопоставлении реальных значений HDR с ограниченным охватом экрана компьютера.</span><span class="sxs-lookup"><span data-stu-id="0d9c2-107">The challenge to producing HDR rendered images is to map the real world HDR values into the limited gamut of a computer screen.</span></span>

<span data-ttu-id="0d9c2-108">Сопоставление тонов — это методика, используемая DirectX для сопоставления информации HDR с более ограниченным диапазоном.</span><span class="sxs-lookup"><span data-stu-id="0d9c2-108">Tone mapping is the technique used by DirectX for mapping HDR information into a more limited range.</span></span> <span data-ttu-id="0d9c2-109">Сопоставление тонов, применяемое к отрисовке CGI, может значительно увеличить объем отображаемых сведений об освещении, позволяя получить подробные сведения о самых темных областях и обеспечить контрастность областей, которые настолько яркие, они будут записаны.</span><span class="sxs-lookup"><span data-stu-id="0d9c2-109">Tone mapping applied to CGI rendering can dramatically improve the amount of lighting detail rendered, allowing details in the darkest areas to be seen, and providing contrast in areas that are so bright, they appear burned.</span></span> <span data-ttu-id="0d9c2-110">Итоговые сцены отображаются с гораздо более видимыми сведениями о освещении.</span><span class="sxs-lookup"><span data-stu-id="0d9c2-110">The resulting scenes render with far more visible lighting detail.</span></span>

<span data-ttu-id="0d9c2-111">[Пример хдрлигхтинг](https://msdn.microsoft.com/library/Ee417769(v=VS.85).aspx) — это пример пакета SDK, демонстрирующий освещение в виде HDR-освещения.</span><span class="sxs-lookup"><span data-stu-id="0d9c2-111">[HDRLighting Sample](https://msdn.microsoft.com/library/Ee417769(v=VS.85).aspx) is a SDK sample that demonstrates HDR lighting.</span></span>

## <a name="tone-mapping"></a><span data-ttu-id="0d9c2-112">Сопоставление тонов</span><span class="sxs-lookup"><span data-stu-id="0d9c2-112">Tone Mapping</span></span>

<span data-ttu-id="0d9c2-113">Сопоставление тонов обычно имитирует оптическое явлений, которое не может быть вызвано аварийным восстановлением монитора.</span><span class="sxs-lookup"><span data-stu-id="0d9c2-113">Tone mapping generally simulates optical phenomena that cannot be caused by the DR of the monitor.</span></span> <span data-ttu-id="0d9c2-114">Например, фларес или цветут (в основном это свойства lenses), синий сдвиг, происходящий в человеческих глазах с низкими причинами, и другие адаптации, которые являются результатом биохимии глаз.</span><span class="sxs-lookup"><span data-stu-id="0d9c2-114">Examples of this are flares or blooming (which are mostly properties of lenses), the blue shift that happens in the human eye in low light conditions, and other adaptations that are a result of the biochemistry of the eye.</span></span> <span data-ttu-id="0d9c2-115">Если аварийное восстановление отображения было достаточно большим, сопоставление тонов не будет необходимым, за исключением художественных эффектов или некоторых свойств линзы или устройства с загрузкой платы (ККД).</span><span class="sxs-lookup"><span data-stu-id="0d9c2-115">If the DR of the display were large enough, tone mapping would not be as neccessary, except for providing artistic effects or some of the properties of a camera lens or a charge coupled device (CCD).</span></span>

<span data-ttu-id="0d9c2-116">При сопоставлении тонов ряд значений светимости в сцене делится на набор зон.</span><span class="sxs-lookup"><span data-stu-id="0d9c2-116">Tone mapping divides the range of luminance values in a scene into a set of zones.</span></span> <span data-ttu-id="0d9c2-117">Каждая зона охватывает диапазон значений светимости.</span><span class="sxs-lookup"><span data-stu-id="0d9c2-117">Each zone encompasses a range of luminance values.</span></span>

<span data-ttu-id="0d9c2-118">HDR использует следующие термины:</span><span class="sxs-lookup"><span data-stu-id="0d9c2-118">HDR uses the following terms:</span></span>

-   <span data-ttu-id="0d9c2-119">Зона — диапазон значений светимости</span><span class="sxs-lookup"><span data-stu-id="0d9c2-119">Zone - range of luminance values</span></span>
-   <span data-ttu-id="0d9c2-120">Средняя серая-средняя область яркости сцены</span><span class="sxs-lookup"><span data-stu-id="0d9c2-120">Middle gray - middle brightness region of the scene</span></span>
-   <span data-ttu-id="0d9c2-121">Динамическое отношение диапазона к наибольшей освещенности сцены до наименьшей освещенности сцены</span><span class="sxs-lookup"><span data-stu-id="0d9c2-121">Dynamic range - ratio of the highest scene luminance to the lowest scene luminance</span></span>
-   <span data-ttu-id="0d9c2-122">Основные ключевые меры освещения сцены: это может быть от светлого к умеренному до темного</span><span class="sxs-lookup"><span data-stu-id="0d9c2-122">Key - subjective measurement of scene lighting: this varies from light to moderate to dark</span></span>

<span data-ttu-id="0d9c2-123">Чтобы вычислить светимость из значений RGB, используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="0d9c2-123">To calculate luminance from RGB values, use this:</span></span>


```
L = 0.27R + 0.67G + 0.06B;
```



<span data-ttu-id="0d9c2-124">Светимость по среднему логарифму является полезной аппроксимацией для ключа сцены.</span><span class="sxs-lookup"><span data-stu-id="0d9c2-124">The log-average luminance is a useful approximation for the key of a scene.</span></span> <span data-ttu-id="0d9c2-125">Общее уравнение выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="0d9c2-125">A general equation looks like this:</span></span>

<span data-ttu-id="0d9c2-126">L<sub>w</sub> = exp \[ 1/N ( \[ Журнал Sum (Дельта + L<sub>w</sub>(x, y)) \] ) \]</span><span class="sxs-lookup"><span data-stu-id="0d9c2-126">L<sub>w</sub> = exp\[ 1 / N( sum\[ log( delta + L<sub>w</sub>( x, y ) ) \] ) \]</span></span>

<span data-ttu-id="0d9c2-127">Где:</span><span class="sxs-lookup"><span data-stu-id="0d9c2-127">Where:</span></span>

-   <span data-ttu-id="0d9c2-128">L<sub>w</sub> — средний уровень освещенности журнала</span><span class="sxs-lookup"><span data-stu-id="0d9c2-128">L<sub>w</sub> - log-average luminance</span></span>
-   <span data-ttu-id="0d9c2-129">N — число пикселей в изображении</span><span class="sxs-lookup"><span data-stu-id="0d9c2-129">N - number of pixels in the image</span></span>
-   <span data-ttu-id="0d9c2-130">Дельта — небольшой фактор, позволяющий избежать проблем с черными пикселями</span><span class="sxs-lookup"><span data-stu-id="0d9c2-130">delta - a small factor to avoid problems with black pixels</span></span>
-   <span data-ttu-id="0d9c2-131">L<sub>w</sub>(x, y) — светимость мировой области для пикселя (x, y)</span><span class="sxs-lookup"><span data-stu-id="0d9c2-131">L<sub>w</sub>( x, y ) - the world space luminance for pixel ( x, y )</span></span>

<span data-ttu-id="0d9c2-132">Чтобы преобразовать это значение в среднее-серое, ниже приведен оператор масштабирования светимости:</span><span class="sxs-lookup"><span data-stu-id="0d9c2-132">To map this to a middle-gray value, here is a luminance scaling operator:</span></span>

<span data-ttu-id="0d9c2-133">L (x, y) = a \* l<sub>w</sub>(x, y)/L<sub>w</sub></span><span class="sxs-lookup"><span data-stu-id="0d9c2-133">L( x, y ) = a \* L<sub>w</sub>( x, y ) / L<sub>w</sub></span></span>

<span data-ttu-id="0d9c2-134">Где:</span><span class="sxs-lookup"><span data-stu-id="0d9c2-134">Where:</span></span>

-   <span data-ttu-id="0d9c2-135">L (x, y) — масштабируемая светимость для Pixel (x, y)</span><span class="sxs-lookup"><span data-stu-id="0d9c2-135">L( x, y ) - scaled luminance for pixel ( x, y )</span></span>
-   <span data-ttu-id="0d9c2-136">значение ключа-изображения после применения масштабирования</span><span class="sxs-lookup"><span data-stu-id="0d9c2-136">a - image key value after applying the scaling</span></span>

<span data-ttu-id="0d9c2-137">И, наконец, вот простой оператор сопоставления тонов для сжатия высокой освещенности:</span><span class="sxs-lookup"><span data-stu-id="0d9c2-137">And finally, here is a simple tone mapping operator for compressing the high luminances:</span></span>

<span data-ttu-id="0d9c2-138">L<sub>d</sub>(x, y) = L (x, y)/(1 + L (x, y))</span><span class="sxs-lookup"><span data-stu-id="0d9c2-138">L<sub>d</sub>( x, y ) = L( x, y ) / ( 1 + L( x, y ) )</span></span>

<span data-ttu-id="0d9c2-139">Где:</span><span class="sxs-lookup"><span data-stu-id="0d9c2-139">Where:</span></span>

-   <span data-ttu-id="0d9c2-140">L<sub>d</sub>(x, y) — сжатая и масштабируемая светимость для пикселей (x, y)</span><span class="sxs-lookup"><span data-stu-id="0d9c2-140">L<sub>d</sub>( x, y ) - compressed and scaled luminance for pixel ( x, y )</span></span>
-   <span data-ttu-id="0d9c2-141">значение ключа-изображения после применения масштабирования</span><span class="sxs-lookup"><span data-stu-id="0d9c2-141">a - image key value after applying the scaling</span></span>

<span data-ttu-id="0d9c2-142">Этот оператор масштабирует высокую освещенность на 1/д и низкую светимость на 1.</span><span class="sxs-lookup"><span data-stu-id="0d9c2-142">This operator scales high luminances by 1/L and low luminances by 1.</span></span> <span data-ttu-id="0d9c2-143">Дополнительные сведения см. в следующем документе.</span><span class="sxs-lookup"><span data-stu-id="0d9c2-143">For more details, see the following paper.</span></span>

<span data-ttu-id="0d9c2-144">Реинхард, Эрик, Mike контрастной, Питер Ширлэй и Джеймс Ферверда.</span><span class="sxs-lookup"><span data-stu-id="0d9c2-144">Reinhard, Erik, Mike Stark, Peter Shirley, and James Ferwerda.</span></span> <span data-ttu-id="0d9c2-145">[«Фотографическое воспроизведение цифровых изображений»](https://www.cs.utah.edu/~reinhard/cdrom/tonemap.pdf).</span><span class="sxs-lookup"><span data-stu-id="0d9c2-145">["Photographic Tone Reproduction for Digital Images"](https://www.cs.utah.edu/~reinhard/cdrom/tonemap.pdf).</span></span> <span data-ttu-id="0d9c2-146">ACM транзакции на графике (ТОГ), материалы из 29-годовой конференции по компьютерной графике и интерактивным методикам (СИГГРАФ), PP. 267-276.</span><span class="sxs-lookup"><span data-stu-id="0d9c2-146">ACM Transactions on Graphics (TOG), Proceedings of the 29th Annual Conference on Computer Graphics and Interactive Techniques (SIGGRAPH), pp. 267-276.</span></span> <span data-ttu-id="0d9c2-147">Нью Йорк, Москва: ACM Press, 2002.</span><span class="sxs-lookup"><span data-stu-id="0d9c2-147">New York, NY: ACM Press, 2002.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0d9c2-148">См. также</span><span class="sxs-lookup"><span data-stu-id="0d9c2-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d9c2-149">Дополнительные разделы</span><span class="sxs-lookup"><span data-stu-id="0d9c2-149">Advanced Topics</span></span>](advanced-topics.md)
</dt> </dl>

 

 



