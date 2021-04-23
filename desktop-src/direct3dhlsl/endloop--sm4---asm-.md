---
title: ендлуп (SM4-ASM)
description: Завершает оператор Loop.
ms.assetid: 0BEFADF4-036E-4FDA-9681-10965D6BA9FC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 655fa6addd19a6ce9f6f6b20a2677ef43cb8b751
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104412126"
---
# <a name="endloop-sm4---asm"></a><span data-ttu-id="fb181-103">ендлуп (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="fb181-103">endloop (sm4 - asm)</span></span>

<span data-ttu-id="fb181-104">Завершает оператор Loop.</span><span class="sxs-lookup"><span data-stu-id="fb181-104">Ends a loop statement.</span></span>



| <span data-ttu-id="fb181-105">ендлуп</span><span class="sxs-lookup"><span data-stu-id="fb181-105">endloop</span></span> |
|---------|



 

## <a name="remarks"></a><span data-ttu-id="fb181-106">Примечания</span><span class="sxs-lookup"><span data-stu-id="fb181-106">Remarks</span></span>

<span data-ttu-id="fb181-107">В следующем примере показано, как использовать эту инструкцию.</span><span class="sxs-lookup"><span data-stu-id="fb181-107">The following example shows how to use this instruction.</span></span>

``` syntax
                loop
                    // example of termination condition
                    if_nz r0.x
                        break
                    endif
                    ...
                endloop
```

<span data-ttu-id="fb181-108">Формат маркера содержит смещение соответствующей инструкции Loop в шейдере для удобства.</span><span class="sxs-lookup"><span data-stu-id="fb181-108">The token format contains the offset of the corresponding loop instruction in the Shader as a convenience.</span></span>

<span data-ttu-id="fb181-109">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="fb181-109">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="fb181-110">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="fb181-110">Vertex Shader</span></span> | <span data-ttu-id="fb181-111">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="fb181-111">Geometry Shader</span></span> | <span data-ttu-id="fb181-112">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="fb181-112">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="fb181-113">x</span><span class="sxs-lookup"><span data-stu-id="fb181-113">x</span></span>             | <span data-ttu-id="fb181-114">x</span><span class="sxs-lookup"><span data-stu-id="fb181-114">x</span></span>               | <span data-ttu-id="fb181-115">x</span><span class="sxs-lookup"><span data-stu-id="fb181-115">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="fb181-116">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="fb181-116">Minimum Shader Model</span></span>

<span data-ttu-id="fb181-117">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="fb181-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="fb181-118">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="fb181-118">Shader Model</span></span>                                              | <span data-ttu-id="fb181-119">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="fb181-119">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="fb181-120">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="fb181-120">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="fb181-121">да</span><span class="sxs-lookup"><span data-stu-id="fb181-121">yes</span></span>       |
| [<span data-ttu-id="fb181-122">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="fb181-122">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="fb181-123">да</span><span class="sxs-lookup"><span data-stu-id="fb181-123">yes</span></span>       |
| [<span data-ttu-id="fb181-124">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="fb181-124">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="fb181-125">да</span><span class="sxs-lookup"><span data-stu-id="fb181-125">yes</span></span>       |
| [<span data-ttu-id="fb181-126">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fb181-126">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="fb181-127">Нет</span><span class="sxs-lookup"><span data-stu-id="fb181-127">no</span></span>        |
| [<span data-ttu-id="fb181-128">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fb181-128">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="fb181-129">Нет</span><span class="sxs-lookup"><span data-stu-id="fb181-129">no</span></span>        |
| [<span data-ttu-id="fb181-130">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fb181-130">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="fb181-131">Нет</span><span class="sxs-lookup"><span data-stu-id="fb181-131">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="fb181-132">См. также</span><span class="sxs-lookup"><span data-stu-id="fb181-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb181-133">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fb181-133">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




