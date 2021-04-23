---
description: Вычитает два двумерных вектора.
ms.assetid: e5a693e9-b143-41d5-923d-3f3f71461a42
title: Функция D3DXVec2Subtract (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Subtract
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7c12f41da7594f3eff9743eed7a1b0780f36c5fe
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104547871"
---
# <a name="d3dxvec2subtract-function"></a><span data-ttu-id="07bbf-103">Функция D3DXVec2Subtract</span><span class="sxs-lookup"><span data-stu-id="07bbf-103">D3DXVec2Subtract function</span></span>

<span data-ttu-id="07bbf-104">Вычитает два двумерных вектора.</span><span class="sxs-lookup"><span data-stu-id="07bbf-104">Subtracts two 2D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="07bbf-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="07bbf-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2Subtract(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV1,
  _In_    const D3DXVECTOR2 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="07bbf-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="07bbf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07bbf-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="07bbf-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="07bbf-108">Тип: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="07bbf-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="07bbf-109">Указатель на структуру [**D3DXVECTOR2**](d3dxvector2.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="07bbf-109">Pointer to the [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="07bbf-110">*pV1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="07bbf-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07bbf-111">Тип: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="07bbf-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="07bbf-112">Указатель на исходную структуру [**D3DXVECTOR2**](d3dxvector2.md) .</span><span class="sxs-lookup"><span data-stu-id="07bbf-112">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="07bbf-113">*pV2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="07bbf-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07bbf-114">Тип: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="07bbf-114">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="07bbf-115">Указатель на исходную структуру [**D3DXVECTOR2**](d3dxvector2.md) .</span><span class="sxs-lookup"><span data-stu-id="07bbf-115">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07bbf-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="07bbf-116">Return value</span></span>

<span data-ttu-id="07bbf-117">Тип: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="07bbf-117">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="07bbf-118">Указатель на структуру [**D3DXVECTOR2**](d3dxvector2.md) , которая является разностью двух векторов.</span><span class="sxs-lookup"><span data-stu-id="07bbf-118">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that is the difference of two vectors.</span></span>

## <a name="remarks"></a><span data-ttu-id="07bbf-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="07bbf-119">Remarks</span></span>

<span data-ttu-id="07bbf-120">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="07bbf-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="07bbf-121">Таким образом, функция **D3DXVec2Subtract** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="07bbf-121">In this way, the **D3DXVec2Subtract** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="07bbf-122">Требования</span><span class="sxs-lookup"><span data-stu-id="07bbf-122">Requirements</span></span>



| <span data-ttu-id="07bbf-123">Требование</span><span class="sxs-lookup"><span data-stu-id="07bbf-123">Requirement</span></span> | <span data-ttu-id="07bbf-124">Значение</span><span class="sxs-lookup"><span data-stu-id="07bbf-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="07bbf-125">Header</span><span class="sxs-lookup"><span data-stu-id="07bbf-125">Header</span></span><br/>  | <dl> <span data-ttu-id="07bbf-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="07bbf-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="07bbf-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="07bbf-127">Library</span></span><br/> | <dl> <span data-ttu-id="07bbf-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="07bbf-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="07bbf-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="07bbf-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07bbf-130">Математические функции</span><span class="sxs-lookup"><span data-stu-id="07bbf-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="07bbf-131">**D3DXVec2Add**</span><span class="sxs-lookup"><span data-stu-id="07bbf-131">**D3DXVec2Add**</span></span>](d3dxvec2add.md)
</dt> <dt>

[<span data-ttu-id="07bbf-132">**D3DXVec2Scale**</span><span class="sxs-lookup"><span data-stu-id="07bbf-132">**D3DXVec2Scale**</span></span>](d3dxvec2scale.md)
</dt> </dl>

 

 




