---
description: Функция D3DXVec2TransformCoord (D3DX10Math. h) — преобразует двумерный вектор по заданной матрице с проецированием результата обратно в w = 1.
ms.assetid: bb24204f-0c8e-4dc5-bcae-12e3033d1a39
title: Функция D3DXVec2TransformCoord (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2TransformCoord
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 95321d377ad5af29075764e2c2d9386abf5b1441
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108342"
---
# <a name="d3dxvec2transformcoord-function-d3dx10mathh"></a><span data-ttu-id="beb33-103">Функция D3DXVec2TransformCoord (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="beb33-103">D3DXVec2TransformCoord function (D3DX10Math.h)</span></span>

<span data-ttu-id="beb33-104">Преобразует двумерный вектор по заданной матрице, проецирование результата обратно в w = 1.</span><span class="sxs-lookup"><span data-stu-id="beb33-104">Transforms a 2D vector by a given matrix, projecting the result back into w = 1.</span></span>

## <a name="syntax"></a><span data-ttu-id="beb33-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="beb33-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2TransformCoord(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="beb33-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="beb33-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="beb33-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="beb33-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="beb33-108">Тип: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="beb33-108">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="beb33-109">Указатель на [**D3DXVECTOR2**](d3d10-d3dxvector2.md) , который является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="beb33-109">Pointer to the [**D3DXVECTOR2**](d3d10-d3dxvector2.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="beb33-110">*ПС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="beb33-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="beb33-111">Тип: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="beb33-111">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="beb33-112">Указатель на исходную структуру D3DXVECTOR2.</span><span class="sxs-lookup"><span data-stu-id="beb33-112">Pointer to the source D3DXVECTOR2 structure.</span></span>

</dd> <dt>

<span data-ttu-id="beb33-113">*PM* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="beb33-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="beb33-114">Тип: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="beb33-114">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="beb33-115">Указатель на исходную структуру [**D3DXMATRIX**](d3d10-d3dxmatrix.md) .</span><span class="sxs-lookup"><span data-stu-id="beb33-115">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="beb33-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="beb33-116">Return value</span></span>

<span data-ttu-id="beb33-117">Тип: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="beb33-117">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="beb33-118">Указатель на структуру D3DXVECTOR2, которая является преобразованным вектором.</span><span class="sxs-lookup"><span data-stu-id="beb33-118">Pointer to a D3DXVECTOR2 structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="beb33-119">Remarks</span><span class="sxs-lookup"><span data-stu-id="beb33-119">Remarks</span></span>

<span data-ttu-id="beb33-120">Эта функция преобразует вектор, НЗ (x, y, 0, 1), по матрице, в проекцию результата обратно в w = 1.</span><span class="sxs-lookup"><span data-stu-id="beb33-120">This function transforms the vector, pV (x, y, 0, 1), by the matrix, pM, projecting the result back into w=1.</span></span>

<span data-ttu-id="beb33-121">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="beb33-121">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="beb33-122">Таким образом, функция D3DXVec2TransformCoord может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="beb33-122">In this way, the D3DXVec2TransformCoord function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="beb33-123">Требования</span><span class="sxs-lookup"><span data-stu-id="beb33-123">Requirements</span></span>



| <span data-ttu-id="beb33-124">Требование</span><span class="sxs-lookup"><span data-stu-id="beb33-124">Requirement</span></span> | <span data-ttu-id="beb33-125">Значение</span><span class="sxs-lookup"><span data-stu-id="beb33-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="beb33-126">Header</span><span class="sxs-lookup"><span data-stu-id="beb33-126">Header</span></span><br/>  | <dl> <span data-ttu-id="beb33-127"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="beb33-127"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="beb33-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="beb33-128">Library</span></span><br/> | <dl> <span data-ttu-id="beb33-129"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="beb33-129"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="beb33-130">См. также</span><span class="sxs-lookup"><span data-stu-id="beb33-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="beb33-131">Математические функции</span><span class="sxs-lookup"><span data-stu-id="beb33-131">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
