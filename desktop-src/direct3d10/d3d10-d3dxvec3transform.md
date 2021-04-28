---
description: Функция D3DXVec3Transform (D3DX10Math. h) — преобразует вектор (x, y, z, 1) в заданную матрицу.
ms.assetid: 88b26d94-2550-4126-bf91-b06391ec5c75
title: Функция D3DXVec3Transform (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Transform
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 9b5cd69ce603f56e4837818cac6ee18fe3ab1e53
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108142"
---
# <a name="d3dxvec3transform-function-d3dx10mathh"></a><span data-ttu-id="e6585-103">Функция D3DXVec3Transform (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="e6585-103">D3DXVec3Transform function (D3DX10Math.h)</span></span>

<span data-ttu-id="e6585-104">Преобразует вектор (x, y, z, 1) в заданную матрицу.</span><span class="sxs-lookup"><span data-stu-id="e6585-104">Transforms vector (x, y, z, 1) by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6585-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e6585-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec3Transform(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="e6585-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e6585-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6585-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="e6585-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e6585-108">Тип: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="e6585-108">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="e6585-109">Указатель на структуру [**D3DXVECTOR4**](d3d10-d3dxvector4.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="e6585-109">Pointer to the [**D3DXVECTOR4**](d3d10-d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="e6585-110">*ПС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e6585-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6585-111">Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="e6585-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="e6585-112">Указатель на источник [**D3DXVECTOR3**](d3d10-d3dxvector3.md).</span><span class="sxs-lookup"><span data-stu-id="e6585-112">Pointer to the source [**D3DXVECTOR3**](d3d10-d3dxvector3.md).</span></span>

</dd> <dt>

<span data-ttu-id="e6585-113">*PM* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e6585-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6585-114">Тип: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="e6585-114">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e6585-115">Указатель на исходную структуру [**D3DXMATRIX**](d3d10-d3dxmatrix.md) .</span><span class="sxs-lookup"><span data-stu-id="e6585-115">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6585-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e6585-116">Return value</span></span>

<span data-ttu-id="e6585-117">Тип: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="e6585-117">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="e6585-118">Указатель на структуру D3DXVECTOR4, которая является преобразованным вектором.</span><span class="sxs-lookup"><span data-stu-id="e6585-118">Pointer to a D3DXVECTOR4 structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6585-119">Remarks</span><span class="sxs-lookup"><span data-stu-id="e6585-119">Remarks</span></span>

<span data-ttu-id="e6585-120">Эта функция преобразует вектор, НЗ (x, y, z, 1) в матрицу pM.</span><span class="sxs-lookup"><span data-stu-id="e6585-120">This function transforms the vector, pV (x, y, z, 1), by the matrix pM.</span></span>

<span data-ttu-id="e6585-121">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="e6585-121">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="e6585-122">Таким образом, функция D3DXVec3Transform может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="e6585-122">In this way, the D3DXVec3Transform function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6585-123">Требования</span><span class="sxs-lookup"><span data-stu-id="e6585-123">Requirements</span></span>



| <span data-ttu-id="e6585-124">Требование</span><span class="sxs-lookup"><span data-stu-id="e6585-124">Requirement</span></span> | <span data-ttu-id="e6585-125">Значение</span><span class="sxs-lookup"><span data-stu-id="e6585-125">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e6585-126">Header</span><span class="sxs-lookup"><span data-stu-id="e6585-126">Header</span></span><br/> | <dl> <span data-ttu-id="e6585-127"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6585-127"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6585-128">См. также</span><span class="sxs-lookup"><span data-stu-id="e6585-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6585-129">Математические функции</span><span class="sxs-lookup"><span data-stu-id="e6585-129">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
