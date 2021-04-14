---
description: Корректирует значение контрастности цвета.
ms.assetid: c111d3c7-19c6-4a6b-af0d-a9e1bc0bb7d9
title: Функция D3DXColorAdjustContrast (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorAdjustContrast
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 24586b2a8d2206d6818e00af9ea86e4c5e9758fa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105647873"
---
# <a name="d3dxcoloradjustcontrast-function-d3dx10mathh"></a><span data-ttu-id="5d183-103">Функция D3DXColorAdjustContrast (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="5d183-103">D3DXColorAdjustContrast function (D3DX10Math.h)</span></span>

<span data-ttu-id="5d183-104">Корректирует значение контрастности цвета.</span><span class="sxs-lookup"><span data-stu-id="5d183-104">Adjusts the contrast value of a color.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d183-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5d183-105">Syntax</span></span>


```C++
D3DXCOLOR* D3DXColorAdjustContrast(
  _In_       D3DXCOLOR *pOut,
  _In_ const D3DXCOLOR *pC,
  _In_       FLOAT     c
);
```



## <a name="parameters"></a><span data-ttu-id="5d183-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5d183-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d183-107">*тоска* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5d183-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d183-108">Тип: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="5d183-108">Type: **[**D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***</span></span>

<span data-ttu-id="5d183-109">\[в указатель out \] на [**D3DXCOLOR**](d3d10-d3dxcolor.md) , который является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="5d183-109">\[in, out\] Pointer to a [**D3DXCOLOR**](d3d10-d3dxcolor.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="5d183-110">*ПК* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5d183-110">*pC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d183-111">Тип: **const [**D3DXCOLOR**](../direct3d9/d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="5d183-111">Type: **const [**D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***</span></span>

<span data-ttu-id="5d183-112">Указатель на исходную структуру D3DXCOLOR.</span><span class="sxs-lookup"><span data-stu-id="5d183-112">Pointer to a source D3DXCOLOR structure.</span></span>

</dd> <dt>

<span data-ttu-id="5d183-113">*c* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="5d183-113">*c* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d183-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5d183-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5d183-115">Значение контрастности.</span><span class="sxs-lookup"><span data-stu-id="5d183-115">Contrast value.</span></span> <span data-ttu-id="5d183-116">Этот параметр линейно выполняет интерполяцию между 50% серого и цветом, ПК.</span><span class="sxs-lookup"><span data-stu-id="5d183-116">This parameter linearly interpolates between fifty percent gray and the color, pC.</span></span> <span data-ttu-id="5d183-117">Нет ограничений на значение в.</span><span class="sxs-lookup"><span data-stu-id="5d183-117">There are no limits on the value of c.</span></span> <span data-ttu-id="5d183-118">Если этот параметр равен нулю, возвращается цвет 50% серого цвета.</span><span class="sxs-lookup"><span data-stu-id="5d183-118">If this parameter is zero, then the returned color is fifty percent gray.</span></span> <span data-ttu-id="5d183-119">Если этот параметр равен 1, то возвращенным цветом будет исходный цвет.</span><span class="sxs-lookup"><span data-stu-id="5d183-119">If this parameter is 1, then the returned color is the original color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d183-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5d183-120">Return value</span></span>

<span data-ttu-id="5d183-121">Тип: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="5d183-121">Type: **[**D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***</span></span>

<span data-ttu-id="5d183-122">Эта функция возвращает указатель на структуру D3DXCOLOR, которая является результатом корректировки контрастности.</span><span class="sxs-lookup"><span data-stu-id="5d183-122">This function returns a pointer to a D3DXCOLOR structure that is the result of the contrast adjustment.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d183-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5d183-123">Remarks</span></span>

<span data-ttu-id="5d183-124">Входной альфа-канал копируется, не изменяется, в выходной альфа-канал.</span><span class="sxs-lookup"><span data-stu-id="5d183-124">The input alpha channel is copied, unmodified, to the output alpha channel.</span></span>

<span data-ttu-id="5d183-125">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="5d183-125">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="5d183-126">Таким образом, эта функция может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="5d183-126">In this way, this function can be used as a parameter for another function.</span></span>

<span data-ttu-id="5d183-127">Эта функция интерполирует компоненты красного, зеленого и синего цветов структуры D3DXCOLOR в диапазоне от 50% серого до указанного значения контраста, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="5d183-127">This function interpolates the red, green, and blue color components of a D3DXCOLOR structure between fifty percent gray and a specified contrast value, as shown in the following example.</span></span>


```
pOut->r = 0.5f + c * (pC->r - 0.5f);
```



<span data-ttu-id="5d183-128">Если c больше 0 и меньше 1, контрастность уменьшается.</span><span class="sxs-lookup"><span data-stu-id="5d183-128">If c is greater than 0 and less than 1, the contrast is decreased.</span></span> <span data-ttu-id="5d183-129">Если c больше 1, контрастность увеличивается.</span><span class="sxs-lookup"><span data-stu-id="5d183-129">If c is greater than 1, the contrast is increased.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d183-130">Требования</span><span class="sxs-lookup"><span data-stu-id="5d183-130">Requirements</span></span>



| <span data-ttu-id="5d183-131">Требование</span><span class="sxs-lookup"><span data-stu-id="5d183-131">Requirement</span></span> | <span data-ttu-id="5d183-132">Значение</span><span class="sxs-lookup"><span data-stu-id="5d183-132">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5d183-133">Header</span><span class="sxs-lookup"><span data-stu-id="5d183-133">Header</span></span><br/>  | <dl> <span data-ttu-id="5d183-134"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d183-134"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="5d183-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5d183-135">Library</span></span><br/> | <dl> <span data-ttu-id="5d183-136"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5d183-136"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5d183-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5d183-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d183-138">Математические функции</span><span class="sxs-lookup"><span data-stu-id="5d183-138">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
