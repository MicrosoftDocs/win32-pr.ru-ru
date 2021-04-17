---
description: Преобразует массив (x, y, 0, 0) в заданную матрицу.
ms.assetid: a53f998a-f2a5-4e4b-bc1c-c1f46284d78b
title: Функция D3DXVec2TransformNormalArray (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2TransformNormalArray
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4850961560ae810b9a21f58fbefa9b6b07227c77
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694244"
---
# <a name="d3dxvec2transformnormalarray-function-d3dx10mathh"></a><span data-ttu-id="798ea-103">Функция D3DXVec2TransformNormalArray (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="798ea-103">D3DXVec2TransformNormalArray function (D3DX10Math.h)</span></span>

<span data-ttu-id="798ea-104">Преобразует массив (x, y, 0, 0) в заданную матрицу.</span><span class="sxs-lookup"><span data-stu-id="798ea-104">Transforms an array (x, y, 0, 0) by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="798ea-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="798ea-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2TransformNormalArray(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_          UINT        OutStride,
  _In_    const D3DXVECTOR2 *pV,
  _In_          UINT        VStride,
  _In_    const D3DXMATRIX  *pM,
  _In_          UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="798ea-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="798ea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="798ea-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="798ea-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="798ea-108">Тип: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="798ea-108">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="798ea-109">Указатель на [**D3DXVECTOR2**](d3d10-d3dxvector2.md) , который является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="798ea-109">Pointer to the [**D3DXVECTOR2**](d3d10-d3dxvector2.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="798ea-110">*Шаг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="798ea-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="798ea-111">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="798ea-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="798ea-112">Шаг между векторами в потоке выходных данных.</span><span class="sxs-lookup"><span data-stu-id="798ea-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="798ea-113">*ПС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="798ea-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="798ea-114">Тип: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="798ea-114">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="798ea-115">Указатель на исходный массив D3DXVECTOR2.</span><span class="sxs-lookup"><span data-stu-id="798ea-115">Pointer to the source D3DXVECTOR2 array.</span></span>

</dd> <dt>

<span data-ttu-id="798ea-116">*Встриде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="798ea-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="798ea-117">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="798ea-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="798ea-118">Шаг между векторами во входном потоке данных.</span><span class="sxs-lookup"><span data-stu-id="798ea-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="798ea-119">*PM* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="798ea-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="798ea-120">Тип: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="798ea-120">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="798ea-121">Указатель на исходную структуру [**D3DXMATRIX**](d3d10-d3dxmatrix.md) .</span><span class="sxs-lookup"><span data-stu-id="798ea-121">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="798ea-122">*n* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="798ea-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="798ea-123">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="798ea-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="798ea-124">Число элементов в массиве.</span><span class="sxs-lookup"><span data-stu-id="798ea-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="798ea-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="798ea-125">Return value</span></span>

<span data-ttu-id="798ea-126">Тип: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="798ea-126">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="798ea-127">Указатель на структуру D3DXVECTOR2, которая является преобразованным массивом.</span><span class="sxs-lookup"><span data-stu-id="798ea-127">Pointer to a D3DXVECTOR2 structure that is the transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="798ea-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="798ea-128">Remarks</span></span>

<span data-ttu-id="798ea-129">Эта функция преобразует вектор (pV->x, pV->y, 0, 0) на матрицу, на которую указывает pM.</span><span class="sxs-lookup"><span data-stu-id="798ea-129">This function transforms the vector (pV->x, pV->y, 0, 0) by the matrix pointed to by pM.</span></span>

<span data-ttu-id="798ea-130">Если необходимо преобразовать обычное значение, то матрица, передаваемая в эту функцию, должна быть преобразована обратно в матрицу, которая будет использоваться для преобразования точки.</span><span class="sxs-lookup"><span data-stu-id="798ea-130">If you want to transform a normal, the matrix you pass to this function should be the transpose of the inverse of the matrix you would use to transform a point.</span></span>

<span data-ttu-id="798ea-131">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="798ea-131">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="798ea-132">Таким образом, функция **D3DXVec2TransformNormalArray** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="798ea-132">In this way, the **D3DXVec2TransformNormalArray** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="798ea-133">Требования</span><span class="sxs-lookup"><span data-stu-id="798ea-133">Requirements</span></span>



| <span data-ttu-id="798ea-134">Требование</span><span class="sxs-lookup"><span data-stu-id="798ea-134">Requirement</span></span> | <span data-ttu-id="798ea-135">Значение</span><span class="sxs-lookup"><span data-stu-id="798ea-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="798ea-136">Header</span><span class="sxs-lookup"><span data-stu-id="798ea-136">Header</span></span><br/>  | <dl> <span data-ttu-id="798ea-137"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="798ea-137"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="798ea-138">Библиотека</span><span class="sxs-lookup"><span data-stu-id="798ea-138">Library</span></span><br/> | <dl> <span data-ttu-id="798ea-139"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="798ea-139"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="798ea-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="798ea-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="798ea-141">Математические функции</span><span class="sxs-lookup"><span data-stu-id="798ea-141">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
