---
description: Задает значения допуска для каждого компонента вершины при сравнении вершин, чтобы определить, достаточно ли они, чтобы они были связаны друг с другом.
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
ms.openlocfilehash: c72f63e3ecef1fdb193fcaec9220f9768204d099
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713775"
---
# <a name="d3dx10_weld_epsilons-structure"></a><span data-ttu-id="d734b-103">\_ \_ Структура Эпсилон D3DX10ного шва</span><span class="sxs-lookup"><span data-stu-id="d734b-103">D3DX10\_WELD\_EPSILONS structure</span></span>

<span data-ttu-id="d734b-104">Задает значения допуска для каждого компонента вершины при сравнении вершин, чтобы определить, достаточно ли они, чтобы они были связаны друг с другом.</span><span class="sxs-lookup"><span data-stu-id="d734b-104">Specifies tolerance values for each vertex component when comparing vertices to determine if they are similar enough to be welded together.</span></span>

## <a name="syntax"></a><span data-ttu-id="d734b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d734b-105">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="d734b-106">Члены</span><span class="sxs-lookup"><span data-stu-id="d734b-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="d734b-107">**Позиция**</span><span class="sxs-lookup"><span data-stu-id="d734b-107">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="d734b-108">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d734b-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d734b-109">Положение</span><span class="sxs-lookup"><span data-stu-id="d734b-109">Position</span></span>

</dd> <dt>

<span data-ttu-id="d734b-110">**блендвеигхтс**</span><span class="sxs-lookup"><span data-stu-id="d734b-110">**BlendWeights**</span></span>
</dt> <dd>

<span data-ttu-id="d734b-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d734b-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d734b-112">Вес смешения</span><span class="sxs-lookup"><span data-stu-id="d734b-112">Blend weight</span></span>

</dd> <dt>

<span data-ttu-id="d734b-113">**Обычный**</span><span class="sxs-lookup"><span data-stu-id="d734b-113">**Normal**</span></span>
</dt> <dd>

<span data-ttu-id="d734b-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d734b-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d734b-115">Норм.</span><span class="sxs-lookup"><span data-stu-id="d734b-115">Normal</span></span>

</dd> <dt>

<span data-ttu-id="d734b-116">**псизе**</span><span class="sxs-lookup"><span data-stu-id="d734b-116">**PSize**</span></span>
</dt> <dd>

<span data-ttu-id="d734b-117">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d734b-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d734b-118">Значение размера точки</span><span class="sxs-lookup"><span data-stu-id="d734b-118">Point size value</span></span>

</dd> <dt>

<span data-ttu-id="d734b-119">**Отражающее**</span><span class="sxs-lookup"><span data-stu-id="d734b-119">**Specular**</span></span>
</dt> <dd>

<span data-ttu-id="d734b-120">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d734b-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d734b-121">Значение отраженного освещения</span><span class="sxs-lookup"><span data-stu-id="d734b-121">Specular lighting value</span></span>

</dd> <dt>

<span data-ttu-id="d734b-122">**Диффузное**</span><span class="sxs-lookup"><span data-stu-id="d734b-122">**Diffuse**</span></span>
</dt> <dd>

<span data-ttu-id="d734b-123">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d734b-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d734b-124">Рассеянное значение освещения</span><span class="sxs-lookup"><span data-stu-id="d734b-124">Diffuse lighting value</span></span>

</dd> <dt>

<span data-ttu-id="d734b-125">**текскурд**</span><span class="sxs-lookup"><span data-stu-id="d734b-125">**Texcoord**</span></span>
</dt> <dd>

<span data-ttu-id="d734b-126">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d734b-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d734b-127">Восемь координат текстуры</span><span class="sxs-lookup"><span data-stu-id="d734b-127">Eight texture coordinates</span></span>

</dd> <dt>

<span data-ttu-id="d734b-128">**Тангенс**</span><span class="sxs-lookup"><span data-stu-id="d734b-128">**Tangent**</span></span>
</dt> <dd>

<span data-ttu-id="d734b-129">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d734b-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d734b-130">Тангенс</span><span class="sxs-lookup"><span data-stu-id="d734b-130">Tangent</span></span>

</dd> <dt>

<span data-ttu-id="d734b-131">**бинормал**</span><span class="sxs-lookup"><span data-stu-id="d734b-131">**Binormal**</span></span>
</dt> <dd>

<span data-ttu-id="d734b-132">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d734b-132">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d734b-133">бинормал</span><span class="sxs-lookup"><span data-stu-id="d734b-133">Binormal</span></span>

</dd> <dt>

<span data-ttu-id="d734b-134">**тессфактор**</span><span class="sxs-lookup"><span data-stu-id="d734b-134">**TessFactor**</span></span>
</dt> <dd>

<span data-ttu-id="d734b-135">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d734b-135">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d734b-136">Фактор тесселяции</span><span class="sxs-lookup"><span data-stu-id="d734b-136">Tessellation factor</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d734b-137">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d734b-137">Remarks</span></span>

<span data-ttu-id="d734b-138">Тип LPD3DXWeldEpsilons определяется как указатель на структуру D3DXWeldEpsilons.</span><span class="sxs-lookup"><span data-stu-id="d734b-138">The LPD3DXWeldEpsilons type is defined as a pointer to the D3DXWeldEpsilons structure.</span></span>


```
typedef D3DX_WELD_EPSILONS *LPD3DX_WELD_EPSILONS;
```



## <a name="requirements"></a><span data-ttu-id="d734b-139">Требования</span><span class="sxs-lookup"><span data-stu-id="d734b-139">Requirements</span></span>



| <span data-ttu-id="d734b-140">Требование</span><span class="sxs-lookup"><span data-stu-id="d734b-140">Requirement</span></span> | <span data-ttu-id="d734b-141">Значение</span><span class="sxs-lookup"><span data-stu-id="d734b-141">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d734b-142">Header</span><span class="sxs-lookup"><span data-stu-id="d734b-142">Header</span></span><br/> | <dl> <span data-ttu-id="d734b-143"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="d734b-143"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d734b-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d734b-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d734b-145">Структуры D3DX</span><span class="sxs-lookup"><span data-stu-id="d734b-145">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
