---
description: Преобразует массив (x, y, z, 1) по заданной матрице и проецирует результат обратно в w = 1.
ms.assetid: 259a885d-89be-4fea-a579-dac3dd76878f
title: Функция D3DXVec3TransformCoordArray (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformCoordArray
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: b0b7ca3c2898e07dc8b5e9ced0117e642bfdfb41
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000394"
---
# <a name="d3dxvec3transformcoordarray-function-d3dx10mathh"></a><span data-ttu-id="c0efe-103">Функция D3DXVec3TransformCoordArray (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="c0efe-103">D3DXVec3TransformCoordArray function (D3DX10Math.h)</span></span>

<span data-ttu-id="c0efe-104">Преобразует массив (x, y, z, 1) по заданной матрице и проецирует результат обратно в w = 1.</span><span class="sxs-lookup"><span data-stu-id="c0efe-104">Transforms an array (x, y, z, 1) by a given matrix, and projects the result back into w = 1.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0efe-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c0efe-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3TransformCoordArray(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_          UINT        OutStride,
  _In_    const D3DXVECTOR3 *pV,
  _In_          UINT        VStride,
  _In_    const D3DXMATRIX  *pM,
  _In_          UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="c0efe-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c0efe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0efe-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="c0efe-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c0efe-108">Тип: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="c0efe-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="c0efe-109">Указатель на [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , который является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="c0efe-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="c0efe-110">*Шаг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c0efe-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0efe-111">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c0efe-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c0efe-112">Шаг между векторами в потоке выходных данных.</span><span class="sxs-lookup"><span data-stu-id="c0efe-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="c0efe-113">*ПС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c0efe-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0efe-114">Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="c0efe-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="c0efe-115">Указатель на исходный массив D3DXVECTOR3.</span><span class="sxs-lookup"><span data-stu-id="c0efe-115">Pointer to the source D3DXVECTOR3 array.</span></span>

</dd> <dt>

<span data-ttu-id="c0efe-116">*Встриде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c0efe-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0efe-117">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c0efe-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c0efe-118">Шаг между векторами во входном потоке данных.</span><span class="sxs-lookup"><span data-stu-id="c0efe-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="c0efe-119">*PM* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c0efe-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0efe-120">Тип: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="c0efe-120">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c0efe-121">Указатель на исходную структуру [**D3DXMATRIX**](d3d10-d3dxmatrix.md) .</span><span class="sxs-lookup"><span data-stu-id="c0efe-121">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="c0efe-122">*n* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="c0efe-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0efe-123">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c0efe-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c0efe-124">Число элементов в массиве.</span><span class="sxs-lookup"><span data-stu-id="c0efe-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0efe-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c0efe-125">Return value</span></span>

<span data-ttu-id="c0efe-126">Тип: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="c0efe-126">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="c0efe-127">Указатель на структуру D3DXVECTOR3, которая является преобразованным массивом.</span><span class="sxs-lookup"><span data-stu-id="c0efe-127">Pointer to a D3DXVECTOR3 structure that is the transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0efe-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c0efe-128">Remarks</span></span>

<span data-ttu-id="c0efe-129">Эта функция преобразует массив ПС (x, y, z, 1) на матрицу pM, проецирование результата обратно в w = 1.</span><span class="sxs-lookup"><span data-stu-id="c0efe-129">This function transforms the array pV (x, y, z, 1) by the matrix pM, projecting the result back into w = 1.</span></span>

<span data-ttu-id="c0efe-130">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="c0efe-130">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="c0efe-131">Таким образом, функция [**D3DXVec3TransformCoord**](d3d10-d3dxvec3transformcoord.md) может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="c0efe-131">In this way, the [**D3DXVec3TransformCoord**](d3d10-d3dxvec3transformcoord.md) function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0efe-132">Требования</span><span class="sxs-lookup"><span data-stu-id="c0efe-132">Requirements</span></span>



| <span data-ttu-id="c0efe-133">Требование</span><span class="sxs-lookup"><span data-stu-id="c0efe-133">Requirement</span></span> | <span data-ttu-id="c0efe-134">Значение</span><span class="sxs-lookup"><span data-stu-id="c0efe-134">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c0efe-135">Header</span><span class="sxs-lookup"><span data-stu-id="c0efe-135">Header</span></span><br/> | <dl> <span data-ttu-id="c0efe-136"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0efe-136"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0efe-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c0efe-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0efe-138">Математические функции</span><span class="sxs-lookup"><span data-stu-id="c0efe-138">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
