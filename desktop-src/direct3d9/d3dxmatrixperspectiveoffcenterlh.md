---
description: Создает настроенную левую матрицу проекции с левой стороны.
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
ms.openlocfilehash: 15743af16be84587fd8dc03e845ffcd8bd8dbc2b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713477"
---
# <a name="d3dxmatrixperspectiveoffcenterlh-function-d3dx9mathh"></a><span data-ttu-id="c013a-103">Функция D3DXMatrixPerspectiveOffCenterLH (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="c013a-103">D3DXMatrixPerspectiveOffCenterLH function (D3dx9math.h)</span></span>

<span data-ttu-id="c013a-104">Создает настроенную левую матрицу проекции с левой стороны.</span><span class="sxs-lookup"><span data-stu-id="c013a-104">Builds a customized, left-handed perspective projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="c013a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c013a-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="c013a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c013a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c013a-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="c013a-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c013a-108">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="c013a-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c013a-109">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="c013a-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="c013a-110">*l* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="c013a-110">*l* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c013a-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c013a-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c013a-112">Минимальное значение x для представления объема.</span><span class="sxs-lookup"><span data-stu-id="c013a-112">Minimum x-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="c013a-113">*r* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="c013a-113">*r* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c013a-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c013a-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c013a-115">Максимальное значение x-значения для представления объема.</span><span class="sxs-lookup"><span data-stu-id="c013a-115">Maximum x-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="c013a-116">*б* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="c013a-116">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c013a-117">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c013a-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c013a-118">Минимальное значение y для представления объема.</span><span class="sxs-lookup"><span data-stu-id="c013a-118">Minimum y-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="c013a-119">*t* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="c013a-119">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c013a-120">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c013a-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c013a-121">Максимальное значение y для представления объема.</span><span class="sxs-lookup"><span data-stu-id="c013a-121">Maximum y-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="c013a-122">*ЗН* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c013a-122">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c013a-123">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c013a-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c013a-124">Минимальное z-значение отображаемого объема.</span><span class="sxs-lookup"><span data-stu-id="c013a-124">Minimum z-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="c013a-125">*ЗФ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c013a-125">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c013a-126">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c013a-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c013a-127">Максимальное z-значение отображаемого объема.</span><span class="sxs-lookup"><span data-stu-id="c013a-127">Maximum z-value of the view volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c013a-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c013a-128">Return value</span></span>

<span data-ttu-id="c013a-129">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="c013a-129">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c013a-130">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , которая является настраиваемой матрицей проекции слева.</span><span class="sxs-lookup"><span data-stu-id="c013a-130">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is a customized, left-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="c013a-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c013a-131">Remarks</span></span>

<span data-ttu-id="c013a-132">Все параметры функции **D3DXMatrixPerspectiveOffCenterLH** — это расстояния в пространстве камеры.</span><span class="sxs-lookup"><span data-stu-id="c013a-132">All the parameters of the **D3DXMatrixPerspectiveOffCenterLH** function are distances in camera space.</span></span> <span data-ttu-id="c013a-133">Параметры описывают размеры представления объема.</span><span class="sxs-lookup"><span data-stu-id="c013a-133">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="c013a-134">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="c013a-134">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="c013a-135">Таким образом, функция **D3DXMatrixPerspectiveOffCenterLH** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="c013a-135">In this way, the **D3DXMatrixPerspectiveOffCenterLH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="c013a-136">Эта функция использует следующую формулу для вычисления возвращаемой матрицы.</span><span class="sxs-lookup"><span data-stu-id="c013a-136">This function uses the following formula to compute the returned matrix.</span></span>


```
2*zn/(r-l)   0            0              0
0            2*zn/(t-b)   0              0
(l+r)/(l-r)  (t+b)/(b-t)  zf/(zf-zn)     1
0            0            zn*zf/(zn-zf)  0
```



## <a name="requirements"></a><span data-ttu-id="c013a-137">Требования</span><span class="sxs-lookup"><span data-stu-id="c013a-137">Requirements</span></span>



| <span data-ttu-id="c013a-138">Требование</span><span class="sxs-lookup"><span data-stu-id="c013a-138">Requirement</span></span> | <span data-ttu-id="c013a-139">Значение</span><span class="sxs-lookup"><span data-stu-id="c013a-139">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c013a-140">Header</span><span class="sxs-lookup"><span data-stu-id="c013a-140">Header</span></span><br/>  | <dl> <span data-ttu-id="c013a-141"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="c013a-141"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="c013a-142">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c013a-142">Library</span></span><br/> | <dl> <span data-ttu-id="c013a-143"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c013a-143"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c013a-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c013a-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c013a-145">Математические функции</span><span class="sxs-lookup"><span data-stu-id="c013a-145">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="c013a-146">**D3DXMatrixPerspectiveRH**</span><span class="sxs-lookup"><span data-stu-id="c013a-146">**D3DXMatrixPerspectiveRH**</span></span>](d3dxmatrixperspectiverh.md)
</dt> <dt>

[<span data-ttu-id="c013a-147">**D3DXMatrixPerspectiveLH**</span><span class="sxs-lookup"><span data-stu-id="c013a-147">**D3DXMatrixPerspectiveLH**</span></span>](d3dxmatrixperspectivelh.md)
</dt> <dt>

[<span data-ttu-id="c013a-148">**D3DXMatrixPerspectiveFovRH**</span><span class="sxs-lookup"><span data-stu-id="c013a-148">**D3DXMatrixPerspectiveFovRH**</span></span>](d3dxmatrixperspectivefovrh.md)
</dt> <dt>

[<span data-ttu-id="c013a-149">**D3DXMatrixPerspectiveFovLH**</span><span class="sxs-lookup"><span data-stu-id="c013a-149">**D3DXMatrixPerspectiveFovLH**</span></span>](d3dxmatrixperspectivefovlh.md)
</dt> <dt>

[<span data-ttu-id="c013a-150">**D3DXMatrixPerspectiveOffCenterRH**</span><span class="sxs-lookup"><span data-stu-id="c013a-150">**D3DXMatrixPerspectiveOffCenterRH**</span></span>](d3dxmatrixperspectiveoffcenterrh.md)
</dt> </dl>

 

 
