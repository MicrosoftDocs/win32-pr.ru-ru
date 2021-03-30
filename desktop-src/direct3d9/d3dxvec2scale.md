---
description: Масштабирует 2D-вектор.
ms.assetid: 1887bc48-3766-42d7-840b-1e29d78db4ce
title: Функция D3DXVec2Scale (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Scale
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 941e85763b15724e3c810c0416b5b142c9d95913
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354600"
---
# <a name="d3dxvec2scale-function"></a><span data-ttu-id="7e950-103">Функция D3DXVec2Scale</span><span class="sxs-lookup"><span data-stu-id="7e950-103">D3DXVec2Scale function</span></span>

<span data-ttu-id="7e950-104">Масштабирует 2D-вектор.</span><span class="sxs-lookup"><span data-stu-id="7e950-104">Scales a 2D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e950-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7e950-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2Scale(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a><span data-ttu-id="7e950-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7e950-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e950-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="7e950-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7e950-108">Тип: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="7e950-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="7e950-109">Указатель на структуру [**D3DXVECTOR2**](d3dxvector2.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="7e950-109">Pointer to the [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="7e950-110">*ПС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7e950-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e950-111">Тип: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="7e950-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="7e950-112">Указатель на исходную структуру [**D3DXVECTOR2**](d3dxvector2.md) .</span><span class="sxs-lookup"><span data-stu-id="7e950-112">Pointer to the source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="7e950-113">*s* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="7e950-113">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e950-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7e950-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7e950-115">Значение масштабирования.</span><span class="sxs-lookup"><span data-stu-id="7e950-115">Scaling value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e950-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7e950-116">Return value</span></span>

<span data-ttu-id="7e950-117">Тип: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="7e950-117">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="7e950-118">Указатель на структуру [**D3DXVECTOR2**](d3dxvector2.md) , которая является масштабируемым вектором.</span><span class="sxs-lookup"><span data-stu-id="7e950-118">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that is the scaled vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e950-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7e950-119">Remarks</span></span>

<span data-ttu-id="7e950-120">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="7e950-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="7e950-121">Таким образом, функция **D3DXVec2Scale** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="7e950-121">In this way, the **D3DXVec2Scale** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e950-122">Требования</span><span class="sxs-lookup"><span data-stu-id="7e950-122">Requirements</span></span>



| <span data-ttu-id="7e950-123">Требование</span><span class="sxs-lookup"><span data-stu-id="7e950-123">Requirement</span></span> | <span data-ttu-id="7e950-124">Значение</span><span class="sxs-lookup"><span data-stu-id="7e950-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7e950-125">Header</span><span class="sxs-lookup"><span data-stu-id="7e950-125">Header</span></span><br/>  | <dl> <span data-ttu-id="7e950-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e950-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="7e950-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7e950-127">Library</span></span><br/> | <dl> <span data-ttu-id="7e950-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7e950-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7e950-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7e950-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e950-130">Математические функции</span><span class="sxs-lookup"><span data-stu-id="7e950-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="7e950-131">**D3DXVec2Add**</span><span class="sxs-lookup"><span data-stu-id="7e950-131">**D3DXVec2Add**</span></span>](d3dxvec2add.md)
</dt> <dt>

[<span data-ttu-id="7e950-132">**D3DXVec2Subtract**</span><span class="sxs-lookup"><span data-stu-id="7e950-132">**D3DXVec2Subtract**</span></span>](d3dxvec2subtract.md)
</dt> </dl>

 

 
