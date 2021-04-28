---
description: Функция D3DXMatrixPerspectiveLH (D3DX10Math. h) — строит матрицу левой проекции перспективы
ms.assetid: 5fd8da67-ff12-42fa-b915-b50fa2680b32
title: Функция D3DXMatrixPerspectiveLH (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixPerspectiveLH
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a0f6c976f64fe64d3ca583351ae5c7c32aa958fd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109102"
---
# <a name="d3dxmatrixperspectivelh-function-d3dx10mathh"></a><span data-ttu-id="a2346-103">Функция D3DXMatrixPerspectiveLH (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="a2346-103">D3DXMatrixPerspectiveLH function (D3DX10Math.h)</span></span>

<span data-ttu-id="a2346-104">Формирует матрицу левой проекции перспективы</span><span class="sxs-lookup"><span data-stu-id="a2346-104">Builds a left-handed perspective projection matrix</span></span>

## <a name="syntax"></a><span data-ttu-id="a2346-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a2346-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      w,
  _In_    FLOAT      h,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="a2346-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a2346-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2346-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="a2346-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a2346-108">Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="a2346-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="a2346-109">Указатель на структуру [**D3DXMATRIX**](d3d10-d3dxmatrix.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="a2346-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="a2346-110">*w* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="a2346-110">*w* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2346-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a2346-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a2346-112">Ширина отображаемого объема на ближайшей плоскости представления.</span><span class="sxs-lookup"><span data-stu-id="a2346-112">Width of the view volume at the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="a2346-113">*ч* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="a2346-113">*h* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2346-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a2346-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a2346-115">Высота отображаемого объема на ближайшей плоскости представления.</span><span class="sxs-lookup"><span data-stu-id="a2346-115">Height of the view volume at the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="a2346-116">*ЗН* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a2346-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2346-117">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a2346-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a2346-118">Z-значение ближней плоскости просмотра.</span><span class="sxs-lookup"><span data-stu-id="a2346-118">Z-value of the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="a2346-119">*ЗФ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a2346-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2346-120">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a2346-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a2346-121">Z-значение дальней плоскости просмотра.</span><span class="sxs-lookup"><span data-stu-id="a2346-121">Z-value of the far view-plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2346-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a2346-122">Return value</span></span>

<span data-ttu-id="a2346-123">Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="a2346-123">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="a2346-124">Указатель на структуру D3DXMATRIX, которая является матрицей перспективной проекции влево.</span><span class="sxs-lookup"><span data-stu-id="a2346-124">Pointer to a D3DXMATRIX structure that is a left-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2346-125">Remarks</span><span class="sxs-lookup"><span data-stu-id="a2346-125">Remarks</span></span>

<span data-ttu-id="a2346-126">Все параметры функции D3DXMatrixPerspectiveLH — это расстояния в пространстве камеры.</span><span class="sxs-lookup"><span data-stu-id="a2346-126">All the parameters of the D3DXMatrixPerspectiveLH function are distances in camera space.</span></span> <span data-ttu-id="a2346-127">Параметры описывают размеры представления объема.</span><span class="sxs-lookup"><span data-stu-id="a2346-127">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="a2346-128">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="a2346-128">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="a2346-129">Таким образом, функция D3DXMatrixPerspectiveLH может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="a2346-129">In this way, the D3DXMatrixPerspectiveLH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="a2346-130">Эта функция использует следующую формулу для вычисления возвращаемой матрицы.</span><span class="sxs-lookup"><span data-stu-id="a2346-130">This function uses the following formula to compute the returned matrix.</span></span>


```
2*zn/w  0       0              0
0       2*zn/h  0              0
0       0       zf/(zf-zn)     1
0       0       zn*zf/(zn-zf)  0
```



## <a name="requirements"></a><span data-ttu-id="a2346-131">Требования</span><span class="sxs-lookup"><span data-stu-id="a2346-131">Requirements</span></span>



| <span data-ttu-id="a2346-132">Требование</span><span class="sxs-lookup"><span data-stu-id="a2346-132">Requirement</span></span> | <span data-ttu-id="a2346-133">Значение</span><span class="sxs-lookup"><span data-stu-id="a2346-133">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a2346-134">Header</span><span class="sxs-lookup"><span data-stu-id="a2346-134">Header</span></span><br/>  | <dl> <span data-ttu-id="a2346-135"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2346-135"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="a2346-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a2346-136">Library</span></span><br/> | <dl> <span data-ttu-id="a2346-137"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a2346-137"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a2346-138">См. также</span><span class="sxs-lookup"><span data-stu-id="a2346-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2346-139">Математические функции</span><span class="sxs-lookup"><span data-stu-id="a2346-139">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
