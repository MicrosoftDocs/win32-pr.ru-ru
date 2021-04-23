---
description: Описывает прямоугольное исправление высокого порядка.
ms.assetid: 5f195009-d047-4dc0-a386-e1a434914e34
title: Структура D3DRECTPATCH_INFO (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRECTPATCH_INFO
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: a2b7fedbaac2cc9c204d4691828d31794cea1f47
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703831"
---
# <a name="d3drectpatch_info-structure"></a><span data-ttu-id="34b14-103">\_Структура сведений о D3DRECTPATCH</span><span class="sxs-lookup"><span data-stu-id="34b14-103">D3DRECTPATCH\_INFO structure</span></span>

<span data-ttu-id="34b14-104">Описывает прямоугольное исправление высокого порядка.</span><span class="sxs-lookup"><span data-stu-id="34b14-104">Describes a rectangular high-order patch.</span></span>

## <a name="syntax"></a><span data-ttu-id="34b14-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="34b14-105">Syntax</span></span>


```C++
typedef struct D3DRECTPATCH_INFO {
  UINT          StartVertexOffsetWidth;
  UINT          StartVertexOffsetHeight;
  UINT          Width;
  UINT          Height;
  UINT          Stride;
  D3DBASISTYPE  Basis;
  D3DDEGREETYPE Degree;
} D3DRECTPATCH_INFO, *LPD3DRECTPATCH_INFO;
```



## <a name="members"></a><span data-ttu-id="34b14-106">Члены</span><span class="sxs-lookup"><span data-stu-id="34b14-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="34b14-107">**стартвертексоффсетвидс**</span><span class="sxs-lookup"><span data-stu-id="34b14-107">**StartVertexOffsetWidth**</span></span>
</dt> <dd>

<span data-ttu-id="34b14-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="34b14-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="34b14-109">Начальная ширина смещения вершины в количестве вершин.</span><span class="sxs-lookup"><span data-stu-id="34b14-109">Starting vertex offset width, in number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="34b14-110">**стартвертексоффсесеигхт**</span><span class="sxs-lookup"><span data-stu-id="34b14-110">**StartVertexOffsetHeight**</span></span>
</dt> <dd>

<span data-ttu-id="34b14-111">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="34b14-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="34b14-112">Начальная высота смещения вершины, в количестве вершин.</span><span class="sxs-lookup"><span data-stu-id="34b14-112">Starting vertex offset height, in number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="34b14-113">**Width**</span><span class="sxs-lookup"><span data-stu-id="34b14-113">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="34b14-114">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="34b14-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="34b14-115">Ширина каждой вершины в количестве вершин.</span><span class="sxs-lookup"><span data-stu-id="34b14-115">Width of each vertex, in number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="34b14-116">**Height**</span><span class="sxs-lookup"><span data-stu-id="34b14-116">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="34b14-117">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="34b14-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="34b14-118">Высота каждой вершины в количестве вершин.</span><span class="sxs-lookup"><span data-stu-id="34b14-118">Height of each vertex, in number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="34b14-119">**Stride**</span><span class="sxs-lookup"><span data-stu-id="34b14-119">**Stride**</span></span>
</dt> <dd>

<span data-ttu-id="34b14-120">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="34b14-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="34b14-121">Ширина мнимого двумерного массива вершин, который занимает то же пространство, что и буфер вершин.</span><span class="sxs-lookup"><span data-stu-id="34b14-121">Width of the imaginary two-dimensional vertex array, which occupies the same space as the vertex buffer.</span></span> <span data-ttu-id="34b14-122">Пример см. на приведенной ниже схеме.</span><span class="sxs-lookup"><span data-stu-id="34b14-122">For an example, see the diagram below.</span></span>

</dd> <dt>

<span data-ttu-id="34b14-123">**База**</span><span class="sxs-lookup"><span data-stu-id="34b14-123">**Basis**</span></span>
</dt> <dd>

<span data-ttu-id="34b14-124">Тип: **[ **D3DBASISTYPE**](./d3dbasistype.md)**</span><span class="sxs-lookup"><span data-stu-id="34b14-124">Type: **[**D3DBASISTYPE**](./d3dbasistype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="34b14-125">Элемент перечисляемого типа [**D3DBASISTYPE**](./d3dbasistype.md) , определяющий тип базиса для прямоугольного исправления высокого порядка.</span><span class="sxs-lookup"><span data-stu-id="34b14-125">Member of the [**D3DBASISTYPE**](./d3dbasistype.md) enumerated type, defining the basis type for the rectangular high-order patch.</span></span>



| <span data-ttu-id="34b14-126">Значение</span><span class="sxs-lookup"><span data-stu-id="34b14-126">Value</span></span>                 | <span data-ttu-id="34b14-127">Поддерживаемые заказы</span><span class="sxs-lookup"><span data-stu-id="34b14-127">Order supported</span></span>            | <span data-ttu-id="34b14-128">Ширина и высота</span><span class="sxs-lookup"><span data-stu-id="34b14-128">Width and height</span></span>                  |
|-----------------------|----------------------------|-----------------------------------|
| <span data-ttu-id="34b14-129">D3DBASIS \_ Безье</span><span class="sxs-lookup"><span data-stu-id="34b14-129">D3DBASIS\_BEZIER</span></span>      | <span data-ttu-id="34b14-130">Линейный, кубический и куинтик</span><span class="sxs-lookup"><span data-stu-id="34b14-130">Linear, cubic, and quintic</span></span> | <span data-ttu-id="34b14-131">Width = height = (DWORD) порядок + 1</span><span class="sxs-lookup"><span data-stu-id="34b14-131">Width = height = (DWORD)order + 1</span></span> |
| <span data-ttu-id="34b14-132">D3DBASIS \_ бсплине</span><span class="sxs-lookup"><span data-stu-id="34b14-132">D3DBASIS\_BSPLINE</span></span>     | <span data-ttu-id="34b14-133">Линейный, кубический и куинтик</span><span class="sxs-lookup"><span data-stu-id="34b14-133">Linear, cubic, and quintic</span></span> | <span data-ttu-id="34b14-134">Width = высота > (DWORD)</span><span class="sxs-lookup"><span data-stu-id="34b14-134">Width = height > (DWORD)order</span></span>  |
| <span data-ttu-id="34b14-135">D3DBASIS \_ интерполяция</span><span class="sxs-lookup"><span data-stu-id="34b14-135">D3DBASIS\_INTERPOLATE</span></span> | <span data-ttu-id="34b14-136">Кривой</span><span class="sxs-lookup"><span data-stu-id="34b14-136">Cubic</span></span>                      | <span data-ttu-id="34b14-137">Width = высота > (DWORD)</span><span class="sxs-lookup"><span data-stu-id="34b14-137">Width = height > (DWORD)order</span></span>  |



 

</dd> <dt>

<span data-ttu-id="34b14-138">**Градус**</span><span class="sxs-lookup"><span data-stu-id="34b14-138">**Degree**</span></span>
</dt> <dd>

<span data-ttu-id="34b14-139">Тип: **[ **D3DDEGREETYPE**](./d3ddegreetype.md)**</span><span class="sxs-lookup"><span data-stu-id="34b14-139">Type: **[**D3DDEGREETYPE**](./d3ddegreetype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="34b14-140">Член перечисляемого типа [**D3DDEGREETYPE**](./d3ddegreetype.md) , определяющий степень прямоугольного исправления.</span><span class="sxs-lookup"><span data-stu-id="34b14-140">Member of the [**D3DDEGREETYPE**](./d3ddegreetype.md) enumerated type, defining the degree for the rectangular patch.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="34b14-141">Комментарии</span><span class="sxs-lookup"><span data-stu-id="34b14-141">Remarks</span></span>

<span data-ttu-id="34b14-142">На следующей схеме указываются параметры, определяющие обновление прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="34b14-142">The following diagram identifies the parameters that specify a rectangle patch.</span></span>

![Схема прямоугольного исправления высокого порядка и параметров, которые его задают](images/hop-rectpatch.png)

<span data-ttu-id="34b14-144">Каждая вершина в буфере вершин отображается в виде черной точки.</span><span class="sxs-lookup"><span data-stu-id="34b14-144">Each of the vertices in the vertex buffer is shown as a black dot.</span></span> <span data-ttu-id="34b14-145">В этом случае в буфере вершин имеется 20 вершин, 16 из которых находятся в области обновления прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="34b14-145">In this case, the vertex buffer has 20 vertices in it, 16 of which are in the rectangle patch.</span></span> <span data-ttu-id="34b14-146">Шаг — это число вершин в ширине буфера вершин, в данном случае пять.</span><span class="sxs-lookup"><span data-stu-id="34b14-146">The stride is the number of vertices in the width of the vertex buffer, in this case five.</span></span> <span data-ttu-id="34b14-147">Смещение x к первой вершине называется Стартиндексвертексвидс и в данном случае равно 1.</span><span class="sxs-lookup"><span data-stu-id="34b14-147">The x offset to the first vertex is called the StartIndexVertexWidth and is in this case 1.</span></span> <span data-ttu-id="34b14-148">Смещение y к первой вершине исправления называется Стартиндексвертексхеигхт и в данном случае 0.</span><span class="sxs-lookup"><span data-stu-id="34b14-148">The y offset to the first patch vertex is called the StartIndexVertexHeight and is in this case 0.</span></span>

<span data-ttu-id="34b14-149">Для отображения потока отдельных прямоугольных исправлений (не мозаики) необходимо интерпретировать геометрию как длинное частное (1 x N) прямоугольное исправление.</span><span class="sxs-lookup"><span data-stu-id="34b14-149">To render a stream of individual rectangular patches (non-mosaic), you should interpret your geometry as a long narrow (1 x N) rectangular patch.</span></span> <span data-ttu-id="34b14-150">Структура **\_ сведений о D3DRECTPATCH** для такого полоска (кубический Безье) будет настроена следующим образом.</span><span class="sxs-lookup"><span data-stu-id="34b14-150">The **D3DRECTPATCH\_INFO** structure for such a strip (cubic Bézier) would be set up in the following manner.</span></span>


```
    
D3DRECTPATCH_INFO RectInfo;

RectInfo.Width = 4;
RectInfo.Height = 4;
RectInfo.Stride = 4;
RectInfo.Basis = D3DBASIS_BEZIER;
RectInfo.Order = D3DORDER_CUBIC;
RectInfo.StartVertexOffsetWidth = 0;
RectInfo.StartVertexOffsetHeight = 4*i;  // The variable i is the index of the 
//   patch you want to render.
```



## <a name="requirements"></a><span data-ttu-id="34b14-151">Требования</span><span class="sxs-lookup"><span data-stu-id="34b14-151">Requirements</span></span>



| <span data-ttu-id="34b14-152">Требование</span><span class="sxs-lookup"><span data-stu-id="34b14-152">Requirement</span></span> | <span data-ttu-id="34b14-153">Значение</span><span class="sxs-lookup"><span data-stu-id="34b14-153">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="34b14-154">Header</span><span class="sxs-lookup"><span data-stu-id="34b14-154">Header</span></span><br/> | <dl> <span data-ttu-id="34b14-155"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="34b14-155"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34b14-156">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="34b14-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34b14-157">Структуры Direct3D</span><span class="sxs-lookup"><span data-stu-id="34b14-157">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="34b14-158">**дравректпатч**</span><span class="sxs-lookup"><span data-stu-id="34b14-158">**DrawRectPatch**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawrectpatch)
</dt> <dt>

[<span data-ttu-id="34b14-159">**D3DXTessellateRectPatch**</span><span class="sxs-lookup"><span data-stu-id="34b14-159">**D3DXTessellateRectPatch**</span></span>](d3dxtessellaterectpatch.md)
</dt> </dl>

 

 
