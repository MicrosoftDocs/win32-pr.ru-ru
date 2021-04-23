---
title: Абсолютное значение
description: Получение абсолютного значения исходного операнда, используемого в арифметической операции.
ms.assetid: FD2ACE91-0AF6-43E8-80C5-849488E39BEF
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 27ceefa2c4b4ee2eb890b0692a33266e89a18cfb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104335616"
---
# <a name="absolute-value"></a><span data-ttu-id="1835a-103">Абсолютное значение</span><span class="sxs-lookup"><span data-stu-id="1835a-103">Absolute Value</span></span>

<span data-ttu-id="1835a-104">Получение абсолютного значения исходного операнда, используемого в арифметической операции.</span><span class="sxs-lookup"><span data-stu-id="1835a-104">Take the absolute value of a source operand used in an arithmetic operation.</span></span>



| <span data-ttu-id="1835a-105">\_просто</span><span class="sxs-lookup"><span data-stu-id="1835a-105">\_abs</span></span> |
|-------|



 

<span data-ttu-id="1835a-106">Этот модификатор используется только для одиночной и двойной точности с плавающей запятой и инструкций.</span><span class="sxs-lookup"><span data-stu-id="1835a-106">This modifier is used for single and double precision floating point and instructions only.</span></span> <span data-ttu-id="1835a-107">Модификатор **\_ ABS** вызывает срабатывание знака чисел в исходном операнде, в том числе для значений INF.</span><span class="sxs-lookup"><span data-stu-id="1835a-107">The **\_abs** modifier forces the sign of the number(s) on the source operand positive, including on INF values.</span></span>

<span data-ttu-id="1835a-108">Применение функции **\_ ABS** к NaN сохраняет значение NaN, хотя определенный битовый шаблон NaN не определен.</span><span class="sxs-lookup"><span data-stu-id="1835a-108">Applying **\_abs** on NaN preserves NaN, although the particular NaN bit pattern that results is not defined.</span></span>

<span data-ttu-id="1835a-109">Если \_ ABS сочетается с модификатором [отрицания](negate.md) , это сочетание приводит к тому, что знак будет отрицательным, как если бы первым был применен модификатор **\_ ABS** , а затем — **отрицание**.</span><span class="sxs-lookup"><span data-stu-id="1835a-109">When \_abs is combined with the [negate](negate.md) modifier, the combination forces the sign to be negative, as if the **\_abs** modifier is applied first, then the **negate**.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="1835a-110">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="1835a-110">Minimum Shader Model</span></span>

<span data-ttu-id="1835a-111">Этот модификатор поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="1835a-111">This modifier is supported in the following shader models.</span></span>



| <span data-ttu-id="1835a-112">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="1835a-112">Shader Model</span></span>                                              | <span data-ttu-id="1835a-113">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="1835a-113">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="1835a-114">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="1835a-114">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="1835a-115">да</span><span class="sxs-lookup"><span data-stu-id="1835a-115">yes</span></span>       |
| [<span data-ttu-id="1835a-116">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="1835a-116">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="1835a-117">да</span><span class="sxs-lookup"><span data-stu-id="1835a-117">yes</span></span>       |
| [<span data-ttu-id="1835a-118">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="1835a-118">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="1835a-119">да</span><span class="sxs-lookup"><span data-stu-id="1835a-119">yes</span></span>       |
| [<span data-ttu-id="1835a-120">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1835a-120">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="1835a-121">Нет</span><span class="sxs-lookup"><span data-stu-id="1835a-121">no</span></span>        |
| [<span data-ttu-id="1835a-122">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1835a-122">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="1835a-123">Нет</span><span class="sxs-lookup"><span data-stu-id="1835a-123">no</span></span>        |
| [<span data-ttu-id="1835a-124">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1835a-124">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="1835a-125">Нет</span><span class="sxs-lookup"><span data-stu-id="1835a-125">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="1835a-126">См. также</span><span class="sxs-lookup"><span data-stu-id="1835a-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1835a-127">Модификаторы инструкций</span><span class="sxs-lookup"><span data-stu-id="1835a-127">Instruction Modifiers</span></span>](instruction-modifiers.md)
</dt> </dl>

 

 




