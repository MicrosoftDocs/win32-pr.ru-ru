---
title: Сравнение if_comp
description: Запуск if bool-vs... else-vs... endif — блок VS с условием на основе значений, которые могут быть вычислены в шейдере. Эта инструкция используется для пропуска блока кода на основе условия.
ms.assetid: a3fe93c6-be26-4216-a601-3be52a74be06
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dadbe9620367efc75f821a711de89eb3498d247f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996847"
---
# <a name="if_comp---vs"></a><span data-ttu-id="5fc0c-104">Если \_ comp-VS</span><span class="sxs-lookup"><span data-stu-id="5fc0c-104">if\_comp - vs</span></span>

<span data-ttu-id="5fc0c-105">Запуск [If bool-VS](if-bool---vs.md)... [else-VS](else---vs.md)... [endif — блок VS](endif---vs.md) с условием на основе значений, которые могут быть вычислены в шейдере.</span><span class="sxs-lookup"><span data-stu-id="5fc0c-105">Start an [if bool - vs](if-bool---vs.md)...[else - vs](else---vs.md)...[endif - vs](endif---vs.md) block, with a condition based on values that could be computed in a shader.</span></span> <span data-ttu-id="5fc0c-106">Эта инструкция используется для пропуска блока кода на основе условия.</span><span class="sxs-lookup"><span data-stu-id="5fc0c-106">This instruction is used to skip a block of code, based on a condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fc0c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5fc0c-107">Syntax</span></span>



| <span data-ttu-id="5fc0c-108">Если \_ comp src0, src1</span><span class="sxs-lookup"><span data-stu-id="5fc0c-108">if\_comp src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="5fc0c-109">Где:</span><span class="sxs-lookup"><span data-stu-id="5fc0c-109">Where:</span></span>

-   <span data-ttu-id="5fc0c-110">\_Comp — это сравнение двух исходных регистров.</span><span class="sxs-lookup"><span data-stu-id="5fc0c-110">\_comp is a comparison between the two source registers.</span></span> <span data-ttu-id="5fc0c-111">Может принимать одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="5fc0c-111">It can be one of the following:</span></span> 

    | <span data-ttu-id="5fc0c-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5fc0c-112">Syntax</span></span> | <span data-ttu-id="5fc0c-113">Сравнение</span><span class="sxs-lookup"><span data-stu-id="5fc0c-113">Comparison</span></span>            |
    |--------|-----------------------|
    | <span data-ttu-id="5fc0c-114">\_gt</span><span class="sxs-lookup"><span data-stu-id="5fc0c-114">\_gt</span></span>   | <span data-ttu-id="5fc0c-115">Больше чем</span><span class="sxs-lookup"><span data-stu-id="5fc0c-115">Greater than</span></span>          |
    | <span data-ttu-id="5fc0c-116">\_светл</span><span class="sxs-lookup"><span data-stu-id="5fc0c-116">\_lt</span></span>   | <span data-ttu-id="5fc0c-117">Меньше чем</span><span class="sxs-lookup"><span data-stu-id="5fc0c-117">Less than</span></span>             |
    | <span data-ttu-id="5fc0c-118">\_GE</span><span class="sxs-lookup"><span data-stu-id="5fc0c-118">\_ge</span></span>   | <span data-ttu-id="5fc0c-119">Больше или равно</span><span class="sxs-lookup"><span data-stu-id="5fc0c-119">Greater than or equal</span></span> |
    | <span data-ttu-id="5fc0c-120">\_Le</span><span class="sxs-lookup"><span data-stu-id="5fc0c-120">\_le</span></span>   | <span data-ttu-id="5fc0c-121">Меньше или равно</span><span class="sxs-lookup"><span data-stu-id="5fc0c-121">Less than or equal</span></span>    |
    | <span data-ttu-id="5fc0c-122">\_EQ</span><span class="sxs-lookup"><span data-stu-id="5fc0c-122">\_eq</span></span>   | <span data-ttu-id="5fc0c-123">Равно</span><span class="sxs-lookup"><span data-stu-id="5fc0c-123">Equal to</span></span>              |
    | <span data-ttu-id="5fc0c-124">\_видимому</span><span class="sxs-lookup"><span data-stu-id="5fc0c-124">\_ne</span></span>   | <span data-ttu-id="5fc0c-125">Не равно</span><span class="sxs-lookup"><span data-stu-id="5fc0c-125">Not equal to</span></span>          |

    

     

-   <span data-ttu-id="5fc0c-126">src0 является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="5fc0c-126">src0 is a source register.</span></span> <span data-ttu-id="5fc0c-127">Для выбора компонента требуется репликация свиззле.</span><span class="sxs-lookup"><span data-stu-id="5fc0c-127">Replicate swizzle is required to select a component.</span></span>
-   <span data-ttu-id="5fc0c-128">src1 является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="5fc0c-128">src1 is a source register.</span></span> <span data-ttu-id="5fc0c-129">Для выбора компонента требуется репликация свиззле.</span><span class="sxs-lookup"><span data-stu-id="5fc0c-129">Replicate swizzle is required to select a component.</span></span>

## <a name="remarks"></a><span data-ttu-id="5fc0c-130">Примечания</span><span class="sxs-lookup"><span data-stu-id="5fc0c-130">Remarks</span></span>



