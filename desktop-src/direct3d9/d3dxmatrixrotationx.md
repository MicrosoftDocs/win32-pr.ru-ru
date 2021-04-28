---
description: Функция D3DXMatrixRotationX (D3dx9math. h) — строит матрицу, которая поворачивается вокруг оси x.
ms.assetid: 45a2668d-787f-4354-882a-94a72edaa543
title: Функция D3DXMatrixRotationX (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a4f51f8acab7caddd4571d60f7deae795440f02a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118182"
---
# <a name="d3dxmatrixrotationx-function-d3dx9mathh"></a><span data-ttu-id="e1cfa-103">Функция D3DXMatrixRotationX (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="e1cfa-103">D3DXMatrixRotationX function (D3dx9math.h)</span></span>

<span data-ttu-id="e1cfa-104">Строит матрицу, которая поворачивается вокруг оси x.</span><span class="sxs-lookup"><span data-stu-id="e1cfa-104">Builds a matrix that rotates around the x-axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1cfa-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e1cfa-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationX(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      Angle
);
```



## <a name="parameters"></a><span data-ttu-id="e1cfa-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e1cfa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1cfa-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="e1cfa-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e1cfa-108">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="e1cfa-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e1cfa-109">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="e1cfa-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="e1cfa-110">*Угол* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e1cfa-110">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1cfa-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e1cfa-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e1cfa-112">Угол поворота в радианах.</span><span class="sxs-lookup"><span data-stu-id="e1cfa-112">Angle of rotation in radians.</span></span> <span data-ttu-id="e1cfa-113">Углы измеряются по часовой стрелке, если смотреть вдоль оси поворота в направлении начала координат.</span><span class="sxs-lookup"><span data-stu-id="e1cfa-113">Angles are measured clockwise when looking along the rotation axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1cfa-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e1cfa-114">Return value</span></span>

<span data-ttu-id="e1cfa-115">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="e1cfa-115">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e1cfa-116">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , повернутую вокруг оси x.</span><span class="sxs-lookup"><span data-stu-id="e1cfa-116">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure rotated around the x-axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1cfa-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="e1cfa-117">Remarks</span></span>

<span data-ttu-id="e1cfa-118">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="e1cfa-118">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="e1cfa-119">Таким образом, функция **D3DXMatrixRotationX** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="e1cfa-119">In this way, the **D3DXMatrixRotationX** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1cfa-120">Требования</span><span class="sxs-lookup"><span data-stu-id="e1cfa-120">Requirements</span></span>



| <span data-ttu-id="e1cfa-121">Требование</span><span class="sxs-lookup"><span data-stu-id="e1cfa-121">Requirement</span></span> | <span data-ttu-id="e1cfa-122">Значение</span><span class="sxs-lookup"><span data-stu-id="e1cfa-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e1cfa-123">Header</span><span class="sxs-lookup"><span data-stu-id="e1cfa-123">Header</span></span><br/>  | <dl> <span data-ttu-id="e1cfa-124"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1cfa-124"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="e1cfa-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e1cfa-125">Library</span></span><br/> | <dl> <span data-ttu-id="e1cfa-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e1cfa-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e1cfa-127">См. также</span><span class="sxs-lookup"><span data-stu-id="e1cfa-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1cfa-128">Математические функции</span><span class="sxs-lookup"><span data-stu-id="e1cfa-128">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="e1cfa-129">**D3DXMatrixRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="e1cfa-129">**D3DXMatrixRotationAxis**</span></span>](d3dxmatrixrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="e1cfa-130">**D3DXMatrixRotationQuaternion**</span><span class="sxs-lookup"><span data-stu-id="e1cfa-130">**D3DXMatrixRotationQuaternion**</span></span>](d3dxmatrixrotationquaternion.md)
</dt> <dt>

[<span data-ttu-id="e1cfa-131">**D3DXMatrixRotationY**</span><span class="sxs-lookup"><span data-stu-id="e1cfa-131">**D3DXMatrixRotationY**</span></span>](d3dxmatrixrotationy.md)
</dt> <dt>

[<span data-ttu-id="e1cfa-132">**D3DXMatrixRotationYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="e1cfa-132">**D3DXMatrixRotationYawPitchRoll**</span></span>](d3dxmatrixrotationyawpitchroll.md)
</dt> <dt>

[<span data-ttu-id="e1cfa-133">**D3DXMatrixRotationZ**</span><span class="sxs-lookup"><span data-stu-id="e1cfa-133">**D3DXMatrixRotationZ**</span></span>](d3dxmatrixrotationz.md)
</dt> </dl>

 

 
