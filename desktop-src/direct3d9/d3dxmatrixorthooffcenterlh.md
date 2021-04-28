---
description: Функция D3DXMatrixOrthoOffCenterLH (D3dx9math. h) — создает настроенную левую матрицу ортогональной проекции.
ms.assetid: e4f087e5-63d9-49ca-9d8e-3a25070e1a51
title: Функция D3DXMatrixOrthoOffCenterLH (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixOrthoOffCenterLH
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 704bdab1d486399b28117cd078f556beb1347f7b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107492"
---
# <a name="d3dxmatrixorthooffcenterlh-function-d3dx9mathh"></a><span data-ttu-id="836b8-103">Функция D3DXMatrixOrthoOffCenterLH (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="836b8-103">D3DXMatrixOrthoOffCenterLH function (D3dx9math.h)</span></span>

<span data-ttu-id="836b8-104">Создает настроенную левую матрицу ортогональной проекции.</span><span class="sxs-lookup"><span data-stu-id="836b8-104">Builds a customized, left-handed orthographic projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="836b8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="836b8-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixOrthoOffCenterLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      l,
  _In_    FLOAT      r,
  _In_    FLOAT      b,
  _In_    FLOAT      t,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="836b8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="836b8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="836b8-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="836b8-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="836b8-108">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="836b8-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="836b8-109">Указатель на результирующий [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="836b8-109">Pointer to the resulting [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="836b8-110">*l* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="836b8-110">*l* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="836b8-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="836b8-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="836b8-112">Минимальное значение x для представления объема.</span><span class="sxs-lookup"><span data-stu-id="836b8-112">Minimum x-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="836b8-113">*r* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="836b8-113">*r* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="836b8-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="836b8-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="836b8-115">Максимальное значение x-значения для представления объема.</span><span class="sxs-lookup"><span data-stu-id="836b8-115">Maximum x-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="836b8-116">*б* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="836b8-116">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="836b8-117">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="836b8-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="836b8-118">Минимальное значение y для параметра "Показать том".</span><span class="sxs-lookup"><span data-stu-id="836b8-118">Minimum y-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="836b8-119">*t* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="836b8-119">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="836b8-120">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="836b8-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="836b8-121">Максимальное значение y для параметра "Показать том".</span><span class="sxs-lookup"><span data-stu-id="836b8-121">Maximum y-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="836b8-122">*ЗН* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="836b8-122">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="836b8-123">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="836b8-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="836b8-124">Минимальное z-значение отображаемого объема.</span><span class="sxs-lookup"><span data-stu-id="836b8-124">Minimum z-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="836b8-125">*ЗФ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="836b8-125">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="836b8-126">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="836b8-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="836b8-127">Максимальное z-значение отображаемого объема.</span><span class="sxs-lookup"><span data-stu-id="836b8-127">Maximum z-value of the view volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="836b8-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="836b8-128">Return value</span></span>

<span data-ttu-id="836b8-129">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="836b8-129">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="836b8-130">Указатель на результирующий [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="836b8-130">Pointer to the resulting [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="836b8-131">Remarks</span><span class="sxs-lookup"><span data-stu-id="836b8-131">Remarks</span></span>

<span data-ttu-id="836b8-132">Функция [**D3DXMatrixOrthoLH**](d3dxmatrixortholh.md) является особым случаем функции **D3DXMatrixOrthoOffCenterLH** .</span><span class="sxs-lookup"><span data-stu-id="836b8-132">The [**D3DXMatrixOrthoLH**](d3dxmatrixortholh.md) function is a special case of the **D3DXMatrixOrthoOffCenterLH** function.</span></span> <span data-ttu-id="836b8-133">Чтобы создать ту же проекцию с помощью **D3DXMatrixOrthoOffCenterLH**, используйте следующие значения: l =-w/2, r = w/2, b =-h/2 и t = h/2.</span><span class="sxs-lookup"><span data-stu-id="836b8-133">To create the same projection using **D3DXMatrixOrthoOffCenterLH**, use the following values: l = -w/2, r = w/2, b = -h/2, and t = h/2.</span></span>

<span data-ttu-id="836b8-134">Все параметры функции **D3DXMatrixOrthoOffCenterLH** — это расстояния в пространстве камеры.</span><span class="sxs-lookup"><span data-stu-id="836b8-134">All the parameters of the **D3DXMatrixOrthoOffCenterLH** function are distances in camera space.</span></span> <span data-ttu-id="836b8-135">Параметры описывают размеры представления объема.</span><span class="sxs-lookup"><span data-stu-id="836b8-135">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="836b8-136">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="836b8-136">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="836b8-137">Таким образом, функция **D3DXMatrixOrthoOffCenterLH** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="836b8-137">In this way, the **D3DXMatrixOrthoOffCenterLH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="836b8-138">Эта функция использует следующую формулу для вычисления возвращаемой матрицы.</span><span class="sxs-lookup"><span data-stu-id="836b8-138">This function uses the following formula to compute the returned matrix.</span></span>


```
2/(r-l)      0            0           0
0            2/(t-b)      0           0
0            0            1/(zf-zn)   0
(l+r)/(l-r)  (t+b)/(b-t)  zn/(zn-zf)  1
```



## <a name="requirements"></a><span data-ttu-id="836b8-139">Требования</span><span class="sxs-lookup"><span data-stu-id="836b8-139">Requirements</span></span>



| <span data-ttu-id="836b8-140">Требование</span><span class="sxs-lookup"><span data-stu-id="836b8-140">Requirement</span></span> | <span data-ttu-id="836b8-141">Значение</span><span class="sxs-lookup"><span data-stu-id="836b8-141">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="836b8-142">Header</span><span class="sxs-lookup"><span data-stu-id="836b8-142">Header</span></span><br/>  | <dl> <span data-ttu-id="836b8-143"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="836b8-143"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="836b8-144">Библиотека</span><span class="sxs-lookup"><span data-stu-id="836b8-144">Library</span></span><br/> | <dl> <span data-ttu-id="836b8-145"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="836b8-145"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="836b8-146">См. также</span><span class="sxs-lookup"><span data-stu-id="836b8-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="836b8-147">Математические функции</span><span class="sxs-lookup"><span data-stu-id="836b8-147">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="836b8-148">**D3DXMatrixOrthoRH**</span><span class="sxs-lookup"><span data-stu-id="836b8-148">**D3DXMatrixOrthoRH**</span></span>](d3dxmatrixorthorh.md)
</dt> <dt>

[<span data-ttu-id="836b8-149">**D3DXMatrixOrthoLH**</span><span class="sxs-lookup"><span data-stu-id="836b8-149">**D3DXMatrixOrthoLH**</span></span>](d3dxmatrixortholh.md)
</dt> <dt>

[<span data-ttu-id="836b8-150">**D3DXMatrixOrthoOffCenterRH**</span><span class="sxs-lookup"><span data-stu-id="836b8-150">**D3DXMatrixOrthoOffCenterRH**</span></span>](d3dxmatrixorthooffcenterrh.md)
</dt> </dl>

 

 
