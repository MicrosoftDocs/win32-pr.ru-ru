---
description: Значения ширины, высоты и глубины из структуры D3D12_DISPATCH_RAYS_DESC, указанной в исходном вызове Диспатчрайс.
ms.assetid: ''
title: DispatchRaysDimensions
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DispatchRaysDimensions
api_type:
- NA
ms.openlocfilehash: e35c967ad831c82912d2962da72d9ad17eab1c15
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701292"
---
# <a name="dispatchraysdimensions"></a><span data-ttu-id="3abc7-103">DispatchRaysDimensions</span><span class="sxs-lookup"><span data-stu-id="3abc7-103">DispatchRaysDimensions</span></span>

<span data-ttu-id="3abc7-104">Значения ширины, высоты и глубины из структуры **\_ \_ \_ DESC D3D12 диспетчеризации** , указанной в исходном вызове [**диспатчрайс**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-dispatchrays) .</span><span class="sxs-lookup"><span data-stu-id="3abc7-104">The width, height and depth values from the **D3D12\_DISPATCH\_RAYS\_DESC** structure specified in the originating [**DispatchRays**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-dispatchrays) call.</span></span>

## <a name="syntax"></a><span data-ttu-id="3abc7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3abc7-105">Syntax</span></span>

```
uint3 DispatchRaysDimensions();
```

## <a name="remarks"></a><span data-ttu-id="3abc7-106">Примечания</span><span class="sxs-lookup"><span data-stu-id="3abc7-106">Remarks</span></span>

<span data-ttu-id="3abc7-107">Эту функцию можно вызывать из следующих типов шейдеров райтраЦинг:</span><span class="sxs-lookup"><span data-stu-id="3abc7-107">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="3abc7-108">**Шейдер любых попаданий**</span><span class="sxs-lookup"><span data-stu-id="3abc7-108">**Any Hit Shader**</span></span>](any-hit-shader.md)
* [<span data-ttu-id="3abc7-109">**Вызываемый шейдер**</span><span class="sxs-lookup"><span data-stu-id="3abc7-109">**Callable Shader**</span></span>](callable-shader.md)
* [<span data-ttu-id="3abc7-110">**Шейдер ближайшего попадания**</span><span class="sxs-lookup"><span data-stu-id="3abc7-110">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="3abc7-111">**Шейдер пересечения**</span><span class="sxs-lookup"><span data-stu-id="3abc7-111">**Intersection Shader**</span></span>](intersection-shader.md)
* [<span data-ttu-id="3abc7-112">**Шейдер непопаданий**</span><span class="sxs-lookup"><span data-stu-id="3abc7-112">**Miss Shader**</span></span>](miss-shader.md)
* [<span data-ttu-id="3abc7-113">**Шейдер создания лучей**</span><span class="sxs-lookup"><span data-stu-id="3abc7-113">**Ray Generation Shader**</span></span>](ray-generation-shader.md)

## <a name="see-also"></a><span data-ttu-id="3abc7-114">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3abc7-114">See also</span></span>

* [<span data-ttu-id="3abc7-115">Справочник по HLSL для трассировки лучей в Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="3abc7-115">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
