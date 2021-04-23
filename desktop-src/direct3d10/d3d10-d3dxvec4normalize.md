---
description: Возвращает нормализованную версию вектора 4D.
ms.assetid: ed3c48cf-4985-4ef3-b733-f8532e3ff6b5
title: Функция D3DXVec4Normalize (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Normalize
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: ebedbdddbe558bfad71520b64aa0cf2ff4c2f451
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355293"
---
# <a name="d3dxvec4normalize-function-d3dx10mathh"></a><span data-ttu-id="17eaf-103">Функция D3DXVec4Normalize (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="17eaf-103">D3DXVec4Normalize function (D3DX10Math.h)</span></span>

<span data-ttu-id="17eaf-104">Возвращает нормализованную версию вектора 4D.</span><span class="sxs-lookup"><span data-stu-id="17eaf-104">Returns the normalized version of a 4D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="17eaf-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="17eaf-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Normalize(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="17eaf-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="17eaf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17eaf-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="17eaf-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="17eaf-108">Тип: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="17eaf-108">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="17eaf-109">Указатель на [**D3DXVECTOR4**](d3d10-d3dxvector4.md) , который является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="17eaf-109">Pointer to the [**D3DXVECTOR4**](d3d10-d3dxvector4.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="17eaf-110">*ПС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="17eaf-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17eaf-111">Тип: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="17eaf-111">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="17eaf-112">Указатель на исходную структуру D3DXVECTOR4.</span><span class="sxs-lookup"><span data-stu-id="17eaf-112">Pointer to the source D3DXVECTOR4 structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17eaf-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="17eaf-113">Return value</span></span>

<span data-ttu-id="17eaf-114">Тип: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="17eaf-114">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="17eaf-115">Указатель на структуру D3DXVECTOR4, которая является нормализованной версией вектора.</span><span class="sxs-lookup"><span data-stu-id="17eaf-115">Pointer to a D3DXVECTOR4 structure that is the normalized version of the vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="17eaf-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="17eaf-116">Remarks</span></span>

<span data-ttu-id="17eaf-117">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="17eaf-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="17eaf-118">Таким образом, функция D3DXVec4Normalize может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="17eaf-118">In this way, the D3DXVec4Normalize function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="17eaf-119">Требования</span><span class="sxs-lookup"><span data-stu-id="17eaf-119">Requirements</span></span>



| <span data-ttu-id="17eaf-120">Требование</span><span class="sxs-lookup"><span data-stu-id="17eaf-120">Requirement</span></span> | <span data-ttu-id="17eaf-121">Значение</span><span class="sxs-lookup"><span data-stu-id="17eaf-121">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="17eaf-122">Header</span><span class="sxs-lookup"><span data-stu-id="17eaf-122">Header</span></span><br/> | <dl> <span data-ttu-id="17eaf-123"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="17eaf-123"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17eaf-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="17eaf-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17eaf-125">Математические функции</span><span class="sxs-lookup"><span data-stu-id="17eaf-125">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
