---
description: Выполняет Catmull-Rom интерполяцию с использованием указанных векторов 4D.
ms.assetid: e3a10989-e25e-46fa-b72e-bade936cacf1
title: Функция D3DXVec4CatmullRom (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4CatmullRom
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 8e027272a038f17a77dbeda861d6be909afa2f7f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000335"
---
# <a name="d3dxvec4catmullrom-function-d3dx10mathh"></a><span data-ttu-id="6ab87-103">Функция D3DXVec4CatmullRom (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="6ab87-103">D3DXVec4CatmullRom function (D3DX10Math.h)</span></span>

<span data-ttu-id="6ab87-104">Выполняет Catmull-Rom интерполяцию с использованием указанных векторов 4D.</span><span class="sxs-lookup"><span data-stu-id="6ab87-104">Performs a Catmull-Rom interpolation, using the specified 4D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ab87-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6ab87-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4CatmullRom(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV0,
  _In_    const D3DXVECTOR4 *pV1,
  _In_    const D3DXVECTOR4 *pV2,
  _In_    const D3DXVECTOR4 *pV3,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a><span data-ttu-id="6ab87-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6ab87-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ab87-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="6ab87-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6ab87-108">Тип: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="6ab87-108">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="6ab87-109">Указатель на [**D3DXVECTOR4**](d3d10-d3dxvector4.md) , который является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="6ab87-109">Pointer to the [**D3DXVECTOR4**](d3d10-d3dxvector4.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="6ab87-110">*pV0* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6ab87-110">*pV0* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ab87-111">Тип: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="6ab87-111">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="6ab87-112">Указатель на исходную структуру D3DXVECTOR4, вектор позиции.</span><span class="sxs-lookup"><span data-stu-id="6ab87-112">Pointer to a source D3DXVECTOR4 structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="6ab87-113">*pV1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6ab87-113">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ab87-114">Тип: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="6ab87-114">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="6ab87-115">Указатель на исходную структуру D3DXVECTOR4, вектор позиции.</span><span class="sxs-lookup"><span data-stu-id="6ab87-115">Pointer to a source D3DXVECTOR4 structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="6ab87-116">*pV2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6ab87-116">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ab87-117">Тип: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="6ab87-117">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="6ab87-118">Указатель на исходную структуру D3DXVECTOR4, вектор позиции.</span><span class="sxs-lookup"><span data-stu-id="6ab87-118">Pointer to a source D3DXVECTOR4 structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="6ab87-119">*pV3* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6ab87-119">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ab87-120">Тип: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="6ab87-120">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="6ab87-121">Указатель на исходную структуру D3DXVECTOR4, вектор позиции.</span><span class="sxs-lookup"><span data-stu-id="6ab87-121">Pointer to a source D3DXVECTOR4 structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="6ab87-122">*s* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="6ab87-122">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ab87-123">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6ab87-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6ab87-124">Весовой коэффициент.</span><span class="sxs-lookup"><span data-stu-id="6ab87-124">Weighting factor.</span></span> <span data-ttu-id="6ab87-125">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="6ab87-125">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ab87-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6ab87-126">Return value</span></span>

<span data-ttu-id="6ab87-127">Тип: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="6ab87-127">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="6ab87-128">Указатель на структуру D3DXVECTOR4, которая является результатом интерполяции Catmull-Rom.</span><span class="sxs-lookup"><span data-stu-id="6ab87-128">Pointer to a D3DXVECTOR4 structure that is the result of the Catmull-Rom interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ab87-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6ab87-129">Remarks</span></span>

<span data-ttu-id="6ab87-130">Учитывая четыре точки (P1, P2, P3, P4), найдите функцию Q (с) таким образом:</span><span class="sxs-lookup"><span data-stu-id="6ab87-130">Given four points (p1, p2, p3, p4), find a function Q(s) such that:</span></span>


```
Q(s) is a cubic function. 
Q(s) interpolates between p2 and p3 as s ranges from 0 to 1. 
Q(s) is parallel to the line joining p1 to p3 when s is 0. 
Q(s) is parallel to the line joining p2 to p4 when s is 1. 
```



<span data-ttu-id="6ab87-131">Catmull-Rom сплайн может быть производным от сплайна Хермите, настроив:</span><span class="sxs-lookup"><span data-stu-id="6ab87-131">The Catmull-Rom spline can be derived from the Hermite spline by setting:</span></span>


```
v1 = p2
v2 = p3
t1 = (p3 - p1) / 2
t2 = (p4 - p2) / 2
```



<span data-ttu-id="6ab87-132">где:</span><span class="sxs-lookup"><span data-stu-id="6ab87-132">where:</span></span>

<span data-ttu-id="6ab87-133">значение v1 является содержимым pV0.</span><span class="sxs-lookup"><span data-stu-id="6ab87-133">v1 is the contents of pV0.</span></span>

<span data-ttu-id="6ab87-134">v2 в содержимом pV1.</span><span class="sxs-lookup"><span data-stu-id="6ab87-134">v2 in the contents of pV1.</span></span>

<span data-ttu-id="6ab87-135">P3 — это содержимое pV2.</span><span class="sxs-lookup"><span data-stu-id="6ab87-135">p3 is the contents of pV2.</span></span>

<span data-ttu-id="6ab87-136">P4 — это содержимое pV3.</span><span class="sxs-lookup"><span data-stu-id="6ab87-136">p4 is the contents of pV3.</span></span>

<span data-ttu-id="6ab87-137">С помощью уравнения сплайна Хермите:</span><span class="sxs-lookup"><span data-stu-id="6ab87-137">Using the Hermite spline equation:</span></span>


```
Q(s) = (2s3 - 3s2 + 1)v1 + (-2s3 + 3s2)v2 + (s3 - 2s2 + s)t1 + (s3 - s2)t2
```



<span data-ttu-id="6ab87-138">и подстановка для v1, v2, T1, T2 выдает:</span><span class="sxs-lookup"><span data-stu-id="6ab87-138">and substituting for v1, v2, t1, t2 yields:</span></span>


```
Q(s) = (2s3 - 3s2 + 1)p2 + (-2s3 + 3s2)p3 + (s3 - 2s2 + s)(p3 - p1) / 2 + (s3 - s2)(p4 - p2) / 2
```



<span data-ttu-id="6ab87-139">Его можно расположить следующим образом:</span><span class="sxs-lookup"><span data-stu-id="6ab87-139">This can be rearranged as:</span></span>


```
Q(s) = [(-s3 + 2s2 - s)p1 + (3s3 - 5s2 + 2)p2 + (-3s3 + 4s2 + s)p3 + (s3 - s2)p4] / 2
```



## <a name="requirements"></a><span data-ttu-id="6ab87-140">Требования</span><span class="sxs-lookup"><span data-stu-id="6ab87-140">Requirements</span></span>



| <span data-ttu-id="6ab87-141">Требование</span><span class="sxs-lookup"><span data-stu-id="6ab87-141">Requirement</span></span> | <span data-ttu-id="6ab87-142">Значение</span><span class="sxs-lookup"><span data-stu-id="6ab87-142">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ab87-143">Header</span><span class="sxs-lookup"><span data-stu-id="6ab87-143">Header</span></span><br/> | <dl> <span data-ttu-id="6ab87-144"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ab87-144"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ab87-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6ab87-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ab87-146">Математические функции</span><span class="sxs-lookup"><span data-stu-id="6ab87-146">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
