---
title: Оператор for
description: Итеративно выполняет последовательность инструкций на основе вычисления условного выражения.
ms.assetid: d795c89e-7088-4bf3-93a8-798ed9c1a353
keywords:
- для инструкции HLSL
topic_type:
- apiref
api_name:
- for Statement
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 50f8c18ebc23455563b4b3e6bfee72bfa9d3ec4c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104133122"
---
# <a name="for-statement"></a><span data-ttu-id="6463a-104">Оператор for</span><span class="sxs-lookup"><span data-stu-id="6463a-104">for Statement</span></span>

<span data-ttu-id="6463a-105">Итеративно выполняет последовательность инструкций на основе вычисления условного выражения.</span><span class="sxs-lookup"><span data-stu-id="6463a-105">Iteratively executes a series of statements, based on the evaluation of the conditional expression.</span></span>



|                                                                                       |
|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6463a-106">\[*Атрибут* \] для ( *инициализатор; Условие Итератор* ) { *блок операторов*;}</span><span class="sxs-lookup"><span data-stu-id="6463a-106">\[*Attribute*\] for ( *Initializer; Conditional; Iterator* ) {   *Statement Block*; }</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="6463a-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="6463a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6463a-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Версию*</span><span class="sxs-lookup"><span data-stu-id="6463a-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attribute*</span></span>
</dt> <dd>

<span data-ttu-id="6463a-109">Необязательный параметр, управляющий компиляцией инструкции.</span><span class="sxs-lookup"><span data-stu-id="6463a-109">An optional parameter that controls how the statement is compiled.</span></span> <span data-ttu-id="6463a-110">Если атрибут не указан, компилятор сначала попытается создать свернутую версию цикла, если это не удается, или если некоторые операции были бы проще, если цикл был отменен, будет возвращено к несвернутой версии цикла.</span><span class="sxs-lookup"><span data-stu-id="6463a-110">When no attribute is specified the compiler will first attempt to emit a rolled version of the loop, and if that fails, or if some operations would be easier if the loop was unrolled, will fall back to an unrolled version of the loop.</span></span>



| <span data-ttu-id="6463a-111">attribute</span><span class="sxs-lookup"><span data-stu-id="6463a-111">Attribute</span></span>             | <span data-ttu-id="6463a-112">Описание</span><span class="sxs-lookup"><span data-stu-id="6463a-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6463a-113">unroll (x)</span><span class="sxs-lookup"><span data-stu-id="6463a-113">unroll(x)</span></span>             | <span data-ttu-id="6463a-114">Выполните откат цикла до тех пор, пока не прекратится выполнение.</span><span class="sxs-lookup"><span data-stu-id="6463a-114">Unroll the loop until it stops executing.</span></span> <span data-ttu-id="6463a-115">При необходимости можно указать максимальное число запусков цикла.</span><span class="sxs-lookup"><span data-stu-id="6463a-115">Can optionally specify the maximum number of times the loop is to execute.</span></span> <span data-ttu-id="6463a-116">Не совместимо с атрибутом **\[ Loop \]** .</span><span class="sxs-lookup"><span data-stu-id="6463a-116">Not compatible with the **\[loop\]** attribute.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="6463a-117">loop</span><span class="sxs-lookup"><span data-stu-id="6463a-117">loop</span></span>                  | <span data-ttu-id="6463a-118">Создание кода, использующего управление потоком для выполнения каждой итерации цикла.</span><span class="sxs-lookup"><span data-stu-id="6463a-118">Generate code that uses flow control to execute each iteration of the loop.</span></span> <span data-ttu-id="6463a-119">Не совместимо с атрибутом **\[ unrollа \]** .</span><span class="sxs-lookup"><span data-stu-id="6463a-119">Not compatible with the **\[unroll\]** attribute.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="6463a-120">фастопт</span><span class="sxs-lookup"><span data-stu-id="6463a-120">fastopt</span></span>               | <span data-ttu-id="6463a-121">Сокращает время компиляции, но создает менее агрессивные оптимизации.</span><span class="sxs-lookup"><span data-stu-id="6463a-121">Reduces the compile time but produces less aggressive optimizations.</span></span> <span data-ttu-id="6463a-122">При использовании этого атрибута компилятор не будет выполнять откат.</span><span class="sxs-lookup"><span data-stu-id="6463a-122">If you use this attribute, the compiler will not unroll loops.</span></span><br/> <span data-ttu-id="6463a-123">Этот атрибут влияет только на цели модели шейдеров, поддерживающие инструкции по [прерыванию](dx-graphics-hlsl-break.md) .</span><span class="sxs-lookup"><span data-stu-id="6463a-123">This attribute affects only shader model targets that support [break](dx-graphics-hlsl-break.md) instructions.</span></span> <span data-ttu-id="6463a-124">Этот атрибут доступен в модели шейдеров [VS \_ 2 \_ x](dx9-graphics-reference-asm-vs-2-x.md) и [шейдере 3](dx-graphics-hlsl-sm3.md) и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="6463a-124">This attribute is available in shader model [vs\_2\_x](dx9-graphics-reference-asm-vs-2-x.md) and [shader model 3](dx-graphics-hlsl-sm3.md) and later.</span></span> <span data-ttu-id="6463a-125">Он особенно полезен в [модели шейдеров 4](dx-graphics-hlsl-sm4.md) и более поздних версиях, когда компилятор компилирует циклы.</span><span class="sxs-lookup"><span data-stu-id="6463a-125">It is particularly useful in [shader model 4](dx-graphics-hlsl-sm4.md) and later when the compiler compiles loops.</span></span> <span data-ttu-id="6463a-126">Компилятор имитирует циклы по умолчанию, чтобы определить, может ли он их отменить.</span><span class="sxs-lookup"><span data-stu-id="6463a-126">The compiler simulates loops by default to evaluate whether it can unroll them.</span></span> <span data-ttu-id="6463a-127">Если не нужно, чтобы компилятор выпало из циклов, используйте этот атрибут для сокращения времени компиляции.</span><span class="sxs-lookup"><span data-stu-id="6463a-127">If you do not want the compiler to unroll loops, use this attribute to reduce compile time.</span></span> <br/> |
| <span data-ttu-id="6463a-128">Разрешить \_ \_ условие UAV</span><span class="sxs-lookup"><span data-stu-id="6463a-128">allow\_uav\_condition</span></span> | <span data-ttu-id="6463a-129">Позволяет использовать условие завершения цикла шейдера для UAV чтения.</span><span class="sxs-lookup"><span data-stu-id="6463a-129">Allows a compute shader loop termination condition to be based off of a UAV read.</span></span> <span data-ttu-id="6463a-130">Цикл не должен содержать встроенные функции синхронизации.</span><span class="sxs-lookup"><span data-stu-id="6463a-130">The loop must not contain synchronization intrinsics.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="6463a-131"><span id="Initializer"></span><span id="initializer"></span><span id="INITIALIZER"></span>*Initializer*</span><span class="sxs-lookup"><span data-stu-id="6463a-131"><span id="Initializer"></span><span id="initializer"></span><span id="INITIALIZER"></span>*Initializer*</span></span>
</dt> <dd>

