---
title: Перенос объектов НУРБС
description: OpenGL рассматривает НУРБС как объекты, аналогично тому, как он обрабатывает куадрикс создает объект НУРБС, а затем указывает, как он должен быть визуализирован. В следующей таблице перечислены функции OpenGL GLU для управления объектами НУРБС.
ms.assetid: baddf81b-219f-44bb-aa17-37404028b258
keywords:
- Перенос GL в ГК, объекты НУРБС
- Перенос из ДИАФРАГМы в ГК, объекты НУРБС
- перенос в OpenGL из IRI GL, объекты НУРБС
- Перенос по стандарту OpenGL из IRI GL, объекты НУРБС
- Объекты НУРБС
- НУРБС (неоднородный рациональный B-сплайн)
- Неоднородный рациональный B-сплайн (НУРБС)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e0e56c06eea4e4a9a48f9062205277f8b999499
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411125"
---
# <a name="porting-nurbs-objects"></a><span data-ttu-id="379bf-111">Перенос объектов НУРБС</span><span class="sxs-lookup"><span data-stu-id="379bf-111">Porting NURBS Objects</span></span>

<span data-ttu-id="379bf-112">OpenGL рассматривает НУРБС как объекты, аналогично тому, как он обрабатывает куадрикс: вы создаете объект НУРБС, а затем указываете, как он должен быть визуализирован.</span><span class="sxs-lookup"><span data-stu-id="379bf-112">OpenGL treats NURBS as objects, similar to the way it treats quadrics: you create a NURBS object and then specify how it should be rendered.</span></span> <span data-ttu-id="379bf-113">В следующей таблице перечислены функции OpenGL GLU для управления объектами НУРБС.</span><span class="sxs-lookup"><span data-stu-id="379bf-113">The following table lists the OpenGL GLU functions for managing NURBS objects.</span></span>



| <span data-ttu-id="379bf-114">Функция OpenGL GLU</span><span class="sxs-lookup"><span data-stu-id="379bf-114">OpenGL GLU function</span></span>                                      | <span data-ttu-id="379bf-115">Значение</span><span class="sxs-lookup"><span data-stu-id="379bf-115">Meaning</span></span>                                                        |
|----------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="379bf-116">**глуневнурбсрендерер**</span><span class="sxs-lookup"><span data-stu-id="379bf-116">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)       | <span data-ttu-id="379bf-117">Создает новый объект НУРБС.</span><span class="sxs-lookup"><span data-stu-id="379bf-117">Creates a new NURBS object.</span></span>                                    |
| [<span data-ttu-id="379bf-118">**глуделетенурбсрендерер**</span><span class="sxs-lookup"><span data-stu-id="379bf-118">**gluDeleteNurbsRenderer**</span></span>](gludeletenurbsrenderer.md) | <span data-ttu-id="379bf-119">Удаляет объект НУРБС.</span><span class="sxs-lookup"><span data-stu-id="379bf-119">Deletes a NURBS object.</span></span>                                        |
| [<span data-ttu-id="379bf-120">*глунурбскаллбакк*</span><span class="sxs-lookup"><span data-stu-id="379bf-120">*gluNurbsCallback*</span></span>](glunurbs.md)                       | <span data-ttu-id="379bf-121">Связывает обратный вызов с объектом НУРБС для обработки ошибок.</span><span class="sxs-lookup"><span data-stu-id="379bf-121">Associates a callback with a NURBS object, for error handling.</span></span> |



 

<span data-ttu-id="379bf-122">При переносе кода IRI GL НУРБС в OpenGL следует учитывать следующие моменты:</span><span class="sxs-lookup"><span data-stu-id="379bf-122">When porting IRIS GL NURBS code to OpenGL, keep the following points in mind:</span></span>

-   <span data-ttu-id="379bf-123">Точки управления НУРБС являются плавающими, а не Double.</span><span class="sxs-lookup"><span data-stu-id="379bf-123">NURBS control points are floats, not doubles.</span></span>
-   <span data-ttu-id="379bf-124">Параметр STRIDE учитывается в float, а не в байтах.</span><span class="sxs-lookup"><span data-stu-id="379bf-124">The stride parameter is counted in floats, not bytes.</span></span>
-   <span data-ttu-id="379bf-125">Если вы используете освещение и не указываете нормали, вызовите [**гленабле**](glenable.md) с \_ \_ параметром GL Auto нормали в качестве параметра для автоматического создания нормалей.</span><span class="sxs-lookup"><span data-stu-id="379bf-125">If you're using lighting and you're not specifying normals, call [**glEnable**](glenable.md) with GL\_AUTO\_NORMAL as the parameter to generate normals automatically.</span></span>

<span data-ttu-id="379bf-126">??</span><span class="sxs-lookup"><span data-stu-id="379bf-126">??</span></span>

 

 




