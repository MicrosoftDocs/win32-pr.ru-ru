---
description: Создает настроенную левую матрицу ортогональной проекции.
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
ms.openlocfilehash: 1e286197233b2abb2b19138b8fc9d154df355a6a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000454"
---
# <a name="d3dxmatrixorthooffcenterlh-function-d3dx9mathh"></a><span data-ttu-id="82434-103">Функция D3DXMatrixOrthoOffCenterLH (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="82434-103">D3DXMatrixOrthoOffCenterLH function (D3dx9math.h)</span></span>

<span data-ttu-id="82434-104">Создает настроенную левую матрицу ортогональной проекции.</span><span class="sxs-lookup"><span data-stu-id="82434-104">Builds a customized, left-handed orthographic projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="82434-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="82434-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="82434-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="82434-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82434-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="82434-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="82434-108">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="82434-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="82434-109">Указатель на результирующий [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="82434-109">Pointer to the resulting [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="82434-110">*l* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="82434-110">*l* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82434-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="82434-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="82434-112">Минимальное значение x для представления объема.</span><span class="sxs-lookup"><span data-stu-id="82434-112">Minimum x-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="82434-113">*r* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="82434-113">*r* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82434-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="82434-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="82434-115">Максимальное значение x-значения для представления объема.</span><span class="sxs-lookup"><span data-stu-id="82434-115">Maximum x-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="82434-116">*б* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="82434-116">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82434-117">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="82434-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="82434-118">Минимальное значение y для параметра "Показать том".</span><span class="sxs-lookup"><span data-stu-id="82434-118">Minimum y-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="82434-119">*t* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="82434-119">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82434-120">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="82434-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="82434-121">Максимальное значение y для параметра "Показать том".</span><span class="sxs-lookup"><span data-stu-id="82434-121">Maximum y-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="82434-122">*ЗН* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="82434-122">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82434-123">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="82434-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="82434-124">Минимальное z-значение отображаемого объема.</span><span class="sxs-lookup"><span data-stu-id="82434-124">Minimum z-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="82434-125">*ЗФ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="82434-125">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82434-126">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="82434-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="82434-127">Максимальное z-значение отображаемого объема.</span><span class="sxs-lookup"><span data-stu-id="82434-127">Maximum z-value of the view volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82434-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="82434-128">Return value</span></span>

<span data-ttu-id="82434-129">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="82434-129">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="82434-130">Указатель на результирующий [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="82434-130">Pointer to the resulting [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="82434-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="82434-131">Remarks</span></span>

<span data-ttu-id="82434-132">Функция [**D3DXMatrixOrthoLH**](d3dxmatrixortholh.md) является особым случаем функции **D3DXMatrixOrthoOffCenterLH** .</span><span class="sxs-lookup"><span data-stu-id="82434-132">The [**D3DXMatrixOrthoLH**](d3dxmatrixortholh.md) function is a special case of the **D3DXMatrixOrthoOffCenterLH** function.</span></span> <span data-ttu-id="82434-133">Чтобы создать ту же проекцию с помощью **D3DXMatrixOrthoOffCenterLH**, используйте следующие значения: l =-w/2, r = w/2, b =-h/2 и t = h/2.</span><span class="sxs-lookup"><span data-stu-id="82434-133">To create the same projection using **D3DXMatrixOrthoOffCenterLH**, use the following values: l = -w/2, r = w/2, b = -h/2, and t = h/2.</span></span>

<span data-ttu-id="82434-134">Все параметры функции **D3DXMatrixOrthoOffCenterLH** — это расстояния в пространстве камеры.</span><span class="sxs-lookup"><span data-stu-id="82434-134">All the parameters of the **D3DXMatrixOrthoOffCenterLH** function are distances in camera space.</span></span> <span data-ttu-id="82434-135">Параметры описывают размеры представления объема.</span><span class="sxs-lookup"><span data-stu-id="82434-135">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="82434-136">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="82434-136">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="82434-137">Таким образом, функция **D3DXMatrixOrthoOffCenterLH** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="82434-137">In this way, the **D3DXMatrixOrthoOffCenterLH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="82434-138">Эта функция использует следующую формулу для вычисления возвращаемой матрицы.</span><span class="sxs-lookup"><span data-stu-id="82434-138">This function uses the following formula to compute the returned matrix.</span></span>


```
2/(r-l)      0            0           0
0            2/(t-b)      0           0
0            0            1/(zf-zn)   0
(l+r)/(l-r)  (t+b)/(b-t)  zn/(zn-zf)  1
```



## <a name="requirements"></a><span data-ttu-id="82434-139">Требования</span><span class="sxs-lookup"><span data-stu-id="82434-139">Requirements</span></span>



| <span data-ttu-id="82434-140">Требование</span><span class="sxs-lookup"><span data-stu-id="82434-140">Requirement</span></span> | <span data-ttu-id="82434-141">Значение</span><span class="sxs-lookup"><span data-stu-id="82434-141">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="82434-142">Header</span><span class="sxs-lookup"><span data-stu-id="82434-142">Header</span></span><br/>  | <dl> <span data-ttu-id="82434-143"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="82434-143"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="82434-144">Библиотека</span><span class="sxs-lookup"><span data-stu-id="82434-144">Library</span></span><br/> | <dl> <span data-ttu-id="82434-145"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="82434-145"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="82434-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="82434-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82434-147">Математические функции</span><span class="sxs-lookup"><span data-stu-id="82434-147">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="82434-148">**D3DXMatrixOrthoRH**</span><span class="sxs-lookup"><span data-stu-id="82434-148">**D3DXMatrixOrthoRH**</span></span>](d3dxmatrixorthorh.md)
</dt> <dt>

[<span data-ttu-id="82434-149">**D3DXMatrixOrthoLH**</span><span class="sxs-lookup"><span data-stu-id="82434-149">**D3DXMatrixOrthoLH**</span></span>](d3dxmatrixortholh.md)
</dt> <dt>

[<span data-ttu-id="82434-150">**D3DXMatrixOrthoOffCenterRH**</span><span class="sxs-lookup"><span data-stu-id="82434-150">**D3DXMatrixOrthoOffCenterRH**</span></span>](d3dxmatrixorthooffcenterrh.md)
</dt> </dl>

 

 
