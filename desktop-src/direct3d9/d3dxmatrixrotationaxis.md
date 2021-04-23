---
description: Строит матрицу, которая поворачивается вокруг произвольной оси.
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
ms.openlocfilehash: fffc4a5bdd287c79352beb3ee0eeaf97b0573753
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703641"
---
# <a name="d3dxmatrixrotationaxis-function-d3dx9mathh"></a><span data-ttu-id="feb73-103">Функция D3DXMatrixRotationAxis (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="feb73-103">D3DXMatrixRotationAxis function (D3dx9math.h)</span></span>

<span data-ttu-id="feb73-104">Строит матрицу, которая поворачивается вокруг произвольной оси.</span><span class="sxs-lookup"><span data-stu-id="feb73-104">Builds a matrix that rotates around an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="feb73-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="feb73-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationAxis(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_          FLOAT       Angle
);
```



## <a name="parameters"></a><span data-ttu-id="feb73-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="feb73-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="feb73-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="feb73-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="feb73-108">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="feb73-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="feb73-109">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="feb73-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="feb73-110">*ПС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="feb73-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="feb73-111">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="feb73-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="feb73-112">Указатель на произвольную ось.</span><span class="sxs-lookup"><span data-stu-id="feb73-112">Pointer to the arbitrary axis.</span></span> <span data-ttu-id="feb73-113">См. [**D3DXVECTOR3**](d3dxvector3.md).</span><span class="sxs-lookup"><span data-stu-id="feb73-113">See [**D3DXVECTOR3**](d3dxvector3.md).</span></span>

</dd> <dt>

<span data-ttu-id="feb73-114">*Угол* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="feb73-114">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="feb73-115">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="feb73-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="feb73-116">Угол поворота в радианах.</span><span class="sxs-lookup"><span data-stu-id="feb73-116">Angle of rotation in radians.</span></span> <span data-ttu-id="feb73-117">Углы измеряются по часовой стрелке, если смотреть вдоль оси поворота в направлении начала координат.</span><span class="sxs-lookup"><span data-stu-id="feb73-117">Angles are measured clockwise when looking along the rotation axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="feb73-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="feb73-118">Return value</span></span>

<span data-ttu-id="feb73-119">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="feb73-119">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="feb73-120">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , повернутую вокруг указанной оси.</span><span class="sxs-lookup"><span data-stu-id="feb73-120">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure rotated around the specified axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="feb73-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="feb73-121">Remarks</span></span>

<span data-ttu-id="feb73-122">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="feb73-122">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="feb73-123">Таким образом, функция **D3DXMatrixRotationAxis** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="feb73-123">In this way, the **D3DXMatrixRotationAxis** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="feb73-124">Требования</span><span class="sxs-lookup"><span data-stu-id="feb73-124">Requirements</span></span>



| <span data-ttu-id="feb73-125">Требование</span><span class="sxs-lookup"><span data-stu-id="feb73-125">Requirement</span></span> | <span data-ttu-id="feb73-126">Значение</span><span class="sxs-lookup"><span data-stu-id="feb73-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="feb73-127">Header</span><span class="sxs-lookup"><span data-stu-id="feb73-127">Header</span></span><br/>  | <dl> <span data-ttu-id="feb73-128"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="feb73-128"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="feb73-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="feb73-129">Library</span></span><br/> | <dl> <span data-ttu-id="feb73-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="feb73-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="feb73-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="feb73-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="feb73-132">Математические функции</span><span class="sxs-lookup"><span data-stu-id="feb73-132">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="feb73-133">**D3DXMatrixRotationQuaternion**</span><span class="sxs-lookup"><span data-stu-id="feb73-133">**D3DXMatrixRotationQuaternion**</span></span>](d3dxmatrixrotationquaternion.md)
</dt> <dt>

[<span data-ttu-id="feb73-134">**D3DXMatrixRotationX**</span><span class="sxs-lookup"><span data-stu-id="feb73-134">**D3DXMatrixRotationX**</span></span>](d3dxmatrixrotationx.md)
</dt> <dt>

[<span data-ttu-id="feb73-135">**D3DXMatrixRotationY**</span><span class="sxs-lookup"><span data-stu-id="feb73-135">**D3DXMatrixRotationY**</span></span>](d3dxmatrixrotationy.md)
</dt> <dt>

[<span data-ttu-id="feb73-136">**D3DXMatrixRotationYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="feb73-136">**D3DXMatrixRotationYawPitchRoll**</span></span>](d3dxmatrixrotationyawpitchroll.md)
</dt> <dt>

[<span data-ttu-id="feb73-137">**D3DXMatrixRotationZ**</span><span class="sxs-lookup"><span data-stu-id="feb73-137">**D3DXMatrixRotationZ**</span></span>](d3dxmatrixrotationz.md)
</dt> </dl>

 

 
