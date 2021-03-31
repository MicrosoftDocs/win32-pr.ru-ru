---
title: Использование кривых и поверхностей НУРБС
description: Неоднородные рациональные функции B-сплайна (НУРБС) предоставляют общие и эффективные описания кривых и поверхностей в двух и трех измерениях, преобразуя кривые и поверхности в средства оценки OpenGL.
ms.assetid: 0b55659d-9fa2-47fc-ae15-0c296bd94dcb
keywords:
- Служебная программа OpenGL (GLU), неоднородный рациональный B-сплайн (НУРБС)
- GLU (служебная программа OpenGL), неоднородный рациональный B-сплайн (НУРБС)
- Неоднородный рациональный B-сплайн (НУРБС) OpenGL
- НУРБС (неоднородный рациональный B-сплайн) OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f85e9a2045c417007c34d714ae6635ebfaf1180
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329200"
---
# <a name="using-nurbs-curves-and-surfaces"></a><span data-ttu-id="15aff-107">Использование кривых и поверхностей НУРБС</span><span class="sxs-lookup"><span data-stu-id="15aff-107">Using NURBS Curves and Surfaces</span></span>

<span data-ttu-id="15aff-108">Неоднородные рациональные функции B-сплайна (НУРБС) предоставляют общие и эффективные описания кривых и поверхностей в двух и трех измерениях, преобразуя кривые и поверхности в средства оценки OpenGL.</span><span class="sxs-lookup"><span data-stu-id="15aff-108">Non-Uniform Rational B-Spline (NURBS) functions provide general and powerful descriptions of curves and surfaces in two and three dimensions, converting the curves and surfaces to OpenGL evaluators.</span></span> <span data-ttu-id="15aff-109">Функции НУРБС могут представлять геометрию во многих автоматизированных системах проектирования на основе компьютеров.</span><span class="sxs-lookup"><span data-stu-id="15aff-109">The NURBS functions can represent geometry in many computer-aided mechanical design systems.</span></span> <span data-ttu-id="15aff-110">Они могут отображать кривые и поверхностные типы в различных стилях, а также автоматически обрабатывать Адаптивное подразделение, которое разбивает домен на небольшие треугольники в регионах с высокой кривизной и близкими силуэт краями.</span><span class="sxs-lookup"><span data-stu-id="15aff-110">They can render curves and surfaces in a variety of styles, and they can automatically handle adaptive subdivision that tessellates the domain into smaller triangles in regions of high curvature and near silhouette edges.</span></span> <span data-ttu-id="15aff-111">Функции НУРБС делятся на следующие категории.</span><span class="sxs-lookup"><span data-stu-id="15aff-111">NURBS functions fall into the following categories.</span></span>

<span data-ttu-id="15aff-112">Для управления объектом НУРБС используйте:</span><span class="sxs-lookup"><span data-stu-id="15aff-112">To manage a NURBS object, use:</span></span>

-   <span data-ttu-id="15aff-113">[**глуневнурбсрендерер**](glunewnurbsrenderer.md) (создание объекта нурбс)</span><span class="sxs-lookup"><span data-stu-id="15aff-113">[**gluNewNurbsRenderer**](glunewnurbsrenderer.md) (create a NURBS object)</span></span>
-   <span data-ttu-id="15aff-114">[**глуделетенурбсрендерер**](gludeletenurbsrenderer.md) (удаление объекта нурбс)</span><span class="sxs-lookup"><span data-stu-id="15aff-114">[**gluDeleteNurbsRenderer**](gludeletenurbsrenderer.md) (deletes a NURBS object)</span></span>
-   <span data-ttu-id="15aff-115">[*глунурбскаллбакк*](glunurbs.md) (устанавливает функцию обработки ошибок)</span><span class="sxs-lookup"><span data-stu-id="15aff-115">[*gluNurbsCallback*](glunurbs.md) (establishes an error-handling function)</span></span>

<span data-ttu-id="15aff-116">Чтобы указать нужные кривые, используйте:</span><span class="sxs-lookup"><span data-stu-id="15aff-116">To specify the desired curves, use:</span></span>

-   [<span data-ttu-id="15aff-117">**глубегинкурве**</span><span class="sxs-lookup"><span data-stu-id="15aff-117">**gluBeginCurve**</span></span>](glubegincurve.md)
-   [<span data-ttu-id="15aff-118">**глунурбскурве**</span><span class="sxs-lookup"><span data-stu-id="15aff-118">**gluNurbsCurve**</span></span>](glunurbscurve.md)
-   [<span data-ttu-id="15aff-119">**глуендкурве**</span><span class="sxs-lookup"><span data-stu-id="15aff-119">**gluEndCurve**</span></span>](gluendcurve.md)

