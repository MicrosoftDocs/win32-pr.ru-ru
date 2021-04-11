---
description: Формирует матрицу левой ортогональной проекции.
ms.assetid: 67bec4a3-2126-4f5a-9301-97faa6dc6e84
title: Функция D3DXMatrixOrthoLH (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 0b49e6008b52f7060075688730c72f5f5d3f725a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273927"
---
# <a name="d3dxmatrixortholh-function-d3dx10mathh"></a><span data-ttu-id="a0d1d-103">Функция D3DXMatrixOrthoLH (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="a0d1d-103">D3DXMatrixOrthoLH function (D3DX10Math.h)</span></span>

<span data-ttu-id="a0d1d-104">Формирует матрицу левой ортогональной проекции.</span><span class="sxs-lookup"><span data-stu-id="a0d1d-104">Builds a left-handed orthographic projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0d1d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a0d1d-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixOrthoLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      w,
  _In_    FLOAT      h,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="a0d1d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a0d1d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0d1d-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="a0d1d-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a0d1d-108">Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="a0d1d-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="a0d1d-109">Указатель на результирующий [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="a0d1d-109">Pointer to the resulting [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="a0d1d-110">*w* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="a0d1d-110">*w* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0d1d-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a0d1d-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a0d1d-112">Ширина объема представления.</span><span class="sxs-lookup"><span data-stu-id="a0d1d-112">Width of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="a0d1d-113">*ч* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="a0d1d-113">*h* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0d1d-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a0d1d-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a0d1d-115">Высота представления объема.</span><span class="sxs-lookup"><span data-stu-id="a0d1d-115">Height of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="a0d1d-116">*ЗН* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a0d1d-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0d1d-117">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a0d1d-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a0d1d-118">Минимальное z-значение отображаемого тома, называемое z-NEAR.</span><span class="sxs-lookup"><span data-stu-id="a0d1d-118">Minimum z-value of the view volume which is referred to as z-near.</span></span>

</dd> <dt>

<span data-ttu-id="a0d1d-119">*ЗФ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a0d1d-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0d1d-120">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a0d1d-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a0d1d-121">Максимальное z-значение объема представления, которое называется z-далеко.</span><span class="sxs-lookup"><span data-stu-id="a0d1d-121">Maximum z-value of the view volume which is referred to as z-far.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0d1d-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a0d1d-122">Return value</span></span>

<span data-ttu-id="a0d1d-123">Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="a0d1d-123">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="a0d1d-124">Указатель на результирующий [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="a0d1d-124">Pointer to the resulting [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a0d1d-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a0d1d-125">Remarks</span></span>

<span data-ttu-id="a0d1d-126">Все параметры функции D3DXMatrixOrthoLH — это расстояния в пространстве камеры.</span><span class="sxs-lookup"><span data-stu-id="a0d1d-126">All the parameters of the D3DXMatrixOrthoLH function are distances in camera space.</span></span> <span data-ttu-id="a0d1d-127">Параметры описывают размеры представления объема.</span><span class="sxs-lookup"><span data-stu-id="a0d1d-127">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="a0d1d-128">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="a0d1d-128">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="a0d1d-129">Таким образом, функция D3DXMatrixOrthoLH может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="a0d1d-129">In this way, the D3DXMatrixOrthoLH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="a0d1d-130">Эта функция использует следующую формулу для вычисления возвращаемой матрицы.</span><span class="sxs-lookup"><span data-stu-id="a0d1d-130">This function uses the following formula to compute the returned matrix.</span></span>


```
2/w  0    0           0
0    2/h  0           0
0    0    1/(zf-zn)   0
0    0    zn/(zn-zf)  1
```



## <a name="requirements"></a><span data-ttu-id="a0d1d-131">Требования</span><span class="sxs-lookup"><span data-stu-id="a0d1d-131">Requirements</span></span>



| <span data-ttu-id="a0d1d-132">Требование</span><span class="sxs-lookup"><span data-stu-id="a0d1d-132">Requirement</span></span> | <span data-ttu-id="a0d1d-133">Значение</span><span class="sxs-lookup"><span data-stu-id="a0d1d-133">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a0d1d-134">Header</span><span class="sxs-lookup"><span data-stu-id="a0d1d-134">Header</span></span><br/>  | <dl> <span data-ttu-id="a0d1d-135"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0d1d-135"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="a0d1d-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a0d1d-136">Library</span></span><br/> | <dl> <span data-ttu-id="a0d1d-137"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a0d1d-137"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a0d1d-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a0d1d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0d1d-139">Математические функции</span><span class="sxs-lookup"><span data-stu-id="a0d1d-139">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
