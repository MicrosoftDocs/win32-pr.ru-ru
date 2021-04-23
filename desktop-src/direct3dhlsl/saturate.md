---
title: Насыщенность (ссылка HLSL)
description: Отменяет результат арифметической операции одинарной или двойной точности с плавающей запятой до 0,0 f... 1,0 f \ диапазон.
ms.assetid: ce3e79c7-c3e6-4a2c-910a-2cd568aece50
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 05b6048777ac7b6ecd2c4b59ff3c9e0287380949
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/23/2019
ms.locfileid: "104412273"
---
# <a name="saturate-hlsl-reference"></a><span data-ttu-id="c513c-103">Насыщенность (ссылка HLSL)</span><span class="sxs-lookup"><span data-stu-id="c513c-103">Saturate (HLSL reference)</span></span>

<span data-ttu-id="c513c-104">Отменяет результат арифметической операции одинарной или двойной точности с плавающей запятой до \[ 0,0 f... 1,0 f \] диапазона.</span><span class="sxs-lookup"><span data-stu-id="c513c-104">Clamps the result of a single or double precision floating point arithmetic operation to \[0.0f...1.0f\] range.</span></span>



| <span data-ttu-id="c513c-105">\_Кот</span><span class="sxs-lookup"><span data-stu-id="c513c-105">\_sat</span></span> |
|-------|



 

<span data-ttu-id="c513c-106">Модификатор результата инструкции " **насыщенность** " выполняет следующую операцию с результирующими значениями из арифметической операции с плавающей запятой, к которой \_ применены результаты.</span><span class="sxs-lookup"><span data-stu-id="c513c-106">The **saturate** instruction result modifier performs the following operation on the result values(s) from a floating point arithmetic operation that has \_sat applied to it:</span></span>

`min(1.0f, max(0.0f, value))`

<span data-ttu-id="c513c-107">Если min () и Max () в приведенном выше выражении ведут себя так, как [min](min--sm4---asm-.md), [Max](max--sm4---asm-.md), [DMin](dmin--sm5---asm-.md)или [DMax](dmax--sm5---asm-.md) работают.</span><span class="sxs-lookup"><span data-stu-id="c513c-107">where min() and max() in the above expression behave in the way [min](min--sm4---asm-.md), [max](max--sm4---asm-.md), [dmin](dmin--sm5---asm-.md), or [dmax](dmax--sm5---asm-.md) operate.</span></span>

<span data-ttu-id="c513c-108">`_sat(NaN)` Возвращает 0, по правилам для min и Max.</span><span class="sxs-lookup"><span data-stu-id="c513c-108">`_sat(NaN)` returns 0, by the rules for min and max.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="c513c-109">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="c513c-109">Minimum Shader Model</span></span>

<span data-ttu-id="c513c-110">Этот модификатор поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="c513c-110">This modifier is supported in the following shader models.</span></span>



| <span data-ttu-id="c513c-111">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="c513c-111">Shader Model</span></span>                                              | <span data-ttu-id="c513c-112">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="c513c-112">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="c513c-113">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="c513c-113">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="c513c-114">да</span><span class="sxs-lookup"><span data-stu-id="c513c-114">yes</span></span>       |
| [<span data-ttu-id="c513c-115">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="c513c-115">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="c513c-116">да</span><span class="sxs-lookup"><span data-stu-id="c513c-116">yes</span></span>       |
| [<span data-ttu-id="c513c-117">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="c513c-117">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="c513c-118">да</span><span class="sxs-lookup"><span data-stu-id="c513c-118">yes</span></span>       |
| [<span data-ttu-id="c513c-119">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c513c-119">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="c513c-120">Нет</span><span class="sxs-lookup"><span data-stu-id="c513c-120">no</span></span>        |
| [<span data-ttu-id="c513c-121">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c513c-121">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="c513c-122">Нет</span><span class="sxs-lookup"><span data-stu-id="c513c-122">no</span></span>        |
| [<span data-ttu-id="c513c-123">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c513c-123">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="c513c-124">Нет</span><span class="sxs-lookup"><span data-stu-id="c513c-124">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="c513c-125">См. также</span><span class="sxs-lookup"><span data-stu-id="c513c-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c513c-126">Модификаторы инструкций</span><span class="sxs-lookup"><span data-stu-id="c513c-126">Instruction Modifiers</span></span>](instruction-modifiers.md)
</dt> </dl>

 

 




