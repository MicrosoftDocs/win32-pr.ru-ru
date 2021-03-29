---
description: Определяет исправление для элемента управления «B&\# 233; Безье». Массив определяет контрольные точки для исправления.
ms.assetid: vs|directx_sdk|~\patch.htm
title: Обновление
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 480457b3dd3800aca8b23210e3fe653b4e713e94
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103894090"
---
# <a name="patch"></a><span data-ttu-id="4442c-104">Обновление</span><span class="sxs-lookup"><span data-stu-id="4442c-104">Patch</span></span>

<span data-ttu-id="4442c-105">Определяет исправление элемента управления Безье.</span><span class="sxs-lookup"><span data-stu-id="4442c-105">Defines a Bézier control patch.</span></span> <span data-ttu-id="4442c-106">Массив определяет контрольные точки для исправления.</span><span class="sxs-lookup"><span data-stu-id="4442c-106">The array defines the control points for the patch.</span></span>

``` syntax
template Patch
{
    < A3EB5D44-FC22-429D-9AFB-3221CB9719A6 >
    DWORD nControlIndices;
    array DWORD controlIndices[nControlIndices];
} 
```

<span data-ttu-id="4442c-107">Где:</span><span class="sxs-lookup"><span data-stu-id="4442c-107">Where:</span></span>

-   <span data-ttu-id="4442c-108">Нконтролиндицес — число индексов контрольных точек.</span><span class="sxs-lookup"><span data-stu-id="4442c-108">nControlIndices - Number of control point indices.</span></span>
-   <span data-ttu-id="4442c-109">массив DWORD Контролиндицес \[ нконтролиндицес \] -массив индексов контрольных точек.</span><span class="sxs-lookup"><span data-stu-id="4442c-109">array DWORD controlIndices\[nControlIndices\] - Array of control point indices.</span></span>

<span data-ttu-id="4442c-110">Тип исправления определяется количеством контрольных точек, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="4442c-110">The type of patch is defined by the number of control points, as shown in the following table.</span></span>



| <span data-ttu-id="4442c-111">Число контрольных точек</span><span class="sxs-lookup"><span data-stu-id="4442c-111">Number of control points</span></span> | <span data-ttu-id="4442c-112">Тип</span><span class="sxs-lookup"><span data-stu-id="4442c-112">Type</span></span>                              |
|--------------------------|-----------------------------------|
| <span data-ttu-id="4442c-113">10</span><span class="sxs-lookup"><span data-stu-id="4442c-113">10</span></span>                       | <span data-ttu-id="4442c-114">Треугольное исправление Безье третьего порядка</span><span class="sxs-lookup"><span data-stu-id="4442c-114">Cubic Bézier triangular patch</span></span>     |
| <span data-ttu-id="4442c-115">15</span><span class="sxs-lookup"><span data-stu-id="4442c-115">15</span></span>                       | <span data-ttu-id="4442c-116">Треугольное исправление для Безье</span><span class="sxs-lookup"><span data-stu-id="4442c-116">Quartic Bézier triangular patch</span></span>   |
| <span data-ttu-id="4442c-117">16</span><span class="sxs-lookup"><span data-stu-id="4442c-117">16</span></span>                       | <span data-ttu-id="4442c-118">Исправление для четырехъядерного прямоугольника Безье третьего порядка</span><span class="sxs-lookup"><span data-stu-id="4442c-118">Cubic Bézier quad rectangle patch</span></span> |



 

<span data-ttu-id="4442c-119">Порядок контрольных точек задается в шаблоне «спираль», как показано на следующих диаграммах для треугольных и прямоугольных исправлений.</span><span class="sxs-lookup"><span data-stu-id="4442c-119">The order of the control points are given in a spiral pattern, as shown in the following diagrams for triangular and rectangular patches.</span></span>

<span data-ttu-id="4442c-120">Треугольные исправления используют следующий шаблон.</span><span class="sxs-lookup"><span data-stu-id="4442c-120">Triangular patches use the following pattern.</span></span>

![Схема шаблона для треугольных исправлений](images/tripatch.png)

<span data-ttu-id="4442c-122">В прямоугольных исправлениях используется следующий шаблон.</span><span class="sxs-lookup"><span data-stu-id="4442c-122">Rectangular patches use the following pattern.</span></span>

![Схема шаблона для прямоугольных исправлений](images/quadpatch.png)

## <a name="see-also"></a><span data-ttu-id="4442c-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4442c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4442c-125">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="4442c-125">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



