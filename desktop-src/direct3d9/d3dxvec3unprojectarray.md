---
description: Функция D3DXVec3UnprojectArray (D3dx9math. h) — проецирует массив (x, y, z, 0) из пространства экрана в объектное пространство.
ms.assetid: fef2a76c-c2fe-48c5-a1bb-6669bcc76b9b
title: Функция D3DXVec3UnprojectArray (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3UnprojectArray
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 67e42b30a8f8d44bb9b21668a515a202436b7631
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097722"
---
# <a name="d3dxvec3unprojectarray-function-d3dx9mathh"></a><span data-ttu-id="da92d-103">Функция D3DXVec3UnprojectArray (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="da92d-103">D3DXVec3UnprojectArray function (D3dx9math.h)</span></span>

<span data-ttu-id="da92d-104">Проецирует массив (x, y, z, 0) из пространства экрана в объектное пространство.</span><span class="sxs-lookup"><span data-stu-id="da92d-104">Projects an array (x, y, z, 0) from screen space into object space.</span></span>

## <a name="syntax"></a><span data-ttu-id="da92d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="da92d-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3UnprojectArray(
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



## <a name="parameters"></a><span data-ttu-id="da92d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="da92d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da92d-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="da92d-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="da92d-108">Тип: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="da92d-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="da92d-109">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="da92d-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="da92d-110">*Шаг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="da92d-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da92d-111">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="da92d-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="da92d-112">Шаг между векторами в потоке выходных данных.</span><span class="sxs-lookup"><span data-stu-id="da92d-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="da92d-113">*ПС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="da92d-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da92d-114">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="da92d-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="da92d-115">Указатель на исходную структуру [**D3DXVECTOR3**](d3dxvector3.md) .</span><span class="sxs-lookup"><span data-stu-id="da92d-115">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="da92d-116">*Встриде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="da92d-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da92d-117">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="da92d-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="da92d-118">Шаг между векторами во входном потоке данных.</span><span class="sxs-lookup"><span data-stu-id="da92d-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="da92d-119">*пвиевпорт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="da92d-119">*pViewport* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da92d-120">Тип: **const [**D3DVIEWPORT9**](d3dviewport9.md) \***</span><span class="sxs-lookup"><span data-stu-id="da92d-120">Type: **const [**D3DVIEWPORT9**](d3dviewport9.md)\***</span></span>

<span data-ttu-id="da92d-121">Указатель на структуру [**D3DVIEWPORT9**](d3dviewport9.md) , представляющую окно просмотра.</span><span class="sxs-lookup"><span data-stu-id="da92d-121">Pointer to a [**D3DVIEWPORT9**](d3dviewport9.md) structure, representing the viewport.</span></span>

</dd> <dt>

<span data-ttu-id="da92d-122">*ппрожектион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="da92d-122">*pProjection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da92d-123">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="da92d-123">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="da92d-124">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , представляющую матрицу проекции.</span><span class="sxs-lookup"><span data-stu-id="da92d-124">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the projection matrix.</span></span>

</dd> <dt>

<span data-ttu-id="da92d-125">*pView* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="da92d-125">*pView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da92d-126">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="da92d-126">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="da92d-127">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , представляющую матрицу представления.</span><span class="sxs-lookup"><span data-stu-id="da92d-127">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the view matrix.</span></span>

</dd> <dt>

<span data-ttu-id="da92d-128">*пворлд* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="da92d-128">*pWorld* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da92d-129">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="da92d-129">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="da92d-130">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , представляющую матрицу мира.</span><span class="sxs-lookup"><span data-stu-id="da92d-130">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the world matrix.</span></span>

</dd> <dt>

<span data-ttu-id="da92d-131">*n* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="da92d-131">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da92d-132">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="da92d-132">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="da92d-133">Число элементов в массиве.</span><span class="sxs-lookup"><span data-stu-id="da92d-133">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da92d-134">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="da92d-134">Return value</span></span>

<span data-ttu-id="da92d-135">Тип: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="da92d-135">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="da92d-136">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , которая представляет собой массив, проецируемый из пространства экрана, в объектное пространство.</span><span class="sxs-lookup"><span data-stu-id="da92d-136">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the array projected from screen space to object space.</span></span>

## <a name="remarks"></a><span data-ttu-id="da92d-137">Remarks</span><span class="sxs-lookup"><span data-stu-id="da92d-137">Remarks</span></span>

<span data-ttu-id="da92d-138">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="da92d-138">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="da92d-139">Таким образом, функция [**D3DXVec3Unproject**](d3dxvec3unproject.md) может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="da92d-139">In this way, the [**D3DXVec3Unproject**](d3dxvec3unproject.md) function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="da92d-140">Требования</span><span class="sxs-lookup"><span data-stu-id="da92d-140">Requirements</span></span>



| <span data-ttu-id="da92d-141">Требование</span><span class="sxs-lookup"><span data-stu-id="da92d-141">Requirement</span></span> | <span data-ttu-id="da92d-142">Значение</span><span class="sxs-lookup"><span data-stu-id="da92d-142">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="da92d-143">Header</span><span class="sxs-lookup"><span data-stu-id="da92d-143">Header</span></span><br/>  | <dl> <span data-ttu-id="da92d-144"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="da92d-144"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="da92d-145">Библиотека</span><span class="sxs-lookup"><span data-stu-id="da92d-145">Library</span></span><br/> | <dl> <span data-ttu-id="da92d-146"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="da92d-146"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="da92d-147">См. также</span><span class="sxs-lookup"><span data-stu-id="da92d-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da92d-148">Математические функции</span><span class="sxs-lookup"><span data-stu-id="da92d-148">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="da92d-149">**D3DXVec3Project**</span><span class="sxs-lookup"><span data-stu-id="da92d-149">**D3DXVec3Project**</span></span>](d3dxvec3project.md)
</dt> </dl>

 

 
