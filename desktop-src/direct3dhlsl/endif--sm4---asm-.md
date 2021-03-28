---
title: endif (SM4-ASM)
description: Завершает оператор if.
ms.assetid: 9F4CF9E0-4D9D-4300-B432-432C560F34BB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d3fa6cf0efd395843212f6bacac478285e496c2
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104069316"
---
# <a name="endif-sm4---asm"></a><span data-ttu-id="d02c8-103">endif (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="d02c8-103">endif (sm4 - asm)</span></span>

<span data-ttu-id="d02c8-104">Завершает оператор [If](if--sm4---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="d02c8-104">Ends an [if](if--sm4---asm-.md) statement.</span></span>



| <span data-ttu-id="d02c8-105">endif</span><span class="sxs-lookup"><span data-stu-id="d02c8-105">endif</span></span> |
|-------|



 

## <a name="remarks"></a><span data-ttu-id="d02c8-106">Примечания</span><span class="sxs-lookup"><span data-stu-id="d02c8-106">Remarks</span></span>

<span data-ttu-id="d02c8-107">В следующем примере показано, как использовать инструкцию endif.</span><span class="sxs-lookup"><span data-stu-id="d02c8-107">The following example shows how to use the endif instruction.</span></span>

``` syntax
                if     // any of the various forms of if* statements
                   ...
                else   // (optional)
                   ...
                endif
```

<span data-ttu-id="d02c8-108">Формат маркера содержит смещение соответствующей инструкции **If** в шейдере для удобства.</span><span class="sxs-lookup"><span data-stu-id="d02c8-108">The token format contains the offset of the corresponding **if** instruction in the Shader as a convenience.</span></span>

<span data-ttu-id="d02c8-109">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="d02c8-109">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="d02c8-110">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="d02c8-110">Vertex Shader</span></span> | <span data-ttu-id="d02c8-111">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="d02c8-111">Geometry Shader</span></span> | <span data-ttu-id="d02c8-112">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="d02c8-112">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="d02c8-113">x</span><span class="sxs-lookup"><span data-stu-id="d02c8-113">x</span></span>             | <span data-ttu-id="d02c8-114">x</span><span class="sxs-lookup"><span data-stu-id="d02c8-114">x</span></span>               | <span data-ttu-id="d02c8-115">x</span><span class="sxs-lookup"><span data-stu-id="d02c8-115">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d02c8-116">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="d02c8-116">Minimum Shader Model</span></span>

<span data-ttu-id="d02c8-117">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="d02c8-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d02c8-118">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="d02c8-118">Shader Model</span></span>                                              | <span data-ttu-id="d02c8-119">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="d02c8-119">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="d02c8-120">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="d02c8-120">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="d02c8-121">да</span><span class="sxs-lookup"><span data-stu-id="d02c8-121">yes</span></span>       |
| [<span data-ttu-id="d02c8-122">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="d02c8-122">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="d02c8-123">да</span><span class="sxs-lookup"><span data-stu-id="d02c8-123">yes</span></span>       |
| [<span data-ttu-id="d02c8-124">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="d02c8-124">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="d02c8-125">да</span><span class="sxs-lookup"><span data-stu-id="d02c8-125">yes</span></span>       |
| [<span data-ttu-id="d02c8-126">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d02c8-126">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="d02c8-127">Нет</span><span class="sxs-lookup"><span data-stu-id="d02c8-127">no</span></span>        |
| [<span data-ttu-id="d02c8-128">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d02c8-128">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="d02c8-129">Нет</span><span class="sxs-lookup"><span data-stu-id="d02c8-129">no</span></span>        |
| [<span data-ttu-id="d02c8-130">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d02c8-130">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="d02c8-131">Нет</span><span class="sxs-lookup"><span data-stu-id="d02c8-131">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="d02c8-132">См. также</span><span class="sxs-lookup"><span data-stu-id="d02c8-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d02c8-133">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d02c8-133">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




