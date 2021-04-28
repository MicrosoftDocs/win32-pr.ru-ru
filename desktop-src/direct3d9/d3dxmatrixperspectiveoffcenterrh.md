---
description: Функция D3DXMatrixPerspectiveOffCenterRH (D3dx9math. h) — создает настраиваемую, правую матрицу проекции с правой стороны.
ms.assetid: e6826e46-fc80-41fa-b0d8-45b6797df76f
title: Функция D3DXMatrixPerspectiveOffCenterRH (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixPerspectiveOffCenterRH
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3d051894a6706cf8d58b81a85003666513f2a956
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118282"
---
# <a name="d3dxmatrixperspectiveoffcenterrh-function-d3dx9mathh"></a><span data-ttu-id="71610-103">Функция D3DXMatrixPerspectiveOffCenterRH (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="71610-103">D3DXMatrixPerspectiveOffCenterRH function (D3dx9math.h)</span></span>

<span data-ttu-id="71610-104">Создает настраиваемую, правую матрицу перспективной проекции.</span><span class="sxs-lookup"><span data-stu-id="71610-104">Builds a customized, right-handed perspective projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="71610-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="71610-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveOffCenterRH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      l,
  _In_    FLOAT      r,
  _In_    FLOAT      b,
  _In_    FLOAT      t,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="71610-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="71610-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71610-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="71610-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="71610-108">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="71610-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="71610-109">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="71610-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="71610-110">*l* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="71610-110">*l* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71610-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="71610-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="71610-112">Минимальное значение x для представления объема.</span><span class="sxs-lookup"><span data-stu-id="71610-112">Minimum x-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="71610-113">*r* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="71610-113">*r* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71610-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="71610-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="71610-115">Максимальное значение x-значения для представления объема.</span><span class="sxs-lookup"><span data-stu-id="71610-115">Maximum x-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="71610-116">*б* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="71610-116">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71610-117">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="71610-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="71610-118">Минимальное значение y для представления объема.</span><span class="sxs-lookup"><span data-stu-id="71610-118">Minimum y-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="71610-119">*t* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="71610-119">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71610-120">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="71610-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="71610-121">Максимальное значение y для представления объема.</span><span class="sxs-lookup"><span data-stu-id="71610-121">Maximum y-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="71610-122">*ЗН* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="71610-122">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71610-123">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="71610-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="71610-124">Минимальное z-значение отображаемого объема.</span><span class="sxs-lookup"><span data-stu-id="71610-124">Minimum z-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="71610-125">*ЗФ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="71610-125">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71610-126">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="71610-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="71610-127">Максимальное z-значение отображаемого объема.</span><span class="sxs-lookup"><span data-stu-id="71610-127">Maximum z-value of the view volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71610-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="71610-128">Return value</span></span>

<span data-ttu-id="71610-129">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="71610-129">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="71610-130">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , которая представляет собой настраиваемую, правую матрицу проекции с правой стороны.</span><span class="sxs-lookup"><span data-stu-id="71610-130">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is a customized, right-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="71610-131">Remarks</span><span class="sxs-lookup"><span data-stu-id="71610-131">Remarks</span></span>

<span data-ttu-id="71610-132">Все параметры функции **D3DXMatrixPerspectiveOffCenterRH** — это расстояния в пространстве камеры.</span><span class="sxs-lookup"><span data-stu-id="71610-132">All the parameters of the **D3DXMatrixPerspectiveOffCenterRH** function are distances in camera space.</span></span> <span data-ttu-id="71610-133">Параметры описывают размеры представления объема.</span><span class="sxs-lookup"><span data-stu-id="71610-133">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="71610-134">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="71610-134">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="71610-135">Таким образом, функция **D3DXMatrixPerspectiveOffCenterRH** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="71610-135">In this way, the **D3DXMatrixPerspectiveOffCenterRH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="71610-136">Эта функция использует следующую формулу для вычисления возвращаемой матрицы.</span><span class="sxs-lookup"><span data-stu-id="71610-136">This function uses the following formula to compute the returned matrix.</span></span>


```
2*zn/(r-l)   0            0                0
0            2*zn/(t-b)   0                0
(l+r)/(r-l)  (t+b)/(t-b)  zf/(zn-zf)      -1
0            0            zn*zf/(zn-zf)    0
```



## <a name="requirements"></a><span data-ttu-id="71610-137">Требования</span><span class="sxs-lookup"><span data-stu-id="71610-137">Requirements</span></span>



| <span data-ttu-id="71610-138">Требование</span><span class="sxs-lookup"><span data-stu-id="71610-138">Requirement</span></span> | <span data-ttu-id="71610-139">Значение</span><span class="sxs-lookup"><span data-stu-id="71610-139">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="71610-140">Header</span><span class="sxs-lookup"><span data-stu-id="71610-140">Header</span></span><br/>  | <dl> <span data-ttu-id="71610-141"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="71610-141"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="71610-142">Библиотека</span><span class="sxs-lookup"><span data-stu-id="71610-142">Library</span></span><br/> | <dl> <span data-ttu-id="71610-143"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="71610-143"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="71610-144">См. также</span><span class="sxs-lookup"><span data-stu-id="71610-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71610-145">Математические функции</span><span class="sxs-lookup"><span data-stu-id="71610-145">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="71610-146">**D3DXMatrixPerspectiveRH**</span><span class="sxs-lookup"><span data-stu-id="71610-146">**D3DXMatrixPerspectiveRH**</span></span>](d3dxmatrixperspectiverh.md)
</dt> <dt>

[<span data-ttu-id="71610-147">**D3DXMatrixPerspectiveLH**</span><span class="sxs-lookup"><span data-stu-id="71610-147">**D3DXMatrixPerspectiveLH**</span></span>](d3dxmatrixperspectivelh.md)
</dt> <dt>

[<span data-ttu-id="71610-148">**D3DXMatrixPerspectiveFovRH**</span><span class="sxs-lookup"><span data-stu-id="71610-148">**D3DXMatrixPerspectiveFovRH**</span></span>](d3dxmatrixperspectivefovrh.md)
</dt> <dt>

[<span data-ttu-id="71610-149">**D3DXMatrixPerspectiveFovLH**</span><span class="sxs-lookup"><span data-stu-id="71610-149">**D3DXMatrixPerspectiveFovLH**</span></span>](d3dxmatrixperspectivefovlh.md)
</dt> <dt>

[<span data-ttu-id="71610-150">**D3DXMatrixPerspectiveOffCenterLH**</span><span class="sxs-lookup"><span data-stu-id="71610-150">**D3DXMatrixPerspectiveOffCenterLH**</span></span>](d3dxmatrixperspectiveoffcenterlh.md)
</dt> </dl>

 

 
