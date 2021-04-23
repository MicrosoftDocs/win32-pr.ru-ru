---
description: Масштабирует трехмерный вектор.
ms.assetid: b2483d6e-56e4-4557-a603-d59c0767774d
title: Функция D3DXVec3Scale (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Scale
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e5357b862b9cf82e458429edea27001163eb9635
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105704004"
---
# <a name="d3dxvec3scale-function"></a><span data-ttu-id="c3cf6-103">Функция D3DXVec3Scale</span><span class="sxs-lookup"><span data-stu-id="c3cf6-103">D3DXVec3Scale function</span></span>

<span data-ttu-id="c3cf6-104">Масштабирует трехмерный вектор.</span><span class="sxs-lookup"><span data-stu-id="c3cf6-104">Scales a 3D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3cf6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c3cf6-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Scale(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a><span data-ttu-id="c3cf6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c3cf6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3cf6-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="c3cf6-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c3cf6-108">Тип: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="c3cf6-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="c3cf6-109">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="c3cf6-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="c3cf6-110">*ПС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c3cf6-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3cf6-111">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="c3cf6-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="c3cf6-112">Указатель на исходную структуру [**D3DXVECTOR3**](d3dxvector3.md) .</span><span class="sxs-lookup"><span data-stu-id="c3cf6-112">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="c3cf6-113">*s* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="c3cf6-113">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3cf6-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c3cf6-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c3cf6-115">Значение масштабирования.</span><span class="sxs-lookup"><span data-stu-id="c3cf6-115">Scaling value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3cf6-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c3cf6-116">Return value</span></span>

<span data-ttu-id="c3cf6-117">Тип: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="c3cf6-117">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="c3cf6-118">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , которая является масштабируемым вектором.</span><span class="sxs-lookup"><span data-stu-id="c3cf6-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the scaled vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3cf6-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c3cf6-119">Remarks</span></span>

<span data-ttu-id="c3cf6-120">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="c3cf6-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="c3cf6-121">Таким образом, функция **D3DXVec3Scale** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="c3cf6-121">In this way, the **D3DXVec3Scale** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3cf6-122">Требования</span><span class="sxs-lookup"><span data-stu-id="c3cf6-122">Requirements</span></span>



| <span data-ttu-id="c3cf6-123">Требование</span><span class="sxs-lookup"><span data-stu-id="c3cf6-123">Requirement</span></span> | <span data-ttu-id="c3cf6-124">Значение</span><span class="sxs-lookup"><span data-stu-id="c3cf6-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c3cf6-125">Header</span><span class="sxs-lookup"><span data-stu-id="c3cf6-125">Header</span></span><br/>  | <dl> <span data-ttu-id="c3cf6-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3cf6-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="c3cf6-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c3cf6-127">Library</span></span><br/> | <dl> <span data-ttu-id="c3cf6-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c3cf6-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c3cf6-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c3cf6-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3cf6-130">Математические функции</span><span class="sxs-lookup"><span data-stu-id="c3cf6-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="c3cf6-131">**D3DXVec3Add**</span><span class="sxs-lookup"><span data-stu-id="c3cf6-131">**D3DXVec3Add**</span></span>](d3dxvec3add.md)
</dt> <dt>

[<span data-ttu-id="c3cf6-132">**D3DXVec3Subtract**</span><span class="sxs-lookup"><span data-stu-id="c3cf6-132">**D3DXVec3Subtract**</span></span>](d3dxvec3subtract.md)
</dt> </dl>

 

 
