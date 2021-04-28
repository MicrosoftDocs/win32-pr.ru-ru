---
description: Структура D3DXWELDEPSILONS. задает значения допуска для каждого компонента вершины при сравнении вершин, чтобы определить, достаточно ли они, чтобы их можно было использовать одновременно.
ms.assetid: 534903da-ff65-4629-9be9-66c9daed6ef5
title: Структура D3DXWELDEPSILONS (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXWELDEPSILONS
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: bb11e6f5481b1adf7cc1bac58edf40d4ac770e92
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115502"
---
# <a name="d3dxweldepsilons-structure"></a><span data-ttu-id="73c81-103">Структура D3DXWELDEPSILONS</span><span class="sxs-lookup"><span data-stu-id="73c81-103">D3DXWELDEPSILONS structure</span></span>

<span data-ttu-id="73c81-104">Задает значения допуска для каждого компонента вершины при сравнении вершин, чтобы определить, достаточно ли они, чтобы они были связаны друг с другом.</span><span class="sxs-lookup"><span data-stu-id="73c81-104">Specifies tolerance values for each vertex component when comparing vertices to determine if they are similar enough to be welded together.</span></span>

## <a name="syntax"></a><span data-ttu-id="73c81-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="73c81-105">Syntax</span></span>


```C++
typedef struct _D3DXWELDEPSILONS {
  FLOAT Position;
  FLOAT BlendWeights;
  FLOAT Normal;
  FLOAT PSize;
  FLOAT Specular;
  FLOAT Diffuse;
  FLOAT Texcoord[8];
  FLOAT Tangent;
  FLOAT Binormal;
  FLOAT TessFactor;
} D3DXWELDEPSILONS, *LPD3DXWELDEPSILONS;
```



## <a name="members"></a><span data-ttu-id="73c81-106">Члены</span><span class="sxs-lookup"><span data-stu-id="73c81-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="73c81-107">**Позиция**</span><span class="sxs-lookup"><span data-stu-id="73c81-107">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="73c81-108">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="73c81-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="73c81-109">Положение</span><span class="sxs-lookup"><span data-stu-id="73c81-109">Position</span></span>

</dd> <dt>

<span data-ttu-id="73c81-110">**блендвеигхтс**</span><span class="sxs-lookup"><span data-stu-id="73c81-110">**BlendWeights**</span></span>
</dt> <dd>

<span data-ttu-id="73c81-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="73c81-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="73c81-112">Вес смешения</span><span class="sxs-lookup"><span data-stu-id="73c81-112">Blend weight</span></span>

</dd> <dt>

<span data-ttu-id="73c81-113">**Обычный**</span><span class="sxs-lookup"><span data-stu-id="73c81-113">**Normal**</span></span>
</dt> <dd>

<span data-ttu-id="73c81-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="73c81-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="73c81-115">Норм.</span><span class="sxs-lookup"><span data-stu-id="73c81-115">Normal</span></span>

</dd> <dt>

<span data-ttu-id="73c81-116">**псизе**</span><span class="sxs-lookup"><span data-stu-id="73c81-116">**PSize**</span></span>
</dt> <dd>

<span data-ttu-id="73c81-117">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="73c81-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="73c81-118">Значение размера точки</span><span class="sxs-lookup"><span data-stu-id="73c81-118">Point size value</span></span>

</dd> <dt>

<span data-ttu-id="73c81-119">**Отражающее**</span><span class="sxs-lookup"><span data-stu-id="73c81-119">**Specular**</span></span>
</dt> <dd>

<span data-ttu-id="73c81-120">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="73c81-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="73c81-121">Значение отраженного освещения</span><span class="sxs-lookup"><span data-stu-id="73c81-121">Specular lighting value</span></span>

</dd> <dt>

<span data-ttu-id="73c81-122">**Диффузное**</span><span class="sxs-lookup"><span data-stu-id="73c81-122">**Diffuse**</span></span>
</dt> <dd>

<span data-ttu-id="73c81-123">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="73c81-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="73c81-124">Рассеянное значение освещения</span><span class="sxs-lookup"><span data-stu-id="73c81-124">Diffuse lighting value</span></span>

</dd> <dt>

<span data-ttu-id="73c81-125">**текскурд**</span><span class="sxs-lookup"><span data-stu-id="73c81-125">**Texcoord**</span></span>
</dt> <dd>

<span data-ttu-id="73c81-126">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="73c81-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="73c81-127">Восемь координат текстуры</span><span class="sxs-lookup"><span data-stu-id="73c81-127">Eight texture coordinates</span></span>

</dd> <dt>

<span data-ttu-id="73c81-128">**Тангенс**</span><span class="sxs-lookup"><span data-stu-id="73c81-128">**Tangent**</span></span>
</dt> <dd>

<span data-ttu-id="73c81-129">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="73c81-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="73c81-130">Тангенс</span><span class="sxs-lookup"><span data-stu-id="73c81-130">Tangent</span></span>

</dd> <dt>

<span data-ttu-id="73c81-131">**бинормал**</span><span class="sxs-lookup"><span data-stu-id="73c81-131">**Binormal**</span></span>
</dt> <dd>

<span data-ttu-id="73c81-132">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="73c81-132">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="73c81-133">бинормал</span><span class="sxs-lookup"><span data-stu-id="73c81-133">Binormal</span></span>

</dd> <dt>

<span data-ttu-id="73c81-134">**тессфактор**</span><span class="sxs-lookup"><span data-stu-id="73c81-134">**TessFactor**</span></span>
</dt> <dd>

<span data-ttu-id="73c81-135">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="73c81-135">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="73c81-136">Фактор тесселяции</span><span class="sxs-lookup"><span data-stu-id="73c81-136">Tessellation factor</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="73c81-137">Remarks</span><span class="sxs-lookup"><span data-stu-id="73c81-137">Remarks</span></span>

<span data-ttu-id="73c81-138">Тип LPD3DXWELDEPSILONS определяется как указатель на структуру **D3DXWELDEPSILONS** .</span><span class="sxs-lookup"><span data-stu-id="73c81-138">The LPD3DXWELDEPSILONS type is defined as a pointer to the **D3DXWELDEPSILONS** structure.</span></span>


```
typedef D3DXWELDEPSILONS *LPD3DXWELDEPSILONS;
```



## <a name="requirements"></a><span data-ttu-id="73c81-139">Требования</span><span class="sxs-lookup"><span data-stu-id="73c81-139">Requirements</span></span>



| <span data-ttu-id="73c81-140">Требование</span><span class="sxs-lookup"><span data-stu-id="73c81-140">Requirement</span></span> | <span data-ttu-id="73c81-141">Значение</span><span class="sxs-lookup"><span data-stu-id="73c81-141">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="73c81-142">Header</span><span class="sxs-lookup"><span data-stu-id="73c81-142">Header</span></span><br/> | <dl> <span data-ttu-id="73c81-143"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="73c81-143"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73c81-144">См. также</span><span class="sxs-lookup"><span data-stu-id="73c81-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73c81-145">Структуры D3DX</span><span class="sxs-lookup"><span data-stu-id="73c81-145">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="73c81-146">**D3DXWeldVertices**</span><span class="sxs-lookup"><span data-stu-id="73c81-146">**D3DXWeldVertices**</span></span>](d3dxweldvertices.md)
</dt> </dl>

 

 
