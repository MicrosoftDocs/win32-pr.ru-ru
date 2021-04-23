---
description: Преобразует массив (x, y, z, 1) в заданную матрицу.
ms.assetid: f64c55df-ea93-4c93-be89-eee650e6ecf0
title: Функция D3DXVec3TransformArray (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformArray
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 9ae223d4e1b8c424230ba12719f25258dae18548
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104081910"
---
# <a name="d3dxvec3transformarray-function-d3dx10mathh"></a><span data-ttu-id="54d1a-103">Функция D3DXVec3TransformArray (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="54d1a-103">D3DXVec3TransformArray function (D3DX10Math.h)</span></span>

<span data-ttu-id="54d1a-104">Преобразует массив (x, y, z, 1) в заданную матрицу.</span><span class="sxs-lookup"><span data-stu-id="54d1a-104">Transforms an array (x, y, z, 1) by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="54d1a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="54d1a-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec3TransformArray(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_          UINT        OutStride,
  _In_    const D3DXVECTOR3 *pV,
  _In_          UINT        VStride,
  _In_    const D3DXMATRIX  *pM,
  _In_          UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="54d1a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="54d1a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54d1a-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="54d1a-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="54d1a-108">Тип: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="54d1a-108">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="54d1a-109">Указатель на массив [**D3DXVECTOR4**](d3d10-d3dxvector4.md) , который является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="54d1a-109">Pointer to the [**D3DXVECTOR4**](d3d10-d3dxvector4.md) array that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="54d1a-110">*Шаг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="54d1a-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54d1a-111">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="54d1a-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="54d1a-112">Шаг между векторами в потоке выходных данных.</span><span class="sxs-lookup"><span data-stu-id="54d1a-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="54d1a-113">*ПС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="54d1a-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54d1a-114">Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="54d1a-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="54d1a-115">Указатель на исходный массив [**D3DXVECTOR3**](d3d10-d3dxvector3.md) .</span><span class="sxs-lookup"><span data-stu-id="54d1a-115">Pointer to the source [**D3DXVECTOR3**](d3d10-d3dxvector3.md) array.</span></span>

</dd> <dt>

<span data-ttu-id="54d1a-116">*Встриде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="54d1a-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54d1a-117">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="54d1a-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="54d1a-118">Шаг между векторами во входном потоке данных.</span><span class="sxs-lookup"><span data-stu-id="54d1a-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="54d1a-119">*PM* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="54d1a-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54d1a-120">Тип: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="54d1a-120">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="54d1a-121">Указатель на исходную структуру [**D3DXMATRIX**](d3d10-d3dxmatrix.md) .</span><span class="sxs-lookup"><span data-stu-id="54d1a-121">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="54d1a-122">*n* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="54d1a-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54d1a-123">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="54d1a-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="54d1a-124">Число элементов в массиве.</span><span class="sxs-lookup"><span data-stu-id="54d1a-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54d1a-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="54d1a-125">Return value</span></span>

<span data-ttu-id="54d1a-126">Тип: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="54d1a-126">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="54d1a-127">Указатель на преобразованный массив [**D3DXVECTOR4**](d3d10-d3dxvector4.md) .</span><span class="sxs-lookup"><span data-stu-id="54d1a-127">Pointer to a [**D3DXVECTOR4**](d3d10-d3dxvector4.md) transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="54d1a-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="54d1a-128">Remarks</span></span>

<span data-ttu-id="54d1a-129">Эта функция преобразует массив ПС (x, y, z, 1) матрицей pM.</span><span class="sxs-lookup"><span data-stu-id="54d1a-129">This function transforms the array pV (x, y, z, 1) by the matrix pM.</span></span>

<span data-ttu-id="54d1a-130">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="54d1a-130">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="54d1a-131">Таким образом, функция D3DXVec3TransformArray может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="54d1a-131">In this way, the D3DXVec3TransformArray function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="54d1a-132">Требования</span><span class="sxs-lookup"><span data-stu-id="54d1a-132">Requirements</span></span>



| <span data-ttu-id="54d1a-133">Требование</span><span class="sxs-lookup"><span data-stu-id="54d1a-133">Requirement</span></span> | <span data-ttu-id="54d1a-134">Значение</span><span class="sxs-lookup"><span data-stu-id="54d1a-134">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="54d1a-135">Header</span><span class="sxs-lookup"><span data-stu-id="54d1a-135">Header</span></span><br/> | <dl> <span data-ttu-id="54d1a-136"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="54d1a-136"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54d1a-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="54d1a-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54d1a-138">Математические функции</span><span class="sxs-lookup"><span data-stu-id="54d1a-138">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
