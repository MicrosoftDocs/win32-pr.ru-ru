---
description: Преобразует трехмерный вектор в нормальный по заданной матрице.
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
ms.openlocfilehash: 8dd0bf3fa2083d2cf0cc0cea72343f4774a586f5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273925"
---
# <a name="d3dxvec3transformnormal-function-d3dx9mathh"></a><span data-ttu-id="93ea0-103">Функция D3DXVec3TransformNormal (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="93ea0-103">D3DXVec3TransformNormal function (D3dx9math.h)</span></span>

<span data-ttu-id="93ea0-104">Преобразует трехмерный вектор в нормальный по заданной матрице.</span><span class="sxs-lookup"><span data-stu-id="93ea0-104">Transforms the 3D vector normal by the given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="93ea0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="93ea0-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3TransformNormal(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="93ea0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="93ea0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93ea0-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="93ea0-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="93ea0-108">Тип: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="93ea0-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="93ea0-109">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="93ea0-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="93ea0-110">*ПС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="93ea0-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93ea0-111">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="93ea0-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="93ea0-112">Указатель на исходную структуру [**D3DXVECTOR3**](d3dxvector3.md) .</span><span class="sxs-lookup"><span data-stu-id="93ea0-112">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="93ea0-113">*PM* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="93ea0-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93ea0-114">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="93ea0-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="93ea0-115">Указатель на исходную структуру [**D3DXMATRIX**](d3dxmatrix.md) .</span><span class="sxs-lookup"><span data-stu-id="93ea0-115">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93ea0-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="93ea0-116">Return value</span></span>

<span data-ttu-id="93ea0-117">Тип: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="93ea0-117">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="93ea0-118">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , которая является преобразованным вектором.</span><span class="sxs-lookup"><span data-stu-id="93ea0-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="93ea0-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="93ea0-119">Remarks</span></span>

<span data-ttu-id="93ea0-120">Эта функция преобразует вектор (*ПС*->x, *PV*->y, *PV*->z, 0) матрице, на которую указывает *PM*.</span><span class="sxs-lookup"><span data-stu-id="93ea0-120">This function transforms the vector (*pV*->x, *pV*->y, *pV*->z, 0) by the matrix pointed to by *pM*.</span></span>

<span data-ttu-id="93ea0-121">Если необходимо преобразовать обычное значение, то матрица, передаваемая в эту функцию, должна быть преобразована обратно в матрицу, которая будет использоваться для преобразования точки.</span><span class="sxs-lookup"><span data-stu-id="93ea0-121">If you want to transform a normal, the matrix you pass to this function should be the transpose of the inverse of the matrix you would use to transform a point.</span></span>

<span data-ttu-id="93ea0-122">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="93ea0-122">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="93ea0-123">Таким образом, функция **D3DXVec3TransformNormal** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="93ea0-123">In this way, the **D3DXVec3TransformNormal** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="93ea0-124">Требования</span><span class="sxs-lookup"><span data-stu-id="93ea0-124">Requirements</span></span>



| <span data-ttu-id="93ea0-125">Требование</span><span class="sxs-lookup"><span data-stu-id="93ea0-125">Requirement</span></span> | <span data-ttu-id="93ea0-126">Значение</span><span class="sxs-lookup"><span data-stu-id="93ea0-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="93ea0-127">Header</span><span class="sxs-lookup"><span data-stu-id="93ea0-127">Header</span></span><br/>  | <dl> <span data-ttu-id="93ea0-128"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="93ea0-128"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="93ea0-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="93ea0-129">Library</span></span><br/> | <dl> <span data-ttu-id="93ea0-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="93ea0-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="93ea0-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="93ea0-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93ea0-132">Математические функции</span><span class="sxs-lookup"><span data-stu-id="93ea0-132">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




