---
title: Конвейер обработки OpenGL
description: Конвейер обработки OpenGL
ms.assetid: 98ac89d1-0d7b-45b2-8d6e-c421b9289d60
keywords:
- OpenGL, конвейер обработки
- Обработка конвейера с каналом OpenGL
- канал OpenGL
- фрамебуфферс, конвейер обработки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73d67447066b9d397bbb272932f51c6d3003f11e
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "104554924"
---
# <a name="opengl-processing-pipeline"></a><span data-ttu-id="b544d-107">Конвейер обработки OpenGL</span><span class="sxs-lookup"><span data-stu-id="b544d-107">OpenGL Processing Pipeline</span></span>

<span data-ttu-id="b544d-108">Многие функции OpenGL используются специально для рисования объектов, таких как точки, линии, многоугольники и точечные рисунки.</span><span class="sxs-lookup"><span data-stu-id="b544d-108">Many OpenGL functions are used specifically for drawing objects such as points, lines, polygons, and bitmaps.</span></span> <span data-ttu-id="b544d-109">Некоторые функции управляют способом выполнения некоторых из этих операций рисования (например, для включения сглаживания или текстурирования).</span><span class="sxs-lookup"><span data-stu-id="b544d-109">Some functions control the way that some of this drawing occurs (such as those that enable antialiasing or texturing).</span></span> <span data-ttu-id="b544d-110">Другие функции особенно связаны с буфера кадров манипуляцией.</span><span class="sxs-lookup"><span data-stu-id="b544d-110">Other functions are specifically concerned with framebuffer manipulation.</span></span> <span data-ttu-id="b544d-111">В подразделах этого раздела описывается, как все функции OpenGL работают вместе для создания конвейера обработки OpenGL.</span><span class="sxs-lookup"><span data-stu-id="b544d-111">The topics in this section describe how all of the OpenGL functions work together to create the OpenGL processing pipeline.</span></span> <span data-ttu-id="b544d-112">Этот раздел также подробно рассматривает этапы, в которых данные фактически обрабатываются, и привязывает эти этапы к функциям OpenGL.</span><span class="sxs-lookup"><span data-stu-id="b544d-112">This section also takes a closer look at the stages in which data is actually processed, and ties these stages to OpenGL functions.</span></span>

<span data-ttu-id="b544d-113">На следующей схеме подробно описывается конвейер обработки OpenGL.</span><span class="sxs-lookup"><span data-stu-id="b544d-113">The following diagram details the OpenGL processing pipeline.</span></span> <span data-ttu-id="b544d-114">Для большей части конвейера можно увидеть три вертикальные стрелки между основными этапами.</span><span class="sxs-lookup"><span data-stu-id="b544d-114">For most of the pipeline, you can see three vertical arrows between the major stages.</span></span> <span data-ttu-id="b544d-115">Эти стрелки представляют вершины и два основных типа данных, которые могут быть связаны с вершинами: значения цвета и координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="b544d-115">These arrows represent vertices and the two primary types of data that can be associated with vertices: color values and texture coordinates.</span></span> <span data-ttu-id="b544d-116">Также обратите внимание, что вершины собраны в примитивы, затем в фрагменты и, наконец, в Пиксели в буфера кадров.</span><span class="sxs-lookup"><span data-stu-id="b544d-116">Also note that vertices are assembled into primitives, then into fragments, and finally into pixels in the framebuffer.</span></span> <span data-ttu-id="b544d-117">Этот ход выполнения рассматривается более подробно в [вершинах](vertices.md), [примитивах](primitives.md), [фрагментах](fragments.md)и [пикселях](pixels.md).</span><span class="sxs-lookup"><span data-stu-id="b544d-117">This progression is discussed in more detail in [Vertices](vertices.md), [Primitives](primitives.md), [Fragments](fragments.md), and [Pixels](pixels.md).</span></span>

![Схема, показывающая конвейер обработки OpenGL.](images/proc01.png)

 

 




