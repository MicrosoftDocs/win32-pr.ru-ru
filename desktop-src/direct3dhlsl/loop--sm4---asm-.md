---
title: Loop (SM4-ASM)
description: Указывает цикл, который выполняет итерацию до тех пор, пока не встретится инструкция Break.
ms.assetid: 0BEFADF4-036E-4FDA-9681-10965D6BA9FC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 243bdf3b370d3505d787451162c22340acef3a45
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996919"
---
# <a name="loop-sm4---asm"></a><span data-ttu-id="a008e-103">Loop (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="a008e-103">loop (sm4 - asm)</span></span>

<span data-ttu-id="a008e-104">Указывает цикл, который выполняет итерацию до тех пор, пока не встретится инструкция Break.</span><span class="sxs-lookup"><span data-stu-id="a008e-104">Specifies a loop which iterates until a break instruction is encountered.</span></span>



| <span data-ttu-id="a008e-105">loop</span><span class="sxs-lookup"><span data-stu-id="a008e-105">loop</span></span> |
|------|



 

## <a name="remarks"></a><span data-ttu-id="a008e-106">Примечания</span><span class="sxs-lookup"><span data-stu-id="a008e-106">Remarks</span></span>

<span data-ttu-id="a008e-107">**цикл** может выполнять итерацию неограниченно, хотя общее выполнение шейдера может быть принудительно завершено после выполнения некоторого числа инструкций.</span><span class="sxs-lookup"><span data-stu-id="a008e-107">**loop** can iterate indefinitely, although overall execution of the Shader may be forced to terminate after some number of instructions are executed.</span></span>

<span data-ttu-id="a008e-108">Блоки управления потоком могут вкладывать до 64 глубоких позиций на подпрограммы и Main.</span><span class="sxs-lookup"><span data-stu-id="a008e-108">Flow control blocks can nest up to 64 deep per subroutine and main.</span></span> <span data-ttu-id="a008e-109">Компилятор HLSL не будет создавать подпрограммы, превышающие это ограничение.</span><span class="sxs-lookup"><span data-stu-id="a008e-109">The HLSL compiler will not generate subroutines that exceed this limit.</span></span> <span data-ttu-id="a008e-110">Поведение инструкций потока управления свыше 64 уровней в каждой подподпрограмме не определено.</span><span class="sxs-lookup"><span data-stu-id="a008e-110">Behavior of control flow instructions beyond 64 levels deep per subroutine is undefined.</span></span>

<span data-ttu-id="a008e-111">Формат маркера содержит смещение соответствующей инструкции [ендлуп](endloop--sm4---asm-.md) в шейдере для удобства.</span><span class="sxs-lookup"><span data-stu-id="a008e-111">The token format contains the offset of the corresponding [endloop](endloop--sm4---asm-.md) instruction in the Shader as a convenience.</span></span>

<span data-ttu-id="a008e-112">В следующем примере показано, как использовать инструкцию Loop.</span><span class="sxs-lookup"><span data-stu-id="a008e-112">The following example shows how to use the loop instruction.</span></span>

``` syntax
                loop
                    // example of termination condition
                    if_nz r0.x
                        break
                    endif
                    ...
                endloop
```

<span data-ttu-id="a008e-113">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="a008e-113">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="a008e-114">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="a008e-114">Vertex Shader</span></span> | <span data-ttu-id="a008e-115">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="a008e-115">Geometry Shader</span></span> | <span data-ttu-id="a008e-116">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="a008e-116">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="a008e-117">x</span><span class="sxs-lookup"><span data-stu-id="a008e-117">x</span></span>             | <span data-ttu-id="a008e-118">x</span><span class="sxs-lookup"><span data-stu-id="a008e-118">x</span></span>               | <span data-ttu-id="a008e-119">x</span><span class="sxs-lookup"><span data-stu-id="a008e-119">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="a008e-120">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="a008e-120">Minimum Shader Model</span></span>

<span data-ttu-id="a008e-121">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="a008e-121">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="a008e-122">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="a008e-122">Shader Model</span></span>                                              | <span data-ttu-id="a008e-123">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="a008e-123">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="a008e-124">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="a008e-124">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="a008e-125">да</span><span class="sxs-lookup"><span data-stu-id="a008e-125">yes</span></span>       |
| [<span data-ttu-id="a008e-126">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="a008e-126">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="a008e-127">да</span><span class="sxs-lookup"><span data-stu-id="a008e-127">yes</span></span>       |
| [<span data-ttu-id="a008e-128">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="a008e-128">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="a008e-129">да</span><span class="sxs-lookup"><span data-stu-id="a008e-129">yes</span></span>       |
| [<span data-ttu-id="a008e-130">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a008e-130">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="a008e-131">Нет</span><span class="sxs-lookup"><span data-stu-id="a008e-131">no</span></span>        |
| [<span data-ttu-id="a008e-132">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a008e-132">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="a008e-133">Нет</span><span class="sxs-lookup"><span data-stu-id="a008e-133">no</span></span>        |
| [<span data-ttu-id="a008e-134">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a008e-134">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="a008e-135">Нет</span><span class="sxs-lookup"><span data-stu-id="a008e-135">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="a008e-136">См. также</span><span class="sxs-lookup"><span data-stu-id="a008e-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a008e-137">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a008e-137">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




