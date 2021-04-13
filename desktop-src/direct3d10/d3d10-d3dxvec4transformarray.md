---
description: Преобразует массив (x, y, z, w) по заданной матрице.
ms.assetid: afd5cccb-e22f-4726-a84e-9eac1c1c277f
title: Функция D3DXVec4TransformArray (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4TransformArray
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 5571fb19786e19a61c85741bcf6d4acb5231e977
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105647865"
---
# <a name="d3dxvec4transformarray-function-d3dx10mathh"></a><span data-ttu-id="35a23-103">Функция D3DXVec4TransformArray (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="35a23-103">D3DXVec4TransformArray function (D3DX10Math.h)</span></span>

<span data-ttu-id="35a23-104">Преобразует массив (x, y, z, w) по заданной матрице.</span><span class="sxs-lookup"><span data-stu-id="35a23-104">Transforms an array (x, y, z, w) by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="35a23-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="35a23-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4TransformArray(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_          UINT        OutStride,
  _In_    const D3DXVECTOR4 *pV,
  _In_          UINT        VStride,
  _In_    const D3DXMATRIX  *pM,
  _In_          UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="35a23-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="35a23-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35a23-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="35a23-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="35a23-108">Тип: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="35a23-108">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="35a23-109">Указатель на массив [**D3DXVECTOR4**](d3d10-d3dxvector4.md) , который является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="35a23-109">Pointer to the [**D3DXVECTOR4**](d3d10-d3dxvector4.md) array that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="35a23-110">*Шаг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="35a23-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35a23-111">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="35a23-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="35a23-112">Шаг между векторами в потоке выходных данных.</span><span class="sxs-lookup"><span data-stu-id="35a23-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="35a23-113">*ПС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="35a23-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35a23-114">Тип: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="35a23-114">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="35a23-115">Указатель на исходный массив D3DXVECTOR4.</span><span class="sxs-lookup"><span data-stu-id="35a23-115">Pointer to the source D3DXVECTOR4 array.</span></span>

</dd> <dt>

<span data-ttu-id="35a23-116">*Встриде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="35a23-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35a23-117">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="35a23-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="35a23-118">Шаг между векторами во входном потоке данных.</span><span class="sxs-lookup"><span data-stu-id="35a23-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="35a23-119">*PM* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="35a23-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35a23-120">Тип: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="35a23-120">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="35a23-121">Указатель на исходную структуру [**D3DXMATRIX**](d3d10-d3dxmatrix.md) .</span><span class="sxs-lookup"><span data-stu-id="35a23-121">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="35a23-122">*n* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="35a23-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35a23-123">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="35a23-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="35a23-124">Число элементов в массиве.</span><span class="sxs-lookup"><span data-stu-id="35a23-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35a23-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="35a23-125">Return value</span></span>

<span data-ttu-id="35a23-126">Тип: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="35a23-126">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="35a23-127">Указатель на структуру [**D3DXVECTOR4**](d3d10-d3dxvector4.md) , которая является преобразованным массивом.</span><span class="sxs-lookup"><span data-stu-id="35a23-127">Pointer to a [**D3DXVECTOR4**](d3d10-d3dxvector4.md) structure that is the transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="35a23-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="35a23-128">Remarks</span></span>

<span data-ttu-id="35a23-129">Эта функция преобразует массив ПС (x, y, z, w) на матрицу pM.</span><span class="sxs-lookup"><span data-stu-id="35a23-129">This function transforms the array pV (x, y, z, w) by the matrix pM.</span></span>

<span data-ttu-id="35a23-130">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="35a23-130">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="35a23-131">Таким образом, функция **D3DXVec4TransformArray** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="35a23-131">In this way, the **D3DXVec4TransformArray** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="35a23-132">Требования</span><span class="sxs-lookup"><span data-stu-id="35a23-132">Requirements</span></span>



| <span data-ttu-id="35a23-133">Требование</span><span class="sxs-lookup"><span data-stu-id="35a23-133">Requirement</span></span> | <span data-ttu-id="35a23-134">Значение</span><span class="sxs-lookup"><span data-stu-id="35a23-134">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="35a23-135">Header</span><span class="sxs-lookup"><span data-stu-id="35a23-135">Header</span></span><br/> | <dl> <span data-ttu-id="35a23-136"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="35a23-136"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35a23-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="35a23-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35a23-138">Математические функции</span><span class="sxs-lookup"><span data-stu-id="35a23-138">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
