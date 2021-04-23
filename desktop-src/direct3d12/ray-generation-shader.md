---
description: Шейдер, который вызывает Трацерай для создания лучей.
ms.assetid: ''
title: Шейдер создания лучей
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RAY_FLAG
api_type:
- NA
ms.openlocfilehash: 75d67293e489eee0f1d100002965c017de7c682c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701289"
---
# <a name="ray-generation-shader"></a><span data-ttu-id="16d38-103">Шейдер создания лучей</span><span class="sxs-lookup"><span data-stu-id="16d38-103">Ray Generation Shader</span></span>

<span data-ttu-id="16d38-104">Шейдер, который вызывает [**трацерай**](traceray-function.md) для создания лучей.</span><span class="sxs-lookup"><span data-stu-id="16d38-104">A shader that calls [**TraceRay**](traceray-function.md) to generate rays.</span></span> <span data-ttu-id="16d38-105">Начальные пользовательские полезные данные лучей для каждого луча предоставляются на сайт вызова **трацерай** .</span><span class="sxs-lookup"><span data-stu-id="16d38-105">The initial user-defined ray payload for each ray is provided to the **TraceRay** call site.</span></span>  <span data-ttu-id="16d38-106">[**Каллшадер**](callshader-function.md) также можно использовать в шейдерах создания лучей для вызова [вызываемых шейдеров](callable-shader.md).</span><span class="sxs-lookup"><span data-stu-id="16d38-106">[**CallShader**](callshader-function.md) may also be used in ray generation shaders to invoke [callable shaders](callable-shader.md).</span></span>

<span data-ttu-id="16d38-107">**Диспатчрайс** вызывает сетку вызовов шейдера создания лучей.</span><span class="sxs-lookup"><span data-stu-id="16d38-107">**DispatchRays** invokes a grid of ray generation shader invocations.</span></span>  <span data-ttu-id="16d38-108">Каждый вызов (поток) шейдера создания лучей знает его расположение в общей сетке, может создавать произвольные лучи через [**трацерай**](traceray-function.md)и работать независимо от других вызовов.</span><span class="sxs-lookup"><span data-stu-id="16d38-108">Each invocation (thread) of a ray generation shader knows its location in the overall grid, can generate arbitrary rays via [**TraceRay**](traceray-function.md), and operates independently of other invocations.</span></span> <span data-ttu-id="16d38-109">Не существует определенного порядка выполнения потоков по отношению друг к другу.</span><span class="sxs-lookup"><span data-stu-id="16d38-109">There is no defined order of execution of threads with respect to each other.</span></span>

## <a name="shader-type-attribute"></a><span data-ttu-id="16d38-110">Атрибут типа шейдера</span><span class="sxs-lookup"><span data-stu-id="16d38-110">Shader Type attribute</span></span>


```
[shader("raygeneration")]
```



## <a name="example"></a><span data-ttu-id="16d38-111">Пример</span><span class="sxs-lookup"><span data-stu-id="16d38-111">Example</span></span>

```
struct SceneConstantStructure { ... };
ConstantBuffer<SceneConstantStructure> SceneConstants;
RaytracingAccelerationStructure MyAccelerationStructure : register(t3);
struct MyPayload { ... };

[shader("raygeneration")]
void raygen_main()
{
    RayDesc myRay = {
        SceneConstants.CameraOrigin,
        SceneConstants.TMin,
        computeRayDirection(SceneConstants.LensParams, DispatchRaysIndex(), 
                            DispatchRaysDimensions()),
        SceneConstants.TMax};
    MyPayload payload = { ... };    // init payload
    TraceRay(
        MyAccelerationStructure,
        SceneConstants.RayFlags,
        SceneConstants.InstanceInclusionMask,
        SceneConstants.RayContributionToHitGroupIndex,
        SceneConstants.MultiplierForGeometryContributionToHitGroupIndex,
        SceneConstants.MissShaderIndex,
        myRay,
        payload);
    WriteFinalPixel(DispatchRaysIndex(), payload);
}
```

 

 




