---
title: ps_1_1, ps_1_2, ps_1_3, ps_1_4
description: Ассемблер построителя текстуры состоит из набора инструкций, которые работают с данными пикселей, содержащимися в регистрах.
ms.assetid: 51b59f98-2fa8-4280-bc36-f4328a646168
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 761721a4de64e8a9168bcfea49ce7adf567ea7ef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104252740"
---
# <a name="ps_1_1-ps_1_2-ps_1_3-ps_1_4"></a><span data-ttu-id="157b4-103">PS \_ 1 \_ 1, PS \_ 1 \_ 2, PS \_ 1 \_ 3, PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="157b4-103">ps\_1\_1, ps\_1\_2, ps\_1\_3, ps\_1\_4</span></span>

<span data-ttu-id="157b4-104">Ассемблер построителя текстуры состоит из набора инструкций, которые работают с данными пикселей, содержащимися в регистрах.</span><span class="sxs-lookup"><span data-stu-id="157b4-104">The pixel shader assembler is made up of a set of instructions that operate on pixel data contained in registers.</span></span> <span data-ttu-id="157b4-105">Операции выражаются в виде инструкций, составляющих оператор, и одного или нескольких операндов.</span><span class="sxs-lookup"><span data-stu-id="157b4-105">Operations are expressed as instructions comprised of an operator and one or more operands.</span></span> <span data-ttu-id="157b4-106">Инструкции используют регистры для перемещения данных построителя текстуры ALU и из него.</span><span class="sxs-lookup"><span data-stu-id="157b4-106">Instructions use registers to transfer data in and out of the pixel shader ALU.</span></span> <span data-ttu-id="157b4-107">Регистры также могут использоваться некоторыми инструкциями для хранения временных результатов.</span><span class="sxs-lookup"><span data-stu-id="157b4-107">Registers can also be used by some instructions to hold temporary results.</span></span>

> [!Note]  
> <span data-ttu-id="157b4-108">Поддержка HLSL для Pixel Shader 1. x является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="157b4-108">HLSL support for pixel shader 1.x is deprecated.</span></span>

 

## <a name="instructions"></a><span data-ttu-id="157b4-109">Инструкции</span><span class="sxs-lookup"><span data-stu-id="157b4-109">Instructions</span></span>

<span data-ttu-id="157b4-110">Существуют две основные категории инструкций шейдера пикселей: арифметические инструкции и инструкции по адресации текстур.</span><span class="sxs-lookup"><span data-stu-id="157b4-110">There are two main categories of pixel shader instructions: arithmetic instructions and texture addressing instructions.</span></span> <span data-ttu-id="157b4-111">Арифметические инструкции изменяют данные цвета.</span><span class="sxs-lookup"><span data-stu-id="157b4-111">Arithmetic instructions modify color data.</span></span> <span data-ttu-id="157b4-112">Операции адресации текстур обрабатывают данные координат текстуры и в большинстве случаев представляют собой образец текстуры.</span><span class="sxs-lookup"><span data-stu-id="157b4-112">Texture addressing operations process texture coordinate data and in most cases, sample a texture.</span></span> <span data-ttu-id="157b4-113">Инструкции шейдера пикселей выполняются на пиксельном уровне; то есть у них нет сведений о других пикселях в конвейере.</span><span class="sxs-lookup"><span data-stu-id="157b4-113">Pixel shader instructions are run on a per-pixel basis; that is, they have no knowledge of other pixels in the pipeline.</span></span>

<span data-ttu-id="157b4-114">Каждая из них использует один слот, но арифметические инструкции можно связать, чтобы включить как компоненты цвета (RGB), так и инструкции альфа-компонента в одном слоте.</span><span class="sxs-lookup"><span data-stu-id="157b4-114">Texture addressing instructions each consume one slot, but arithmetic instructions can be paired to enable both color components (RGB) and an alpha component instruction in a single slot.</span></span>

<span data-ttu-id="157b4-115">[PS \_ 1 \_ 1, PS \_ 1 \_ 2, PS \_ 1 \_ 3, \_ инструкции PS 1 \_ 4](dx9-graphics-reference-asm-ps-instructions-ps-1-x.md) содержат список доступных инструкций.</span><span class="sxs-lookup"><span data-stu-id="157b4-115">[ps\_1\_1, ps\_1\_2, ps\_1\_3, ps\_1\_4 Instructions](dx9-graphics-reference-asm-ps-instructions-ps-1-x.md) contains a list of the available instructions.</span></span>

