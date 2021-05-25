---
description: Следующие флаги используются для указания каналов текстуры для обработки.
ms.assetid: 0317b857-2512-4ad7-b6e3-82afdda7ea10
title: D3DX_FILTER
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c83fd0b3e12d6b5bccb13f9c5fab5e078587dbd4
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342869"
---
# <a name="d3dx_filter"></a><span data-ttu-id="cc21e-103">\_Фильтр D3DX</span><span class="sxs-lookup"><span data-stu-id="cc21e-103">D3DX\_FILTER</span></span>

<span data-ttu-id="cc21e-104">Следующие флаги используются для указания каналов текстуры для обработки.</span><span class="sxs-lookup"><span data-stu-id="cc21e-104">The following flags are used to specify which channels in a texture to operate on.</span></span>



| <span data-ttu-id="cc21e-105">\#определенно</span><span class="sxs-lookup"><span data-stu-id="cc21e-105">\#define</span></span>                | <span data-ttu-id="cc21e-106">Описание</span><span class="sxs-lookup"><span data-stu-id="cc21e-106">Description</span></span>                                                                                                                                                                                                 |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc21e-107">\_Фильтр D3DX \_ None</span><span class="sxs-lookup"><span data-stu-id="cc21e-107">D3DX\_FILTER\_NONE</span></span>      | <span data-ttu-id="cc21e-108">Масштабирование или фильтрация не выполняются.</span><span class="sxs-lookup"><span data-stu-id="cc21e-108">No scaling or filtering will take place.</span></span> <span data-ttu-id="cc21e-109">Пиксели вне границ исходного изображения считаются прозрачными черными.</span><span class="sxs-lookup"><span data-stu-id="cc21e-109">Pixels outside the bounds of the source image are assumed to be transparent black.</span></span>                                                                                 |
| <span data-ttu-id="cc21e-110">\_Точка фильтра \_ D3DX</span><span class="sxs-lookup"><span data-stu-id="cc21e-110">D3DX\_FILTER\_POINT</span></span>     | <span data-ttu-id="cc21e-111">Каждый конечный пиксель вычисляются путем выборки ближайшего пикселя из исходного изображения.</span><span class="sxs-lookup"><span data-stu-id="cc21e-111">Each destination pixel is computed by sampling the nearest pixel from the source image.</span></span>                                                                                                                     |
| <span data-ttu-id="cc21e-112">\_ \_ Линейный фильтр D3DX</span><span class="sxs-lookup"><span data-stu-id="cc21e-112">D3DX\_FILTER\_LINEAR</span></span>    | <span data-ttu-id="cc21e-113">Каждый конечный пиксель вычисляются путем выборки четырех ближайших пикселей из исходного изображения.</span><span class="sxs-lookup"><span data-stu-id="cc21e-113">Each destination pixel is computed by sampling the four nearest pixels from the source image.</span></span> <span data-ttu-id="cc21e-114">Этот фильтр лучше подходит, если масштаб по обеим осям меньше двух.</span><span class="sxs-lookup"><span data-stu-id="cc21e-114">This filter works best when the scale on both axes is less than two.</span></span>                                          |
| <span data-ttu-id="cc21e-115">\_Треугольник фильтра \_ D3DX</span><span class="sxs-lookup"><span data-stu-id="cc21e-115">D3DX\_FILTER\_TRIANGLE</span></span>  | <span data-ttu-id="cc21e-116">Каждый пиксель в исходном изображении одинаково соответствует целевому образу.</span><span class="sxs-lookup"><span data-stu-id="cc21e-116">Every pixel in the source image contributes equally to the destination image.</span></span> <span data-ttu-id="cc21e-117">Это самая медленная из фильтров.</span><span class="sxs-lookup"><span data-stu-id="cc21e-117">This is the slowest of the filters.</span></span>                                                                                           |
| <span data-ttu-id="cc21e-118">\_Поле фильтра \_ D3DX</span><span class="sxs-lookup"><span data-stu-id="cc21e-118">D3DX\_FILTER\_BOX</span></span>       | <span data-ttu-id="cc21e-119">Каждый пиксель вычисляются путем усреднения поля 2x2 (x2) пикселей из исходного изображения.</span><span class="sxs-lookup"><span data-stu-id="cc21e-119">Each pixel is computed by averaging a 2x2(x2) box of pixels from the source image.</span></span> <span data-ttu-id="cc21e-120">Этот фильтр работает только в том случае, если измерения назначения являются половиной значений источника, как в случае с MIP-карты.</span><span class="sxs-lookup"><span data-stu-id="cc21e-120">This filter works only when the dimensions of the destination are half those of the source, as is the case with mipmaps.</span></span> |
| <span data-ttu-id="cc21e-121">\_Зеркало фильтра \_ D3DX \_ U</span><span class="sxs-lookup"><span data-stu-id="cc21e-121">D3DX\_FILTER\_MIRROR\_U</span></span> | <span data-ttu-id="cc21e-122">Пиксели от края текстуры на оси u должны быть зеркально отображены, а не переноситься в оболочку.</span><span class="sxs-lookup"><span data-stu-id="cc21e-122">Pixels off the edge of the texture on the u-axis should be mirrored, not wrapped.</span></span>                                                                                                                           |
| <span data-ttu-id="cc21e-123">\_ \_ Зеркальное отображение фильтра D3DX \_ V</span><span class="sxs-lookup"><span data-stu-id="cc21e-123">D3DX\_FILTER\_MIRROR\_V</span></span> | <span data-ttu-id="cc21e-124">Пиксели от края текстуры на оси v должны быть зеркально отображены, а не переноситься в оболочку.</span><span class="sxs-lookup"><span data-stu-id="cc21e-124">Pixels off the edge of the texture on the v-axis should be mirrored, not wrapped.</span></span>                                                                                                                           |
| <span data-ttu-id="cc21e-125">\_ \_ Зеркальное отображение фильтра D3DX \_ W</span><span class="sxs-lookup"><span data-stu-id="cc21e-125">D3DX\_FILTER\_MIRROR\_W</span></span> | <span data-ttu-id="cc21e-126">Пиксели от края текстуры на оси w должны быть зеркально отражены, а не переноситься в оболочку.</span><span class="sxs-lookup"><span data-stu-id="cc21e-126">Pixels off the edge of the texture on the w-axis should be mirrored, not wrapped.</span></span>                                                                                                                           |
| <span data-ttu-id="cc21e-127">\_Зеркало фильтра \_ D3DX</span><span class="sxs-lookup"><span data-stu-id="cc21e-127">D3DX\_FILTER\_MIRROR</span></span>    | <span data-ttu-id="cc21e-128">Задание этого флага аналогично указанию \_ \_ флага зеркального отображения D3DX фильтра \_ U, D3DX \_ Filter \_ \_ V и \_ D3DX \_ фильтр \_ W Mirror.</span><span class="sxs-lookup"><span data-stu-id="cc21e-128">Specifying this flag is the same as specifying the D3DX\_FILTER\_MIRROR\_U, D3DX\_FILTER\_MIRROR\_V, and D3DX\_FILTER\_MIRROR\_W flags.</span></span>                                                                     |
| <span data-ttu-id="cc21e-129">\_Дизеринг фильтра \_ D3DX</span><span class="sxs-lookup"><span data-stu-id="cc21e-129">D3DX\_FILTER\_DITHER</span></span>    | <span data-ttu-id="cc21e-130">Полученный образ должен отменяться с помощью алгоритма сглаживания 4x4 с упорядочением.</span><span class="sxs-lookup"><span data-stu-id="cc21e-130">The resulting image must be dithered using a 4x4 ordered dither algorithm.</span></span>                                                                                                                                  |
| <span data-ttu-id="cc21e-131">D3DX \_ фильтр \_ sRGB \_ в</span><span class="sxs-lookup"><span data-stu-id="cc21e-131">D3DX\_FILTER\_SRGB\_IN</span></span>  | <span data-ttu-id="cc21e-132">Входные данные находятся в цветовом пространстве sRGB (гамма-2,2).</span><span class="sxs-lookup"><span data-stu-id="cc21e-132">Input data is in sRGB (gamma 2.2) color space.</span></span>                                                                                                                                                              |
| <span data-ttu-id="cc21e-133">D3DX \_ фильтр \_ sRGB \_</span><span class="sxs-lookup"><span data-stu-id="cc21e-133">D3DX\_FILTER\_SRGB\_OUT</span></span> | <span data-ttu-id="cc21e-134">Выходные данные находятся в цветовом пространстве sRGB (гамма-2,2).</span><span class="sxs-lookup"><span data-stu-id="cc21e-134">The output data is in sRGB (gamma 2.2) color space.</span></span>                                                                                                                                                         |
| <span data-ttu-id="cc21e-135">\_Фильтр D3DX \_ sRGB</span><span class="sxs-lookup"><span data-stu-id="cc21e-135">D3DX\_FILTER\_SRGB</span></span>      | <span data-ttu-id="cc21e-136">Аналогично указанию D3DX \_ Filter \_ sRGB \_ в \| D3DX \_ Filtering \_ sRGB \_ out.</span><span class="sxs-lookup"><span data-stu-id="cc21e-136">Same as specifying D3DX\_FILTER\_SRGB\_IN \| D3DX\_FILTER\_SRGB\_OUT.</span></span>                                                                                                                                       |



 

