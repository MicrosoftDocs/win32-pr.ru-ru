---
description: Задает атрибуты веса сетки.
ms.assetid: 554bb8f2-9e92-4e9e-b500-c3cc47d57830
title: Структура D3DX10_ATTRIBUTE_WEIGHTS (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_ATTRIBUTE_WEIGHTS
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: 4f137c1ecc29c184c4dec3995fb0202741ce9f09
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355110"
---
# <a name="d3dx10_attribute_weights-structure"></a><span data-ttu-id="31cf0-103">\_ \_ Структура весовых коэффициентов атрибутов D3DX10</span><span class="sxs-lookup"><span data-stu-id="31cf0-103">D3DX10\_ATTRIBUTE\_WEIGHTS structure</span></span>

<span data-ttu-id="31cf0-104">Задает атрибуты веса сетки.</span><span class="sxs-lookup"><span data-stu-id="31cf0-104">Specifies mesh weight attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="31cf0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="31cf0-105">Syntax</span></span>


```C++
typedef struct D3DX10_ATTRIBUTE_WEIGHTS {
  FLOAT Position;
  FLOAT Boundary;
  FLOAT Normal;
  FLOAT Diffuse;
  FLOAT Specular;
  FLOAT Texcoord[8];
  FLOAT Tangent;
  FLOAT Binormal;
} D3DX10_ATTRIBUTE_WEIGHTS, *LPD3DX10_ATTRIBUTE_WEIGHTS;
```



## <a name="members"></a><span data-ttu-id="31cf0-106">Члены</span><span class="sxs-lookup"><span data-stu-id="31cf0-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="31cf0-107">**Позиция**</span><span class="sxs-lookup"><span data-stu-id="31cf0-107">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="31cf0-108">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="31cf0-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="31cf0-109">Положение.</span><span class="sxs-lookup"><span data-stu-id="31cf0-109">Position.</span></span>

</dd> <dt>

<span data-ttu-id="31cf0-110">**Граница**</span><span class="sxs-lookup"><span data-stu-id="31cf0-110">**Boundary**</span></span>
</dt> <dd>

<span data-ttu-id="31cf0-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="31cf0-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="31cf0-112">Вес смешения.</span><span class="sxs-lookup"><span data-stu-id="31cf0-112">Blend weight.</span></span>

</dd> <dt>

<span data-ttu-id="31cf0-113">**Обычный**</span><span class="sxs-lookup"><span data-stu-id="31cf0-113">**Normal**</span></span>
</dt> <dd>

<span data-ttu-id="31cf0-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="31cf0-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="31cf0-115">Нормальный.</span><span class="sxs-lookup"><span data-stu-id="31cf0-115">Normal.</span></span>

</dd> <dt>

<span data-ttu-id="31cf0-116">**Диффузное**</span><span class="sxs-lookup"><span data-stu-id="31cf0-116">**Diffuse**</span></span>
</dt> <dd>

<span data-ttu-id="31cf0-117">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="31cf0-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="31cf0-118">Рассеянное значение освещения.</span><span class="sxs-lookup"><span data-stu-id="31cf0-118">Diffuse lighting value.</span></span>

</dd> <dt>

<span data-ttu-id="31cf0-119">**Отражающее**</span><span class="sxs-lookup"><span data-stu-id="31cf0-119">**Specular**</span></span>
</dt> <dd>

<span data-ttu-id="31cf0-120">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="31cf0-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="31cf0-121">Значение отраженного освещения.</span><span class="sxs-lookup"><span data-stu-id="31cf0-121">Specular lighting value.</span></span>

</dd> <dt>

<span data-ttu-id="31cf0-122">**текскурд**</span><span class="sxs-lookup"><span data-stu-id="31cf0-122">**Texcoord**</span></span>
</dt> <dd>

<span data-ttu-id="31cf0-123">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="31cf0-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="31cf0-124">Восемь координат текстуры.</span><span class="sxs-lookup"><span data-stu-id="31cf0-124">Eight texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="31cf0-125">**Тангенс**</span><span class="sxs-lookup"><span data-stu-id="31cf0-125">**Tangent**</span></span>
</dt> <dd>

<span data-ttu-id="31cf0-126">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="31cf0-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="31cf0-127">Тангенс.</span><span class="sxs-lookup"><span data-stu-id="31cf0-127">Tangent.</span></span>

</dd> <dt>

<span data-ttu-id="31cf0-128">**бинормал**</span><span class="sxs-lookup"><span data-stu-id="31cf0-128">**Binormal**</span></span>
</dt> <dd>

<span data-ttu-id="31cf0-129">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="31cf0-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="31cf0-130">Бинормал.</span><span class="sxs-lookup"><span data-stu-id="31cf0-130">Binormal.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="31cf0-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="31cf0-131">Remarks</span></span>

<span data-ttu-id="31cf0-132">Эта структура описывает, как операция упрощения будет учитывать данные вершин при вычислении относительных затрат между свертыванием краев.</span><span class="sxs-lookup"><span data-stu-id="31cf0-132">This structure describes how a simplification operation will consider vertex data when calculating relative costs between collapsing edges.</span></span> <span data-ttu-id="31cf0-133">Например, если значение обычного поля равно 0,0, то при вычислении ошибки для сворачивания операция упрощения будет игнорировать компонент нормали вершины.</span><span class="sxs-lookup"><span data-stu-id="31cf0-133">For example, if the Normal field is 0.0, the simplification operation will ignore the vertex normal component when calculating the error for the collapse.</span></span> <span data-ttu-id="31cf0-134">Однако если значение обычного поля равно 1,0, то операция упрощения будет использовать компонент нормали вершины.</span><span class="sxs-lookup"><span data-stu-id="31cf0-134">However, if the Normal field is 1.0, the simplification operation will use the vertex normal component.</span></span> <span data-ttu-id="31cf0-135">Если значение обычного поля равно 2,0, удваивается количество ошибок. Если значение обычного поля равно 4,0, то число ошибок и т. д.</span><span class="sxs-lookup"><span data-stu-id="31cf0-135">If the Normal field is 2.0, double the amount of errors; if the Normal field is 4.0, then quadruple the number of errors, and so on.</span></span>

<span data-ttu-id="31cf0-136">\_ \_ Тип веса атрибута LPD3DX определяется как указатель на \_ \_ структуру веса атрибута D3DX.</span><span class="sxs-lookup"><span data-stu-id="31cf0-136">The LPD3DX\_ATTRIBUTE\_WEIGHTS type is defined as a pointer to the D3DX\_ATTRIBUTE\_WEIGHTS structure.</span></span>


```
    typedef D3DX_ATTRIBUTE_WEIGHTS* LPD3DX_ATTRIBUTE_WEIGHTS;
```



## <a name="requirements"></a><span data-ttu-id="31cf0-137">Требования</span><span class="sxs-lookup"><span data-stu-id="31cf0-137">Requirements</span></span>



| <span data-ttu-id="31cf0-138">Требование</span><span class="sxs-lookup"><span data-stu-id="31cf0-138">Requirement</span></span> | <span data-ttu-id="31cf0-139">Значение</span><span class="sxs-lookup"><span data-stu-id="31cf0-139">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="31cf0-140">Header</span><span class="sxs-lookup"><span data-stu-id="31cf0-140">Header</span></span><br/> | <dl> <span data-ttu-id="31cf0-141"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="31cf0-141"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31cf0-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="31cf0-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31cf0-143">Структуры D3DX</span><span class="sxs-lookup"><span data-stu-id="31cf0-143">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
