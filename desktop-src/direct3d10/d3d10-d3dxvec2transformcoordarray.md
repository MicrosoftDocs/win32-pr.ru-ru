---
description: Функция D3DXVec2TransformCoordArray (D3DX10Math. h) — преобразует массив (x, y, 0, 1) по заданной матрице и проецирует результат обратно в w = 1.
ms.assetid: dba68678-2ab4-4f64-9975-5e9f2a20f66a
title: Функция D3DXVec2TransformCoordArray (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2TransformCoordArray
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: f36b5fb5a5263f83c42ac66cc5f606fa1c4b75ab
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108332"
---
# <a name="d3dxvec2transformcoordarray-function-d3dx10mathh"></a><span data-ttu-id="7b5d9-103">Функция D3DXVec2TransformCoordArray (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="7b5d9-103">D3DXVec2TransformCoordArray function (D3DX10Math.h)</span></span>

<span data-ttu-id="7b5d9-104">Преобразует массив (x, y, 0, 1) по заданной матрице и проецирует результат обратно в w = 1.</span><span class="sxs-lookup"><span data-stu-id="7b5d9-104">Transforms an array (x, y, 0, 1) by a given matrix, and projects the result back into w = 1.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b5d9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7b5d9-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2TransformCoordArray(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_          UINT        OutStride,
  _In_    const D3DXVECTOR2 *pV,
  _In_          UINT        VStride,
  _In_    const D3DXMATRIX  *pM,
  _In_          UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="7b5d9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7b5d9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b5d9-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="7b5d9-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7b5d9-108">Тип: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="7b5d9-108">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="7b5d9-109">Указатель на [**D3DXVECTOR2**](d3d10-d3dxvector2.md) , который является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="7b5d9-109">Pointer to the [**D3DXVECTOR2**](d3d10-d3dxvector2.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="7b5d9-110">*Шаг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7b5d9-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b5d9-111">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7b5d9-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7b5d9-112">Шаг между векторами в потоке выходных данных.</span><span class="sxs-lookup"><span data-stu-id="7b5d9-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="7b5d9-113">*ПС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7b5d9-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b5d9-114">Тип: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="7b5d9-114">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="7b5d9-115">Указатель на исходный массив D3DXVECTOR2.</span><span class="sxs-lookup"><span data-stu-id="7b5d9-115">Pointer to the source D3DXVECTOR2 array.</span></span>

</dd> <dt>

<span data-ttu-id="7b5d9-116">*Встриде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7b5d9-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b5d9-117">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7b5d9-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7b5d9-118">Шаг между векторами во входном потоке данных.</span><span class="sxs-lookup"><span data-stu-id="7b5d9-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="7b5d9-119">*PM* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7b5d9-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b5d9-120">Тип: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="7b5d9-120">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="7b5d9-121">Указатель на исходную структуру [**D3DXMATRIX**](d3d10-d3dxmatrix.md) .</span><span class="sxs-lookup"><span data-stu-id="7b5d9-121">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="7b5d9-122">*n* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="7b5d9-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b5d9-123">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7b5d9-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7b5d9-124">Число элементов в массиве.</span><span class="sxs-lookup"><span data-stu-id="7b5d9-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b5d9-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7b5d9-125">Return value</span></span>

<span data-ttu-id="7b5d9-126">Тип: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="7b5d9-126">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="7b5d9-127">Указатель на преобразованный массив [**D3DXVECTOR4**](d3d10-d3dxvector4.md) .</span><span class="sxs-lookup"><span data-stu-id="7b5d9-127">Pointer to a [**D3DXVECTOR4**](d3d10-d3dxvector4.md) transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b5d9-128">Remarks</span><span class="sxs-lookup"><span data-stu-id="7b5d9-128">Remarks</span></span>

<span data-ttu-id="7b5d9-129">Эта функция преобразует массив ПС (x, y, 0, 1) на матрицу pM, проецирование результата обратно в w = 1.</span><span class="sxs-lookup"><span data-stu-id="7b5d9-129">This function transforms the array pV (x, y, 0, 1) by the matrix pM, projecting the result back into w = 1.</span></span>

<span data-ttu-id="7b5d9-130">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="7b5d9-130">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="7b5d9-131">Таким образом, функция D3DXVec2TransformCoordArray может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="7b5d9-131">In this way, the D3DXVec2TransformCoordArray function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b5d9-132">Требования</span><span class="sxs-lookup"><span data-stu-id="7b5d9-132">Requirements</span></span>



| <span data-ttu-id="7b5d9-133">Требование</span><span class="sxs-lookup"><span data-stu-id="7b5d9-133">Requirement</span></span> | <span data-ttu-id="7b5d9-134">Значение</span><span class="sxs-lookup"><span data-stu-id="7b5d9-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7b5d9-135">Header</span><span class="sxs-lookup"><span data-stu-id="7b5d9-135">Header</span></span><br/>  | <dl> <span data-ttu-id="7b5d9-136"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b5d9-136"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="7b5d9-137">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7b5d9-137">Library</span></span><br/> | <dl> <span data-ttu-id="7b5d9-138"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7b5d9-138"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7b5d9-139">См. также</span><span class="sxs-lookup"><span data-stu-id="7b5d9-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b5d9-140">Математические функции</span><span class="sxs-lookup"><span data-stu-id="7b5d9-140">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
