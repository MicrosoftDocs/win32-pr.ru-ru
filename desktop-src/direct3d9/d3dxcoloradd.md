---
description: Складывает два значения цвета для создания нового значения цвета.
ms.assetid: 7743392d-4676-4408-93e9-f92d4bf02411
title: Функция D3DXColorAdd (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorAdd
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f326c9bec4802a9a94accc76b825cd1c6ea28fd5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105674733"
---
# <a name="d3dxcoloradd-function"></a><span data-ttu-id="c2be1-103">Функция D3DXColorAdd</span><span class="sxs-lookup"><span data-stu-id="c2be1-103">D3DXColorAdd function</span></span>

<span data-ttu-id="c2be1-104">Складывает два значения цвета для создания нового значения цвета.</span><span class="sxs-lookup"><span data-stu-id="c2be1-104">Adds two color values together to create a new color value.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2be1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c2be1-105">Syntax</span></span>


```C++
D3DXCOLOR* D3DXColorAdd(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC1,
  _In_    const D3DXCOLOR *pC2
);
```



## <a name="parameters"></a><span data-ttu-id="c2be1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c2be1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2be1-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="c2be1-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c2be1-108">Тип: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="c2be1-108">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="c2be1-109">Указатель на структуру [**D3DXCOLOR**](d3dxcolor.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="c2be1-109">Pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="c2be1-110">*pC1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c2be1-110">*pC1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2be1-111">Тип: **const [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="c2be1-111">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="c2be1-112">Указатель на исходную структуру [**D3DXCOLOR**](d3dxcolor.md) .</span><span class="sxs-lookup"><span data-stu-id="c2be1-112">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="c2be1-113">*pC2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c2be1-113">*pC2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2be1-114">Тип: **const [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="c2be1-114">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="c2be1-115">Указатель на исходную структуру [**D3DXCOLOR**](d3dxcolor.md) .</span><span class="sxs-lookup"><span data-stu-id="c2be1-115">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2be1-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c2be1-116">Return value</span></span>

<span data-ttu-id="c2be1-117">Тип: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="c2be1-117">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="c2be1-118">Эта функция возвращает указатель на структуру [**D3DXCOLOR**](d3dxcolor.md) , которая является суммой значений двух цветов.</span><span class="sxs-lookup"><span data-stu-id="c2be1-118">This function returns a pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the sum of two color values.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2be1-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c2be1-119">Remarks</span></span>

<span data-ttu-id="c2be1-120">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в тоска.</span><span class="sxs-lookup"><span data-stu-id="c2be1-120">The return value for this function is the same value returned in pOut.</span></span> <span data-ttu-id="c2be1-121">Таким образом, функция **D3DXColorAdd** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="c2be1-121">In this way, the **D3DXColorAdd** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2be1-122">Требования</span><span class="sxs-lookup"><span data-stu-id="c2be1-122">Requirements</span></span>



| <span data-ttu-id="c2be1-123">Требование</span><span class="sxs-lookup"><span data-stu-id="c2be1-123">Requirement</span></span> | <span data-ttu-id="c2be1-124">Значение</span><span class="sxs-lookup"><span data-stu-id="c2be1-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c2be1-125">Header</span><span class="sxs-lookup"><span data-stu-id="c2be1-125">Header</span></span><br/>  | <dl> <span data-ttu-id="c2be1-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2be1-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="c2be1-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c2be1-127">Library</span></span><br/> | <dl> <span data-ttu-id="c2be1-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c2be1-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c2be1-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c2be1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2be1-130">Математические функции</span><span class="sxs-lookup"><span data-stu-id="c2be1-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="c2be1-131">**D3DXColorModulate**</span><span class="sxs-lookup"><span data-stu-id="c2be1-131">**D3DXColorModulate**</span></span>](d3dxcolormodulate.md)
</dt> <dt>

[<span data-ttu-id="c2be1-132">**D3DXColorSubtract**</span><span class="sxs-lookup"><span data-stu-id="c2be1-132">**D3DXColorSubtract**</span></span>](d3dxcolorsubtract.md)
</dt> </dl>

 

 




