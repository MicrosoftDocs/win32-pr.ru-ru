---
description: Определяет стиль перехода между значениями анимации сетки.
ms.assetid: 4416ef28-ba6b-47ca-be7d-831daad619e5
title: Перечисление D3DXTRANSITION_TYPE (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTRANSITION_TYPE
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 0ca6ef7f9dcee8e865a1cd4089aecd1bc239d5d4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000350"
---
# <a name="d3dxtransition_type-enumeration"></a><span data-ttu-id="9f6af-103">\_Перечисление типов D3DXTRANSITION</span><span class="sxs-lookup"><span data-stu-id="9f6af-103">D3DXTRANSITION\_TYPE enumeration</span></span>

<span data-ttu-id="9f6af-104">Определяет стиль перехода между значениями анимации сетки.</span><span class="sxs-lookup"><span data-stu-id="9f6af-104">Defines the transition style between values of a mesh animation.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f6af-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9f6af-105">Syntax</span></span>


```C++
typedef enum D3DXTRANSITION_TYPE { 
  D3DXTRANSITION_LINEAR         = 0x000,
  D3DXTRANSITION_EASEINEASEOUT  = 0x001,
  D3DXTRANSITION_FORCE_DWORD    = 0x7fffffff
} D3DXTRANSITION_TYPE, *LPD3DXTRANSITION_TYPE;
```



## <a name="constants"></a><span data-ttu-id="9f6af-106">Константы</span><span class="sxs-lookup"><span data-stu-id="9f6af-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="9f6af-107"><span id="D3DXTRANSITION_LINEAR"></span><span id="d3dxtransition_linear"></span>**\_Линейная D3DXTRANSITION**</span><span class="sxs-lookup"><span data-stu-id="9f6af-107"><span id="D3DXTRANSITION_LINEAR"></span><span id="d3dxtransition_linear"></span>**D3DXTRANSITION\_LINEAR**</span></span>
</dt> <dd>

<span data-ttu-id="9f6af-108">Линейный переход между значениями.</span><span class="sxs-lookup"><span data-stu-id="9f6af-108">Linear transition between values.</span></span>

</dd> <dt>

<span data-ttu-id="9f6af-109"><span id="D3DXTRANSITION_EASEINEASEOUT"></span><span id="d3dxtransition_easeineaseout"></span>**D3DXTRANSITION \_ еасеинеасеаут**</span><span class="sxs-lookup"><span data-stu-id="9f6af-109"><span id="D3DXTRANSITION_EASEINEASEOUT"></span><span id="d3dxtransition_easeineaseout"></span>**D3DXTRANSITION\_EASEINEASEOUT**</span></span>
</dt> <dd>

<span data-ttu-id="9f6af-110">Простота, удобство переноса сплайна между значениями.</span><span class="sxs-lookup"><span data-stu-id="9f6af-110">Ease-in, ease-out spline transition between values.</span></span>

</dd> <dt>

<span data-ttu-id="9f6af-111"><span id="D3DXTRANSITION_FORCE_DWORD"></span><span id="d3dxtransition_force_dword"></span>**D3DXTRANSITION \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="9f6af-111"><span id="D3DXTRANSITION_FORCE_DWORD"></span><span id="d3dxtransition_force_dword"></span>**D3DXTRANSITION\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="9f6af-112">Заставляет это перечисление компилироваться до 32 бит в размере.</span><span class="sxs-lookup"><span data-stu-id="9f6af-112">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="9f6af-113">Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит.</span><span class="sxs-lookup"><span data-stu-id="9f6af-113">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="9f6af-114">Это значение не используется.</span><span class="sxs-lookup"><span data-stu-id="9f6af-114">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9f6af-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9f6af-115">Remarks</span></span>

<span data-ttu-id="9f6af-116">Вычисление шкалы с простотой в целях упрощения вычисляется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="9f6af-116">The calculation for the ramp from ease in to ease out is calculated as follows:</span></span>

<dl> <span data-ttu-id="9f6af-117">Q (t) = 2 (x-y) t ³ + 3 (y-x) t ² + x</span><span class="sxs-lookup"><span data-stu-id="9f6af-117">Q(t) = 2(x - y)t³ + 3(y - x)t² + x</span></span>  
</dl>

<span data-ttu-id="9f6af-118">где пандус — это функция Q (t) со следующими свойствами:</span><span class="sxs-lookup"><span data-stu-id="9f6af-118">where the ramp is a function Q(t) with the following properties:</span></span>

-   <span data-ttu-id="9f6af-119">Q (t) — это Кубический сплайн.</span><span class="sxs-lookup"><span data-stu-id="9f6af-119">Q(t) is a cubic spline.</span></span>
-   <span data-ttu-id="9f6af-120">Q (t) выполняет интерполяцию между x и y в диапазоне от 0 до 1.</span><span class="sxs-lookup"><span data-stu-id="9f6af-120">Q(t) interpolates between x and y as t ranges from 0 to 1.</span></span>
-   <span data-ttu-id="9f6af-121">Q (t) является горизонтальным, когда t = 0 и t = 1.</span><span class="sxs-lookup"><span data-stu-id="9f6af-121">Q(t) is horizontal when t = 0 and t = 1.</span></span>

<span data-ttu-id="9f6af-122">Математически, это преобразуется в:</span><span class="sxs-lookup"><span data-stu-id="9f6af-122">Mathematically, this translates into:</span></span>

<dl> <span data-ttu-id="9f6af-123">Q (t) = at ³ + BT ² + CT + D (и, следовательно, Q ' (t) = 3At ² + 2Bt + C)</span><span class="sxs-lookup"><span data-stu-id="9f6af-123">Q(t) = At³ + Bt² + Ct + D (and therefore, Q'(t) = 3At² + 2Bt + C)</span></span>  
<span data-ttu-id="9f6af-124">2a) Q (0) = x</span><span class="sxs-lookup"><span data-stu-id="9f6af-124">2a) Q(0) = x</span></span>  
<span data-ttu-id="9f6af-125">2b) Q (1) = y</span><span class="sxs-lookup"><span data-stu-id="9f6af-125">2b) Q(1) = y</span></span>  
<span data-ttu-id="9f6af-126">3a) Q "(0) = 0</span><span class="sxs-lookup"><span data-stu-id="9f6af-126">3a) Q'(0) = 0</span></span>  
<span data-ttu-id="9f6af-127">3b) Q ' (1) = 0</span><span class="sxs-lookup"><span data-stu-id="9f6af-127">3b) Q'(1) = 0</span></span>  
</dl>

