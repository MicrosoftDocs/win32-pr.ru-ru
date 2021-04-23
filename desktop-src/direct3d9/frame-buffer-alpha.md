---
description: Альфа-смешение буфера фрейма отличается от Alpha альфа, Material альфа и текстуры Alpha.
ms.assetid: 3664215d-ad03-400e-beab-b0421cf6b693
title: Буфер кадров Alpha (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb310e2c66f43282e65425fd0d6c6a24961accaa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104139558"
---
# <a name="frame-buffer-alpha-direct3d-9"></a><span data-ttu-id="40f7b-103">Буфер кадров Alpha (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="40f7b-103">Frame Buffer Alpha (Direct3D 9)</span></span>

<span data-ttu-id="40f7b-104">Альфа-смешение буфера фрейма отличается от Alpha альфа, Material альфа и текстуры Alpha.</span><span class="sxs-lookup"><span data-stu-id="40f7b-104">Frame buffer alpha-blending is a bit different than vertex alpha, material alpha, and texture alpha.</span></span> <span data-ttu-id="40f7b-105">Значения прозрачности в наборе вершин, материалов и текстур, которые используются только для текущего примитива, и сами по себе не влияют на другие примитивы.</span><span class="sxs-lookup"><span data-stu-id="40f7b-105">Vertex, material, and texture alpha set transparency values that are used only for the current primitive, and by themselves have no effect on other primitives.</span></span> <span data-ttu-id="40f7b-106">Альфа-смешение буфера фрейма управляет тем, как текущий примитив объединяется с существующими пикселями в буфере кадров, чтобы получить окончательный цвет пикселя.</span><span class="sxs-lookup"><span data-stu-id="40f7b-106">Frame buffer alpha-blending controls how the current primitive is combined with existing pixels in the frame buffer to yield a final pixel color.</span></span>

<span data-ttu-id="40f7b-107">При выполнении альфа-смешения объединяются два цвета: исходный цвет и целевой цвет.</span><span class="sxs-lookup"><span data-stu-id="40f7b-107">When performing alpha blending, two colors are being combined: a source color and a destination color.</span></span> <span data-ttu-id="40f7b-108">Исходный цвет определяется прозрачным объектом, а целевой цвет — цветом, который уже находится в расположении в пикселях.</span><span class="sxs-lookup"><span data-stu-id="40f7b-108">The source color is from the transparent object, the destination color is the color already at the pixel location.</span></span> <span data-ttu-id="40f7b-109">Целевой цвет является результатом отрисовки другого объекта, который находится позади прозрачного объекта, то есть объекта, который будет виден через прозрачный объект.</span><span class="sxs-lookup"><span data-stu-id="40f7b-109">The destination color is the result of rendering some other object that is behind the transparent object, that is, the object that will be visible through the transparent object.</span></span> <span data-ttu-id="40f7b-110">Альфа-смешение использует формулу для управления отношением между исходным и целевым объектами.</span><span class="sxs-lookup"><span data-stu-id="40f7b-110">Alpha blending uses a formula to control the ratio between the source and destination objects.</span></span>


```
Final Color = ObjectColor * SourceBlendFactor + PixelColor * DestinationBlendFactor 
```



<span data-ttu-id="40f7b-111">Обжектколор — это вклад из примитива, отображаемого в текущем положении в пикселях.</span><span class="sxs-lookup"><span data-stu-id="40f7b-111">ObjectColor is the contribution from the primitive being rendered at the current pixel location.</span></span> <span data-ttu-id="40f7b-112">Пикселколор — это вклад из буфера кадров в текущем положении в пикселях.</span><span class="sxs-lookup"><span data-stu-id="40f7b-112">PixelColor is the contribution from the frame buffer at the current pixel location.</span></span>

<span data-ttu-id="40f7b-113">Ниже приведен набор коэффициентов альфа-смешения, которые можно использовать.</span><span class="sxs-lookup"><span data-stu-id="40f7b-113">The set of alpha blend factors that can be used are listed below.</span></span>



| <span data-ttu-id="40f7b-114">Коэффициент режима смешения</span><span class="sxs-lookup"><span data-stu-id="40f7b-114">Blend mode factor</span></span>         | <span data-ttu-id="40f7b-115">Описание</span><span class="sxs-lookup"><span data-stu-id="40f7b-115">Description</span></span>                                                                                                                                                                              |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40f7b-116">D3DBLEND \_ 0</span><span class="sxs-lookup"><span data-stu-id="40f7b-116">D3DBLEND\_ZERO</span></span>            | <span data-ttu-id="40f7b-117">(0, 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="40f7b-117">(0, 0, 0, 0)</span></span>                                                                                                                                                                             |
| <span data-ttu-id="40f7b-118">D3DBLEND \_ один</span><span class="sxs-lookup"><span data-stu-id="40f7b-118">D3DBLEND\_ONE</span></span>             | <span data-ttu-id="40f7b-119">(1, 1, 1, 1)</span><span class="sxs-lookup"><span data-stu-id="40f7b-119">(1, 1, 1, 1)</span></span>                                                                                                                                                                             |
| <span data-ttu-id="40f7b-120">D3DBLEND \_ сркколор</span><span class="sxs-lookup"><span data-stu-id="40f7b-120">D3DBLEND\_SRCCOLOR</span></span>        | <span data-ttu-id="40f7b-121">(RS, GS, BS, AS)</span><span class="sxs-lookup"><span data-stu-id="40f7b-121">(Rs, Gs, Bs, As)</span></span>                                                                                                                                                                         |
| <span data-ttu-id="40f7b-122">D3DBLEND \_ инвсркколор</span><span class="sxs-lookup"><span data-stu-id="40f7b-122">D3DBLEND\_INVSRCCOLOR</span></span>     | <span data-ttu-id="40f7b-123">(1-RS, 1-GS, 1-BS, 1-как)</span><span class="sxs-lookup"><span data-stu-id="40f7b-123">(1-Rs, 1-Gs, 1-Bs, 1-As)</span></span>                                                                                                                                                                 |
| <span data-ttu-id="40f7b-124">D3DBLEND \_ сркалфа</span><span class="sxs-lookup"><span data-stu-id="40f7b-124">D3DBLEND\_SRCALPHA</span></span>        | <span data-ttu-id="40f7b-125">(Как, как, как, как)</span><span class="sxs-lookup"><span data-stu-id="40f7b-125">(As, As, As, As)</span></span>                                                                                                                                                                         |
| <span data-ttu-id="40f7b-126">D3DBLEND \_ инвсркалфа</span><span class="sxs-lookup"><span data-stu-id="40f7b-126">D3DBLEND\_INVSRCALPHA</span></span>     | <span data-ttu-id="40f7b-127">(1-как, 1-как, 1-как, 1 — как)</span><span class="sxs-lookup"><span data-stu-id="40f7b-127">(1-As, 1-As, 1-As, 1-As)</span></span>                                                                                                                                                                 |
| <span data-ttu-id="40f7b-128">D3DBLEND \_ десталфа</span><span class="sxs-lookup"><span data-stu-id="40f7b-128">D3DBLEND\_DESTALPHA</span></span>       | <span data-ttu-id="40f7b-129">(AD, AD, AD, AD)</span><span class="sxs-lookup"><span data-stu-id="40f7b-129">(Ad, Ad, Ad, Ad)</span></span>                                                                                                                                                                         |
| <span data-ttu-id="40f7b-130">D3DBLEND \_ инвдесталфа</span><span class="sxs-lookup"><span data-stu-id="40f7b-130">D3DBLEND\_INVDESTALPHA</span></span>    | <span data-ttu-id="40f7b-131">(1-AD, 1-AD, 1-AD, 1-AD)</span><span class="sxs-lookup"><span data-stu-id="40f7b-131">(1-Ad, 1-Ad, 1-Ad, 1-Ad)</span></span>                                                                                                                                                                 |
| <span data-ttu-id="40f7b-132">D3DBLEND \_ дестколор</span><span class="sxs-lookup"><span data-stu-id="40f7b-132">D3DBLEND\_DESTCOLOR</span></span>       | <span data-ttu-id="40f7b-133">(RD, GD, BD, AD)</span><span class="sxs-lookup"><span data-stu-id="40f7b-133">(Rd, Gd, Bd, Ad)</span></span>                                                                                                                                                                         |
| <span data-ttu-id="40f7b-134">D3DBLEND \_ инвдестколор</span><span class="sxs-lookup"><span data-stu-id="40f7b-134">D3DBLEND\_INVDESTCOLOR</span></span>    | <span data-ttu-id="40f7b-135">(1-Rd, 1-GD, 1-BD, 1-AD)</span><span class="sxs-lookup"><span data-stu-id="40f7b-135">(1-Rd, 1-Gd, 1-Bd, 1-Ad)</span></span>                                                                                                                                                                 |
| <span data-ttu-id="40f7b-136">D3DBLEND \_ сркалфасат</span><span class="sxs-lookup"><span data-stu-id="40f7b-136">D3DBLEND\_SRCALPHASAT</span></span>     | <span data-ttu-id="40f7b-137">(f, f, f, 1); f = min (AS, 1-AD)</span><span class="sxs-lookup"><span data-stu-id="40f7b-137">(f, f, f, 1); f = min(As, 1-Ad)</span></span>                                                                                                                                                          |
| <span data-ttu-id="40f7b-138">D3DBLEND \_ боссркалфа</span><span class="sxs-lookup"><span data-stu-id="40f7b-138">D3DBLEND\_BOTHSRCALPHA</span></span>    | <span data-ttu-id="40f7b-139">Устарело для DirectX 6 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="40f7b-139">Obsolete for DirectX 6 and later.</span></span> <span data-ttu-id="40f7b-140">Вы можете добиться того же результата, установив для исходных и целевых коэффициентов смешения значения D3DBLEND \_ сркалфа и D3DBLEND \_ инвсркалфа в отдельных вызовах.</span><span class="sxs-lookup"><span data-stu-id="40f7b-140">You can achieve the same effect by setting the source and destination blend factors to D3DBLEND\_SRCALPHA and D3DBLEND\_INVSRCALPHA in separate calls.</span></span> |
| <span data-ttu-id="40f7b-141">D3DBLEND \_ босинвсркалфа</span><span class="sxs-lookup"><span data-stu-id="40f7b-141">D3DBLEND\_BOTHINVSRCALPHA</span></span> | <span data-ttu-id="40f7b-142">Устарело для DirectX 6.</span><span class="sxs-lookup"><span data-stu-id="40f7b-142">Obsolete for DirectX 6.</span></span> <span data-ttu-id="40f7b-143">Вы можете добиться того же результата, установив для исходных и целевых коэффициентов смешения значения D3DBLEND \_ инвсркалфа и D3DBLEND \_ сркалфа в отдельных вызовах.</span><span class="sxs-lookup"><span data-stu-id="40f7b-143">You can achieve the same effect by setting the source and destination blend factors to D3DBLEND\_INVSRCALPHA and D3DBLEND\_SRCALPHA in separate calls.</span></span>           |
| <span data-ttu-id="40f7b-144">D3DBLEND \_ блендфактор</span><span class="sxs-lookup"><span data-stu-id="40f7b-144">D3DBLEND\_BLENDFACTOR</span></span>     | <span data-ttu-id="40f7b-145">Используйте цвет. r, Color. g, цвет. b и цвет. объект, полученный из \_ параметра D3DRS блендфактор.</span><span class="sxs-lookup"><span data-stu-id="40f7b-145">Use color.r, color.g, color.b, and color.a obtained from the D3DRS\_BLENDFACTOR setting.</span></span>                                                                                                 |
| <span data-ttu-id="40f7b-146">D3DBLEND \_ инвблендфактор</span><span class="sxs-lookup"><span data-stu-id="40f7b-146">D3DBLEND\_INVBLENDFACTOR</span></span>  | <span data-ttu-id="40f7b-147">Используйте 1-Color. r, 1-Color. g, 1 – Color. b и 1-Color. a, полученное из \_ параметра D3DRS блендфактор.</span><span class="sxs-lookup"><span data-stu-id="40f7b-147">Use 1-color.r, 1-color.g, 1-color.b, and 1-color.a obtained from the D3DRS\_BLENDFACTOR setting.</span></span>                                                                                         |



 

<span data-ttu-id="40f7b-148">Direct3D использует \_ состояние рендеринга D3DRS алфабленденабле для включения альфа-прозрачного смешения.</span><span class="sxs-lookup"><span data-stu-id="40f7b-148">Direct3D uses the D3DRS\_ALPHABLENDENABLE render state to enable alpha transparency blending.</span></span> <span data-ttu-id="40f7b-149">Тип альфа-смешения, который выполняется, зависит от \_ состояния отрисовки D3DRS сркбленд и D3DRS \_ дестбленд.</span><span class="sxs-lookup"><span data-stu-id="40f7b-149">The type of alpha blending that is done depends on the D3DRS\_SRCBLEND and D3DRS\_DESTBLEND render states.</span></span> <span data-ttu-id="40f7b-150">Исходное и целевое состояния смешения используются парами.</span><span class="sxs-lookup"><span data-stu-id="40f7b-150">Source and destination blend states are used in pairs.</span></span> <span data-ttu-id="40f7b-151">Следующий фрагмент кода задает для состояния источника Blend значение D3DBLEND \_ сркколор, а для целевого состояния Blend — D3DBLEND \_ инвсркколор.</span><span class="sxs-lookup"><span data-stu-id="40f7b-151">The following code fragment sets the source blend state to D3DBLEND\_SRCCOLOR and the destination blend state to D3DBLEND\_INVSRCCOLOR.</span></span>


```
// This code fragment assumes that lpD3DDevice is a 
//   valid pointer to a device.

// Enable alpha blending.
lpD3DDevice->SetRenderState(D3DRS_ALPHABLENDENABLE, 
                            TRUE);

// Set the source blend state.
lpD3DDevice->SetRenderState(D3DRS_SRCBLEND, 
                            D3DBLEND_SRCCOLOR);

// Set the destination blend state.
lpD3DDevice->SetRenderState(D3DRS_DESTBLEND, 
                            D3DBLEND_INVSRCCOLOR);
```



<span data-ttu-id="40f7b-152">Этот код выполняет линейное смешение исходного цвета (цвет примитива, отображаемого в текущем расположении) и цвет назначения (цвет в текущем положении в буфере кадров).</span><span class="sxs-lookup"><span data-stu-id="40f7b-152">This code performs a linear blend between the source color (the color of the primitive being rendered at the current location) and the destination color (the color at the current location in the frame buffer).</span></span> <span data-ttu-id="40f7b-153">Полученный внешний вид аналогичен оттенку стекла в том, что некоторые цвета целевого объекта передаются через исходный объект. Оставшаяся часть он замещается.</span><span class="sxs-lookup"><span data-stu-id="40f7b-153">The resulting appearance is similar to tinted glass in that some of the color of the destination object seems to be transmitted through the source object; the rest of it appears to be absorbed.</span></span>

<span data-ttu-id="40f7b-154">Многие из этих факторов смешения предполагают, что альфа-значения в текстуре правильно работают.</span><span class="sxs-lookup"><span data-stu-id="40f7b-154">Many of these blend factors require alpha values in the texture to operate correctly.</span></span> <span data-ttu-id="40f7b-155">Таким образом, при использовании вершины или альфа-составляющей приложение ограничивается режимом, в котором будут выдаваться интересные результаты.</span><span class="sxs-lookup"><span data-stu-id="40f7b-155">Thus, when using vertex or material alpha, the application is restricted as to which modes will produce interesting results.</span></span>

## <a name="related-topics"></a><span data-ttu-id="40f7b-156">См. также</span><span class="sxs-lookup"><span data-stu-id="40f7b-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40f7b-157">Альфа-смешение</span><span class="sxs-lookup"><span data-stu-id="40f7b-157">Alpha Blending</span></span>](alpha-blending.md)
</dt> </dl>

 

 