<span data-ttu-id="6463a-132">Начальное значение счетчика цикла.</span><span class="sxs-lookup"><span data-stu-id="6463a-132">The initial value of the loop counter.</span></span>

</dd> <dt>

<span data-ttu-id="6463a-133"><span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Условие*</span><span class="sxs-lookup"><span data-stu-id="6463a-133"><span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Conditional*</span></span>
</dt> <dd>

<span data-ttu-id="6463a-134">Условное [выражение](dx-graphics-hlsl-expressions.md).</span><span class="sxs-lookup"><span data-stu-id="6463a-134">A conditional [expression](dx-graphics-hlsl-expressions.md).</span></span> <span data-ttu-id="6463a-135">Если условное выражение имеет значение true, то выполняется блок операторов.</span><span class="sxs-lookup"><span data-stu-id="6463a-135">If the conditional expression evaluates to true, the statement block is executed.</span></span> <span data-ttu-id="6463a-136">Цикл завершается, когда выражение принимает значение false.</span><span class="sxs-lookup"><span data-stu-id="6463a-136">The loop ends when the expression evaluates to false.</span></span>

</dd> <dt>

<span data-ttu-id="6463a-137"><span id="Iterator"></span><span id="iterator"></span><span id="ITERATOR"></span>*Итераци*</span><span class="sxs-lookup"><span data-stu-id="6463a-137"><span id="Iterator"></span><span id="iterator"></span><span id="ITERATOR"></span>*Iterator*</span></span>
</dt> <dd>

<span data-ttu-id="6463a-138">Обновите значение счетчика цикла.</span><span class="sxs-lookup"><span data-stu-id="6463a-138">Update the value of the loop counter.</span></span>

</dd> <dt>

<span data-ttu-id="6463a-139"><span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Блок инструкции*</span><span class="sxs-lookup"><span data-stu-id="6463a-139"><span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Statement Block*</span></span>
</dt> <dd>

<span data-ttu-id="6463a-140">Одна или несколько [инструкций HLSL](dx-graphics-hlsl-statement-blocks.md).</span><span class="sxs-lookup"><span data-stu-id="6463a-140">One or more [HLSL statements](dx-graphics-hlsl-statement-blocks.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6463a-141">Примечания</span><span class="sxs-lookup"><span data-stu-id="6463a-141">Remarks</span></span>

<span data-ttu-id="6463a-142">Атрибуты " **\[ unroll \]** " и " **\[ цикл \]** " являются взаимоисключающими и будут формировать ошибки компилятора, если указаны оба значения.</span><span class="sxs-lookup"><span data-stu-id="6463a-142">The **\[unroll\]** and **\[loop\]** attributes are mutually exclusive and will generate compiler errors when both are specified.</span></span>

<span data-ttu-id="6463a-143">Атрибуты **\[ \]** **\[ \_ \_ условия \] фастопт и Allow UAV** игнорируются, если задан параметр **\[ unroll \]** .</span><span class="sxs-lookup"><span data-stu-id="6463a-143">The **\[fastopt\]** and **\[allow\_uav\_condition\]** attributes are ignored if **\[unroll\]** is specified.</span></span>

## <a name="see-also"></a><span data-ttu-id="6463a-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6463a-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6463a-145">Управление потоком</span><span class="sxs-lookup"><span data-stu-id="6463a-145">Flow Control</span></span>](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 





