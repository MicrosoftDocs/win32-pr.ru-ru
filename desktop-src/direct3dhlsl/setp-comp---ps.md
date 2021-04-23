---
title: setp_comp-PS
description: Задайте регистр предиката. | setp_comp-PS
ms.assetid: a9acb685-f9aa-41f1-8ef1-6d104cb76a09
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a68da290ecb04e9cb7ae49c5525997fbf4c112a3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104273586"
---
# <a name="setp_comp---ps"></a><span data-ttu-id="aec20-104">сетп \_ comp-PS</span><span class="sxs-lookup"><span data-stu-id="aec20-104">setp\_comp - ps</span></span>

<span data-ttu-id="aec20-105">Задайте регистр предиката.</span><span class="sxs-lookup"><span data-stu-id="aec20-105">Set the predicate register.</span></span>

## <a name="syntax"></a><span data-ttu-id="aec20-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="aec20-106">Syntax</span></span>



| <span data-ttu-id="aec20-107">сетпие \_ летнего времени, src0, src1</span><span class="sxs-lookup"><span data-stu-id="aec20-107">setp\_comp dst, src0, src1</span></span> |
|----------------------------|



 

<span data-ttu-id="aec20-108">Где:</span><span class="sxs-lookup"><span data-stu-id="aec20-108">Where:</span></span>

-   <span data-ttu-id="aec20-109">\_Comp — это сравнение двух исходных регистров по каналу.</span><span class="sxs-lookup"><span data-stu-id="aec20-109">\_comp is a per-channel comparison between the two source registers.</span></span> <span data-ttu-id="aec20-110">Может принимать одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="aec20-110">It can be one of the following:</span></span> 

    | <span data-ttu-id="aec20-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="aec20-111">Syntax</span></span> | <span data-ttu-id="aec20-112">Сравнение</span><span class="sxs-lookup"><span data-stu-id="aec20-112">Comparison</span></span>            |
    |--------|-----------------------|
    | <span data-ttu-id="aec20-113">\_gt</span><span class="sxs-lookup"><span data-stu-id="aec20-113">\_gt</span></span>   | <span data-ttu-id="aec20-114">Больше чем</span><span class="sxs-lookup"><span data-stu-id="aec20-114">Greater than</span></span>          |
    | <span data-ttu-id="aec20-115">\_светл</span><span class="sxs-lookup"><span data-stu-id="aec20-115">\_lt</span></span>   | <span data-ttu-id="aec20-116">Меньше чем</span><span class="sxs-lookup"><span data-stu-id="aec20-116">Less than</span></span>             |
    | <span data-ttu-id="aec20-117">\_GE</span><span class="sxs-lookup"><span data-stu-id="aec20-117">\_ge</span></span>   | <span data-ttu-id="aec20-118">Больше или равно</span><span class="sxs-lookup"><span data-stu-id="aec20-118">Greater than or equal</span></span> |
    | <span data-ttu-id="aec20-119">\_Le</span><span class="sxs-lookup"><span data-stu-id="aec20-119">\_le</span></span>   | <span data-ttu-id="aec20-120">Меньше или равно</span><span class="sxs-lookup"><span data-stu-id="aec20-120">Less than or equal</span></span>    |
    | <span data-ttu-id="aec20-121">\_EQ</span><span class="sxs-lookup"><span data-stu-id="aec20-121">\_eq</span></span>   | <span data-ttu-id="aec20-122">Равно</span><span class="sxs-lookup"><span data-stu-id="aec20-122">Equal to</span></span>              |
    | <span data-ttu-id="aec20-123">\_видимому</span><span class="sxs-lookup"><span data-stu-id="aec20-123">\_ne</span></span>   | <span data-ttu-id="aec20-124">Не равно</span><span class="sxs-lookup"><span data-stu-id="aec20-124">Not equal to</span></span>          |

    

     

-   <span data-ttu-id="aec20-125">DST — это регистр [регистрации предиката](dx9-graphics-reference-asm-ps-registers-predicate.md) , P0.</span><span class="sxs-lookup"><span data-stu-id="aec20-125">dst is the [Predicate Register](dx9-graphics-reference-asm-ps-registers-predicate.md) register, p0.</span></span>
-   <span data-ttu-id="aec20-126">src0 является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="aec20-126">src0 is a source register.</span></span>
-   <span data-ttu-id="aec20-127">src1 является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="aec20-127">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="aec20-128">Примечания</span><span class="sxs-lookup"><span data-stu-id="aec20-128">Remarks</span></span>



