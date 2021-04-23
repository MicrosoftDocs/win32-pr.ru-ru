---
title: Вырезать (SM4-ASM)
description: Инструкция шейдера геометрии, которая завершает текущую топологию примитива (если были выданы вершины) и запускает новую топологию типа, объявленного шейдером Geometry.
ms.assetid: 9B28E33D-F518-4844-BE3F-BE61B5F08B4F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c462d2f4dc2e0c6b4076f577610c93794e890af
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104983824"
---
# <a name="cut-sm4---asm"></a><span data-ttu-id="310e4-103">Вырезать (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="310e4-103">cut (sm4 - asm)</span></span>

<span data-ttu-id="310e4-104">Инструкция шейдера геометрии, которая завершает текущую топологию примитива (если были выданы вершины) и запускает новую топологию типа, объявленного шейдером Geometry.</span><span class="sxs-lookup"><span data-stu-id="310e4-104">Geometry Shader instruction that completes the current primitive topology (if any vertices have been emitted), and starts a new topology of the type declared by the Geometry Shader.</span></span>



| <span data-ttu-id="310e4-105">вырезать</span><span class="sxs-lookup"><span data-stu-id="310e4-105">cut</span></span> |
|-----|



 

## <a name="remarks"></a><span data-ttu-id="310e4-106">Примечания</span><span class="sxs-lookup"><span data-stu-id="310e4-106">Remarks</span></span>

<span data-ttu-id="310e4-107">Когда выполняется **Cut** , первое, что происходит, это то, что все ранее выпущенная топология при вызове шейдера Geometry завершена.</span><span class="sxs-lookup"><span data-stu-id="310e4-107">When **cut** is executed, the first thing that happens is that any previously emitted topology by the Geometry Shader invocation is completed.</span></span> <span data-ttu-id="310e4-108">Если для предыдущей простой топологии не было создано достаточное количество вершин, они отбрасываются.</span><span class="sxs-lookup"><span data-stu-id="310e4-108">If not enough vertices were emitted for the previous primitive topology, they are discarded.</span></span> <span data-ttu-id="310e4-109">Поскольку единственными доступными выходными топологиями для шейдера Geometry являются поинтлист, линестрип и трианглестрип, то при **вырезании** не осталось ни одного из оставшихся вершин.</span><span class="sxs-lookup"><span data-stu-id="310e4-109">Because the only available output topologies for the Geometry Shader are pointlist, linestrip, and trianglestrip, there are never any leftover vertices upon **cut**.</span></span>

<span data-ttu-id="310e4-110">После завершения предыдущей топологии, если таковая имеется, инструкция **Cut** приводит к запуску новой топологии с использованием топологии, объявленной в качестве выходных данных шейдера геометрии.</span><span class="sxs-lookup"><span data-stu-id="310e4-110">After the previous topology, if any, is completed, **cut** causes a new topology to begin, using the topology declared as the Geometry Shader output.</span></span>

## <a name="restrictions"></a><span data-ttu-id="310e4-111">Ограничения</span><span class="sxs-lookup"><span data-stu-id="310e4-111">Restrictions</span></span>

-   <span data-ttu-id="310e4-112">Инструкция **Cut** применяется только к шейдеру Geometry.</span><span class="sxs-lookup"><span data-stu-id="310e4-112">The **cut** instruction applies only to the Geometry Shader.</span></span>
-   <span data-ttu-id="310e4-113">**вырезание** может появляться любое количество раз в шейдере Geometry, в том числе в элементе управления потоком.</span><span class="sxs-lookup"><span data-stu-id="310e4-113">**cut** can appear any number of times in the Geometry Shader, including within flow control.</span></span>
-   <span data-ttu-id="310e4-114">Если шейдер геометрии завершается и порождены вершины, топология, которую они создают, завершается, как если бы операция **вырезания** была выполнена в качестве последней инструкции.</span><span class="sxs-lookup"><span data-stu-id="310e4-114">If the Geometry Shader ends and vertices have been emitted, the topology they are building is completed, as if a **cut** was executed as the last instruction.</span></span>
-   <span data-ttu-id="310e4-115">Если были объявлены потоки, вместо **вырезания** необходимо использовать [Вырезать \_ поток](cut-stream---sm5---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="310e4-115">If streams have been declared, then [cut\_stream](cut-stream---sm5---asm-.md) must be used instead of **cut**.</span></span>

<span data-ttu-id="310e4-116">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="310e4-116">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="310e4-117">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="310e4-117">Vertex Shader</span></span> | <span data-ttu-id="310e4-118">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="310e4-118">Geometry Shader</span></span> | <span data-ttu-id="310e4-119">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="310e4-119">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               | <span data-ttu-id="310e4-120">x</span><span class="sxs-lookup"><span data-stu-id="310e4-120">x</span></span>               |              |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="310e4-121">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="310e4-121">Minimum Shader Model</span></span>

<span data-ttu-id="310e4-122">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="310e4-122">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="310e4-123">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="310e4-123">Shader Model</span></span>                                              | <span data-ttu-id="310e4-124">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="310e4-124">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="310e4-125">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="310e4-125">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="310e4-126">да</span><span class="sxs-lookup"><span data-stu-id="310e4-126">yes</span></span>       |
| [<span data-ttu-id="310e4-127">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="310e4-127">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="310e4-128">да</span><span class="sxs-lookup"><span data-stu-id="310e4-128">yes</span></span>       |
| [<span data-ttu-id="310e4-129">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="310e4-129">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="310e4-130">да</span><span class="sxs-lookup"><span data-stu-id="310e4-130">yes</span></span>       |
| [<span data-ttu-id="310e4-131">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="310e4-131">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="310e4-132">Нет</span><span class="sxs-lookup"><span data-stu-id="310e4-132">no</span></span>        |
| [<span data-ttu-id="310e4-133">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="310e4-133">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="310e4-134">Нет</span><span class="sxs-lookup"><span data-stu-id="310e4-134">no</span></span>        |
| [<span data-ttu-id="310e4-135">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="310e4-135">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="310e4-136">Нет</span><span class="sxs-lookup"><span data-stu-id="310e4-136">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="310e4-137">См. также</span><span class="sxs-lookup"><span data-stu-id="310e4-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="310e4-138">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="310e4-138">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




