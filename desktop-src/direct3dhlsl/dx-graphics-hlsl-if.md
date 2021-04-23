---
title: Оператор if
description: Условно выполняет ряд инструкций на основе вычисления условного выражения.
ms.assetid: ed4e347b-b5ee-40bc-a3f8-36e83ccf45b8
keywords:
- Оператор If HLSL
topic_type:
- apiref
api_name:
- if Statement
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8e8a3c20e73b9783d39b4f4cbdb7c0be5b75fcda
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/11/2020
ms.locfileid: "104069502"
---
# <a name="if-statement"></a><span data-ttu-id="9708c-104">Оператор if</span><span class="sxs-lookup"><span data-stu-id="9708c-104">if Statement</span></span>

<span data-ttu-id="9708c-105">Условно выполняет ряд инструкций на основе вычисления условного выражения.</span><span class="sxs-lookup"><span data-stu-id="9708c-105">Conditionally execute a series of statements, based on the evaluation of the conditional expression.</span></span>



|                                                               |
|---------------------------------------------------------------|
| <span data-ttu-id="9708c-106">\[*Атрибут* \] If ( *Условный* ) { *блок операторов*;}</span><span class="sxs-lookup"><span data-stu-id="9708c-106">\[*Attribute*\] if ( *Conditional* ) {   *Statement Block*; }</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="9708c-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="9708c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9708c-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Версию*</span><span class="sxs-lookup"><span data-stu-id="9708c-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attribute*</span></span>
</dt> <dd>

<span data-ttu-id="9708c-109">Необязательный параметр, управляющий компиляцией инструкции.</span><span class="sxs-lookup"><span data-stu-id="9708c-109">An optional parameter that controls how the statement is compiled.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9708c-110">attribute</span><span class="sxs-lookup"><span data-stu-id="9708c-110">Attribute</span></span></th>
<th><span data-ttu-id="9708c-111">Описание</span><span class="sxs-lookup"><span data-stu-id="9708c-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9708c-112">ветвь</span><span class="sxs-lookup"><span data-stu-id="9708c-112">branch</span></span></td>
<td><span data-ttu-id="9708c-113">Оцените только одну сторону оператора if в зависимости от заданного условия.</span><span class="sxs-lookup"><span data-stu-id="9708c-113">Evaluate only one side of the if statement depending on the given condition.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="9708c-114">При использовании <a href="dx-graphics-hlsl-sm2.md">модели шейдеров 2. x</a> или <a href="dx-graphics-hlsl-sm3.md">Shader Model 3,0</a>каждый раз при использовании динамического ветвления используются ресурсы.</span><span class="sxs-lookup"><span data-stu-id="9708c-114">When you use <a href="dx-graphics-hlsl-sm2.md">Shader Model 2.x</a> or <a href="dx-graphics-hlsl-sm3.md">Shader Model 3.0</a>, each time you use dynamic branching you consume resources.</span></span> <span data-ttu-id="9708c-115">Поэтому при чрезмерном использовании динамической ветви при выборе этих профилей могут возникнуть ошибки компиляции.</span><span class="sxs-lookup"><span data-stu-id="9708c-115">So, if you use dynamic branching excessively when you target these profiles, you can receive compilation errors.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9708c-116">преобразовать в плоский формат</span><span class="sxs-lookup"><span data-stu-id="9708c-116">flatten</span></span></td>
<td><span data-ttu-id="9708c-117">Оцените обе стороны оператора if и выберите один из двух результирующих значений.</span><span class="sxs-lookup"><span data-stu-id="9708c-117">Evaluate both sides of the if statement and choose between the two resulting values.</span></span></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="9708c-118"><span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Условие*</span><span class="sxs-lookup"><span data-stu-id="9708c-118"><span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Conditional*</span></span>
</dt> <dd>

<span data-ttu-id="9708c-119">Условное [выражение](dx-graphics-hlsl-expressions.md).</span><span class="sxs-lookup"><span data-stu-id="9708c-119">A conditional [expression](dx-graphics-hlsl-expressions.md).</span></span> <span data-ttu-id="9708c-120">Выражение вычисляется, и, если значение true, выполняется блок операторов.</span><span class="sxs-lookup"><span data-stu-id="9708c-120">The expression is evaluated, and if true, the statement block is executed.</span></span>

</dd> <dt>

<span data-ttu-id="9708c-121"><span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Блок инструкции*</span><span class="sxs-lookup"><span data-stu-id="9708c-121"><span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Statement Block*</span></span>
</dt> <dd>

