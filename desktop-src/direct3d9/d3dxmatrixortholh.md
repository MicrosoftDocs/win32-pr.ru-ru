---
description: Формирует матрицу левой ортогональной проекции.
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
ms.openlocfilehash: 4aaf4a1a770ba0200a6afe389d37e248b9f4c7de
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355423"
---
# <a name="d3dxmatrixortholh-function-d3dx9mathh"></a><span data-ttu-id="b0d60-103">Функция D3DXMatrixOrthoLH (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="b0d60-103">D3DXMatrixOrthoLH function (D3dx9math.h)</span></span>

<span data-ttu-id="b0d60-104">Формирует матрицу левой ортогональной проекции.</span><span class="sxs-lookup"><span data-stu-id="b0d60-104">Builds a left-handed orthographic projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0d60-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b0d60-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixOrthoLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      w,
  _In_    FLOAT      h,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="b0d60-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b0d60-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0d60-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="b0d60-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b0d60-108">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="b0d60-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="b0d60-109">Указатель на результирующий [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="b0d60-109">Pointer to the resulting [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="b0d60-110">*w* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="b0d60-110">*w* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0d60-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b0d60-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b0d60-112">Ширина объема представления.</span><span class="sxs-lookup"><span data-stu-id="b0d60-112">Width of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="b0d60-113">*ч* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="b0d60-113">*h* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0d60-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b0d60-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b0d60-115">Высота представления объема.</span><span class="sxs-lookup"><span data-stu-id="b0d60-115">Height of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="b0d60-116">*ЗН* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b0d60-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0d60-117">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b0d60-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b0d60-118">Минимальное z-значение отображаемого тома, называемое z-NEAR.</span><span class="sxs-lookup"><span data-stu-id="b0d60-118">Minimum z-value of the view volume which is referred to as z-near.</span></span>

</dd> <dt>

<span data-ttu-id="b0d60-119">*ЗФ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b0d60-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0d60-120">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b0d60-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b0d60-121">Максимальное z-значение объема представления, которое называется z-далеко.</span><span class="sxs-lookup"><span data-stu-id="b0d60-121">Maximum z-value of the view volume which is referred to as z-far.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0d60-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b0d60-122">Return value</span></span>

<span data-ttu-id="b0d60-123">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="b0d60-123">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="b0d60-124">Указатель на результирующий [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="b0d60-124">Pointer to the resulting [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b0d60-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b0d60-125">Remarks</span></span>

<span data-ttu-id="b0d60-126">Все параметры функции **D3DXMatrixOrthoLH** — это расстояния в пространстве камеры.</span><span class="sxs-lookup"><span data-stu-id="b0d60-126">All the parameters of the **D3DXMatrixOrthoLH** function are distances in camera space.</span></span> <span data-ttu-id="b0d60-127">Параметры описывают размеры представления объема.</span><span class="sxs-lookup"><span data-stu-id="b0d60-127">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="b0d60-128">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="b0d60-128">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="b0d60-129">Таким образом, функция **D3DXMatrixOrthoLH** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="b0d60-129">In this way, the **D3DXMatrixOrthoLH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="b0d60-130">Эта функция использует следующую формулу для вычисления возвращаемой матрицы.</span><span class="sxs-lookup"><span data-stu-id="b0d60-130">This function uses the following formula to compute the returned matrix.</span></span>


```
2/w  0    0           0
0    2/h  0           0
0    0    1/(zf-zn)   0
0    0   -zn/(zf-zn)  1
```



## <a name="requirements"></a><span data-ttu-id="b0d60-131">Требования</span><span class="sxs-lookup"><span data-stu-id="b0d60-131">Requirements</span></span>



| <span data-ttu-id="b0d60-132">Требование</span><span class="sxs-lookup"><span data-stu-id="b0d60-132">Requirement</span></span> | <span data-ttu-id="b0d60-133">Значение</span><span class="sxs-lookup"><span data-stu-id="b0d60-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b0d60-134">Header</span><span class="sxs-lookup"><span data-stu-id="b0d60-134">Header</span></span><br/>  | <dl> <span data-ttu-id="b0d60-135"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0d60-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="b0d60-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b0d60-136">Library</span></span><br/> | <dl> <span data-ttu-id="b0d60-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b0d60-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b0d60-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b0d60-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0d60-139">Математические функции</span><span class="sxs-lookup"><span data-stu-id="b0d60-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="b0d60-140">**D3DXMatrixOrthoRH**</span><span class="sxs-lookup"><span data-stu-id="b0d60-140">**D3DXMatrixOrthoRH**</span></span>](d3dxmatrixorthorh.md)
</dt> <dt>

[<span data-ttu-id="b0d60-141">**D3DXMatrixOrthoOffCenterRH**</span><span class="sxs-lookup"><span data-stu-id="b0d60-141">**D3DXMatrixOrthoOffCenterRH**</span></span>](d3dxmatrixorthooffcenterrh.md)
</dt> <dt>

[<span data-ttu-id="b0d60-142">**D3DXMatrixOrthoOffCenterLH**</span><span class="sxs-lookup"><span data-stu-id="b0d60-142">**D3DXMatrixOrthoOffCenterLH**</span></span>](d3dxmatrixorthooffcenterlh.md)
</dt> </dl>

 

 
