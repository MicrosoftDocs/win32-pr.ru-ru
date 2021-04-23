---
description: Преобразует массив (x, y, z, 0) в заданную матрицу.
ms.assetid: 7f0a41ce-bd3a-4e35-9a5d-8178a4e7bd44
title: Функция D3DXVec3TransformNormalArray (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformNormalArray
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: facb5591becd27d3fff283e8d531118ca433d5d2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105674682"
---
# <a name="d3dxvec3transformnormalarray-function-d3dx10mathh"></a><span data-ttu-id="8a3a5-103">Функция D3DXVec3TransformNormalArray (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="8a3a5-103">D3DXVec3TransformNormalArray function (D3DX10Math.h)</span></span>

<span data-ttu-id="8a3a5-104">Преобразует массив (x, y, z, 0) в заданную матрицу.</span><span class="sxs-lookup"><span data-stu-id="8a3a5-104">Transforms an array (x, y, z, 0) by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a3a5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8a3a5-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3TransformNormalArray(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_          UINT        OutStride,
  _In_    const D3DXVECTOR3 *pV,
  _In_          UINT        VStride,
  _In_    const D3DXMATRIX  *pM,
  _In_          UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="8a3a5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8a3a5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a3a5-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="8a3a5-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8a3a5-108">Тип: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="8a3a5-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="8a3a5-109">Указатель на массив [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , который является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="8a3a5-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) array that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="8a3a5-110">*Шаг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8a3a5-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a3a5-111">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8a3a5-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8a3a5-112">Шаг между векторами в потоке выходных данных.</span><span class="sxs-lookup"><span data-stu-id="8a3a5-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="8a3a5-113">*ПС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8a3a5-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a3a5-114">Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="8a3a5-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="8a3a5-115">Указатель на исходный массив D3DXVECTOR3.</span><span class="sxs-lookup"><span data-stu-id="8a3a5-115">Pointer to the source D3DXVECTOR3 array.</span></span>

</dd> <dt>

<span data-ttu-id="8a3a5-116">*Встриде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8a3a5-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a3a5-117">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8a3a5-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8a3a5-118">Шаг между векторами во входном потоке данных.</span><span class="sxs-lookup"><span data-stu-id="8a3a5-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="8a3a5-119">*PM* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8a3a5-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a3a5-120">Тип: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="8a3a5-120">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="8a3a5-121">Указатель на исходную структуру [**D3DXMATRIX**](d3d10-d3dxmatrix.md) .</span><span class="sxs-lookup"><span data-stu-id="8a3a5-121">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="8a3a5-122">*n* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="8a3a5-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a3a5-123">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8a3a5-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8a3a5-124">Число элементов в массиве.</span><span class="sxs-lookup"><span data-stu-id="8a3a5-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a3a5-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8a3a5-125">Return value</span></span>

<span data-ttu-id="8a3a5-126">Тип: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="8a3a5-126">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="8a3a5-127">Указатель на массив D3DXVECTOR3, который является преобразованным массивом.</span><span class="sxs-lookup"><span data-stu-id="8a3a5-127">Pointer to a D3DXVECTOR3 array that is the transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a3a5-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8a3a5-128">Remarks</span></span>

<span data-ttu-id="8a3a5-129">Эта функция преобразует вектор (ПС->x, pV->y, pV->z, 0) матрице, на которую указывает pM.</span><span class="sxs-lookup"><span data-stu-id="8a3a5-129">This function transforms the vector (pV->x, pV->y, pV->z, 0) by the matrix pointed to by pM.</span></span>

<span data-ttu-id="8a3a5-130">Если необходимо преобразовать обычное значение, то матрица, передаваемая в эту функцию, должна быть преобразована обратно в матрицу, которая будет использоваться для преобразования точки.</span><span class="sxs-lookup"><span data-stu-id="8a3a5-130">If you want to transform a normal, the matrix you pass to this function should be the transpose of the inverse of the matrix you would use to transform a point.</span></span>

<span data-ttu-id="8a3a5-131">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="8a3a5-131">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="8a3a5-132">Таким образом, функция **D3DXVec3TransformNormalArray** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="8a3a5-132">In this way, the **D3DXVec3TransformNormalArray** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a3a5-133">Требования</span><span class="sxs-lookup"><span data-stu-id="8a3a5-133">Requirements</span></span>



| <span data-ttu-id="8a3a5-134">Требование</span><span class="sxs-lookup"><span data-stu-id="8a3a5-134">Requirement</span></span> | <span data-ttu-id="8a3a5-135">Значение</span><span class="sxs-lookup"><span data-stu-id="8a3a5-135">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8a3a5-136">Header</span><span class="sxs-lookup"><span data-stu-id="8a3a5-136">Header</span></span><br/> | <dl> <span data-ttu-id="8a3a5-137"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a3a5-137"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a3a5-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8a3a5-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a3a5-139">Математические функции</span><span class="sxs-lookup"><span data-stu-id="8a3a5-139">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
