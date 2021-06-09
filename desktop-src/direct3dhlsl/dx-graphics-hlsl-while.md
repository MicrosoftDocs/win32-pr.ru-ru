---
title: Оператор while
description: Выполняет блок инструкции до тех пор, пока не завершится выполнение условного выражения.
ms.assetid: 0fe420db-3c09-40bd-b689-f85c02e2f817
keywords:
- While, инструкция HLSL
topic_type:
- apiref
api_name:
- while Statement
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7bf1f0049ac474e7840753a8cfe05c972aa346c1
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826677"
---
# <a name="while-statement"></a><span data-ttu-id="e1794-104">Оператор while</span><span class="sxs-lookup"><span data-stu-id="e1794-104">while Statement</span></span>

<span data-ttu-id="e1794-105">Выполняет блок инструкции до тех пор, пока не завершится выполнение условного выражения.</span><span class="sxs-lookup"><span data-stu-id="e1794-105">Executes a statement block until the conditional expression fails.</span></span>

<span data-ttu-id="e1794-106">\[*Атрибут* \] while ( *Условный* ) { *блок операторов*;}</span><span class="sxs-lookup"><span data-stu-id="e1794-106">\[*Attribute*\] while ( *Conditional* ) {   *Statement Block*; }</span></span>



 

## <a name="parameters"></a><span data-ttu-id="e1794-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="e1794-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1794-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Версию*</span><span class="sxs-lookup"><span data-stu-id="e1794-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attribute*</span></span>
</dt> <dd>

<span data-ttu-id="e1794-109">Необязательный параметр, управляющий компиляцией инструкции.</span><span class="sxs-lookup"><span data-stu-id="e1794-109">An optional parameter that controls how the statement is compiled.</span></span>



| <span data-ttu-id="e1794-110">attribute</span><span class="sxs-lookup"><span data-stu-id="e1794-110">Attribute</span></span>             | <span data-ttu-id="e1794-111">Описание</span><span class="sxs-lookup"><span data-stu-id="e1794-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1794-112">unroll (x)</span><span class="sxs-lookup"><span data-stu-id="e1794-112">unroll(x)</span></span>             | <span data-ttu-id="e1794-113">Выполните откат цикла до тех пор, пока не прекратится выполнение.</span><span class="sxs-lookup"><span data-stu-id="e1794-113">Unroll the loop until it stops executing.</span></span> <span data-ttu-id="e1794-114">При необходимости можно указать максимальное число запусков цикла.</span><span class="sxs-lookup"><span data-stu-id="e1794-114">Optionally, you can specify the maximum number of times the loop can execute.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="e1794-115">loop</span><span class="sxs-lookup"><span data-stu-id="e1794-115">loop</span></span>                  | <span data-ttu-id="e1794-116">Используйте инструкции управления потоком в скомпилированном шейдере. не расвращайте цикл.</span><span class="sxs-lookup"><span data-stu-id="e1794-116">Use flow-control statements in the compiled shader; do not unroll the loop.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="e1794-117">фастопт</span><span class="sxs-lookup"><span data-stu-id="e1794-117">fastopt</span></span>               | <span data-ttu-id="e1794-118">Сокращает время компиляции, но создает менее агрессивные оптимизации.</span><span class="sxs-lookup"><span data-stu-id="e1794-118">Reduces the compile time but produces less aggressive optimizations.</span></span> <span data-ttu-id="e1794-119">При использовании этого атрибута компилятор не будет выполнять откат.</span><span class="sxs-lookup"><span data-stu-id="e1794-119">If you use this attribute, the compiler will not unroll loops.</span></span><br/> <span data-ttu-id="e1794-120">Этот атрибут влияет только на цели модели шейдеров, поддерживающие инструкции по [прерыванию](dx-graphics-hlsl-break.md) .</span><span class="sxs-lookup"><span data-stu-id="e1794-120">This attribute affects only shader model targets that support [break](dx-graphics-hlsl-break.md) instructions.</span></span> <span data-ttu-id="e1794-121">Этот атрибут доступен в модели шейдеров [VS \_ 2 \_ x](dx9-graphics-reference-asm-vs-2-x.md) и [шейдере 3](dx-graphics-hlsl-sm3.md) и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="e1794-121">This attribute is available in shader model [vs\_2\_x](dx9-graphics-reference-asm-vs-2-x.md) and [shader model 3](dx-graphics-hlsl-sm3.md) and later.</span></span> <span data-ttu-id="e1794-122">Он особенно полезен в [модели шейдеров 4](dx-graphics-hlsl-sm4.md) и более поздних версиях, когда компилятор компилирует циклы.</span><span class="sxs-lookup"><span data-stu-id="e1794-122">It is particularly useful in [shader model 4](dx-graphics-hlsl-sm4.md) and later when the compiler compiles loops.</span></span> <span data-ttu-id="e1794-123">Компилятор имитирует циклы по умолчанию, чтобы определить, может ли он их отменить.</span><span class="sxs-lookup"><span data-stu-id="e1794-123">The compiler simulates loops by default to evaluate whether it can unroll them.</span></span> <span data-ttu-id="e1794-124">Если не нужно, чтобы компилятор выпало из циклов, используйте этот атрибут для сокращения времени компиляции.</span><span class="sxs-lookup"><span data-stu-id="e1794-124">If you do not want the compiler to unroll loops, use this attribute to reduce compile time.</span></span><br/> |
| <span data-ttu-id="e1794-125">Разрешить \_ \_ условие UAV</span><span class="sxs-lookup"><span data-stu-id="e1794-125">allow\_uav\_condition</span></span> | <span data-ttu-id="e1794-126">Позволяет использовать условие завершения цикла шейдера для UAV чтения.</span><span class="sxs-lookup"><span data-stu-id="e1794-126">Allows a compute shader loop termination condition to be based off of a UAV read.</span></span> <span data-ttu-id="e1794-127">Цикл не должен содержать встроенные функции синхронизации.</span><span class="sxs-lookup"><span data-stu-id="e1794-127">The loop must not contain synchronization intrinsics.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="e1794-128"><span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Условие*</span><span class="sxs-lookup"><span data-stu-id="e1794-128"><span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Conditional*</span></span>
</dt> <dd>

<span data-ttu-id="e1794-129">Условное [выражение](dx-graphics-hlsl-expressions.md).</span><span class="sxs-lookup"><span data-stu-id="e1794-129">A conditional [expression](dx-graphics-hlsl-expressions.md).</span></span> <span data-ttu-id="e1794-130">Если выражение принимает значение true, выполняется блок операторов.</span><span class="sxs-lookup"><span data-stu-id="e1794-130">If the expression evaluates to true, the statement block is executed.</span></span> <span data-ttu-id="e1794-131">Цикл завершается, когда выражение принимает значение false.</span><span class="sxs-lookup"><span data-stu-id="e1794-131">The loop ends when the expression evaluates to false.</span></span>

</dd> <dt>

<span data-ttu-id="e1794-132"><span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Блок инструкции*</span><span class="sxs-lookup"><span data-stu-id="e1794-132"><span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Statement Block*</span></span>
</dt> <dd>

<span data-ttu-id="e1794-133">Одна или несколько [инструкций](dx-graphics-hlsl-statement-blocks.md).</span><span class="sxs-lookup"><span data-stu-id="e1794-133">One or more [statements](dx-graphics-hlsl-statement-blocks.md).</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="e1794-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e1794-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1794-135">Управление потоком</span><span class="sxs-lookup"><span data-stu-id="e1794-135">Flow Control</span></span>](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 





