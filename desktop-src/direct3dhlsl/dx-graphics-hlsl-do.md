---
title: Оператор Do (ОЦидл. h)
description: Непрерывно выполнять последовательность операторов до тех пор, пока не завершится выполнение условного выражения.
ms.assetid: 07fd37b0-59c2-404b-a755-7178e4a058e4
keywords:
- Do, инструкция HLSL
topic_type:
- apiref
api_name:
- do Statement
api_location:
- ocidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1f019af77ef0021ad0574bf703ff2a2a52ac0f6
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118789"
---
# <a name="do-statement"></a><span data-ttu-id="2fa54-104">Do, инструкция</span><span class="sxs-lookup"><span data-stu-id="2fa54-104">do Statement</span></span>

<span data-ttu-id="2fa54-105">Непрерывно выполнять последовательность операторов до тех пор, пока не завершится выполнение условного выражения.</span><span class="sxs-lookup"><span data-stu-id="2fa54-105">Execute a series of statements continuously until the conditional expression fails.</span></span>

<span data-ttu-id="2fa54-106">\[*Атрибут* \] Do { *блок операторов*;} while ( *Условный* );</span><span class="sxs-lookup"><span data-stu-id="2fa54-106">\[*Attribute*\] do {   *Statement Block*; } while( *Conditional* );</span></span>



 

## <a name="parameters"></a><span data-ttu-id="2fa54-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="2fa54-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2fa54-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Версию*</span><span class="sxs-lookup"><span data-stu-id="2fa54-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attribute*</span></span>
</dt> <dd>

<span data-ttu-id="2fa54-109">Необязательный параметр, управляющий компиляцией инструкции.</span><span class="sxs-lookup"><span data-stu-id="2fa54-109">An optional parameter that controls how the statement is compiled.</span></span>



| <span data-ttu-id="2fa54-110">attribute</span><span class="sxs-lookup"><span data-stu-id="2fa54-110">Attribute</span></span> | <span data-ttu-id="2fa54-111">Описание</span><span class="sxs-lookup"><span data-stu-id="2fa54-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2fa54-112">фастопт</span><span class="sxs-lookup"><span data-stu-id="2fa54-112">fastopt</span></span>   | <span data-ttu-id="2fa54-113">Сокращает время компиляции, но создает менее агрессивные оптимизации.</span><span class="sxs-lookup"><span data-stu-id="2fa54-113">Reduces the compile time but produces less aggressive optimizations.</span></span> <span data-ttu-id="2fa54-114">При использовании этого атрибута компилятор не будет выполнять откат.</span><span class="sxs-lookup"><span data-stu-id="2fa54-114">If you use this attribute, the compiler will not unroll loops.</span></span><br/> <span data-ttu-id="2fa54-115">Этот атрибут влияет только на цели модели шейдеров, поддерживающие инструкции по [прерыванию](dx-graphics-hlsl-break.md) .</span><span class="sxs-lookup"><span data-stu-id="2fa54-115">This attribute affects only shader model targets that support [break](dx-graphics-hlsl-break.md) instructions.</span></span> <span data-ttu-id="2fa54-116">Этот атрибут доступен в модели шейдеров [VS \_ 2 \_ x](dx9-graphics-reference-asm-vs-2-x.md) и [шейдере 3](dx-graphics-hlsl-sm3.md) и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="2fa54-116">This attribute is available in shader model [vs\_2\_x](dx9-graphics-reference-asm-vs-2-x.md) and [shader model 3](dx-graphics-hlsl-sm3.md) and later.</span></span> <span data-ttu-id="2fa54-117">Он особенно полезен в [модели шейдеров 4](dx-graphics-hlsl-sm4.md) и более поздних версиях, когда компилятор компилирует циклы.</span><span class="sxs-lookup"><span data-stu-id="2fa54-117">It is particularly useful in [shader model 4](dx-graphics-hlsl-sm4.md) and later when the compiler compiles loops.</span></span> <span data-ttu-id="2fa54-118">Компилятор имитирует циклы по умолчанию, чтобы определить, может ли он их отменить.</span><span class="sxs-lookup"><span data-stu-id="2fa54-118">The compiler simulates loops by default to evaluate whether it can unroll them.</span></span> <span data-ttu-id="2fa54-119">Если не нужно, чтобы компилятор выпало из циклов, используйте этот атрибут для сокращения времени компиляции.</span><span class="sxs-lookup"><span data-stu-id="2fa54-119">If you do not want the compiler to unroll loops, use this attribute to reduce compile time.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2fa54-120"><span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Блок инструкции*</span><span class="sxs-lookup"><span data-stu-id="2fa54-120"><span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Statement Block*</span></span>
</dt> <dd>

<span data-ttu-id="2fa54-121">Одна или несколько [инструкций](dx-graphics-hlsl-statement-blocks.md).</span><span class="sxs-lookup"><span data-stu-id="2fa54-121">One or more [statements](dx-graphics-hlsl-statement-blocks.md).</span></span>

</dd> <dt>

<span data-ttu-id="2fa54-122"><span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Условие*</span><span class="sxs-lookup"><span data-stu-id="2fa54-122"><span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Conditional*</span></span>
</dt> <dd>

<span data-ttu-id="2fa54-123">Условное [выражение](dx-graphics-hlsl-expressions.md).</span><span class="sxs-lookup"><span data-stu-id="2fa54-123">A conditional [expression](dx-graphics-hlsl-expressions.md).</span></span> <span data-ttu-id="2fa54-124">Блок операторов выполняется перед вычислением выражения.</span><span class="sxs-lookup"><span data-stu-id="2fa54-124">The statement block is executed before the expression is evaluated.</span></span> <span data-ttu-id="2fa54-125">Цикл завершается, когда выражение принимает значение false.</span><span class="sxs-lookup"><span data-stu-id="2fa54-125">The loop is exited when the expression evaluates to false.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2fa54-126">Требования</span><span class="sxs-lookup"><span data-stu-id="2fa54-126">Requirements</span></span>



| <span data-ttu-id="2fa54-127">Требование</span><span class="sxs-lookup"><span data-stu-id="2fa54-127">Requirement</span></span> | <span data-ttu-id="2fa54-128">Значение</span><span class="sxs-lookup"><span data-stu-id="2fa54-128">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2fa54-129">Заголовок</span><span class="sxs-lookup"><span data-stu-id="2fa54-129">Header</span></span><br/> | <dl> <span data-ttu-id="2fa54-130"><dt>ОЦидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="2fa54-130"><dt>Ocidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2fa54-131">См. также</span><span class="sxs-lookup"><span data-stu-id="2fa54-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fa54-132">Управление потоком</span><span class="sxs-lookup"><span data-stu-id="2fa54-132">Flow Control</span></span>](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 





