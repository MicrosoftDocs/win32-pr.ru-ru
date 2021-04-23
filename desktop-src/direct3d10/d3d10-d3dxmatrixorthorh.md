---
description: Формирует матрицу правой ортогональной проекции.
ms.assetid: e6673ff4-06a2-4a16-b72e-5ca69ddf2438
title: Функция D3DXMatrixOrthoRH (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 2a8883f2690fa5a5f0bfa1bb1570163b714974b3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105720928"
---
# <a name="d3dxmatrixorthorh-function-d3dx10mathh"></a><span data-ttu-id="4580b-103">Функция D3DXMatrixOrthoRH (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="4580b-103">D3DXMatrixOrthoRH function (D3DX10Math.h)</span></span>

<span data-ttu-id="4580b-104">Формирует матрицу правой ортогональной проекции.</span><span class="sxs-lookup"><span data-stu-id="4580b-104">Builds a right-handed orthographic projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="4580b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4580b-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixOrthoRH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      w,
  _In_    FLOAT      h,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="4580b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4580b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4580b-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="4580b-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4580b-108">Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="4580b-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="4580b-109">Указатель на результирующий [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="4580b-109">Pointer to the resulting [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="4580b-110">*w* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="4580b-110">*w* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4580b-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4580b-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4580b-112">Ширина объема представления.</span><span class="sxs-lookup"><span data-stu-id="4580b-112">Width of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="4580b-113">*ч* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="4580b-113">*h* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4580b-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4580b-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4580b-115">Высота представления объема.</span><span class="sxs-lookup"><span data-stu-id="4580b-115">Height of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="4580b-116">*ЗН* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4580b-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4580b-117">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4580b-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4580b-118">Минимальное z-значение отображаемого объема.</span><span class="sxs-lookup"><span data-stu-id="4580b-118">Minimum z-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="4580b-119">*ЗФ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4580b-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4580b-120">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4580b-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4580b-121">Максимальное z-значение отображаемого объема.</span><span class="sxs-lookup"><span data-stu-id="4580b-121">Maximum z-value of the view volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4580b-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4580b-122">Return value</span></span>

<span data-ttu-id="4580b-123">Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="4580b-123">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="4580b-124">Указатель на результирующий [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="4580b-124">Pointer to the resulting [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4580b-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4580b-125">Remarks</span></span>

<span data-ttu-id="4580b-126">Все параметры функции D3DXMatrixOrthoRH — это расстояния в пространстве камеры.</span><span class="sxs-lookup"><span data-stu-id="4580b-126">All the parameters of the D3DXMatrixOrthoRH function are distances in camera space.</span></span> <span data-ttu-id="4580b-127">Параметры описывают размеры представления объема.</span><span class="sxs-lookup"><span data-stu-id="4580b-127">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="4580b-128">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="4580b-128">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="4580b-129">Таким образом, функция D3DXMatrixOrthoRH может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="4580b-129">In this way, the D3DXMatrixOrthoRH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="4580b-130">Эта функция использует следующую формулу для вычисления возвращаемой матрицы.</span><span class="sxs-lookup"><span data-stu-id="4580b-130">This function uses the following formula to compute the returned matrix.</span></span>


```
2/w  0    0           0
0    2/h  0           0
0    0    1/(zn-zf)   0
0    0    zn/(zn-zf)  1
```



## <a name="requirements"></a><span data-ttu-id="4580b-131">Требования</span><span class="sxs-lookup"><span data-stu-id="4580b-131">Requirements</span></span>



| <span data-ttu-id="4580b-132">Требование</span><span class="sxs-lookup"><span data-stu-id="4580b-132">Requirement</span></span> | <span data-ttu-id="4580b-133">Значение</span><span class="sxs-lookup"><span data-stu-id="4580b-133">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4580b-134">Header</span><span class="sxs-lookup"><span data-stu-id="4580b-134">Header</span></span><br/>  | <dl> <span data-ttu-id="4580b-135"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="4580b-135"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="4580b-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4580b-136">Library</span></span><br/> | <dl> <span data-ttu-id="4580b-137"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4580b-137"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4580b-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4580b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4580b-139">Математические функции</span><span class="sxs-lookup"><span data-stu-id="4580b-139">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
