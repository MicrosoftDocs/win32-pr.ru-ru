---
description: Функция D3DXPlaneIntersectLine (D3DX10Math. h) — Находит пересечение между плоскостью и линией.
ms.assetid: aea1c4e1-f8c0-46df-bb33-2b517396d69e
title: Функция D3DXPlaneIntersectLine (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneIntersectLine
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1d32bb312c97b793f492f7a29bebe11529b79cf9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108812"
---
# <a name="d3dxplaneintersectline-function-d3dx10mathh"></a><span data-ttu-id="6f13c-103">Функция D3DXPlaneIntersectLine (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="6f13c-103">D3DXPlaneIntersectLine function (D3DX10Math.h)</span></span>

<span data-ttu-id="6f13c-104">Находит пересечение между плоскостью и линией.</span><span class="sxs-lookup"><span data-stu-id="6f13c-104">Finds the intersection between a plane and a line.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f13c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6f13c-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXPlaneIntersectLine(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXPLANE   *pP,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="6f13c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6f13c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f13c-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="6f13c-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6f13c-108">Тип: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="6f13c-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="6f13c-109">Указатель на [**D3DXVECTOR3**](d3d10-d3dxvector3.md), определяющий пересечение между указанной плоскостью и линией.</span><span class="sxs-lookup"><span data-stu-id="6f13c-109">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md), identifying the intersection between the specified plane and line.</span></span>

</dd> <dt>

<span data-ttu-id="6f13c-110">*PP* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6f13c-110">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f13c-111">Тип: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="6f13c-111">Type: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="6f13c-112">Указатель на источник [**D3DXPLANE**](d3d10-d3dxplane.md).</span><span class="sxs-lookup"><span data-stu-id="6f13c-112">Pointer to the source [**D3DXPLANE**](d3d10-d3dxplane.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f13c-113">*pV1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6f13c-113">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f13c-114">Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="6f13c-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="6f13c-115">Указатель на исходную структуру D3DXVECTOR3, определяющую начальную точку строки.</span><span class="sxs-lookup"><span data-stu-id="6f13c-115">Pointer to a source D3DXVECTOR3 structure, defining a line starting point.</span></span>

</dd> <dt>

<span data-ttu-id="6f13c-116">*pV2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6f13c-116">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f13c-117">Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="6f13c-117">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="6f13c-118">Указатель на исходную структуру D3DXVECTOR3, определяющую конечную точку строки.</span><span class="sxs-lookup"><span data-stu-id="6f13c-118">Pointer to a source D3DXVECTOR3 structure, defining a line ending point.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f13c-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6f13c-119">Return value</span></span>

<span data-ttu-id="6f13c-120">Тип: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="6f13c-120">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="6f13c-121">Указатель на структуру D3DXVECTOR3, которая является пересечением между указанной плоскостью и линией.</span><span class="sxs-lookup"><span data-stu-id="6f13c-121">Pointer to a D3DXVECTOR3 structure that is the intersection between the specified plane and line.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f13c-122">Remarks</span><span class="sxs-lookup"><span data-stu-id="6f13c-122">Remarks</span></span>

<span data-ttu-id="6f13c-123">Если линия параллельна плоскости, возвращается **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="6f13c-123">If the line is parallel to the plane, **NULL** is returned.</span></span>

<span data-ttu-id="6f13c-124">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="6f13c-124">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="6f13c-125">Таким образом, функция D3DXPlaneIntersectLine может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="6f13c-125">In this way, the D3DXPlaneIntersectLine function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f13c-126">Требования</span><span class="sxs-lookup"><span data-stu-id="6f13c-126">Requirements</span></span>



| <span data-ttu-id="6f13c-127">Требование</span><span class="sxs-lookup"><span data-stu-id="6f13c-127">Requirement</span></span> | <span data-ttu-id="6f13c-128">Значение</span><span class="sxs-lookup"><span data-stu-id="6f13c-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6f13c-129">Header</span><span class="sxs-lookup"><span data-stu-id="6f13c-129">Header</span></span><br/>  | <dl> <span data-ttu-id="6f13c-130"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f13c-130"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="6f13c-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6f13c-131">Library</span></span><br/> | <dl> <span data-ttu-id="6f13c-132"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6f13c-132"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6f13c-133">См. также</span><span class="sxs-lookup"><span data-stu-id="6f13c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f13c-134">Математические функции</span><span class="sxs-lookup"><span data-stu-id="6f13c-134">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
