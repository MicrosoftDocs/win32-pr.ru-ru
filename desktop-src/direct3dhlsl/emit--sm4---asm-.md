---
title: Emit (SM4-ASM)
description: Выдает вершину.
ms.assetid: FDD18CCD-8088-46BD-897C-434B77FF81E6
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b17711b6f9cf5d707fb8eae3465100a78620c0c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "103784893"
---
# <a name="emit-sm4---asm"></a><span data-ttu-id="6d7d6-103">Emit (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="6d7d6-103">emit (sm4 - asm)</span></span>

<span data-ttu-id="6d7d6-104">Выдает вершину.</span><span class="sxs-lookup"><span data-stu-id="6d7d6-104">Emit a vertex.</span></span>



| <span data-ttu-id="6d7d6-105">давать</span><span class="sxs-lookup"><span data-stu-id="6d7d6-105">emit</span></span> |
|------|



 

## <a name="remarks"></a><span data-ttu-id="6d7d6-106">Примечания</span><span class="sxs-lookup"><span data-stu-id="6d7d6-106">Remarks</span></span>

<span data-ttu-id="6d7d6-107">**выдача** приводит к считыванию всех объявленных \# регистров o из шейдера Geometry для создания вершины.</span><span class="sxs-lookup"><span data-stu-id="6d7d6-107">**emit** causes all declared o\# registers to be read out of the Geometry Shader to generate a vertex.</span></span>

<span data-ttu-id="6d7d6-108">При выдаче нескольких вызовов **выдачи** создаются примитивы.</span><span class="sxs-lookup"><span data-stu-id="6d7d6-108">As multiple **emit** calls are issued, primitives are generated.</span></span>

<span data-ttu-id="6d7d6-109">**выдача** может появляться любое количество раз в шейдере Geometry, в том числе в элементе управления потоком.</span><span class="sxs-lookup"><span data-stu-id="6d7d6-109">**emit** can appear any number of times in a Geometry Shader, including within flow control.</span></span>

<span data-ttu-id="6d7d6-110">Если были объявлены потоки, необходимо использовать [отражательный \_ поток](emit-stream--sm5---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="6d7d6-110">If streams have been declared, you must use [emit\_stream](emit-stream--sm5---asm-.md).</span></span>

<span data-ttu-id="6d7d6-111">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="6d7d6-111">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="6d7d6-112">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="6d7d6-112">Vertex Shader</span></span> | <span data-ttu-id="6d7d6-113">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="6d7d6-113">Geometry Shader</span></span> | <span data-ttu-id="6d7d6-114">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="6d7d6-114">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               | <span data-ttu-id="6d7d6-115">x</span><span class="sxs-lookup"><span data-stu-id="6d7d6-115">x</span></span>               |              |



 

### <a name="minimum-shader-model"></a><span data-ttu-id="6d7d6-116">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="6d7d6-116">Minimum Shader Model</span></span>

<span data-ttu-id="6d7d6-117">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="6d7d6-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="6d7d6-118">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="6d7d6-118">Shader Model</span></span>                                              | <span data-ttu-id="6d7d6-119">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="6d7d6-119">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="6d7d6-120">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="6d7d6-120">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="6d7d6-121">да</span><span class="sxs-lookup"><span data-stu-id="6d7d6-121">yes</span></span>       |
| [<span data-ttu-id="6d7d6-122">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="6d7d6-122">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="6d7d6-123">да</span><span class="sxs-lookup"><span data-stu-id="6d7d6-123">yes</span></span>       |
| [<span data-ttu-id="6d7d6-124">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="6d7d6-124">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="6d7d6-125">да</span><span class="sxs-lookup"><span data-stu-id="6d7d6-125">yes</span></span>       |
| [<span data-ttu-id="6d7d6-126">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6d7d6-126">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="6d7d6-127">Нет</span><span class="sxs-lookup"><span data-stu-id="6d7d6-127">no</span></span>        |
| [<span data-ttu-id="6d7d6-128">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6d7d6-128">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="6d7d6-129">Нет</span><span class="sxs-lookup"><span data-stu-id="6d7d6-129">no</span></span>        |
| [<span data-ttu-id="6d7d6-130">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6d7d6-130">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="6d7d6-131">Нет</span><span class="sxs-lookup"><span data-stu-id="6d7d6-131">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="6d7d6-132">См. также</span><span class="sxs-lookup"><span data-stu-id="6d7d6-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d7d6-133">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6d7d6-133">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