<span data-ttu-id="cc21e-137">Каждый допустимый фильтр должен содержать только один из следующих флагов: D3DX \_ Filter \_ None, D3DX \_ Filter \_ , D3DX \_ линейный фильтр, \_ \_ треугольник фильтра D3DX \_ или D3DX \_ поле фильтра \_ .</span><span class="sxs-lookup"><span data-stu-id="cc21e-137">Each valid filter must contain exactly one of the following flags: D3DX\_FILTER\_NONE, D3DX\_FILTER\_POINT, D3DX\_FILTER\_LINEAR, D3DX\_FILTER\_TRIANGLE, or D3DX\_FILTER\_BOX.</span></span> <span data-ttu-id="cc21e-138">Кроме того, можно использовать оператор или, чтобы указать ноль или более следующих необязательных флагов с допустимым фильтром: D3DX фильтр U, зеркальная копия фильтра \_ \_ D3DX, \_ \_ \_ \_ D3DX \_ Фильтр W, зеркальная копия фильтра \_ , D3DX фильтр, \_ \_ \_ \_ \_ D3DX \_ фильтр \_ sRGB \_ в, D3DX \_ Фильтровать \_ sRGB \_ out или D3DX \_ Filter \_ sRGB.</span><span class="sxs-lookup"><span data-stu-id="cc21e-138">In addition, you can use the OR operator to specify zero or more of the following optional flags with a valid filter: D3DX\_FILTER\_MIRROR\_U, D3DX\_FILTER\_MIRROR\_V, D3DX\_FILTER\_MIRROR\_W, D3DX\_FILTER\_MIRROR, D3DX\_FILTER\_DITHER, D3DX\_FILTER\_SRGB\_IN, D3DX\_FILTER\_SRGB\_OUT or D3DX\_FILTER\_SRGB.</span></span>

