---
title: if_comp-PS
description: Запуск if bool-PS... else-PS... endif-PS блок с условием на основе значений, которые могут быть вычислены в шейдере. Эта инструкция используется для пропуска блока кода на основе условия.
ms.assetid: a641e347-df28-4a3f-a461-0b6aee758e59
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: db30983c83bc7d66e06befd07f4eb1dcdc9b21ea
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "103784887"
---
# <a name="if_comp---ps"></a><span data-ttu-id="55872-104">Если \_ comp-PS</span><span class="sxs-lookup"><span data-stu-id="55872-104">if\_comp - ps</span></span>

<span data-ttu-id="55872-105">Запуск [If bool-PS](if-bool---ps.md)... [else-PS](else---ps.md)... [endif-PS](endif---ps.md) блок с условием на основе значений, которые могут быть вычислены в шейдере.</span><span class="sxs-lookup"><span data-stu-id="55872-105">Start an [if bool - ps](if-bool---ps.md)...[else - ps](else---ps.md)...[endif - ps](endif---ps.md) block, with a condition based on values that could be computed in a shader.</span></span> <span data-ttu-id="55872-106">Эта инструкция используется для пропуска блока кода на основе условия.</span><span class="sxs-lookup"><span data-stu-id="55872-106">This instruction is used to skip a block of code, based on a condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="55872-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="55872-107">Syntax</span></span>



| <span data-ttu-id="55872-108">Если \_ comp src0, src1</span><span class="sxs-lookup"><span data-stu-id="55872-108">if\_comp src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="55872-109">Где:</span><span class="sxs-lookup"><span data-stu-id="55872-109">Where:</span></span>

-   <span data-ttu-id="55872-110">\_Comp — это сравнение двух исходных регистров.</span><span class="sxs-lookup"><span data-stu-id="55872-110">\_comp is a comparison between the two source registers.</span></span> <span data-ttu-id="55872-111">Может принимать одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="55872-111">It can be one of the following:</span></span> 

    | <span data-ttu-id="55872-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="55872-112">Syntax</span></span> | <span data-ttu-id="55872-113">Сравнение</span><span class="sxs-lookup"><span data-stu-id="55872-113">Comparison</span></span>            |
    |--------|-----------------------|
    | <span data-ttu-id="55872-114">\_gt</span><span class="sxs-lookup"><span data-stu-id="55872-114">\_gt</span></span>   | <span data-ttu-id="55872-115">Больше чем</span><span class="sxs-lookup"><span data-stu-id="55872-115">Greater than</span></span>          |
    | <span data-ttu-id="55872-116">\_светл</span><span class="sxs-lookup"><span data-stu-id="55872-116">\_lt</span></span>   | <span data-ttu-id="55872-117">Меньше чем</span><span class="sxs-lookup"><span data-stu-id="55872-117">Less than</span></span>             |
    | <span data-ttu-id="55872-118">\_GE</span><span class="sxs-lookup"><span data-stu-id="55872-118">\_ge</span></span>   | <span data-ttu-id="55872-119">Больше или равно</span><span class="sxs-lookup"><span data-stu-id="55872-119">Greater than or equal</span></span> |
    | <span data-ttu-id="55872-120">\_Le</span><span class="sxs-lookup"><span data-stu-id="55872-120">\_le</span></span>   | <span data-ttu-id="55872-121">Меньше или равно</span><span class="sxs-lookup"><span data-stu-id="55872-121">Less than or equal</span></span>    |
    | <span data-ttu-id="55872-122">\_EQ</span><span class="sxs-lookup"><span data-stu-id="55872-122">\_eq</span></span>   | <span data-ttu-id="55872-123">Равно</span><span class="sxs-lookup"><span data-stu-id="55872-123">Equal to</span></span>              |
    | <span data-ttu-id="55872-124">\_видимому</span><span class="sxs-lookup"><span data-stu-id="55872-124">\_ne</span></span>   | <span data-ttu-id="55872-125">Не равно</span><span class="sxs-lookup"><span data-stu-id="55872-125">Not equal to</span></span>          |

    

     

-   <span data-ttu-id="55872-126">src0 является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="55872-126">src0 is a source register.</span></span> <span data-ttu-id="55872-127">Для выбора компонента требуется репликация свиззле.</span><span class="sxs-lookup"><span data-stu-id="55872-127">Replicate swizzle is required to select a component.</span></span>
-   <span data-ttu-id="55872-128">src1 является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="55872-128">src1 is a source register.</span></span> <span data-ttu-id="55872-129">Для выбора компонента требуется репликация свиззле.</span><span class="sxs-lookup"><span data-stu-id="55872-129">Replicate swizzle is required to select a component.</span></span>

## <a name="remarks"></a><span data-ttu-id="55872-130">Примечания</span><span class="sxs-lookup"><span data-stu-id="55872-130">Remarks</span></span>



