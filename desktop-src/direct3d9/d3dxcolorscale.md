---
description: Масштабирует значение цвета.
ms.assetid: 35e8adee-7ce5-4db5-8276-f0e408748e78
title: Функция D3DXColorScale (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorScale
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 74020f302a26162df1e42cb4c9f020af3f64e59c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105674731"
---
# <a name="d3dxcolorscale-function"></a><span data-ttu-id="d16df-103">Функция D3DXColorScale</span><span class="sxs-lookup"><span data-stu-id="d16df-103">D3DXColorScale function</span></span>

<span data-ttu-id="d16df-104">Масштабирует значение цвета.</span><span class="sxs-lookup"><span data-stu-id="d16df-104">Scales a color value.</span></span>

## <a name="syntax"></a><span data-ttu-id="d16df-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d16df-105">Syntax</span></span>


```C++
D3DXCOLOR* D3DXColorScale(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC,
  _In_          FLOAT     s
);
```



## <a name="parameters"></a><span data-ttu-id="d16df-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d16df-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d16df-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="d16df-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d16df-108">Тип: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="d16df-108">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="d16df-109">Указатель на структуру [**D3DXCOLOR**](d3dxcolor.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="d16df-109">Pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="d16df-110">*ПК* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d16df-110">*pC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d16df-111">Тип: **const [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="d16df-111">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="d16df-112">Указатель на исходную структуру [**D3DXCOLOR**](d3dxcolor.md) .</span><span class="sxs-lookup"><span data-stu-id="d16df-112">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="d16df-113">*s* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="d16df-113">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d16df-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d16df-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d16df-115">Коэффициент масштабирования.</span><span class="sxs-lookup"><span data-stu-id="d16df-115">Scale factor.</span></span> <span data-ttu-id="d16df-116">Он масштабирует цвет, рассматривая его как вектор 4D.</span><span class="sxs-lookup"><span data-stu-id="d16df-116">It scales the color, treating it like a 4D vector.</span></span> <span data-ttu-id="d16df-117">Ограничения на значение s отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="d16df-117">There are no limits on the value of s.</span></span> <span data-ttu-id="d16df-118">Если параметр s имеет значение 1, то результирующим цветом будет исходный цвет.</span><span class="sxs-lookup"><span data-stu-id="d16df-118">If s is 1, the resulting color is the original color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d16df-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d16df-119">Return value</span></span>

<span data-ttu-id="d16df-120">Тип: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="d16df-120">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="d16df-121">Эта функция возвращает указатель на структуру [**D3DXCOLOR**](d3dxcolor.md) , которая является масштабируемым значением цвета.</span><span class="sxs-lookup"><span data-stu-id="d16df-121">This function returns a pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the scaled color value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d16df-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d16df-122">Remarks</span></span>

<span data-ttu-id="d16df-123">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="d16df-123">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="d16df-124">Таким образом, функция **D3DXColorScale** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="d16df-124">In this way, the **D3DXColorScale** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="d16df-125">Эта функция вычисляет масштабированное значение цвета, умножая компоненты цвета структуры [**D3DXCOLOR**](d3dxcolor.md) на заданный коэффициент масштабирования, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="d16df-125">This function computes the scaled color value by multiplying the color components of the [**D3DXCOLOR**](d3dxcolor.md) structure by the specified scale factor, as shown in the following example.</span></span>


```
pOut->r = pC->r * s;
```



## <a name="requirements"></a><span data-ttu-id="d16df-126">Требования</span><span class="sxs-lookup"><span data-stu-id="d16df-126">Requirements</span></span>



| <span data-ttu-id="d16df-127">Требование</span><span class="sxs-lookup"><span data-stu-id="d16df-127">Requirement</span></span> | <span data-ttu-id="d16df-128">Значение</span><span class="sxs-lookup"><span data-stu-id="d16df-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d16df-129">Header</span><span class="sxs-lookup"><span data-stu-id="d16df-129">Header</span></span><br/>  | <dl> <span data-ttu-id="d16df-130"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="d16df-130"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="d16df-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d16df-131">Library</span></span><br/> | <dl> <span data-ttu-id="d16df-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d16df-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d16df-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d16df-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d16df-134">Математические функции</span><span class="sxs-lookup"><span data-stu-id="d16df-134">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="d16df-135">**D3DXColorLerp**</span><span class="sxs-lookup"><span data-stu-id="d16df-135">**D3DXColorLerp**</span></span>](d3dxcolorlerp.md)
</dt> <dt>

[<span data-ttu-id="d16df-136">**D3DXColorModulate**</span><span class="sxs-lookup"><span data-stu-id="d16df-136">**D3DXColorModulate**</span></span>](d3dxcolormodulate.md)
</dt> <dt>

[<span data-ttu-id="d16df-137">**D3DXColorNegative**</span><span class="sxs-lookup"><span data-stu-id="d16df-137">**D3DXColorNegative**</span></span>](d3dxcolornegative.md)
</dt> </dl>

 

 
