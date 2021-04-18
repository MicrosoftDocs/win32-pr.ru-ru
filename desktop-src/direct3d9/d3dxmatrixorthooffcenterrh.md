---
description: Создает настроенную правую матрицу ортогональной проекции.
ms.assetid: d6171e28-b138-4ccf-9f12-fb977a30aca1
title: Функция D3DXMatrixOrthoOffCenterRH (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixOrthoOffCenterRH
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7de5e4b3a872ea7466840e511fc0a57448861b55
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713874"
---
# <a name="d3dxmatrixorthooffcenterrh-function-d3dx9mathh"></a><span data-ttu-id="cc5ee-103">Функция D3DXMatrixOrthoOffCenterRH (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="cc5ee-103">D3DXMatrixOrthoOffCenterRH function (D3dx9math.h)</span></span>

<span data-ttu-id="cc5ee-104">Создает настроенную правую матрицу ортогональной проекции.</span><span class="sxs-lookup"><span data-stu-id="cc5ee-104">Builds a customized, right-handed orthographic projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc5ee-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cc5ee-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixOrthoOffCenterRH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      l,
  _In_    FLOAT      r,
  _In_    FLOAT      b,
  _In_    FLOAT      t,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="cc5ee-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cc5ee-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc5ee-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="cc5ee-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="cc5ee-108">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="cc5ee-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="cc5ee-109">Указатель на результирующий [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="cc5ee-109">Pointer to the resulting [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="cc5ee-110">*l* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="cc5ee-110">*l* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc5ee-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cc5ee-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cc5ee-112">Минимальное значение x для представления объема.</span><span class="sxs-lookup"><span data-stu-id="cc5ee-112">Minimum x-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="cc5ee-113">*r* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="cc5ee-113">*r* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc5ee-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cc5ee-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cc5ee-115">Максимальное значение x-значения для представления объема.</span><span class="sxs-lookup"><span data-stu-id="cc5ee-115">Maximum x-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="cc5ee-116">*б* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="cc5ee-116">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc5ee-117">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cc5ee-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cc5ee-118">Минимальное значение y для параметра "Показать том".</span><span class="sxs-lookup"><span data-stu-id="cc5ee-118">Minimum y-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="cc5ee-119">*t* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="cc5ee-119">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc5ee-120">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cc5ee-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cc5ee-121">Максимальное значение y для параметра "Показать том".</span><span class="sxs-lookup"><span data-stu-id="cc5ee-121">Maximum y-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="cc5ee-122">*ЗН* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cc5ee-122">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc5ee-123">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cc5ee-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cc5ee-124">Минимальное z-значение отображаемого объема.</span><span class="sxs-lookup"><span data-stu-id="cc5ee-124">Minimum z-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="cc5ee-125">*ЗФ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cc5ee-125">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc5ee-126">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cc5ee-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cc5ee-127">Максимальное z-значение отображаемого объема.</span><span class="sxs-lookup"><span data-stu-id="cc5ee-127">Maximum z-value of the view volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc5ee-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cc5ee-128">Return value</span></span>

<span data-ttu-id="cc5ee-129">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="cc5ee-129">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="cc5ee-130">Указатель на результирующий [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="cc5ee-130">Pointer to the resulting [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="cc5ee-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cc5ee-131">Remarks</span></span>

<span data-ttu-id="cc5ee-132">Функция [**D3DXMatrixOrthoRH**](d3dxmatrixorthorh.md) является особым случаем функции **D3DXMatrixOrthoOffCenterRH** .</span><span class="sxs-lookup"><span data-stu-id="cc5ee-132">The [**D3DXMatrixOrthoRH**](d3dxmatrixorthorh.md) function is a special case of the **D3DXMatrixOrthoOffCenterRH** function.</span></span> <span data-ttu-id="cc5ee-133">Чтобы создать ту же проекцию с помощью **D3DXMatrixOrthoOffCenterRH**, используйте следующие значения: l =-w/2, r = w/2, b =-h/2 и t = h/2.</span><span class="sxs-lookup"><span data-stu-id="cc5ee-133">To create the same projection using **D3DXMatrixOrthoOffCenterRH**, use the following values: l = -w/2, r = w/2, b = -h/2, and t = h/2.</span></span>

<span data-ttu-id="cc5ee-134">Все параметры функции **D3DXMatrixOrthoOffCenterRH** — это расстояния в пространстве камеры.</span><span class="sxs-lookup"><span data-stu-id="cc5ee-134">All the parameters of the **D3DXMatrixOrthoOffCenterRH** function are distances in camera space.</span></span> <span data-ttu-id="cc5ee-135">Параметры описывают размеры представления объема.</span><span class="sxs-lookup"><span data-stu-id="cc5ee-135">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="cc5ee-136">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="cc5ee-136">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="cc5ee-137">Таким образом, функция **D3DXMatrixOrthoOffCenterRH** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="cc5ee-137">In this way, the **D3DXMatrixOrthoOffCenterRH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="cc5ee-138">Эта функция использует следующую формулу для вычисления возвращаемой матрицы.</span><span class="sxs-lookup"><span data-stu-id="cc5ee-138">This function uses the following formula to compute the returned matrix.</span></span>


```
2/(r-l)      0            0           0
0            2/(t-b)      0           0
0            0            1/(zn-zf)   0
(l+r)/(l-r)  (t+b)/(b-t)  zn/(zn-zf)  1
```



## <a name="requirements"></a><span data-ttu-id="cc5ee-139">Требования</span><span class="sxs-lookup"><span data-stu-id="cc5ee-139">Requirements</span></span>



| <span data-ttu-id="cc5ee-140">Требование</span><span class="sxs-lookup"><span data-stu-id="cc5ee-140">Requirement</span></span> | <span data-ttu-id="cc5ee-141">Значение</span><span class="sxs-lookup"><span data-stu-id="cc5ee-141">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cc5ee-142">Header</span><span class="sxs-lookup"><span data-stu-id="cc5ee-142">Header</span></span><br/>  | <dl> <span data-ttu-id="cc5ee-143"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc5ee-143"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="cc5ee-144">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cc5ee-144">Library</span></span><br/> | <dl> <span data-ttu-id="cc5ee-145"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cc5ee-145"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="cc5ee-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cc5ee-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc5ee-147">Математические функции</span><span class="sxs-lookup"><span data-stu-id="cc5ee-147">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="cc5ee-148">**D3DXMatrixOrthoRH**</span><span class="sxs-lookup"><span data-stu-id="cc5ee-148">**D3DXMatrixOrthoRH**</span></span>](d3dxmatrixorthorh.md)
</dt> <dt>

[<span data-ttu-id="cc5ee-149">**D3DXMatrixOrthoLH**</span><span class="sxs-lookup"><span data-stu-id="cc5ee-149">**D3DXMatrixOrthoLH**</span></span>](d3dxmatrixortholh.md)
</dt> <dt>

[<span data-ttu-id="cc5ee-150">**D3DXMatrixOrthoOffCenterLH**</span><span class="sxs-lookup"><span data-stu-id="cc5ee-150">**D3DXMatrixOrthoOffCenterLH**</span></span>](d3dxmatrixorthooffcenterlh.md)
</dt> </dl>

 

 
