---
description: Определяет тип базиса для поверхности исправления высокого порядка.
ms.assetid: 18c31c77-7ba3-449c-af4a-717b8c1dced1
title: Перечисление D3DBASISTYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DBASISTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 7e166f56aa2625c868d3e2e2223efbb577e05bf5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157151"
---
# <a name="d3dbasistype-enumeration"></a><span data-ttu-id="f16e1-103">Перечисление D3DBASISTYPE</span><span class="sxs-lookup"><span data-stu-id="f16e1-103">D3DBASISTYPE enumeration</span></span>

<span data-ttu-id="f16e1-104">Определяет тип базиса для поверхности исправления высокого порядка.</span><span class="sxs-lookup"><span data-stu-id="f16e1-104">Defines the basis type of a high-order patch surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="f16e1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f16e1-105">Syntax</span></span>


```C++
typedef enum D3DBASISTYPE { 
  D3DBASIS_BEZIER       = 0,
  D3DBASIS_BSPLINE      = 1,
  D3DBASIS_CATMULL_ROM  = 2,
  D3DBASIS_FORCE_DWORD  = 0x7fffffff
} D3DBASISTYPE, *LPD3DBASISTYPE;
```



## <a name="constants"></a><span data-ttu-id="f16e1-106">Константы</span><span class="sxs-lookup"><span data-stu-id="f16e1-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="f16e1-107"><span id="D3DBASIS_BEZIER"></span><span id="d3dbasis_bezier"></span>**D3DBASIS \_ Безье**</span><span class="sxs-lookup"><span data-stu-id="f16e1-107"><span id="D3DBASIS_BEZIER"></span><span id="d3dbasis_bezier"></span>**D3DBASIS\_BEZIER**</span></span>
</dt> <dd>

<span data-ttu-id="f16e1-108">Входные вершины рассматриваются как ряд исправлений Безье.</span><span class="sxs-lookup"><span data-stu-id="f16e1-108">Input vertices are treated as a series of Bézier patches.</span></span> <span data-ttu-id="f16e1-109">Указанное число вершин должно быть кратным 4.</span><span class="sxs-lookup"><span data-stu-id="f16e1-109">The number of vertices specified must be divisible by 4.</span></span> <span data-ttu-id="f16e1-110">Части сетки, превышающие этот критерий, не будут подготавливаться к просмотру.</span><span class="sxs-lookup"><span data-stu-id="f16e1-110">Portions of the mesh beyond this criterion will not be rendered.</span></span> <span data-ttu-id="f16e1-111">Между подисправлениями в внутренней области, отображаемой каждым вызовом, подразумевается полная непрерывность.</span><span class="sxs-lookup"><span data-stu-id="f16e1-111">Full continuity is assumed between sub-patches in the interior of the surface rendered by each call.</span></span> <span data-ttu-id="f16e1-112">На результирующей поверхности гарантированно помещаются только вершины в углах каждого подобновления.</span><span class="sxs-lookup"><span data-stu-id="f16e1-112">Only the vertices at the corners of each sub-patch are guaranteed to lie on the resulting surface.</span></span>

</dd> <dt>

<span data-ttu-id="f16e1-113"><span id="D3DBASIS_BSPLINE"></span><span id="d3dbasis_bspline"></span>**D3DBASIS \_ бсплине**</span><span class="sxs-lookup"><span data-stu-id="f16e1-113"><span id="D3DBASIS_BSPLINE"></span><span id="d3dbasis_bspline"></span>**D3DBASIS\_BSPLINE**</span></span>
</dt> <dd>

<span data-ttu-id="f16e1-114">Входные вершины обрабатываются как контрольные точки в области B-сплайна.</span><span class="sxs-lookup"><span data-stu-id="f16e1-114">Input vertices are treated as control points of a B-spline surface.</span></span> <span data-ttu-id="f16e1-115">Число отображаемых апертур меньше, чем число апертур в этом направлении.</span><span class="sxs-lookup"><span data-stu-id="f16e1-115">The number of apertures rendered is two fewer than the number of apertures in that direction.</span></span> <span data-ttu-id="f16e1-116">В общем случае созданная поверхность не содержит заданных вершин элемента управления.</span><span class="sxs-lookup"><span data-stu-id="f16e1-116">In general, the generated surface does not contain the control vertices specified.</span></span>

