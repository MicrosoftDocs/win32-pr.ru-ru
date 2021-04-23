---
title: Модификаторы для ps_2_0 и более поздних версий
description: Модификаторы инструкций влияют на результат инструкции перед его записью в регистр назначения.
ms.assetid: eb2a8a1f-51bc-4516-b679-a8fb25b0dda0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7141576b80b7a05a3e61ee9a98fa36958b1d5530
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103889220"
---
# <a name="modifiers-for-ps_2_0-and-above"></a><span data-ttu-id="4ddfc-103">Модификаторы для PS \_ 2 \_ и более поздних версий</span><span class="sxs-lookup"><span data-stu-id="4ddfc-103">Modifiers for ps\_2\_0 and Above</span></span>

<span data-ttu-id="4ddfc-104">Модификаторы инструкций влияют на результат инструкции перед его записью в регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="4ddfc-104">Instruction modifiers affect the result of the instruction before it is written into the destination register.</span></span>

<span data-ttu-id="4ddfc-105">В этом разделе содержатся справочные сведения по модификаторам инструкций, реализованным построителем пиксельных шейдеров версии 2 \_ 0 и выше.</span><span class="sxs-lookup"><span data-stu-id="4ddfc-105">This section contains reference information for the instruction modifiers implemented by pixel shader version 2\_0 and above.</span></span>



