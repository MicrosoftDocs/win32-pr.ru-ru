---
title: Шейдеры HLSL для трассировки лучей в Direct3D 12
description: Следующие Шейдеры HLSL поддерживают конвейер Direct3D 12 райтраЦинг.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe1dd545532208095781f6fbca25480a6dbfd31e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "105647133"
---
# <a name="direct3d-12-raytracing-hlsl-shaders"></a><span data-ttu-id="97e2c-103">Шейдеры HLSL для трассировки лучей в Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="97e2c-103">Direct3D 12 Raytracing HLSL Shaders</span></span>

<span data-ttu-id="97e2c-104">Следующие Шейдеры HLSL поддерживают конвейер Direct3D 12 райтраЦинг.</span><span class="sxs-lookup"><span data-stu-id="97e2c-104">The following HLSL shaders support the Direct3D 12 raytracing pipeline.</span></span> <span data-ttu-id="97e2c-105">Эти шейдеры — это функции, компилируемые в библиотеку с целевой моделью lib_6_3 и определяемые атрибутом *[шейдер ("шадертипе")]* в функции шейдера.</span><span class="sxs-lookup"><span data-stu-id="97e2c-105">These shaders are functions compiled into a library, with target model lib_6_3, and identified by an attribute *[shader("shadertype")]* on the shader function.</span></span> <span data-ttu-id="97e2c-106">См. раздел **встроенные функции** и **системные значения** , чтобы увидеть, что разрешено для каждого типа шейдера.</span><span class="sxs-lookup"><span data-stu-id="97e2c-106">See **Intrinsics** and **System Values** to see what is allowed for each shader type.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="97e2c-107">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="97e2c-107">In this section</span></span>



| <span data-ttu-id="97e2c-108">Раздел</span><span class="sxs-lookup"><span data-stu-id="97e2c-108">Topic</span></span>                                                                                                       | <span data-ttu-id="97e2c-109">Описание</span><span class="sxs-lookup"><span data-stu-id="97e2c-109">Description</span></span>                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="97e2c-110">**Шейдер любых попаданий**</span><span class="sxs-lookup"><span data-stu-id="97e2c-110">**Any Hit Shader**</span></span>](any-hit-shader.md)<br/>                              | <span data-ttu-id="97e2c-111">Шейдер, который вызывается, если пересечения лучей не являются непрозрачными.</span><span class="sxs-lookup"><span data-stu-id="97e2c-111">A shader that is invoked when ray intersections are not opaque.</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="97e2c-112">**Вызываемый шейдер**</span><span class="sxs-lookup"><span data-stu-id="97e2c-112">**Callable Shader**</span></span>](callable-shader.md)<br/>                              | <span data-ttu-id="97e2c-113">Шейдер, который вызывается из другого шейдера с встроенной функцией **каллшадер** .</span><span class="sxs-lookup"><span data-stu-id="97e2c-113">A shader that is invoked from another shader with the **CallShader** intrinsic.</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="97e2c-114">**Шейдер ближайшего попадания**</span><span class="sxs-lookup"><span data-stu-id="97e2c-114">**Closest Hit Shader**</span></span>](closest-hit-shader.md)<br/>                              | <span data-ttu-id="97e2c-115">Построитель текстуры, который вызывается, когда он включен, и было определено ближайшее попадание или закончено поиск пересечения лучей.</span><span class="sxs-lookup"><span data-stu-id="97e2c-115">A shader that is invoked when it is enabled and the closest hit has been determined or ray intersection search ended.</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="97e2c-116">**Шейдер пересечения**</span><span class="sxs-lookup"><span data-stu-id="97e2c-116">**Intersection Shader**</span></span>](intersection-shader.md)<br/>                              | <span data-ttu-id="97e2c-117">Шейдер, используемый для реализации пользовательских примитивов пересечения для луча, пересекающих связанный ограничивающий том (ограничивающий прямоугольник).</span><span class="sxs-lookup"><span data-stu-id="97e2c-117">A shader that is used to implement custom intersection primitives for rays intersecting an associated bounding volume (bounding box).</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="97e2c-118">**Шейдер непопаданий**</span><span class="sxs-lookup"><span data-stu-id="97e2c-118">**Miss Shader**</span></span>](miss-shader.md)<br/>                              | <span data-ttu-id="97e2c-119">Шейдер, который вызывается, когда ни один из пересечения лучей не найден или не принят.</span><span class="sxs-lookup"><span data-stu-id="97e2c-119">A shader that is invoked when no ray intersections are found or accepted.</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="97e2c-120">**Шейдер создания лучей**</span><span class="sxs-lookup"><span data-stu-id="97e2c-120">**Ray Generation Shader**</span></span>](ray-generation-shader.md)<br/>                              | <span data-ttu-id="97e2c-121">Шейдер, который вызывает [**трацерай**](traceray-function.md) для создания лучей.</span><span class="sxs-lookup"><span data-stu-id="97e2c-121">A shader that calls [**TraceRay**](traceray-function.md) to generate rays.</span></span><br/>                                                                                                                                                                                                                                              |

## <a name="related-topics"></a><span data-ttu-id="97e2c-122">См. также</span><span class="sxs-lookup"><span data-stu-id="97e2c-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97e2c-123">Справочник по основным</span><span class="sxs-lookup"><span data-stu-id="97e2c-123">Core Reference</span></span>](direct3d-12-core-reference.md)
</dt> <dt>

[<span data-ttu-id="97e2c-124">Справочник по Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="97e2c-124">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
</dt> </dl>

 

 





