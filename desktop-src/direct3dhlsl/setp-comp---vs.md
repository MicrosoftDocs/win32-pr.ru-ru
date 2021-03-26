---
title: Сравнение setp_comp
description: Задайте регистр предиката. | Сравнение setp_comp
ms.assetid: bfead3f8-f7fe-4fc1-939f-8e5fbc3e0adf
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 77d9e5f46e9fb8bbcfb96e56d13cd6f7cebfecc2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104424246"
---
# <a name="setp_comp---vs"></a><span data-ttu-id="f8f53-104">сетп \_ comp-VS</span><span class="sxs-lookup"><span data-stu-id="f8f53-104">setp\_comp - vs</span></span>

<span data-ttu-id="f8f53-105">Задайте регистр предиката.</span><span class="sxs-lookup"><span data-stu-id="f8f53-105">Set the predicate register.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8f53-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f8f53-106">Syntax</span></span>



| <span data-ttu-id="f8f53-107">сетпие \_ летнего времени, src0, src1</span><span class="sxs-lookup"><span data-stu-id="f8f53-107">setp\_comp dst, src0, src1</span></span> |
|----------------------------|



 

<span data-ttu-id="f8f53-108">Где:</span><span class="sxs-lookup"><span data-stu-id="f8f53-108">Where:</span></span>

-   <span data-ttu-id="f8f53-109">\_Comp — это сравнение двух исходных регистров по каналу.</span><span class="sxs-lookup"><span data-stu-id="f8f53-109">\_comp is a per-channel comparison between the two source registers.</span></span> <span data-ttu-id="f8f53-110">Может принимать одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="f8f53-110">It can be one of the following:</span></span> 

    | <span data-ttu-id="f8f53-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f8f53-111">Syntax</span></span> | <span data-ttu-id="f8f53-112">Сравнение</span><span class="sxs-lookup"><span data-stu-id="f8f53-112">Comparison</span></span>            |
    |--------|-----------------------|
    | <span data-ttu-id="f8f53-113">\_gt</span><span class="sxs-lookup"><span data-stu-id="f8f53-113">\_gt</span></span>   | <span data-ttu-id="f8f53-114">Больше чем</span><span class="sxs-lookup"><span data-stu-id="f8f53-114">Greater than</span></span>          |
    | <span data-ttu-id="f8f53-115">\_светл</span><span class="sxs-lookup"><span data-stu-id="f8f53-115">\_lt</span></span>   | <span data-ttu-id="f8f53-116">Меньше чем</span><span class="sxs-lookup"><span data-stu-id="f8f53-116">Less than</span></span>             |
    | <span data-ttu-id="f8f53-117">\_GE</span><span class="sxs-lookup"><span data-stu-id="f8f53-117">\_ge</span></span>   | <span data-ttu-id="f8f53-118">Больше или равно</span><span class="sxs-lookup"><span data-stu-id="f8f53-118">Greater than or equal</span></span> |
    | <span data-ttu-id="f8f53-119">\_Le</span><span class="sxs-lookup"><span data-stu-id="f8f53-119">\_le</span></span>   | <span data-ttu-id="f8f53-120">Меньше или равно</span><span class="sxs-lookup"><span data-stu-id="f8f53-120">Less than or equal</span></span>    |
    | <span data-ttu-id="f8f53-121">\_EQ</span><span class="sxs-lookup"><span data-stu-id="f8f53-121">\_eq</span></span>   | <span data-ttu-id="f8f53-122">Равно</span><span class="sxs-lookup"><span data-stu-id="f8f53-122">Equal to</span></span>              |
    | <span data-ttu-id="f8f53-123">\_видимому</span><span class="sxs-lookup"><span data-stu-id="f8f53-123">\_ne</span></span>   | <span data-ttu-id="f8f53-124">Не равно</span><span class="sxs-lookup"><span data-stu-id="f8f53-124">Not equal to</span></span>          |

    

     

-   <span data-ttu-id="f8f53-125">DST — это регистр [регистрации предиката](dx9-graphics-reference-asm-vs-registers-predicate.md) , P0.</span><span class="sxs-lookup"><span data-stu-id="f8f53-125">dst is the [Predicate Register](dx9-graphics-reference-asm-vs-registers-predicate.md) register, p0.</span></span>
-   <span data-ttu-id="f8f53-126">src0 является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="f8f53-126">src0 is a source register.</span></span>
-   <span data-ttu-id="f8f53-127">src1 является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="f8f53-127">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8f53-128">Примечания</span><span class="sxs-lookup"><span data-stu-id="f8f53-128">Remarks</span></span>



