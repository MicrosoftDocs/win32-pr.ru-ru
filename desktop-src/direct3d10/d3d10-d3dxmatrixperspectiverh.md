---
description: Функция D3DXMatrixPerspectiveRH (D3DX10Math. h) — формирует матрицу правой проекции перспективы.
ms.assetid: 324c8a21-24ef-4b3a-aac1-a753e26076d4
title: Функция D3DXMatrixPerspectiveRH (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixPerspectiveRH
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 03ffd99d016023612daa3de96ae29275d71074a0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109012"
---
# <a name="d3dxmatrixperspectiverh-function-d3dx10mathh"></a><span data-ttu-id="c5831-103">Функция D3DXMatrixPerspectiveRH (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="c5831-103">D3DXMatrixPerspectiveRH function (D3DX10Math.h)</span></span>

<span data-ttu-id="c5831-104">Строит правовинтовую матрицу перспективной проекции.</span><span class="sxs-lookup"><span data-stu-id="c5831-104">Builds a right-handed perspective projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5831-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c5831-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveRH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      w,
  _In_    FLOAT      h,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="c5831-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c5831-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5831-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="c5831-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c5831-108">Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="c5831-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c5831-109">Указатель на структуру [**D3DXMATRIX**](d3d10-d3dxmatrix.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="c5831-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="c5831-110">*w* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="c5831-110">*w* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5831-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c5831-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c5831-112">Ширина отображаемого объема на ближайшей плоскости представления.</span><span class="sxs-lookup"><span data-stu-id="c5831-112">Width of the view volume at the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="c5831-113">*ч* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="c5831-113">*h* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5831-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c5831-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c5831-115">Высота отображаемого объема на ближайшей плоскости представления.</span><span class="sxs-lookup"><span data-stu-id="c5831-115">Height of the view volume at the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="c5831-116">*ЗН* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c5831-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5831-117">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c5831-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c5831-118">Z-значение ближней плоскости просмотра.</span><span class="sxs-lookup"><span data-stu-id="c5831-118">Z-value of the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="c5831-119">*ЗФ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c5831-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5831-120">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c5831-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c5831-121">Z-значение дальней плоскости просмотра.</span><span class="sxs-lookup"><span data-stu-id="c5831-121">Z-value of the far view-plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5831-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c5831-122">Return value</span></span>

<span data-ttu-id="c5831-123">Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="c5831-123">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c5831-124">Указатель на структуру D3DXMATRIX, которая является матрицей с правой стороны проекций.</span><span class="sxs-lookup"><span data-stu-id="c5831-124">Pointer to a D3DXMATRIX structure that is a right-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5831-125">Remarks</span><span class="sxs-lookup"><span data-stu-id="c5831-125">Remarks</span></span>

<span data-ttu-id="c5831-126">Все параметры функции D3DXMatrixPerspectiveRH — это расстояния в пространстве камеры.</span><span class="sxs-lookup"><span data-stu-id="c5831-126">All the parameters of the D3DXMatrixPerspectiveRH function are distances in camera space.</span></span> <span data-ttu-id="c5831-127">Параметры описывают размеры представления объема.</span><span class="sxs-lookup"><span data-stu-id="c5831-127">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="c5831-128">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="c5831-128">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="c5831-129">Таким образом, функция D3DXMatrixPerspectiveRH может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="c5831-129">In this way, the D3DXMatrixPerspectiveRH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="c5831-130">Эта функция использует следующую формулу для вычисления возвращаемой матрицы.</span><span class="sxs-lookup"><span data-stu-id="c5831-130">This function uses the following formula to compute the returned matrix.</span></span>


```
2*zn/w  0       0              0
0       2*zn/h  0              0
0       0       zf/(zn-zf)    -1
0       0       zn*zf/(zn-zf)  0
```



## <a name="requirements"></a><span data-ttu-id="c5831-131">Требования</span><span class="sxs-lookup"><span data-stu-id="c5831-131">Requirements</span></span>



| <span data-ttu-id="c5831-132">Требование</span><span class="sxs-lookup"><span data-stu-id="c5831-132">Requirement</span></span> | <span data-ttu-id="c5831-133">Значение</span><span class="sxs-lookup"><span data-stu-id="c5831-133">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c5831-134">Header</span><span class="sxs-lookup"><span data-stu-id="c5831-134">Header</span></span><br/>  | <dl> <span data-ttu-id="c5831-135"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5831-135"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="c5831-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c5831-136">Library</span></span><br/> | <dl> <span data-ttu-id="c5831-137"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c5831-137"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c5831-138">См. также</span><span class="sxs-lookup"><span data-stu-id="c5831-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5831-139">Математические функции</span><span class="sxs-lookup"><span data-stu-id="c5831-139">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
