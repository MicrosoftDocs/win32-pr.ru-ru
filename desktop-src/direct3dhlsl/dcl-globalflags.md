---
title: dcl_globalFlags (SM4-ASM)
description: дкл \_ глобалфлагс (SM4-ASM)
ms.assetid: 7289db9e-f0cd-4849-854f-34aa38ec2c2d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e15fce958056f91a41954b987850ad4c5a43e521
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104412245"
---
# <a name="dcl_globalflags-sm4---asm"></a><span data-ttu-id="98fa3-103">дкл \_ глобалфлагс (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="98fa3-103">dcl\_globalFlags (sm4 - asm)</span></span>

<span data-ttu-id="98fa3-104">Объявляет глобальные флаги шейдера.</span><span class="sxs-lookup"><span data-stu-id="98fa3-104">Declares shader global flags.</span></span>



| <span data-ttu-id="98fa3-105">\_ *Флаги* глобалфлагс дкл</span><span class="sxs-lookup"><span data-stu-id="98fa3-105">dcl\_globalFlags *flags*</span></span> |
|--------------------------|



 

<dl> <dt>

<span data-ttu-id="98fa3-106"><span id="flags"></span><span id="FLAGS"></span>*Метки*</span><span class="sxs-lookup"><span data-stu-id="98fa3-106"><span id="flags"></span><span id="FLAGS"></span>*flags*</span></span>
</dt> <dd>

<span data-ttu-id="98fa3-107">\[в \] флаге глобального шейдера.</span><span class="sxs-lookup"><span data-stu-id="98fa3-107">\[in\] A global shader flag.</span></span> <span data-ttu-id="98fa3-108">В настоящий момент определен один флаг.</span><span class="sxs-lookup"><span data-stu-id="98fa3-108">There is currently one flag defined.</span></span>

-   <span data-ttu-id="98fa3-109">РЕФАКТОРИНГ \_ разрешен — разрешает драйверу изменять порядок арифметических операций для оптимизации, как показано здесь.</span><span class="sxs-lookup"><span data-stu-id="98fa3-109">REFACTORING\_ALLOWED - Permits the driver to reorder arithmetic operations for optimization, as shown here.</span></span>

    ```
    // Original code
    a = b*c + b*d + b*e + b*f

    // Reordered code
    a = b*(c + d + e + f)
    // or 
    a = dot4((b,b,b,b), (c,d,e,f))
    ```

    

> [!Note]
>
> <span data-ttu-id="98fa3-110">Изменение порядка арифметических операций может привести к различным результатам.</span><span class="sxs-lookup"><span data-stu-id="98fa3-110">Reordering arithmetic operations may generate different results.</span></span>

 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="98fa3-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="98fa3-111">Remarks</span></span>

<span data-ttu-id="98fa3-112">Эта необязательная инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="98fa3-112">This optional instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="98fa3-113">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="98fa3-113">Vertex Shader</span></span> | <span data-ttu-id="98fa3-114">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="98fa3-114">Geometry Shader</span></span> | <span data-ttu-id="98fa3-115">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="98fa3-115">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="98fa3-116">x</span><span class="sxs-lookup"><span data-stu-id="98fa3-116">x</span></span>             | <span data-ttu-id="98fa3-117">x</span><span class="sxs-lookup"><span data-stu-id="98fa3-117">x</span></span>               | <span data-ttu-id="98fa3-118">x</span><span class="sxs-lookup"><span data-stu-id="98fa3-118">x</span></span>            |



 

<span data-ttu-id="98fa3-119">Эта инструкция включена для облегчения отладки шейдера в сборке; нельзя создать шейдер на языке ассемблера с использованием модели шейдеров 4.</span><span class="sxs-lookup"><span data-stu-id="98fa3-119">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="98fa3-120">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="98fa3-120">Minimum Shader Model</span></span>

<span data-ttu-id="98fa3-121">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="98fa3-121">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="98fa3-122">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="98fa3-122">Shader Model</span></span>                                              | <span data-ttu-id="98fa3-123">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="98fa3-123">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="98fa3-124">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="98fa3-124">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="98fa3-125">да</span><span class="sxs-lookup"><span data-stu-id="98fa3-125">yes</span></span>       |
| [<span data-ttu-id="98fa3-126">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="98fa3-126">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="98fa3-127">да</span><span class="sxs-lookup"><span data-stu-id="98fa3-127">yes</span></span>       |
| [<span data-ttu-id="98fa3-128">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="98fa3-128">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="98fa3-129">да</span><span class="sxs-lookup"><span data-stu-id="98fa3-129">yes</span></span>       |
| [<span data-ttu-id="98fa3-130">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="98fa3-130">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="98fa3-131">Нет</span><span class="sxs-lookup"><span data-stu-id="98fa3-131">no</span></span>        |
| [<span data-ttu-id="98fa3-132">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="98fa3-132">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="98fa3-133">Нет</span><span class="sxs-lookup"><span data-stu-id="98fa3-133">no</span></span>        |
| [<span data-ttu-id="98fa3-134">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="98fa3-134">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="98fa3-135">Нет</span><span class="sxs-lookup"><span data-stu-id="98fa3-135">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="98fa3-136">См. также</span><span class="sxs-lookup"><span data-stu-id="98fa3-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="98fa3-137">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="98fa3-137">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




