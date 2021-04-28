---
description: Функция D3DXVec3TransformCoordArray (D3DX10Math. h) — преобразует массив (x, y, z, 1) по заданной матрице и проецирует результат обратно в w = 1.
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
ms.openlocfilehash: c4a1edfd89b127d0782d3bab23c2390775422c69
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103112"
---
# <a name="d3dxvec3transformcoordarray-function-d3dx10mathh"></a><span data-ttu-id="bbb88-103">Функция D3DXVec3TransformCoordArray (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="bbb88-103">D3DXVec3TransformCoordArray function (D3DX10Math.h)</span></span>

<span data-ttu-id="bbb88-104">Преобразует массив (x, y, z, 1) по заданной матрице и проецирует результат обратно в w = 1.</span><span class="sxs-lookup"><span data-stu-id="bbb88-104">Transforms an array (x, y, z, 1) by a given matrix, and projects the result back into w = 1.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbb88-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bbb88-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="bbb88-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bbb88-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bbb88-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="bbb88-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="bbb88-108">Тип: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="bbb88-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="bbb88-109">Указатель на [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , который является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="bbb88-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="bbb88-110">*Шаг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bbb88-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bbb88-111">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bbb88-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bbb88-112">Шаг между векторами в потоке выходных данных.</span><span class="sxs-lookup"><span data-stu-id="bbb88-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="bbb88-113">*ПС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bbb88-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bbb88-114">Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="bbb88-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="bbb88-115">Указатель на исходный массив D3DXVECTOR3.</span><span class="sxs-lookup"><span data-stu-id="bbb88-115">Pointer to the source D3DXVECTOR3 array.</span></span>

</dd> <dt>

<span data-ttu-id="bbb88-116">*Встриде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bbb88-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bbb88-117">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bbb88-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bbb88-118">Шаг между векторами во входном потоке данных.</span><span class="sxs-lookup"><span data-stu-id="bbb88-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="bbb88-119">*PM* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bbb88-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bbb88-120">Тип: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="bbb88-120">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="bbb88-121">Указатель на исходную структуру [**D3DXMATRIX**](d3d10-d3dxmatrix.md) .</span><span class="sxs-lookup"><span data-stu-id="bbb88-121">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="bbb88-122">*n* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="bbb88-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bbb88-123">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bbb88-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bbb88-124">Число элементов в массиве.</span><span class="sxs-lookup"><span data-stu-id="bbb88-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bbb88-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bbb88-125">Return value</span></span>

<span data-ttu-id="bbb88-126">Тип: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="bbb88-126">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="bbb88-127">Указатель на структуру D3DXVECTOR3, которая является преобразованным массивом.</span><span class="sxs-lookup"><span data-stu-id="bbb88-127">Pointer to a D3DXVECTOR3 structure that is the transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="bbb88-128">Remarks</span><span class="sxs-lookup"><span data-stu-id="bbb88-128">Remarks</span></span>

<span data-ttu-id="bbb88-129">Эта функция преобразует массив ПС (x, y, z, 1) на матрицу pM, проецирование результата обратно в w = 1.</span><span class="sxs-lookup"><span data-stu-id="bbb88-129">This function transforms the array pV (x, y, z, 1) by the matrix pM, projecting the result back into w = 1.</span></span>

<span data-ttu-id="bbb88-130">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="bbb88-130">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="bbb88-131">Таким образом, функция [**D3DXVec3TransformCoord**](d3d10-d3dxvec3transformcoord.md) может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="bbb88-131">In this way, the [**D3DXVec3TransformCoord**](d3d10-d3dxvec3transformcoord.md) function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="bbb88-132">Требования</span><span class="sxs-lookup"><span data-stu-id="bbb88-132">Requirements</span></span>



| <span data-ttu-id="bbb88-133">Требование</span><span class="sxs-lookup"><span data-stu-id="bbb88-133">Requirement</span></span> | <span data-ttu-id="bbb88-134">Значение</span><span class="sxs-lookup"><span data-stu-id="bbb88-134">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bbb88-135">Header</span><span class="sxs-lookup"><span data-stu-id="bbb88-135">Header</span></span><br/> | <dl> <span data-ttu-id="bbb88-136"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="bbb88-136"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bbb88-137">См. также</span><span class="sxs-lookup"><span data-stu-id="bbb88-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbb88-138">Математические функции</span><span class="sxs-lookup"><span data-stu-id="bbb88-138">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
