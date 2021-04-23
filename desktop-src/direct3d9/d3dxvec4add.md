---
description: Складывает два вектора 4D.
ms.assetid: da807dc0-6a31-4315-a32d-a42062c22199
title: Функция D3DXVec4Add (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Add
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 62747cec15c4a9916dfb42572006cbb9fc908b3e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105647879"
---
# <a name="d3dxvec4add-function"></a><span data-ttu-id="d40a9-103">Функция D3DXVec4Add</span><span class="sxs-lookup"><span data-stu-id="d40a9-103">D3DXVec4Add function</span></span>

<span data-ttu-id="d40a9-104">Складывает два вектора 4D.</span><span class="sxs-lookup"><span data-stu-id="d40a9-104">Adds two 4D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="d40a9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d40a9-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Add(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV1,
  _In_    const D3DXVECTOR4 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="d40a9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d40a9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d40a9-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="d40a9-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d40a9-108">Тип: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="d40a9-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="d40a9-109">Указатель на структуру [**D3DXVECTOR4**](d3dxvector4.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="d40a9-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="d40a9-110">*pV1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d40a9-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d40a9-111">Тип: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="d40a9-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="d40a9-112">Указатель на исходную структуру [**D3DXVECTOR4**](d3dxvector4.md) .</span><span class="sxs-lookup"><span data-stu-id="d40a9-112">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="d40a9-113">*pV2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d40a9-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d40a9-114">Тип: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="d40a9-114">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="d40a9-115">Указатель на исходную структуру [**D3DXVECTOR4**](d3dxvector4.md) .</span><span class="sxs-lookup"><span data-stu-id="d40a9-115">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d40a9-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d40a9-116">Return value</span></span>

<span data-ttu-id="d40a9-117">Тип: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="d40a9-117">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="d40a9-118">Указатель на структуру [**D3DXVECTOR4**](d3dxvector4.md) , которая является суммой двух векторов.</span><span class="sxs-lookup"><span data-stu-id="d40a9-118">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is the sum of the two vectors.</span></span>

## <a name="remarks"></a><span data-ttu-id="d40a9-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d40a9-119">Remarks</span></span>

<span data-ttu-id="d40a9-120">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="d40a9-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="d40a9-121">Таким образом, функция **D3DXVec4Add** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="d40a9-121">In this way, the **D3DXVec4Add** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d40a9-122">Требования</span><span class="sxs-lookup"><span data-stu-id="d40a9-122">Requirements</span></span>



| <span data-ttu-id="d40a9-123">Требование</span><span class="sxs-lookup"><span data-stu-id="d40a9-123">Requirement</span></span> | <span data-ttu-id="d40a9-124">Значение</span><span class="sxs-lookup"><span data-stu-id="d40a9-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d40a9-125">Header</span><span class="sxs-lookup"><span data-stu-id="d40a9-125">Header</span></span><br/>  | <dl> <span data-ttu-id="d40a9-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="d40a9-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="d40a9-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d40a9-127">Library</span></span><br/> | <dl> <span data-ttu-id="d40a9-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d40a9-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d40a9-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d40a9-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d40a9-130">Математические функции</span><span class="sxs-lookup"><span data-stu-id="d40a9-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="d40a9-131">**D3DXVec4Subtract**</span><span class="sxs-lookup"><span data-stu-id="d40a9-131">**D3DXVec4Subtract**</span></span>](d3dxvec4subtract.md)
</dt> <dt>

[<span data-ttu-id="d40a9-132">**D3DXVec4Scale**</span><span class="sxs-lookup"><span data-stu-id="d40a9-132">**D3DXVec4Scale**</span></span>](d3dxvec4scale.md)
</dt> </dl>

 

 