| <span data-ttu-id="aec20-129">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="aec20-129">Pixel shader versions</span></span> | <span data-ttu-id="aec20-130">1\_1</span><span class="sxs-lookup"><span data-stu-id="aec20-130">1\_1</span></span> | <span data-ttu-id="aec20-131">1\_2</span><span class="sxs-lookup"><span data-stu-id="aec20-131">1\_2</span></span> | <span data-ttu-id="aec20-132">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="aec20-132">1\_3</span></span> | <span data-ttu-id="aec20-133">1\_4</span><span class="sxs-lookup"><span data-stu-id="aec20-133">1\_4</span></span> | <span data-ttu-id="aec20-134">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="aec20-134">2\_0</span></span> | <span data-ttu-id="aec20-135">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="aec20-135">2\_x</span></span> | <span data-ttu-id="aec20-136">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="aec20-136">2\_sw</span></span> | <span data-ttu-id="aec20-137">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="aec20-137">3\_0</span></span> | <span data-ttu-id="aec20-138">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="aec20-138">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="aec20-139">сетпная \_ comp</span><span class="sxs-lookup"><span data-stu-id="aec20-139">setp\_comp</span></span>            |      |      |      |      |      | <span data-ttu-id="aec20-140">x</span><span class="sxs-lookup"><span data-stu-id="aec20-140">x</span></span>    | <span data-ttu-id="aec20-141">x</span><span class="sxs-lookup"><span data-stu-id="aec20-141">x</span></span>     | <span data-ttu-id="aec20-142">x</span><span class="sxs-lookup"><span data-stu-id="aec20-142">x</span></span>    | <span data-ttu-id="aec20-143">x</span><span class="sxs-lookup"><span data-stu-id="aec20-143">x</span></span>     |



 

<span data-ttu-id="aec20-144">Эта инструкция работает следующим образом:</span><span class="sxs-lookup"><span data-stu-id="aec20-144">This instruction operates as:</span></span>


```
per channel in destination write mask
{
  dst.channel = src0.channel cmp src1.channel
}
```



<span data-ttu-id="aec20-145">Для каждого канала, который может быть записан в соответствии с целевой маской записи, сохраните логический результат операции сравнения между соответствующими каналами src0 и src1 (после разрешения модификатора источника свиззлес).</span><span class="sxs-lookup"><span data-stu-id="aec20-145">For each channel that can be written according to the destination write mask, save the boolean result of the comparison operation between the corresponding channels of src0 and src1 (after the source modifier swizzles have been resolved).</span></span>

<span data-ttu-id="aec20-146">Регистры источников позволяют указать произвольный компонент свиззлес.</span><span class="sxs-lookup"><span data-stu-id="aec20-146">Source registers allow arbitrary component swizzles to be specified.</span></span>

<span data-ttu-id="aec20-147">Регистр назначения позволяет использовать произвольные маски записи.</span><span class="sxs-lookup"><span data-stu-id="aec20-147">The destination register allows arbitrary write masks.</span></span>

<span data-ttu-id="aec20-148">Регистр летнего времени должен быть регистром предиката.</span><span class="sxs-lookup"><span data-stu-id="aec20-148">The dst register must be the predicate register.</span></span>

## <a name="applying-the-predicate-register"></a><span data-ttu-id="aec20-149">Применение регистра предиката</span><span class="sxs-lookup"><span data-stu-id="aec20-149">Applying the Predicate Register</span></span>

<span data-ttu-id="aec20-150">После инициализации регистра предиката с помощью сетп \_ comp его можно использовать для управления инструкциями на каждый компонент.</span><span class="sxs-lookup"><span data-stu-id="aec20-150">Once the predicate register has been initialized with setp\_comp, it can be used to control an instruction per component.</span></span> <span data-ttu-id="aec20-151">Ниже приведен синтаксис.</span><span class="sxs-lookup"><span data-stu-id="aec20-151">Here's the syntax:</span></span>


```
([!]p0[.swizzle]) instruction dest, src0, ...
```



