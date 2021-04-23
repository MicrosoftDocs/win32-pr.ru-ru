---
description: Описывает пересечение лучей-треугольника.
ms.assetid: 21658b74-6f1d-4a16-a8b3-0c7bb6edf899
title: Структура D3DX10_INTERSECT_INFO (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_INTERSECT_INFO
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: 87490e734299cba57952bb43d1ee4ffad8e014c8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821173"
---
# <a name="d3dx10_intersect_info-structure"></a><span data-ttu-id="ac233-103">\_ \_ Структура сведений о ПЕРЕСЕЧЕНии D3DX10</span><span class="sxs-lookup"><span data-stu-id="ac233-103">D3DX10\_INTERSECT\_INFO structure</span></span>

<span data-ttu-id="ac233-104">Описывает пересечение лучей-треугольника.</span><span class="sxs-lookup"><span data-stu-id="ac233-104">Describes a ray-triangle intersection.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac233-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ac233-105">Syntax</span></span>


```C++
typedef struct D3DX10_INTERSECT_INFO {
  UINT  FaceIndex;
  FLOAT U;
  FLOAT V;
  FLOAT Dist;
} D3DX10_INTERSECT_INFO, *LPD3DX10_INTERSECT_INFO;
```



## <a name="members"></a><span data-ttu-id="ac233-106">Члены</span><span class="sxs-lookup"><span data-stu-id="ac233-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ac233-107">**фацеиндекс**</span><span class="sxs-lookup"><span data-stu-id="ac233-107">**FaceIndex**</span></span>
</dt> <dd>

<span data-ttu-id="ac233-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ac233-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ac233-109">Индекс треугольника, который попадают на луч.</span><span class="sxs-lookup"><span data-stu-id="ac233-109">Index of the triangle that hit the ray.</span></span>

</dd> <dt>

<span data-ttu-id="ac233-110">**U**</span><span class="sxs-lookup"><span data-stu-id="ac233-110">**U**</span></span>
</dt> <dd>

<span data-ttu-id="ac233-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ac233-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ac233-112">Координата барицентрик в пределах треугольника, на котором пересекается луч.</span><span class="sxs-lookup"><span data-stu-id="ac233-112">Barycentric coordinate within the triangle where the ray intersects.</span></span>

</dd> <dt>

<span data-ttu-id="ac233-113">**V**</span><span class="sxs-lookup"><span data-stu-id="ac233-113">**V**</span></span>
</dt> <dd>

<span data-ttu-id="ac233-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ac233-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ac233-115">Координата барицентрик в пределах треугольника, на котором пересекается луч.</span><span class="sxs-lookup"><span data-stu-id="ac233-115">Barycentric coordinate within the triangle where the ray intersects.</span></span>

</dd> <dt>

<span data-ttu-id="ac233-116">**Файле**</span><span class="sxs-lookup"><span data-stu-id="ac233-116">**Dist**</span></span>
</dt> <dd>

<span data-ttu-id="ac233-117">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ac233-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ac233-118">Расстояние вдоль луча, где произошло пересечение.</span><span class="sxs-lookup"><span data-stu-id="ac233-118">Distance along the ray where the intersection occurred.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ac233-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ac233-119">Remarks</span></span>

<span data-ttu-id="ac233-120">Координаты барицентрик определяют точку внутри треугольника с точки зрения вершин треугольника.</span><span class="sxs-lookup"><span data-stu-id="ac233-120">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="ac233-121">Более подробное описание координат барицентрик см. в разделе [Описание координат Барицентрик MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="ac233-121">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="ac233-122">Требования</span><span class="sxs-lookup"><span data-stu-id="ac233-122">Requirements</span></span>



| <span data-ttu-id="ac233-123">Требование</span><span class="sxs-lookup"><span data-stu-id="ac233-123">Requirement</span></span> | <span data-ttu-id="ac233-124">Значение</span><span class="sxs-lookup"><span data-stu-id="ac233-124">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ac233-125">Header</span><span class="sxs-lookup"><span data-stu-id="ac233-125">Header</span></span><br/> | <dl> <span data-ttu-id="ac233-126"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac233-126"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac233-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ac233-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac233-128">Структуры D3DX</span><span class="sxs-lookup"><span data-stu-id="ac233-128">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
