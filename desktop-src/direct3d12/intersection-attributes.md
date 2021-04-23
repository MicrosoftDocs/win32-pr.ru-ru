---
title: Структура атрибутов пересечения
description: Структура, объявленная в HLSL, представляющая атрибуты нажатия для пересечения треугольников с фиксированной функцией или ограничивающего прямоугольника, ориентированного на оси, для перекрестия процедурных примитивов.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: language-reference
ms.date: 05/31/2018
ms.openlocfilehash: b2f1dd8fee7371f81dd538b6ea6622f22e3bfd3d
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2021
ms.locfileid: "105713245"
---
# <a name="intersection-attributes-structure"></a><span data-ttu-id="63bb5-103">Структура атрибутов пересечения</span><span class="sxs-lookup"><span data-stu-id="63bb5-103">Intersection attributes structure</span></span> 

<span data-ttu-id="63bb5-104">Структура, объявленная в HLSL, представляющая атрибуты нажатия для пересечения треугольников с фиксированной функцией или ограничивающего прямоугольника, ориентированного на оси, для перекрестия процедурных примитивов.</span><span class="sxs-lookup"><span data-stu-id="63bb5-104">A structure declared in HLSL to represent hit attributes for fixed-function triangle intersection or axis-aligned bounding box for procedural primitive intersection.</span></span>

## <a name="fixed-function-triangle-intersection"></a><span data-ttu-id="63bb5-105">Пересечение треугольников с фиксированной функцией</span><span class="sxs-lookup"><span data-stu-id="63bb5-105">Fixed-function triangle intersection</span></span>

<span data-ttu-id="63bb5-106">Следующая структура объявляется в HLSL для представления атрибутов попадания для пересечения треугольников с фиксированной функцией.</span><span class="sxs-lookup"><span data-stu-id="63bb5-106">The following structure is declared in HLSL to represent hit attributes for fixed-function triangle intersection:</span></span>


```
struct BuiltInTriangleIntersectionAttributes
{
    float2 barycentrics;
};
```

<span data-ttu-id="63bb5-107">[Все попадания](any-hit-shader.md) и [ближайшие](closest-hit-shader.md) построители текстур, вызываемые с помощью перекрестной функции с использованием треугольника, должны использовать эту структуру для атрибутов попадания.</span><span class="sxs-lookup"><span data-stu-id="63bb5-107">[Any hit](any-hit-shader.md) and [closest hit](closest-hit-shader.md) shaders invoked using fixed-function triangle intersection must use this structure for hit attributes.</span></span> <span data-ttu-id="63bb5-108">Заданными атрибутами a0, a1 и a2 для 3 вершин треугольника барицентрикс. x — это вес a1 и барицентрикс. y — вес a2.</span><span class="sxs-lookup"><span data-stu-id="63bb5-108">Given attributes a0, a1 and a2 for the 3 vertices of a triangle, barycentrics.x is the weight for a1 and barycentrics.y is the weight for a2.</span></span>  <span data-ttu-id="63bb5-109">Например, приложение может выполнить интерполяцию: a = a0 + барицентрикс. x \* (a1-a0) + барицентрикс. y \* (a2 – a0).</span><span class="sxs-lookup"><span data-stu-id="63bb5-109">For example, the app can interpolate by doing:  a = a0 + barycentrics.x \* (a1-a0) + barycentrics.y\* (a2 – a0).</span></span>

## <a name="axis-aligned-bounding-box-for-procedural-primitive-intersection"></a><span data-ttu-id="63bb5-110">Ограничивающий прямоугольник с согласованием по осям для перекрестия процедурных примитивов</span><span class="sxs-lookup"><span data-stu-id="63bb5-110">Axis-aligned bounding box for procedural primitive intersection</span></span>

<span data-ttu-id="63bb5-111">Если ограничивающие прямоугольники, ориентированные по осям, используются для пересечений с помощью процедурных примитивов, активируется шейдер пересечения.</span><span class="sxs-lookup"><span data-stu-id="63bb5-111">When axis-aligned bounding boxes are used for intersection with procedural primitives, an intersection shader is triggered.</span></span>  <span data-ttu-id="63bb5-112">Этот шейдер предоставляет определяемую пользователем структуру атрибута пересечения с вызовом [**репорсит**](reporthit-function.md) .</span><span class="sxs-lookup"><span data-stu-id="63bb5-112">That shader provides a user-defined intersection attribute structure to the [**ReportHit**](reporthit-function.md) call.</span></span>  <span data-ttu-id="63bb5-113">Любые пограничные шейдеры, привязанные к одной группе нажатий с этим построителем пересечения, должны использовать ту же структуру для атрибутов попадания, даже если на эти атрибуты нет ссылок.</span><span class="sxs-lookup"><span data-stu-id="63bb5-113">The any hit and closest hit shaders bound in the same hit group with this intersection shader must use the same structure for hit attributes, even if the attributes are not referenced.</span></span>  <span data-ttu-id="63bb5-114">Максимальный размер структуры атрибута составляет 32 байт, определенный как **D3D12 \_ райтраЦинг \_ максимальный \_ Размер атрибута \_ \_ в \_ байтах**.</span><span class="sxs-lookup"><span data-stu-id="63bb5-114">The maximum attribute structure size is 32 bytes, defined as **D3D12\_RAYTRACING\_MAX\_ATTRIBUTE\_SIZE\_IN\_BYTES**.</span></span>


