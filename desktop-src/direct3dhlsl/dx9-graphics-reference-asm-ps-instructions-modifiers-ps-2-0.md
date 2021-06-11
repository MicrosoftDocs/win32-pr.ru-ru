---
title: Модификаторы для ps_2_0 и более поздних версий
description: Модификаторы инструкций влияют на результат инструкции перед его записью в регистр назначения. Сведения об модификаторах для ps_2_0 и более поздних версий.
ms.assetid: eb2a8a1f-51bc-4516-b679-a8fb25b0dda0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dc8ed91f8e103ebbab7c43ffe53201f0e1d5dfcf
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989289"
---
# <a name="modifiers-for-ps_2_0-and-above"></a><span data-ttu-id="178bd-104">Модификаторы для PS \_ 2 \_ и более поздних версий</span><span class="sxs-lookup"><span data-stu-id="178bd-104">Modifiers for ps\_2\_0 and Above</span></span>

<span data-ttu-id="178bd-105">Модификаторы инструкций влияют на результат инструкции перед его записью в регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="178bd-105">Instruction modifiers affect the result of the instruction before it is written into the destination register.</span></span>

<span data-ttu-id="178bd-106">В этом разделе содержатся справочные сведения по модификаторам инструкций, реализованным построителем пиксельных шейдеров версии 2 \_ 0 и выше.</span><span class="sxs-lookup"><span data-stu-id="178bd-106">This section contains reference information for the instruction modifiers implemented by pixel shader version 2\_0 and above.</span></span>



