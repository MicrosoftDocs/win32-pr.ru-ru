---
description: Преобразует массив (x, y, 0, 1) по заданной матрице и проецирует результат обратно в w = 1.
ms.assetid: 23c88bed-344b-4b3a-bb92-e50cbe96daf9
title: Функция D3DXVec2TransformCoordArray (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e924f9c008efe76490f9f51903a1c31f254e0001
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694198"
---
# <a name="d3dxvec2transformcoordarray-function-d3dx9mathh"></a><span data-ttu-id="8c546-103">Функция D3DXVec2TransformCoordArray (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="8c546-103">D3DXVec2TransformCoordArray function (D3dx9math.h)</span></span>

<span data-ttu-id="8c546-104">Преобразует массив (x, y, 0, 1) по заданной матрице и проецирует результат обратно в w = 1.</span><span class="sxs-lookup"><span data-stu-id="8c546-104">Transforms an array (x, y, 0, 1) by a given matrix, and projects the result back into w = 1.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c546-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8c546-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="8c546-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8c546-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c546-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="8c546-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8c546-108">Тип: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="8c546-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="8c546-109">Указатель на структуру [**D3DXVECTOR2**](d3dxvector2.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="8c546-109">Pointer to the [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="8c546-110">*Шаг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8c546-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c546-111">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8c546-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8c546-112">Шаг между векторами в потоке выходных данных.</span><span class="sxs-lookup"><span data-stu-id="8c546-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="8c546-113">*ПС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8c546-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c546-114">Тип: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="8c546-114">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="8c546-115">Указатель на исходный массив [**D3DXVECTOR2**](d3dxvector2.md) .</span><span class="sxs-lookup"><span data-stu-id="8c546-115">Pointer to the source [**D3DXVECTOR2**](d3dxvector2.md) array.</span></span>

</dd> <dt>

<span data-ttu-id="8c546-116">*Встриде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8c546-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c546-117">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8c546-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8c546-118">Шаг между векторами во входном потоке данных.</span><span class="sxs-lookup"><span data-stu-id="8c546-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="8c546-119">*PM* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8c546-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c546-120">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="8c546-120">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="8c546-121">Указатель на исходную структуру [**D3DXMATRIX**](d3dxmatrix.md) .</span><span class="sxs-lookup"><span data-stu-id="8c546-121">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="8c546-122">*n* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="8c546-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c546-123">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8c546-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8c546-124">Число элементов в массиве.</span><span class="sxs-lookup"><span data-stu-id="8c546-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c546-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8c546-125">Return value</span></span>

<span data-ttu-id="8c546-126">Тип: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="8c546-126">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="8c546-127">Указатель на преобразованный массив [**D3DXVECTOR4**](d3dxvector4.md) .</span><span class="sxs-lookup"><span data-stu-id="8c546-127">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c546-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8c546-128">Remarks</span></span>

<span data-ttu-id="8c546-129">Эта функция преобразует массив *ПС* (x, y, 0, 1) на матрицу *PM*, проецирование результата обратно в w = 1.</span><span class="sxs-lookup"><span data-stu-id="8c546-129">This function transforms the array *pV* (x, y, 0, 1) by the matrix *pM*, projecting the result back into w = 1.</span></span>

<span data-ttu-id="8c546-130">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="8c546-130">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="8c546-131">Таким образом, функция **D3DXVec2TransformCoordArray** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="8c546-131">In this way, the **D3DXVec2TransformCoordArray** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c546-132">Требования</span><span class="sxs-lookup"><span data-stu-id="8c546-132">Requirements</span></span>



| <span data-ttu-id="8c546-133">Требование</span><span class="sxs-lookup"><span data-stu-id="8c546-133">Requirement</span></span> | <span data-ttu-id="8c546-134">Значение</span><span class="sxs-lookup"><span data-stu-id="8c546-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8c546-135">Header</span><span class="sxs-lookup"><span data-stu-id="8c546-135">Header</span></span><br/>  | <dl> <span data-ttu-id="8c546-136"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c546-136"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="8c546-137">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8c546-137">Library</span></span><br/> | <dl> <span data-ttu-id="8c546-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8c546-138"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8c546-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8c546-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c546-140">Математические функции</span><span class="sxs-lookup"><span data-stu-id="8c546-140">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
