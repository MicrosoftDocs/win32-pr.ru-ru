---
description: Возвращает двумерный вектор, состоящие из самых крупных компонентов двух двумерных векторов.
ms.assetid: 5eb5141b-d611-4c6b-a3e3-c7ad8f223657
title: Функция D3DXVec2Maximize (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Maximize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ffd5fbc98e653a6bbaffa7d3cec16b13695365b2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424381"
---
# <a name="d3dxvec2maximize-function"></a><span data-ttu-id="c9c32-103">Функция D3DXVec2Maximize</span><span class="sxs-lookup"><span data-stu-id="c9c32-103">D3DXVec2Maximize function</span></span>

<span data-ttu-id="c9c32-104">Возвращает двумерный вектор, состоящие из самых крупных компонентов двух двумерных векторов.</span><span class="sxs-lookup"><span data-stu-id="c9c32-104">Returns a 2D vector that is made up of the largest components of two 2D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9c32-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c9c32-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2Maximize(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV1,
  _In_    const D3DXVECTOR2 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="c9c32-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c9c32-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9c32-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="c9c32-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c9c32-108">Тип: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="c9c32-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="c9c32-109">Указатель на структуру [**D3DXVECTOR2**](d3dxvector2.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="c9c32-109">Pointer to the [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="c9c32-110">*pV1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c9c32-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9c32-111">Тип: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="c9c32-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="c9c32-112">Указатель на исходную структуру [**D3DXVECTOR2**](d3dxvector2.md) .</span><span class="sxs-lookup"><span data-stu-id="c9c32-112">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="c9c32-113">*pV2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c9c32-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9c32-114">Тип: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="c9c32-114">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="c9c32-115">Указатель на исходную структуру [**D3DXVECTOR2**](d3dxvector2.md) .</span><span class="sxs-lookup"><span data-stu-id="c9c32-115">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9c32-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c9c32-116">Return value</span></span>

<span data-ttu-id="c9c32-117">Тип: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="c9c32-117">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="c9c32-118">Указатель на структуру [**D3DXVECTOR2**](d3dxvector2.md) , которая состоит из самых крупных компонентов двух векторов.</span><span class="sxs-lookup"><span data-stu-id="c9c32-118">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that is made up of the largest components of the two vectors.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9c32-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c9c32-119">Remarks</span></span>

<span data-ttu-id="c9c32-120">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="c9c32-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="c9c32-121">Таким образом, функция **D3DXVec2Maximize** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="c9c32-121">In this way, the **D3DXVec2Maximize** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9c32-122">Требования</span><span class="sxs-lookup"><span data-stu-id="c9c32-122">Requirements</span></span>



| <span data-ttu-id="c9c32-123">Требование</span><span class="sxs-lookup"><span data-stu-id="c9c32-123">Requirement</span></span> | <span data-ttu-id="c9c32-124">Значение</span><span class="sxs-lookup"><span data-stu-id="c9c32-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c9c32-125">Header</span><span class="sxs-lookup"><span data-stu-id="c9c32-125">Header</span></span><br/>  | <dl> <span data-ttu-id="c9c32-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9c32-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="c9c32-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c9c32-127">Library</span></span><br/> | <dl> <span data-ttu-id="c9c32-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c9c32-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c9c32-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c9c32-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9c32-130">Математические функции</span><span class="sxs-lookup"><span data-stu-id="c9c32-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="c9c32-131">**D3DXVec2Minimize**</span><span class="sxs-lookup"><span data-stu-id="c9c32-131">**D3DXVec2Minimize**</span></span>](d3dxvec2minimize.md)
</dt> </dl>

 

 




