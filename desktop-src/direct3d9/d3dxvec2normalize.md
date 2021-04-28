---
description: Функция D3DXVec2Normalize (D3dx9math. h) — Возвращает нормализованную версию 2D-вектора.
ms.assetid: 2796a5d1-cb1c-4093-87f2-a2ad43279d91
title: Функция D3DXVec2Normalize (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Normalize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3322981be5c266bee20a61e85302cb22538a7b0d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097972"
---
# <a name="d3dxvec2normalize-function-d3dx9mathh"></a><span data-ttu-id="590fc-103">Функция D3DXVec2Normalize (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="590fc-103">D3DXVec2Normalize function (D3dx9math.h)</span></span>

<span data-ttu-id="590fc-104">Возвращает нормализованную версию 2D-вектора.</span><span class="sxs-lookup"><span data-stu-id="590fc-104">Returns the normalized version of a 2D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="590fc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="590fc-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2Normalize(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="590fc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="590fc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="590fc-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="590fc-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="590fc-108">Тип: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="590fc-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="590fc-109">Указатель на структуру [**D3DXVECTOR2**](d3dxvector2.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="590fc-109">Pointer to the [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="590fc-110">*ПС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="590fc-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="590fc-111">Тип: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="590fc-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="590fc-112">Указатель на исходную структуру [**D3DXVECTOR2**](d3dxvector2.md) .</span><span class="sxs-lookup"><span data-stu-id="590fc-112">Pointer to the source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="590fc-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="590fc-113">Return value</span></span>

<span data-ttu-id="590fc-114">Тип: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="590fc-114">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="590fc-115">Указатель на структуру [**D3DXVECTOR2**](d3dxvector2.md) , которая является нормализованной версией вектора.</span><span class="sxs-lookup"><span data-stu-id="590fc-115">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that is the normalized version of the vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="590fc-116">Remarks</span><span class="sxs-lookup"><span data-stu-id="590fc-116">Remarks</span></span>

<span data-ttu-id="590fc-117">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="590fc-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="590fc-118">Таким образом, функция **D3DXVec2Normalize** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="590fc-118">In this way, the **D3DXVec2Normalize** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="590fc-119">Требования</span><span class="sxs-lookup"><span data-stu-id="590fc-119">Requirements</span></span>



| <span data-ttu-id="590fc-120">Требование</span><span class="sxs-lookup"><span data-stu-id="590fc-120">Requirement</span></span> | <span data-ttu-id="590fc-121">Значение</span><span class="sxs-lookup"><span data-stu-id="590fc-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="590fc-122">Header</span><span class="sxs-lookup"><span data-stu-id="590fc-122">Header</span></span><br/>  | <dl> <span data-ttu-id="590fc-123"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="590fc-123"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="590fc-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="590fc-124">Library</span></span><br/> | <dl> <span data-ttu-id="590fc-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="590fc-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="590fc-126">См. также</span><span class="sxs-lookup"><span data-stu-id="590fc-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="590fc-127">Математические функции</span><span class="sxs-lookup"><span data-stu-id="590fc-127">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




