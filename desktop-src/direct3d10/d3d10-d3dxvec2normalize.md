---
description: Функция D3DXVec2Normalize (D3DX10Math. h) — Возвращает нормализованную версию 2D-вектора.
ms.assetid: fac4f269-2778-4500-af9e-23a0112543b0
title: Функция D3DXVec2Normalize (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: aaa7bde759b9023b69204d6cb39259f0905b9928
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108392"
---
# <a name="d3dxvec2normalize-function-d3dx10mathh"></a><span data-ttu-id="8a0c4-103">Функция D3DXVec2Normalize (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="8a0c4-103">D3DXVec2Normalize function (D3DX10Math.h)</span></span>

<span data-ttu-id="8a0c4-104">Возвращает нормализованную версию 2D-вектора.</span><span class="sxs-lookup"><span data-stu-id="8a0c4-104">Returns the normalized version of a 2D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a0c4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8a0c4-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2Normalize(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="8a0c4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8a0c4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a0c4-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="8a0c4-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8a0c4-108">Тип: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="8a0c4-108">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="8a0c4-109">Указатель на [**D3DXVECTOR2**](d3d10-d3dxvector2.md) , который является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="8a0c4-109">Pointer to the [**D3DXVECTOR2**](d3d10-d3dxvector2.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="8a0c4-110">*ПС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8a0c4-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a0c4-111">Тип: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="8a0c4-111">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="8a0c4-112">Указатель на исходную структуру D3DXVECTOR2.</span><span class="sxs-lookup"><span data-stu-id="8a0c4-112">Pointer to the source D3DXVECTOR2 structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a0c4-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8a0c4-113">Return value</span></span>

<span data-ttu-id="8a0c4-114">Тип: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="8a0c4-114">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="8a0c4-115">Указатель на структуру D3DXVECTOR2, которая является нормализованной версией вектора.</span><span class="sxs-lookup"><span data-stu-id="8a0c4-115">Pointer to a D3DXVECTOR2 structure that is the normalized version of the vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a0c4-116">Remarks</span><span class="sxs-lookup"><span data-stu-id="8a0c4-116">Remarks</span></span>

<span data-ttu-id="8a0c4-117">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="8a0c4-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="8a0c4-118">Таким образом, функция D3DXVec2Normalize может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="8a0c4-118">In this way, the D3DXVec2Normalize function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a0c4-119">Требования</span><span class="sxs-lookup"><span data-stu-id="8a0c4-119">Requirements</span></span>



| <span data-ttu-id="8a0c4-120">Требование</span><span class="sxs-lookup"><span data-stu-id="8a0c4-120">Requirement</span></span> | <span data-ttu-id="8a0c4-121">Значение</span><span class="sxs-lookup"><span data-stu-id="8a0c4-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8a0c4-122">Header</span><span class="sxs-lookup"><span data-stu-id="8a0c4-122">Header</span></span><br/>  | <dl> <span data-ttu-id="8a0c4-123"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a0c4-123"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="8a0c4-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8a0c4-124">Library</span></span><br/> | <dl> <span data-ttu-id="8a0c4-125"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8a0c4-125"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8a0c4-126">См. также</span><span class="sxs-lookup"><span data-stu-id="8a0c4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a0c4-127">Математические функции</span><span class="sxs-lookup"><span data-stu-id="8a0c4-127">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