<span data-ttu-id="cc21e-139">Указание D3DX \_ по умолчанию для этого параметра обычно эквивалентно указанию D3DX \_ фильтра \_ D3DX- \| \_ \_ дизеринга Filter.</span><span class="sxs-lookup"><span data-stu-id="cc21e-139">Specifying D3DX\_DEFAULT for this parameter is usually the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span> <span data-ttu-id="cc21e-140">Однако D3DX \_ по умолчанию может иметь разные значения в зависимости от того, какой метод использует фильтр.</span><span class="sxs-lookup"><span data-stu-id="cc21e-140">However, D3DX\_DEFAULT can have different meanings, depending on which method uses the filter.</span></span> <span data-ttu-id="cc21e-141">Пример.</span><span class="sxs-lookup"><span data-stu-id="cc21e-141">For example:</span></span>

-   <span data-ttu-id="cc21e-142">При использовании [**D3DXCreateTextureFromFileEx**](d3dxcreatetexturefromfileex.md)D3DX \_ по умолчанию сопоставляется с \_ фильтром D3DX \_ треугольник \| D3DX \_ Filter \_ .</span><span class="sxs-lookup"><span data-stu-id="cc21e-142">When using [**D3DXCreateTextureFromFileEx**](d3dxcreatetexturefromfileex.md), D3DX\_DEFAULT maps to D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>
-   <span data-ttu-id="cc21e-143">При использовании [**D3DXFilterTexture**](d3dxfiltertexture.md)значение D3DX \_ по умолчанию сопоставляется с \_ полем фильтра D3DX \_ , если размер текстуры является степенью числа 2, а D3DX \_ \_ поле фильтра \| D3DX \_ фильтр \_ — в противном случае.</span><span class="sxs-lookup"><span data-stu-id="cc21e-143">When using [**D3DXFilterTexture**](d3dxfiltertexture.md), D3DX\_DEFAULT maps to D3DX\_FILTER\_BOX if the texture size is a power of two, and D3DX\_FILTER\_BOX \| D3DX\_FILTER\_DITHER otherwise.</span></span>

<span data-ttu-id="cc21e-144">Сослаться на каждый метод для проверки сведений о \_ сопоставлении фильтра по умолчанию D3DX.</span><span class="sxs-lookup"><span data-stu-id="cc21e-144">Reference each method to check for information about how D3DX\_DEFAULT filter is mapped.</span></span>

## <a name="constant-information"></a><span data-ttu-id="cc21e-145">Сведения о константе</span><span class="sxs-lookup"><span data-stu-id="cc21e-145">Constant Information</span></span>



| <span data-ttu-id="cc21e-146">Требование</span><span class="sxs-lookup"><span data-stu-id="cc21e-146">Requirement</span></span>                         | <span data-ttu-id="cc21e-147">Значение</span><span class="sxs-lookup"><span data-stu-id="cc21e-147">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="cc21e-148">Заголовок</span><span class="sxs-lookup"><span data-stu-id="cc21e-148">Header</span></span>                   | <span data-ttu-id="cc21e-149">d3dx9tex. h</span><span class="sxs-lookup"><span data-stu-id="cc21e-149">d3dx9tex.h</span></span> |
| <span data-ttu-id="cc21e-150">Минимальная операционная система</span><span class="sxs-lookup"><span data-stu-id="cc21e-150">Minimum operating system</span></span> | <span data-ttu-id="cc21e-151">Windows 98</span><span class="sxs-lookup"><span data-stu-id="cc21e-151">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="cc21e-152">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="cc21e-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc21e-153">Константы D3DX</span><span class="sxs-lookup"><span data-stu-id="cc21e-153">D3DX Constants</span></span>](dx9-graphics-reference-d3dx-constants.md)
</dt> </dl>

 

 



