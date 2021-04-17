---
description: Шейдер, который вызывается, если пересечения лучей не являются непрозрачными.
ms.assetid: ''
title: Шейдер любых попаданий
ms.date: 05/31/2018
ms.topic: reference
ms.localizationpriority: low
topic_type:
- APIRef
- kbSyntax
api_name:
- RAY_FLAG
api_type:
- NA
ms.openlocfilehash: aad2f8b94f6ea53d500d285cac3555f5ff8b95f4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710721"
---
# <a name="any-hit-shader"></a><span data-ttu-id="4d317-103">Шейдер любых попаданий</span><span class="sxs-lookup"><span data-stu-id="4d317-103">Any Hit Shader</span></span>

<span data-ttu-id="4d317-104">Шейдер, который вызывается, если пересечения лучей не являются непрозрачными.</span><span class="sxs-lookup"><span data-stu-id="4d317-104">A shader that is invoked when ray intersections are not opaque.</span></span> 

<span data-ttu-id="4d317-105">Все шейдеры попадания должны объявлять параметр полезной нагрузки, за которым следует параметр attributes.</span><span class="sxs-lookup"><span data-stu-id="4d317-105">Any hit shaders must declare a payload parameter followed by an attributes parameter.</span></span> <span data-ttu-id="4d317-106">Каждый из этих параметров должен быть определяемым пользователем типом структуры, соответствующим типам, используемым для [**трацерай**](traceray-function.md) и [**репорсит**](reporthit-function.md) соответственно, или [**структурой атрибутов пересечения**](intersection-attributes.md) при использовании пересечения с нефиксированной функцией треугольника.</span><span class="sxs-lookup"><span data-stu-id="4d317-106">Each of these parameters must be a user-defined structure type matching types used for [**TraceRay**](traceray-function.md) and [**ReportHit**](reporthit-function.md) respectively, or the [**Intersection Attributes Structure**](intersection-attributes.md) when fixed function triangle intersection is used.</span></span>

<span data-ttu-id="4d317-107">Любые шейдеры попадания могут выполнять следующие виды операций:</span><span class="sxs-lookup"><span data-stu-id="4d317-107">Any hit shaders may perform the following kinds of operations:</span></span>

*   <span data-ttu-id="4d317-108">Чтение и изменение полезных данных луча: (InOut payload_t Райпайлоад)</span><span class="sxs-lookup"><span data-stu-id="4d317-108">Read and modify the ray payload: (inout payload_t rayPayload)</span></span>
*   <span data-ttu-id="4d317-109">Чтение атрибутов пересечения: (в атрибутах attr_t)</span><span class="sxs-lookup"><span data-stu-id="4d317-109">Read the intersection attributes: (in attr_t attributes)</span></span>
*   <span data-ttu-id="4d317-110">Вызовите метод [**акцепситандендсеарч**](accepthitandendsearch-function.md), который принимает текущее попадание, завершает [любой шейдер попадания](any-hit-shader.md), завершает [шейдер пересечения](intersection-shader.md) , если он имеется, и выполняет [ближайший построитель текстуры](closest-hit-shader.md) на ближайшее попадание, если оно активно.</span><span class="sxs-lookup"><span data-stu-id="4d317-110">Call [**AcceptHitAndEndSearch**](accepthitandendsearch-function.md), which accepts the current hit, ends the [any hit shader](any-hit-shader.md), ends the [intersection shader](intersection-shader.md) if one is present, and executes the [closest hit shader](closest-hit-shader.md) on the closest hit so far if it is active.</span></span>
*   <span data-ttu-id="4d317-111">Вызовите [**игнорехит**](ignorehit-function.md), который завершает любой шейдер попадания и сообщает системе, что будет продолжать поиск попаданий, включая возврат управления шейдеру пересечения, если он выполняется в данный момент, возвращая значение false из сайта вызова [**репорсит**](reporthit-function.md)\*.</span><span class="sxs-lookup"><span data-stu-id="4d317-111">Call [**IgnoreHit**](ignorehit-function.md), which ends the any hit shader and tells the system to continue searching for hits, including returning control to an intersection shader, if it is currently executing, returning false from the [**ReportHit**](reporthit-function.md)\* call site.</span></span> 
*   <span data-ttu-id="4d317-112">Возвращает, не вызывая ни одну из этих встроенных функций, которая принимает текущее попадание и сообщает системе о необходимости продолжения поиска попаданий, включая возврат управления шейдеру пересечения, если таковой имеется, возвращая значение true на веб-сайте [**репорсит**](reporthit-function.md) Call, чтобы указать, что попадание было принято.</span><span class="sxs-lookup"><span data-stu-id="4d317-112">Return without calling either of these intrinsics, which accepts the current hit and tells the system to continue searching for hits, including returning control to the intersection shader if there is one, returning true at the [**ReportHit**](reporthit-function.md) call site to indicate that the hit was accepted.</span></span>

<span data-ttu-id="4d317-113">Даже при завершении любого вызова шейдера нажатием [**игнорехит**](ignorehit-function.md) или [**акцепситандендсеарч**](accepthitandendsearch-function.md)любые изменения, внесенные в полезные данные лучей, пока все еще должны быть сохранены.</span><span class="sxs-lookup"><span data-stu-id="4d317-113">Even if an any hit shader invocation is ended by [**IgnoreHit**](ignorehit-function.md) or [**AcceptHitAndEndSearch**](accepthitandendsearch-function.md), any modifications made to the ray payload so far must still be retained.</span></span>

## <a name="shader-type-attribute"></a><span data-ttu-id="4d317-114">Атрибут типа шейдера</span><span class="sxs-lookup"><span data-stu-id="4d317-114">Shader Type attribute</span></span>

```
[shader("anyhit")]
```

## <a name="example"></a><span data-ttu-id="4d317-115">Пример</span><span class="sxs-lookup"><span data-stu-id="4d317-115">Example</span></span>

```
[shader("anyhit")]
void anyhit_main( inout MyPayload payload, in MyAttributes attr )
{
    float3 hitLocation = ObjectRayOrigin() + ObjectRayDirection() * RayTCurrent();
    float alpha = computeAlpha(hitLocation, attr, ...);

    // Processing shadow and only care if a hit is registered?
    if (TerminateShadowRay(alpha))
        AcceptHitAndEndSearch(); // aborts function

    // Save alpha contribution and ignoring hit?
    if (SaveAndIgnore(payload, RayTCurrent(), alpha, attr, ...))
        IgnoreHit(); // aborts function

    // do something else
    // return to accept and update closest hit
}
```
