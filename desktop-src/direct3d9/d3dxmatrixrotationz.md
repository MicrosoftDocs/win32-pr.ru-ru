---
description: Функция D3DXMatrixRotationZ (D3dx9math. h) — строит матрицу, которая поворачивается вокруг оси z.
ms.assetid: 73db43e6-3831-4867-8eda-80127b61e169
title: Функция D3DXMatrixRotationZ (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixRotationZ
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0b109f71052657a5d9c32d9af5cb38b2cbcf1f0e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118112"
---
# <a name="d3dxmatrixrotationz-function-d3dx9mathh"></a><span data-ttu-id="9c2a3-103">Функция D3DXMatrixRotationZ (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="9c2a3-103">D3DXMatrixRotationZ function (D3dx9math.h)</span></span>

<span data-ttu-id="9c2a3-104">Строит матрицу, которая поворачивается вокруг оси z.</span><span class="sxs-lookup"><span data-stu-id="9c2a3-104">Builds a matrix that rotates around the z-axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c2a3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9c2a3-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationZ(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      Angle
);
```



## <a name="parameters"></a><span data-ttu-id="9c2a3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9c2a3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c2a3-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="9c2a3-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9c2a3-108">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="9c2a3-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="9c2a3-109">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="9c2a3-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="9c2a3-110">*Угол* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9c2a3-110">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c2a3-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9c2a3-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9c2a3-112">Угол поворота в радианах.</span><span class="sxs-lookup"><span data-stu-id="9c2a3-112">Angle of rotation, in radians.</span></span> <span data-ttu-id="9c2a3-113">Углы измеряются по часовой стрелке при просмотре из оси вращения (положительная сторона) в направлении к источнику.</span><span class="sxs-lookup"><span data-stu-id="9c2a3-113">Angles are measured clockwise when viewed from the rotation axis (positive side) toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c2a3-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9c2a3-114">Return value</span></span>

<span data-ttu-id="9c2a3-115">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="9c2a3-115">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="9c2a3-116">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , повернутую вокруг оси z.</span><span class="sxs-lookup"><span data-stu-id="9c2a3-116">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure rotated around the z-axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c2a3-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="9c2a3-117">Remarks</span></span>

<span data-ttu-id="9c2a3-118">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="9c2a3-118">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="9c2a3-119">Таким образом, функция **D3DXMatrixRotationZ** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="9c2a3-119">In this way, the **D3DXMatrixRotationZ** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c2a3-120">Требования</span><span class="sxs-lookup"><span data-stu-id="9c2a3-120">Requirements</span></span>



| <span data-ttu-id="9c2a3-121">Требование</span><span class="sxs-lookup"><span data-stu-id="9c2a3-121">Requirement</span></span> | <span data-ttu-id="9c2a3-122">Значение</span><span class="sxs-lookup"><span data-stu-id="9c2a3-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9c2a3-123">Header</span><span class="sxs-lookup"><span data-stu-id="9c2a3-123">Header</span></span><br/>  | <dl> <span data-ttu-id="9c2a3-124"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c2a3-124"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="9c2a3-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9c2a3-125">Library</span></span><br/> | <dl> <span data-ttu-id="9c2a3-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9c2a3-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9c2a3-127">См. также</span><span class="sxs-lookup"><span data-stu-id="9c2a3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c2a3-128">Математические функции</span><span class="sxs-lookup"><span data-stu-id="9c2a3-128">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="9c2a3-129">**D3DXMatrixRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="9c2a3-129">**D3DXMatrixRotationAxis**</span></span>](d3dxmatrixrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="9c2a3-130">**D3DXMatrixRotationQuaternion**</span><span class="sxs-lookup"><span data-stu-id="9c2a3-130">**D3DXMatrixRotationQuaternion**</span></span>](d3dxmatrixrotationquaternion.md)
</dt> <dt>

[<span data-ttu-id="9c2a3-131">**D3DXMatrixRotationX**</span><span class="sxs-lookup"><span data-stu-id="9c2a3-131">**D3DXMatrixRotationX**</span></span>](d3dxmatrixrotationx.md)
</dt> <dt>

[<span data-ttu-id="9c2a3-132">**D3DXMatrixRotationY**</span><span class="sxs-lookup"><span data-stu-id="9c2a3-132">**D3DXMatrixRotationY**</span></span>](d3dxmatrixrotationy.md)
</dt> <dt>

[<span data-ttu-id="9c2a3-133">**D3DXMatrixRotationYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="9c2a3-133">**D3DXMatrixRotationYawPitchRoll**</span></span>](d3dxmatrixrotationyawpitchroll.md)
</dt> </dl>

 

 
