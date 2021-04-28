---
description: Функция D3DXVec2TransformNormal (D3dx9math. h) — преобразует двумерный вектор, нормализованный заданной матрицей.
ms.assetid: aa9adf6d-5aae-4acf-bbd9-f5c14d90470e
title: Функция D3DXVec2TransformNormal (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2TransformNormal
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c8ed31300027fcb2e827988809cce1c50dbf77de
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097912"
---
# <a name="d3dxvec2transformnormal-function-d3dx9mathh"></a><span data-ttu-id="e5203-103">Функция D3DXVec2TransformNormal (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="e5203-103">D3DXVec2TransformNormal function (D3dx9math.h)</span></span>

<span data-ttu-id="e5203-104">Преобразует двумерный вектор, нормализованный заданной матрицей.</span><span class="sxs-lookup"><span data-stu-id="e5203-104">Transforms the 2D vector normal by the given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5203-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e5203-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2TransformNormal(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="e5203-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e5203-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5203-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="e5203-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e5203-108">Тип: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="e5203-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="e5203-109">Указатель на структуру [**D3DXVECTOR2**](d3dxvector2.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="e5203-109">Pointer to the [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="e5203-110">*ПС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e5203-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5203-111">Тип: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="e5203-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="e5203-112">Указатель на исходную структуру [**D3DXVECTOR2**](d3dxvector2.md) .</span><span class="sxs-lookup"><span data-stu-id="e5203-112">Pointer to the source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="e5203-113">*PM* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e5203-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5203-114">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="e5203-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e5203-115">Указатель на исходную структуру [**D3DXMATRIX**](d3dxmatrix.md) .</span><span class="sxs-lookup"><span data-stu-id="e5203-115">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5203-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e5203-116">Return value</span></span>

<span data-ttu-id="e5203-117">Тип: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="e5203-117">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="e5203-118">Указатель на структуру [**D3DXVECTOR2**](d3dxvector2.md) , которая является преобразованным вектором.</span><span class="sxs-lookup"><span data-stu-id="e5203-118">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5203-119">Remarks</span><span class="sxs-lookup"><span data-stu-id="e5203-119">Remarks</span></span>

<span data-ttu-id="e5203-120">Эта функция преобразует вектор (*PV-*>x, *pV-*>y, 0, 0) на матрицу, на которую указывает *PM*.</span><span class="sxs-lookup"><span data-stu-id="e5203-120">This function transforms the vector (*pV-*>x, *pV-*>y, 0, 0) by the matrix pointed to by *pM*.</span></span>

<span data-ttu-id="e5203-121">Если необходимо преобразовать обычное значение, то матрица, передаваемая в эту функцию, должна быть преобразована обратно в матрицу, которая будет использоваться для преобразования точки.</span><span class="sxs-lookup"><span data-stu-id="e5203-121">If you want to transform a normal, the matrix you pass to this function should be the transpose of the inverse of the matrix you would use to transform a point.</span></span>

<span data-ttu-id="e5203-122">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="e5203-122">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="e5203-123">Таким образом, функция **D3DXVec2TransformNormal** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="e5203-123">In this way, the **D3DXVec2TransformNormal** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5203-124">Требования</span><span class="sxs-lookup"><span data-stu-id="e5203-124">Requirements</span></span>



| <span data-ttu-id="e5203-125">Требование</span><span class="sxs-lookup"><span data-stu-id="e5203-125">Requirement</span></span> | <span data-ttu-id="e5203-126">Значение</span><span class="sxs-lookup"><span data-stu-id="e5203-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e5203-127">Header</span><span class="sxs-lookup"><span data-stu-id="e5203-127">Header</span></span><br/>  | <dl> <span data-ttu-id="e5203-128"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5203-128"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="e5203-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e5203-129">Library</span></span><br/> | <dl> <span data-ttu-id="e5203-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e5203-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e5203-131">См. также</span><span class="sxs-lookup"><span data-stu-id="e5203-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5203-132">Математические функции</span><span class="sxs-lookup"><span data-stu-id="e5203-132">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="e5203-133">**D3DXVec2Transform**</span><span class="sxs-lookup"><span data-stu-id="e5203-133">**D3DXVec2Transform**</span></span>](d3dxvec2transform.md)
</dt> <dt>

[<span data-ttu-id="e5203-134">**D3DXVec2TransformCoord**</span><span class="sxs-lookup"><span data-stu-id="e5203-134">**D3DXVec2TransformCoord**</span></span>](d3dxvec2transformcoord.md)
</dt> </dl>

 

 




