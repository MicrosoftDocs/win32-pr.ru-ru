---
description: Функция D3DXVec2Transform (D3DX10Math. h) — преобразует 2D-вектор по заданной матрице.
ms.assetid: 4b57eb7f-fae9-48ac-a806-510da75d25a6
title: Функция D3DXVec2Transform (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Transform
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: b1d8eed447b56e6f379ffe96cbbcb4820fbdaf14
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108362"
---
# <a name="d3dxvec2transform-function-d3dx10mathh"></a><span data-ttu-id="10c08-103">Функция D3DXVec2Transform (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="10c08-103">D3DXVec2Transform function (D3DX10Math.h)</span></span>

<span data-ttu-id="10c08-104">Преобразует двумерный вектор по заданной матрице.</span><span class="sxs-lookup"><span data-stu-id="10c08-104">Transforms a 2D vector by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="10c08-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="10c08-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec2Transform(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR2 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="10c08-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="10c08-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10c08-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="10c08-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="10c08-108">Тип: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="10c08-108">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="10c08-109">Указатель на структуру [**D3DXVECTOR4**](d3d10-d3dxvector4.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="10c08-109">Pointer to the [**D3DXVECTOR4**](d3d10-d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="10c08-110">*ПС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="10c08-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10c08-111">Тип: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="10c08-111">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="10c08-112">Указатель на источник [**D3DXVECTOR2**](d3d10-d3dxvector2.md).</span><span class="sxs-lookup"><span data-stu-id="10c08-112">Pointer to the source [**D3DXVECTOR2**](d3d10-d3dxvector2.md).</span></span>

</dd> <dt>

<span data-ttu-id="10c08-113">*PM* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="10c08-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10c08-114">Тип: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="10c08-114">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="10c08-115">Указатель на исходную структуру [**D3DXMATRIX**](d3d10-d3dxmatrix.md) .</span><span class="sxs-lookup"><span data-stu-id="10c08-115">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10c08-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="10c08-116">Return value</span></span>

<span data-ttu-id="10c08-117">Тип: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="10c08-117">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="10c08-118">Указатель на структуру D3DXVECTOR4, которая является преобразованным вектором.</span><span class="sxs-lookup"><span data-stu-id="10c08-118">Pointer to a D3DXVECTOR4 structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="10c08-119">Remarks</span><span class="sxs-lookup"><span data-stu-id="10c08-119">Remarks</span></span>

<span data-ttu-id="10c08-120">Эта функция преобразует вектор ПС (x, y, 0, 1) на матрицу pM.</span><span class="sxs-lookup"><span data-stu-id="10c08-120">This function transforms the vector pV (x, y, 0, 1) by the matrix pM.</span></span>

<span data-ttu-id="10c08-121">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="10c08-121">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="10c08-122">Таким образом, функция D3DXVec2Transform может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="10c08-122">In this way, the D3DXVec2Transform function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="10c08-123">Требования</span><span class="sxs-lookup"><span data-stu-id="10c08-123">Requirements</span></span>



| <span data-ttu-id="10c08-124">Требование</span><span class="sxs-lookup"><span data-stu-id="10c08-124">Requirement</span></span> | <span data-ttu-id="10c08-125">Значение</span><span class="sxs-lookup"><span data-stu-id="10c08-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="10c08-126">Header</span><span class="sxs-lookup"><span data-stu-id="10c08-126">Header</span></span><br/>  | <dl> <span data-ttu-id="10c08-127"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="10c08-127"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="10c08-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="10c08-128">Library</span></span><br/> | <dl> <span data-ttu-id="10c08-129"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="10c08-129"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="10c08-130">См. также</span><span class="sxs-lookup"><span data-stu-id="10c08-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10c08-131">Математические функции</span><span class="sxs-lookup"><span data-stu-id="10c08-131">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
