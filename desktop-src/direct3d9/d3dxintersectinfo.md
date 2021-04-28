---
description: Структура D3DXINTERSECTINFO — описывает пересечение лучей-треугольника.
ms.assetid: b6f50fc0-2c8a-4efa-a144-bd0851f8b0ca
title: Структура D3DXINTERSECTINFO (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXINTERSECTINFO
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: f4a63c7f4a479bfbe9dcb49f485ce0acb8db6486
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098292"
---
# <a name="d3dxintersectinfo-structure"></a><span data-ttu-id="92be6-103">Структура D3DXINTERSECTINFO</span><span class="sxs-lookup"><span data-stu-id="92be6-103">D3DXINTERSECTINFO structure</span></span>

<span data-ttu-id="92be6-104">Описывает пересечение лучей-треугольника.</span><span class="sxs-lookup"><span data-stu-id="92be6-104">Describes a ray-triangle intersection.</span></span>

## <a name="syntax"></a><span data-ttu-id="92be6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="92be6-105">Syntax</span></span>


```C++
typedef struct D3DXINTERSECTINFO {
  DWORD FaceIndex;
  FLOAT U;
  FLOAT V;
  FLOAT Dist;
} D3DXINTERSECTINFO, *LPD3DXINTERSECTINFO;
```



## <a name="members"></a><span data-ttu-id="92be6-106">Члены</span><span class="sxs-lookup"><span data-stu-id="92be6-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="92be6-107">**фацеиндекс**</span><span class="sxs-lookup"><span data-stu-id="92be6-107">**FaceIndex**</span></span>
</dt> <dd>

<span data-ttu-id="92be6-108">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="92be6-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="92be6-109">Индекс треугольника, который попадают на луч.</span><span class="sxs-lookup"><span data-stu-id="92be6-109">Index of the triangle that hit the ray.</span></span>

</dd> <dt>

<span data-ttu-id="92be6-110">**U**</span><span class="sxs-lookup"><span data-stu-id="92be6-110">**U**</span></span>
</dt> <dd>

<span data-ttu-id="92be6-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="92be6-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="92be6-112">Координата барицентрик в пределах треугольника, на котором пересекается луч.</span><span class="sxs-lookup"><span data-stu-id="92be6-112">Barycentric coordinate within the triangle where the ray intersects.</span></span>

</dd> <dt>

<span data-ttu-id="92be6-113">**V**</span><span class="sxs-lookup"><span data-stu-id="92be6-113">**V**</span></span>
</dt> <dd>

<span data-ttu-id="92be6-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="92be6-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="92be6-115">Координата барицентрик в пределах треугольника, на котором пересекается луч.</span><span class="sxs-lookup"><span data-stu-id="92be6-115">Barycentric coordinate within the triangle where the ray intersects.</span></span>

</dd> <dt>

<span data-ttu-id="92be6-116">**Файле**</span><span class="sxs-lookup"><span data-stu-id="92be6-116">**Dist**</span></span>
</dt> <dd>

<span data-ttu-id="92be6-117">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="92be6-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="92be6-118">Расстояние вдоль луча, где произошло пересечение.</span><span class="sxs-lookup"><span data-stu-id="92be6-118">Distance along the ray where the intersection occurred.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="92be6-119">Remarks</span><span class="sxs-lookup"><span data-stu-id="92be6-119">Remarks</span></span>

<span data-ttu-id="92be6-120">Координаты барицентрик определяют точку внутри треугольника с точки зрения вершин треугольника.</span><span class="sxs-lookup"><span data-stu-id="92be6-120">Barycentric coordinates define a point inside a triangle in terms of the triangle's vertices.</span></span> <span data-ttu-id="92be6-121">Более подробное описание координат барицентрик см. в разделе [Описание координат Барицентрик MathWorld](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span><span class="sxs-lookup"><span data-stu-id="92be6-121">For a more in-depth description of barycentric coordinates, see [Mathworld's Barycentric Coordinates Description](https://mathworld.wolfram.com/BarycentricCoordinates.html).</span></span>

## <a name="requirements"></a><span data-ttu-id="92be6-122">Требования</span><span class="sxs-lookup"><span data-stu-id="92be6-122">Requirements</span></span>



| <span data-ttu-id="92be6-123">Требование</span><span class="sxs-lookup"><span data-stu-id="92be6-123">Requirement</span></span> | <span data-ttu-id="92be6-124">Значение</span><span class="sxs-lookup"><span data-stu-id="92be6-124">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="92be6-125">Header</span><span class="sxs-lookup"><span data-stu-id="92be6-125">Header</span></span><br/> | <dl> <span data-ttu-id="92be6-126"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="92be6-126"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92be6-127">См. также</span><span class="sxs-lookup"><span data-stu-id="92be6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92be6-128">Структуры D3DX</span><span class="sxs-lookup"><span data-stu-id="92be6-128">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
