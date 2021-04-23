---
description: Проецирует массив (x, y, z, 0) из пространства объекта в пространство экрана.
ms.assetid: 33f0f65a-c027-4a31-83a7-f5f6b2a2f72f
title: Функция D3DXVec3ProjectArray (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3ProjectArray
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: bdbda9201d23a6c525dc054c53874c71d548e65e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355383"
---
# <a name="d3dxvec3projectarray-function-d3dx10mathh"></a><span data-ttu-id="5ae91-103">Функция D3DXVec3ProjectArray (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="5ae91-103">D3DXVec3ProjectArray function (D3DX10Math.h)</span></span>

<span data-ttu-id="5ae91-104">Проецирует массив (x, y, z, 0) из пространства объекта в пространство экрана.</span><span class="sxs-lookup"><span data-stu-id="5ae91-104">Projects an array (x, y, z, 0) from object space into screen space.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ae91-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5ae91-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3ProjectArray(
  _Inout_       D3DXVECTOR3    *pOut,
  _In_          UINT           OutStride,
  _In_    const D3DXVECTOR3    *pV,
  _In_          UINT           VStride,
  _In_    const D3D10_VIEWPORT *pViewport,
  _In_    const D3DXMATRIX     *pProjection,
  _In_    const D3DXMATRIX     *pView,
  _In_    const D3DXMATRIX     *pWorld,
  _In_          UINT           n
);
```



## <a name="parameters"></a><span data-ttu-id="5ae91-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5ae91-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ae91-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="5ae91-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5ae91-108">Тип: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="5ae91-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="5ae91-109">Указатель на [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , который является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="5ae91-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="5ae91-110">*Шаг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5ae91-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ae91-111">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5ae91-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5ae91-112">Шаг между векторами в потоке выходных данных.</span><span class="sxs-lookup"><span data-stu-id="5ae91-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="5ae91-113">*ПС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5ae91-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ae91-114">Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="5ae91-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="5ae91-115">Указатель на исходную структуру D3DXVECTOR3.</span><span class="sxs-lookup"><span data-stu-id="5ae91-115">Pointer to the source D3DXVECTOR3 structure.</span></span>

</dd> <dt>

<span data-ttu-id="5ae91-116">*Встриде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5ae91-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ae91-117">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5ae91-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5ae91-118">Шаг между векторами во входном потоке данных.</span><span class="sxs-lookup"><span data-stu-id="5ae91-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="5ae91-119">*пвиевпорт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5ae91-119">*pViewport* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ae91-120">Тип: **const [**D3D10 \_ окно просмотра**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport) \***</span><span class="sxs-lookup"><span data-stu-id="5ae91-120">Type: **const [**D3D10\_VIEWPORT**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport)\***</span></span>

<span data-ttu-id="5ae91-121">Указатель на [**\_ окно просмотра D3D10**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport), представляющее окно просмотра.</span><span class="sxs-lookup"><span data-stu-id="5ae91-121">Pointer to a [**D3D10\_VIEWPORT**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport), representing the viewport.</span></span>

</dd> <dt>

<span data-ttu-id="5ae91-122">*ппрожектион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5ae91-122">*pProjection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ae91-123">Тип: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="5ae91-123">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="5ae91-124">Указатель на структуру [**D3DXMATRIX**](d3d10-d3dxmatrix.md) , представляющую матрицу проекции.</span><span class="sxs-lookup"><span data-stu-id="5ae91-124">Pointer to a [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure, representing the projection matrix.</span></span>

</dd> <dt>

<span data-ttu-id="5ae91-125">*pView* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5ae91-125">*pView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ae91-126">Тип: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="5ae91-126">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="5ae91-127">Указатель на структуру D3DXMATRIX, представляющую матрицу представления.</span><span class="sxs-lookup"><span data-stu-id="5ae91-127">Pointer to a D3DXMATRIX structure, representing the view matrix.</span></span>

</dd> <dt>

<span data-ttu-id="5ae91-128">*пворлд* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5ae91-128">*pWorld* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ae91-129">Тип: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="5ae91-129">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="5ae91-130">Указатель на структуру D3DXMATRIX, представляющую матрицу мира.</span><span class="sxs-lookup"><span data-stu-id="5ae91-130">Pointer to a D3DXMATRIX structure, representing the world matrix.</span></span>

</dd> <dt>

<span data-ttu-id="5ae91-131">*n* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="5ae91-131">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ae91-132">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5ae91-132">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5ae91-133">Число элементов в массиве.</span><span class="sxs-lookup"><span data-stu-id="5ae91-133">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ae91-134">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5ae91-134">Return value</span></span>

<span data-ttu-id="5ae91-135">Тип: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="5ae91-135">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="5ae91-136">Указатель на структуру D3DXVECTOR3, которая представляет собой массив, проецируемый из объектного пространства в пространство экрана.</span><span class="sxs-lookup"><span data-stu-id="5ae91-136">Pointer to a D3DXVECTOR3 structure that is the array projected from object space to screen space.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ae91-137">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5ae91-137">Remarks</span></span>

<span data-ttu-id="5ae91-138">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="5ae91-138">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="5ae91-139">Таким образом, функция D3DXVec3ProjectArray может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="5ae91-139">In this way, the D3DXVec3ProjectArray function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ae91-140">Требования</span><span class="sxs-lookup"><span data-stu-id="5ae91-140">Requirements</span></span>



| <span data-ttu-id="5ae91-141">Требование</span><span class="sxs-lookup"><span data-stu-id="5ae91-141">Requirement</span></span> | <span data-ttu-id="5ae91-142">Значение</span><span class="sxs-lookup"><span data-stu-id="5ae91-142">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ae91-143">Header</span><span class="sxs-lookup"><span data-stu-id="5ae91-143">Header</span></span><br/> | <dl> <span data-ttu-id="5ae91-144"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ae91-144"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ae91-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5ae91-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ae91-146">Математические функции</span><span class="sxs-lookup"><span data-stu-id="5ae91-146">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
