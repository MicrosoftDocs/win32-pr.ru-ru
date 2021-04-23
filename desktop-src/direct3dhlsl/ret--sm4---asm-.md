---
title: RET (SM4-ASM)
description: Оператор Return.
ms.assetid: 1B690036-99C5-441D-9DD3-E09D43E48AFF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d834cd9f32d6e38f40666ab235f705c0fc80513f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "103784917"
---
# <a name="ret-sm4---asm"></a><span data-ttu-id="03ac9-103">RET (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="03ac9-103">ret (sm4 - asm)</span></span>

<span data-ttu-id="03ac9-104">Оператор Return.</span><span class="sxs-lookup"><span data-stu-id="03ac9-104">Return statement.</span></span>



| <span data-ttu-id="03ac9-105">обратно</span><span class="sxs-lookup"><span data-stu-id="03ac9-105">ret</span></span> |
|-----|



 

## <a name="remarks"></a><span data-ttu-id="03ac9-106">Примечания</span><span class="sxs-lookup"><span data-stu-id="03ac9-106">Remarks</span></span>

<span data-ttu-id="03ac9-107">Если внутри подпрограммы, вернитесь к инструкции после вызова.</span><span class="sxs-lookup"><span data-stu-id="03ac9-107">If within a subroutine, return to the instruction after the call.</span></span> <span data-ttu-id="03ac9-108">Если не входит в подпрограмму, завершите выполнение программы.</span><span class="sxs-lookup"><span data-stu-id="03ac9-108">If not inside a subroutine, terminate program execution.</span></span>

<span data-ttu-id="03ac9-109">В следующем примере показано, как использовать эту инструкцию.</span><span class="sxs-lookup"><span data-stu-id="03ac9-109">The following example shows how to use this instruction.</span></span>

``` syntax
 
               ...
                call l3
                ...
                ret
                label l3
                    ...
                ret
```

### <a name="restrictions"></a><span data-ttu-id="03ac9-110">Ограничения</span><span class="sxs-lookup"><span data-stu-id="03ac9-110">Restrictions</span></span>

-   <span data-ttu-id="03ac9-111">Программа **RET** может появляться в любом месте программы, любое количество раз.</span><span class="sxs-lookup"><span data-stu-id="03ac9-111">**ret** can appear anywhere in a program, any number of times.</span></span>
-   <span data-ttu-id="03ac9-112">Если инструкция [Label](label--sm4---asm-.md) отображается в шейдере, ей должна предшествовать команда **RET** , которая не вложена ни в какие инструкции управления потоком.</span><span class="sxs-lookup"><span data-stu-id="03ac9-112">If a [label](label--sm4---asm-.md) instruction appears in a Shader, it must be preceded by a **ret** command that is not nested in any flow control statements.</span></span>
-   <span data-ttu-id="03ac9-113">Если в шейдере есть подпрограммы, последняя инструкция в шейдере должна быть **RET**.</span><span class="sxs-lookup"><span data-stu-id="03ac9-113">If there are subroutines in a Shader, the last instruction in the Shader must be a **ret**.</span></span>

<span data-ttu-id="03ac9-114">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="03ac9-114">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="03ac9-115">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="03ac9-115">Vertex Shader</span></span> | <span data-ttu-id="03ac9-116">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="03ac9-116">Geometry Shader</span></span> | <span data-ttu-id="03ac9-117">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="03ac9-117">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="03ac9-118">x</span><span class="sxs-lookup"><span data-stu-id="03ac9-118">x</span></span>             | <span data-ttu-id="03ac9-119">x</span><span class="sxs-lookup"><span data-stu-id="03ac9-119">x</span></span>               | <span data-ttu-id="03ac9-120">x</span><span class="sxs-lookup"><span data-stu-id="03ac9-120">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="03ac9-121">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="03ac9-121">Minimum Shader Model</span></span>

<span data-ttu-id="03ac9-122">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="03ac9-122">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="03ac9-123">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="03ac9-123">Shader Model</span></span>                                              | <span data-ttu-id="03ac9-124">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="03ac9-124">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="03ac9-125">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="03ac9-125">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="03ac9-126">да</span><span class="sxs-lookup"><span data-stu-id="03ac9-126">yes</span></span>       |
| [<span data-ttu-id="03ac9-127">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="03ac9-127">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="03ac9-128">да</span><span class="sxs-lookup"><span data-stu-id="03ac9-128">yes</span></span>       |
| [<span data-ttu-id="03ac9-129">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="03ac9-129">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="03ac9-130">да</span><span class="sxs-lookup"><span data-stu-id="03ac9-130">yes</span></span>       |
| [<span data-ttu-id="03ac9-131">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="03ac9-131">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="03ac9-132">Нет</span><span class="sxs-lookup"><span data-stu-id="03ac9-132">no</span></span>        |
| [<span data-ttu-id="03ac9-133">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="03ac9-133">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="03ac9-134">Нет</span><span class="sxs-lookup"><span data-stu-id="03ac9-134">no</span></span>        |
| [<span data-ttu-id="03ac9-135">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="03ac9-135">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="03ac9-136">Нет</span><span class="sxs-lookup"><span data-stu-id="03ac9-136">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="03ac9-137">См. также</span><span class="sxs-lookup"><span data-stu-id="03ac9-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03ac9-138">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="03ac9-138">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