<span data-ttu-id="15aff-120">Чтобы указать нужные поверхности, используйте:</span><span class="sxs-lookup"><span data-stu-id="15aff-120">To specify the desired surfaces, use:</span></span>

-   [<span data-ttu-id="15aff-121">**глубегинсурфаце**</span><span class="sxs-lookup"><span data-stu-id="15aff-121">**gluBeginSurface**</span></span>](glubeginsurface.md)
-   [<span data-ttu-id="15aff-122">**глунурбссурфаце**</span><span class="sxs-lookup"><span data-stu-id="15aff-122">**gluNurbsSurface**</span></span>](glunurbssurface.md)
-   [<span data-ttu-id="15aff-123">**глуендсурфаце**</span><span class="sxs-lookup"><span data-stu-id="15aff-123">**gluEndSurface**</span></span>](gluendsurface.md)

<span data-ttu-id="15aff-124">Можно также указать область обрезки, которая определяет подмножество НУРБС домена Surface для оценки, чтобы можно было создавать поверхности с гладкими границами или содержать отверстия.</span><span class="sxs-lookup"><span data-stu-id="15aff-124">You can also specify a trimming region, which defines a subset of the NURBS surface domain to be evaluated so you can create surfaces that have smooth boundaries or that contain holes.</span></span>

<span data-ttu-id="15aff-125">Чтобы указать область обрезки, используйте:</span><span class="sxs-lookup"><span data-stu-id="15aff-125">To specify the trimming region, use:</span></span>

-   [<span data-ttu-id="15aff-126">**глубегинтрим**</span><span class="sxs-lookup"><span data-stu-id="15aff-126">**gluBeginTrim**</span></span>](glubegintrim.md)
-   [<span data-ttu-id="15aff-127">**глупвлкурве**</span><span class="sxs-lookup"><span data-stu-id="15aff-127">**gluPwlCurve**</span></span>](glupwlcurve.md)
-   [<span data-ttu-id="15aff-128">**глунурбскурве**</span><span class="sxs-lookup"><span data-stu-id="15aff-128">**gluNurbsCurve**</span></span>](glunurbscurve.md)
-   [<span data-ttu-id="15aff-129">**глуендтрим**</span><span class="sxs-lookup"><span data-stu-id="15aff-129">**gluEndTrim**</span></span>](gluendtrim.md)

<span data-ttu-id="15aff-130">Как и объекты куадрик, вы можете управлять визуализацией НУРБС кривых и поверхностей.</span><span class="sxs-lookup"><span data-stu-id="15aff-130">As with quadric objects, you can control how NURBS curves and surfaces are rendered.</span></span> <span data-ttu-id="15aff-131">Вы можете определить следующее:</span><span class="sxs-lookup"><span data-stu-id="15aff-131">You can determine:</span></span>

-   <span data-ttu-id="15aff-132">Следует ли отбросить кривую или поверхность, элемент управления которой многогранника находится за пределами текущего окна просмотра.</span><span class="sxs-lookup"><span data-stu-id="15aff-132">Whether to discard a curve or surface whose control polyhedron lies outside the current viewport.</span></span>
-   <span data-ttu-id="15aff-133">Максимальная длина (в пикселях) краев многоугольников, используемых для отрисовки кривых и поверхностей.</span><span class="sxs-lookup"><span data-stu-id="15aff-133">The maximum length (in pixels) of edges of polygons used to render curves and surfaces.</span></span>
-   <span data-ttu-id="15aff-134">Будет ли выбрана матрица проекции, моделвиевная матрица и окно просмотра с сервера OpenGL или предоставлены неявно с [**глулоадсамплингматрицес**](gluloadsamplingmatrices.md).</span><span class="sxs-lookup"><span data-stu-id="15aff-134">Whether you will take the projection matrix, modelview matrix, and viewport from the OpenGL server or supply them explictly with [**gluLoadSamplingMatrices**](gluloadsamplingmatrices.md).</span></span>

<span data-ttu-id="15aff-135">Используйте [**глунурбспроперти**](glunurbsproperty.md) для задания этих свойств или используйте значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="15aff-135">Use [**gluNurbsProperty**](glunurbsproperty.md) to set these properties, or use the default values.</span></span> <span data-ttu-id="15aff-136">Вы можете запросить объект НУРБС о своем стиле подготовки к просмотру с помощью [**глужетнурбспроперти**](glugetnurbsproperty.md).</span><span class="sxs-lookup"><span data-stu-id="15aff-136">You can query a NURBS object about its rendering style with [**gluGetNurbsProperty**](glugetnurbsproperty.md).</span></span>

 

 




