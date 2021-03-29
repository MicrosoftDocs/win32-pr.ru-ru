---
title: Справочник по шейдеру ASM
description: Шейдеры управляют программируемым графическим конвейером.
ms.assetid: 2c58815c-83b5-4ae8-a192-ba865b485bd6
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2941f4c32d03187ce08266bf1382cd1d94301ce0
ms.sourcegitcommit: 477b1efe7d9c2f91d5f2ac588a20edf348b1c734
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2019
ms.locfileid: "104983932"
---
# <a name="asm-shader-reference"></a><span data-ttu-id="b5499-103">Справочник по шейдеру ASM</span><span class="sxs-lookup"><span data-stu-id="b5499-103">Asm Shader Reference</span></span>

<span data-ttu-id="b5499-104">Шейдеры управляют программируемым графическим конвейером.</span><span class="sxs-lookup"><span data-stu-id="b5499-104">Shaders drive the programmable graphics pipeline.</span></span>

## <a name="vertex-shader-reference"></a><span data-ttu-id="b5499-105">Справочник по шейдеру вершин</span><span class="sxs-lookup"><span data-stu-id="b5499-105">Vertex Shader Reference</span></span>

-   [<span data-ttu-id="b5499-106">VS \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="b5499-106">vs\_1\_1</span></span>](dx9-graphics-reference-asm-vs-1-1.md)
-   [<span data-ttu-id="b5499-107">VS \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b5499-107">vs\_2\_0</span></span>](dx9-graphics-reference-asm-vs-2-0.md)
-   [<span data-ttu-id="b5499-108">VS \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="b5499-108">vs\_2\_x</span></span>](dx9-graphics-reference-asm-vs-2-x.md)
-   [<span data-ttu-id="b5499-109">VS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b5499-109">vs\_3\_0</span></span>](dx9-graphics-reference-asm-vs-3-0.md)

<span data-ttu-id="b5499-110">[Различия в шейдере вершин](dx9-graphics-reference-asm-vs-differences.md) обобщены различия между версиями шейдеров вершин.</span><span class="sxs-lookup"><span data-stu-id="b5499-110">[Vertex Shader Differences](dx9-graphics-reference-asm-vs-differences.md) summarizes the differences between vertex shader versions.</span></span>

## <a name="pixel-shader-reference"></a><span data-ttu-id="b5499-111">Справочник по шейдеру пикселей</span><span class="sxs-lookup"><span data-stu-id="b5499-111">Pixel Shader Reference</span></span>

-   [<span data-ttu-id="b5499-112">PS \_ 1 \_ 1, PS \_ 1 \_ 2, PS \_ 1 \_ 3, PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="b5499-112">ps\_1\_1, ps\_1\_2, ps\_1\_3, ps\_1\_4</span></span>](dx9-graphics-reference-asm-ps-1-x.md)
-   [<span data-ttu-id="b5499-113">PS \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b5499-113">ps\_2\_0</span></span>](dx9-graphics-reference-asm-ps-2-0.md)
-   [<span data-ttu-id="b5499-114">PS \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="b5499-114">ps\_2\_x</span></span>](dx9-graphics-reference-asm-ps-2-x.md)
-   [<span data-ttu-id="b5499-115">PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b5499-115">ps\_3\_0</span></span>](dx9-graphics-reference-asm-ps-3-0.md)

<span data-ttu-id="b5499-116">[Различия шейдера пикселей](dx9-graphics-reference-asm-ps-differences.md) обобщены различия между версиями построителей текстуры.</span><span class="sxs-lookup"><span data-stu-id="b5499-116">[Pixel Shader Differences](dx9-graphics-reference-asm-ps-differences.md) summarizes the differences between pixel shader versions.</span></span>

## <a name="shader-model-4-and-5-reference"></a><span data-ttu-id="b5499-117">Справочник по модели шейдеров 4 и 5</span><span class="sxs-lookup"><span data-stu-id="b5499-117">Shader Model 4 and 5 Reference</span></span>

<span data-ttu-id="b5499-118">В разделах [«Сборка» и «](dx-graphics-hlsl-sm4-asm.md) шейдер» модели построителя текстур [5](shader-model-5-assembly--directx-hlsl-.md) описываются инструкции, поддерживаемые в модели шейдеров 4 и 5.</span><span class="sxs-lookup"><span data-stu-id="b5499-118">The [Shader Model 4 Assembly](dx-graphics-hlsl-sm4-asm.md) and [Shader Model 5 Assembly](shader-model-5-assembly--directx-hlsl-.md) sections describe the instructions that shader model 4 and 5 support.</span></span>

## <a name="behavior-of-constant-registers-in-assembly-shaders"></a><span data-ttu-id="b5499-119">Поведение регистров констант в шейдерах сборки</span><span class="sxs-lookup"><span data-stu-id="b5499-119">Behavior of Constant Registers in Assembly Shaders</span></span>

<span data-ttu-id="b5499-120">Существует два способа установки регистров констант в шейдере сборки:</span><span class="sxs-lookup"><span data-stu-id="b5499-120">There are two ways to set constant registers in an assembly shader:</span></span>

-   <span data-ttu-id="b5499-121">Объявите константу шейдера в коде сборки с помощью одной из \* инструкций DEF.</span><span class="sxs-lookup"><span data-stu-id="b5499-121">Declare a shader constant in assembly code using one of the def\* instructions.</span></span>
-   <span data-ttu-id="b5499-122">Используйте один из \* \* \* \* методов API Set шадерконстант.</span><span class="sxs-lookup"><span data-stu-id="b5499-122">Use one of the Set\*\*\*ShaderConstant\* API methods.</span></span>

### <a name="direct3d-9-shader-constants"></a><span data-ttu-id="b5499-123">Константы шейдера Direct3D 9</span><span class="sxs-lookup"><span data-stu-id="b5499-123">Direct3D 9 Shader Constants</span></span>

<span data-ttu-id="b5499-124">В Direct3D 9 время существования определенных констант в заданном шейдере ограничено выполнением только этого шейдера (и не может быть переопределяемым).</span><span class="sxs-lookup"><span data-stu-id="b5499-124">In Direct3D 9 the lifetime of defined constants in a given shader is confined to the execution of that shader only (and is non-overridable).</span></span> <span data-ttu-id="b5499-125">Определенные константы в Direct3D 9 не имеют побочных эффектов вне шейдера.</span><span class="sxs-lookup"><span data-stu-id="b5499-125">Defined constants in Direct3D 9 have no side effects outside of the shader.</span></span>

<span data-ttu-id="b5499-126">Ниже приведен пример использования Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="b5499-126">Here's an example using Direct3D 9:</span></span>


```
Given: 
    Create shader1 which references c4 and defines it with the def instruction

Scenario 1:
    Call Set***Shader shader1
    Call Set***ShaderConstant* to set c4
    Call Draw
    Result: The shader will see the def'd value in c4

    
Given: 
    Scenario 1 has just completed
    Create shader2 (which references c4 but does not use the def instruction
      to define it) 

Scenario 2: 
    Call Set***Shader shader2
    Call Draw
    Result: The shader will see the value last set in c4 by 
     Set***ShaderConstant* in scenario 1. This is because shader 2 
     didn't def c4.
```



<span data-ttu-id="b5499-127">В Direct3D 9 вызов get \* \* \* шадерконстант \* будет получать только постоянные значения, заданные через Set \* \* \* шадерконстант \* .</span><span class="sxs-lookup"><span data-stu-id="b5499-127">In Direct3D 9, calling Get\*\*\*ShaderConstant\* will only retrieve constant values set via Set\*\*\*ShaderConstant\*.</span></span>

### <a name="direct3d-8-shader-constants"></a><span data-ttu-id="b5499-128">Константы шейдера Direct3D 8</span><span class="sxs-lookup"><span data-stu-id="b5499-128">Direct3D 8 Shader Constants</span></span>

<span data-ttu-id="b5499-129">Это поведение отличается в Direct3D 8. x.</span><span class="sxs-lookup"><span data-stu-id="b5499-129">This behavior is different in Direct3D 8.x.</span></span>


```
Given:
    Create shader1 which references c4 and defines it with the def instruction

Scenario 1 (repeated with Direct3D 8):
    Call Set***Shader with shader1
    Call Set***ShaderConstant to set c4
    Call Draw
    Result: The shader will see the value in c4 from Set***ShaderConstant
```



<span data-ttu-id="b5499-130">В Direct3D 8. x Set \* \* \* шадерконстант вступает в силу немедленно.</span><span class="sxs-lookup"><span data-stu-id="b5499-130">In Direct3D 8.x Set\*\*\*ShaderConstant takes effect immediately.</span></span> <span data-ttu-id="b5499-131">Рассмотрим следующий сценарий.</span><span class="sxs-lookup"><span data-stu-id="b5499-131">Consider this scenario:</span></span>


```
Given:
    Create shader1 which references c4 and defines it with the def instruction
    
Scenario 3:
    Call Set***Shader with shader1
    Call Draw
    Result: The shader will see the def'd value in c4

Given:
    Scenario 3 has just completed
    Create shader2 (which references c4 but does not use the def instruction 
      to define it)     
    
Scenario 4 :    
    Call Set***Shader with shader2
    Call Draw
    Result: The shader will see the def'd value in c4 (set by def in shader 1)
```



<span data-ttu-id="b5499-132">Нежелательный результат заключается в том, что порядок, в котором задаются шейдеры, может повлиять на наблюдаемое поведение отдельных шейдеров.</span><span class="sxs-lookup"><span data-stu-id="b5499-132">The undesirable result is that the order in which the shaders are set could affect the observed behavior of individual shaders.</span></span>

## <a name="shader-driver-model-requirements"></a><span data-ttu-id="b5499-133">Требования к модели драйвера шейдеров</span><span class="sxs-lookup"><span data-stu-id="b5499-133">Shader Driver Model Requirements</span></span>

<span data-ttu-id="b5499-134">Интерфейсы Direct3D 9 ограничены драйверами интерфейса драйвера устройства (DDI), поддерживающими DirectX 7 и выше.</span><span class="sxs-lookup"><span data-stu-id="b5499-134">Direct3D 9 interfaces are restricted to device driver interface (DDI) drivers that are DirectX 7-level and above.</span></span> <span data-ttu-id="b5499-135">Чтобы проверить уровень DDI, запустите [средство диагностики DirectX](https://msdn.microsoft.com/library/Ee416792(v=VS.85).aspx) и изучите сохраненный текстовый файл.</span><span class="sxs-lookup"><span data-stu-id="b5499-135">To check the DDI level, run the [DirectX Diagnostic Tool](https://msdn.microsoft.com/library/Ee416792(v=VS.85).aspx) and examine the saved text file.</span></span>

<span data-ttu-id="b5499-136">Для справки интерфейсы Direct3D 8 работают только с драйверами DDI, которые имеют версию DirectX 6 и выше.</span><span class="sxs-lookup"><span data-stu-id="b5499-136">For reference, Direct3D 8 interfaces work only on DDI drivers that are DirectX 6-level and above.</span></span>

## <a name="shader-binary-format"></a><span data-ttu-id="b5499-137">Двоичный формат шейдера</span><span class="sxs-lookup"><span data-stu-id="b5499-137">Shader Binary Format</span></span>

<span data-ttu-id="b5499-138">Побитовая структура потока инструкций шейдера определена в D3d9types. h.</span><span class="sxs-lookup"><span data-stu-id="b5499-138">The bitwise layout of the shader instruction stream is defined in D3d9types.h.</span></span> <span data-ttu-id="b5499-139">Если вы хотите разработать собственные компиляторы шейдеров или средства построения и хотите получить дополнительные сведения о потоке маркера шейдера, обратитесь к комплекту средств разработки драйверов Direct3D 9 (DDK).</span><span class="sxs-lookup"><span data-stu-id="b5499-139">If you want to design your own shader compiler or construction tools and you want more information about the shader token stream, refer to the Direct3D 9 Driver Development Kit (DDK).</span></span>

## <a name="c-like-shader-language"></a><span data-ttu-id="b5499-140">Язык шейдера, похожего на C</span><span class="sxs-lookup"><span data-stu-id="b5499-140">C-like Shader Language</span></span>

<span data-ttu-id="b5499-141">См. раздел [Справочник по HLSL](dx-graphics-hlsl-reference.md) для работы с языком шейдера, похожим на C.</span><span class="sxs-lookup"><span data-stu-id="b5499-141">See [HLSL Reference](dx-graphics-hlsl-reference.md) to experience a C-like shader language.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b5499-142">См. также</span><span class="sxs-lookup"><span data-stu-id="b5499-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5499-143">Справочник по HLSL</span><span class="sxs-lookup"><span data-stu-id="b5499-143">Reference for HLSL</span></span>](dx-graphics-hlsl-reference.md)
</dt> </dl>

 

 