| <span data-ttu-id="5fc0c-131">Версии шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="5fc0c-131">Vertex shader versions</span></span> | <span data-ttu-id="5fc0c-132">1\_1</span><span class="sxs-lookup"><span data-stu-id="5fc0c-132">1\_1</span></span> | <span data-ttu-id="5fc0c-133">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5fc0c-133">2\_0</span></span> | <span data-ttu-id="5fc0c-134">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="5fc0c-134">2\_x</span></span> | <span data-ttu-id="5fc0c-135">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="5fc0c-135">2\_sw</span></span> | <span data-ttu-id="5fc0c-136">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5fc0c-136">3\_0</span></span> | <span data-ttu-id="5fc0c-137">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="5fc0c-137">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="5fc0c-138">Если \_ comp</span><span class="sxs-lookup"><span data-stu-id="5fc0c-138">if\_comp</span></span>               |      |      | <span data-ttu-id="5fc0c-139">x</span><span class="sxs-lookup"><span data-stu-id="5fc0c-139">x</span></span>    | <span data-ttu-id="5fc0c-140">x</span><span class="sxs-lookup"><span data-stu-id="5fc0c-140">x</span></span>     | <span data-ttu-id="5fc0c-141">x</span><span class="sxs-lookup"><span data-stu-id="5fc0c-141">x</span></span>    | <span data-ttu-id="5fc0c-142">x</span><span class="sxs-lookup"><span data-stu-id="5fc0c-142">x</span></span>     |



 

<span data-ttu-id="5fc0c-143">Эта инструкция используется для пропуска блока кода на основе условия.</span><span class="sxs-lookup"><span data-stu-id="5fc0c-143">This instruction is used to skip a block of code, based on a condition.</span></span>


```
if_lt src0, src1
   jump to the corresponding else or endif instruction;
```



<span data-ttu-id="5fc0c-144">Будьте внимательны при использовании режимов сравнения «равно» и «не равно» для чисел с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="5fc0c-144">Be careful using the equals and not equals comparison modes on floating point numbers.</span></span> <span data-ttu-id="5fc0c-145">Поскольку округление происходит во время вычислений с плавающей запятой, для предотвращения ошибок можно выполнить сравнение со значением Эпсилон (небольшим ненулевым числом).</span><span class="sxs-lookup"><span data-stu-id="5fc0c-145">Because rounding occurs during during floating point calculations, the comparison can be done against an epsilon value (small nonzero number) to avoid errors.</span></span>

<span data-ttu-id="5fc0c-146">К ним относятся указанные ниже ограничения.</span><span class="sxs-lookup"><span data-stu-id="5fc0c-146">Restrictions include:</span></span>

-   <span data-ttu-id="5fc0c-147">Если \_ comp... [else-VS](else---vs.md)... [endif — блоки VS](endif---vs.md) (вместе с блоками в виде предикатов) могут быть вложены в глубину до 24 слоев.</span><span class="sxs-lookup"><span data-stu-id="5fc0c-147">if\_comp...[else - vs](else---vs.md)...[endif - vs](endif---vs.md) blocks (along with the predicated if blocks) can be nested up to 24 layers deep.</span></span>
-   <span data-ttu-id="5fc0c-148">для регистров src0 и src1 требуется репликация свиззле.</span><span class="sxs-lookup"><span data-stu-id="5fc0c-148">src0 and src1 registers require a replicate swizzle.</span></span>
-   <span data-ttu-id="5fc0c-149">Если \_ блоки Comp должны заканчиваться инструкциями [else-VS](else---vs.md) или [endif-VS](endif---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="5fc0c-149">if\_comp blocks must end with an [else - vs](else---vs.md) or [endif - vs](endif---vs.md) instruction.</span></span>
-   <span data-ttu-id="5fc0c-150">Если \_ comp... [else-VS](else---vs.md)... [endif — блоки VS](endif---vs.md) не могут помешать блоку цикла.</span><span class="sxs-lookup"><span data-stu-id="5fc0c-150">if\_comp...[else - vs](else---vs.md)...[endif - vs](endif---vs.md) blocks cannot straddle a loop block.</span></span> <span data-ttu-id="5fc0c-151">Блок if \_ должен быть полностью внутри блока [цикла VS](loop---vs.md) или снаружи.</span><span class="sxs-lookup"><span data-stu-id="5fc0c-151">The if\_comp block must be completely inside, or outside the [loop - vs](loop---vs.md) block.</span></span>

## <a name="example"></a><span data-ttu-id="5fc0c-152">Например, .</span><span class="sxs-lookup"><span data-stu-id="5fc0c-152">Example</span></span>

<span data-ttu-id="5fc0c-153">Эта инструкция обеспечивает условное динамическое управление потоком.</span><span class="sxs-lookup"><span data-stu-id="5fc0c-153">This instruction provides conditional dynamic flow control.</span></span>


```
if_lt r3.x, r4.y
// Instructions to run if r3.x < r4.y

else
// Instructions to run otherwise

endif
```



## <a name="related-topics"></a><span data-ttu-id="5fc0c-154">См. также</span><span class="sxs-lookup"><span data-stu-id="5fc0c-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5fc0c-155">Инструкции шейдера вершин</span><span class="sxs-lookup"><span data-stu-id="5fc0c-155">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




