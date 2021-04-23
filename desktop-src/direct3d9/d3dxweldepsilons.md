---
description: Задает значения допуска для каждого компонента вершины при сравнении вершин, чтобы определить, достаточно ли они, чтобы они были связаны друг с другом.
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
ms.openlocfilehash: 6b6673e16b153f53baf17967b7f33c4bcb40d518
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105647847"
---
# <a name="d3dxweldepsilons-structure"></a><span data-ttu-id="bae23-103">Структура D3DXWELDEPSILONS</span><span class="sxs-lookup"><span data-stu-id="bae23-103">D3DXWELDEPSILONS structure</span></span>

<span data-ttu-id="bae23-104">Задает значения допуска для каждого компонента вершины при сравнении вершин, чтобы определить, достаточно ли они, чтобы они были связаны друг с другом.</span><span class="sxs-lookup"><span data-stu-id="bae23-104">Specifies tolerance values for each vertex component when comparing vertices to determine if they are similar enough to be welded together.</span></span>

## <a name="syntax"></a><span data-ttu-id="bae23-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bae23-105">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="bae23-106">Члены</span><span class="sxs-lookup"><span data-stu-id="bae23-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="bae23-107">**Позиция**</span><span class="sxs-lookup"><span data-stu-id="bae23-107">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="bae23-108">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bae23-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bae23-109">Положение</span><span class="sxs-lookup"><span data-stu-id="bae23-109">Position</span></span>

</dd> <dt>

<span data-ttu-id="bae23-110">**блендвеигхтс**</span><span class="sxs-lookup"><span data-stu-id="bae23-110">**BlendWeights**</span></span>
</dt> <dd>

<span data-ttu-id="bae23-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bae23-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bae23-112">Вес смешения</span><span class="sxs-lookup"><span data-stu-id="bae23-112">Blend weight</span></span>

</dd> <dt>

<span data-ttu-id="bae23-113">**Обычный**</span><span class="sxs-lookup"><span data-stu-id="bae23-113">**Normal**</span></span>
</dt> <dd>

<span data-ttu-id="bae23-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bae23-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bae23-115">Норм.</span><span class="sxs-lookup"><span data-stu-id="bae23-115">Normal</span></span>

</dd> <dt>

<span data-ttu-id="bae23-116">**псизе**</span><span class="sxs-lookup"><span data-stu-id="bae23-116">**PSize**</span></span>
</dt> <dd>

<span data-ttu-id="bae23-117">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bae23-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bae23-118">Значение размера точки</span><span class="sxs-lookup"><span data-stu-id="bae23-118">Point size value</span></span>

</dd> <dt>

<span data-ttu-id="bae23-119">**Отражающее**</span><span class="sxs-lookup"><span data-stu-id="bae23-119">**Specular**</span></span>
</dt> <dd>

<span data-ttu-id="bae23-120">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bae23-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bae23-121">Значение отраженного освещения</span><span class="sxs-lookup"><span data-stu-id="bae23-121">Specular lighting value</span></span>

</dd> <dt>

<span data-ttu-id="bae23-122">**Диффузное**</span><span class="sxs-lookup"><span data-stu-id="bae23-122">**Diffuse**</span></span>
</dt> <dd>

<span data-ttu-id="bae23-123">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bae23-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bae23-124">Рассеянное значение освещения</span><span class="sxs-lookup"><span data-stu-id="bae23-124">Diffuse lighting value</span></span>

</dd> <dt>

<span data-ttu-id="bae23-125">**текскурд**</span><span class="sxs-lookup"><span data-stu-id="bae23-125">**Texcoord**</span></span>
</dt> <dd>

<span data-ttu-id="bae23-126">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bae23-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bae23-127">Восемь координат текстуры</span><span class="sxs-lookup"><span data-stu-id="bae23-127">Eight texture coordinates</span></span>

</dd> <dt>

<span data-ttu-id="bae23-128">**Тангенс**</span><span class="sxs-lookup"><span data-stu-id="bae23-128">**Tangent**</span></span>
</dt> <dd>

<span data-ttu-id="bae23-129">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bae23-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bae23-130">Тангенс</span><span class="sxs-lookup"><span data-stu-id="bae23-130">Tangent</span></span>

</dd> <dt>

<span data-ttu-id="bae23-131">**бинормал**</span><span class="sxs-lookup"><span data-stu-id="bae23-131">**Binormal**</span></span>
</dt> <dd>

<span data-ttu-id="bae23-132">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bae23-132">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bae23-133">бинормал</span><span class="sxs-lookup"><span data-stu-id="bae23-133">Binormal</span></span>

</dd> <dt>

<span data-ttu-id="bae23-134">**тессфактор**</span><span class="sxs-lookup"><span data-stu-id="bae23-134">**TessFactor**</span></span>
</dt> <dd>

<span data-ttu-id="bae23-135">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bae23-135">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bae23-136">Фактор тесселяции</span><span class="sxs-lookup"><span data-stu-id="bae23-136">Tessellation factor</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bae23-137">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bae23-137">Remarks</span></span>

<span data-ttu-id="bae23-138">Тип LPD3DXWELDEPSILONS определяется как указатель на структуру **D3DXWELDEPSILONS** .</span><span class="sxs-lookup"><span data-stu-id="bae23-138">The LPD3DXWELDEPSILONS type is defined as a pointer to the **D3DXWELDEPSILONS** structure.</span></span>


```
typedef D3DXWELDEPSILONS *LPD3DXWELDEPSILONS;
```



## <a name="requirements"></a><span data-ttu-id="bae23-139">Требования</span><span class="sxs-lookup"><span data-stu-id="bae23-139">Requirements</span></span>



| <span data-ttu-id="bae23-140">Требование</span><span class="sxs-lookup"><span data-stu-id="bae23-140">Requirement</span></span> | <span data-ttu-id="bae23-141">Значение</span><span class="sxs-lookup"><span data-stu-id="bae23-141">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bae23-142">Header</span><span class="sxs-lookup"><span data-stu-id="bae23-142">Header</span></span><br/> | <dl> <span data-ttu-id="bae23-143"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="bae23-143"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bae23-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bae23-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bae23-145">Структуры D3DX</span><span class="sxs-lookup"><span data-stu-id="bae23-145">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="bae23-146">**D3DXWeldVertices**</span><span class="sxs-lookup"><span data-stu-id="bae23-146">**D3DXWeldVertices**</span></span>](d3dxweldvertices.md)
</dt> </dl>

 

 
