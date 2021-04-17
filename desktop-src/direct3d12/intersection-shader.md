---
description: Шейдер, используемый для реализации пользовательских примитивов пересечения для луча, пересекающих связанный ограничивающий том (ограничивающий прямоугольник).
ms.assetid: ''
title: Шейдер пересечения
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
ms.openlocfilehash: f20d9ceb90b716ca5e5c04fb796a8b20f535825d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710797"
---
# <a name="intersection-shader"></a><span data-ttu-id="63183-103">Шейдер пересечения</span><span class="sxs-lookup"><span data-stu-id="63183-103">Intersection Shader</span></span>

<span data-ttu-id="63183-104">Шейдер, используемый для реализации пользовательских примитивов пересечения для луча, пересекающих связанный ограничивающий том (ограничивающий прямоугольник).</span><span class="sxs-lookup"><span data-stu-id="63183-104">A shader that is used to implement custom intersection primitives for rays intersecting an associated bounding volume (bounding box).</span></span> 

<span data-ttu-id="63183-105">Шейдер пересечения не имеет доступа к полезной нагрузке луча, но определяет атрибуты пересечения для каждого попадания через вызов [**репорсит**](reporthit-function.md).</span><span class="sxs-lookup"><span data-stu-id="63183-105">The intersection shader does not have access to the ray payload, but defines the intersection attributes for each hit through a call to [**ReportHit**](reporthit-function.md).</span></span>  <span data-ttu-id="63183-106">Обработка **репорсит** может помешать построителей шейдера на раннем этапе, если **флаг луча \_ \_ принимает \_ первый \_ HIT_ \анд \_ \енд \_ поиска** , или [**акцепситандендсеарч**](accepthitandendsearch-function.md) вызывается из любого шейдера нажатия.</span><span class="sxs-lookup"><span data-stu-id="63183-106">The handling of **ReportHit** may stop the intersection shader early, if the ray flag **RAY\_FLAG\_ACCEPT\_FIRST\_HIT_\AND\_\END\_SEARCH** is set, or [**AcceptHitAndEndSearch**](accepthitandendsearch-function.md) is called from an any hit shader.</span></span>  <span data-ttu-id="63183-107">В противном случае возвращается значение true, если попадание было принято, или значение false, если попадание было отклонено.</span><span class="sxs-lookup"><span data-stu-id="63183-107">Otherwise, it returns true if the hit was accepted or false if the hit was rejected.</span></span>  <span data-ttu-id="63183-108">Это означает, что любой шейдер нажатий, если он есть, должен выполняться до условного возврата управления в шейдер пересечения.</span><span class="sxs-lookup"><span data-stu-id="63183-108">This means that an any hit shader, if present, must execute before control conditionally returns to the intersection shader.</span></span>

## <a name="shader-type-attribute"></a><span data-ttu-id="63183-109">Атрибут типа шейдера</span><span class="sxs-lookup"><span data-stu-id="63183-109">Shader Type attribute</span></span>


```
[shader("intersection")]
```



## <a name="example"></a><span data-ttu-id="63183-110">Пример</span><span class="sxs-lookup"><span data-stu-id="63183-110">Example</span></span>

```
struct CustomPrimitiveDef { ... };
struct MyAttributes { ... };
struct CustomIntersectionIterator {...};
void InitCustomIntersectionIterator(CustomIntersectionIterator it) {...}
bool IntersectCustomPrimitiveFrontToBack(
    CustomPrimitiveDef prim,
    inout CustomIntersectionIterator it,
    float3 origin, float3 dir,
    float rayTMin, inout float curT,
    out MyAttributes attr);

[shader("intersection")]
void intersection_main()
{
    float THit = RayTCurrent();
    MyAttributes attr;
    CustomIntersectionIterator it;
    InitCustomIntersectionIterator(it); 
    while(IntersectCustomPrimitiveFrontToBack(
            CustomPrimitiveDefinitions[LocalConstants.PrimitiveIndex],
            it, ObjectRayOrigin(), ObjectRayDirection(), 
            RayTMin(), THit, attr))
    {
        // Exit on the first hit.  Note that if the ray has
        // RAY_FLAG_ACCEPT_FIRST_HIT_AND_END_SEARCH or an
        // anyhit shader is used and calls AcceptHitAndEndSearch(),
        // that would also fully exit this intersection shader (making
        // the “break” below moot in that case).        
        if (ReportHit(THit, /*hitKind*/ 0, attr) && (RayFlags() &  RAY_FLAG_FORCE_OPAQUE))
            break;
    }
}
```

 

 




