---
description: Создает настроенную правую матрицу ортогональной проекции.
ms.assetid: 01d4d61e-de7b-4431-a168-68a50b1d6021
title: Функция D3DXMatrixOrthoOffCenterRH (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 3b5b544a4144ebc283686385638435ec42b4d801
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105720929"
---
# <a name="d3dxmatrixorthooffcenterrh-function-d3dx10mathh"></a><span data-ttu-id="64c78-103">Функция D3DXMatrixOrthoOffCenterRH (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="64c78-103">D3DXMatrixOrthoOffCenterRH function (D3DX10Math.h)</span></span>

<span data-ttu-id="64c78-104">Создает настроенную правую матрицу ортогональной проекции.</span><span class="sxs-lookup"><span data-stu-id="64c78-104">Builds a customized, right-handed orthographic projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="64c78-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="64c78-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="64c78-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="64c78-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64c78-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="64c78-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="64c78-108">Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="64c78-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="64c78-109">Указатель на результирующий [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="64c78-109">Pointer to the resulting [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="64c78-110">*l* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="64c78-110">*l* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64c78-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="64c78-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="64c78-112">Минимальное значение x для представления объема.</span><span class="sxs-lookup"><span data-stu-id="64c78-112">Minimum x-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="64c78-113">*r* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="64c78-113">*r* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64c78-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="64c78-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="64c78-115">Максимальное значение x-значения для представления объема.</span><span class="sxs-lookup"><span data-stu-id="64c78-115">Maximum x-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="64c78-116">*б* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="64c78-116">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64c78-117">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="64c78-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="64c78-118">Минимальное значение y для параметра "Показать том".</span><span class="sxs-lookup"><span data-stu-id="64c78-118">Minimum y-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="64c78-119">*t* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="64c78-119">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64c78-120">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="64c78-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="64c78-121">Максимальное значение y для параметра "Показать том".</span><span class="sxs-lookup"><span data-stu-id="64c78-121">Maximum y-value of view volume.</span></span>

</dd> <dt>

<span data-ttu-id="64c78-122">*ЗН* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="64c78-122">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64c78-123">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="64c78-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="64c78-124">Минимальное z-значение отображаемого объема.</span><span class="sxs-lookup"><span data-stu-id="64c78-124">Minimum z-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="64c78-125">*ЗФ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="64c78-125">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64c78-126">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="64c78-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="64c78-127">Максимальное z-значение отображаемого объема.</span><span class="sxs-lookup"><span data-stu-id="64c78-127">Maximum z-value of the view volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64c78-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="64c78-128">Return value</span></span>

<span data-ttu-id="64c78-129">Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="64c78-129">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="64c78-130">Указатель на результирующий [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="64c78-130">Pointer to the resulting [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="64c78-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="64c78-131">Remarks</span></span>

<span data-ttu-id="64c78-132">Функция [**D3DXMatrixOrthoRH**](d3d10-d3dxmatrixorthorh.md) является особым случаем функции D3DXMatrixOrthoOffCenterRH.</span><span class="sxs-lookup"><span data-stu-id="64c78-132">The [**D3DXMatrixOrthoRH**](d3d10-d3dxmatrixorthorh.md) function is a special case of the D3DXMatrixOrthoOffCenterRH function.</span></span> <span data-ttu-id="64c78-133">Чтобы создать ту же проекцию с помощью D3DXMatrixOrthoOffCenterRH, используйте следующие значения:</span><span class="sxs-lookup"><span data-stu-id="64c78-133">To create the same projection using D3DXMatrixOrthoOffCenterRH, use the following values:</span></span>

<span data-ttu-id="64c78-134">l =-w/2,</span><span class="sxs-lookup"><span data-stu-id="64c78-134">l = -w/2,</span></span>

<span data-ttu-id="64c78-135">r = w/2,</span><span class="sxs-lookup"><span data-stu-id="64c78-135">r = w/2,</span></span>

<span data-ttu-id="64c78-136">b =-h/2, и</span><span class="sxs-lookup"><span data-stu-id="64c78-136">b = -h/2, and</span></span>

<span data-ttu-id="64c78-137">t = h/2.</span><span class="sxs-lookup"><span data-stu-id="64c78-137">t = h/2.</span></span>

<span data-ttu-id="64c78-138">Все параметры функции D3DXMatrixOrthoOffCenterRH — это расстояния в пространстве камеры.</span><span class="sxs-lookup"><span data-stu-id="64c78-138">All the parameters of the D3DXMatrixOrthoOffCenterRH function are distances in camera space.</span></span> <span data-ttu-id="64c78-139">Параметры описывают размеры представления объема.</span><span class="sxs-lookup"><span data-stu-id="64c78-139">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="64c78-140">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="64c78-140">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="64c78-141">Таким образом, функция D3DXMatrixOrthoOffCenterRH может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="64c78-141">In this way, the D3DXMatrixOrthoOffCenterRH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="64c78-142">Эта функция использует следующую формулу для вычисления возвращаемой матрицы.</span><span class="sxs-lookup"><span data-stu-id="64c78-142">This function uses the following formula to compute the returned matrix.</span></span>


```
2/(r-l)      0            0           0
0            2/(t-b)      0           0
0            0            1/(zn-zf)   0
(l+r)/(l-r)  (t+b)/(b-t)  zn/(zn-zf)  1
```



## <a name="requirements"></a><span data-ttu-id="64c78-143">Требования</span><span class="sxs-lookup"><span data-stu-id="64c78-143">Requirements</span></span>



| <span data-ttu-id="64c78-144">Требование</span><span class="sxs-lookup"><span data-stu-id="64c78-144">Requirement</span></span> | <span data-ttu-id="64c78-145">Значение</span><span class="sxs-lookup"><span data-stu-id="64c78-145">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="64c78-146">Header</span><span class="sxs-lookup"><span data-stu-id="64c78-146">Header</span></span><br/>  | <dl> <span data-ttu-id="64c78-147"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="64c78-147"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="64c78-148">Библиотека</span><span class="sxs-lookup"><span data-stu-id="64c78-148">Library</span></span><br/> | <dl> <span data-ttu-id="64c78-149"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="64c78-149"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="64c78-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="64c78-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64c78-151">Математические функции</span><span class="sxs-lookup"><span data-stu-id="64c78-151">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