<span data-ttu-id="aec20-152">Где:</span><span class="sxs-lookup"><span data-stu-id="aec20-152">Where:</span></span>

-   <span data-ttu-id="aec20-153">\[!\] является необязательным логическим значением NOT</span><span class="sxs-lookup"><span data-stu-id="aec20-153">\[!\] is an optional boolean NOT</span></span>
-   <span data-ttu-id="aec20-154">P0 — это регистр предикатов</span><span class="sxs-lookup"><span data-stu-id="aec20-154">p0 is the predicate register</span></span>
-   <span data-ttu-id="aec20-155">\[. свиззле \] — это необязательный свиззле, применяемый к содержимому регистра предиката, прежде чем использовать его для маскирования инструкции.</span><span class="sxs-lookup"><span data-stu-id="aec20-155">\[.swizzle\] is an optional swizzle to apply to the contents of the predicate register before using it to mask the instruction.</span></span> <span data-ttu-id="aec20-156">Доступные свиззлес:. ксизв (по умолчанию, если не указано ни одного) или репликация свиззле:. x/. r,. y/. g,. z/. b или. a/. w.</span><span class="sxs-lookup"><span data-stu-id="aec20-156">The available swizzles are: .xyzw (default when none specified), or any replicate swizzle: .x/.r, .y/.g, .z/.b or .a/.w.</span></span>
-   <span data-ttu-id="aec20-157">Инструкция является любой аритметик или инструкцией текстуры.</span><span class="sxs-lookup"><span data-stu-id="aec20-157">instruction is any aritmetic, or texture instruction.</span></span> <span data-ttu-id="aec20-158">Это не может быть статической или динамической инструкцией по управлению потоком.</span><span class="sxs-lookup"><span data-stu-id="aec20-158">This cannot be a static or dynamic flow control instruction.</span></span>
-   <span data-ttu-id="aec20-159">dest, src0,... являются регистрами, необходимыми для инструкции</span><span class="sxs-lookup"><span data-stu-id="aec20-159">dest, src0, ... are the registers required by the instruction</span></span>

<span data-ttu-id="aec20-160">При условии, что регистр предиката настроен для значений компонентов (true, true, false, false), он может быть применен к этой инструкции:</span><span class="sxs-lookup"><span data-stu-id="aec20-160">Assuming the predicate register has been set up with (true, true, false, false) component values, it can be applied to this instruction:</span></span>


```
(p0) add r1, r2, r3
```



<span data-ttu-id="aec20-161">чтобы выполнить 2 компонента, добавьте.</span><span class="sxs-lookup"><span data-stu-id="aec20-161">to perform a 2 component add.</span></span>


```
r1.x = r2.x + r3.x
r1.y = r2.y + r3.y
```



<span data-ttu-id="aec20-162">Компоненты z и w элемента R1 не будут записаны, так как регистр предикатов содержал значение false в компонентах z и w.</span><span class="sxs-lookup"><span data-stu-id="aec20-162">The z and w components of r1 will not be written since the predicate register contained false in components z and w.</span></span>

<span data-ttu-id="aec20-163">Применение регистра предиката к арифметической или текстурной инструкции увеличивает число слотов инструкций на 1.</span><span class="sxs-lookup"><span data-stu-id="aec20-163">Applying the predicate register to an arithmetic or texture instruction increases its instruction slot count by 1.</span></span>

<span data-ttu-id="aec20-164">Кроме того, регистр предиката можно применить к инструкциям in [-PS](if-pred---ps.md), [каллнз пред-PS](callnz-pred---ps.md) и [бреакп-PS](break-p---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="aec20-164">The predicate register can also be applied to [if pred - ps](if-pred---ps.md), [callnz pred - ps](callnz-pred---ps.md) and [breakp - ps](break-p---ps.md) instructions.</span></span> <span data-ttu-id="aec20-165">Эти инструкции по управлению потоком не увеличивают число слотов инструкций при использовании регистра предиката.</span><span class="sxs-lookup"><span data-stu-id="aec20-165">These flow control instructions do not have any increase in the instruction slot count when using the predicate register.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aec20-166">См. также</span><span class="sxs-lookup"><span data-stu-id="aec20-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aec20-167">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="aec20-167">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




