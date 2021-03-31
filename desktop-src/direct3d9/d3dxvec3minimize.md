---
description: Возвращает трехмерный вектор, который состоит из наименьших компонентов двух трехмерных векторов.
ms.assetid: f38164a5-d016-4a8a-a7fe-d7eb0a681107
title: Функция D3DXVec3Minimize (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Minimize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 532c3cfaddc63b0f358fa3ce88afeccc2f12e289
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104081948"
---
# <a name="d3dxvec3minimize-function"></a><span data-ttu-id="eff3b-103">Функция D3DXVec3Minimize</span><span class="sxs-lookup"><span data-stu-id="eff3b-103">D3DXVec3Minimize function</span></span>

<span data-ttu-id="eff3b-104">Возвращает трехмерный вектор, который состоит из наименьших компонентов двух трехмерных векторов.</span><span class="sxs-lookup"><span data-stu-id="eff3b-104">Returns a 3D vector that is made up of the smallest components of two 3D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="eff3b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="eff3b-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Minimize(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="eff3b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="eff3b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eff3b-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="eff3b-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="eff3b-108">Тип: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="eff3b-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="eff3b-109">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="eff3b-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="eff3b-110">*pV1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="eff3b-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eff3b-111">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="eff3b-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="eff3b-112">Указатель на исходную структуру [**D3DXVECTOR3**](d3dxvector3.md) .</span><span class="sxs-lookup"><span data-stu-id="eff3b-112">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="eff3b-113">*pV2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="eff3b-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eff3b-114">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="eff3b-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="eff3b-115">Указатель на исходную структуру [**D3DXVECTOR3**](d3dxvector3.md) .</span><span class="sxs-lookup"><span data-stu-id="eff3b-115">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eff3b-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="eff3b-116">Return value</span></span>

<span data-ttu-id="eff3b-117">Тип: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="eff3b-117">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="eff3b-118">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , которая состоит из наименьших компонентов двух векторов.</span><span class="sxs-lookup"><span data-stu-id="eff3b-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is made up of the smallest components of the two vectors.</span></span>

## <a name="remarks"></a><span data-ttu-id="eff3b-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="eff3b-119">Remarks</span></span>

<span data-ttu-id="eff3b-120">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="eff3b-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="eff3b-121">Таким образом, функция **D3DXVec3Minimize** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="eff3b-121">In this way, the **D3DXVec3Minimize** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="eff3b-122">Требования</span><span class="sxs-lookup"><span data-stu-id="eff3b-122">Requirements</span></span>



| <span data-ttu-id="eff3b-123">Требование</span><span class="sxs-lookup"><span data-stu-id="eff3b-123">Requirement</span></span> | <span data-ttu-id="eff3b-124">Значение</span><span class="sxs-lookup"><span data-stu-id="eff3b-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="eff3b-125">Header</span><span class="sxs-lookup"><span data-stu-id="eff3b-125">Header</span></span><br/>  | <dl> <span data-ttu-id="eff3b-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="eff3b-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="eff3b-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="eff3b-127">Library</span></span><br/> | <dl> <span data-ttu-id="eff3b-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eff3b-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="eff3b-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="eff3b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eff3b-130">Математические функции</span><span class="sxs-lookup"><span data-stu-id="eff3b-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="eff3b-131">**D3DXVec3Maximize**</span><span class="sxs-lookup"><span data-stu-id="eff3b-131">**D3DXVec3Maximize**</span></span>](d3dxvec3maximize.md)
</dt> </dl>

 

 




