---
title: по умолчанию (SM4-ASM)
description: Необязательная метка в операторе switch.
ms.assetid: DB10F654-4A98-4ED8-A3B4-CA9FE1DFE6CD
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b92364212e4d20a6e9229c057ba424f43f8f8556
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104983829"
---
# <a name="default-sm4---asm"></a><span data-ttu-id="e4b04-103">по умолчанию (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="e4b04-103">default (sm4 - asm)</span></span>

<span data-ttu-id="e4b04-104">Необязательная метка в операторе [switch](switch--sm4---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="e4b04-104">An optional label in a [switch](switch--sm4---asm-.md) statement.</span></span>



| <span data-ttu-id="e4b04-105">default</span><span class="sxs-lookup"><span data-stu-id="e4b04-105">default</span></span> |
|---------|



 

## <a name="remarks"></a><span data-ttu-id="e4b04-106">Примечания</span><span class="sxs-lookup"><span data-stu-id="e4b04-106">Remarks</span></span>

<span data-ttu-id="e4b04-107">Эта инструкция действует так же, как и **по умолчанию** в языке C. Использование оператора допускается только в том случае, если код не добавлен, поэтому несколько вариантов (включая **значение по умолчанию**) могут совместно использовать один и тот же блок кода.</span><span class="sxs-lookup"><span data-stu-id="e4b04-107">This instruction operates just like **default** in C. Falling through is valid only if there is no code added, so multiple cases (including **default**) can share the same code block.</span></span>

<span data-ttu-id="e4b04-108">В конструкции **switch** допускается только одна инструкция **по умолчанию** .</span><span class="sxs-lookup"><span data-stu-id="e4b04-108">Only one **default** statement is permitted in a **switch** construct.</span></span>

<span data-ttu-id="e4b04-109">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="e4b04-109">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="e4b04-110">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="e4b04-110">Vertex Shader</span></span> | <span data-ttu-id="e4b04-111">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="e4b04-111">Geometry Shader</span></span> | <span data-ttu-id="e4b04-112">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="e4b04-112">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="e4b04-113">x</span><span class="sxs-lookup"><span data-stu-id="e4b04-113">x</span></span>             | <span data-ttu-id="e4b04-114">x</span><span class="sxs-lookup"><span data-stu-id="e4b04-114">x</span></span>               | <span data-ttu-id="e4b04-115">x</span><span class="sxs-lookup"><span data-stu-id="e4b04-115">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="e4b04-116">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="e4b04-116">Minimum Shader Model</span></span>

<span data-ttu-id="e4b04-117">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="e4b04-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="e4b04-118">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="e4b04-118">Shader Model</span></span>                                              | <span data-ttu-id="e4b04-119">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="e4b04-119">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="e4b04-120">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="e4b04-120">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="e4b04-121">да</span><span class="sxs-lookup"><span data-stu-id="e4b04-121">yes</span></span>       |
| [<span data-ttu-id="e4b04-122">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="e4b04-122">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="e4b04-123">да</span><span class="sxs-lookup"><span data-stu-id="e4b04-123">yes</span></span>       |
| [<span data-ttu-id="e4b04-124">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="e4b04-124">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="e4b04-125">да</span><span class="sxs-lookup"><span data-stu-id="e4b04-125">yes</span></span>       |
| [<span data-ttu-id="e4b04-126">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e4b04-126">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="e4b04-127">Нет</span><span class="sxs-lookup"><span data-stu-id="e4b04-127">no</span></span>        |
| [<span data-ttu-id="e4b04-128">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e4b04-128">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="e4b04-129">Нет</span><span class="sxs-lookup"><span data-stu-id="e4b04-129">no</span></span>        |
| [<span data-ttu-id="e4b04-130">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e4b04-130">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="e4b04-131">Нет</span><span class="sxs-lookup"><span data-stu-id="e4b04-131">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="e4b04-132">См. также</span><span class="sxs-lookup"><span data-stu-id="e4b04-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4b04-133">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e4b04-133">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




