---
description: Функция D3DXMatrixRotationX (D3DX10Math. h) — строит матрицу, которая поворачивается вокруг оси x.
ms.assetid: 895079bf-b807-4bfd-9222-a7c1251d7d1e
title: Функция D3DXMatrixRotationX (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixRotationX
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 53c4bf27a359bd6d131f8d6d9c685e929d1a9ec1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108992"
---
# <a name="d3dxmatrixrotationx-function-d3dx10mathh"></a><span data-ttu-id="bb3c3-103">Функция D3DXMatrixRotationX (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="bb3c3-103">D3DXMatrixRotationX function (D3DX10Math.h)</span></span>

<span data-ttu-id="bb3c3-104">Строит матрицу, которая поворачивается вокруг оси x.</span><span class="sxs-lookup"><span data-stu-id="bb3c3-104">Builds a matrix that rotates around the x-axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb3c3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bb3c3-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationX(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      Angle
);
```



## <a name="parameters"></a><span data-ttu-id="bb3c3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bb3c3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb3c3-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="bb3c3-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="bb3c3-108">Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="bb3c3-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="bb3c3-109">Указатель на структуру [**D3DXMATRIX**](d3d10-d3dxmatrix.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="bb3c3-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="bb3c3-110">*Угол* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bb3c3-110">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb3c3-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bb3c3-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bb3c3-112">Угол поворота в радианах.</span><span class="sxs-lookup"><span data-stu-id="bb3c3-112">Angle of rotation in radians.</span></span> <span data-ttu-id="bb3c3-113">Углы измеряются по часовой стрелке, если смотреть вдоль оси поворота в направлении начала координат.</span><span class="sxs-lookup"><span data-stu-id="bb3c3-113">Angles are measured clockwise when looking along the rotation axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb3c3-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bb3c3-114">Return value</span></span>

<span data-ttu-id="bb3c3-115">Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="bb3c3-115">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="bb3c3-116">Указатель на структуру D3DXMATRIX, повернутую вокруг оси x.</span><span class="sxs-lookup"><span data-stu-id="bb3c3-116">Pointer to a D3DXMATRIX structure rotated around the x-axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb3c3-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="bb3c3-117">Remarks</span></span>

<span data-ttu-id="bb3c3-118">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="bb3c3-118">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="bb3c3-119">Таким образом, функция D3DXMatrixRotationX может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="bb3c3-119">In this way, the D3DXMatrixRotationX function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb3c3-120">Требования</span><span class="sxs-lookup"><span data-stu-id="bb3c3-120">Requirements</span></span>



| <span data-ttu-id="bb3c3-121">Требование</span><span class="sxs-lookup"><span data-stu-id="bb3c3-121">Requirement</span></span> | <span data-ttu-id="bb3c3-122">Значение</span><span class="sxs-lookup"><span data-stu-id="bb3c3-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bb3c3-123">Header</span><span class="sxs-lookup"><span data-stu-id="bb3c3-123">Header</span></span><br/>  | <dl> <span data-ttu-id="bb3c3-124"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb3c3-124"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="bb3c3-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="bb3c3-125">Library</span></span><br/> | <dl> <span data-ttu-id="bb3c3-126"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bb3c3-126"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bb3c3-127">См. также</span><span class="sxs-lookup"><span data-stu-id="bb3c3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb3c3-128">Математические функции</span><span class="sxs-lookup"><span data-stu-id="bb3c3-128">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