</dd> <dt>

<span data-ttu-id="f16e1-117"><span id="D3DBASIS_CATMULL_ROM"></span><span id="d3dbasis_catmull_rom"></span>**D3DBASIS \_ катмулл \_ ROM**</span><span class="sxs-lookup"><span data-stu-id="f16e1-117"><span id="D3DBASIS_CATMULL_ROM"></span><span id="d3dbasis_catmull_rom"></span>**D3DBASIS\_CATMULL\_ROM**</span></span>
</dt> <dd>

<span data-ttu-id="f16e1-118">На основе интерполяции определяется поверхность, так что поверхность проходит через все указанные вершины входных вершин.</span><span class="sxs-lookup"><span data-stu-id="f16e1-118">An interpolating basis defines the surface so that the surface goes through all the input vertices specified.</span></span> <span data-ttu-id="f16e1-119">В DirectX 8 это было D3DBASIS \_ интерполяцией.</span><span class="sxs-lookup"><span data-stu-id="f16e1-119">In DirectX 8, this was D3DBASIS\_INTERPOLATE.</span></span>

</dd> <dt>

<span data-ttu-id="f16e1-120"><span id="D3DBASIS_FORCE_DWORD"></span><span id="d3dbasis_force_dword"></span>**D3DBASIS \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="f16e1-120"><span id="D3DBASIS_FORCE_DWORD"></span><span id="d3dbasis_force_dword"></span>**D3DBASIS\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="f16e1-121">Заставляет это перечисление компилироваться до 32 бит в размере.</span><span class="sxs-lookup"><span data-stu-id="f16e1-121">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="f16e1-122">Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит.</span><span class="sxs-lookup"><span data-stu-id="f16e1-122">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="f16e1-123">Это значение не используется.</span><span class="sxs-lookup"><span data-stu-id="f16e1-123">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f16e1-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f16e1-124">Remarks</span></span>

<span data-ttu-id="f16e1-125">Члены **D3DBASISTYPE** задают формулировку, который будет использоваться для вычисления примитива поверхности исправления высокого порядка во время тесселяции.</span><span class="sxs-lookup"><span data-stu-id="f16e1-125">The members of **D3DBASISTYPE** specify the formulation to be used in evaluating the high-order patch surface primitive during tessellation.</span></span>

## <a name="requirements"></a><span data-ttu-id="f16e1-126">Требования</span><span class="sxs-lookup"><span data-stu-id="f16e1-126">Requirements</span></span>



| <span data-ttu-id="f16e1-127">Требование</span><span class="sxs-lookup"><span data-stu-id="f16e1-127">Requirement</span></span> | <span data-ttu-id="f16e1-128">Значение</span><span class="sxs-lookup"><span data-stu-id="f16e1-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f16e1-129">Header</span><span class="sxs-lookup"><span data-stu-id="f16e1-129">Header</span></span><br/> | <dl> <span data-ttu-id="f16e1-130"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="f16e1-130"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f16e1-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f16e1-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f16e1-132">Перечисления Direct3D</span><span class="sxs-lookup"><span data-stu-id="f16e1-132">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="f16e1-133">**\_Сведения о D3DRECTPATCH**</span><span class="sxs-lookup"><span data-stu-id="f16e1-133">**D3DRECTPATCH\_INFO**</span></span>](d3drectpatch-info.md)
</dt> <dt>

[<span data-ttu-id="f16e1-134">**\_Сведения о D3DTRIPATCH**</span><span class="sxs-lookup"><span data-stu-id="f16e1-134">**D3DTRIPATCH\_INFO**</span></span>](d3dtripatch-info.md)
</dt> </dl>

 

 