| <span data-ttu-id="f8f53-129">Версии шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="f8f53-129">Vertex shader versions</span></span> | <span data-ttu-id="f8f53-130">1\_1</span><span class="sxs-lookup"><span data-stu-id="f8f53-130">1\_1</span></span> | <span data-ttu-id="f8f53-131">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f8f53-131">2\_0</span></span> | <span data-ttu-id="f8f53-132">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="f8f53-132">2\_x</span></span> | <span data-ttu-id="f8f53-133">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="f8f53-133">2\_sw</span></span> | <span data-ttu-id="f8f53-134">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f8f53-134">3\_0</span></span> | <span data-ttu-id="f8f53-135">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="f8f53-135">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="f8f53-136">сетпная \_ comp</span><span class="sxs-lookup"><span data-stu-id="f8f53-136">setp\_comp</span></span>             |      |      | <span data-ttu-id="f8f53-137">x</span><span class="sxs-lookup"><span data-stu-id="f8f53-137">x</span></span>    | <span data-ttu-id="f8f53-138">x</span><span class="sxs-lookup"><span data-stu-id="f8f53-138">x</span></span>     | <span data-ttu-id="f8f53-139">x</span><span class="sxs-lookup"><span data-stu-id="f8f53-139">x</span></span>    | <span data-ttu-id="f8f53-140">x</span><span class="sxs-lookup"><span data-stu-id="f8f53-140">x</span></span>     |



 

<span data-ttu-id="f8f53-141">Эта инструкция работает следующим образом:</span><span class="sxs-lookup"><span data-stu-id="f8f53-141">This instruction operates as:</span></span>


```
per channel in destination write mask
{
  dst.channel = src0.channel cmp src1.channel
}
```



<span data-ttu-id="f8f53-142">Для каждого канала, который может быть записан в соответствии с целевой маской записи, сохраните логический результат операции сравнения между соответствующими каналами src0 и src1 (после разрешения модификатора источника свиззлес).</span><span class="sxs-lookup"><span data-stu-id="f8f53-142">For each channel that can be written according to the destination write mask, save the boolean result of the comparison operation between the corresponding channels of src0 and src1 (after the source modifier swizzles have been resolved).</span></span>

<span data-ttu-id="f8f53-143">Регистры источников позволяют указать произвольный компонент свиззлес.</span><span class="sxs-lookup"><span data-stu-id="f8f53-143">Source registers allow arbitrary component swizzles to be specified.</span></span>

<span data-ttu-id="f8f53-144">Регистр назначения позволяет использовать произвольные маски записи.</span><span class="sxs-lookup"><span data-stu-id="f8f53-144">The destination register allows arbitrary write masks.</span></span>

<span data-ttu-id="f8f53-145">Регистр приемника должен быть регистром предиката.</span><span class="sxs-lookup"><span data-stu-id="f8f53-145">The dest register must be the predicate register.</span></span>

## <a name="applying-the-predicate-register"></a><span data-ttu-id="f8f53-146">Применение регистра предиката</span><span class="sxs-lookup"><span data-stu-id="f8f53-146">Applying the Predicate Register</span></span>

<span data-ttu-id="f8f53-147">После того как регистр предиката инициализирован с помощью сетп, его можно использовать для управления инструкциями для каждого компонента.</span><span class="sxs-lookup"><span data-stu-id="f8f53-147">Once the predicate register has been initialized with setp, it can be used to control an instruction per component.</span></span> <span data-ttu-id="f8f53-148">Ниже приведен синтаксис.</span><span class="sxs-lookup"><span data-stu-id="f8f53-148">Here's the syntax:</span></span>


```
([!]p0[.swizzle]) instruction dest, srcReg, ...
```



<span data-ttu-id="f8f53-149">Где:</span><span class="sxs-lookup"><span data-stu-id="f8f53-149">Where:</span></span>

