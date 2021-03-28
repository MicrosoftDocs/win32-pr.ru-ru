---
title: dcl_output Одепс (SM4-ASM)
description: дкл \_ Output одепс (SM4-ASM)
ms.assetid: 7ee3026d-507f-4aa8-8335-d92c5f649f46
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 43580a542c1a66961cfa7434c65cd8d271fb0367
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104335635"
---
# <a name="dcl_output-odepth-sm4---asm"></a><span data-ttu-id="c88bc-103">дкл \_ Output одепс (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="c88bc-103">dcl\_output oDepth (sm4 - asm)</span></span>

<span data-ttu-id="c88bc-104">Объявляет, что построитель текстуры будет использовать регистр глубины вывода.</span><span class="sxs-lookup"><span data-stu-id="c88bc-104">Declares that a pixel shader will use the output-depth register.</span></span>



| <span data-ttu-id="c88bc-105">дкл \_ выходной одепс</span><span class="sxs-lookup"><span data-stu-id="c88bc-105">dcl\_output oDepth</span></span> |
|--------------------|



 

<span data-ttu-id="c88bc-106">Значение в регистре глубины вывода используется при сравнении глубины (если включена функция глубины сравнения).</span><span class="sxs-lookup"><span data-stu-id="c88bc-106">The value in the output-depth register is used during a depth comparison (if depth compare is enabled).</span></span>

<span data-ttu-id="c88bc-107">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="c88bc-107">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="c88bc-108">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="c88bc-108">Vertex Shader</span></span> | <span data-ttu-id="c88bc-109">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="c88bc-109">Geometry Shader</span></span> | <span data-ttu-id="c88bc-110">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="c88bc-110">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               |                 | <span data-ttu-id="c88bc-111">x</span><span class="sxs-lookup"><span data-stu-id="c88bc-111">x</span></span>            |



 

<span data-ttu-id="c88bc-112">Эта инструкция включена для облегчения отладки шейдера в сборке; нельзя создать шейдер на языке ассемблера с использованием модели шейдеров 4.</span><span class="sxs-lookup"><span data-stu-id="c88bc-112">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="c88bc-113">Например, .</span><span class="sxs-lookup"><span data-stu-id="c88bc-113">Example</span></span>

<span data-ttu-id="c88bc-114">Вот несколько примеров.</span><span class="sxs-lookup"><span data-stu-id="c88bc-114">Here are some examples.</span></span>


```
dcl_output oDepth
```



## <a name="minimum-shader-model"></a><span data-ttu-id="c88bc-115">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="c88bc-115">Minimum Shader Model</span></span>

<span data-ttu-id="c88bc-116">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="c88bc-116">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="c88bc-117">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="c88bc-117">Shader Model</span></span>                                              | <span data-ttu-id="c88bc-118">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="c88bc-118">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="c88bc-119">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="c88bc-119">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="c88bc-120">да</span><span class="sxs-lookup"><span data-stu-id="c88bc-120">yes</span></span>       |
| [<span data-ttu-id="c88bc-121">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="c88bc-121">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="c88bc-122">да</span><span class="sxs-lookup"><span data-stu-id="c88bc-122">yes</span></span>       |
| [<span data-ttu-id="c88bc-123">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="c88bc-123">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="c88bc-124">да</span><span class="sxs-lookup"><span data-stu-id="c88bc-124">yes</span></span>       |
| [<span data-ttu-id="c88bc-125">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c88bc-125">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="c88bc-126">Нет</span><span class="sxs-lookup"><span data-stu-id="c88bc-126">no</span></span>        |
| [<span data-ttu-id="c88bc-127">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c88bc-127">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="c88bc-128">Нет</span><span class="sxs-lookup"><span data-stu-id="c88bc-128">no</span></span>        |
| [<span data-ttu-id="c88bc-129">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c88bc-129">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="c88bc-130">Нет</span><span class="sxs-lookup"><span data-stu-id="c88bc-130">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="c88bc-131">См. также</span><span class="sxs-lookup"><span data-stu-id="c88bc-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c88bc-132">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c88bc-132">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




