---
description: Функция D3DXVec4Cross (D3dx9math. h) — определяет перекрестное произведение четырех измерений.
ms.assetid: 10b965c9-7ed7-450c-86a0-114f068c888f
title: Функция D3DXVec4Cross (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Cross
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e3630a486f6c8fcd456373445bd931d878fdc38e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097692"
---
# <a name="d3dxvec4cross-function-d3dx9mathh"></a><span data-ttu-id="e7e1c-103">Функция D3DXVec4Cross (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="e7e1c-103">D3DXVec4Cross function (D3dx9math.h)</span></span>

<span data-ttu-id="e7e1c-104">Определяет перекрестное произведение четырех измерений.</span><span class="sxs-lookup"><span data-stu-id="e7e1c-104">Determines the cross-product in four dimensions.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7e1c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e7e1c-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Cross(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV1,
  _In_    const D3DXVECTOR4 *pV2,
  _In_    const D3DXVECTOR4 *pV3
);
```



## <a name="parameters"></a><span data-ttu-id="e7e1c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e7e1c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7e1c-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="e7e1c-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e7e1c-108">Тип: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="e7e1c-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="e7e1c-109">Указатель на структуру [**D3DXVECTOR4**](d3dxvector4.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="e7e1c-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="e7e1c-110">*pV1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e7e1c-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7e1c-111">Тип: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="e7e1c-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="e7e1c-112">Указатель на исходную структуру [**D3DXVECTOR4**](d3dxvector4.md) .</span><span class="sxs-lookup"><span data-stu-id="e7e1c-112">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="e7e1c-113">*pV2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e7e1c-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7e1c-114">Тип: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="e7e1c-114">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="e7e1c-115">Указатель на исходную структуру [**D3DXVECTOR4**](d3dxvector4.md) .</span><span class="sxs-lookup"><span data-stu-id="e7e1c-115">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="e7e1c-116">*pV3* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e7e1c-116">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7e1c-117">Тип: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="e7e1c-117">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="e7e1c-118">Указатель на исходную структуру [**D3DXVECTOR4**](d3dxvector4.md) .</span><span class="sxs-lookup"><span data-stu-id="e7e1c-118">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7e1c-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e7e1c-119">Return value</span></span>

<span data-ttu-id="e7e1c-120">Тип: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="e7e1c-120">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="e7e1c-121">Указатель на структуру [**D3DXVECTOR4**](d3dxvector4.md) , которая является перекрестным продуктом.</span><span class="sxs-lookup"><span data-stu-id="e7e1c-121">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is the cross product.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7e1c-122">Remarks</span><span class="sxs-lookup"><span data-stu-id="e7e1c-122">Remarks</span></span>

<span data-ttu-id="e7e1c-123">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="e7e1c-123">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="e7e1c-124">Таким образом, функция **D3DXVec4Cross** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="e7e1c-124">In this way, the **D3DXVec4Cross** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7e1c-125">Требования</span><span class="sxs-lookup"><span data-stu-id="e7e1c-125">Requirements</span></span>



| <span data-ttu-id="e7e1c-126">Требование</span><span class="sxs-lookup"><span data-stu-id="e7e1c-126">Requirement</span></span> | <span data-ttu-id="e7e1c-127">Значение</span><span class="sxs-lookup"><span data-stu-id="e7e1c-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e7e1c-128">Header</span><span class="sxs-lookup"><span data-stu-id="e7e1c-128">Header</span></span><br/>  | <dl> <span data-ttu-id="e7e1c-129"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7e1c-129"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="e7e1c-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e7e1c-130">Library</span></span><br/> | <dl> <span data-ttu-id="e7e1c-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e7e1c-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e7e1c-132">См. также</span><span class="sxs-lookup"><span data-stu-id="e7e1c-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7e1c-133">Математические функции</span><span class="sxs-lookup"><span data-stu-id="e7e1c-133">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="e7e1c-134">**D3DXVec4Dot**</span><span class="sxs-lookup"><span data-stu-id="e7e1c-134">**D3DXVec4Dot**</span></span>](d3dxvec4dot.md)
</dt> </dl>

 

 




