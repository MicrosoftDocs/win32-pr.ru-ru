---
description: Преобразует массив (x, y, 0, 1) по заданной матрице и проецирует результат обратно в w = 1.
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
ms.openlocfilehash: aa57d96b0497fea572e580cfe6d1af2a0184f09d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694245"
---
# <a name="d3dxvec2transformcoordarray-function-d3dx10mathh"></a><span data-ttu-id="93d40-103">Функция D3DXVec2TransformCoordArray (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="93d40-103">D3DXVec2TransformCoordArray function (D3DX10Math.h)</span></span>

<span data-ttu-id="93d40-104">Преобразует массив (x, y, 0, 1) по заданной матрице и проецирует результат обратно в w = 1.</span><span class="sxs-lookup"><span data-stu-id="93d40-104">Transforms an array (x, y, 0, 1) by a given matrix, and projects the result back into w = 1.</span></span>

## <a name="syntax"></a><span data-ttu-id="93d40-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="93d40-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="93d40-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="93d40-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93d40-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="93d40-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="93d40-108">Тип: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="93d40-108">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="93d40-109">Указатель на [**D3DXVECTOR2**](d3d10-d3dxvector2.md) , который является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="93d40-109">Pointer to the [**D3DXVECTOR2**](d3d10-d3dxvector2.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="93d40-110">*Шаг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="93d40-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93d40-111">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="93d40-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="93d40-112">Шаг между векторами в потоке выходных данных.</span><span class="sxs-lookup"><span data-stu-id="93d40-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="93d40-113">*ПС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="93d40-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93d40-114">Тип: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="93d40-114">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="93d40-115">Указатель на исходный массив D3DXVECTOR2.</span><span class="sxs-lookup"><span data-stu-id="93d40-115">Pointer to the source D3DXVECTOR2 array.</span></span>

</dd> <dt>

<span data-ttu-id="93d40-116">*Встриде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="93d40-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93d40-117">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="93d40-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="93d40-118">Шаг между векторами во входном потоке данных.</span><span class="sxs-lookup"><span data-stu-id="93d40-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="93d40-119">*PM* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="93d40-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93d40-120">Тип: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="93d40-120">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="93d40-121">Указатель на исходную структуру [**D3DXMATRIX**](d3d10-d3dxmatrix.md) .</span><span class="sxs-lookup"><span data-stu-id="93d40-121">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="93d40-122">*n* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="93d40-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93d40-123">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="93d40-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="93d40-124">Число элементов в массиве.</span><span class="sxs-lookup"><span data-stu-id="93d40-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93d40-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="93d40-125">Return value</span></span>

<span data-ttu-id="93d40-126">Тип: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="93d40-126">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="93d40-127">Указатель на преобразованный массив [**D3DXVECTOR4**](d3d10-d3dxvector4.md) .</span><span class="sxs-lookup"><span data-stu-id="93d40-127">Pointer to a [**D3DXVECTOR4**](d3d10-d3dxvector4.md) transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="93d40-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="93d40-128">Remarks</span></span>

<span data-ttu-id="93d40-129">Эта функция преобразует массив ПС (x, y, 0, 1) на матрицу pM, проецирование результата обратно в w = 1.</span><span class="sxs-lookup"><span data-stu-id="93d40-129">This function transforms the array pV (x, y, 0, 1) by the matrix pM, projecting the result back into w = 1.</span></span>

<span data-ttu-id="93d40-130">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="93d40-130">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="93d40-131">Таким образом, функция D3DXVec2TransformCoordArray может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="93d40-131">In this way, the D3DXVec2TransformCoordArray function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="93d40-132">Требования</span><span class="sxs-lookup"><span data-stu-id="93d40-132">Requirements</span></span>



| <span data-ttu-id="93d40-133">Требование</span><span class="sxs-lookup"><span data-stu-id="93d40-133">Requirement</span></span> | <span data-ttu-id="93d40-134">Значение</span><span class="sxs-lookup"><span data-stu-id="93d40-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="93d40-135">Header</span><span class="sxs-lookup"><span data-stu-id="93d40-135">Header</span></span><br/>  | <dl> <span data-ttu-id="93d40-136"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="93d40-136"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="93d40-137">Библиотека</span><span class="sxs-lookup"><span data-stu-id="93d40-137">Library</span></span><br/> | <dl> <span data-ttu-id="93d40-138"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="93d40-138"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="93d40-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="93d40-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93d40-140">Математические функции</span><span class="sxs-lookup"><span data-stu-id="93d40-140">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
