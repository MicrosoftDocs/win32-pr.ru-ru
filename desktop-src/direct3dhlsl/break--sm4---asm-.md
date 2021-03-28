---
title: Break (SM4-ASM)
description: Перемещает точку выполнения в инструкцию после следующей ендлуп или ендсвитч.
ms.assetid: 411FB361-FBD1-4180-8D81-2074BA8972B7
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06396d062e9126091052126737e3e05c58dbdb16
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104335512"
---
# <a name="break-sm4---asm"></a><span data-ttu-id="9d3b6-103">Break (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="9d3b6-103">break (sm4 - asm)</span></span>

<span data-ttu-id="9d3b6-104">Перемещает точку выполнения в инструкцию после следующей [ендлуп](endloop--sm4---asm-.md) или [ендсвитч](endswitch--sm4---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="9d3b6-104">Moves the point of execution to the instruction after the next [endloop](endloop--sm4---asm-.md) or [endswitch](endswitch--sm4---asm-.md).</span></span>



| <span data-ttu-id="9d3b6-105">break</span><span class="sxs-lookup"><span data-stu-id="9d3b6-105">break</span></span> |
|-------|



 

## <a name="remarks"></a><span data-ttu-id="9d3b6-106">Примечания</span><span class="sxs-lookup"><span data-stu-id="9d3b6-106">Remarks</span></span>

<span data-ttu-id="9d3b6-107">Формат маркера содержит смещение соответствующей инструкции **ендлуп** или **ендсвитч** в шейдере для удобства.</span><span class="sxs-lookup"><span data-stu-id="9d3b6-107">The token format contains the offset of the corresponding **endloop** or **endswitch** instruction in the Shader as a convenience.</span></span>

<span data-ttu-id="9d3b6-108">В следующем примере показана инструкция **break** .</span><span class="sxs-lookup"><span data-stu-id="9d3b6-108">The following example shows the **break** instruction.</span></span>


```
                loop
                    // example of termination condition
                    if_nz r0.x
                        break
                    endif
                    ...
                endloop
```



<span data-ttu-id="9d3b6-109">Эта инструкция должна находиться в **цикле** / **ендлуп** или в **случае** в **параметре** / **ендсвитч**.</span><span class="sxs-lookup"><span data-stu-id="9d3b6-109">This instruction must appear within a **loop**/**endloop** or in a **case** in a **switch**/**endswitch**.</span></span>

<span data-ttu-id="9d3b6-110">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="9d3b6-110">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="9d3b6-111">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="9d3b6-111">Vertex Shader</span></span> | <span data-ttu-id="9d3b6-112">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="9d3b6-112">Geometry Shader</span></span> | <span data-ttu-id="9d3b6-113">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="9d3b6-113">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="9d3b6-114">x</span><span class="sxs-lookup"><span data-stu-id="9d3b6-114">x</span></span>             | <span data-ttu-id="9d3b6-115">x</span><span class="sxs-lookup"><span data-stu-id="9d3b6-115">x</span></span>               | <span data-ttu-id="9d3b6-116">x</span><span class="sxs-lookup"><span data-stu-id="9d3b6-116">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="9d3b6-117">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="9d3b6-117">Minimum Shader Model</span></span>

<span data-ttu-id="9d3b6-118">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="9d3b6-118">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="9d3b6-119">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="9d3b6-119">Shader Model</span></span>                                              | <span data-ttu-id="9d3b6-120">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="9d3b6-120">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="9d3b6-121">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="9d3b6-121">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="9d3b6-122">да</span><span class="sxs-lookup"><span data-stu-id="9d3b6-122">yes</span></span>       |
| [<span data-ttu-id="9d3b6-123">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="9d3b6-123">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="9d3b6-124">да</span><span class="sxs-lookup"><span data-stu-id="9d3b6-124">yes</span></span>       |
| [<span data-ttu-id="9d3b6-125">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="9d3b6-125">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="9d3b6-126">да</span><span class="sxs-lookup"><span data-stu-id="9d3b6-126">yes</span></span>       |
| [<span data-ttu-id="9d3b6-127">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9d3b6-127">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="9d3b6-128">Нет</span><span class="sxs-lookup"><span data-stu-id="9d3b6-128">no</span></span>        |
| [<span data-ttu-id="9d3b6-129">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9d3b6-129">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="9d3b6-130">Нет</span><span class="sxs-lookup"><span data-stu-id="9d3b6-130">no</span></span>        |
| [<span data-ttu-id="9d3b6-131">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9d3b6-131">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="9d3b6-132">Нет</span><span class="sxs-lookup"><span data-stu-id="9d3b6-132">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="9d3b6-133">См. также</span><span class="sxs-lookup"><span data-stu-id="9d3b6-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d3b6-134">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9d3b6-134">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




