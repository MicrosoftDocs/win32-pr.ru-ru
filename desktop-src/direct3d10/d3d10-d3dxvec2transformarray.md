---
description: Преобразует массив (x, y, 0, 1) по заданной матрице.
ms.assetid: 66c8909c-6c20-4b32-9546-fcf2d0e824fa
title: Функция D3DXVec2TransformArray (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2TransformArray
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c5aef5ecaa720e8c859d37f03ce88223187d16f0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103914732"
---
# <a name="d3dxvec2transformarray-function-d3dx10mathh"></a><span data-ttu-id="f21e8-103">Функция D3DXVec2TransformArray (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="f21e8-103">D3DXVec2TransformArray function (D3DX10Math.h)</span></span>

<span data-ttu-id="f21e8-104">Преобразует массив (x, y, 0, 1) по заданной матрице.</span><span class="sxs-lookup"><span data-stu-id="f21e8-104">Transforms an array (x, y, 0, 1) by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="f21e8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f21e8-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec2TransformArray(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_          UINT        OutStride,
  _In_    const D3DXVECTOR2 *pV,
  _In_          UINT        VStride,
  _In_    const D3DXMATRIX  *pM,
  _In_          UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="f21e8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f21e8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f21e8-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="f21e8-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f21e8-108">Тип: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="f21e8-108">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="f21e8-109">Указатель на структуру [**D3DXVECTOR4**](d3d10-d3dxvector4.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="f21e8-109">Pointer to the [**D3DXVECTOR4**](d3d10-d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="f21e8-110">*Шаг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f21e8-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f21e8-111">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f21e8-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f21e8-112">Шаг между векторами в потоке выходных данных.</span><span class="sxs-lookup"><span data-stu-id="f21e8-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="f21e8-113">*ПС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f21e8-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f21e8-114">Тип: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="f21e8-114">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="f21e8-115">Указатель на источник [**D3DXVECTOR2**](d3d10-d3dxvector2.md).</span><span class="sxs-lookup"><span data-stu-id="f21e8-115">Pointer to the source [**D3DXVECTOR2**](d3d10-d3dxvector2.md).</span></span>

</dd> <dt>

<span data-ttu-id="f21e8-116">*Встриде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f21e8-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f21e8-117">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f21e8-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f21e8-118">Шаг между векторами во входном потоке данных.</span><span class="sxs-lookup"><span data-stu-id="f21e8-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="f21e8-119">*PM* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f21e8-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f21e8-120">Тип: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="f21e8-120">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f21e8-121">Указатель на исходную структуру [**D3DXMATRIX**](d3d10-d3dxmatrix.md) .</span><span class="sxs-lookup"><span data-stu-id="f21e8-121">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="f21e8-122">*n* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="f21e8-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f21e8-123">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f21e8-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f21e8-124">Число элементов в массиве.</span><span class="sxs-lookup"><span data-stu-id="f21e8-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f21e8-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f21e8-125">Return value</span></span>

<span data-ttu-id="f21e8-126">Тип: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="f21e8-126">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="f21e8-127">Указатель на структуру D3DXVECTOR4, которая является преобразованным массивом.</span><span class="sxs-lookup"><span data-stu-id="f21e8-127">Pointer to a D3DXVECTOR4 structure that is the transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="f21e8-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f21e8-128">Remarks</span></span>

<span data-ttu-id="f21e8-129">Эта функция преобразует массив ПС (x, y, 0, 1) на матрицу pM.</span><span class="sxs-lookup"><span data-stu-id="f21e8-129">This function transforms the array pV (x, y, 0, 1) by the matrix pM.</span></span>

<span data-ttu-id="f21e8-130">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="f21e8-130">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="f21e8-131">Таким образом, функция [**D3DXVec2Transform**](d3d10-d3dxvec2transform.md) может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="f21e8-131">In this way, the [**D3DXVec2Transform**](d3d10-d3dxvec2transform.md) function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="f21e8-132">Требования</span><span class="sxs-lookup"><span data-stu-id="f21e8-132">Requirements</span></span>



| <span data-ttu-id="f21e8-133">Требование</span><span class="sxs-lookup"><span data-stu-id="f21e8-133">Requirement</span></span> | <span data-ttu-id="f21e8-134">Значение</span><span class="sxs-lookup"><span data-stu-id="f21e8-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f21e8-135">Header</span><span class="sxs-lookup"><span data-stu-id="f21e8-135">Header</span></span><br/>  | <dl> <span data-ttu-id="f21e8-136"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="f21e8-136"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="f21e8-137">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f21e8-137">Library</span></span><br/> | <dl> <span data-ttu-id="f21e8-138"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f21e8-138"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f21e8-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f21e8-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f21e8-140">Математические функции</span><span class="sxs-lookup"><span data-stu-id="f21e8-140">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
