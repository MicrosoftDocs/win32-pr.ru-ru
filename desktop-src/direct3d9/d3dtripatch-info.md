---
description: Описывает треугольное обновление высокого порядка.
ms.assetid: 3f97120b-3b32-4f95-8614-7b263ff330db
title: Структура D3DTRIPATCH_INFO (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTRIPATCH_INFO
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: b910d38025c44d6157a76aa3e3425ba46d628787
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713878"
---
# <a name="d3dtripatch_info-structure"></a><span data-ttu-id="d0fbb-103">\_Структура сведений о D3DTRIPATCH</span><span class="sxs-lookup"><span data-stu-id="d0fbb-103">D3DTRIPATCH\_INFO structure</span></span>

<span data-ttu-id="d0fbb-104">Описывает треугольное обновление высокого порядка.</span><span class="sxs-lookup"><span data-stu-id="d0fbb-104">Describes a triangular high-order patch.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0fbb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d0fbb-105">Syntax</span></span>


```C++
typedef struct D3DTRIPATCH_INFO {
  UINT          StartVertexOffset;
  UINT          NumVertices;
  D3DBASISTYPE  Basis;
  D3DDEGREETYPE Degree;
} D3DTRIPATCH_INFO, *LPD3DTRIPATCH_INFO;
```



## <a name="members"></a><span data-ttu-id="d0fbb-106">Члены</span><span class="sxs-lookup"><span data-stu-id="d0fbb-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="d0fbb-107">**стартвертексоффсет**</span><span class="sxs-lookup"><span data-stu-id="d0fbb-107">**StartVertexOffset**</span></span>
</dt> <dd>

<span data-ttu-id="d0fbb-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d0fbb-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d0fbb-109">Начальное смещение вершины в количестве вершин.</span><span class="sxs-lookup"><span data-stu-id="d0fbb-109">Starting vertex offset, in number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="d0fbb-110">**нумвертицес**</span><span class="sxs-lookup"><span data-stu-id="d0fbb-110">**NumVertices**</span></span>
</dt> <dd>

<span data-ttu-id="d0fbb-111">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d0fbb-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d0fbb-112">Число вершин.</span><span class="sxs-lookup"><span data-stu-id="d0fbb-112">Number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="d0fbb-113">**База**</span><span class="sxs-lookup"><span data-stu-id="d0fbb-113">**Basis**</span></span>
</dt> <dd>

<span data-ttu-id="d0fbb-114">Тип: **[ **D3DBASISTYPE**](./d3dbasistype.md)**</span><span class="sxs-lookup"><span data-stu-id="d0fbb-114">Type: **[**D3DBASISTYPE**](./d3dbasistype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d0fbb-115">Член перечисляемого типа [**D3DBASISTYPE**](./d3dbasistype.md) , который определяет тип базиса для треугольного высококачественного исправления.</span><span class="sxs-lookup"><span data-stu-id="d0fbb-115">Member of the [**D3DBASISTYPE**](./d3dbasistype.md) enumerated type, which defines the basis type for the triangular high-order patch.</span></span> <span data-ttu-id="d0fbb-116">Единственным допустимым значением для этого элемента является D3DBASIS \_ Безье.</span><span class="sxs-lookup"><span data-stu-id="d0fbb-116">The only valid value for this member is D3DBASIS\_BEZIER.</span></span>

</dd> <dt>

<span data-ttu-id="d0fbb-117">**Градус**</span><span class="sxs-lookup"><span data-stu-id="d0fbb-117">**Degree**</span></span>
</dt> <dd>

<span data-ttu-id="d0fbb-118">Тип: **[ **D3DDEGREETYPE**](./d3ddegreetype.md)**</span><span class="sxs-lookup"><span data-stu-id="d0fbb-118">Type: **[**D3DDEGREETYPE**](./d3ddegreetype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d0fbb-119">Элемент перечисляемого типа [**D3DDEGREETYPE**](./d3ddegreetype.md) , определяющий тип степени для треугольного исправления высокого порядка.</span><span class="sxs-lookup"><span data-stu-id="d0fbb-119">Member of the [**D3DDEGREETYPE**](./d3ddegreetype.md) enumerated type, defining the degree type for the triangular high-order patch.</span></span>



| <span data-ttu-id="d0fbb-120">Значение</span><span class="sxs-lookup"><span data-stu-id="d0fbb-120">Value</span></span>                | <span data-ttu-id="d0fbb-121">Число вершин</span><span class="sxs-lookup"><span data-stu-id="d0fbb-121">Number of vertices</span></span> |
|----------------------|--------------------|
| <span data-ttu-id="d0fbb-122">D3DDEGREE \_ кубический</span><span class="sxs-lookup"><span data-stu-id="d0fbb-122">D3DDEGREE\_CUBIC</span></span>     | <span data-ttu-id="d0fbb-123">10</span><span class="sxs-lookup"><span data-stu-id="d0fbb-123">10</span></span>                 |
| <span data-ttu-id="d0fbb-124">\_Линейная D3DDEGREE</span><span class="sxs-lookup"><span data-stu-id="d0fbb-124">D3DDEGREE\_LINEAR</span></span>    | <span data-ttu-id="d0fbb-125">3</span><span class="sxs-lookup"><span data-stu-id="d0fbb-125">3</span></span>                  |
| <span data-ttu-id="d0fbb-126">D3DDEGREE, \_ квадрат</span><span class="sxs-lookup"><span data-stu-id="d0fbb-126">D3DDEGREE\_QUADRATIC</span></span> | <span data-ttu-id="d0fbb-127">Н/Д</span><span class="sxs-lookup"><span data-stu-id="d0fbb-127">N/A</span></span>                |
| <span data-ttu-id="d0fbb-128">D3DDEGREE \_ куинтик</span><span class="sxs-lookup"><span data-stu-id="d0fbb-128">D3DDEGREE\_QUINTIC</span></span>   | <span data-ttu-id="d0fbb-129">21</span><span class="sxs-lookup"><span data-stu-id="d0fbb-129">21</span></span>                 |



 

<span data-ttu-id="d0fbb-130">Н/д — недоступно.</span><span class="sxs-lookup"><span data-stu-id="d0fbb-130">N/A - Not available.</span></span> <span data-ttu-id="d0fbb-131">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="d0fbb-131">Not supported.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d0fbb-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d0fbb-132">Remarks</span></span>

<span data-ttu-id="d0fbb-133">Например, на следующей схеме определяются порядок вершин и номера сегментов для исправления треугольника Безье третьего порядка.</span><span class="sxs-lookup"><span data-stu-id="d0fbb-133">For example, the following diagram identifies the vertex order and segment numbers for a cubic Bézier triangle patch.</span></span> <span data-ttu-id="d0fbb-134">Порядок вершин определяет номера сегментов, используемые [**дравтрипатч**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawtripatch).</span><span class="sxs-lookup"><span data-stu-id="d0fbb-134">The vertex order determines the segment numbers used by [**DrawTriPatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawtripatch).</span></span> <span data-ttu-id="d0fbb-135">Смещение — это число байтов для первого вершинного исправления треугольника в буфере вершин.</span><span class="sxs-lookup"><span data-stu-id="d0fbb-135">The offset is the number of bytes to the first triangle patch vertex in the vertex buffer.</span></span>

![Схема треугольного исправления высокого порядка с девятью вершинами](images/hop-tripatch-info.png)

## <a name="requirements"></a><span data-ttu-id="d0fbb-137">Требования</span><span class="sxs-lookup"><span data-stu-id="d0fbb-137">Requirements</span></span>



| <span data-ttu-id="d0fbb-138">Требование</span><span class="sxs-lookup"><span data-stu-id="d0fbb-138">Requirement</span></span> | <span data-ttu-id="d0fbb-139">Значение</span><span class="sxs-lookup"><span data-stu-id="d0fbb-139">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d0fbb-140">Header</span><span class="sxs-lookup"><span data-stu-id="d0fbb-140">Header</span></span><br/> | <dl> <span data-ttu-id="d0fbb-141"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0fbb-141"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0fbb-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d0fbb-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0fbb-143">Структуры Direct3D</span><span class="sxs-lookup"><span data-stu-id="d0fbb-143">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="d0fbb-144">**дравтрипатч**</span><span class="sxs-lookup"><span data-stu-id="d0fbb-144">**DrawTriPatch**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawtripatch)
</dt> <dt>

[<span data-ttu-id="d0fbb-145">**D3DXTessellateTriPatch**</span><span class="sxs-lookup"><span data-stu-id="d0fbb-145">**D3DXTessellateTriPatch**</span></span>](d3dxtessellatetripatch.md)
</dt> </dl>

 

 
