---
description: В режиме плоской заливки Следующая пирамида отображается с четким ребром между соседними лицами. Однако в режиме заливки Гуро значения заливки интерполируются на границе, а окончательный вид — на изогнутой поверхности.
ms.assetid: efcaf3f7-b474-4719-adde-10096e296b9f
title: Сравнение режимов заливки (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b275f18aa7283a8109db5d6709595cff0ddd09be
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142943"
---
# <a name="comparing-shading-modes-direct3d-9"></a><span data-ttu-id="5eeb2-104">Сравнение режимов заливки (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="5eeb2-104">Comparing Shading Modes (Direct3D 9)</span></span>

<span data-ttu-id="5eeb2-105">В режиме плоской заливки Следующая пирамида отображается с четким ребром между соседними лицами.</span><span class="sxs-lookup"><span data-stu-id="5eeb2-105">In flat shading mode, the following pyramid is displayed with a sharp edge between adjoining faces.</span></span> <span data-ttu-id="5eeb2-106">Однако в режиме заливки Гуро значения заливки интерполируются на границе, а окончательный вид — на изогнутой поверхности.</span><span class="sxs-lookup"><span data-stu-id="5eeb2-106">In Gouraud shading mode, however, shading values are interpolated across the edge, and the final appearance is of a curved surface.</span></span>

![Иллюстрация пирамиды с четкими краями и стрелками, указывающими на нормальную поверхность](images/shade2.png)

<span data-ttu-id="5eeb2-108">Заливка по методу Гуро охватывает плоские поверхности более реалистично, чем Плоская заливка.</span><span class="sxs-lookup"><span data-stu-id="5eeb2-108">Gouraud shading lights flat surfaces more realistically than flat shading.</span></span> <span data-ttu-id="5eeb2-109">Грань в режиме плоской заливки — это однородный цвет, но заливка по методу Гуро позволяет более правильно попадать в сторону.</span><span class="sxs-lookup"><span data-stu-id="5eeb2-109">A face in the flat shading mode is a uniform color, but Gouraud shading enables light to fall across a face more correctly.</span></span> <span data-ttu-id="5eeb2-110">Этот результат особенно заметен, если имеется источник точки поблизости.</span><span class="sxs-lookup"><span data-stu-id="5eeb2-110">This effect is particularly obvious if there is a nearby point source.</span></span>

<span data-ttu-id="5eeb2-111">Заливка по методу Гуро сглаживает четкие края многоугольников, которые видны с плоской заливкой.</span><span class="sxs-lookup"><span data-stu-id="5eeb2-111">Gouraud shading smoothes the sharp edges between polygons that are visible with flat shading.</span></span> <span data-ttu-id="5eeb2-112">Однако это может привести к созданию диапазонов машинного типа, которые являются полосами цветов или освещения, которые не смешиваются плавно в смежных многоугольниках.</span><span class="sxs-lookup"><span data-stu-id="5eeb2-112">However, it can result in mach bands, which are bands of color or light that are not smoothly blended across adjacent polygons.</span></span> <span data-ttu-id="5eeb2-113">Приложение может уменьшить внешний вид диапазонов, увеличивая количество многоугольников в объекте, увеличивая разрешение экрана или увеличивая глубину цвета приложения.</span><span class="sxs-lookup"><span data-stu-id="5eeb2-113">Your application can reduce the appearance of Mach bands by increasing the number of polygons in an object, increasing screen resolution, or increasing the color depth of the application.</span></span>

<span data-ttu-id="5eeb2-114">Заливка по методу Гуро может пропускать некоторые сведения.</span><span class="sxs-lookup"><span data-stu-id="5eeb2-114">Gouraud shading can miss some details.</span></span> <span data-ttu-id="5eeb2-115">Например, на следующем рисунке фокус полностью содержится в многоугольнике.</span><span class="sxs-lookup"><span data-stu-id="5eeb2-115">For example, in the following illustration, a spotlight is completely contained within a polygon face.</span></span>

![Иллюстрация прожектора в пределах многоугольника](images/gouraud.png)

<span data-ttu-id="5eeb2-117">В этом случае заливка по методу Гуро, которая выполняет интерполяцию между вершинами, полностью пропустила прожектор; грань будет отображаться, как будто прожектор не существовал.</span><span class="sxs-lookup"><span data-stu-id="5eeb2-117">In this case, Gouraud shading, which interpolates between vertices, would miss the spotlight altogether; the face would be rendered as though the spotlight did not exist.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5eeb2-118">См. также</span><span class="sxs-lookup"><span data-stu-id="5eeb2-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5eeb2-119">Заливка</span><span class="sxs-lookup"><span data-stu-id="5eeb2-119">Shading</span></span>](shading.md)
</dt> </dl>

 

 



