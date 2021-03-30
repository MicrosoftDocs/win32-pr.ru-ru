---
description: Строит матрицу, которая поворачивается вокруг оси y.
ms.assetid: 80449e5d-f9bb-48c0-a787-a5e5a9d1c9a3
title: Функция D3DXMatrixRotationY (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixRotationY
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 81e233f3d643e99c829c7d567721e52b9b5d3e82
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355410"
---
# <a name="d3dxmatrixrotationy-function-d3dx9mathh"></a><span data-ttu-id="67d6c-103">Функция D3DXMatrixRotationY (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="67d6c-103">D3DXMatrixRotationY function (D3dx9math.h)</span></span>

<span data-ttu-id="67d6c-104">Строит матрицу, которая поворачивается вокруг оси y.</span><span class="sxs-lookup"><span data-stu-id="67d6c-104">Builds a matrix that rotates around the y-axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="67d6c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="67d6c-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationY(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      Angle
);
```



## <a name="parameters"></a><span data-ttu-id="67d6c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="67d6c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67d6c-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="67d6c-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="67d6c-108">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="67d6c-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="67d6c-109">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="67d6c-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="67d6c-110">*Угол* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="67d6c-110">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67d6c-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="67d6c-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="67d6c-112">Угол поворота в радианах.</span><span class="sxs-lookup"><span data-stu-id="67d6c-112">Angle of rotation in radians.</span></span> <span data-ttu-id="67d6c-113">Углы измеряются по часовой стрелке, если смотреть вдоль оси поворота в направлении начала координат.</span><span class="sxs-lookup"><span data-stu-id="67d6c-113">Angles are measured clockwise when looking along the rotation axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67d6c-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="67d6c-114">Return value</span></span>

<span data-ttu-id="67d6c-115">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="67d6c-115">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="67d6c-116">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , повернутую вокруг оси y.</span><span class="sxs-lookup"><span data-stu-id="67d6c-116">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure rotated around the y-axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="67d6c-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="67d6c-117">Remarks</span></span>

<span data-ttu-id="67d6c-118">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="67d6c-118">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="67d6c-119">Таким образом, функция **D3DXMatrixRotationY** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="67d6c-119">In this way, the **D3DXMatrixRotationY** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="67d6c-120">Требования</span><span class="sxs-lookup"><span data-stu-id="67d6c-120">Requirements</span></span>



| <span data-ttu-id="67d6c-121">Требование</span><span class="sxs-lookup"><span data-stu-id="67d6c-121">Requirement</span></span> | <span data-ttu-id="67d6c-122">Значение</span><span class="sxs-lookup"><span data-stu-id="67d6c-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="67d6c-123">Header</span><span class="sxs-lookup"><span data-stu-id="67d6c-123">Header</span></span><br/>  | <dl> <span data-ttu-id="67d6c-124"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="67d6c-124"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="67d6c-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="67d6c-125">Library</span></span><br/> | <dl> <span data-ttu-id="67d6c-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="67d6c-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="67d6c-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="67d6c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67d6c-128">Математические функции</span><span class="sxs-lookup"><span data-stu-id="67d6c-128">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="67d6c-129">**D3DXMatrixRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="67d6c-129">**D3DXMatrixRotationAxis**</span></span>](d3dxmatrixrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="67d6c-130">**D3DXMatrixRotationQuaternion**</span><span class="sxs-lookup"><span data-stu-id="67d6c-130">**D3DXMatrixRotationQuaternion**</span></span>](d3dxmatrixrotationquaternion.md)
</dt> <dt>

[<span data-ttu-id="67d6c-131">**D3DXMatrixRotationX**</span><span class="sxs-lookup"><span data-stu-id="67d6c-131">**D3DXMatrixRotationX**</span></span>](d3dxmatrixrotationx.md)
</dt> <dt>

[<span data-ttu-id="67d6c-132">**D3DXMatrixRotationYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="67d6c-132">**D3DXMatrixRotationYawPitchRoll**</span></span>](d3dxmatrixrotationyawpitchroll.md)
</dt> <dt>

[<span data-ttu-id="67d6c-133">**D3DXMatrixRotationZ**</span><span class="sxs-lookup"><span data-stu-id="67d6c-133">**D3DXMatrixRotationZ**</span></span>](d3dxmatrixrotationz.md)
</dt> </dl>

 

 