| <span data-ttu-id="55872-131">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="55872-131">Pixel shader versions</span></span> | <span data-ttu-id="55872-132">1\_1</span><span class="sxs-lookup"><span data-stu-id="55872-132">1\_1</span></span> | <span data-ttu-id="55872-133">1\_2</span><span class="sxs-lookup"><span data-stu-id="55872-133">1\_2</span></span> | <span data-ttu-id="55872-134">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="55872-134">1\_3</span></span> | <span data-ttu-id="55872-135">1\_4</span><span class="sxs-lookup"><span data-stu-id="55872-135">1\_4</span></span> | <span data-ttu-id="55872-136">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="55872-136">2\_0</span></span> | <span data-ttu-id="55872-137">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="55872-137">2\_x</span></span> | <span data-ttu-id="55872-138">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="55872-138">2\_sw</span></span> | <span data-ttu-id="55872-139">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="55872-139">3\_0</span></span> | <span data-ttu-id="55872-140">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="55872-140">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="55872-141">Если \_ comp</span><span class="sxs-lookup"><span data-stu-id="55872-141">if\_comp</span></span>              |      |      |      |      |      | <span data-ttu-id="55872-142">x</span><span class="sxs-lookup"><span data-stu-id="55872-142">x</span></span>    | <span data-ttu-id="55872-143">x</span><span class="sxs-lookup"><span data-stu-id="55872-143">x</span></span>     | <span data-ttu-id="55872-144">x</span><span class="sxs-lookup"><span data-stu-id="55872-144">x</span></span>    | <span data-ttu-id="55872-145">x</span><span class="sxs-lookup"><span data-stu-id="55872-145">x</span></span>     |



 

<span data-ttu-id="55872-146">Эта инструкция используется для пропуска блока кода на основе условия.</span><span class="sxs-lookup"><span data-stu-id="55872-146">This instruction is used to skip a block of code, based on a condition.</span></span>


```
if (src0 comparison src1)
   jump to the corresponding else or endif instruction;
```



<span data-ttu-id="55872-147">Будьте внимательны при использовании режимов сравнения «равно» и «не равно» для чисел с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="55872-147">Be careful using the equals and not equals comparison modes on floating point numbers.</span></span> <span data-ttu-id="55872-148">Поскольку округление происходит во время вычислений с плавающей запятой, для предотвращения ошибок можно выполнить сравнение со значением Эпсилон (небольшим ненулевым числом).</span><span class="sxs-lookup"><span data-stu-id="55872-148">Because rounding occurs during during floating point calculations, the comparison can be done against an epsilon value (small nonzero number) to avoid errors.</span></span>

<span data-ttu-id="55872-149">К ним относятся указанные ниже ограничения.</span><span class="sxs-lookup"><span data-stu-id="55872-149">Restrictions include:</span></span>

-   <span data-ttu-id="55872-150">Если \_ comp... [else-PS](else---ps.md)... в виде блоков [endif-PS](endif---ps.md) (вместе [с блоками](if-bool---ps.md) в виде предикатов) можно вкладывать до 24 слоев.</span><span class="sxs-lookup"><span data-stu-id="55872-150">if\_comp...[else - ps](else---ps.md)...[endif - ps](endif---ps.md) blocks (along with the predicated [if](if-bool---ps.md) blocks) can be nested up to 24 layers deep.</span></span>
-   <span data-ttu-id="55872-151">для регистров src0 и src1 требуется репликация свиззле.</span><span class="sxs-lookup"><span data-stu-id="55872-151">src0 and src1 registers require a replicate swizzle.</span></span>
-   <span data-ttu-id="55872-152">Если \_ блоки Comp должны заканчиваться инструкциями [else-VS](else---vs.md) или [endif-VS](endif---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="55872-152">if\_comp blocks must end with an [else - vs](else---vs.md) or [endif - vs](endif---vs.md) instruction.</span></span>
-   <span data-ttu-id="55872-153">Если \_ comp... [else-PS](else---ps.md)... [endif-блоки PS](endif---ps.md) не могут помешать блоку цикла.</span><span class="sxs-lookup"><span data-stu-id="55872-153">if\_comp...[else - ps](else---ps.md)...[endif - ps](endif---ps.md) blocks cannot straddle a loop block.</span></span> <span data-ttu-id="55872-154">\_Блок catch должен быть полностью внутри блока Loop или вне его.</span><span class="sxs-lookup"><span data-stu-id="55872-154">The if\_comp block must be completely inside or outside the loop block.</span></span>

## <a name="example"></a><span data-ttu-id="55872-155">Например, .</span><span class="sxs-lookup"><span data-stu-id="55872-155">Example</span></span>

<span data-ttu-id="55872-156">Эта инструкция обеспечивает условное динамическое управление потоком.</span><span class="sxs-lookup"><span data-stu-id="55872-156">This instruction provides conditional dynamic flow control.</span></span>


```
if_lt r3.x, r4.y
// Instructions to run if r3.x < r4.y

else
// Instructions to run otherwise

endif
```



## <a name="related-topics"></a><span data-ttu-id="55872-157">См. также</span><span class="sxs-lookup"><span data-stu-id="55872-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55872-158">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="55872-158">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




