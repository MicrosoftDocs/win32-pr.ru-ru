---
description: Проецирует массив (x, y, z, 0) из пространства объекта в пространство экрана.
ms.assetid: cf022741-0bae-4c22-872f-bd94c3721aff
title: Функция D3DXVec3ProjectArray (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3ProjectArray
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f802d8ab564f2cbfe1cc60ad6aed13959bef9383
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105714015"
---
# <a name="d3dxvec3projectarray-function-d3dx9mathh"></a><span data-ttu-id="6faa8-103">Функция D3DXVec3ProjectArray (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="6faa8-103">D3DXVec3ProjectArray function (D3dx9math.h)</span></span>

<span data-ttu-id="6faa8-104">Проецирует массив (x, y, z, 0) из пространства объекта в пространство экрана.</span><span class="sxs-lookup"><span data-stu-id="6faa8-104">Projects an array (x, y, z, 0) from object space into screen space.</span></span>

## <a name="syntax"></a><span data-ttu-id="6faa8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6faa8-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3ProjectArray(
  _Inout_       D3DXVECTOR3  *pOut,
  _In_          UINT         OutStride,
  _In_    const D3DXVECTOR3  *pV,
  _In_          UINT         VStride,
  _In_    const D3DVIEWPORT9 *pViewport,
  _In_    const D3DXMATRIX   *pProjection,
  _In_    const D3DXMATRIX   *pView,
  _In_    const D3DXMATRIX   *pWorld,
  _In_          UINT         n
);
```



## <a name="parameters"></a><span data-ttu-id="6faa8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6faa8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6faa8-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="6faa8-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6faa8-108">Тип: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="6faa8-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="6faa8-109">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="6faa8-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="6faa8-110">*Шаг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6faa8-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6faa8-111">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6faa8-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6faa8-112">Шаг между векторами в потоке выходных данных.</span><span class="sxs-lookup"><span data-stu-id="6faa8-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="6faa8-113">*ПС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6faa8-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6faa8-114">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="6faa8-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="6faa8-115">Указатель на исходную структуру [**D3DXVECTOR3**](d3dxvector3.md) .</span><span class="sxs-lookup"><span data-stu-id="6faa8-115">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="6faa8-116">*Встриде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6faa8-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6faa8-117">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6faa8-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6faa8-118">Шаг между векторами во входном потоке данных.</span><span class="sxs-lookup"><span data-stu-id="6faa8-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="6faa8-119">*пвиевпорт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6faa8-119">*pViewport* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6faa8-120">Тип: **const [**D3DVIEWPORT9**](d3dviewport9.md) \***</span><span class="sxs-lookup"><span data-stu-id="6faa8-120">Type: **const [**D3DVIEWPORT9**](d3dviewport9.md)\***</span></span>

<span data-ttu-id="6faa8-121">Указатель на структуру [**D3DVIEWPORT9**](d3dviewport9.md) , представляющую окно просмотра.</span><span class="sxs-lookup"><span data-stu-id="6faa8-121">Pointer to a [**D3DVIEWPORT9**](d3dviewport9.md) structure, representing the viewport.</span></span>

</dd> <dt>

<span data-ttu-id="6faa8-122">*ппрожектион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6faa8-122">*pProjection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6faa8-123">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="6faa8-123">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="6faa8-124">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , представляющую матрицу проекции.</span><span class="sxs-lookup"><span data-stu-id="6faa8-124">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the projection matrix.</span></span>

</dd> <dt>

<span data-ttu-id="6faa8-125">*pView* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6faa8-125">*pView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6faa8-126">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="6faa8-126">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="6faa8-127">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , представляющую матрицу представления.</span><span class="sxs-lookup"><span data-stu-id="6faa8-127">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the view matrix.</span></span>

</dd> <dt>

<span data-ttu-id="6faa8-128">*пворлд* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6faa8-128">*pWorld* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6faa8-129">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="6faa8-129">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="6faa8-130">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , представляющую матрицу мира.</span><span class="sxs-lookup"><span data-stu-id="6faa8-130">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the world matrix.</span></span>

</dd> <dt>

<span data-ttu-id="6faa8-131">*n* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="6faa8-131">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6faa8-132">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6faa8-132">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6faa8-133">Число элементов в массиве.</span><span class="sxs-lookup"><span data-stu-id="6faa8-133">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6faa8-134">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6faa8-134">Return value</span></span>

<span data-ttu-id="6faa8-135">Тип: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="6faa8-135">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="6faa8-136">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , которая представляет собой массив, проецируемый из объектного пространства в пространство экрана.</span><span class="sxs-lookup"><span data-stu-id="6faa8-136">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the array projected from object space to screen space.</span></span>

## <a name="remarks"></a><span data-ttu-id="6faa8-137">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6faa8-137">Remarks</span></span>

<span data-ttu-id="6faa8-138">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="6faa8-138">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="6faa8-139">Таким образом, функция **D3DXVec3ProjectArray** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="6faa8-139">In this way, the **D3DXVec3ProjectArray** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="6faa8-140">Требования</span><span class="sxs-lookup"><span data-stu-id="6faa8-140">Requirements</span></span>



| <span data-ttu-id="6faa8-141">Требование</span><span class="sxs-lookup"><span data-stu-id="6faa8-141">Requirement</span></span> | <span data-ttu-id="6faa8-142">Значение</span><span class="sxs-lookup"><span data-stu-id="6faa8-142">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6faa8-143">Header</span><span class="sxs-lookup"><span data-stu-id="6faa8-143">Header</span></span><br/>  | <dl> <span data-ttu-id="6faa8-144"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="6faa8-144"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="6faa8-145">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6faa8-145">Library</span></span><br/> | <dl> <span data-ttu-id="6faa8-146"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6faa8-146"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6faa8-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6faa8-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6faa8-148">Математические функции</span><span class="sxs-lookup"><span data-stu-id="6faa8-148">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="6faa8-149">**D3DXVec3Unproject**</span><span class="sxs-lookup"><span data-stu-id="6faa8-149">**D3DXVec3Unproject**</span></span>](d3dxvec3unproject.md)
</dt> </dl>

 

 
