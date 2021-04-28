---
description: Функция D3DXMatrixPerspectiveOffCenterLH (D3dx9math. h) — создает настроенную левую матрицу проекции с левой стороны.
ms.assetid: de2732dd-a4f2-47bc-9509-de16f1ca85c2
title: Функция D3DXMatrixPerspectiveOffCenterLH (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixPerspectiveOffCenterLH
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 404147cfbab0b4fedb7c7356dc1c31d3e203eb5f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118292"
---
# <a name="d3dxmatrixperspectiveoffcenterlh-function-d3dx9mathh"></a><span data-ttu-id="d8f92-103">Функция D3DXMatrixPerspectiveOffCenterLH (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="d8f92-103">D3DXMatrixPerspectiveOffCenterLH function (D3dx9math.h)</span></span>

<span data-ttu-id="d8f92-104">Создает настроенную левую матрицу проекции с левой стороны.</span><span class="sxs-lookup"><span data-stu-id="d8f92-104">Builds a customized, left-handed perspective projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8f92-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d8f92-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveOffCenterLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      l,
  _In_    FLOAT      r,
  _In_    FLOAT      b,
  _In_    FLOAT      t,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="d8f92-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d8f92-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8f92-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="d8f92-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d8f92-108">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="d8f92-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d8f92-109">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="d8f92-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="d8f92-110">*l* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="d8f92-110">*l* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8f92-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d8f92-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d8f92-112">Минимальное значение x для представления объема.</span><span class="sxs-lookup"><span data-stu-id="d8f92-112">Minimum x-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="d8f92-113">*r* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="d8f92-113">*r* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8f92-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d8f92-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d8f92-115">Максимальное значение x-значения для представления объема.</span><span class="sxs-lookup"><span data-stu-id="d8f92-115">Maximum x-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="d8f92-116">*б* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="d8f92-116">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8f92-117">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d8f92-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d8f92-118">Минимальное значение y для представления объема.</span><span class="sxs-lookup"><span data-stu-id="d8f92-118">Minimum y-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="d8f92-119">*t* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="d8f92-119">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8f92-120">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d8f92-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d8f92-121">Максимальное значение y для представления объема.</span><span class="sxs-lookup"><span data-stu-id="d8f92-121">Maximum y-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="d8f92-122">*ЗН* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d8f92-122">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8f92-123">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d8f92-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d8f92-124">Минимальное z-значение отображаемого объема.</span><span class="sxs-lookup"><span data-stu-id="d8f92-124">Minimum z-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="d8f92-125">*ЗФ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d8f92-125">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8f92-126">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d8f92-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d8f92-127">Максимальное z-значение отображаемого объема.</span><span class="sxs-lookup"><span data-stu-id="d8f92-127">Maximum z-value of the view volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8f92-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d8f92-128">Return value</span></span>

<span data-ttu-id="d8f92-129">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="d8f92-129">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d8f92-130">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , которая является настраиваемой матрицей проекции слева.</span><span class="sxs-lookup"><span data-stu-id="d8f92-130">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is a customized, left-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8f92-131">Remarks</span><span class="sxs-lookup"><span data-stu-id="d8f92-131">Remarks</span></span>

<span data-ttu-id="d8f92-132">Все параметры функции **D3DXMatrixPerspectiveOffCenterLH** — это расстояния в пространстве камеры.</span><span class="sxs-lookup"><span data-stu-id="d8f92-132">All the parameters of the **D3DXMatrixPerspectiveOffCenterLH** function are distances in camera space.</span></span> <span data-ttu-id="d8f92-133">Параметры описывают размеры представления объема.</span><span class="sxs-lookup"><span data-stu-id="d8f92-133">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="d8f92-134">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="d8f92-134">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="d8f92-135">Таким образом, функция **D3DXMatrixPerspectiveOffCenterLH** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="d8f92-135">In this way, the **D3DXMatrixPerspectiveOffCenterLH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="d8f92-136">Эта функция использует следующую формулу для вычисления возвращаемой матрицы.</span><span class="sxs-lookup"><span data-stu-id="d8f92-136">This function uses the following formula to compute the returned matrix.</span></span>


```
2*zn/(r-l)   0            0              0
0            2*zn/(t-b)   0              0
(l+r)/(l-r)  (t+b)/(b-t)  zf/(zf-zn)     1
0            0            zn*zf/(zn-zf)  0
```



## <a name="requirements"></a><span data-ttu-id="d8f92-137">Требования</span><span class="sxs-lookup"><span data-stu-id="d8f92-137">Requirements</span></span>



| <span data-ttu-id="d8f92-138">Требование</span><span class="sxs-lookup"><span data-stu-id="d8f92-138">Requirement</span></span> | <span data-ttu-id="d8f92-139">Значение</span><span class="sxs-lookup"><span data-stu-id="d8f92-139">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d8f92-140">Header</span><span class="sxs-lookup"><span data-stu-id="d8f92-140">Header</span></span><br/>  | <dl> <span data-ttu-id="d8f92-141"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8f92-141"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="d8f92-142">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d8f92-142">Library</span></span><br/> | <dl> <span data-ttu-id="d8f92-143"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d8f92-143"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d8f92-144">См. также</span><span class="sxs-lookup"><span data-stu-id="d8f92-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8f92-145">Математические функции</span><span class="sxs-lookup"><span data-stu-id="d8f92-145">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="d8f92-146">**D3DXMatrixPerspectiveRH**</span><span class="sxs-lookup"><span data-stu-id="d8f92-146">**D3DXMatrixPerspectiveRH**</span></span>](d3dxmatrixperspectiverh.md)
</dt> <dt>

[<span data-ttu-id="d8f92-147">**D3DXMatrixPerspectiveLH**</span><span class="sxs-lookup"><span data-stu-id="d8f92-147">**D3DXMatrixPerspectiveLH**</span></span>](d3dxmatrixperspectivelh.md)
</dt> <dt>

[<span data-ttu-id="d8f92-148">**D3DXMatrixPerspectiveFovRH**</span><span class="sxs-lookup"><span data-stu-id="d8f92-148">**D3DXMatrixPerspectiveFovRH**</span></span>](d3dxmatrixperspectivefovrh.md)
</dt> <dt>

[<span data-ttu-id="d8f92-149">**D3DXMatrixPerspectiveFovLH**</span><span class="sxs-lookup"><span data-stu-id="d8f92-149">**D3DXMatrixPerspectiveFovLH**</span></span>](d3dxmatrixperspectivefovlh.md)
</dt> <dt>

[<span data-ttu-id="d8f92-150">**D3DXMatrixPerspectiveOffCenterRH**</span><span class="sxs-lookup"><span data-stu-id="d8f92-150">**D3DXMatrixPerspectiveOffCenterRH**</span></span>](d3dxmatrixperspectiveoffcenterrh.md)
</dt> </dl>

 

 
