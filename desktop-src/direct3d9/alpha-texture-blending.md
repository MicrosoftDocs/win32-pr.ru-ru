---
description: Подсистема освещения сочетает цвет материала, цвет вершины и сведения о освещении для создания цвета на уровне вершины.
ms.assetid: 1e7c31cb-dc63-4f4a-9ddc-d1d1d0b69085
title: Смешение текстур альфа (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ad394b70b96e17b2ce858f871fb869afde0d122
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673135"
---
# <a name="alpha-texture-blending-direct3d-9"></a><span data-ttu-id="087e0-103">Смешение текстур альфа (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="087e0-103">Alpha Texture Blending (Direct3D 9)</span></span>

<span data-ttu-id="087e0-104">Подсистема освещения сочетает цвет материала, цвет вершины и сведения о освещении для создания цвета на уровне вершины.</span><span class="sxs-lookup"><span data-stu-id="087e0-104">The lighting engine combines material color, vertex color, and lighting information to generate a per-vertex color.</span></span> <span data-ttu-id="087e0-105">После интерполяции создается цвет для каждого пикселя, который записывается в буфер кадров.</span><span class="sxs-lookup"><span data-stu-id="087e0-105">Once interpolated, this generates a per-pixel color that is written to the frame buffer.</span></span> <span data-ttu-id="087e0-106">Если приложение включает смешение текстур, цвет пикселя станет сочетанием текущего пикселя в буфере кадров и цвета текстуры.</span><span class="sxs-lookup"><span data-stu-id="087e0-106">If an application enables texture blending, the pixel color will become a combination of the current pixel in the frame buffer and a texture color.</span></span>

<span data-ttu-id="087e0-107">Эта формула определяет цвет окончательного смешенного пикселя:</span><span class="sxs-lookup"><span data-stu-id="087e0-107">This formula determines the final blended pixel color:</span></span>


```
Color = TexelColor x SourceBlend + CurrentPixelColor x DestBlend
```



<span data-ttu-id="087e0-108">Где:</span><span class="sxs-lookup"><span data-stu-id="087e0-108">Where:</span></span>

-   <span data-ttu-id="087e0-109">Color — цвет пикселя вывода.</span><span class="sxs-lookup"><span data-stu-id="087e0-109">Color is the output pixel color.</span></span>
-   <span data-ttu-id="087e0-110">Текселколор — это цвет ввода после фильтрации текстур.</span><span class="sxs-lookup"><span data-stu-id="087e0-110">TexelColor is the input color after texture filtering.</span></span>
-   <span data-ttu-id="087e0-111">Саурцебленд — это процентная доля конечного цвета пикселя, который состоит из исходного шаг текселя цвета.</span><span class="sxs-lookup"><span data-stu-id="087e0-111">SourceBlend is the percentage of the final pixel color that is made up of the source texel color.</span></span>
-   <span data-ttu-id="087e0-112">Куррентпикселколор — цвет текущего пикселя.</span><span class="sxs-lookup"><span data-stu-id="087e0-112">CurrentPixelColor is the color of the current pixel.</span></span>
-   <span data-ttu-id="087e0-113">Дестбленд — это процентная доля конечного цвета пикселя, который составляет текущий цвет пикселя.</span><span class="sxs-lookup"><span data-stu-id="087e0-113">DestBlend is the percentage of the final pixel color that is made up of the current pixel color.</span></span>

<span data-ttu-id="087e0-114">Заключительное уравнение смешения задается путем вызова [**IDirect3DDevice9:: сетрендерстате**](/windows/desktop/api) и указания состояния отрисовки Blend (D3DRS \_ блендкскскс) с соответствующим коэффициентом смешения ([**D3DBLEND**](./d3dblend.md)).</span><span class="sxs-lookup"><span data-stu-id="087e0-114">The final blending equation is set by calling [**IDirect3DDevice9::SetRenderState**](/windows/desktop/api) and specifying the blend render state (D3DRS\_BLENDXXX) with a corresponding blending factor ([**D3DBLEND**](./d3dblend.md)).</span></span> <span data-ttu-id="087e0-115">Значения Саурцебленд и Дестбленд находятся в диапазоне от 0,0 (прозрачные) до 1,0 (непрозрачный) включительно.</span><span class="sxs-lookup"><span data-stu-id="087e0-115">The values of SourceBlend and DestBlend range from 0.0 (transparent) to 1.0 (opaque) inclusive.</span></span> <span data-ttu-id="087e0-116">Кроме того, приложение может управлять прозрачностью пикселя, задавая значение альфа в текстуре.</span><span class="sxs-lookup"><span data-stu-id="087e0-116">In addition, an application can control the transparency of a pixel by setting the alpha value in a texture.</span></span> <span data-ttu-id="087e0-117">В этом случае используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="087e0-117">In this case, use the following:</span></span>


```
SourceBlend = D3DBLEND_ZERO 
DestBlend = D3DBLEND_ONE
```



<span data-ttu-id="087e0-118">Уравнение смешения приведет к прозрачности отображаемого пикселя.</span><span class="sxs-lookup"><span data-stu-id="087e0-118">The blending equation will cause the rendered pixel to be transparent.</span></span> <span data-ttu-id="087e0-119">Значения по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="087e0-119">The default values are:</span></span>


```
SourceBlend = D3DBLEND_SRCALPHA 
DestBlend = D3DBLEND_INVSRCALPHA
```



## <a name="related-topics"></a><span data-ttu-id="087e0-120">См. также</span><span class="sxs-lookup"><span data-stu-id="087e0-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="087e0-121">Смешение текстур</span><span class="sxs-lookup"><span data-stu-id="087e0-121">Texture Blending</span></span>](texture-blending.md)
</dt> <dt>

[<span data-ttu-id="087e0-122">Фильтрация текстур (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="087e0-122">Texture Filtering (Direct3D 9)</span></span>](texture-filtering.md)
</dt> <dt>

[<span data-ttu-id="087e0-123">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="087e0-123">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 
