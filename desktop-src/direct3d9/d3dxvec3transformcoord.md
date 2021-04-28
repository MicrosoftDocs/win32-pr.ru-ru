---
description: Функция D3DXVec3TransformCoord (D3dx9math. h) — Преобразует трехмерный вектор в заданную матрицу с проецированием результата обратно в w = 1.
ms.assetid: 4075b067-1e64-46c9-be73-5fa765c9cb9d
title: Функция D3DXVec3TransformCoord (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformCoord
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e4e3514d4717262a7afab7ae808d747de3a1b635
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115632"
---
# <a name="d3dxvec3transformcoord-function-d3dx9mathh"></a><span data-ttu-id="03a7f-103">Функция D3DXVec3TransformCoord (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="03a7f-103">D3DXVec3TransformCoord function (D3dx9math.h)</span></span>

<span data-ttu-id="03a7f-104">Преобразует трехмерный вектор в заданную матрицу с проецированием результата обратно в w = 1.</span><span class="sxs-lookup"><span data-stu-id="03a7f-104">Transforms a 3D vector by a given matrix, projecting the result back into w = 1.</span></span>

## <a name="syntax"></a><span data-ttu-id="03a7f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="03a7f-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3TransformCoord(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="03a7f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="03a7f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03a7f-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="03a7f-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="03a7f-108">Тип: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="03a7f-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="03a7f-109">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="03a7f-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="03a7f-110">*ПС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="03a7f-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03a7f-111">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="03a7f-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="03a7f-112">Указатель на исходную структуру [**D3DXVECTOR3**](d3dxvector3.md) .</span><span class="sxs-lookup"><span data-stu-id="03a7f-112">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="03a7f-113">*PM* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="03a7f-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03a7f-114">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="03a7f-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="03a7f-115">Указатель на исходную структуру [**D3DXMATRIX**](d3dxmatrix.md) .</span><span class="sxs-lookup"><span data-stu-id="03a7f-115">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03a7f-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="03a7f-116">Return value</span></span>

<span data-ttu-id="03a7f-117">Тип: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="03a7f-117">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="03a7f-118">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , которая является преобразованным вектором.</span><span class="sxs-lookup"><span data-stu-id="03a7f-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="03a7f-119">Remarks</span><span class="sxs-lookup"><span data-stu-id="03a7f-119">Remarks</span></span>

<span data-ttu-id="03a7f-120">Эта функция преобразует вектор, *НЗ* (x, y, z, 1) матрицу, выполнив проецирование результата обратно в w = 1.</span><span class="sxs-lookup"><span data-stu-id="03a7f-120">This function transforms the vector, *pV* (x, y, z, 1), by the matrix, *pM*, projecting the result back into w=1.</span></span>

<span data-ttu-id="03a7f-121">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="03a7f-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="03a7f-122">Таким образом, функция **D3DXVec3TransformCoord** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="03a7f-122">In this way, the **D3DXVec3TransformCoord** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="03a7f-123">Требования</span><span class="sxs-lookup"><span data-stu-id="03a7f-123">Requirements</span></span>



| <span data-ttu-id="03a7f-124">Требование</span><span class="sxs-lookup"><span data-stu-id="03a7f-124">Requirement</span></span> | <span data-ttu-id="03a7f-125">Значение</span><span class="sxs-lookup"><span data-stu-id="03a7f-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="03a7f-126">Header</span><span class="sxs-lookup"><span data-stu-id="03a7f-126">Header</span></span><br/>  | <dl> <span data-ttu-id="03a7f-127"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="03a7f-127"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="03a7f-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="03a7f-128">Library</span></span><br/> | <dl> <span data-ttu-id="03a7f-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="03a7f-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="03a7f-130">См. также</span><span class="sxs-lookup"><span data-stu-id="03a7f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03a7f-131">Математические функции</span><span class="sxs-lookup"><span data-stu-id="03a7f-131">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="03a7f-132">**D3DXVec3Transform**</span><span class="sxs-lookup"><span data-stu-id="03a7f-132">**D3DXVec3Transform**</span></span>](d3dxvec3transform.md)
</dt> <dt>

[<span data-ttu-id="03a7f-133">**D3DXVec3TransformNormal**</span><span class="sxs-lookup"><span data-stu-id="03a7f-133">**D3DXVec3TransformNormal**</span></span>](d3dxvec3transformnormal.md)
</dt> </dl>

 

 




