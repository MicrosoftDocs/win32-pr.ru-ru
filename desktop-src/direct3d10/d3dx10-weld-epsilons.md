---
description: D3DX10_WELD_EPSILONSная структура — задает значения допуска для каждого компонента вершины при сравнении вершин, чтобы определить, достаточно ли они для разаппаратного разшва.
ms.assetid: b28a17bd-5d5b-41b3-86d9-327f5497fc94
title: Структура D3DX10_WELD_EPSILONS (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_WELD_EPSILONS
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: 720a10dbe4b22b69910d88d3c03cea9ded768f1b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105432"
---
# <a name="d3dx10_weld_epsilons-structure"></a><span data-ttu-id="5c317-103">\_ \_ Структура Эпсилон D3DX10ного шва</span><span class="sxs-lookup"><span data-stu-id="5c317-103">D3DX10\_WELD\_EPSILONS structure</span></span>

<span data-ttu-id="5c317-104">Задает значения допуска для каждого компонента вершины при сравнении вершин, чтобы определить, достаточно ли они, чтобы они были связаны друг с другом.</span><span class="sxs-lookup"><span data-stu-id="5c317-104">Specifies tolerance values for each vertex component when comparing vertices to determine if they are similar enough to be welded together.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c317-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5c317-105">Syntax</span></span>


```C++
typedef struct D3DX10_WELD_EPSILONS {
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
} D3DX10_WELD_EPSILONS, *LPD3DX10_WELD_EPSILONS;
```



## <a name="members"></a><span data-ttu-id="5c317-106">Члены</span><span class="sxs-lookup"><span data-stu-id="5c317-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="5c317-107">**Позиция**</span><span class="sxs-lookup"><span data-stu-id="5c317-107">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="5c317-108">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5c317-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5c317-109">Положение</span><span class="sxs-lookup"><span data-stu-id="5c317-109">Position</span></span>

</dd> <dt>

<span data-ttu-id="5c317-110">**блендвеигхтс**</span><span class="sxs-lookup"><span data-stu-id="5c317-110">**BlendWeights**</span></span>
</dt> <dd>

<span data-ttu-id="5c317-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5c317-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5c317-112">Вес смешения</span><span class="sxs-lookup"><span data-stu-id="5c317-112">Blend weight</span></span>

</dd> <dt>

<span data-ttu-id="5c317-113">**Обычный**</span><span class="sxs-lookup"><span data-stu-id="5c317-113">**Normal**</span></span>
</dt> <dd>

<span data-ttu-id="5c317-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5c317-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5c317-115">Норм.</span><span class="sxs-lookup"><span data-stu-id="5c317-115">Normal</span></span>

</dd> <dt>

<span data-ttu-id="5c317-116">**псизе**</span><span class="sxs-lookup"><span data-stu-id="5c317-116">**PSize**</span></span>
</dt> <dd>

<span data-ttu-id="5c317-117">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5c317-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5c317-118">Значение размера точки</span><span class="sxs-lookup"><span data-stu-id="5c317-118">Point size value</span></span>

</dd> <dt>

<span data-ttu-id="5c317-119">**Отражающее**</span><span class="sxs-lookup"><span data-stu-id="5c317-119">**Specular**</span></span>
</dt> <dd>

<span data-ttu-id="5c317-120">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5c317-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5c317-121">Значение отраженного освещения</span><span class="sxs-lookup"><span data-stu-id="5c317-121">Specular lighting value</span></span>

</dd> <dt>

<span data-ttu-id="5c317-122">**Диффузное**</span><span class="sxs-lookup"><span data-stu-id="5c317-122">**Diffuse**</span></span>
</dt> <dd>

<span data-ttu-id="5c317-123">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5c317-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5c317-124">Рассеянное значение освещения</span><span class="sxs-lookup"><span data-stu-id="5c317-124">Diffuse lighting value</span></span>

</dd> <dt>

<span data-ttu-id="5c317-125">**текскурд**</span><span class="sxs-lookup"><span data-stu-id="5c317-125">**Texcoord**</span></span>
</dt> <dd>

<span data-ttu-id="5c317-126">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5c317-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5c317-127">Восемь координат текстуры</span><span class="sxs-lookup"><span data-stu-id="5c317-127">Eight texture coordinates</span></span>

</dd> <dt>

<span data-ttu-id="5c317-128">**Тангенс**</span><span class="sxs-lookup"><span data-stu-id="5c317-128">**Tangent**</span></span>
</dt> <dd>

<span data-ttu-id="5c317-129">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5c317-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5c317-130">Тангенс</span><span class="sxs-lookup"><span data-stu-id="5c317-130">Tangent</span></span>

</dd> <dt>

<span data-ttu-id="5c317-131">**бинормал**</span><span class="sxs-lookup"><span data-stu-id="5c317-131">**Binormal**</span></span>
</dt> <dd>

<span data-ttu-id="5c317-132">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5c317-132">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5c317-133">бинормал</span><span class="sxs-lookup"><span data-stu-id="5c317-133">Binormal</span></span>

</dd> <dt>

<span data-ttu-id="5c317-134">**тессфактор**</span><span class="sxs-lookup"><span data-stu-id="5c317-134">**TessFactor**</span></span>
</dt> <dd>

<span data-ttu-id="5c317-135">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5c317-135">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5c317-136">Фактор тесселяции</span><span class="sxs-lookup"><span data-stu-id="5c317-136">Tessellation factor</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5c317-137">Remarks</span><span class="sxs-lookup"><span data-stu-id="5c317-137">Remarks</span></span>

<span data-ttu-id="5c317-138">Тип LPD3DXWeldEpsilons определяется как указатель на структуру D3DXWeldEpsilons.</span><span class="sxs-lookup"><span data-stu-id="5c317-138">The LPD3DXWeldEpsilons type is defined as a pointer to the D3DXWeldEpsilons structure.</span></span>


```
typedef D3DX_WELD_EPSILONS *LPD3DX_WELD_EPSILONS;
```



## <a name="requirements"></a><span data-ttu-id="5c317-139">Требования</span><span class="sxs-lookup"><span data-stu-id="5c317-139">Requirements</span></span>



| <span data-ttu-id="5c317-140">Требование</span><span class="sxs-lookup"><span data-stu-id="5c317-140">Requirement</span></span> | <span data-ttu-id="5c317-141">Значение</span><span class="sxs-lookup"><span data-stu-id="5c317-141">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5c317-142">Header</span><span class="sxs-lookup"><span data-stu-id="5c317-142">Header</span></span><br/> | <dl> <span data-ttu-id="5c317-143"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c317-143"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c317-144">См. также</span><span class="sxs-lookup"><span data-stu-id="5c317-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c317-145">Структуры D3DX</span><span class="sxs-lookup"><span data-stu-id="5c317-145">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
