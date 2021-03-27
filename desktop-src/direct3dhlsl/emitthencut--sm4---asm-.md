---
title: Емитсенкут (SM4-ASM)
description: Эквивалентно команде Emit, за которой следует команда Cut. | Емитсенкут (SM4-ASM)
ms.assetid: 80DE112A-790A-4DDF-A5BE-51F70BD7872C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb5b413ca11e22c7cfc17691fc0a39fe96bf7c0f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353862"
---
# <a name="emitthencut-sm4---asm"></a><span data-ttu-id="c0054-104">Емитсенкут (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="c0054-104">emitThenCut (sm4 - asm)</span></span>

<span data-ttu-id="c0054-105">Эквивалентно команде [Emit](emit--sm4---asm-.md) , за которой следует команда [Cut](cut--sm4---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="c0054-105">Equivalent to an [emit](emit--sm4---asm-.md) command followed by a [cut](cut--sm4---asm-.md) command.</span></span>



| <span data-ttu-id="c0054-106">емитсенкут</span><span class="sxs-lookup"><span data-stu-id="c0054-106">emitThenCut</span></span> |
|-------------|



 

## <a name="remarks"></a><span data-ttu-id="c0054-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="c0054-107">Remarks</span></span>

<span data-ttu-id="c0054-108">Эта команда полезна, когда вы узнаете о размещении последней вершины в топологии.</span><span class="sxs-lookup"><span data-stu-id="c0054-108">This command is useful when knowingly outputting the last vertex in a topology.</span></span>

<span data-ttu-id="c0054-109">Если были объявлены потоки, необходимо использовать [ \_ поток емитсенкут](emitthencut-stream--sm5---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="c0054-109">If streams have been declared, you must use [emitthencut\_stream](emitthencut-stream--sm5---asm-.md).</span></span>

<span data-ttu-id="c0054-110">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="c0054-110">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="c0054-111">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="c0054-111">Vertex Shader</span></span> | <span data-ttu-id="c0054-112">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="c0054-112">Geometry Shader</span></span> | <span data-ttu-id="c0054-113">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="c0054-113">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               | <span data-ttu-id="c0054-114">x</span><span class="sxs-lookup"><span data-stu-id="c0054-114">x</span></span>               |              |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="c0054-115">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="c0054-115">Minimum Shader Model</span></span>

<span data-ttu-id="c0054-116">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="c0054-116">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="c0054-117">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="c0054-117">Shader Model</span></span>                                              | <span data-ttu-id="c0054-118">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="c0054-118">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="c0054-119">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="c0054-119">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="c0054-120">да</span><span class="sxs-lookup"><span data-stu-id="c0054-120">yes</span></span>       |
| [<span data-ttu-id="c0054-121">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="c0054-121">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="c0054-122">да</span><span class="sxs-lookup"><span data-stu-id="c0054-122">yes</span></span>       |
| [<span data-ttu-id="c0054-123">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="c0054-123">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="c0054-124">да</span><span class="sxs-lookup"><span data-stu-id="c0054-124">yes</span></span>       |
| [<span data-ttu-id="c0054-125">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c0054-125">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="c0054-126">Нет</span><span class="sxs-lookup"><span data-stu-id="c0054-126">no</span></span>        |
| [<span data-ttu-id="c0054-127">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c0054-127">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="c0054-128">Нет</span><span class="sxs-lookup"><span data-stu-id="c0054-128">no</span></span>        |
| [<span data-ttu-id="c0054-129">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c0054-129">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="c0054-130">Нет</span><span class="sxs-lookup"><span data-stu-id="c0054-130">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="c0054-131">См. также</span><span class="sxs-lookup"><span data-stu-id="c0054-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c0054-132">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c0054-132">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