<span data-ttu-id="9f6af-128">Решение для A, B, C, D:</span><span class="sxs-lookup"><span data-stu-id="9f6af-128">Solving for A, B, C, D:</span></span>

<dl> <span data-ttu-id="9f6af-129">D = x (от 2A)</span><span class="sxs-lookup"><span data-stu-id="9f6af-129">D = x (from 2a)</span></span>  
<span data-ttu-id="9f6af-130">C = 0 (из 3a)</span><span class="sxs-lookup"><span data-stu-id="9f6af-130">C = 0 (from 3a)</span></span>  
<span data-ttu-id="9f6af-131">3A + 2B = 0 (от 3b)</span><span class="sxs-lookup"><span data-stu-id="9f6af-131">3A + 2B = 0 (from 3b)</span></span>  
<span data-ttu-id="9f6af-132">A + B = y-x (от 2b до D = x)</span><span class="sxs-lookup"><span data-stu-id="9f6af-132">A + B = y - x (from 2b and D = x)</span></span>  
</dl>

<span data-ttu-id="9f6af-133">Таким образом:</span><span class="sxs-lookup"><span data-stu-id="9f6af-133">Therefore:</span></span>

<dl> <span data-ttu-id="9f6af-134">A = 2 (x-y), B = 3 (y-x), C = 0, D = x</span><span class="sxs-lookup"><span data-stu-id="9f6af-134">A = 2(x - y), B = 3(y - x), C = 0, D = x</span></span>  
</dl>

## <a name="requirements"></a><span data-ttu-id="9f6af-135">Требования</span><span class="sxs-lookup"><span data-stu-id="9f6af-135">Requirements</span></span>



| <span data-ttu-id="9f6af-136">Требование</span><span class="sxs-lookup"><span data-stu-id="9f6af-136">Requirement</span></span> | <span data-ttu-id="9f6af-137">Значение</span><span class="sxs-lookup"><span data-stu-id="9f6af-137">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9f6af-138">Header</span><span class="sxs-lookup"><span data-stu-id="9f6af-138">Header</span></span><br/> | <dl> <span data-ttu-id="9f6af-139"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f6af-139"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f6af-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9f6af-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f6af-141">Перечисления D3DX</span><span class="sxs-lookup"><span data-stu-id="9f6af-141">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




