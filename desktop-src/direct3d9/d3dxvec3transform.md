---
description: Функция D3DXVec3Transform (D3dx9math. h) — преобразует вектор (x, y, z, 1) в заданную матрицу.
ms.assetid: 5b290c4c-22f1-4086-8e5e-f995757ef193
title: Функция D3DXVec3Transform (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Transform
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5128be3fd9e0409b403006fdb1de3c9c48f6aee4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115642"
---
# <a name="d3dxvec3transform-function-d3dx9mathh"></a><span data-ttu-id="41e87-103">Функция D3DXVec3Transform (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="41e87-103">D3DXVec3Transform function (D3dx9math.h)</span></span>

<span data-ttu-id="41e87-104">Преобразует вектор (x, y, z, 1) в заданную матрицу.</span><span class="sxs-lookup"><span data-stu-id="41e87-104">Transforms vector (x, y, z, 1) by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="41e87-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="41e87-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec3Transform(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="41e87-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="41e87-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41e87-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="41e87-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="41e87-108">Тип: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="41e87-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="41e87-109">Указатель на структуру [**D3DXVECTOR4**](d3dxvector4.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="41e87-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="41e87-110">*ПС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="41e87-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41e87-111">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="41e87-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="41e87-112">Указатель на исходную структуру [**D3DXVECTOR3**](d3dxvector3.md) .</span><span class="sxs-lookup"><span data-stu-id="41e87-112">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="41e87-113">*PM* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="41e87-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41e87-114">Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="41e87-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="41e87-115">Указатель на исходную структуру [**D3DXMATRIX**](d3dxmatrix.md) .</span><span class="sxs-lookup"><span data-stu-id="41e87-115">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41e87-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="41e87-116">Return value</span></span>

<span data-ttu-id="41e87-117">Тип: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="41e87-117">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="41e87-118">Указатель на структуру [**D3DXVECTOR4**](d3dxvector4.md) , которая является преобразованным вектором.</span><span class="sxs-lookup"><span data-stu-id="41e87-118">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="41e87-119">Remarks</span><span class="sxs-lookup"><span data-stu-id="41e87-119">Remarks</span></span>

<span data-ttu-id="41e87-120">Эта функция преобразует вектор, *НЗ* (x, y, z, 1) в матрицу *PM*.</span><span class="sxs-lookup"><span data-stu-id="41e87-120">This function transforms the vector, *pV* (x, y, z, 1), by the matrix *pM*.</span></span>

<span data-ttu-id="41e87-121">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="41e87-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="41e87-122">Таким образом, функция **D3DXVec3Transform** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="41e87-122">In this way, the **D3DXVec3Transform** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="41e87-123">Требования</span><span class="sxs-lookup"><span data-stu-id="41e87-123">Requirements</span></span>



| <span data-ttu-id="41e87-124">Требование</span><span class="sxs-lookup"><span data-stu-id="41e87-124">Requirement</span></span> | <span data-ttu-id="41e87-125">Значение</span><span class="sxs-lookup"><span data-stu-id="41e87-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="41e87-126">Header</span><span class="sxs-lookup"><span data-stu-id="41e87-126">Header</span></span><br/>  | <dl> <span data-ttu-id="41e87-127"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="41e87-127"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="41e87-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="41e87-128">Library</span></span><br/> | <dl> <span data-ttu-id="41e87-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="41e87-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="41e87-130">См. также</span><span class="sxs-lookup"><span data-stu-id="41e87-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41e87-131">Математические функции</span><span class="sxs-lookup"><span data-stu-id="41e87-131">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




