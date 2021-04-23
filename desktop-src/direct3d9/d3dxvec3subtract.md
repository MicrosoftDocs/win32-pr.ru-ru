---
description: Вычитает два трехмерных вектора.
ms.assetid: 09e2cede-a0a3-4a5e-a7e1-e7a98cdc433b
title: Функция D3DXVec3Subtract (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Subtract
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 17f41f2fd133db1064e2ba2778eacc139bab01ca
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273967"
---
# <a name="d3dxvec3subtract-function"></a><span data-ttu-id="5d2e7-103">Функция D3DXVec3Subtract</span><span class="sxs-lookup"><span data-stu-id="5d2e7-103">D3DXVec3Subtract function</span></span>

<span data-ttu-id="5d2e7-104">Вычитает два трехмерных вектора.</span><span class="sxs-lookup"><span data-stu-id="5d2e7-104">Subtracts two 3D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d2e7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5d2e7-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Subtract(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="5d2e7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5d2e7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d2e7-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="5d2e7-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5d2e7-108">Тип: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="5d2e7-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="5d2e7-109">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="5d2e7-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="5d2e7-110">*pV1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5d2e7-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d2e7-111">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="5d2e7-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="5d2e7-112">Указатель на исходную структуру [**D3DXVECTOR3**](d3dxvector3.md) .</span><span class="sxs-lookup"><span data-stu-id="5d2e7-112">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="5d2e7-113">*pV2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5d2e7-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d2e7-114">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="5d2e7-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="5d2e7-115">Указатель на исходную структуру [**D3DXVECTOR3**](d3dxvector3.md) .</span><span class="sxs-lookup"><span data-stu-id="5d2e7-115">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d2e7-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5d2e7-116">Return value</span></span>

<span data-ttu-id="5d2e7-117">Тип: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="5d2e7-117">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="5d2e7-118">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , которая является разностью двух векторов.</span><span class="sxs-lookup"><span data-stu-id="5d2e7-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the difference of two vectors.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d2e7-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5d2e7-119">Remarks</span></span>

<span data-ttu-id="5d2e7-120">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="5d2e7-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="5d2e7-121">Таким образом, функция **D3DXVec3Subtract** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="5d2e7-121">In this way, the **D3DXVec3Subtract** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d2e7-122">Требования</span><span class="sxs-lookup"><span data-stu-id="5d2e7-122">Requirements</span></span>



| <span data-ttu-id="5d2e7-123">Требование</span><span class="sxs-lookup"><span data-stu-id="5d2e7-123">Requirement</span></span> | <span data-ttu-id="5d2e7-124">Значение</span><span class="sxs-lookup"><span data-stu-id="5d2e7-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5d2e7-125">Header</span><span class="sxs-lookup"><span data-stu-id="5d2e7-125">Header</span></span><br/>  | <dl> <span data-ttu-id="5d2e7-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d2e7-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="5d2e7-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5d2e7-127">Library</span></span><br/> | <dl> <span data-ttu-id="5d2e7-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5d2e7-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5d2e7-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5d2e7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d2e7-130">Математические функции</span><span class="sxs-lookup"><span data-stu-id="5d2e7-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="5d2e7-131">**D3DXVec3Add**</span><span class="sxs-lookup"><span data-stu-id="5d2e7-131">**D3DXVec3Add**</span></span>](d3dxvec3add.md)
</dt> <dt>

[<span data-ttu-id="5d2e7-132">**D3DXVec3Scale**</span><span class="sxs-lookup"><span data-stu-id="5d2e7-132">**D3DXVec3Scale**</span></span>](d3dxvec3scale.md)
</dt> </dl>

 

 




