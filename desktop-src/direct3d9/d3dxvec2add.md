---
description: Добавляет два 2D-вектора.
ms.assetid: 82b2fdf6-1b1f-4768-8c0b-ac8faa77d7ed
title: Функция D3DXVec2Add (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Add
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5087177448b01763bd94acb9b50c27c6cdf38815
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000342"
---
# <a name="d3dxvec2add-function"></a><span data-ttu-id="af402-103">Функция D3DXVec2Add</span><span class="sxs-lookup"><span data-stu-id="af402-103">D3DXVec2Add function</span></span>

<span data-ttu-id="af402-104">Добавляет два 2D-вектора.</span><span class="sxs-lookup"><span data-stu-id="af402-104">Adds two 2D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="af402-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="af402-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2Add(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV1,
  _In_    const D3DXVECTOR2 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="af402-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="af402-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af402-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="af402-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="af402-108">Тип: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="af402-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="af402-109">Указатель на структуру [**D3DXVECTOR2**](d3dxvector2.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="af402-109">Pointer to the [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="af402-110">*pV1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="af402-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af402-111">Тип: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="af402-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="af402-112">Указатель на исходную структуру [**D3DXVECTOR2**](d3dxvector2.md) .</span><span class="sxs-lookup"><span data-stu-id="af402-112">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="af402-113">*pV2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="af402-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af402-114">Тип: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="af402-114">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="af402-115">Указатель на исходную структуру [**D3DXVECTOR2**](d3dxvector2.md) .</span><span class="sxs-lookup"><span data-stu-id="af402-115">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af402-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="af402-116">Return value</span></span>

<span data-ttu-id="af402-117">Тип: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="af402-117">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="af402-118">Указатель на структуру [**D3DXVECTOR2**](d3dxvector2.md) , которая является суммой двух векторов.</span><span class="sxs-lookup"><span data-stu-id="af402-118">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that is the sum of the two vectors.</span></span>

## <a name="remarks"></a><span data-ttu-id="af402-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="af402-119">Remarks</span></span>

<span data-ttu-id="af402-120">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="af402-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="af402-121">Таким образом, функция **D3DXVec2Add** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="af402-121">In this way, the **D3DXVec2Add** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="af402-122">Требования</span><span class="sxs-lookup"><span data-stu-id="af402-122">Requirements</span></span>



| <span data-ttu-id="af402-123">Требование</span><span class="sxs-lookup"><span data-stu-id="af402-123">Requirement</span></span> | <span data-ttu-id="af402-124">Значение</span><span class="sxs-lookup"><span data-stu-id="af402-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="af402-125">Header</span><span class="sxs-lookup"><span data-stu-id="af402-125">Header</span></span><br/>  | <dl> <span data-ttu-id="af402-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="af402-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="af402-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="af402-127">Library</span></span><br/> | <dl> <span data-ttu-id="af402-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="af402-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="af402-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="af402-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af402-130">Математические функции</span><span class="sxs-lookup"><span data-stu-id="af402-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="af402-131">**D3DXVec2Subtract**</span><span class="sxs-lookup"><span data-stu-id="af402-131">**D3DXVec2Subtract**</span></span>](d3dxvec2subtract.md)
</dt> <dt>

[<span data-ttu-id="af402-132">**D3DXVec2Scale**</span><span class="sxs-lookup"><span data-stu-id="af402-132">**D3DXVec2Scale**</span></span>](d3dxvec2scale.md)
</dt> </dl>

 

 




