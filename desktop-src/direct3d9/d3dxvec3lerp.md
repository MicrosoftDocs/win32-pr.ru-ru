---
description: Выполняет линейную интерполяцию между двумя трехмерными векторами.
ms.assetid: f3f06f1b-8824-47f0-b2ed-c212fa4c3225
title: Функция D3DXVec3Lerp (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Lerp
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ed6905cc0b13908a4e60e221737e9b5dc5a627f1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105714006"
---
# <a name="d3dxvec3lerp-function"></a><span data-ttu-id="465c5-103">Функция D3DXVec3Lerp</span><span class="sxs-lookup"><span data-stu-id="465c5-103">D3DXVec3Lerp function</span></span>

<span data-ttu-id="465c5-104">Выполняет линейную интерполяцию между двумя трехмерными векторами.</span><span class="sxs-lookup"><span data-stu-id="465c5-104">Performs a linear interpolation between two 3D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="465c5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="465c5-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Lerp(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a><span data-ttu-id="465c5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="465c5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="465c5-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="465c5-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="465c5-108">Тип: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="465c5-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="465c5-109">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="465c5-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="465c5-110">*pV1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="465c5-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="465c5-111">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="465c5-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="465c5-112">Указатель на исходную структуру [**D3DXVECTOR3**](d3dxvector3.md) .</span><span class="sxs-lookup"><span data-stu-id="465c5-112">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="465c5-113">*pV2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="465c5-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="465c5-114">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="465c5-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="465c5-115">Указатель на исходную структуру [**D3DXVECTOR3**](d3dxvector3.md) .</span><span class="sxs-lookup"><span data-stu-id="465c5-115">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="465c5-116">*s* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="465c5-116">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="465c5-117">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="465c5-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="465c5-118">Параметр, который линейно выполняет интерполяцию между векторами.</span><span class="sxs-lookup"><span data-stu-id="465c5-118">Parameter that linearly interpolates between the vectors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="465c5-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="465c5-119">Return value</span></span>

<span data-ttu-id="465c5-120">Тип: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="465c5-120">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="465c5-121">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , которая является результатом линейной интерполяции.</span><span class="sxs-lookup"><span data-stu-id="465c5-121">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the linear interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="465c5-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="465c5-122">Remarks</span></span>

<span data-ttu-id="465c5-123">Эта функция выполняет линейную интерполяцию на основе следующей формулы: v1 + s (V2-v1).</span><span class="sxs-lookup"><span data-stu-id="465c5-123">This function performs the linear interpolation based on the following formula: V1 + s(V2-V1).</span></span>

<span data-ttu-id="465c5-124">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="465c5-124">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="465c5-125">Таким образом, функция **D3DXVec3Lerp** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="465c5-125">In this way, the **D3DXVec3Lerp** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="465c5-126">Требования</span><span class="sxs-lookup"><span data-stu-id="465c5-126">Requirements</span></span>



| <span data-ttu-id="465c5-127">Требование</span><span class="sxs-lookup"><span data-stu-id="465c5-127">Requirement</span></span> | <span data-ttu-id="465c5-128">Значение</span><span class="sxs-lookup"><span data-stu-id="465c5-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="465c5-129">Header</span><span class="sxs-lookup"><span data-stu-id="465c5-129">Header</span></span><br/>  | <dl> <span data-ttu-id="465c5-130"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="465c5-130"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="465c5-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="465c5-131">Library</span></span><br/> | <dl> <span data-ttu-id="465c5-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="465c5-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="465c5-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="465c5-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="465c5-134">Математические функции</span><span class="sxs-lookup"><span data-stu-id="465c5-134">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
