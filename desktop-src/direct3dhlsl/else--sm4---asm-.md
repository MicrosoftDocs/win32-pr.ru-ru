---
title: else (SM4-ASM)
description: Запускает блок else.
ms.assetid: CFF25E78-D986-4EC5-B542-B3396EFF88E1
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e283a2621c916ac254daab9f055be0ffe1ba67d
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104983889"
---
# <a name="else-sm4---asm"></a><span data-ttu-id="a0a6e-103">else (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="a0a6e-103">else (sm4 - asm)</span></span>

<span data-ttu-id="a0a6e-104">Запускает блок **else** .</span><span class="sxs-lookup"><span data-stu-id="a0a6e-104">Starts an **else** block.</span></span>



| <span data-ttu-id="a0a6e-105">else</span><span class="sxs-lookup"><span data-stu-id="a0a6e-105">else</span></span> |
|------|



 

## <a name="remarks"></a><span data-ttu-id="a0a6e-106">Примечания</span><span class="sxs-lookup"><span data-stu-id="a0a6e-106">Remarks</span></span>

<span data-ttu-id="a0a6e-107">Формат токена содержит смещение соответствующей инструкции [endif](endif--sm4---asm-.md) в шейдере для удобства.</span><span class="sxs-lookup"><span data-stu-id="a0a6e-107">The token format contains the offset of the corresponding [endif](endif--sm4---asm-.md) instruction in the Shader as a convenience.</span></span>

<span data-ttu-id="a0a6e-108">В следующем примере показано, как использовать инструкцию **else** .</span><span class="sxs-lookup"><span data-stu-id="a0a6e-108">The following example shows how to use the **else** instruction.</span></span>

``` syntax
                if     // any of the various forms of if* statements
                   ...
                else   // (optional)
                   ...
                endif
```

<span data-ttu-id="a0a6e-109">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="a0a6e-109">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="a0a6e-110">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="a0a6e-110">Vertex Shader</span></span> | <span data-ttu-id="a0a6e-111">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="a0a6e-111">Geometry Shader</span></span> | <span data-ttu-id="a0a6e-112">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="a0a6e-112">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="a0a6e-113">x</span><span class="sxs-lookup"><span data-stu-id="a0a6e-113">x</span></span>             | <span data-ttu-id="a0a6e-114">x</span><span class="sxs-lookup"><span data-stu-id="a0a6e-114">x</span></span>               | <span data-ttu-id="a0a6e-115">x</span><span class="sxs-lookup"><span data-stu-id="a0a6e-115">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="a0a6e-116">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="a0a6e-116">Minimum Shader Model</span></span>

<span data-ttu-id="a0a6e-117">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="a0a6e-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="a0a6e-118">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="a0a6e-118">Shader Model</span></span>                                              | <span data-ttu-id="a0a6e-119">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="a0a6e-119">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="a0a6e-120">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="a0a6e-120">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="a0a6e-121">да</span><span class="sxs-lookup"><span data-stu-id="a0a6e-121">yes</span></span>       |
| [<span data-ttu-id="a0a6e-122">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="a0a6e-122">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="a0a6e-123">да</span><span class="sxs-lookup"><span data-stu-id="a0a6e-123">yes</span></span>       |
| [<span data-ttu-id="a0a6e-124">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="a0a6e-124">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="a0a6e-125">да</span><span class="sxs-lookup"><span data-stu-id="a0a6e-125">yes</span></span>       |
| [<span data-ttu-id="a0a6e-126">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a0a6e-126">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="a0a6e-127">Нет</span><span class="sxs-lookup"><span data-stu-id="a0a6e-127">no</span></span>        |
| [<span data-ttu-id="a0a6e-128">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a0a6e-128">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="a0a6e-129">Нет</span><span class="sxs-lookup"><span data-stu-id="a0a6e-129">no</span></span>        |
| [<span data-ttu-id="a0a6e-130">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a0a6e-130">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="a0a6e-131">Нет</span><span class="sxs-lookup"><span data-stu-id="a0a6e-131">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="a0a6e-132">См. также</span><span class="sxs-lookup"><span data-stu-id="a0a6e-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0a6e-133">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a0a6e-133">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




