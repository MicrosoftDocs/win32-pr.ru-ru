---
description: Функция D3DXMatrixOrthoLH (D3dx9math. h) — строит матрицу левой ортогональной проекции.
ms.assetid: e42151bd-2302-491b-a211-7d5a4b8e437f
title: Функция D3DXMatrixOrthoLH (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixOrthoLH
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5492a6caba87025d83562c0327ac0e1f5a76f269
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107502"
---
# <a name="d3dxmatrixortholh-function-d3dx9mathh"></a><span data-ttu-id="7dc40-103">Функция D3DXMatrixOrthoLH (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="7dc40-103">D3DXMatrixOrthoLH function (D3dx9math.h)</span></span>

<span data-ttu-id="7dc40-104">Формирует матрицу левой ортогональной проекции.</span><span class="sxs-lookup"><span data-stu-id="7dc40-104">Builds a left-handed orthographic projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="7dc40-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7dc40-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixOrthoLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      w,
  _In_    FLOAT      h,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="7dc40-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7dc40-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7dc40-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="7dc40-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7dc40-108">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="7dc40-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="7dc40-109">Указатель на результирующий [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="7dc40-109">Pointer to the resulting [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="7dc40-110">*w* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="7dc40-110">*w* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7dc40-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7dc40-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7dc40-112">Ширина объема представления.</span><span class="sxs-lookup"><span data-stu-id="7dc40-112">Width of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="7dc40-113">*ч* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="7dc40-113">*h* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7dc40-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7dc40-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7dc40-115">Высота представления объема.</span><span class="sxs-lookup"><span data-stu-id="7dc40-115">Height of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="7dc40-116">*ЗН* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7dc40-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7dc40-117">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7dc40-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7dc40-118">Минимальное z-значение отображаемого тома, называемое z-NEAR.</span><span class="sxs-lookup"><span data-stu-id="7dc40-118">Minimum z-value of the view volume which is referred to as z-near.</span></span>

</dd> <dt>

<span data-ttu-id="7dc40-119">*ЗФ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7dc40-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7dc40-120">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7dc40-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7dc40-121">Максимальное z-значение объема представления, которое называется z-далеко.</span><span class="sxs-lookup"><span data-stu-id="7dc40-121">Maximum z-value of the view volume which is referred to as z-far.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7dc40-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7dc40-122">Return value</span></span>

<span data-ttu-id="7dc40-123">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="7dc40-123">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="7dc40-124">Указатель на результирующий [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="7dc40-124">Pointer to the resulting [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7dc40-125">Remarks</span><span class="sxs-lookup"><span data-stu-id="7dc40-125">Remarks</span></span>

<span data-ttu-id="7dc40-126">Все параметры функции **D3DXMatrixOrthoLH** — это расстояния в пространстве камеры.</span><span class="sxs-lookup"><span data-stu-id="7dc40-126">All the parameters of the **D3DXMatrixOrthoLH** function are distances in camera space.</span></span> <span data-ttu-id="7dc40-127">Параметры описывают размеры представления объема.</span><span class="sxs-lookup"><span data-stu-id="7dc40-127">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="7dc40-128">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="7dc40-128">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="7dc40-129">Таким образом, функция **D3DXMatrixOrthoLH** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="7dc40-129">In this way, the **D3DXMatrixOrthoLH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="7dc40-130">Эта функция использует следующую формулу для вычисления возвращаемой матрицы.</span><span class="sxs-lookup"><span data-stu-id="7dc40-130">This function uses the following formula to compute the returned matrix.</span></span>


```
2/w  0    0           0
0    2/h  0           0
0    0    1/(zf-zn)   0
0    0   -zn/(zf-zn)  1
```



## <a name="requirements"></a><span data-ttu-id="7dc40-131">Требования</span><span class="sxs-lookup"><span data-stu-id="7dc40-131">Requirements</span></span>



| <span data-ttu-id="7dc40-132">Требование</span><span class="sxs-lookup"><span data-stu-id="7dc40-132">Requirement</span></span> | <span data-ttu-id="7dc40-133">Значение</span><span class="sxs-lookup"><span data-stu-id="7dc40-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7dc40-134">Header</span><span class="sxs-lookup"><span data-stu-id="7dc40-134">Header</span></span><br/>  | <dl> <span data-ttu-id="7dc40-135"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="7dc40-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="7dc40-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7dc40-136">Library</span></span><br/> | <dl> <span data-ttu-id="7dc40-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7dc40-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7dc40-138">См. также</span><span class="sxs-lookup"><span data-stu-id="7dc40-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7dc40-139">Математические функции</span><span class="sxs-lookup"><span data-stu-id="7dc40-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="7dc40-140">**D3DXMatrixOrthoRH**</span><span class="sxs-lookup"><span data-stu-id="7dc40-140">**D3DXMatrixOrthoRH**</span></span>](d3dxmatrixorthorh.md)
</dt> <dt>

[<span data-ttu-id="7dc40-141">**D3DXMatrixOrthoOffCenterRH**</span><span class="sxs-lookup"><span data-stu-id="7dc40-141">**D3DXMatrixOrthoOffCenterRH**</span></span>](d3dxmatrixorthooffcenterrh.md)
</dt> <dt>

[<span data-ttu-id="7dc40-142">**D3DXMatrixOrthoOffCenterLH**</span><span class="sxs-lookup"><span data-stu-id="7dc40-142">**D3DXMatrixOrthoOffCenterLH**</span></span>](d3dxmatrixorthooffcenterlh.md)
</dt> </dl>

 

 
