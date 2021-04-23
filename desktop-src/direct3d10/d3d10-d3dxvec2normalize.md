---
description: Возвращает нормализованную версию 2D-вектора.
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
ms.openlocfilehash: e2894a86c0aa0c2ef6b45a41664b2d0cca1427c1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103914784"
---
# <a name="d3dxvec2normalize-function-d3dx10mathh"></a><span data-ttu-id="8d269-103">Функция D3DXVec2Normalize (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="8d269-103">D3DXVec2Normalize function (D3DX10Math.h)</span></span>

<span data-ttu-id="8d269-104">Возвращает нормализованную версию 2D-вектора.</span><span class="sxs-lookup"><span data-stu-id="8d269-104">Returns the normalized version of a 2D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d269-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8d269-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2Normalize(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="8d269-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8d269-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d269-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="8d269-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8d269-108">Тип: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="8d269-108">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="8d269-109">Указатель на [**D3DXVECTOR2**](d3d10-d3dxvector2.md) , который является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="8d269-109">Pointer to the [**D3DXVECTOR2**](d3d10-d3dxvector2.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="8d269-110">*ПС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8d269-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d269-111">Тип: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="8d269-111">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="8d269-112">Указатель на исходную структуру D3DXVECTOR2.</span><span class="sxs-lookup"><span data-stu-id="8d269-112">Pointer to the source D3DXVECTOR2 structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d269-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8d269-113">Return value</span></span>

<span data-ttu-id="8d269-114">Тип: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="8d269-114">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="8d269-115">Указатель на структуру D3DXVECTOR2, которая является нормализованной версией вектора.</span><span class="sxs-lookup"><span data-stu-id="8d269-115">Pointer to a D3DXVECTOR2 structure that is the normalized version of the vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d269-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8d269-116">Remarks</span></span>

<span data-ttu-id="8d269-117">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="8d269-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="8d269-118">Таким образом, функция D3DXVec2Normalize может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="8d269-118">In this way, the D3DXVec2Normalize function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d269-119">Требования</span><span class="sxs-lookup"><span data-stu-id="8d269-119">Requirements</span></span>



| <span data-ttu-id="8d269-120">Требование</span><span class="sxs-lookup"><span data-stu-id="8d269-120">Requirement</span></span> | <span data-ttu-id="8d269-121">Значение</span><span class="sxs-lookup"><span data-stu-id="8d269-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8d269-122">Header</span><span class="sxs-lookup"><span data-stu-id="8d269-122">Header</span></span><br/>  | <dl> <span data-ttu-id="8d269-123"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d269-123"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="8d269-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8d269-124">Library</span></span><br/> | <dl> <span data-ttu-id="8d269-125"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8d269-125"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8d269-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8d269-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d269-127">Математические функции</span><span class="sxs-lookup"><span data-stu-id="8d269-127">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
