---
title: Использование оценивающих
description: Использование оценивающих
ms.assetid: a5a99d0a-526e-4492-90c4-a6b9fdbdff16
keywords:
- OpenGL, оценщики
- Оценщики OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1aef70a7a854e16cf4992d9dd44c4931ad4d044
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329203"
---
# <a name="using-evaluators"></a><span data-ttu-id="a22f1-105">Использование оценивающих</span><span class="sxs-lookup"><span data-stu-id="a22f1-105">Using Evaluators</span></span>

<span data-ttu-id="a22f1-106">Функции оценщика OpenGL позволяют использовать сопоставление полинома для создания вершин, нормалй, координат текстуры и цветов.</span><span class="sxs-lookup"><span data-stu-id="a22f1-106">The OpenGL evaluator functions allow you to use a polynomial mapping to produce vertices, normals, texture coordinates, and colors.</span></span> <span data-ttu-id="a22f1-107">Затем эти вычисляемые значения передаются в конвейер обработки, как если бы они были указаны непосредственно.</span><span class="sxs-lookup"><span data-stu-id="a22f1-107">These calculated values are then passed on to the processing pipeline as if they had been directly specified.</span></span> <span data-ttu-id="a22f1-108">Функции оценщика также являются основанием для функций НУРБС (неоднородного рационального B-сплайна), которые позволяют определять кривые и поверхности, как описано в разделе [библиотека служебной программы OpenGL](opengl-utility-library.md).</span><span class="sxs-lookup"><span data-stu-id="a22f1-108">The evaluator functions are also the basis for the NURBS (Non-Uniform Rational B-Spline) functions, which allow you to define curves and surfaces, as described under [OpenGL Utility library](opengl-utility-library.md).</span></span>

<span data-ttu-id="a22f1-109">Первым шагом при использовании оценивающих является определение соответствующего одномерного или двумерного сопоставлений с помощью [**глмап \***](glmap1.md).</span><span class="sxs-lookup"><span data-stu-id="a22f1-109">The first step in using evaluators is to define the appropriate one- or two-dimensional polynomial mapping using [**glMap\***](glmap1.md).</span></span> <span data-ttu-id="a22f1-110">Затем можно указать и оценить значения домена для этой схемы одним из двух способов:</span><span class="sxs-lookup"><span data-stu-id="a22f1-110">You can then specify and evaluate the domain values for this map in one of two ways:</span></span>

-   <span data-ttu-id="a22f1-111">Определите ряд равномерно пробельных значений домена, которые должны быть сопоставлены с помощью [**глмапгрид**](glmapgrid-functions.md) , а затем вычислите прямоугольное подмножество этой сетки с помощью [**глевалмеш**](glevalmesh-functions.md).</span><span class="sxs-lookup"><span data-stu-id="a22f1-111">Define a series of evenly spaced domain values to be mapped using [**glMapGrid**](glmapgrid-functions.md) and then evaluate a rectangular subset of that grid with [**glEvalMesh**](glevalmesh-functions.md).</span></span> <span data-ttu-id="a22f1-112">Единую точку сетки можно оценить с помощью [**глевалпоинт**](glevalpoint.md).</span><span class="sxs-lookup"><span data-stu-id="a22f1-112">A single point of the grid can be evaluated using [**glEvalPoint**](glevalpoint.md).</span></span>
-   <span data-ttu-id="a22f1-113">Явно укажите требуемое значение домена в качестве аргумента, который оценивает карты по этому значению.</span><span class="sxs-lookup"><span data-stu-id="a22f1-113">Explicitly specify a desired domain value as an argument, which evaluates the maps at that value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a22f1-114">См. также</span><span class="sxs-lookup"><span data-stu-id="a22f1-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a22f1-115">Справочник по оценщикам</span><span class="sxs-lookup"><span data-stu-id="a22f1-115">Evaluators Reference</span></span>](evaluators-reference.md)
</dt> </dl>

 

 




