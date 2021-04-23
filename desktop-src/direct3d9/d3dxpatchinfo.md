---
description: Структура, содержащая атрибуты сетки исправлений.
ms.assetid: aaea69c9-2d33-46e8-bc26-95daf65abf50
title: Структура D3DXPATCHINFO (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPATCHINFO
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 8628cc27a0223580aa1f8072750f4c31a176533e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354143"
---
# <a name="d3dxpatchinfo-structure"></a><span data-ttu-id="7afe8-103">Структура D3DXPATCHINFO</span><span class="sxs-lookup"><span data-stu-id="7afe8-103">D3DXPATCHINFO structure</span></span>

<span data-ttu-id="7afe8-104">Структура, содержащая атрибуты сетки исправлений.</span><span class="sxs-lookup"><span data-stu-id="7afe8-104">Structure that contains the attributes of a patch mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="7afe8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7afe8-105">Syntax</span></span>


```C++
typedef struct D3DXPATCHINFO {
  D3DXPATCHMESHTYPE PatchType;
  D3DDEGREETYPE     Degree;
  D3DBASISTYPE      Basis;
} D3DXPATCHINFO, *LPD3DXPATCHINFO;
```



## <a name="members"></a><span data-ttu-id="7afe8-106">Члены</span><span class="sxs-lookup"><span data-stu-id="7afe8-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="7afe8-107">**патчтипе**</span><span class="sxs-lookup"><span data-stu-id="7afe8-107">**PatchType**</span></span>
</dt> <dd>

<span data-ttu-id="7afe8-108">Тип: **[ **D3DXPATCHMESHTYPE**](./d3dxpatchmeshtype.md)**</span><span class="sxs-lookup"><span data-stu-id="7afe8-108">Type: **[**D3DXPATCHMESHTYPE**](./d3dxpatchmeshtype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7afe8-109">Тип исправления.</span><span class="sxs-lookup"><span data-stu-id="7afe8-109">The patch type.</span></span> <span data-ttu-id="7afe8-110">Сведения о типах исправлений см. в разделе [**D3DXPATCHMESHTYPE**](./d3dxpatchmeshtype.md).</span><span class="sxs-lookup"><span data-stu-id="7afe8-110">For information about patch types, see [**D3DXPATCHMESHTYPE**](./d3dxpatchmeshtype.md).</span></span>

</dd> <dt>

<span data-ttu-id="7afe8-111">**Градус**</span><span class="sxs-lookup"><span data-stu-id="7afe8-111">**Degree**</span></span>
</dt> <dd>

<span data-ttu-id="7afe8-112">Тип: **[ **D3DDEGREETYPE**](./d3ddegreetype.md)**</span><span class="sxs-lookup"><span data-stu-id="7afe8-112">Type: **[**D3DDEGREETYPE**](./d3ddegreetype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7afe8-113">Степень кривых, используемая для создания исправления.</span><span class="sxs-lookup"><span data-stu-id="7afe8-113">Degree of the curves used to construct the patch.</span></span> <span data-ttu-id="7afe8-114">Дополнительные сведения о поддерживаемых градусах см. в разделе [**D3DDEGREETYPE**](./d3ddegreetype.md).</span><span class="sxs-lookup"><span data-stu-id="7afe8-114">For information about the degrees supported, see [**D3DDEGREETYPE**](./d3ddegreetype.md).</span></span>

</dd> <dt>

<span data-ttu-id="7afe8-115">**База**</span><span class="sxs-lookup"><span data-stu-id="7afe8-115">**Basis**</span></span>
</dt> <dd>

<span data-ttu-id="7afe8-116">Тип: **[ **D3DBASISTYPE**](./d3dbasistype.md)**</span><span class="sxs-lookup"><span data-stu-id="7afe8-116">Type: **[**D3DBASISTYPE**](./d3dbasistype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7afe8-117">Тип кривой, используемой для создания исправления.</span><span class="sxs-lookup"><span data-stu-id="7afe8-117">Type of curve used to construct the patch.</span></span> <span data-ttu-id="7afe8-118">Сведения о поддерживаемых типах базисов см. в разделе [**D3DBASISTYPE**](./d3dbasistype.md).</span><span class="sxs-lookup"><span data-stu-id="7afe8-118">For information about the basis types supported, see [**D3DBASISTYPE**](./d3dbasistype.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7afe8-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7afe8-119">Remarks</span></span>

<span data-ttu-id="7afe8-120">Сетка — это набор лиц, каждый из которых описывается простым многоугольником.</span><span class="sxs-lookup"><span data-stu-id="7afe8-120">A mesh is a set of faces, each of which is described by a simple polygon.</span></span> <span data-ttu-id="7afe8-121">Объекты можно создать, подключив несколько сеток друг к другу.</span><span class="sxs-lookup"><span data-stu-id="7afe8-121">Objects can be created by connecting several meshes together.</span></span> <span data-ttu-id="7afe8-122">Сетка исправлений создается на основе исправлений.</span><span class="sxs-lookup"><span data-stu-id="7afe8-122">A patch mesh is constructed from patches.</span></span> <span data-ttu-id="7afe8-123">Исправление — это 4-сторонняя фигура геометрии, созданная на основе кривых.</span><span class="sxs-lookup"><span data-stu-id="7afe8-123">A patch is a four-sided piece of geometry constructed from curves.</span></span> <span data-ttu-id="7afe8-124">Тип используемой кривой и порядок кривой могут быть различными, чтобы поверхность исправления соответствовала любой фигуре поверхности.</span><span class="sxs-lookup"><span data-stu-id="7afe8-124">The type of curve used and the order of the curve can be varied so that the patch surface will fit almost any surface shape.</span></span>

<span data-ttu-id="7afe8-125">Поддерживаются следующие типы комбинаций исправлений:</span><span class="sxs-lookup"><span data-stu-id="7afe8-125">The following types of patch combinations are supported:</span></span>



| <span data-ttu-id="7afe8-126">Тип исправления</span><span class="sxs-lookup"><span data-stu-id="7afe8-126">Patch Type</span></span> | <span data-ttu-id="7afe8-127">Основа</span><span class="sxs-lookup"><span data-stu-id="7afe8-127">Basis</span></span>       | <span data-ttu-id="7afe8-128">Градус</span><span class="sxs-lookup"><span data-stu-id="7afe8-128">Degree</span></span> |
|------------|-------------|--------|
| <span data-ttu-id="7afe8-129">Прямоугольник</span><span class="sxs-lookup"><span data-stu-id="7afe8-129">Rectangle</span></span>  | <span data-ttu-id="7afe8-130">Безье</span><span class="sxs-lookup"><span data-stu-id="7afe8-130">Bezier</span></span>      | <span data-ttu-id="7afe8-131">2, 3, 5</span><span class="sxs-lookup"><span data-stu-id="7afe8-131">2,3,5</span></span>  |
| <span data-ttu-id="7afe8-132">Прямоугольник</span><span class="sxs-lookup"><span data-stu-id="7afe8-132">Rectangle</span></span>  | <span data-ttu-id="7afe8-133">B-сплайн</span><span class="sxs-lookup"><span data-stu-id="7afe8-133">B-Spline</span></span>    | <span data-ttu-id="7afe8-134">2, 3, 5</span><span class="sxs-lookup"><span data-stu-id="7afe8-134">2,3,5</span></span>  |
| <span data-ttu-id="7afe8-135">Прямоугольник</span><span class="sxs-lookup"><span data-stu-id="7afe8-135">Rectangle</span></span>  | <span data-ttu-id="7afe8-136">Catmull-Rom</span><span class="sxs-lookup"><span data-stu-id="7afe8-136">Catmull-Rom</span></span> | <span data-ttu-id="7afe8-137">3</span><span class="sxs-lookup"><span data-stu-id="7afe8-137">3</span></span>      |
| <span data-ttu-id="7afe8-138">Triangle</span><span class="sxs-lookup"><span data-stu-id="7afe8-138">Triangle</span></span>   | <span data-ttu-id="7afe8-139">Безье</span><span class="sxs-lookup"><span data-stu-id="7afe8-139">Bezier</span></span>      | <span data-ttu-id="7afe8-140">2, 3, 5</span><span class="sxs-lookup"><span data-stu-id="7afe8-140">2,3,5</span></span>  |
| <span data-ttu-id="7afe8-141">N-исправление</span><span class="sxs-lookup"><span data-stu-id="7afe8-141">N-patch</span></span>    | <span data-ttu-id="7afe8-142">Недоступно</span><span class="sxs-lookup"><span data-stu-id="7afe8-142">N/A</span></span>         | <span data-ttu-id="7afe8-143">3</span><span class="sxs-lookup"><span data-stu-id="7afe8-143">3</span></span>      |



 

## <a name="requirements"></a><span data-ttu-id="7afe8-144">Требования</span><span class="sxs-lookup"><span data-stu-id="7afe8-144">Requirements</span></span>



| <span data-ttu-id="7afe8-145">Требование</span><span class="sxs-lookup"><span data-stu-id="7afe8-145">Requirement</span></span> | <span data-ttu-id="7afe8-146">Значение</span><span class="sxs-lookup"><span data-stu-id="7afe8-146">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7afe8-147">Header</span><span class="sxs-lookup"><span data-stu-id="7afe8-147">Header</span></span><br/> | <dl> <span data-ttu-id="7afe8-148"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="7afe8-148"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7afe8-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7afe8-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7afe8-150">Структуры D3DX</span><span class="sxs-lookup"><span data-stu-id="7afe8-150">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="7afe8-151">**\_Сведения о D3DRECTPATCH**</span><span class="sxs-lookup"><span data-stu-id="7afe8-151">**D3DRECTPATCH\_INFO**</span></span>](d3drectpatch-info.md)
</dt> <dt>

[<span data-ttu-id="7afe8-152">**\_Сведения о D3DTRIPATCH**</span><span class="sxs-lookup"><span data-stu-id="7afe8-152">**D3DTRIPATCH\_INFO**</span></span>](d3dtripatch-info.md)
</dt> <dt>

[<span data-ttu-id="7afe8-153">**D3DXCreatePatchMesh**</span><span class="sxs-lookup"><span data-stu-id="7afe8-153">**D3DXCreatePatchMesh**</span></span>](d3dxcreatepatchmesh.md)
</dt> </dl>

 

 
