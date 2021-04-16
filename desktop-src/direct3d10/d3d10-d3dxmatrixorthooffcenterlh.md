---
description: Создает настроенную левую матрицу ортогональной проекции.
ms.assetid: 84175c08-5a0b-4183-afe2-8aecafd73897
title: Функция D3DXMatrixOrthoOffCenterLH (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4292f2996b4a19b71531094e5bf39bf7c213b972
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105720930"
---
# <a name="d3dxmatrixorthooffcenterlh-function-d3dx10mathh"></a><span data-ttu-id="63a2d-103">Функция D3DXMatrixOrthoOffCenterLH (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="63a2d-103">D3DXMatrixOrthoOffCenterLH function (D3DX10Math.h)</span></span>

<span data-ttu-id="63a2d-104">Создает настроенную левую матрицу ортогональной проекции.</span><span class="sxs-lookup"><span data-stu-id="63a2d-104">Builds a customized, left-handed orthographic projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="63a2d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="63a2d-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="63a2d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="63a2d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63a2d-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="63a2d-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="63a2d-108">Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="63a2d-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="63a2d-109">Указатель на результирующий [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="63a2d-109">Pointer to the resulting [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="63a2d-110">*l* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="63a2d-110">*l* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63a2d-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="63a2d-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="63a2d-112">Минимальное значение x для представления объема.</span><span class="sxs-lookup"><span data-stu-id="63a2d-112">Minimum x-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="63a2d-113">*r* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="63a2d-113">*r* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63a2d-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="63a2d-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="63a2d-115">Максимальное значение x-значения для представления объема.</span><span class="sxs-lookup"><span data-stu-id="63a2d-115">Maximum x-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="63a2d-116">*б* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="63a2d-116">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63a2d-117">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="63a2d-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="63a2d-118">Минимальное значение y для параметра "Показать том".</span><span class="sxs-lookup"><span data-stu-id="63a2d-118">Minimum y-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="63a2d-119">*t* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="63a2d-119">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63a2d-120">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="63a2d-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="63a2d-121">Максимальное значение y для параметра "Показать том".</span><span class="sxs-lookup"><span data-stu-id="63a2d-121">Maximum y-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="63a2d-122">*ЗН* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="63a2d-122">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63a2d-123">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="63a2d-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="63a2d-124">Минимальное z-значение отображаемого объема.</span><span class="sxs-lookup"><span data-stu-id="63a2d-124">Minimum z-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="63a2d-125">*ЗФ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="63a2d-125">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63a2d-126">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="63a2d-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="63a2d-127">Максимальное z-значение отображаемого объема.</span><span class="sxs-lookup"><span data-stu-id="63a2d-127">Maximum z-value of the view volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63a2d-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="63a2d-128">Return value</span></span>

<span data-ttu-id="63a2d-129">Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="63a2d-129">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="63a2d-130">Указатель на результирующий [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="63a2d-130">Pointer to the resulting [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="63a2d-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="63a2d-131">Remarks</span></span>

<span data-ttu-id="63a2d-132">[**D3DXMatrixOrthoLH**](d3d10-d3dxmatrixortholh.md) — это особый случай функции D3DXMatrixOrthoOffCenterLH.</span><span class="sxs-lookup"><span data-stu-id="63a2d-132">The [**D3DXMatrixOrthoLH**](d3d10-d3dxmatrixortholh.md) is a special case of the D3DXMatrixOrthoOffCenterLH function.</span></span> <span data-ttu-id="63a2d-133">Чтобы создать ту же проекцию с помощью D3DXMatrixOrthoOffCenterLH, используйте следующие значения:</span><span class="sxs-lookup"><span data-stu-id="63a2d-133">To create the same projection using D3DXMatrixOrthoOffCenterLH, use the following values:</span></span>

<span data-ttu-id="63a2d-134">l =-w/2,</span><span class="sxs-lookup"><span data-stu-id="63a2d-134">l = -w/2,</span></span>

<span data-ttu-id="63a2d-135">r = w/2,</span><span class="sxs-lookup"><span data-stu-id="63a2d-135">r = w/2,</span></span>

<span data-ttu-id="63a2d-136">b =-h/2, и</span><span class="sxs-lookup"><span data-stu-id="63a2d-136">b = -h/2, and</span></span>

<span data-ttu-id="63a2d-137">t = h/2.</span><span class="sxs-lookup"><span data-stu-id="63a2d-137">t = h/2.</span></span>

<span data-ttu-id="63a2d-138">Все параметры функции D3DXMatrixOrthoOffCenterLH — это расстояния в пространстве камеры.</span><span class="sxs-lookup"><span data-stu-id="63a2d-138">All the parameters of the D3DXMatrixOrthoOffCenterLH function are distances in camera space.</span></span> <span data-ttu-id="63a2d-139">Параметры описывают размеры представления объема.</span><span class="sxs-lookup"><span data-stu-id="63a2d-139">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="63a2d-140">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="63a2d-140">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="63a2d-141">Таким образом, функция D3DXMatrixOrthoOffCenterLH может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="63a2d-141">In this way, the D3DXMatrixOrthoOffCenterLH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="63a2d-142">Эта функция использует следующую формулу для вычисления возвращаемой матрицы.</span><span class="sxs-lookup"><span data-stu-id="63a2d-142">This function uses the following formula to compute the returned matrix.</span></span>


```
2/(r-l)      0            0           0
0            2/(t-b)      0           0
0            0            1/(zf-zn)   0
(l+r)/(l-r)  (t+b)/(b-t)  zn/(zn-zf)  1
```



## <a name="requirements"></a><span data-ttu-id="63a2d-143">Требования</span><span class="sxs-lookup"><span data-stu-id="63a2d-143">Requirements</span></span>



| <span data-ttu-id="63a2d-144">Требование</span><span class="sxs-lookup"><span data-stu-id="63a2d-144">Requirement</span></span> | <span data-ttu-id="63a2d-145">Значение</span><span class="sxs-lookup"><span data-stu-id="63a2d-145">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="63a2d-146">Header</span><span class="sxs-lookup"><span data-stu-id="63a2d-146">Header</span></span><br/>  | <dl> <span data-ttu-id="63a2d-147"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="63a2d-147"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="63a2d-148">Библиотека</span><span class="sxs-lookup"><span data-stu-id="63a2d-148">Library</span></span><br/> | <dl> <span data-ttu-id="63a2d-149"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="63a2d-149"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="63a2d-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="63a2d-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63a2d-151">Математические функции</span><span class="sxs-lookup"><span data-stu-id="63a2d-151">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
