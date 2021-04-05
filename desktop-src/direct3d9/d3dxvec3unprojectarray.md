---
description: Проецирует массив (x, y, z, 0) из пространства экрана в объектное пространство.
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
ms.openlocfilehash: 3af4cc05b5f8ee30c624f904df7e2ae5cd4b844a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000482"
---
# <a name="d3dxvec3unprojectarray-function-d3dx9mathh"></a><span data-ttu-id="f36d2-103">Функция D3DXVec3UnprojectArray (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="f36d2-103">D3DXVec3UnprojectArray function (D3dx9math.h)</span></span>

<span data-ttu-id="f36d2-104">Проецирует массив (x, y, z, 0) из пространства экрана в объектное пространство.</span><span class="sxs-lookup"><span data-stu-id="f36d2-104">Projects an array (x, y, z, 0) from screen space into object space.</span></span>

## <a name="syntax"></a><span data-ttu-id="f36d2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f36d2-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="f36d2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f36d2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f36d2-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="f36d2-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f36d2-108">Тип: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="f36d2-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="f36d2-109">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="f36d2-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="f36d2-110">*Шаг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f36d2-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f36d2-111">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f36d2-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f36d2-112">Шаг между векторами в потоке выходных данных.</span><span class="sxs-lookup"><span data-stu-id="f36d2-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="f36d2-113">*ПС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f36d2-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f36d2-114">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="f36d2-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="f36d2-115">Указатель на исходную структуру [**D3DXVECTOR3**](d3dxvector3.md) .</span><span class="sxs-lookup"><span data-stu-id="f36d2-115">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="f36d2-116">*Встриде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f36d2-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f36d2-117">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f36d2-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f36d2-118">Шаг между векторами во входном потоке данных.</span><span class="sxs-lookup"><span data-stu-id="f36d2-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="f36d2-119">*пвиевпорт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f36d2-119">*pViewport* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f36d2-120">Тип: **const [**D3DVIEWPORT9**](d3dviewport9.md) \***</span><span class="sxs-lookup"><span data-stu-id="f36d2-120">Type: **const [**D3DVIEWPORT9**](d3dviewport9.md)\***</span></span>

<span data-ttu-id="f36d2-121">Указатель на структуру [**D3DVIEWPORT9**](d3dviewport9.md) , представляющую окно просмотра.</span><span class="sxs-lookup"><span data-stu-id="f36d2-121">Pointer to a [**D3DVIEWPORT9**](d3dviewport9.md) structure, representing the viewport.</span></span>

</dd> <dt>

<span data-ttu-id="f36d2-122">*ппрожектион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f36d2-122">*pProjection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f36d2-123">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="f36d2-123">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f36d2-124">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , представляющую матрицу проекции.</span><span class="sxs-lookup"><span data-stu-id="f36d2-124">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the projection matrix.</span></span>

</dd> <dt>

<span data-ttu-id="f36d2-125">*pView* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f36d2-125">*pView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f36d2-126">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="f36d2-126">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f36d2-127">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , представляющую матрицу представления.</span><span class="sxs-lookup"><span data-stu-id="f36d2-127">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the view matrix.</span></span>

</dd> <dt>

<span data-ttu-id="f36d2-128">*пворлд* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f36d2-128">*pWorld* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f36d2-129">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="f36d2-129">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f36d2-130">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , представляющую матрицу мира.</span><span class="sxs-lookup"><span data-stu-id="f36d2-130">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the world matrix.</span></span>

</dd> <dt>

<span data-ttu-id="f36d2-131">*n* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="f36d2-131">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f36d2-132">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f36d2-132">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f36d2-133">Число элементов в массиве.</span><span class="sxs-lookup"><span data-stu-id="f36d2-133">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f36d2-134">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f36d2-134">Return value</span></span>

<span data-ttu-id="f36d2-135">Тип: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="f36d2-135">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="f36d2-136">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , которая представляет собой массив, проецируемый из пространства экрана, в объектное пространство.</span><span class="sxs-lookup"><span data-stu-id="f36d2-136">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the array projected from screen space to object space.</span></span>

## <a name="remarks"></a><span data-ttu-id="f36d2-137">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f36d2-137">Remarks</span></span>

<span data-ttu-id="f36d2-138">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="f36d2-138">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="f36d2-139">Таким образом, функция [**D3DXVec3Unproject**](d3dxvec3unproject.md) может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="f36d2-139">In this way, the [**D3DXVec3Unproject**](d3dxvec3unproject.md) function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="f36d2-140">Требования</span><span class="sxs-lookup"><span data-stu-id="f36d2-140">Requirements</span></span>



| <span data-ttu-id="f36d2-141">Требование</span><span class="sxs-lookup"><span data-stu-id="f36d2-141">Requirement</span></span> | <span data-ttu-id="f36d2-142">Значение</span><span class="sxs-lookup"><span data-stu-id="f36d2-142">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f36d2-143">Header</span><span class="sxs-lookup"><span data-stu-id="f36d2-143">Header</span></span><br/>  | <dl> <span data-ttu-id="f36d2-144"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="f36d2-144"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="f36d2-145">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f36d2-145">Library</span></span><br/> | <dl> <span data-ttu-id="f36d2-146"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f36d2-146"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f36d2-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f36d2-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f36d2-148">Математические функции</span><span class="sxs-lookup"><span data-stu-id="f36d2-148">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="f36d2-149">**D3DXVec3Project**</span><span class="sxs-lookup"><span data-stu-id="f36d2-149">**D3DXVec3Project**</span></span>](d3dxvec3project.md)
</dt> </dl>

 

 