-   <span data-ttu-id="f8f53-150">\[!\] является необязательным логическим значением NOT</span><span class="sxs-lookup"><span data-stu-id="f8f53-150">\[!\] is an optional boolean NOT</span></span>
-   <span data-ttu-id="f8f53-151">P0 — это регистр предикатов</span><span class="sxs-lookup"><span data-stu-id="f8f53-151">p0 is the predicate register</span></span>
-   <span data-ttu-id="f8f53-152">\[. свиззле \] — это необязательный свиззле, применяемый к содержимому регистра предиката, прежде чем использовать его для маскирования инструкции.</span><span class="sxs-lookup"><span data-stu-id="f8f53-152">\[.swizzle\] is an optional swizzle to apply to the contents of the predicate register before using it to mask the instruction.</span></span> <span data-ttu-id="f8f53-153">Доступные свиззлес:. ксизв (по умолчанию, если не указано ни одного) или репликация свиззле:. x/. r,. y/. g,. z/. b или. a/. w.</span><span class="sxs-lookup"><span data-stu-id="f8f53-153">The available swizzles are: .xyzw (default when none specified), or any replicate swizzle: .x/.r, .y/.g, .z/.b or .a/.w.</span></span>
-   <span data-ttu-id="f8f53-154">Инструкция является любой аритметик или инструкцией текстуры.</span><span class="sxs-lookup"><span data-stu-id="f8f53-154">instruction is any aritmetic, or texture instruction.</span></span> <span data-ttu-id="f8f53-155">Это не может быть статической или динамической инструкцией по управлению потоком.</span><span class="sxs-lookup"><span data-stu-id="f8f53-155">This cannot be a static or dynamic flow control instruction.</span></span>
-   <span data-ttu-id="f8f53-156">dest, Сркрег,... являются регистрами, необходимыми для инструкции</span><span class="sxs-lookup"><span data-stu-id="f8f53-156">dest, srcReg, ... are the registers required by the instruction</span></span>

<span data-ttu-id="f8f53-157">При условии, что регистр предиката настроен для значений компонентов (true, true, false, false), он может быть применен к этой инструкции:</span><span class="sxs-lookup"><span data-stu-id="f8f53-157">Assuming the predicate register has been set up with (true, true, false, false) component values, it can be applied to this instruction:</span></span>


```
// given r0 = 0,0,1,1
// given r1 = 1,1,0,0
setp_le p0, r0, r1
(p0) add r2, r3, r4
```



<span data-ttu-id="f8f53-158">чтобы выполнить 2 компонента, добавьте.</span><span class="sxs-lookup"><span data-stu-id="f8f53-158">to perform a 2 component add.</span></span>


```
r2.x = r3.x + r4.x
r2.y = r3.y + r4.y
```



<span data-ttu-id="f8f53-159">Компоненты x и y R2 не будут записаны, так как регистр предикатов содержал значение false в компонентах z и w.</span><span class="sxs-lookup"><span data-stu-id="f8f53-159">The x and y components of r2 will not be written since the predicate register contained false in components z and w.</span></span>

<span data-ttu-id="f8f53-160">Применение регистра предиката к арифметической или текстурной инструкции увеличивает число слотов инструкций на 1.</span><span class="sxs-lookup"><span data-stu-id="f8f53-160">Applying the predicate register to an arithmetic or texture instruction increases its instruction slot count by 1.</span></span>

<span data-ttu-id="f8f53-161">Регистр предикатов также можно применить к инструкциям " [пред-VS](if-pred---vs.md)", " [каллнз пред-](callnz-pred---vs.md) VS" и [бреакп-VS](breakp---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="f8f53-161">The predicate register can also be applied to [if pred - vs](if-pred---vs.md), [callnz pred - vs](callnz-pred---vs.md) and [breakp - vs](breakp---vs.md) instructions.</span></span> <span data-ttu-id="f8f53-162">Эти инструкции по управлению потоком не увеличивают число слотов инструкций при использовании регистра предиката.</span><span class="sxs-lookup"><span data-stu-id="f8f53-162">These flow control instructions do not have any increase in the instruction slot count when using the predicate register.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f8f53-163">См. также</span><span class="sxs-lookup"><span data-stu-id="f8f53-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f8f53-164">Инструкции шейдера вершин</span><span class="sxs-lookup"><span data-stu-id="f8f53-164">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




