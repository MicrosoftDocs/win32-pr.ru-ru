---
description: Текстуры всегда обрабатываются с помощью (0,0, 0,0) в левом верхнем углу до (1,0, 1,0) в правом нижнем углу, как показано на следующем рисунке.
ms.assetid: 16fb04b9-4476-4dbe-a24f-51c0813a7917
title: Билинейнойная фильтрация текстур (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f51213e5187c775963de2fa740847d55084c5be2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423454"
---
# <a name="bilinear-texture-filtering-direct3d-9"></a><span data-ttu-id="2cbf7-103">Билинейнойная фильтрация текстур (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="2cbf7-103">Bilinear Texture Filtering (Direct3D 9)</span></span>

<span data-ttu-id="2cbf7-104">Текстуры всегда обрабатываются с помощью (0,0, 0,0) в левом верхнем углу до (1,0, 1,0) в правом нижнем углу, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="2cbf7-104">Textures are always linearly addressed from (0.0, 0.0) at the top-left corner to (1.0, 1.0) at the bottom-right corner, as shown in the following illustration.</span></span>

![Иллюстрация текстуры 4x4 со сплошными блоками цвета](images/bilinear-fig7a.png)

<span data-ttu-id="2cbf7-106">Обычно текстуры представляются как состоящие из сплошных блоков цвета, однако правильнее воспринимать текстуры так же, как растровые дисплеи: каждый тексель определяется точно по центру ячейки сетки, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="2cbf7-106">Textures are usually represented as if they were composed of solid blocks of color, but it's actually more correct to think of textures the same way you should think of the raster display: Each texel is defined at the exact center of a grid cell, as shown in the following illustration.</span></span>

![Иллюстрация текстуры 4x4 с текселями, определенными в центре ячеек сетки](images/bilinear-fig7b.png)

<span data-ttu-id="2cbf7-108">Если запросить у инструмента "пипетка" UV-координаты этого цвета текстуры (0,375, 0,375), вы получите однотонный красный (255, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="2cbf7-108">If you ask the texture sampler for this texture's color at UV coordinates (0.375, 0.375) you'll get solid red (255, 0, 0).</span></span> <span data-ttu-id="2cbf7-109">Это имеет смысл, поскольку точный центр красной шаг текселя ячейки находится на UV (0,375, 0,375).</span><span class="sxs-lookup"><span data-stu-id="2cbf7-109">That makes perfect sense because the exact center of the red texel cell is at UV (0.375, 0.375).</span></span> <span data-ttu-id="2cbf7-110">А что если с помощью пипетки определить цвет текстуры на UV (0,25, 0,25)?</span><span class="sxs-lookup"><span data-stu-id="2cbf7-110">What if you ask the sampler for the texture's color at UV (0.25, 0.25)?</span></span> <span data-ttu-id="2cbf7-111">Это не так просто, так как точка UV (0,25, 0,25) находится в точном углу 4 пикселей текстуры.</span><span class="sxs-lookup"><span data-stu-id="2cbf7-111">That's not quite as easy, because the point at UV (0.25, 0.25) lies at the exact corner of 4 texels.</span></span>

<span data-ttu-id="2cbf7-112">Простейшая схема — это просто сделать так, чтобы образец возвращал цвет ближайшего шаг текселяа; Это называется фильтрацией точек (см. раздел [выборка с ближайшими точками (Direct3D 9)](nearest-point-sampling.md)) и обычно нежелательна из-за детализации или блокировки результатов.</span><span class="sxs-lookup"><span data-stu-id="2cbf7-112">The simplest scheme is simply to have the sampler return the color of the closest texel; this is called Point filtering (see [Nearest-Point Sampling (Direct3D 9)](nearest-point-sampling.md)), and is usually undesirable due to grainy or blocky results.</span></span> <span data-ttu-id="2cbf7-113">Точечная выборка нашей текстуры в точке UV (0,25, 0,25) показывает еще одну скрытую проблему с фильтрацией по ближайшим точкам: в этой точке четыре равноудаленных от точки выборки текселя, поэтому выбрать один ближайший тексель невозможно.</span><span class="sxs-lookup"><span data-stu-id="2cbf7-113">Point-sampling our texture at UV (0.25, 0.25) shows another subtle problem with nearest-point filtering: there are four texels equidistant from the sampling point, so there's no single nearest texel.</span></span> <span data-ttu-id="2cbf7-114">Один из этих четырех текселей будет выбран в качестве возвращенного цвета, однако выбор зависит от округления координаты, а это, в свою очередь, может привести к разрывам артефактов (см. статью "Выборка с ближайших точек" в SDK).</span><span class="sxs-lookup"><span data-stu-id="2cbf7-114">One of those four texels will be chosen as the returned color, but the selection depends on how the coordinate is rounded, which may introduce tearing artifacts (see the Nearest-Point Sampling article in the SDK).</span></span>

<span data-ttu-id="2cbf7-115">Немного более точной и более распространенной схемой фильтрации является вычисление взвешенного среднего из 4 пикселей текстуры, ближайшего к точке выборки; Это называется билинейной фильтрацией, а дополнительные вычислительные затраты обычно незначительны, поскольку эта подпрограмма реализована в современных графических устройствах.</span><span class="sxs-lookup"><span data-stu-id="2cbf7-115">A slightly more accurate and more common filtering scheme is to calculate the weighted average of the 4 texels closest to the sampling point; this is called Bilinear filtering, and the extra computational cost is usually negligible because this routine is implemented in modern graphics hardware.</span></span> <span data-ttu-id="2cbf7-116">Вот какие цвета мы получим в разных точках выборки, используя билинейную фильтрацию:</span><span class="sxs-lookup"><span data-stu-id="2cbf7-116">Here are the colors we get at a few different sample points using bilinear filtering:</span></span>


```
UV: (0.5, 0.5)
```



<span data-ttu-id="2cbf7-117">Эта точка находится точно на границе между красным, зеленым, синим и белым текселями.</span><span class="sxs-lookup"><span data-stu-id="2cbf7-117">This point is at the exact border between red, green, blue, and white texels.</span></span> <span data-ttu-id="2cbf7-118">Инструмент "пипетка" возвращает серый цвет:</span><span class="sxs-lookup"><span data-stu-id="2cbf7-118">The color the sampler returns is gray:</span></span>


```
  0.25 * (255, 0, 0)
  0.25 * (0, 255, 0) 
  0.25 * (0, 0, 255) 
## + 0.25 * (255, 255, 255) 
------------------------
= (128, 128, 128)
```




```
UV: (0.5, 0.375)
```



<span data-ttu-id="2cbf7-119">Эта точка находится в середине границы между красным и зеленым текселями.</span><span class="sxs-lookup"><span data-stu-id="2cbf7-119">This point is at the midpoint of the border between red and green texels.</span></span> <span data-ttu-id="2cbf7-120">Пипетка возвращает желто-серый цвет (обратите внимание, что влияние синего и белого текселей равно 0):</span><span class="sxs-lookup"><span data-stu-id="2cbf7-120">The color the sampler returns is yellow-gray (note that the contributions of the blue and white texels are scaled to 0):</span></span>


```
  0.5 * (255, 0, 0)
  0.5 * (0, 255, 0) 
  0.0 * (0, 0, 255) 
## + 0.0 * (255, 255, 255) 
------------------------
= (128, 128, 0)
```




```
UV: (0.375, 0.375)
```



<span data-ttu-id="2cbf7-121">это адрес красного текселя, возвращенного цвета (все остальные тексели в вычислении фильтрации имеют нулевой вес):</span><span class="sxs-lookup"><span data-stu-id="2cbf7-121">This is the address of the red texel, which is the returned color (all other texels in the filtering calculation are weighted to 0):</span></span>


```
  1.0 * (255, 0, 0)
  0.0 * (0, 255, 0) 
  0.0 * (0, 0, 255) 
## + 0.0 * (255, 255, 255) 
------------------------
= (255, 0, 0)
```



<span data-ttu-id="2cbf7-122">Сравните эти вычисления на следующем рисунке, который показывает, что произойдет, если вычисление билинейной фильтрации выполняется в каждом адресе текстуры 4x4.</span><span class="sxs-lookup"><span data-stu-id="2cbf7-122">Compare these calculations against the following illustration, which shows what happens if the bilinear filtering calculation is performed at every texture address across the 4x4 texture.</span></span>

![иллюстрация текстуры 4x4 с выполненной в каждом адресе текстуры билинейной фильтрацией](images/bilinear-fig7c.jpg)

## <a name="related-topics"></a><span data-ttu-id="2cbf7-124">См. также</span><span class="sxs-lookup"><span data-stu-id="2cbf7-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2cbf7-125">Фильтрация текстур</span><span class="sxs-lookup"><span data-stu-id="2cbf7-125">Texture Filtering</span></span>](texture-filtering.md)
</dt> </dl>

 

 