<span data-ttu-id="157b4-116">Если включена многовыборка, шейдеры пикселей выполняются только один раз на пиксель, а не один раз для каждого подпикселя.</span><span class="sxs-lookup"><span data-stu-id="157b4-116">When multisampling is enabled, pixel shaders only get run once per pixel, not once for every subpixel.</span></span> <span data-ttu-id="157b4-117">При множественной выборке увеличивается только разрешение краев многоугольников, а также уровней глубины и трафарета.</span><span class="sxs-lookup"><span data-stu-id="157b4-117">Multisampling only increases the resolution of polygon edges, as well as depth and stencil tests.</span></span> <span data-ttu-id="157b4-118">Например, если включена многовыборочная выборка 3x3, а растровый треугольник обнаруживается, чтобы охватить пять девяти подпикселей для определенного пикселя, построитель текстуры выполняется один раз, и один и тот же цветовый результат применяется ко всем пяти подпикселям.</span><span class="sxs-lookup"><span data-stu-id="157b4-118">For example, if 3x3 multisampling is enabled, and a triangle being rasterized is found to cover five of the nine subpixels for a particular pixel, the pixel shader gets run once and the same color result is applied to all five subpixels.</span></span>

## <a name="registers"></a><span data-ttu-id="157b4-119">Регистры</span><span class="sxs-lookup"><span data-stu-id="157b4-119">Registers</span></span>

<span data-ttu-id="157b4-120">[в \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ регистрах PS 1 1](dx9-graphics-reference-asm-ps-registers-ps-1-x.md) PS 1 2 PS 1 3 PS 1 4 перечислены различные регистры, используемые шейдером ALU.</span><span class="sxs-lookup"><span data-stu-id="157b4-120">[ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md) lists the different registers used by the shader ALU.</span></span>

## <a name="modifiers"></a><span data-ttu-id="157b4-121">Модификаторы</span><span class="sxs-lookup"><span data-stu-id="157b4-121">Modifiers</span></span>

<span data-ttu-id="157b4-122">[Модификаторы для PS \_ 1 \_ X](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-1-x.md) можно использовать для изменения функциональных возможностей инструкции или чтения или записи данных в регистр.</span><span class="sxs-lookup"><span data-stu-id="157b4-122">[Modifiers for ps\_1\_X](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-1-x.md) can be used to change the functionality of an instruction, or the data read from or written to a register.</span></span>

<span data-ttu-id="157b4-123">Для Direct3D 9 требуются промежуточные вычисления, чтобы поддерживать по крайней мере 8-разрядную точность для всех форматов поверхности.</span><span class="sxs-lookup"><span data-stu-id="157b4-123">Direct3D 9 requires intermediate computations to maintain at least 8-bit precision for all surface formats.</span></span> <span data-ttu-id="157b4-124">Рекомендуется использовать как большую точность (12-разрядную) для внутренних математических операций, так и насыщенность до 8 бит между стадиями текстуры.</span><span class="sxs-lookup"><span data-stu-id="157b4-124">Both higher precision (12-bit) for in-stage math, and saturation to 8-bits between texture stages are recommended.</span></span> <span data-ttu-id="157b4-125">Не поддерживаются изменяемые режимы округления или исключения.</span><span class="sxs-lookup"><span data-stu-id="157b4-125">No modifiable rounding modes or exceptions are supported.</span></span> <span data-ttu-id="157b4-126">Умножение должно поддерживаться с точностью до ближайшего значения, чтобы обеспечить минимальную точность.</span><span class="sxs-lookup"><span data-stu-id="157b4-126">Multiplication should be supported with a round-to-nearest precision to keep precision loss to a minimum.</span></span>

## <a name="sampler-count"></a><span data-ttu-id="157b4-127">Число образцов</span><span class="sxs-lookup"><span data-stu-id="157b4-127">Sampler Count</span></span>

<span data-ttu-id="157b4-128">Число доступных образцов для пробных текстур:</span><span class="sxs-lookup"><span data-stu-id="157b4-128">The number of texture samplers available is:</span></span>

-   <span data-ttu-id="157b4-129">Для PS \_ 1 \_ 0-PS \_ 1 \_ 3 Максимальное значение равно 4.</span><span class="sxs-lookup"><span data-stu-id="157b4-129">For ps\_1\_0 - ps\_1\_3, the maximum is 4.</span></span>
-   <span data-ttu-id="157b4-130">Для PS \_ 1 \_ 4 максимальное значение равно 6.</span><span class="sxs-lookup"><span data-stu-id="157b4-130">For ps\_1\_4, the maximum is 6.</span></span>

## <a name="related-topics"></a><span data-ttu-id="157b4-131">См. также</span><span class="sxs-lookup"><span data-stu-id="157b4-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="157b4-132">Шейдеры пикселей</span><span class="sxs-lookup"><span data-stu-id="157b4-132">Pixel Shaders</span></span>](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 




