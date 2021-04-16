---
description: Задает атрибуты веса сетки.
ms.assetid: 8901a0fe-e38a-4045-8e8d-584be2620cc3
title: Структура D3DXATTRIBUTEWEIGHTS (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXATTRIBUTEWEIGHTS
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 49725e410fb700c7ecb93fd56a8db367d7f982a0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105720903"
---
# <a name="d3dxattributeweights-structure"></a><span data-ttu-id="0437e-103">Структура D3DXATTRIBUTEWEIGHTS</span><span class="sxs-lookup"><span data-stu-id="0437e-103">D3DXATTRIBUTEWEIGHTS structure</span></span>

<span data-ttu-id="0437e-104">Задает атрибуты веса сетки.</span><span class="sxs-lookup"><span data-stu-id="0437e-104">Specifies mesh weight attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="0437e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0437e-105">Syntax</span></span>


```C++
typedef struct D3DXATTRIBUTEWEIGHTS {
  FLOAT Position;
  FLOAT Boundary;
  FLOAT Normal;
  FLOAT Diffuse;
  FLOAT Specular;
  FLOAT Texcoord[8];
  FLOAT Tangent;
  FLOAT Binormal;
} D3DXATTRIBUTEWEIGHTS, *LPD3DXATTRIBUTEWEIGHTS;
```



## <a name="members"></a><span data-ttu-id="0437e-106">Члены</span><span class="sxs-lookup"><span data-stu-id="0437e-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="0437e-107">**Позиция**</span><span class="sxs-lookup"><span data-stu-id="0437e-107">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="0437e-108">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0437e-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0437e-109">Положение.</span><span class="sxs-lookup"><span data-stu-id="0437e-109">Position.</span></span>

</dd> <dt>

<span data-ttu-id="0437e-110">**Граница**</span><span class="sxs-lookup"><span data-stu-id="0437e-110">**Boundary**</span></span>
</dt> <dd>

<span data-ttu-id="0437e-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0437e-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0437e-112">Вес смешения.</span><span class="sxs-lookup"><span data-stu-id="0437e-112">Blend weight.</span></span>

</dd> <dt>

<span data-ttu-id="0437e-113">**Обычный**</span><span class="sxs-lookup"><span data-stu-id="0437e-113">**Normal**</span></span>
</dt> <dd>

<span data-ttu-id="0437e-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0437e-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0437e-115">Нормальный.</span><span class="sxs-lookup"><span data-stu-id="0437e-115">Normal.</span></span>

</dd> <dt>

<span data-ttu-id="0437e-116">**Диффузное**</span><span class="sxs-lookup"><span data-stu-id="0437e-116">**Diffuse**</span></span>
</dt> <dd>

<span data-ttu-id="0437e-117">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0437e-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0437e-118">Рассеянное значение освещения.</span><span class="sxs-lookup"><span data-stu-id="0437e-118">Diffuse lighting value.</span></span>

</dd> <dt>

<span data-ttu-id="0437e-119">**Отражающее**</span><span class="sxs-lookup"><span data-stu-id="0437e-119">**Specular**</span></span>
</dt> <dd>

<span data-ttu-id="0437e-120">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0437e-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0437e-121">Значение отраженного освещения.</span><span class="sxs-lookup"><span data-stu-id="0437e-121">Specular lighting value.</span></span>

</dd> <dt>

<span data-ttu-id="0437e-122">**текскурд**</span><span class="sxs-lookup"><span data-stu-id="0437e-122">**Texcoord**</span></span>
</dt> <dd>

<span data-ttu-id="0437e-123">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0437e-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0437e-124">Восемь координат текстуры.</span><span class="sxs-lookup"><span data-stu-id="0437e-124">Eight texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="0437e-125">**Тангенс**</span><span class="sxs-lookup"><span data-stu-id="0437e-125">**Tangent**</span></span>
</dt> <dd>

<span data-ttu-id="0437e-126">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0437e-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0437e-127">Тангенс.</span><span class="sxs-lookup"><span data-stu-id="0437e-127">Tangent.</span></span>

</dd> <dt>

<span data-ttu-id="0437e-128">**бинормал**</span><span class="sxs-lookup"><span data-stu-id="0437e-128">**Binormal**</span></span>
</dt> <dd>

<span data-ttu-id="0437e-129">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0437e-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="0437e-130">Бинормал.</span><span class="sxs-lookup"><span data-stu-id="0437e-130">Binormal.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0437e-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0437e-131">Remarks</span></span>

<span data-ttu-id="0437e-132">Эта структура описывает, как операция упрощения будет учитывать данные вершин при вычислении относительных затрат между свертыванием краев.</span><span class="sxs-lookup"><span data-stu-id="0437e-132">This structure describes how a simplification operation will consider vertex data when calculating relative costs between collapsing edges.</span></span> <span data-ttu-id="0437e-133">Например, если значение обычного поля равно 0,0, то при вычислении ошибки для сворачивания операция упрощения будет игнорировать компонент нормали вершины.</span><span class="sxs-lookup"><span data-stu-id="0437e-133">For example, if the Normal field is 0.0, the simplification operation will ignore the vertex normal component when calculating the error for the collapse.</span></span> <span data-ttu-id="0437e-134">Однако если значение обычного поля равно 1,0, то операция упрощения будет использовать компонент нормали вершины.</span><span class="sxs-lookup"><span data-stu-id="0437e-134">However, if the Normal field is 1.0, the simplification operation will use the vertex normal component.</span></span> <span data-ttu-id="0437e-135">Если значение обычного поля равно 2,0, удваивается количество ошибок. Если значение обычного поля равно 4,0, то число ошибок и т. д.</span><span class="sxs-lookup"><span data-stu-id="0437e-135">If the Normal field is 2.0, double the amount of errors; if the Normal field is 4.0, then quadruple the number of errors, and so on.</span></span>

<span data-ttu-id="0437e-136">Тип LPD3DXATTRIBUTEWEIGHTS определяется как указатель на структуру **D3DXATTRIBUTEWEIGHTS** .</span><span class="sxs-lookup"><span data-stu-id="0437e-136">The LPD3DXATTRIBUTEWEIGHTS type is defined as a pointer to the **D3DXATTRIBUTEWEIGHTS** structure.</span></span>


```
    
    typedef D3DXATTRIBUTEWEIGHTS* LPD3DXATTRIBUTEWEIGHTS;
```



## <a name="requirements"></a><span data-ttu-id="0437e-137">Требования</span><span class="sxs-lookup"><span data-stu-id="0437e-137">Requirements</span></span>



| <span data-ttu-id="0437e-138">Требование</span><span class="sxs-lookup"><span data-stu-id="0437e-138">Requirement</span></span> | <span data-ttu-id="0437e-139">Значение</span><span class="sxs-lookup"><span data-stu-id="0437e-139">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0437e-140">Header</span><span class="sxs-lookup"><span data-stu-id="0437e-140">Header</span></span><br/> | <dl> <span data-ttu-id="0437e-141"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="0437e-141"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0437e-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0437e-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0437e-143">Структуры D3DX</span><span class="sxs-lookup"><span data-stu-id="0437e-143">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="0437e-144">**D3DXSimplifyMesh**</span><span class="sxs-lookup"><span data-stu-id="0437e-144">**D3DXSimplifyMesh**</span></span>](d3dxsimplifymesh.md)
</dt> </dl>

 

 
