---
description: Функция D3DXVec3TransformCoordArray (D3dx9math. h) — преобразует массив (x, y, z, 1) по заданной матрице и проецирует результат обратно в w = 1.
ms.assetid: f1595861-d8cb-4787-8078-b9ba6f76507e
title: Функция D3DXVec3TransformCoordArray (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformCoordArray
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c373705307b2529b3d05609fc4b6ffb47d3abcc2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097752"
---
# <a name="d3dxvec3transformcoordarray-function-d3dx9mathh"></a><span data-ttu-id="28a49-103">Функция D3DXVec3TransformCoordArray (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="28a49-103">D3DXVec3TransformCoordArray function (D3dx9math.h)</span></span>

<span data-ttu-id="28a49-104">Преобразует массив (x, y, z, 1) по заданной матрице и проецирует результат обратно в w = 1.</span><span class="sxs-lookup"><span data-stu-id="28a49-104">Transforms an array (x, y, z, 1) by a given matrix, and projects the result back into w = 1.</span></span>

## <a name="syntax"></a><span data-ttu-id="28a49-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="28a49-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="28a49-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="28a49-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28a49-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="28a49-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="28a49-108">Тип: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="28a49-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="28a49-109">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="28a49-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="28a49-110">*Шаг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="28a49-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28a49-111">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="28a49-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="28a49-112">Шаг между векторами в потоке выходных данных.</span><span class="sxs-lookup"><span data-stu-id="28a49-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="28a49-113">*ПС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="28a49-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28a49-114">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="28a49-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="28a49-115">Указатель на исходный массив [**D3DXVECTOR3**](d3dxvector3.md) .</span><span class="sxs-lookup"><span data-stu-id="28a49-115">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) array.</span></span>

</dd> <dt>

<span data-ttu-id="28a49-116">*Встриде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="28a49-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28a49-117">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="28a49-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="28a49-118">Шаг между векторами во входном потоке данных.</span><span class="sxs-lookup"><span data-stu-id="28a49-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="28a49-119">*PM* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="28a49-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28a49-120">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="28a49-120">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="28a49-121">Указатель на исходную структуру [**D3DXMATRIX**](d3dxmatrix.md) .</span><span class="sxs-lookup"><span data-stu-id="28a49-121">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="28a49-122">*n* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="28a49-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28a49-123">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="28a49-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="28a49-124">Число элементов в массиве.</span><span class="sxs-lookup"><span data-stu-id="28a49-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28a49-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="28a49-125">Return value</span></span>

<span data-ttu-id="28a49-126">Тип: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="28a49-126">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="28a49-127">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , которая является преобразованным массивом.</span><span class="sxs-lookup"><span data-stu-id="28a49-127">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="28a49-128">Remarks</span><span class="sxs-lookup"><span data-stu-id="28a49-128">Remarks</span></span>

<span data-ttu-id="28a49-129">Эта функция преобразует массив *ПС (* x, y, z, 1) на матрицу *PM*, проецирование результата обратно в w = 1.</span><span class="sxs-lookup"><span data-stu-id="28a49-129">This function transforms the array *pV (* x, y, z, 1) by the matrix *pM*, projecting the result back into w = 1.</span></span>

<span data-ttu-id="28a49-130">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="28a49-130">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="28a49-131">Таким образом, функция [**D3DXVec3TransformCoord**](d3dxvec3transformcoord.md) может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="28a49-131">In this way, the [**D3DXVec3TransformCoord**](d3dxvec3transformcoord.md) function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="28a49-132">Требования</span><span class="sxs-lookup"><span data-stu-id="28a49-132">Requirements</span></span>



| <span data-ttu-id="28a49-133">Требование</span><span class="sxs-lookup"><span data-stu-id="28a49-133">Requirement</span></span> | <span data-ttu-id="28a49-134">Значение</span><span class="sxs-lookup"><span data-stu-id="28a49-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="28a49-135">Header</span><span class="sxs-lookup"><span data-stu-id="28a49-135">Header</span></span><br/>  | <dl> <span data-ttu-id="28a49-136"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="28a49-136"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="28a49-137">Библиотека</span><span class="sxs-lookup"><span data-stu-id="28a49-137">Library</span></span><br/> | <dl> <span data-ttu-id="28a49-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="28a49-138"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="28a49-139">См. также</span><span class="sxs-lookup"><span data-stu-id="28a49-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28a49-140">Математические функции</span><span class="sxs-lookup"><span data-stu-id="28a49-140">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
