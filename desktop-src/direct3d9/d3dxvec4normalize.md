---
description: Возвращает нормализованную версию вектора 4D.
ms.assetid: e12d5dc7-b26f-41dd-b89d-1df9ba23077a
title: Функция D3DXVec4Normalize (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Normalize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 38d97f337711375d1d414eb78fb317672bc7c5cb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104081957"
---
# <a name="d3dxvec4normalize-function-d3dx9mathh"></a><span data-ttu-id="439de-103">Функция D3DXVec4Normalize (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="439de-103">D3DXVec4Normalize function (D3dx9math.h)</span></span>

<span data-ttu-id="439de-104">Возвращает нормализованную версию вектора 4D.</span><span class="sxs-lookup"><span data-stu-id="439de-104">Returns the normalized version of a 4D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="439de-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="439de-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Normalize(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="439de-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="439de-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="439de-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="439de-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="439de-108">Тип: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="439de-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="439de-109">Указатель на структуру [**D3DXVECTOR4**](d3dxvector4.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="439de-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="439de-110">*ПС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="439de-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="439de-111">Тип: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="439de-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="439de-112">Указатель на исходную структуру [**D3DXVECTOR4**](d3dxvector4.md) .</span><span class="sxs-lookup"><span data-stu-id="439de-112">Pointer to the source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="439de-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="439de-113">Return value</span></span>

<span data-ttu-id="439de-114">Тип: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="439de-114">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="439de-115">Указатель на структуру [**D3DXVECTOR4**](d3dxvector4.md) , которая является нормализованной версией вектора.</span><span class="sxs-lookup"><span data-stu-id="439de-115">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is the normalized version of the vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="439de-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="439de-116">Remarks</span></span>

<span data-ttu-id="439de-117">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="439de-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="439de-118">Таким образом, функция **D3DXVec4Normalize** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="439de-118">In this way, the **D3DXVec4Normalize** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="439de-119">Требования</span><span class="sxs-lookup"><span data-stu-id="439de-119">Requirements</span></span>



| <span data-ttu-id="439de-120">Требование</span><span class="sxs-lookup"><span data-stu-id="439de-120">Requirement</span></span> | <span data-ttu-id="439de-121">Значение</span><span class="sxs-lookup"><span data-stu-id="439de-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="439de-122">Header</span><span class="sxs-lookup"><span data-stu-id="439de-122">Header</span></span><br/>  | <dl> <span data-ttu-id="439de-123"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="439de-123"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="439de-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="439de-124">Library</span></span><br/> | <dl> <span data-ttu-id="439de-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="439de-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="439de-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="439de-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="439de-127">Математические функции</span><span class="sxs-lookup"><span data-stu-id="439de-127">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




