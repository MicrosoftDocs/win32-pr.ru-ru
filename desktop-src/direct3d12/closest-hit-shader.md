---
description: Построитель текстуры, который вызывается, когда он включен, и было определено ближайшее попадание или закончено поиск пересечения лучей.
ms.assetid: ''
title: Шейдер ближайшего попадания
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
ms.openlocfilehash: 347ad66dce0a81b929d5dc3c82051bf84226e723
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710787"
---
# <a name="closest-hit-shader"></a><span data-ttu-id="e5115-103">Шейдер ближайшего попадания</span><span class="sxs-lookup"><span data-stu-id="e5115-103">Closest Hit Shader</span></span>

<span data-ttu-id="e5115-104">Построитель текстуры, который вызывается, когда он включен, и было определено ближайшее попадание или закончено поиск пересечения лучей.</span><span class="sxs-lookup"><span data-stu-id="e5115-104">A shader that is invoked when it is enabled and the closest hit has been determined or ray intersection search ended.</span></span> <span data-ttu-id="e5115-105">В этом шейдере, как правило, происходит заливка поверхности и дополнительное поколение лучей.</span><span class="sxs-lookup"><span data-stu-id="e5115-105">This shader is where surface shading and additional ray generation will typically occur.</span></span>  <span data-ttu-id="e5115-106">Ближайшие шейдеры попадания должны объявлять параметр полезной нагрузки, за которым следует параметр attributes.</span><span class="sxs-lookup"><span data-stu-id="e5115-106">Closest hit shaders must declare a payload parameter, followed by an attributes parameter.</span></span>  <span data-ttu-id="e5115-107">Каждый должен быть определяемым пользователем типом структуры, соответствующим типам, используемым для [**трацерай**](traceray-function.md) и [**репорсит**](reporthit-function.md) соответственно, или [**структурой атрибутов пересечения**](intersection-attributes.md) при использовании пересечения треугольника с фиксированной функцией.</span><span class="sxs-lookup"><span data-stu-id="e5115-107">Each must be a user-defined structure type matching types used for [**TraceRay**](traceray-function.md) and [**ReportHit**](reporthit-function.md) respectively, or the [**Intersection Attributes Structure**](intersection-attributes.md) when fixed-function triangle intersection is used.</span></span>

## <a name="shader-type-attribute"></a><span data-ttu-id="e5115-108">Атрибут типа шейдера</span><span class="sxs-lookup"><span data-stu-id="e5115-108">Shader Type attribute</span></span>


```
[shader("closesthit")]
```



## <a name="example"></a><span data-ttu-id="e5115-109">Пример</span><span class="sxs-lookup"><span data-stu-id="e5115-109">Example</span></span>

```
[shader("closesthit")]
void closesthit_main(inout MyPayload payload, in MyAttributes attr)
{
    CallShader( ... );  // maybe
    // update payload for surface
    // trace reflection
    float3 worldRayOrigin = WorldRayOrigin() + WorldRayDirection() * RayTCurrent();
    float3 worldNormal = mul(attr.normal, (float3x3)ObjectToWorld3x4());
    RayDesc reflectedRay = { worldRayOrigin, SceneConstants.Epsilon,
                             ReflectRay(WorldRayDirection(), worldNormal),
                             SceneConstants.TMax };
    TraceRay(MyAccelerationStructure,
             SceneConstants.RayFlags,
             SceneConstants.InstanceInclusionMask,
             SceneConstants.RayContributionToHitGroupIndex,
             SceneConstants.MultiplierForGeometryContributionToHitGroupIndex,
             SceneConstants.MissShaderIndex,
             reflectedRay,
             payload);
    // Combine final contributions into ray payload
    // this ray query is now complete.
    // Alternately, could look at data in payload result based on that make other TraceRay
    // calls.  No constraints on the code structure.
}

```

 

 




