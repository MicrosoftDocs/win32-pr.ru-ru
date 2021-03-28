---
title: Negate
description: Переворачивает знак значения исходного операнда, используемого в арифметической операции.
ms.assetid: 83ef3f61-7b0b-4033-8f7b-5345b205c441
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: cc2637a76b52b28eefcfb3637cc8b2d406c02c06
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104069332"
---
# <a name="negate"></a><span data-ttu-id="74552-103">Negate</span><span class="sxs-lookup"><span data-stu-id="74552-103">Negate</span></span>

<span data-ttu-id="74552-104">Переворачивает знак значения исходного операнда, используемого в арифметической операции.</span><span class="sxs-lookup"><span data-stu-id="74552-104">Flips the sign of the value of a source operand used in an arithmetic operation.</span></span>



| \-  |
|-----|



 

<span data-ttu-id="74552-105">Для одиночной и двойной точности с плавающей запятой модификатор отрицания отражает знак числа в исходном операнде, включая значения INF.</span><span class="sxs-lookup"><span data-stu-id="74552-105">For single and double precision floating point and instructions, the negate modifier flips the sign of the number(s) in the source operand, including on INF values.</span></span> <span data-ttu-id="74552-106">Применение функции **отрицания** для NaN сохраняет NaN, хотя определенный битовый шаблон NaN, который не определен, не определяется.</span><span class="sxs-lookup"><span data-stu-id="74552-106">Applying **negate** on NaN preserves NaN, although the particular NaN bit pattern that results is not defined.</span></span>

<span data-ttu-id="74552-107">Для целочисленных инструкций модификатор **отрицания** принимает значение 2 для чисел в исходном операнде.</span><span class="sxs-lookup"><span data-stu-id="74552-107">For integer instructions, the **negate** modifier takes the 2's complement of the number(s) in the source operand.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="74552-108">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="74552-108">Minimum Shader Model</span></span>

<span data-ttu-id="74552-109">Этот модификатор поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="74552-109">This modifier is supported in the following shader models.</span></span>



| <span data-ttu-id="74552-110">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="74552-110">Shader Model</span></span>                                              | <span data-ttu-id="74552-111">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="74552-111">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="74552-112">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="74552-112">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="74552-113">да</span><span class="sxs-lookup"><span data-stu-id="74552-113">yes</span></span>       |
| [<span data-ttu-id="74552-114">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="74552-114">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="74552-115">да</span><span class="sxs-lookup"><span data-stu-id="74552-115">yes</span></span>       |
| [<span data-ttu-id="74552-116">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="74552-116">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="74552-117">да</span><span class="sxs-lookup"><span data-stu-id="74552-117">yes</span></span>       |
| [<span data-ttu-id="74552-118">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="74552-118">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="74552-119">Нет</span><span class="sxs-lookup"><span data-stu-id="74552-119">no</span></span>        |
| [<span data-ttu-id="74552-120">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="74552-120">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="74552-121">Нет</span><span class="sxs-lookup"><span data-stu-id="74552-121">no</span></span>        |
| [<span data-ttu-id="74552-122">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="74552-122">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="74552-123">Нет</span><span class="sxs-lookup"><span data-stu-id="74552-123">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="74552-124">См. также</span><span class="sxs-lookup"><span data-stu-id="74552-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74552-125">Модификаторы инструкций</span><span class="sxs-lookup"><span data-stu-id="74552-125">Instruction Modifiers</span></span>](instruction-modifiers.md)
</dt> </dl>

 

 




