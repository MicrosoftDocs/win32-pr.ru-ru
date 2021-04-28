---
description: Функция D3DXColorAdjustSaturation (D3dx9math. h) — регулирует значение насыщенности цвета.
ms.assetid: 1f66c3b4-2f02-4993-80c6-c484180c2459
title: Функция D3DXColorAdjustSaturation (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorAdjustSaturation
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 878cdd83a04f594da3133eda314486af96ac3d56
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115872"
---
# <a name="d3dxcoloradjustsaturation-function-d3dx9mathh"></a><span data-ttu-id="99a25-103">Функция D3DXColorAdjustSaturation (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="99a25-103">D3DXColorAdjustSaturation function (D3dx9math.h)</span></span>

<span data-ttu-id="99a25-104">Регулирует значение насыщенности цвета.</span><span class="sxs-lookup"><span data-stu-id="99a25-104">Adjusts the saturation value of a color.</span></span>

## <a name="syntax"></a><span data-ttu-id="99a25-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="99a25-105">Syntax</span></span>


```C++
D3DXCOLOR* D3DXColorAdjustSaturation(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC,
  _In_          FLOAT     s
);
```



## <a name="parameters"></a><span data-ttu-id="99a25-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="99a25-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99a25-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="99a25-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="99a25-108">Тип: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="99a25-108">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="99a25-109">Указатель на структуру [**D3DXCOLOR**](d3dxcolor.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="99a25-109">Pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="99a25-110">*ПК* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="99a25-110">*pC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99a25-111">Тип: **const [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="99a25-111">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="99a25-112">Указатель на исходную структуру [**D3DXCOLOR**](d3dxcolor.md) .</span><span class="sxs-lookup"><span data-stu-id="99a25-112">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="99a25-113">*s* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="99a25-113">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99a25-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="99a25-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="99a25-115">Значение насыщенности.</span><span class="sxs-lookup"><span data-stu-id="99a25-115">Saturation value.</span></span> <span data-ttu-id="99a25-116">Этот параметр линейно выполняет интерполяцию цвета, преобразованного в градации серого, и исходного цвета, ПК.</span><span class="sxs-lookup"><span data-stu-id="99a25-116">This parameter linearly interpolates between the color converted to grayscale and the original color, pC.</span></span> <span data-ttu-id="99a25-117">Ограничения на значение s отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="99a25-117">There are no limits on the value of s.</span></span> <span data-ttu-id="99a25-118">Если параметр s имеет значение 0, то возвращается цвет оттенков серого.</span><span class="sxs-lookup"><span data-stu-id="99a25-118">If s is 0, the returned color is the grayscale color.</span></span> <span data-ttu-id="99a25-119">Если параметр s имеет значение 1, возвращается исходный цвет.</span><span class="sxs-lookup"><span data-stu-id="99a25-119">If s is 1, the returned color is the original color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99a25-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="99a25-120">Return value</span></span>

<span data-ttu-id="99a25-121">Тип: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="99a25-121">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="99a25-122">Эта функция возвращает указатель на структуру [**D3DXCOLOR**](d3dxcolor.md) , которая является результатом корректировки насыщенности.</span><span class="sxs-lookup"><span data-stu-id="99a25-122">This function returns a pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the saturation adjustment.</span></span>

## <a name="remarks"></a><span data-ttu-id="99a25-123">Remarks</span><span class="sxs-lookup"><span data-stu-id="99a25-123">Remarks</span></span>

<span data-ttu-id="99a25-124">Входной альфа-канал копируется, не изменяется, в выходной альфа-канал.</span><span class="sxs-lookup"><span data-stu-id="99a25-124">The input alpha channel is copied, unmodified, to the output alpha channel.</span></span>

<span data-ttu-id="99a25-125">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="99a25-125">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="99a25-126">Таким образом, эта функция может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="99a25-126">In this way, this function can be used as a parameter for another function.</span></span>

<span data-ttu-id="99a25-127">Эта функция интерполирует компоненты красного, зеленого и синего цветов структуры [**D3DXCOLOR**](d3dxcolor.md) между ненасыщенным цветом и цветом, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="99a25-127">This function interpolates the red, green, and blue color components of a [**D3DXCOLOR**](d3dxcolor.md) structure between an unsaturated color and a color, as shown in the following example.</span></span>


```
    // Approximate values for each component's contribution to luminance.
    // Based upon the NTSC standard described in ITU-R Recommendation BT.709.
    FLOAT grey = pC->r * 0.2125f + pC->g * 0.7154f + pC->b * 0.0721f;
    
    pOut->r = grey + s * (pC->r - grey);
```



<span data-ttu-id="99a25-128">Если параметр s больше 0 и меньше 1, насыщенность уменьшается.</span><span class="sxs-lookup"><span data-stu-id="99a25-128">If s is greater than 0 and less than 1, the saturation is decreased.</span></span> <span data-ttu-id="99a25-129">Если параметр s больше 1, увеличивается насыщенность.</span><span class="sxs-lookup"><span data-stu-id="99a25-129">If s is greater than 1, the saturation is increased.</span></span>

<span data-ttu-id="99a25-130">Цвет оттенков серого вычисляются следующим образом:</span><span class="sxs-lookup"><span data-stu-id="99a25-130">The grayscale color is computed as:</span></span>


```
r = g = b = 0.2125*r + 0.7154*g + 0.0721*b
```



## <a name="requirements"></a><span data-ttu-id="99a25-131">Требования</span><span class="sxs-lookup"><span data-stu-id="99a25-131">Requirements</span></span>



| <span data-ttu-id="99a25-132">Требование</span><span class="sxs-lookup"><span data-stu-id="99a25-132">Requirement</span></span> | <span data-ttu-id="99a25-133">Значение</span><span class="sxs-lookup"><span data-stu-id="99a25-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="99a25-134">Header</span><span class="sxs-lookup"><span data-stu-id="99a25-134">Header</span></span><br/>  | <dl> <span data-ttu-id="99a25-135"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="99a25-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="99a25-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="99a25-136">Library</span></span><br/> | <dl> <span data-ttu-id="99a25-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="99a25-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="99a25-138">См. также</span><span class="sxs-lookup"><span data-stu-id="99a25-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99a25-139">Математические функции</span><span class="sxs-lookup"><span data-stu-id="99a25-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="99a25-140">**D3DXColorAdjustContrast**</span><span class="sxs-lookup"><span data-stu-id="99a25-140">**D3DXColorAdjustContrast**</span></span>](d3dxcoloradjustcontrast.md)
</dt> </dl>

 

 
