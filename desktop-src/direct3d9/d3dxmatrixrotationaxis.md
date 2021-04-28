---
description: Функция D3DXMatrixRotationAxis (D3dx9math. h) — строит матрицу, которая поворачивается вокруг произвольной оси.
ms.assetid: 368c8f64-7709-4200-94d3-3dbc92a960c1
title: Функция D3DXMatrixRotationAxis (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixRotationAxis
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 720ac4d3bdae2910cee7913b9c34316d72526688
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118192"
---
# <a name="d3dxmatrixrotationaxis-function-d3dx9mathh"></a><span data-ttu-id="7b3c0-103">Функция D3DXMatrixRotationAxis (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="7b3c0-103">D3DXMatrixRotationAxis function (D3dx9math.h)</span></span>

<span data-ttu-id="7b3c0-104">Строит матрицу, которая поворачивается вокруг произвольной оси.</span><span class="sxs-lookup"><span data-stu-id="7b3c0-104">Builds a matrix that rotates around an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b3c0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7b3c0-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationAxis(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_          FLOAT       Angle
);
```



## <a name="parameters"></a><span data-ttu-id="7b3c0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7b3c0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b3c0-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="7b3c0-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7b3c0-108">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="7b3c0-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="7b3c0-109">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="7b3c0-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="7b3c0-110">*ПС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7b3c0-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b3c0-111">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="7b3c0-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="7b3c0-112">Указатель на произвольную ось.</span><span class="sxs-lookup"><span data-stu-id="7b3c0-112">Pointer to the arbitrary axis.</span></span> <span data-ttu-id="7b3c0-113">См. [**D3DXVECTOR3**](d3dxvector3.md).</span><span class="sxs-lookup"><span data-stu-id="7b3c0-113">See [**D3DXVECTOR3**](d3dxvector3.md).</span></span>

</dd> <dt>

<span data-ttu-id="7b3c0-114">*Угол* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7b3c0-114">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b3c0-115">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7b3c0-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7b3c0-116">Угол поворота в радианах.</span><span class="sxs-lookup"><span data-stu-id="7b3c0-116">Angle of rotation in radians.</span></span> <span data-ttu-id="7b3c0-117">Углы измеряются по часовой стрелке, если смотреть вдоль оси поворота в направлении начала координат.</span><span class="sxs-lookup"><span data-stu-id="7b3c0-117">Angles are measured clockwise when looking along the rotation axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b3c0-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7b3c0-118">Return value</span></span>

<span data-ttu-id="7b3c0-119">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="7b3c0-119">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="7b3c0-120">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , повернутую вокруг указанной оси.</span><span class="sxs-lookup"><span data-stu-id="7b3c0-120">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure rotated around the specified axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b3c0-121">Remarks</span><span class="sxs-lookup"><span data-stu-id="7b3c0-121">Remarks</span></span>

<span data-ttu-id="7b3c0-122">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="7b3c0-122">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="7b3c0-123">Таким образом, функция **D3DXMatrixRotationAxis** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="7b3c0-123">In this way, the **D3DXMatrixRotationAxis** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b3c0-124">Требования</span><span class="sxs-lookup"><span data-stu-id="7b3c0-124">Requirements</span></span>



| <span data-ttu-id="7b3c0-125">Требование</span><span class="sxs-lookup"><span data-stu-id="7b3c0-125">Requirement</span></span> | <span data-ttu-id="7b3c0-126">Значение</span><span class="sxs-lookup"><span data-stu-id="7b3c0-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7b3c0-127">Header</span><span class="sxs-lookup"><span data-stu-id="7b3c0-127">Header</span></span><br/>  | <dl> <span data-ttu-id="7b3c0-128"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b3c0-128"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="7b3c0-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7b3c0-129">Library</span></span><br/> | <dl> <span data-ttu-id="7b3c0-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7b3c0-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7b3c0-131">См. также</span><span class="sxs-lookup"><span data-stu-id="7b3c0-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b3c0-132">Математические функции</span><span class="sxs-lookup"><span data-stu-id="7b3c0-132">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="7b3c0-133">**D3DXMatrixRotationQuaternion**</span><span class="sxs-lookup"><span data-stu-id="7b3c0-133">**D3DXMatrixRotationQuaternion**</span></span>](d3dxmatrixrotationquaternion.md)
</dt> <dt>

[<span data-ttu-id="7b3c0-134">**D3DXMatrixRotationX**</span><span class="sxs-lookup"><span data-stu-id="7b3c0-134">**D3DXMatrixRotationX**</span></span>](d3dxmatrixrotationx.md)
</dt> <dt>

[<span data-ttu-id="7b3c0-135">**D3DXMatrixRotationY**</span><span class="sxs-lookup"><span data-stu-id="7b3c0-135">**D3DXMatrixRotationY**</span></span>](d3dxmatrixrotationy.md)
</dt> <dt>

[<span data-ttu-id="7b3c0-136">**D3DXMatrixRotationYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="7b3c0-136">**D3DXMatrixRotationYawPitchRoll**</span></span>](d3dxmatrixrotationyawpitchroll.md)
</dt> <dt>

[<span data-ttu-id="7b3c0-137">**D3DXMatrixRotationZ**</span><span class="sxs-lookup"><span data-stu-id="7b3c0-137">**D3DXMatrixRotationZ**</span></span>](d3dxmatrixrotationz.md)
</dt> </dl>

 

 