| <span data-ttu-id="178bd-107">Имя</span><span class="sxs-lookup"><span data-stu-id="178bd-107">Name</span></span>                                     | <span data-ttu-id="178bd-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="178bd-108">Syntax</span></span>     | <span data-ttu-id="178bd-109">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="178bd-109">2\_0</span></span> | <span data-ttu-id="178bd-110">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="178bd-110">2\_x</span></span> | <span data-ttu-id="178bd-111">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="178bd-111">2\_sw</span></span> | <span data-ttu-id="178bd-112">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="178bd-112">3\_0</span></span> | <span data-ttu-id="178bd-113">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="178bd-113">3\_sw</span></span> |
|------------------------------------------|------------|------|------|-------|------|-------|
| [<span data-ttu-id="178bd-114">Центроид</span><span class="sxs-lookup"><span data-stu-id="178bd-114">Centroid</span></span>](#centroid)                    | <span data-ttu-id="178bd-115">\_центроид</span><span class="sxs-lookup"><span data-stu-id="178bd-115">\_centroid</span></span> | <span data-ttu-id="178bd-116">x</span><span class="sxs-lookup"><span data-stu-id="178bd-116">x</span></span>    | <span data-ttu-id="178bd-117">x</span><span class="sxs-lookup"><span data-stu-id="178bd-117">x</span></span>    | <span data-ttu-id="178bd-118">x</span><span class="sxs-lookup"><span data-stu-id="178bd-118">x</span></span>     | <span data-ttu-id="178bd-119">x</span><span class="sxs-lookup"><span data-stu-id="178bd-119">x</span></span>    | <span data-ttu-id="178bd-120">x</span><span class="sxs-lookup"><span data-stu-id="178bd-120">x</span></span>     |
| [<span data-ttu-id="178bd-121">Частичная \_ точность</span><span class="sxs-lookup"><span data-stu-id="178bd-121">Partial\_Precision</span></span>](#partial-precision) | <span data-ttu-id="178bd-122">\_PP</span><span class="sxs-lookup"><span data-stu-id="178bd-122">\_pp</span></span>       | <span data-ttu-id="178bd-123">x</span><span class="sxs-lookup"><span data-stu-id="178bd-123">x</span></span>    | <span data-ttu-id="178bd-124">x</span><span class="sxs-lookup"><span data-stu-id="178bd-124">x</span></span>    | <span data-ttu-id="178bd-125">x</span><span class="sxs-lookup"><span data-stu-id="178bd-125">x</span></span>     | <span data-ttu-id="178bd-126">x</span><span class="sxs-lookup"><span data-stu-id="178bd-126">x</span></span>    | <span data-ttu-id="178bd-127">x</span><span class="sxs-lookup"><span data-stu-id="178bd-127">x</span></span>     |
| [<span data-ttu-id="178bd-128">Saturate</span><span class="sxs-lookup"><span data-stu-id="178bd-128">Saturate</span></span>](#saturate)                    | <span data-ttu-id="178bd-129">\_Кот</span><span class="sxs-lookup"><span data-stu-id="178bd-129">\_sat</span></span>      | <span data-ttu-id="178bd-130">x</span><span class="sxs-lookup"><span data-stu-id="178bd-130">x</span></span>    | <span data-ttu-id="178bd-131">x</span><span class="sxs-lookup"><span data-stu-id="178bd-131">x</span></span>    | <span data-ttu-id="178bd-132">x</span><span class="sxs-lookup"><span data-stu-id="178bd-132">x</span></span>     | <span data-ttu-id="178bd-133">x</span><span class="sxs-lookup"><span data-stu-id="178bd-133">x</span></span>    | <span data-ttu-id="178bd-134">x</span><span class="sxs-lookup"><span data-stu-id="178bd-134">x</span></span>     |



 

## <a name="centroid"></a><span data-ttu-id="178bd-135">Центроид</span><span class="sxs-lookup"><span data-stu-id="178bd-135">Centroid</span></span>

<span data-ttu-id="178bd-136">Модификатор центроид является необязательным модификатором, который замещает интерполяцию атрибута в диапазоне примитива, если многовыборочный пиксельный центр не охватывается примитивом.</span><span class="sxs-lookup"><span data-stu-id="178bd-136">The centroid modifier is an optional modifier that clamps attribute interpolation within the range of the primitive when a multisample pixel center is not covered by the primitive.</span></span> <span data-ttu-id="178bd-137">Это можно увидеть на [выборки центроид](https://msdn.microsoft.com/library/ee415231(VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="178bd-137">This can be seen in [Centroid Sampling](https://msdn.microsoft.com/library/ee415231(VS.85).aspx).</span></span>

<span data-ttu-id="178bd-138">К инструкции сборки можно применить модификатор центроид, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="178bd-138">You can apply the centroid modifier to an assembly instruction as shown here:</span></span>


```
dcl_texcoord0_centroid v0
```



<span data-ttu-id="178bd-139">Модификатор центроид также можно применить к семантике, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="178bd-139">You can also apply the centroid modifier to a semantic as shown here:</span></span>


```
float4 TexturePointCentroidPS( float4 TexCoord : TEXCOORD0_centroid ) : COLOR0
{
    return tex2D( PointSampler, TexCoord );
}
```



<span data-ttu-id="178bd-140">Кроме того, все [входные цветовые регистры](dx9-graphics-reference-asm-ps-registers-input-color.md) (v \# ), объявленные с помощью семантики цвета, будут автоматически применены к центроид.</span><span class="sxs-lookup"><span data-stu-id="178bd-140">In addition, any [Input Color Register](dx9-graphics-reference-asm-ps-registers-input-color.md) (v\#) declared with a color semantic will automatically have centroid applied.</span></span> <span data-ttu-id="178bd-141">Не гарантируется точность градиентов, вычисленных на основе атрибутов, которые центроид выборка.</span><span class="sxs-lookup"><span data-stu-id="178bd-141">Gradients computed from attributes that are centroid sampled are not guaranteed to be accurate.</span></span>

## <a name="partial-precision"></a><span data-ttu-id="178bd-142">Частичная точность</span><span class="sxs-lookup"><span data-stu-id="178bd-142">Partial Precision</span></span>

<span data-ttu-id="178bd-143">Модификатор инструкции частичной точности ( \_ PP) указывает области, где приемлема точность, при условии, что базовая реализация поддерживает ее.</span><span class="sxs-lookup"><span data-stu-id="178bd-143">The partial precision instruction modifier (\_pp) indicates areas where partial precision is acceptable, provided that the underlying implementation supports it.</span></span> <span data-ttu-id="178bd-144">Реализации всегда могут игнорировать модификатор и выполнять затронутые операции в полной точности.</span><span class="sxs-lookup"><span data-stu-id="178bd-144">Implementations are always free to ignore the modifier and perform the affected operations in full precision.</span></span>

<span data-ttu-id="178bd-145">\_Модификатор PP может находиться в двух контекстах:</span><span class="sxs-lookup"><span data-stu-id="178bd-145">The \_pp modifier can occur in two contexts:</span></span>

-   <span data-ttu-id="178bd-146">Для объявления координат текстуры, чтобы включить передачу координат текстуры в шейдер пикселей в форме частичной точности.</span><span class="sxs-lookup"><span data-stu-id="178bd-146">On a texture coordinate declaration to enable passing texture coordinates to the pixel shader in partial-precision form.</span></span> <span data-ttu-id="178bd-147">Это позволяет, например, использовать координаты текстуры для передачи цветовых данных в шейдер пикселей, что может выполняться быстрее с частичной точностью, чем с полной точностью в некоторых реализациях.</span><span class="sxs-lookup"><span data-stu-id="178bd-147">This allows, for example, the use of texture coordinates to relay color data to the pixel shader, which may be faster with partial precision than with full precision in some implementations.</span></span> <span data-ttu-id="178bd-148">При отсутствии этого модификатора координаты текстуры должны передаваться с полной точностью.</span><span class="sxs-lookup"><span data-stu-id="178bd-148">In the absence of this modifier, texture coordinates must be passed in full precision.</span></span>
-   <span data-ttu-id="178bd-149">В любой инструкции, включая инструкции по загрузке текстур.</span><span class="sxs-lookup"><span data-stu-id="178bd-149">On any instruction including texture load instructions.</span></span> <span data-ttu-id="178bd-150">Это означает, что реализации разрешено выполнять инструкцию с частичной точностью и сохранять результат частичной точности.</span><span class="sxs-lookup"><span data-stu-id="178bd-150">This indicates that the implementation is allowed to execute the instruction with partial precision and store a partial precision result.</span></span> <span data-ttu-id="178bd-151">При отсутствии явного модификатора инструкция должна выполняться с полной точностью (независимо от точности ввода).</span><span class="sxs-lookup"><span data-stu-id="178bd-151">In the absence of an explicit modifier, the instruction must be performed at full precision (regardless of the input precision).</span></span>

<span data-ttu-id="178bd-152">Примеры:</span><span class="sxs-lookup"><span data-stu-id="178bd-152">Examples:</span></span>


```
dcl_texcoord0_pp t1
cmp_pp r0, r1, r2, r3
```



## <a name="saturate"></a><span data-ttu-id="178bd-153">Изменение насыщенности</span><span class="sxs-lookup"><span data-stu-id="178bd-153">Saturate</span></span>

<span data-ttu-id="178bd-154">Модификатор инструкции "насыщенность" ( \_ Кот) насыщенность (или фиксации) результата инструкции в диапазоне от \[ 0 \] до 1 перед записью в регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="178bd-154">The saturate instruction modifier (\_sat) saturates (or clamps) the instruction result to the range \[0, 1\] before writing to the destination register.</span></span>

<span data-ttu-id="178bd-155">\_Модификатор инструкции "Кот" можно использовать с любой инструкцией, кроме [ФРК-PS](frc---ps.md), [синкос-PS](sincos---ps.md)и любых \* инструкций да.</span><span class="sxs-lookup"><span data-stu-id="178bd-155">The \_sat instruction modifier can be used with any instruction except [frc - ps](frc---ps.md), [sincos - ps](sincos---ps.md), and any tex\* instructions.</span></span>

<span data-ttu-id="178bd-156">Для PS \_ 2 \_ 0, PS \_ 2 \_ x и PS \_ 2 \_ SW \_ Модификатор инструкции не может использоваться с инструкциями по записи в какие-либо выходные регистры ([выходной регистр](dx9-graphics-reference-asm-ps-registers-output-color.md) или [регистр глубины вывода](dx9-graphics-reference-asm-ps-registers-output-depth.md)).</span><span class="sxs-lookup"><span data-stu-id="178bd-156">For ps\_2\_0, ps\_2\_x, and ps\_2\_sw, the \_sat instruction modifier cannot be used with instructions writing to any output registers ([Output Color Register](dx9-graphics-reference-asm-ps-registers-output-color.md) or [Output Depth Register](dx9-graphics-reference-asm-ps-registers-output-depth.md)).</span></span> <span data-ttu-id="178bd-157">Это ограничение не применяется к PS \_ 3 \_ и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="178bd-157">This restriction does not apply to ps\_3\_0 and above.</span></span>

<span data-ttu-id="178bd-158">Пример</span><span class="sxs-lookup"><span data-stu-id="178bd-158">Example:</span></span>


```
dp3_sat r0, v0, c1
```



## <a name="related-topics"></a><span data-ttu-id="178bd-159">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="178bd-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="178bd-160">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="178bd-160">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




