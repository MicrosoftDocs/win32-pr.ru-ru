---
description: Выполняет линейную интерполяцию между двумя 2D-векторами.
ms.assetid: f8e9e6be-9696-4a4a-a6c8-c021985decaa
title: Функция D3DXVec2Lerp (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Lerp
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b08b767993143db3057985140b97854b9203d2b5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703722"
---
# <a name="d3dxvec2lerp-function"></a><span data-ttu-id="9f94e-103">Функция D3DXVec2Lerp</span><span class="sxs-lookup"><span data-stu-id="9f94e-103">D3DXVec2Lerp function</span></span>

<span data-ttu-id="9f94e-104">Выполняет линейную интерполяцию между двумя 2D-векторами.</span><span class="sxs-lookup"><span data-stu-id="9f94e-104">Performs a linear interpolation between two 2D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f94e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9f94e-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2Lerp(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV1,
  _In_    const D3DXVECTOR2 *pV2,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a><span data-ttu-id="9f94e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9f94e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f94e-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="9f94e-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9f94e-108">Тип: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="9f94e-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="9f94e-109">Указатель на структуру [**D3DXVECTOR2**](d3dxvector2.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="9f94e-109">Pointer to the [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="9f94e-110">*pV1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9f94e-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f94e-111">Тип: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="9f94e-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="9f94e-112">Указатель на исходную структуру [**D3DXVECTOR2**](d3dxvector2.md) .</span><span class="sxs-lookup"><span data-stu-id="9f94e-112">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="9f94e-113">*pV2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9f94e-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f94e-114">Тип: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="9f94e-114">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="9f94e-115">Указатель на исходную структуру [**D3DXVECTOR2**](d3dxvector2.md) .</span><span class="sxs-lookup"><span data-stu-id="9f94e-115">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="9f94e-116">*s* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="9f94e-116">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f94e-117">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9f94e-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9f94e-118">Параметр, который линейно выполняет интерполяцию между векторами.</span><span class="sxs-lookup"><span data-stu-id="9f94e-118">Parameter that linearly interpolates between the vectors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f94e-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9f94e-119">Return value</span></span>

<span data-ttu-id="9f94e-120">Тип: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="9f94e-120">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="9f94e-121">Указатель на структуру [**D3DXVECTOR2**](d3dxvector2.md) , которая является результатом линейной интерполяции.</span><span class="sxs-lookup"><span data-stu-id="9f94e-121">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the linear interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f94e-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9f94e-122">Remarks</span></span>

<span data-ttu-id="9f94e-123">Эта функция выполняет линейную интерполяцию на основе следующей формулы: v1 + s (V2-v1).</span><span class="sxs-lookup"><span data-stu-id="9f94e-123">This function performs the linear interpolation based on the following formula: V1 + s(V2-V1).</span></span>

<span data-ttu-id="9f94e-124">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="9f94e-124">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="9f94e-125">Таким образом, функция **D3DXVec2Lerp** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="9f94e-125">In this way, the **D3DXVec2Lerp** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f94e-126">Требования</span><span class="sxs-lookup"><span data-stu-id="9f94e-126">Requirements</span></span>



| <span data-ttu-id="9f94e-127">Требование</span><span class="sxs-lookup"><span data-stu-id="9f94e-127">Requirement</span></span> | <span data-ttu-id="9f94e-128">Значение</span><span class="sxs-lookup"><span data-stu-id="9f94e-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9f94e-129">Header</span><span class="sxs-lookup"><span data-stu-id="9f94e-129">Header</span></span><br/>  | <dl> <span data-ttu-id="9f94e-130"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f94e-130"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="9f94e-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9f94e-131">Library</span></span><br/> | <dl> <span data-ttu-id="9f94e-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9f94e-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9f94e-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9f94e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f94e-134">Математические функции</span><span class="sxs-lookup"><span data-stu-id="9f94e-134">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
