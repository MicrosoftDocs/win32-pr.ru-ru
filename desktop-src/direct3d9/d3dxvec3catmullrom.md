---
description: Функция D3DXVec3CatmullRom (D3dx9math. h) — выполняет Catmull-Rom интерполяцию с использованием указанных трехмерных векторов.
ms.assetid: 779f067c-ac46-4fde-9e18-e31b1504b490
title: Функция D3DXVec3CatmullRom (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3CatmullRom
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bc2a72f6d638c7a4daa8db1849a790bdd76556b9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115662"
---
# <a name="d3dxvec3catmullrom-function-d3dx9mathh"></a><span data-ttu-id="3eaf3-103">Функция D3DXVec3CatmullRom (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="3eaf3-103">D3DXVec3CatmullRom function (D3dx9math.h)</span></span>

<span data-ttu-id="3eaf3-104">Выполняет Catmull-Rom интерполяцию с использованием указанных трехмерных векторов.</span><span class="sxs-lookup"><span data-stu-id="3eaf3-104">Performs a Catmull-Rom interpolation, using the specified 3D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="3eaf3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3eaf3-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3CatmullRom(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV0,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2,
  _In_    const D3DXVECTOR3 *pV3,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a><span data-ttu-id="3eaf3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3eaf3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3eaf3-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="3eaf3-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3eaf3-108">Тип: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="3eaf3-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="3eaf3-109">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="3eaf3-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="3eaf3-110">*pV0* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3eaf3-110">*pV0* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3eaf3-111">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="3eaf3-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="3eaf3-112">Указатель на исходную структуру [**D3DXVECTOR3**](d3dxvector3.md) , вектор позиции.</span><span class="sxs-lookup"><span data-stu-id="3eaf3-112">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="3eaf3-113">*pV1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3eaf3-113">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3eaf3-114">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="3eaf3-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="3eaf3-115">Указатель на исходную структуру [**D3DXVECTOR3**](d3dxvector3.md) , вектор позиции.</span><span class="sxs-lookup"><span data-stu-id="3eaf3-115">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="3eaf3-116">*pV2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3eaf3-116">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3eaf3-117">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="3eaf3-117">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="3eaf3-118">Указатель на исходную структуру [**D3DXVECTOR3**](d3dxvector3.md) , вектор позиции.</span><span class="sxs-lookup"><span data-stu-id="3eaf3-118">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="3eaf3-119">*pV3* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3eaf3-119">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3eaf3-120">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="3eaf3-120">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="3eaf3-121">Указатель на исходную структуру [**D3DXVECTOR3**](d3dxvector3.md) , вектор позиции.</span><span class="sxs-lookup"><span data-stu-id="3eaf3-121">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="3eaf3-122">*s* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="3eaf3-122">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3eaf3-123">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3eaf3-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3eaf3-124">Весовой коэффициент.</span><span class="sxs-lookup"><span data-stu-id="3eaf3-124">Weighting factor.</span></span> <span data-ttu-id="3eaf3-125">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="3eaf3-125">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3eaf3-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3eaf3-126">Return value</span></span>

<span data-ttu-id="3eaf3-127">Тип: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="3eaf3-127">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="3eaf3-128">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , которая является результатом интерполяции Catmull-Rom.</span><span class="sxs-lookup"><span data-stu-id="3eaf3-128">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the Catmull-Rom interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="3eaf3-129">Remarks</span><span class="sxs-lookup"><span data-stu-id="3eaf3-129">Remarks</span></span>

<span data-ttu-id="3eaf3-130">Учитывая четыре точки (P1, P2, P3, P4), найдите функцию Q (с) таким образом:</span><span class="sxs-lookup"><span data-stu-id="3eaf3-130">Given four points (p1, p2, p3, p4), find a function Q(s) such that:</span></span>


```
Q(s) is a cubic function. 
Q(s) interpolates between p2 and p3 as s ranges from 0 to 1. 
Q(s) is parallel to the line joining p1 to p3 when s is 0. 
Q(s) is parallel to the line joining p2 to p4 when s is 1. 
```



<span data-ttu-id="3eaf3-131">Catmull-Rom сплайн может быть производным от сплайна Хермите, настроив:</span><span class="sxs-lookup"><span data-stu-id="3eaf3-131">The Catmull-Rom spline can be derived from the Hermite spline by setting:</span></span>


```
v1 = p2
v2 = p3
t1 = (p3 - p1) / 2
t2 = (p4 - p2) / 2
```



<span data-ttu-id="3eaf3-132">где:</span><span class="sxs-lookup"><span data-stu-id="3eaf3-132">where:</span></span>

<span data-ttu-id="3eaf3-133">значение v1 является содержимым pV0.</span><span class="sxs-lookup"><span data-stu-id="3eaf3-133">v1 is the contents of pV0.</span></span>

<span data-ttu-id="3eaf3-134">v2 — это содержимое pV1.</span><span class="sxs-lookup"><span data-stu-id="3eaf3-134">v2 is the contents of pV1.</span></span>

<span data-ttu-id="3eaf3-135">P3 — это содержимое pV2.</span><span class="sxs-lookup"><span data-stu-id="3eaf3-135">p3 is the contents of pV2.</span></span>

<span data-ttu-id="3eaf3-136">P4 — это содержимое pV3.</span><span class="sxs-lookup"><span data-stu-id="3eaf3-136">p4 is the contents of pV3.</span></span>

<span data-ttu-id="3eaf3-137">С помощью уравнения сплайна Хермите:</span><span class="sxs-lookup"><span data-stu-id="3eaf3-137">Using the Hermite spline equation:</span></span>


```
Q(s) = (2s3 - 3s2 + 1)v1 + (-2s3 + 3s2)v2 + (s3 - 2s2 + s)t1 + (s3 - s2)t2
```



<span data-ttu-id="3eaf3-138">и подстановка для v1, v2, T1, T2 выдает:</span><span class="sxs-lookup"><span data-stu-id="3eaf3-138">and substituting for v1, v2, t1, t2 yields:</span></span>


```
Q(s) = (2s3 - 3s2 + 1)p2 + (-2s3 + 3s2)p3 + (s3 - 2s2 + s)(p3 - p1) / 2 + (s3 - s2)(p4 - p2) / 2
```



<span data-ttu-id="3eaf3-139">Его можно расположить следующим образом:</span><span class="sxs-lookup"><span data-stu-id="3eaf3-139">This can be rearranged as:</span></span>


```
Q(s) = [(-s3 + 2s2 - s)p1 + (3s3 - 5s2 + 2)p2 + (-3s3 + 4s2 + s)p3 + (s3 - s2)p4] / 2
```



## <a name="requirements"></a><span data-ttu-id="3eaf3-140">Требования</span><span class="sxs-lookup"><span data-stu-id="3eaf3-140">Requirements</span></span>



| <span data-ttu-id="3eaf3-141">Требование</span><span class="sxs-lookup"><span data-stu-id="3eaf3-141">Requirement</span></span> | <span data-ttu-id="3eaf3-142">Значение</span><span class="sxs-lookup"><span data-stu-id="3eaf3-142">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3eaf3-143">Header</span><span class="sxs-lookup"><span data-stu-id="3eaf3-143">Header</span></span><br/>  | <dl> <span data-ttu-id="3eaf3-144"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="3eaf3-144"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="3eaf3-145">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3eaf3-145">Library</span></span><br/> | <dl> <span data-ttu-id="3eaf3-146"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3eaf3-146"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3eaf3-147">См. также</span><span class="sxs-lookup"><span data-stu-id="3eaf3-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3eaf3-148">Математические функции</span><span class="sxs-lookup"><span data-stu-id="3eaf3-148">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="3eaf3-149">**D3DXVec2CatmullRom**</span><span class="sxs-lookup"><span data-stu-id="3eaf3-149">**D3DXVec2CatmullRom**</span></span>](d3dxvec2catmullrom.md)
</dt> <dt>

[<span data-ttu-id="3eaf3-150">**D3DXVec4CatmullRom**</span><span class="sxs-lookup"><span data-stu-id="3eaf3-150">**D3DXVec4CatmullRom**</span></span>](d3dxvec4catmullrom.md)
</dt> </dl>

 

 
