---
description: Преобразует массив (x, y, z, 1) по заданной матрице и проецирует результат обратно в w = 1.
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
ms.openlocfilehash: 414fd17c3d7077b4aeb399b734b4a6c811a8a291
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000518"
---
# <a name="d3dxvec3transformcoordarray-function-d3dx9mathh"></a><span data-ttu-id="293d4-103">Функция D3DXVec3TransformCoordArray (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="293d4-103">D3DXVec3TransformCoordArray function (D3dx9math.h)</span></span>

<span data-ttu-id="293d4-104">Преобразует массив (x, y, z, 1) по заданной матрице и проецирует результат обратно в w = 1.</span><span class="sxs-lookup"><span data-stu-id="293d4-104">Transforms an array (x, y, z, 1) by a given matrix, and projects the result back into w = 1.</span></span>

## <a name="syntax"></a><span data-ttu-id="293d4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="293d4-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="293d4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="293d4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="293d4-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="293d4-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="293d4-108">Тип: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="293d4-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="293d4-109">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="293d4-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="293d4-110">*Шаг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="293d4-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="293d4-111">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="293d4-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="293d4-112">Шаг между векторами в потоке выходных данных.</span><span class="sxs-lookup"><span data-stu-id="293d4-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="293d4-113">*ПС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="293d4-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="293d4-114">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="293d4-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="293d4-115">Указатель на исходный массив [**D3DXVECTOR3**](d3dxvector3.md) .</span><span class="sxs-lookup"><span data-stu-id="293d4-115">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) array.</span></span>

</dd> <dt>

<span data-ttu-id="293d4-116">*Встриде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="293d4-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="293d4-117">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="293d4-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="293d4-118">Шаг между векторами во входном потоке данных.</span><span class="sxs-lookup"><span data-stu-id="293d4-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="293d4-119">*PM* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="293d4-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="293d4-120">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="293d4-120">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="293d4-121">Указатель на исходную структуру [**D3DXMATRIX**](d3dxmatrix.md) .</span><span class="sxs-lookup"><span data-stu-id="293d4-121">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="293d4-122">*n* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="293d4-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="293d4-123">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="293d4-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="293d4-124">Число элементов в массиве.</span><span class="sxs-lookup"><span data-stu-id="293d4-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="293d4-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="293d4-125">Return value</span></span>

<span data-ttu-id="293d4-126">Тип: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="293d4-126">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="293d4-127">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , которая является преобразованным массивом.</span><span class="sxs-lookup"><span data-stu-id="293d4-127">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="293d4-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="293d4-128">Remarks</span></span>

<span data-ttu-id="293d4-129">Эта функция преобразует массив *ПС (* x, y, z, 1) на матрицу *PM*, проецирование результата обратно в w = 1.</span><span class="sxs-lookup"><span data-stu-id="293d4-129">This function transforms the array *pV (* x, y, z, 1) by the matrix *pM*, projecting the result back into w = 1.</span></span>

<span data-ttu-id="293d4-130">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="293d4-130">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="293d4-131">Таким образом, функция [**D3DXVec3TransformCoord**](d3dxvec3transformcoord.md) может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="293d4-131">In this way, the [**D3DXVec3TransformCoord**](d3dxvec3transformcoord.md) function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="293d4-132">Требования</span><span class="sxs-lookup"><span data-stu-id="293d4-132">Requirements</span></span>



| <span data-ttu-id="293d4-133">Требование</span><span class="sxs-lookup"><span data-stu-id="293d4-133">Requirement</span></span> | <span data-ttu-id="293d4-134">Значение</span><span class="sxs-lookup"><span data-stu-id="293d4-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="293d4-135">Header</span><span class="sxs-lookup"><span data-stu-id="293d4-135">Header</span></span><br/>  | <dl> <span data-ttu-id="293d4-136"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="293d4-136"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="293d4-137">Библиотека</span><span class="sxs-lookup"><span data-stu-id="293d4-137">Library</span></span><br/> | <dl> <span data-ttu-id="293d4-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="293d4-138"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="293d4-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="293d4-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="293d4-140">Математические функции</span><span class="sxs-lookup"><span data-stu-id="293d4-140">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