| <span data-ttu-id="4ddfc-106">Имя</span><span class="sxs-lookup"><span data-stu-id="4ddfc-106">Name</span></span>                                     | <span data-ttu-id="4ddfc-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4ddfc-107">Syntax</span></span>     | <span data-ttu-id="4ddfc-108">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4ddfc-108">2\_0</span></span> | <span data-ttu-id="4ddfc-109">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="4ddfc-109">2\_x</span></span> | <span data-ttu-id="4ddfc-110">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="4ddfc-110">2\_sw</span></span> | <span data-ttu-id="4ddfc-111">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4ddfc-111">3\_0</span></span> | <span data-ttu-id="4ddfc-112">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="4ddfc-112">3\_sw</span></span> |
|------------------------------------------|------------|------|------|-------|------|-------|
| [<span data-ttu-id="4ddfc-113">Центроид</span><span class="sxs-lookup"><span data-stu-id="4ddfc-113">Centroid</span></span>](#centroid)                    | <span data-ttu-id="4ddfc-114">\_центроид</span><span class="sxs-lookup"><span data-stu-id="4ddfc-114">\_centroid</span></span> | <span data-ttu-id="4ddfc-115">x</span><span class="sxs-lookup"><span data-stu-id="4ddfc-115">x</span></span>    | <span data-ttu-id="4ddfc-116">x</span><span class="sxs-lookup"><span data-stu-id="4ddfc-116">x</span></span>    | <span data-ttu-id="4ddfc-117">x</span><span class="sxs-lookup"><span data-stu-id="4ddfc-117">x</span></span>     | <span data-ttu-id="4ddfc-118">x</span><span class="sxs-lookup"><span data-stu-id="4ddfc-118">x</span></span>    | <span data-ttu-id="4ddfc-119">x</span><span class="sxs-lookup"><span data-stu-id="4ddfc-119">x</span></span>     |
| [<span data-ttu-id="4ddfc-120">Частичная \_ точность</span><span class="sxs-lookup"><span data-stu-id="4ddfc-120">Partial\_Precision</span></span>](#partial-precision) | <span data-ttu-id="4ddfc-121">\_PP</span><span class="sxs-lookup"><span data-stu-id="4ddfc-121">\_pp</span></span>       | <span data-ttu-id="4ddfc-122">x</span><span class="sxs-lookup"><span data-stu-id="4ddfc-122">x</span></span>    | <span data-ttu-id="4ddfc-123">x</span><span class="sxs-lookup"><span data-stu-id="4ddfc-123">x</span></span>    | <span data-ttu-id="4ddfc-124">x</span><span class="sxs-lookup"><span data-stu-id="4ddfc-124">x</span></span>     | <span data-ttu-id="4ddfc-125">x</span><span class="sxs-lookup"><span data-stu-id="4ddfc-125">x</span></span>    | <span data-ttu-id="4ddfc-126">x</span><span class="sxs-lookup"><span data-stu-id="4ddfc-126">x</span></span>     |
| [<span data-ttu-id="4ddfc-127">Saturate</span><span class="sxs-lookup"><span data-stu-id="4ddfc-127">Saturate</span></span>](#saturate)                    | <span data-ttu-id="4ddfc-128">\_Кот</span><span class="sxs-lookup"><span data-stu-id="4ddfc-128">\_sat</span></span>      | <span data-ttu-id="4ddfc-129">x</span><span class="sxs-lookup"><span data-stu-id="4ddfc-129">x</span></span>    | <span data-ttu-id="4ddfc-130">x</span><span class="sxs-lookup"><span data-stu-id="4ddfc-130">x</span></span>    | <span data-ttu-id="4ddfc-131">x</span><span class="sxs-lookup"><span data-stu-id="4ddfc-131">x</span></span>     | <span data-ttu-id="4ddfc-132">x</span><span class="sxs-lookup"><span data-stu-id="4ddfc-132">x</span></span>    | <span data-ttu-id="4ddfc-133">x</span><span class="sxs-lookup"><span data-stu-id="4ddfc-133">x</span></span>     |



 

## <a name="centroid"></a><span data-ttu-id="4ddfc-134">Центроид</span><span class="sxs-lookup"><span data-stu-id="4ddfc-134">Centroid</span></span>

<span data-ttu-id="4ddfc-135">Модификатор центроид является необязательным модификатором, который замещает интерполяцию атрибута в диапазоне примитива, если многовыборочный пиксельный центр не охватывается примитивом.</span><span class="sxs-lookup"><span data-stu-id="4ddfc-135">The centroid modifier is an optional modifier that clamps attribute interpolation within the range of the primitive when a multisample pixel center is not covered by the primitive.</span></span> <span data-ttu-id="4ddfc-136">Это можно увидеть на [выборки центроид](https://msdn.microsoft.com/library/ee415231(VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="4ddfc-136">This can be seen in [Centroid Sampling](https://msdn.microsoft.com/library/ee415231(VS.85).aspx).</span></span>

<span data-ttu-id="4ddfc-137">К инструкции сборки можно применить модификатор центроид, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="4ddfc-137">You can apply the centroid modifier to an assembly instruction as shown here:</span></span>


```
dcl_texcoord0_centroid v0
```



<span data-ttu-id="4ddfc-138">Модификатор центроид также можно применить к семантике, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="4ddfc-138">You can also apply the centroid modifier to a semantic as shown here:</span></span>


```
float4 TexturePointCentroidPS( float4 TexCoord : TEXCOORD0_centroid ) : COLOR0
{
    return tex2D( PointSampler, TexCoord );
}
```



<span data-ttu-id="4ddfc-139">Кроме того, все [входные цветовые регистры](dx9-graphics-reference-asm-ps-registers-input-color.md) (v \# ), объявленные с помощью семантики цвета, будут автоматически применены к центроид.</span><span class="sxs-lookup"><span data-stu-id="4ddfc-139">In addition, any [Input Color Register](dx9-graphics-reference-asm-ps-registers-input-color.md) (v\#) declared with a color semantic will automatically have centroid applied.</span></span> <span data-ttu-id="4ddfc-140">Не гарантируется точность градиентов, вычисленных на основе атрибутов, которые центроид выборка.</span><span class="sxs-lookup"><span data-stu-id="4ddfc-140">Gradients computed from attributes that are centroid sampled are not guaranteed to be accurate.</span></span>

## <a name="partial-precision"></a><span data-ttu-id="4ddfc-141">Частичная точность</span><span class="sxs-lookup"><span data-stu-id="4ddfc-141">Partial Precision</span></span>

<span data-ttu-id="4ddfc-142">Модификатор инструкции частичной точности ( \_ PP) указывает области, где приемлема точность, при условии, что базовая реализация поддерживает ее.</span><span class="sxs-lookup"><span data-stu-id="4ddfc-142">The partial precision instruction modifier (\_pp) indicates areas where partial precision is acceptable, provided that the underlying implementation supports it.</span></span> <span data-ttu-id="4ddfc-143">Реализации всегда могут игнорировать модификатор и выполнять затронутые операции в полной точности.</span><span class="sxs-lookup"><span data-stu-id="4ddfc-143">Implementations are always free to ignore the modifier and perform the affected operations in full precision.</span></span>

<span data-ttu-id="4ddfc-144">\_Модификатор PP может находиться в двух контекстах:</span><span class="sxs-lookup"><span data-stu-id="4ddfc-144">The \_pp modifier can occur in two contexts:</span></span>

-   <span data-ttu-id="4ddfc-145">Для объявления координат текстуры, чтобы включить передачу координат текстуры в шейдер пикселей в форме частичной точности.</span><span class="sxs-lookup"><span data-stu-id="4ddfc-145">On a texture coordinate declaration to enable passing texture coordinates to the pixel shader in partial-precision form.</span></span> <span data-ttu-id="4ddfc-146">Это позволяет, например, использовать координаты текстуры для передачи цветовых данных в шейдер пикселей, что может выполняться быстрее с частичной точностью, чем с полной точностью в некоторых реализациях.</span><span class="sxs-lookup"><span data-stu-id="4ddfc-146">This allows, for example, the use of texture coordinates to relay color data to the pixel shader, which may be faster with partial precision than with full precision in some implementations.</span></span> <span data-ttu-id="4ddfc-147">При отсутствии этого модификатора координаты текстуры должны передаваться с полной точностью.</span><span class="sxs-lookup"><span data-stu-id="4ddfc-147">In the absence of this modifier, texture coordinates must be passed in full precision.</span></span>
-   <span data-ttu-id="4ddfc-148">В любой инструкции, включая инструкции по загрузке текстур.</span><span class="sxs-lookup"><span data-stu-id="4ddfc-148">On any instruction including texture load instructions.</span></span> <span data-ttu-id="4ddfc-149">Это означает, что реализации разрешено выполнять инструкцию с частичной точностью и сохранять результат частичной точности.</span><span class="sxs-lookup"><span data-stu-id="4ddfc-149">This indicates that the implementation is allowed to execute the instruction with partial precision and store a partial precision result.</span></span> <span data-ttu-id="4ddfc-150">При отсутствии явного модификатора инструкция должна выполняться с полной точностью (независимо от точности ввода).</span><span class="sxs-lookup"><span data-stu-id="4ddfc-150">In the absence of an explicit modifier, the instruction must be performed at full precision (regardless of the input precision).</span></span>

<span data-ttu-id="4ddfc-151">Примеры:</span><span class="sxs-lookup"><span data-stu-id="4ddfc-151">Examples:</span></span>


```
dcl_texcoord0_pp t1
cmp_pp r0, r1, r2, r3
```



## <a name="saturate"></a><span data-ttu-id="4ddfc-152">Изменение насыщенности</span><span class="sxs-lookup"><span data-stu-id="4ddfc-152">Saturate</span></span>

<span data-ttu-id="4ddfc-153">Модификатор инструкции "насыщенность" ( \_ Кот) насыщенность (или фиксации) результата инструкции в диапазоне от \[ 0 \] до 1 перед записью в регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="4ddfc-153">The saturate instruction modifier (\_sat) saturates (or clamps) the instruction result to the range \[0, 1\] before writing to the destination register.</span></span>

<span data-ttu-id="4ddfc-154">\_Модификатор инструкции "Кот" можно использовать с любой инструкцией, кроме [ФРК-PS](frc---ps.md), [синкос-PS](sincos---ps.md)и любых \* инструкций да.</span><span class="sxs-lookup"><span data-stu-id="4ddfc-154">The \_sat instruction modifier can be used with any instruction except [frc - ps](frc---ps.md), [sincos - ps](sincos---ps.md), and any tex\* instructions.</span></span>

<span data-ttu-id="4ddfc-155">Для PS \_ 2 \_ 0, PS \_ 2 \_ x и PS \_ 2 \_ SW \_ Модификатор инструкции не может использоваться с инструкциями по записи в какие-либо выходные регистры ([выходной регистр](dx9-graphics-reference-asm-ps-registers-output-color.md) или [регистр глубины вывода](dx9-graphics-reference-asm-ps-registers-output-depth.md)).</span><span class="sxs-lookup"><span data-stu-id="4ddfc-155">For ps\_2\_0, ps\_2\_x, and ps\_2\_sw, the \_sat instruction modifier cannot be used with instructions writing to any output registers ([Output Color Register](dx9-graphics-reference-asm-ps-registers-output-color.md) or [Output Depth Register](dx9-graphics-reference-asm-ps-registers-output-depth.md)).</span></span> <span data-ttu-id="4ddfc-156">Это ограничение не применяется к PS \_ 3 \_ и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="4ddfc-156">This restriction does not apply to ps\_3\_0 and above.</span></span>

<span data-ttu-id="4ddfc-157">Пример</span><span class="sxs-lookup"><span data-stu-id="4ddfc-157">Example:</span></span>


```
dp3_sat r0, v0, c1
```



## <a name="related-topics"></a><span data-ttu-id="4ddfc-158">См. также</span><span class="sxs-lookup"><span data-stu-id="4ddfc-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ddfc-159">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="4ddfc-159">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




