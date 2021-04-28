---
description: Функция D3DXVec4Cross (D3DX10Math. h) — определяет перекрестное произведение четырех измерений.
ms.assetid: 4f728fbd-cf5a-4d2e-ba4f-487616d83f6d
title: Функция D3DXVec4Cross (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Cross
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: e52cc1adb1e48f65599b1bf7179f7953823f1e1c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102952"
---
# <a name="d3dxvec4cross-function-d3dx10mathh"></a><span data-ttu-id="13011-103">Функция D3DXVec4Cross (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="13011-103">D3DXVec4Cross function (D3DX10Math.h)</span></span>

<span data-ttu-id="13011-104">Определяет перекрестное произведение четырех измерений.</span><span class="sxs-lookup"><span data-stu-id="13011-104">Determines the cross-product in four dimensions.</span></span>

## <a name="syntax"></a><span data-ttu-id="13011-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="13011-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Cross(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV1,
  _In_    const D3DXVECTOR4 *pV2,
  _In_    const D3DXVECTOR4 *pV3
);
```



## <a name="parameters"></a><span data-ttu-id="13011-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="13011-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13011-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="13011-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="13011-108">Тип: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="13011-108">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="13011-109">Указатель на [**D3DXVECTOR4**](d3d10-d3dxvector4.md) , который является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="13011-109">Pointer to the [**D3DXVECTOR4**](d3d10-d3dxvector4.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="13011-110">*pV1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="13011-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13011-111">Тип: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="13011-111">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="13011-112">Указатель на исходную структуру D3DXVECTOR4.</span><span class="sxs-lookup"><span data-stu-id="13011-112">Pointer to a source D3DXVECTOR4 structure.</span></span>

</dd> <dt>

<span data-ttu-id="13011-113">*pV2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="13011-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13011-114">Тип: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="13011-114">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="13011-115">Указатель на исходную структуру D3DXVECTOR4.</span><span class="sxs-lookup"><span data-stu-id="13011-115">Pointer to a source D3DXVECTOR4 structure.</span></span>

</dd> <dt>

<span data-ttu-id="13011-116">*pV3* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="13011-116">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13011-117">Тип: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="13011-117">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="13011-118">Указатель на исходную структуру D3DXVECTOR4.</span><span class="sxs-lookup"><span data-stu-id="13011-118">Pointer to a source D3DXVECTOR4 structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13011-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="13011-119">Return value</span></span>

<span data-ttu-id="13011-120">Тип: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="13011-120">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="13011-121">Указатель на структуру D3DXVECTOR4, которая является перекрестным продуктом.</span><span class="sxs-lookup"><span data-stu-id="13011-121">Pointer to a D3DXVECTOR4 structure that is the cross product.</span></span>

## <a name="remarks"></a><span data-ttu-id="13011-122">Remarks</span><span class="sxs-lookup"><span data-stu-id="13011-122">Remarks</span></span>

<span data-ttu-id="13011-123">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="13011-123">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="13011-124">Таким образом, функция D3DXVec4Cross может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="13011-124">In this way, the D3DXVec4Cross function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="13011-125">Требования</span><span class="sxs-lookup"><span data-stu-id="13011-125">Requirements</span></span>



| <span data-ttu-id="13011-126">Требование</span><span class="sxs-lookup"><span data-stu-id="13011-126">Requirement</span></span> | <span data-ttu-id="13011-127">Значение</span><span class="sxs-lookup"><span data-stu-id="13011-127">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="13011-128">Header</span><span class="sxs-lookup"><span data-stu-id="13011-128">Header</span></span><br/> | <dl> <span data-ttu-id="13011-129"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="13011-129"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13011-130">См. также</span><span class="sxs-lookup"><span data-stu-id="13011-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13011-131">Математические функции</span><span class="sxs-lookup"><span data-stu-id="13011-131">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
