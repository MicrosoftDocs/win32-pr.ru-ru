---
description: По умолчанию, когда в области отрисовки выполняется глубокое тестирование, система Direct3D обновляет поверхность целевого объекта рендеринга, если соответствующее значение глубины (z или w) для каждой точки меньше значения в буфере глубины.
ms.assetid: e9243c05-e943-4a42-ab73-e684900fc81d
title: Изменение функций сравнения буферов глубины (D3D9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7589ea0035376c6e73bcb70a73fcca3b913c9ecc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807948"
---
# <a name="changing-depth-buffer-comparison-functions-d3d9"></a><span data-ttu-id="09eb5-103">Изменение функций сравнения буферов глубины (D3D9)</span><span class="sxs-lookup"><span data-stu-id="09eb5-103">Changing Depth Buffer Comparison Functions (D3D9)</span></span>

<span data-ttu-id="09eb5-104">По умолчанию, когда в области отрисовки выполняется глубокое тестирование, система Direct3D обновляет поверхность целевого объекта рендеринга, если соответствующее значение глубины (z или w) для каждой точки меньше значения в буфере глубины.</span><span class="sxs-lookup"><span data-stu-id="09eb5-104">By default, when depth-testing is performed on a rendering surface, the Direct3D system updates the render-target surface if the corresponding depth value (z or w) for each point is less than the value in the depth buffer.</span></span> <span data-ttu-id="09eb5-105">В приложении C++ вы изменяете, как система выполняет сравнения значений глубины, вызывая метод [**IDirect3DDevice9:: сетрендерстате**](/windows/desktop/api) с параметром *State* , имеющим значение D3DRS \_ зфунк.</span><span class="sxs-lookup"><span data-stu-id="09eb5-105">In a C++ application, you change how the system performs comparisons on depth values by calling the [**IDirect3DDevice9::SetRenderState**](/windows/desktop/api) method with the *State* parameter set to D3DRS\_ZFUNC.</span></span> <span data-ttu-id="09eb5-106">Параметру *value* должно быть присвоено значение в перечислимом типе [**D3DCMPFUNC**](./d3dcmpfunc.md) .</span><span class="sxs-lookup"><span data-stu-id="09eb5-106">The *Value* parameter should be set to a value in the [**D3DCMPFUNC**](./d3dcmpfunc.md) enumerated type.</span></span>

## <a name="related-topics"></a><span data-ttu-id="09eb5-107">См. также</span><span class="sxs-lookup"><span data-stu-id="09eb5-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09eb5-108">Буферы глубины</span><span class="sxs-lookup"><span data-stu-id="09eb5-108">Depth Buffers</span></span>](depth-buffers.md)
</dt> </dl>

 

 
