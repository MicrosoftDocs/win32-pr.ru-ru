---
description: Функция D3DXVec3Normalize (D3dx9math. h) — Возвращает нормализованную версию трехмерного вектора.
ms.assetid: 7bb8302e-8af2-4328-9b46-bc9f5a009f56
title: Функция D3DXVec3Normalize (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Normalize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f39890a92bbff9d27a1150e76092d865dc36c089
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097832"
---
# <a name="d3dxvec3normalize-function-d3dx9mathh"></a><span data-ttu-id="0e709-103">Функция D3DXVec3Normalize (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="0e709-103">D3DXVec3Normalize function (D3dx9math.h)</span></span>

<span data-ttu-id="0e709-104">Возвращает нормализованную версию трехмерного вектора.</span><span class="sxs-lookup"><span data-stu-id="0e709-104">Returns the normalized version of a 3D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e709-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0e709-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Normalize(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="0e709-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0e709-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e709-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="0e709-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0e709-108">Тип: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="0e709-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="0e709-109">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="0e709-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="0e709-110">*ПС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0e709-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e709-111">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="0e709-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="0e709-112">Указатель на исходную структуру [**D3DXVECTOR3**](d3dxvector3.md) .</span><span class="sxs-lookup"><span data-stu-id="0e709-112">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e709-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0e709-113">Return value</span></span>

<span data-ttu-id="0e709-114">Тип: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="0e709-114">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="0e709-115">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , которая является нормализованной версией указанного вектора.</span><span class="sxs-lookup"><span data-stu-id="0e709-115">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the normalized version of the specified vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e709-116">Remarks</span><span class="sxs-lookup"><span data-stu-id="0e709-116">Remarks</span></span>

<span data-ttu-id="0e709-117">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="0e709-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="0e709-118">Таким образом, функция **D3DXVec3Normalize** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="0e709-118">In this way, the **D3DXVec3Normalize** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e709-119">Требования</span><span class="sxs-lookup"><span data-stu-id="0e709-119">Requirements</span></span>



| <span data-ttu-id="0e709-120">Требование</span><span class="sxs-lookup"><span data-stu-id="0e709-120">Requirement</span></span> | <span data-ttu-id="0e709-121">Значение</span><span class="sxs-lookup"><span data-stu-id="0e709-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0e709-122">Header</span><span class="sxs-lookup"><span data-stu-id="0e709-122">Header</span></span><br/>  | <dl> <span data-ttu-id="0e709-123"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e709-123"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="0e709-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0e709-124">Library</span></span><br/> | <dl> <span data-ttu-id="0e709-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0e709-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0e709-126">См. также</span><span class="sxs-lookup"><span data-stu-id="0e709-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e709-127">Математические функции</span><span class="sxs-lookup"><span data-stu-id="0e709-127">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




