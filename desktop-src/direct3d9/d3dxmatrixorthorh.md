---
description: Формирует матрицу правой ортогональной проекции.
ms.assetid: 6b9b50d5-0307-4fc7-a28d-8f42d2a21bf0
title: Функция D3DXMatrixOrthoRH (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixOrthoRH
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 00df0ee06768e4d57a68291dd1716e4a4574507e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713478"
---
# <a name="d3dxmatrixorthorh-function-d3dx9mathh"></a><span data-ttu-id="9a097-103">Функция D3DXMatrixOrthoRH (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="9a097-103">D3DXMatrixOrthoRH function (D3dx9math.h)</span></span>

<span data-ttu-id="9a097-104">Формирует матрицу правой ортогональной проекции.</span><span class="sxs-lookup"><span data-stu-id="9a097-104">Builds a right-handed orthographic projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a097-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9a097-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixOrthoRH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      w,
  _In_    FLOAT      h,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="9a097-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9a097-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a097-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="9a097-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9a097-108">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="9a097-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="9a097-109">Указатель на результирующий [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="9a097-109">Pointer to the resulting [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="9a097-110">*w* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="9a097-110">*w* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a097-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9a097-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9a097-112">Ширина объема представления.</span><span class="sxs-lookup"><span data-stu-id="9a097-112">Width of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="9a097-113">*ч* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="9a097-113">*h* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a097-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9a097-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9a097-115">Высота представления объема.</span><span class="sxs-lookup"><span data-stu-id="9a097-115">Height of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="9a097-116">*ЗН* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9a097-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a097-117">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9a097-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9a097-118">Минимальное z-значение отображаемого объема.</span><span class="sxs-lookup"><span data-stu-id="9a097-118">Minimum z-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="9a097-119">*ЗФ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9a097-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a097-120">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9a097-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9a097-121">Максимальное z-значение отображаемого объема.</span><span class="sxs-lookup"><span data-stu-id="9a097-121">Maximum z-value of the view volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a097-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9a097-122">Return value</span></span>

<span data-ttu-id="9a097-123">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="9a097-123">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="9a097-124">Указатель на результирующий [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="9a097-124">Pointer to the resulting [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9a097-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9a097-125">Remarks</span></span>

<span data-ttu-id="9a097-126">Все параметры функции **D3DXMatrixOrthoRH** — это расстояния в пространстве камеры.</span><span class="sxs-lookup"><span data-stu-id="9a097-126">All the parameters of the **D3DXMatrixOrthoRH** function are distances in camera space.</span></span> <span data-ttu-id="9a097-127">Параметры описывают размеры представления объема.</span><span class="sxs-lookup"><span data-stu-id="9a097-127">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="9a097-128">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="9a097-128">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="9a097-129">Таким образом, функция **D3DXMatrixOrthoRH** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="9a097-129">In this way, the **D3DXMatrixOrthoRH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="9a097-130">Эта функция использует следующую формулу для вычисления возвращаемой матрицы.</span><span class="sxs-lookup"><span data-stu-id="9a097-130">This function uses the following formula to compute the returned matrix.</span></span>


```
2/w  0    0           0
0    2/h  0           0
0    0    1/(zn-zf)   0
0    0    zn/(zn-zf)  1
```



## <a name="requirements"></a><span data-ttu-id="9a097-131">Требования</span><span class="sxs-lookup"><span data-stu-id="9a097-131">Requirements</span></span>



| <span data-ttu-id="9a097-132">Требование</span><span class="sxs-lookup"><span data-stu-id="9a097-132">Requirement</span></span> | <span data-ttu-id="9a097-133">Значение</span><span class="sxs-lookup"><span data-stu-id="9a097-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9a097-134">Header</span><span class="sxs-lookup"><span data-stu-id="9a097-134">Header</span></span><br/>  | <dl> <span data-ttu-id="9a097-135"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a097-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="9a097-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9a097-136">Library</span></span><br/> | <dl> <span data-ttu-id="9a097-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9a097-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9a097-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9a097-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a097-139">Математические функции</span><span class="sxs-lookup"><span data-stu-id="9a097-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="9a097-140">**D3DXMatrixOrthoLH**</span><span class="sxs-lookup"><span data-stu-id="9a097-140">**D3DXMatrixOrthoLH**</span></span>](d3dxmatrixortholh.md)
</dt> <dt>

[<span data-ttu-id="9a097-141">**D3DXMatrixOrthoOffCenterRH**</span><span class="sxs-lookup"><span data-stu-id="9a097-141">**D3DXMatrixOrthoOffCenterRH**</span></span>](d3dxmatrixorthooffcenterrh.md)
</dt> <dt>

[<span data-ttu-id="9a097-142">**D3DXMatrixOrthoOffCenterLH**</span><span class="sxs-lookup"><span data-stu-id="9a097-142">**D3DXMatrixOrthoOffCenterLH**</span></span>](d3dxmatrixorthooffcenterlh.md)
</dt> </dl>

 

 
