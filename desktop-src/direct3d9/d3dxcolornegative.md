---
description: Создает отрицательное значение цвета для значения цвета.
ms.assetid: 74143126-93f8-49fa-abe3-fd730b644d87
title: Функция D3DXColorNegative (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorNegative
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a6d4d8559e64580897aec5261c450dc739496e75
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105674721"
---
# <a name="d3dxcolornegative-function"></a><span data-ttu-id="d74f5-103">Функция D3DXColorNegative</span><span class="sxs-lookup"><span data-stu-id="d74f5-103">D3DXColorNegative function</span></span>

<span data-ttu-id="d74f5-104">Создает отрицательное значение цвета для значения цвета.</span><span class="sxs-lookup"><span data-stu-id="d74f5-104">Creates the negative color value of a color value.</span></span>

## <a name="syntax"></a><span data-ttu-id="d74f5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d74f5-105">Syntax</span></span>


```C++
D3DXCOLOR* D3DXColorNegative(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC
);
```



## <a name="parameters"></a><span data-ttu-id="d74f5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d74f5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d74f5-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="d74f5-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d74f5-108">Тип: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="d74f5-108">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="d74f5-109">Указатель на структуру [**D3DXCOLOR**](d3dxcolor.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="d74f5-109">Pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="d74f5-110">*ПК* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d74f5-110">*pC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d74f5-111">Тип: **const [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="d74f5-111">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="d74f5-112">Указатель на исходную структуру [**D3DXCOLOR**](d3dxcolor.md) .</span><span class="sxs-lookup"><span data-stu-id="d74f5-112">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d74f5-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d74f5-113">Return value</span></span>

<span data-ttu-id="d74f5-114">Тип: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="d74f5-114">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="d74f5-115">Эта функция возвращает указатель на структуру [**D3DXCOLOR**](d3dxcolor.md) , которая является отрицательным значением цвета для значения цвета.</span><span class="sxs-lookup"><span data-stu-id="d74f5-115">This function returns a pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the negative color value of the color value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d74f5-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d74f5-116">Remarks</span></span>

<span data-ttu-id="d74f5-117">Входной альфа-канал копируется, не изменяется, в выходной альфа-канал.</span><span class="sxs-lookup"><span data-stu-id="d74f5-117">The input alpha channel is copied, unmodified, to the output alpha channel.</span></span>

<span data-ttu-id="d74f5-118">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="d74f5-118">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="d74f5-119">Таким образом, функция **D3DXColorNegative** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="d74f5-119">In this way, the **D3DXColorNegative** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="d74f5-120">Эта функция возвращает отрицательное значение цвета, вычитая 1,0 из цветовых компонентов структуры [**D3DXCOLOR**](d3dxcolor.md) , как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="d74f5-120">This function returns the negative color value by subtracting 1.0 from the color components of the [**D3DXCOLOR**](d3dxcolor.md) structure, as shown in the following example.</span></span>


```
pOut->r = 1.0f - pC->r;
```



## <a name="requirements"></a><span data-ttu-id="d74f5-121">Требования</span><span class="sxs-lookup"><span data-stu-id="d74f5-121">Requirements</span></span>



| <span data-ttu-id="d74f5-122">Требование</span><span class="sxs-lookup"><span data-stu-id="d74f5-122">Requirement</span></span> | <span data-ttu-id="d74f5-123">Значение</span><span class="sxs-lookup"><span data-stu-id="d74f5-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d74f5-124">Header</span><span class="sxs-lookup"><span data-stu-id="d74f5-124">Header</span></span><br/>  | <dl> <span data-ttu-id="d74f5-125"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="d74f5-125"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="d74f5-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d74f5-126">Library</span></span><br/> | <dl> <span data-ttu-id="d74f5-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d74f5-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d74f5-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d74f5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d74f5-129">Математические функции</span><span class="sxs-lookup"><span data-stu-id="d74f5-129">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="d74f5-130">**D3DXColorLerp**</span><span class="sxs-lookup"><span data-stu-id="d74f5-130">**D3DXColorLerp**</span></span>](d3dxcolorlerp.md)
</dt> <dt>

[<span data-ttu-id="d74f5-131">**D3DXColorModulate**</span><span class="sxs-lookup"><span data-stu-id="d74f5-131">**D3DXColorModulate**</span></span>](d3dxcolormodulate.md)
</dt> <dt>

[<span data-ttu-id="d74f5-132">**D3DXColorScale**</span><span class="sxs-lookup"><span data-stu-id="d74f5-132">**D3DXColorScale**</span></span>](d3dxcolorscale.md)
</dt> </dl>

 

 




