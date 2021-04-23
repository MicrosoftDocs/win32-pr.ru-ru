---
description: Строит матрицу, которая поворачивается вокруг оси x.
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
ms.openlocfilehash: 5eade695a3b410877665557bd42d61d1d89b18e2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694266"
---
# <a name="d3dxmatrixrotationx-function-d3dx10mathh"></a><span data-ttu-id="9e910-103">Функция D3DXMatrixRotationX (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="9e910-103">D3DXMatrixRotationX function (D3DX10Math.h)</span></span>

<span data-ttu-id="9e910-104">Строит матрицу, которая поворачивается вокруг оси x.</span><span class="sxs-lookup"><span data-stu-id="9e910-104">Builds a matrix that rotates around the x-axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e910-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9e910-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationX(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      Angle
);
```



## <a name="parameters"></a><span data-ttu-id="9e910-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9e910-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e910-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="9e910-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9e910-108">Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="9e910-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="9e910-109">Указатель на структуру [**D3DXMATRIX**](d3d10-d3dxmatrix.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="9e910-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="9e910-110">*Угол* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9e910-110">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e910-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9e910-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9e910-112">Угол поворота в радианах.</span><span class="sxs-lookup"><span data-stu-id="9e910-112">Angle of rotation in radians.</span></span> <span data-ttu-id="9e910-113">Углы измеряются по часовой стрелке, если смотреть вдоль оси поворота в направлении начала координат.</span><span class="sxs-lookup"><span data-stu-id="9e910-113">Angles are measured clockwise when looking along the rotation axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e910-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9e910-114">Return value</span></span>

<span data-ttu-id="9e910-115">Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="9e910-115">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="9e910-116">Указатель на структуру D3DXMATRIX, повернутую вокруг оси x.</span><span class="sxs-lookup"><span data-stu-id="9e910-116">Pointer to a D3DXMATRIX structure rotated around the x-axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e910-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9e910-117">Remarks</span></span>

<span data-ttu-id="9e910-118">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="9e910-118">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="9e910-119">Таким образом, функция D3DXMatrixRotationX может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="9e910-119">In this way, the D3DXMatrixRotationX function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e910-120">Требования</span><span class="sxs-lookup"><span data-stu-id="9e910-120">Requirements</span></span>



| <span data-ttu-id="9e910-121">Требование</span><span class="sxs-lookup"><span data-stu-id="9e910-121">Requirement</span></span> | <span data-ttu-id="9e910-122">Значение</span><span class="sxs-lookup"><span data-stu-id="9e910-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9e910-123">Header</span><span class="sxs-lookup"><span data-stu-id="9e910-123">Header</span></span><br/>  | <dl> <span data-ttu-id="9e910-124"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e910-124"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="9e910-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9e910-125">Library</span></span><br/> | <dl> <span data-ttu-id="9e910-126"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9e910-126"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9e910-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9e910-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e910-128">Математические функции</span><span class="sxs-lookup"><span data-stu-id="9e910-128">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
