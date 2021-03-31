---
title: Точная
description: Отключение арифметического рефакторинга для каждой инструкции.
ms.assetid: A26E569A-32EA-4AED-83C2-4F937AD3829E
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 03f288fb5dafee0e29c8c11cab72156f7ad3d569
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104532861"
---
# <a name="precise"></a><span data-ttu-id="6db8b-103">Точная</span><span class="sxs-lookup"><span data-stu-id="6db8b-103">Precise</span></span>

<span data-ttu-id="6db8b-104">Отключение арифметического рефакторинга для каждой инструкции.</span><span class="sxs-lookup"><span data-stu-id="6db8b-104">Per-instruction disabling of arithmetic refactoring.</span></span>



| <span data-ttu-id="6db8b-105">Точная (маска компонента)</span><span class="sxs-lookup"><span data-stu-id="6db8b-105">precise (component mask)</span></span> |
|--------------------------|



 

<span data-ttu-id="6db8b-106">Для этого модификатора требуется глобальный флаг шейдера " \_ РАЗРЕШЕН рефакторинг".</span><span class="sxs-lookup"><span data-stu-id="6db8b-106">This modifier requires the global shader flag "REFACTORING\_ALLOWED".</span></span> <span data-ttu-id="6db8b-107">При \_ наличии разрешенного РЕфакторинга результаты отдельных инструкций могут быть принудительно ограничены компиляторами или драйверами.</span><span class="sxs-lookup"><span data-stu-id="6db8b-107">When REFACTORING\_ALLOWED is present, individual component results of individual instructions can be forced to remain precise or not-refactorable by compilers or drivers.</span></span> <span data-ttu-id="6db8b-108">Если компоненты инструкции [**Mad**](mad--sm4---asm-.md) помечены как **точные**, оборудование должно выполнить инструкцию **Mad** или точный эквивалент, и оно не может разделить его на множитель, за которым следует оператор Add.</span><span class="sxs-lookup"><span data-stu-id="6db8b-108">If components of a [**mad**](mad--sm4---asm-.md) instruction are tagged as **precise**, the hardware must execute a **mad** instruction or the exact equivalent, and it cannot split it into a multiply followed by an add.</span></span> <span data-ttu-id="6db8b-109">И наоборот, умножение, за которым следует оператор Add, где один или оба помечены как **точные**, не могут быть объединены в **Mad** с плавким предохранителем.</span><span class="sxs-lookup"><span data-stu-id="6db8b-109">Conversely, a multiply followed by an add, where either or both are flagged as **precise**, cannot be merged into a fused **mad**.</span></span>

<span data-ttu-id="6db8b-110">Если РЕФАКТОРИНГ \_ не указан, то модификатор **точности** не разрешен.</span><span class="sxs-lookup"><span data-stu-id="6db8b-110">If REFACTORING\_ALLOWED has not been specified, the **precise** modifier is not allowed.</span></span> <span data-ttu-id="6db8b-111">Это не требуется, так как все является точным.</span><span class="sxs-lookup"><span data-stu-id="6db8b-111">It is not needed because everything is precise.</span></span> <span data-ttu-id="6db8b-112">Модификатор **точности** влияет на любую операцию, а не только на арифметический.</span><span class="sxs-lookup"><span data-stu-id="6db8b-112">The **precise** modifier affects any operation, not just arithmetic.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="6db8b-113">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="6db8b-113">Minimum Shader Model</span></span>

<span data-ttu-id="6db8b-114">Этот модификатор поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="6db8b-114">This modifier is supported in the following shader models.</span></span>



| <span data-ttu-id="6db8b-115">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="6db8b-115">Shader Model</span></span>                                              | <span data-ttu-id="6db8b-116">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="6db8b-116">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="6db8b-117">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="6db8b-117">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="6db8b-118">да</span><span class="sxs-lookup"><span data-stu-id="6db8b-118">yes</span></span>       |
| [<span data-ttu-id="6db8b-119">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="6db8b-119">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="6db8b-120">Нет</span><span class="sxs-lookup"><span data-stu-id="6db8b-120">no</span></span>        |
| [<span data-ttu-id="6db8b-121">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="6db8b-121">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="6db8b-122">да</span><span class="sxs-lookup"><span data-stu-id="6db8b-122">yes</span></span>       |
| [<span data-ttu-id="6db8b-123">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6db8b-123">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="6db8b-124">Нет</span><span class="sxs-lookup"><span data-stu-id="6db8b-124">no</span></span>        |
| [<span data-ttu-id="6db8b-125">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6db8b-125">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="6db8b-126">Нет</span><span class="sxs-lookup"><span data-stu-id="6db8b-126">no</span></span>        |
| [<span data-ttu-id="6db8b-127">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6db8b-127">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="6db8b-128">Нет</span><span class="sxs-lookup"><span data-stu-id="6db8b-128">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="6db8b-129">См. также</span><span class="sxs-lookup"><span data-stu-id="6db8b-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6db8b-130">Модификаторы инструкций модели шейдеров 5</span><span class="sxs-lookup"><span data-stu-id="6db8b-130">Shader Model 5 Instruction Modifiers</span></span>](shader-model-5-instruction-modifiers.md)
</dt> </dl>

 

 




