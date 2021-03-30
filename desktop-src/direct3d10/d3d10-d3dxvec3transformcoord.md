---
description: Преобразует трехмерный вектор в заданную матрицу с проецированием результата обратно в w = 1.
ms.assetid: e138fdc0-6999-45ab-8bcf-54f53bd9b1bf
title: Функция D3DXVec3TransformCoord (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformCoord
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: a8fc7c7a00133e036921eabaa145dca01a12f042
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354970"
---
# <a name="d3dxvec3transformcoord-function-d3dx10mathh"></a><span data-ttu-id="896fa-103">Функция D3DXVec3TransformCoord (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="896fa-103">D3DXVec3TransformCoord function (D3DX10Math.h)</span></span>

<span data-ttu-id="896fa-104">Преобразует трехмерный вектор в заданную матрицу с проецированием результата обратно в w = 1.</span><span class="sxs-lookup"><span data-stu-id="896fa-104">Transforms a 3D vector by a given matrix, projecting the result back into w = 1.</span></span>

## <a name="syntax"></a><span data-ttu-id="896fa-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="896fa-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3TransformCoord(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="896fa-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="896fa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="896fa-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="896fa-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="896fa-108">Тип: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="896fa-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="896fa-109">Указатель на [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , который является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="896fa-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="896fa-110">*ПС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="896fa-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="896fa-111">Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="896fa-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="896fa-112">Указатель на исходную структуру D3DXVECTOR3.</span><span class="sxs-lookup"><span data-stu-id="896fa-112">Pointer to the source D3DXVECTOR3 structure.</span></span>

</dd> <dt>

<span data-ttu-id="896fa-113">*PM* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="896fa-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="896fa-114">Тип: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="896fa-114">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="896fa-115">Указатель на исходную структуру [**D3DXMATRIX**](d3d10-d3dxmatrix.md) .</span><span class="sxs-lookup"><span data-stu-id="896fa-115">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="896fa-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="896fa-116">Return value</span></span>

<span data-ttu-id="896fa-117">Тип: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="896fa-117">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="896fa-118">Указатель на структуру D3DXVECTOR3, которая является преобразованным вектором.</span><span class="sxs-lookup"><span data-stu-id="896fa-118">Pointer to a D3DXVECTOR3 structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="896fa-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="896fa-119">Remarks</span></span>

<span data-ttu-id="896fa-120">Эта функция преобразует вектор, НЗ (x, y, z, 1) матрицу, выполнив проецирование результата обратно в w = 1.</span><span class="sxs-lookup"><span data-stu-id="896fa-120">This function transforms the vector, pV (x, y, z, 1), by the matrix, pM, projecting the result back into w=1.</span></span>

<span data-ttu-id="896fa-121">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="896fa-121">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="896fa-122">Таким образом, функция D3DXVec3TransformCoord может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="896fa-122">In this way, the D3DXVec3TransformCoord function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="896fa-123">Требования</span><span class="sxs-lookup"><span data-stu-id="896fa-123">Requirements</span></span>



| <span data-ttu-id="896fa-124">Требование</span><span class="sxs-lookup"><span data-stu-id="896fa-124">Requirement</span></span> | <span data-ttu-id="896fa-125">Значение</span><span class="sxs-lookup"><span data-stu-id="896fa-125">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="896fa-126">Header</span><span class="sxs-lookup"><span data-stu-id="896fa-126">Header</span></span><br/> | <dl> <span data-ttu-id="896fa-127"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="896fa-127"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="896fa-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="896fa-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="896fa-129">Математические функции</span><span class="sxs-lookup"><span data-stu-id="896fa-129">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
