---
description: Строит матрицу, которая поворачивается вокруг произвольной оси.
ms.assetid: dc4b8b3f-e1d2-475f-9dcb-622ada9fae6b
title: Функция D3DXMatrixRotationAxis (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: bba74aa7258b39b8fdbbb8cab09684a14bfbda91
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104081924"
---
# <a name="d3dxmatrixrotationaxis-function-d3dx10mathh"></a><span data-ttu-id="1601b-103">Функция D3DXMatrixRotationAxis (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="1601b-103">D3DXMatrixRotationAxis function (D3DX10Math.h)</span></span>

<span data-ttu-id="1601b-104">Строит матрицу, которая поворачивается вокруг произвольной оси.</span><span class="sxs-lookup"><span data-stu-id="1601b-104">Builds a matrix that rotates around an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="1601b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1601b-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationAxis(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_          FLOAT       Angle
);
```



## <a name="parameters"></a><span data-ttu-id="1601b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1601b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1601b-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="1601b-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1601b-108">Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="1601b-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1601b-109">Указатель на структуру [**D3DXMATRIX**](d3d10-d3dxmatrix.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="1601b-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="1601b-110">*ПС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1601b-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1601b-111">Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="1601b-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="1601b-112">Указатель на произвольную ось.</span><span class="sxs-lookup"><span data-stu-id="1601b-112">Pointer to the arbitrary axis.</span></span> <span data-ttu-id="1601b-113">См. [**D3DXVECTOR3**](d3d10-d3dxvector3.md).</span><span class="sxs-lookup"><span data-stu-id="1601b-113">See [**D3DXVECTOR3**](d3d10-d3dxvector3.md).</span></span>

</dd> <dt>

<span data-ttu-id="1601b-114">*Угол* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1601b-114">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1601b-115">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1601b-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1601b-116">Угол поворота в радианах.</span><span class="sxs-lookup"><span data-stu-id="1601b-116">Angle of rotation in radians.</span></span> <span data-ttu-id="1601b-117">Углы измеряются по часовой стрелке, если смотреть вдоль оси поворота в направлении начала координат.</span><span class="sxs-lookup"><span data-stu-id="1601b-117">Angles are measured clockwise when looking along the rotation axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1601b-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1601b-118">Return value</span></span>

<span data-ttu-id="1601b-119">Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="1601b-119">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1601b-120">Указатель на структуру D3DXMATRIX, повернутую вокруг указанной оси.</span><span class="sxs-lookup"><span data-stu-id="1601b-120">Pointer to a D3DXMATRIX structure rotated around the specified axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="1601b-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1601b-121">Remarks</span></span>

<span data-ttu-id="1601b-122">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="1601b-122">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="1601b-123">Таким образом, функция D3DXMatrixRotationAxis может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="1601b-123">In this way, the D3DXMatrixRotationAxis function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="1601b-124">Требования</span><span class="sxs-lookup"><span data-stu-id="1601b-124">Requirements</span></span>



| <span data-ttu-id="1601b-125">Требование</span><span class="sxs-lookup"><span data-stu-id="1601b-125">Requirement</span></span> | <span data-ttu-id="1601b-126">Значение</span><span class="sxs-lookup"><span data-stu-id="1601b-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1601b-127">Header</span><span class="sxs-lookup"><span data-stu-id="1601b-127">Header</span></span><br/>  | <dl> <span data-ttu-id="1601b-128"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="1601b-128"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="1601b-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1601b-129">Library</span></span><br/> | <dl> <span data-ttu-id="1601b-130"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1601b-130"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1601b-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1601b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1601b-132">Математические функции</span><span class="sxs-lookup"><span data-stu-id="1601b-132">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
