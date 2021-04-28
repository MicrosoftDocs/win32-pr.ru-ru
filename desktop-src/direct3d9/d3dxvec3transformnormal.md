---
description: Функция D3DXVec3TransformNormal (D3dx9math. h) — Преобразует трехмерный вектор в нормальный по заданной матрице.
ms.assetid: aa9531e1-b77a-4aad-8d59-2677908cb978
title: Функция D3DXVec3TransformNormal (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformNormal
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 50fb09a4619be9c3dbcff98bc939d6f99ad33bd4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115622"
---
# <a name="d3dxvec3transformnormal-function-d3dx9mathh"></a><span data-ttu-id="4a6d6-103">Функция D3DXVec3TransformNormal (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="4a6d6-103">D3DXVec3TransformNormal function (D3dx9math.h)</span></span>

<span data-ttu-id="4a6d6-104">Преобразует трехмерный вектор в нормальный по заданной матрице.</span><span class="sxs-lookup"><span data-stu-id="4a6d6-104">Transforms the 3D vector normal by the given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a6d6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4a6d6-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3TransformNormal(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="4a6d6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4a6d6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a6d6-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="4a6d6-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4a6d6-108">Тип: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="4a6d6-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="4a6d6-109">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="4a6d6-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="4a6d6-110">*ПС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4a6d6-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a6d6-111">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="4a6d6-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="4a6d6-112">Указатель на исходную структуру [**D3DXVECTOR3**](d3dxvector3.md) .</span><span class="sxs-lookup"><span data-stu-id="4a6d6-112">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="4a6d6-113">*PM* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4a6d6-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a6d6-114">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="4a6d6-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="4a6d6-115">Указатель на исходную структуру [**D3DXMATRIX**](d3dxmatrix.md) .</span><span class="sxs-lookup"><span data-stu-id="4a6d6-115">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a6d6-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4a6d6-116">Return value</span></span>

<span data-ttu-id="4a6d6-117">Тип: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="4a6d6-117">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="4a6d6-118">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , которая является преобразованным вектором.</span><span class="sxs-lookup"><span data-stu-id="4a6d6-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a6d6-119">Remarks</span><span class="sxs-lookup"><span data-stu-id="4a6d6-119">Remarks</span></span>

<span data-ttu-id="4a6d6-120">Эта функция преобразует вектор (*ПС*->x, *PV*->y, *PV*->z, 0) матрице, на которую указывает *PM*.</span><span class="sxs-lookup"><span data-stu-id="4a6d6-120">This function transforms the vector (*pV*->x, *pV*->y, *pV*->z, 0) by the matrix pointed to by *pM*.</span></span>

<span data-ttu-id="4a6d6-121">Если необходимо преобразовать обычное значение, то матрица, передаваемая в эту функцию, должна быть преобразована обратно в матрицу, которая будет использоваться для преобразования точки.</span><span class="sxs-lookup"><span data-stu-id="4a6d6-121">If you want to transform a normal, the matrix you pass to this function should be the transpose of the inverse of the matrix you would use to transform a point.</span></span>

<span data-ttu-id="4a6d6-122">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="4a6d6-122">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="4a6d6-123">Таким образом, функция **D3DXVec3TransformNormal** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="4a6d6-123">In this way, the **D3DXVec3TransformNormal** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a6d6-124">Требования</span><span class="sxs-lookup"><span data-stu-id="4a6d6-124">Requirements</span></span>



| <span data-ttu-id="4a6d6-125">Требование</span><span class="sxs-lookup"><span data-stu-id="4a6d6-125">Requirement</span></span> | <span data-ttu-id="4a6d6-126">Значение</span><span class="sxs-lookup"><span data-stu-id="4a6d6-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4a6d6-127">Header</span><span class="sxs-lookup"><span data-stu-id="4a6d6-127">Header</span></span><br/>  | <dl> <span data-ttu-id="4a6d6-128"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a6d6-128"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="4a6d6-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4a6d6-129">Library</span></span><br/> | <dl> <span data-ttu-id="4a6d6-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4a6d6-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4a6d6-131">См. также</span><span class="sxs-lookup"><span data-stu-id="4a6d6-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a6d6-132">Математические функции</span><span class="sxs-lookup"><span data-stu-id="4a6d6-132">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




