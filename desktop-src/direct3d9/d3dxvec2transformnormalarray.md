---
description: Функция D3DXVec2TransformNormalArray (D3dx9math. h) — преобразует массив (x, y, 0, 0) по заданной матрице.
ms.assetid: 9f5d8fdc-f3e1-41dc-be4e-9ffc6be1947f
title: Функция D3DXVec2TransformNormalArray (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 71706551e73ed9bd52b41aae127625cd09b6d7f8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097900"
---
# <a name="d3dxvec2transformnormalarray-function-d3dx9mathh"></a><span data-ttu-id="713a9-103">Функция D3DXVec2TransformNormalArray (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="713a9-103">D3DXVec2TransformNormalArray function (D3dx9math.h)</span></span>

<span data-ttu-id="713a9-104">Преобразует массив (x, y, 0, 0) в заданную матрицу.</span><span class="sxs-lookup"><span data-stu-id="713a9-104">Transforms an array (x, y, 0, 0) by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="713a9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="713a9-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="713a9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="713a9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="713a9-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="713a9-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="713a9-108">Тип: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="713a9-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="713a9-109">Указатель на структуру [**D3DXVECTOR2**](d3dxvector2.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="713a9-109">Pointer to the [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="713a9-110">*Шаг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="713a9-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="713a9-111">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="713a9-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="713a9-112">Шаг между векторами в потоке выходных данных.</span><span class="sxs-lookup"><span data-stu-id="713a9-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="713a9-113">*ПС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="713a9-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="713a9-114">Тип: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="713a9-114">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="713a9-115">Указатель на исходный массив [**D3DXVECTOR2**](d3dxvector2.md) .</span><span class="sxs-lookup"><span data-stu-id="713a9-115">Pointer to the source [**D3DXVECTOR2**](d3dxvector2.md) array.</span></span>

</dd> <dt>

<span data-ttu-id="713a9-116">*Встриде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="713a9-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="713a9-117">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="713a9-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="713a9-118">Шаг между векторами во входном потоке данных.</span><span class="sxs-lookup"><span data-stu-id="713a9-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="713a9-119">*PM* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="713a9-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="713a9-120">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="713a9-120">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="713a9-121">Указатель на исходную структуру [**D3DXMATRIX**](d3dxmatrix.md) .</span><span class="sxs-lookup"><span data-stu-id="713a9-121">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="713a9-122">*n* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="713a9-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="713a9-123">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="713a9-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="713a9-124">Число элементов в массиве.</span><span class="sxs-lookup"><span data-stu-id="713a9-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="713a9-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="713a9-125">Return value</span></span>

<span data-ttu-id="713a9-126">Тип: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="713a9-126">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="713a9-127">Указатель на структуру [**D3DXVECTOR2**](d3dxvector2.md) , которая является преобразованным массивом.</span><span class="sxs-lookup"><span data-stu-id="713a9-127">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that is the transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="713a9-128">Remarks</span><span class="sxs-lookup"><span data-stu-id="713a9-128">Remarks</span></span>

<span data-ttu-id="713a9-129">Эта функция преобразует вектор (*PV-*>x, *pV-*>y, 0, 0) на матрицу, на которую указывает *PM.*</span><span class="sxs-lookup"><span data-stu-id="713a9-129">This function transforms the vector (*pV-*>x, *pV-*>y, 0, 0) by the matrix pointed to by *pM.*</span></span>

<span data-ttu-id="713a9-130">Если необходимо преобразовать обычное значение, то матрица, передаваемая в эту функцию, должна быть преобразована обратно в матрицу, которая будет использоваться для преобразования точки.</span><span class="sxs-lookup"><span data-stu-id="713a9-130">If you want to transform a normal, the matrix you pass to this function should be the transpose of the inverse of the matrix you would use to transform a point.</span></span>

<span data-ttu-id="713a9-131">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="713a9-131">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="713a9-132">Таким образом, функция **D3DXVec2TransformNormalArray** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="713a9-132">In this way, the **D3DXVec2TransformNormalArray** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="713a9-133">Требования</span><span class="sxs-lookup"><span data-stu-id="713a9-133">Requirements</span></span>



| <span data-ttu-id="713a9-134">Требование</span><span class="sxs-lookup"><span data-stu-id="713a9-134">Requirement</span></span> | <span data-ttu-id="713a9-135">Значение</span><span class="sxs-lookup"><span data-stu-id="713a9-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="713a9-136">Header</span><span class="sxs-lookup"><span data-stu-id="713a9-136">Header</span></span><br/>  | <dl> <span data-ttu-id="713a9-137"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="713a9-137"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="713a9-138">Библиотека</span><span class="sxs-lookup"><span data-stu-id="713a9-138">Library</span></span><br/> | <dl> <span data-ttu-id="713a9-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="713a9-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="713a9-140">См. также</span><span class="sxs-lookup"><span data-stu-id="713a9-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="713a9-141">Математические функции</span><span class="sxs-lookup"><span data-stu-id="713a9-141">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
