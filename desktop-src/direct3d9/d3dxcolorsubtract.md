---
description: Вычитает два значения цвета для создания нового значения цвета.
ms.assetid: c21f8402-c1c2-4909-896f-2872ef518537
title: Функция D3DXColorSubtract (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorSubtract
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 47f28ea3a3fb6d1556e699fed3820e228faf6604
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713749"
---
# <a name="d3dxcolorsubtract-function"></a><span data-ttu-id="10ecb-103">Функция D3DXColorSubtract</span><span class="sxs-lookup"><span data-stu-id="10ecb-103">D3DXColorSubtract function</span></span>

<span data-ttu-id="10ecb-104">Вычитает два значения цвета для создания нового значения цвета.</span><span class="sxs-lookup"><span data-stu-id="10ecb-104">Subtracts two color values to create a new color value.</span></span>

## <a name="syntax"></a><span data-ttu-id="10ecb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="10ecb-105">Syntax</span></span>


```C++
D3DXCOLOR* D3DXColorSubtract(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC1,
  _In_    const D3DXCOLOR *pC2
);
```



## <a name="parameters"></a><span data-ttu-id="10ecb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="10ecb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10ecb-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="10ecb-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="10ecb-108">Тип: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="10ecb-108">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="10ecb-109">Указатель на структуру [**D3DXCOLOR**](d3dxcolor.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="10ecb-109">Pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="10ecb-110">*pC1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="10ecb-110">*pC1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10ecb-111">Тип: **const [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="10ecb-111">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="10ecb-112">Указатель на исходную структуру [**D3DXCOLOR**](d3dxcolor.md) .</span><span class="sxs-lookup"><span data-stu-id="10ecb-112">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="10ecb-113">*pC2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="10ecb-113">*pC2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10ecb-114">Тип: **const [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="10ecb-114">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="10ecb-115">Указатель на исходную структуру [**D3DXCOLOR**](d3dxcolor.md) .</span><span class="sxs-lookup"><span data-stu-id="10ecb-115">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10ecb-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="10ecb-116">Return value</span></span>

<span data-ttu-id="10ecb-117">Тип: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="10ecb-117">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="10ecb-118">Эта функция возвращает указатель на структуру [**D3DXCOLOR**](d3dxcolor.md) , которая является разностью между двумя значениями цвета.</span><span class="sxs-lookup"><span data-stu-id="10ecb-118">This function returns a pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the difference between two color values.</span></span>

## <a name="remarks"></a><span data-ttu-id="10ecb-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="10ecb-119">Remarks</span></span>

<span data-ttu-id="10ecb-120">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="10ecb-120">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="10ecb-121">Таким образом, функция **D3DXColorSubtract** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="10ecb-121">In this way, the **D3DXColorSubtract** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="10ecb-122">Требования</span><span class="sxs-lookup"><span data-stu-id="10ecb-122">Requirements</span></span>



| <span data-ttu-id="10ecb-123">Требование</span><span class="sxs-lookup"><span data-stu-id="10ecb-123">Requirement</span></span> | <span data-ttu-id="10ecb-124">Значение</span><span class="sxs-lookup"><span data-stu-id="10ecb-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="10ecb-125">Header</span><span class="sxs-lookup"><span data-stu-id="10ecb-125">Header</span></span><br/>  | <dl> <span data-ttu-id="10ecb-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="10ecb-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="10ecb-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="10ecb-127">Library</span></span><br/> | <dl> <span data-ttu-id="10ecb-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="10ecb-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="10ecb-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="10ecb-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10ecb-130">Математические функции</span><span class="sxs-lookup"><span data-stu-id="10ecb-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="10ecb-131">**D3DXColorAdd**</span><span class="sxs-lookup"><span data-stu-id="10ecb-131">**D3DXColorAdd**</span></span>](d3dxcoloradd.md)
</dt> </dl>

 

 




