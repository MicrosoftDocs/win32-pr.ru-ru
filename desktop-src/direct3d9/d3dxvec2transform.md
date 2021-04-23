---
description: Преобразует двумерный вектор по заданной матрице.
ms.assetid: ccde9e34-2d99-4112-a8ed-3820d018b547
title: Функция D3DXVec2Transform (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 71dd9c0fee853afe0aee3a514308142241655835
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273755"
---
# <a name="d3dxvec2transform-function-d3dx9mathh"></a><span data-ttu-id="5ca13-103">Функция D3DXVec2Transform (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="5ca13-103">D3DXVec2Transform function (D3dx9math.h)</span></span>

<span data-ttu-id="5ca13-104">Преобразует двумерный вектор по заданной матрице.</span><span class="sxs-lookup"><span data-stu-id="5ca13-104">Transforms a 2D vector by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ca13-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5ca13-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec2Transform(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR2 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="5ca13-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5ca13-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ca13-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="5ca13-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5ca13-108">Тип: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="5ca13-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="5ca13-109">Указатель на структуру [**D3DXVECTOR4**](d3dxvector4.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="5ca13-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="5ca13-110">*ПС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5ca13-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ca13-111">Тип: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="5ca13-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="5ca13-112">Указатель на исходную структуру [**D3DXVECTOR2**](d3dxvector2.md) .</span><span class="sxs-lookup"><span data-stu-id="5ca13-112">Pointer to the source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="5ca13-113">*PM* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5ca13-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ca13-114">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="5ca13-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="5ca13-115">Указатель на исходную структуру [**D3DXMATRIX**](d3dxmatrix.md) .</span><span class="sxs-lookup"><span data-stu-id="5ca13-115">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ca13-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5ca13-116">Return value</span></span>

<span data-ttu-id="5ca13-117">Тип: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="5ca13-117">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="5ca13-118">Указатель на структуру [**D3DXVECTOR4**](d3dxvector4.md) , которая является преобразованным вектором.</span><span class="sxs-lookup"><span data-stu-id="5ca13-118">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ca13-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5ca13-119">Remarks</span></span>

<span data-ttu-id="5ca13-120">Эта функция преобразует вектор *ПС* (x, y, 0, 1) на матрицу *PM*.</span><span class="sxs-lookup"><span data-stu-id="5ca13-120">This function transforms the vector *pV* (x, y, 0, 1) by the matrix *pM*.</span></span>

<span data-ttu-id="5ca13-121">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="5ca13-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="5ca13-122">Таким образом, функция **D3DXVec2Transform** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="5ca13-122">In this way, the **D3DXVec2Transform** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ca13-123">Требования</span><span class="sxs-lookup"><span data-stu-id="5ca13-123">Requirements</span></span>



| <span data-ttu-id="5ca13-124">Требование</span><span class="sxs-lookup"><span data-stu-id="5ca13-124">Requirement</span></span> | <span data-ttu-id="5ca13-125">Значение</span><span class="sxs-lookup"><span data-stu-id="5ca13-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ca13-126">Header</span><span class="sxs-lookup"><span data-stu-id="5ca13-126">Header</span></span><br/>  | <dl> <span data-ttu-id="5ca13-127"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ca13-127"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="5ca13-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5ca13-128">Library</span></span><br/> | <dl> <span data-ttu-id="5ca13-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5ca13-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5ca13-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5ca13-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ca13-131">Математические функции</span><span class="sxs-lookup"><span data-stu-id="5ca13-131">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="5ca13-132">**D3DXVec2TransformCoord**</span><span class="sxs-lookup"><span data-stu-id="5ca13-132">**D3DXVec2TransformCoord**</span></span>](d3dxvec2transformcoord.md)
</dt> <dt>

[<span data-ttu-id="5ca13-133">**D3DXVec2TransformNormal**</span><span class="sxs-lookup"><span data-stu-id="5ca13-133">**D3DXVec2TransformNormal**</span></span>](d3dxvec2transformnormal.md)
</dt> </dl>

 

 