<span data-ttu-id="9708c-122">Одна или несколько [инструкций HLSL](dx-graphics-hlsl-statement-blocks.md).</span><span class="sxs-lookup"><span data-stu-id="9708c-122">One or more [HLSL statements](dx-graphics-hlsl-statement-blocks.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9708c-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="9708c-123">Remarks</span></span>

<span data-ttu-id="9708c-124">Если компилятор использует метод ветвления для компиляции оператора if, он создаст код, который будет оценивать только одну сторону оператора if в зависимости от заданного условия.</span><span class="sxs-lookup"><span data-stu-id="9708c-124">When the compiler uses the branch method for compiling an if statement it will generate code that will evaluate only one side of the if statement depending on the given condition.</span></span> <span data-ttu-id="9708c-125">Например, в операторе if:</span><span class="sxs-lookup"><span data-stu-id="9708c-125">For example, in the if statement:</span></span>


```
[branch] if(x)
{
    x = sqrt(x);
}
```



<span data-ttu-id="9708c-126">Оператор **If** имеет неявный блок Else, эквивалентный x = x.</span><span class="sxs-lookup"><span data-stu-id="9708c-126">The **if** statement has an implicit else block, which is equivalent to x = x.</span></span> <span data-ttu-id="9708c-127">Поскольку мы представили компилятору инструкцию использовать метод Branch с предыдущим атрибутом Branch, скомпилированный код вычислит x и выполнит только часть, которая должна быть выполнена. Если значение x равно нулю, то выполняется и **другая** сторона, и если он не равен нулю, то будет выполняться сторона **then** .</span><span class="sxs-lookup"><span data-stu-id="9708c-127">Because we have told the compiler to use the branch method with the preceding branch attribute, the compiled code will evaluate x and execute only the side that should be executed; if x is zero, then it will execute the **else** side, and if it is non-zero it will execute the **then** side.</span></span>

<span data-ttu-id="9708c-128">И наоборот, если используется атрибут **спрямления** , скомпилированный код будет оценивать обе стороны оператора **If** и выбирать между двумя результирующими значениями, используя исходное значение x.</span><span class="sxs-lookup"><span data-stu-id="9708c-128">Conversely, if the **flatten** attribute is used, then the compiled code will evaluate both sides of the **if** statement and choose between the two resulting values using the original value of x.</span></span> <span data-ttu-id="9708c-129">Ниже приведен пример использования атрибута «сведение»:</span><span class="sxs-lookup"><span data-stu-id="9708c-129">Here is an example of a usage of the flatten attribute:</span></span>


```
[flatten] if(x)
{
    x = sqrt(x);
}
```



<span data-ttu-id="9708c-130">В некоторых случаях использование атрибутов branch или "сведение" может привести к ошибке компиляции.</span><span class="sxs-lookup"><span data-stu-id="9708c-130">There are certain cases where using the branch or flatten attributes may generate a compile error.</span></span> <span data-ttu-id="9708c-131">Атрибут Branch может завершиться ошибкой, если одна из сторон оператора If содержит функцию градиента, например [**tex2D**](dx-graphics-hlsl-tex2d.md).</span><span class="sxs-lookup"><span data-stu-id="9708c-131">The branch attribute may fail if either side of the if statement contains a gradient function, such as [**tex2D**](dx-graphics-hlsl-tex2d.md).</span></span> <span data-ttu-id="9708c-132">Атрибут «сведение» может завершиться ошибкой, если обе стороны оператора if содержат инструкцию добавления потока или любую другую инструкцию, имеющую побочные эффекты.</span><span class="sxs-lookup"><span data-stu-id="9708c-132">The flatten attribute may fail if either side of the if statement contains a stream append statement or any other statement that has side-effects.</span></span>

<span data-ttu-id="9708c-133">Оператор **If** может также использовать необязательный блок else.</span><span class="sxs-lookup"><span data-stu-id="9708c-133">An **if** statement can also use an optional else block.</span></span> <span data-ttu-id="9708c-134">Если выражение **If** имеет значение true, обрабатывается код в блоке инструкций, связанного с оператором if.</span><span class="sxs-lookup"><span data-stu-id="9708c-134">If the **if** expression is true, the code in the statement block associated with the if statement is processed.</span></span> <span data-ttu-id="9708c-135">В противном случае обрабатывается блок инструкций, связанный с необязательным блоком Else.</span><span class="sxs-lookup"><span data-stu-id="9708c-135">Otherwise, the statement block associated with the optional else block is processed.</span></span>

## <a name="see-also"></a><span data-ttu-id="9708c-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9708c-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9708c-137">Управление потоком</span><span class="sxs-lookup"><span data-stu-id="9708c-137">Flow Control</span></span>](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 





