---
title: Операторы
description: Выражения — это последовательности переменных и литералов, прерывистого операторами.
ms.assetid: c31aa0b8-1284-48aa-b000-d72433f0f5cc
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 69fc29f366fa781483edb5fd4653674b387fd156
ms.sourcegitcommit: 37fb32f6150b6ca1db6c52d68a553ec2c8c0879a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2020
ms.locfileid: "104487333"
---
# <a name="operators"></a><span data-ttu-id="d2cb7-103">Операторы</span><span class="sxs-lookup"><span data-stu-id="d2cb7-103">Operators</span></span>

<span data-ttu-id="d2cb7-104">Выражения — это последовательности [переменных](dx-graphics-hlsl-variable-syntax.md) и литералов, прерывистого [операторами](dx-graphics-hlsl-statement-blocks.md).</span><span class="sxs-lookup"><span data-stu-id="d2cb7-104">Expressions are sequences of [variables](dx-graphics-hlsl-variable-syntax.md) and literals punctuated by [operators](dx-graphics-hlsl-statement-blocks.md).</span></span> <span data-ttu-id="d2cb7-105">Операторы определяют, как переменные и литералы объединяются, сравниваются, выбираются и т. д.</span><span class="sxs-lookup"><span data-stu-id="d2cb7-105">Operators determine how the variables and literals are combined, compared, selected, and so on.</span></span> <span data-ttu-id="d2cb7-106">К операторам относятся:</span><span class="sxs-lookup"><span data-stu-id="d2cb7-106">The operators include:</span></span>



|                                                                                 |                                                                    |
|---------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="d2cb7-107">Имя оператора</span><span class="sxs-lookup"><span data-stu-id="d2cb7-107">Operator Name</span></span>                                                                   | <span data-ttu-id="d2cb7-108">Операторы</span><span class="sxs-lookup"><span data-stu-id="d2cb7-108">Operators</span></span>                                                          |
| [<span data-ttu-id="d2cb7-109">Аддитивные и Мультипликативные операторы</span><span class="sxs-lookup"><span data-stu-id="d2cb7-109">Additive and Multiplicative Operators</span></span>](#additive-and-multiplicative-operators) | <span data-ttu-id="d2cb7-110">+, -, \*, /, %</span><span class="sxs-lookup"><span data-stu-id="d2cb7-110">+, -, \*, /, %</span></span>                                                     |
| [<span data-ttu-id="d2cb7-111">Оператор массива</span><span class="sxs-lookup"><span data-stu-id="d2cb7-111">Array Operator</span></span>](#array-operator)                                               | <span data-ttu-id="d2cb7-112">\[i\]</span><span class="sxs-lookup"><span data-stu-id="d2cb7-112">\[i\]</span></span>                                                              |
| [<span data-ttu-id="d2cb7-113">Операторы присваивания</span><span class="sxs-lookup"><span data-stu-id="d2cb7-113">Assignment Operators</span></span>](#assignment-operators)                                   | <span data-ttu-id="d2cb7-114">=, +=, -=, \*=, /=, %=</span><span class="sxs-lookup"><span data-stu-id="d2cb7-114">=, +=, -=, \*=, /=, %=</span></span>                                             |
| [<span data-ttu-id="d2cb7-115">Двоичные приведения</span><span class="sxs-lookup"><span data-stu-id="d2cb7-115">Binary Casts</span></span>](#binary-casts)                                                   | <span data-ttu-id="d2cb7-116">Правила c для логического типа float и int, C Rules или HLSL для bool</span><span class="sxs-lookup"><span data-stu-id="d2cb7-116">C rules for float and int, C rules or HLSL intrinsics for bool</span></span>     |
| [<span data-ttu-id="d2cb7-117">Битовые операторы</span><span class="sxs-lookup"><span data-stu-id="d2cb7-117">Bitwise Operators</span></span>](#bitwise-operators)                                         | <span data-ttu-id="d2cb7-118">~,  <<,  >>, &, \| , ^,  <<=,  >>=, &=, \| =, ^ =</span><span class="sxs-lookup"><span data-stu-id="d2cb7-118">~, <<, >>, &, \|, ^, <<=, >>=, &=, \|=, ^=</span></span> |
| [<span data-ttu-id="d2cb7-119">Логические математические операторы</span><span class="sxs-lookup"><span data-stu-id="d2cb7-119">Boolean Math Operators</span></span>](#boolean-math-operators)                               | <span data-ttu-id="d2cb7-120">& &, \| \| ,?:</span><span class="sxs-lookup"><span data-stu-id="d2cb7-120">& &, \|\|, ?:</span></span>                                                      |
| [<span data-ttu-id="d2cb7-121">Оператор приведения</span><span class="sxs-lookup"><span data-stu-id="d2cb7-121">Cast Operator</span></span>](#cast-operator)                                                 | <span data-ttu-id="d2cb7-122">Тип</span><span class="sxs-lookup"><span data-stu-id="d2cb7-122">(type)</span></span>                                                             |
| [<span data-ttu-id="d2cb7-123">Запятая, оператор</span><span class="sxs-lookup"><span data-stu-id="d2cb7-123">Comma Operator</span></span>](#comma-operator)                                               | <span data-ttu-id="d2cb7-124">,</span><span class="sxs-lookup"><span data-stu-id="d2cb7-124">,</span></span>                                                                  |
| [<span data-ttu-id="d2cb7-125">Операторы сравнения</span><span class="sxs-lookup"><span data-stu-id="d2cb7-125">Comparison Operators</span></span>](#comparison-operators)                                   | <span data-ttu-id="d2cb7-126"><, >, = =,! =, <=, >=</span><span class="sxs-lookup"><span data-stu-id="d2cb7-126"><, >, ==, !=, <=, >=</span></span>                                   |
| [<span data-ttu-id="d2cb7-127">Операторы префикса или постфикс</span><span class="sxs-lookup"><span data-stu-id="d2cb7-127">Prefix or Postfix Operators</span></span>](#prefix-or-postfix-operators)                     | <span data-ttu-id="d2cb7-128">++, --</span><span class="sxs-lookup"><span data-stu-id="d2cb7-128">++, --</span></span>                                                             |
| [<span data-ttu-id="d2cb7-129">Оператор Structure</span><span class="sxs-lookup"><span data-stu-id="d2cb7-129">Structure Operator</span></span>](#structure-operator)                                       | <span data-ttu-id="d2cb7-130">.</span><span class="sxs-lookup"><span data-stu-id="d2cb7-130">.</span></span>                                                                  |
| [<span data-ttu-id="d2cb7-131">Унарные операторы</span><span class="sxs-lookup"><span data-stu-id="d2cb7-131">Unary Operators</span></span>](#unary-operators)                                             | <span data-ttu-id="d2cb7-132">!, -, +</span><span class="sxs-lookup"><span data-stu-id="d2cb7-132">!, -, +</span></span>                                                            |



 

<span data-ttu-id="d2cb7-133">Многие из операторов относятся к каждому компоненту, что означает, что операция выполняется независимо для каждого компонента каждой переменной.</span><span class="sxs-lookup"><span data-stu-id="d2cb7-133">Many of the operators are per-component, which means that the operation is performed independently for each component of each variable.</span></span> <span data-ttu-id="d2cb7-134">Например, одна переменная компонента имеет одну операцию.</span><span class="sxs-lookup"><span data-stu-id="d2cb7-134">For example, a single component variable has one operation performed.</span></span> <span data-ttu-id="d2cb7-135">С другой стороны, в переменной с четырьмя компонентами выполняется четыре операции, по одной для каждого компонента.</span><span class="sxs-lookup"><span data-stu-id="d2cb7-135">On the other hand, a four-component variable has four operations performed, one for each component.</span></span>

<span data-ttu-id="d2cb7-136">Все операторы, которые делают что-то значение, например + и \* , работают на каждом компоненте.</span><span class="sxs-lookup"><span data-stu-id="d2cb7-136">All of the operators that do something to the value, such as + and \*, work per component.</span></span>

<span data-ttu-id="d2cb7-137">Операторы сравнения должны работать только с одним компонентом, если только не используется встроенная функция [**ALL**](dx-graphics-hlsl-all.md) или [**любая**](dx-graphics-hlsl-any.md) из них с несколькими компонентами.</span><span class="sxs-lookup"><span data-stu-id="d2cb7-137">The comparison operators require a single component to work unless you use the [**all**](dx-graphics-hlsl-all.md) or [**any**](dx-graphics-hlsl-any.md) intrinsic function with a multiple-component variable.</span></span> <span data-ttu-id="d2cb7-138">Следующая операция завершается ошибкой, так как оператор If требует один bool, но получает bool4:</span><span class="sxs-lookup"><span data-stu-id="d2cb7-138">The following operation fails because the if statement requires a single bool but receives a bool4:</span></span>


```
if (A4 < B4)
```



<span data-ttu-id="d2cb7-139">Следующие операции выполнены.</span><span class="sxs-lookup"><span data-stu-id="d2cb7-139">The following operations succeed:</span></span>


```
if ( any(A4 < B4) )
if ( all(A4 < B4) )
```



<span data-ttu-id="d2cb7-140">Бинарные операторы приведения [**асфлоат**](dx-graphics-hlsl-asfloat.md), [**ASIN**](dx-graphics-hlsl-asint.md)и т. д. для каждого компонента, за исключением [**асдаубле**](asdouble.md) , для которого задокументированы особые правила.</span><span class="sxs-lookup"><span data-stu-id="d2cb7-140">The binary cast operators [**asfloat**](dx-graphics-hlsl-asfloat.md), [**asint**](dx-graphics-hlsl-asint.md), and so on work per component except for [**asdouble**](asdouble.md) whose special rules are documented.</span></span>

<span data-ttu-id="d2cb7-141">Операторы выбора, такие как точка, запятая и скобки массива, не работают для каждого компонента.</span><span class="sxs-lookup"><span data-stu-id="d2cb7-141">Selection operators like period, comma, and array brackets do not work per component.</span></span>

<span data-ttu-id="d2cb7-142">Операторы CAST изменяют число компонентов.</span><span class="sxs-lookup"><span data-stu-id="d2cb7-142">Cast operators change the number of components.</span></span> <span data-ttu-id="d2cb7-143">Следующие операции приведения показывают их эквивалентность:</span><span class="sxs-lookup"><span data-stu-id="d2cb7-143">The following cast operations show their equivalence:</span></span>


```
(float) i4 ->   float(i4.x)
(float4)i ->   float4(i, i, i, i)
```



## <a name="additive-and-multiplicative-operators"></a><span data-ttu-id="d2cb7-144">Аддитивные и Мультипликативные операторы</span><span class="sxs-lookup"><span data-stu-id="d2cb7-144">Additive and Multiplicative Operators</span></span>

<span data-ttu-id="d2cb7-145">К операторам аддитивного и мультипликативные относятся: +,-, \* ,/,%</span><span class="sxs-lookup"><span data-stu-id="d2cb7-145">The additive and multiplicative operators are: +, -, \*, /, %</span></span>


```
int i1 = 1;
int i2 = 2;
int i3 = i1 + i2;  // i3 = 3
i3 = i1 * i2;        // i3 = 1 * 2 = 2
```




```
i3 = i1/i2;       // i3 = 1/3 = 0.333. Truncated to 0 because i3 is an integer.
i3 = i2/i1;       // i3 = 2/1 = 2
```




```
float f1 = 1.0;
float f2 = 2.0f;
float f3 = f1 - f2; // f3 = 1.0 - 2.0 = -1.0
f3 = f1 * f2;         // f3 = 1.0 * 2.0 = 2.0
```




```
f3 = f1/f2;        // f3 = 1.0/2.0 = 0.5
f3 = f2/f1;        // f3 = 2.0/1.0 = 2.0
```



<span data-ttu-id="d2cb7-146">Оператор модуля возвращает остаток от деления.</span><span class="sxs-lookup"><span data-stu-id="d2cb7-146">The modulus operator returns the remainder of a division.</span></span> <span data-ttu-id="d2cb7-147">Это дает разные результаты при использовании целых чисел и чисел с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="d2cb7-147">This produces different results when using integers and floating-point numbers.</span></span> <span data-ttu-id="d2cb7-148">Целочисленные остатки, которые являются дробными, будут обрезаны.</span><span class="sxs-lookup"><span data-stu-id="d2cb7-148">Integer remainders that are fractional will be truncated.</span></span>


```
int i1 = 1;
int i2 = 2;
i3 = i1 % i2;      // i3 = remainder of 1/2, which is 1
i3 = i2 % i1;      // i3 = remainder of 2/1, which is 0
i3 = 5 % 2;        // i3 = remainder of 5/2, which is 1
i3 = 9 % 2;        // i3 = remainder of 9/2, which is 1
```



<span data-ttu-id="d2cb7-149">Оператор модуля усекает оставшуюся часть при использовании целых чисел.</span><span class="sxs-lookup"><span data-stu-id="d2cb7-149">The modulus operator truncates a fractional remainder when using integers.</span></span>


```
f3 = f1 % f2;      // f3 = remainder of 1.0/2.0, which is 0.5
f3 = f2 % f1;      // f3 = remainder of 2.0/1.0, which is 0.0
```



<span data-ttu-id="d2cb7-150">Оператор% определен только в случаях, когда обе стороны либо положительные, либо обе стороны являются отрицательными.</span><span class="sxs-lookup"><span data-stu-id="d2cb7-150">The % operator is defined only in cases where either both sides are positive or both sides are negative.</span></span> <span data-ttu-id="d2cb7-151">В отличие от C, он также работает с типами данных с плавающей запятой, а также с целыми числами.</span><span class="sxs-lookup"><span data-stu-id="d2cb7-151">Unlike C, it also operates on floating-point data types, as well as integers.</span></span>

## <a name="array-operator"></a><span data-ttu-id="d2cb7-152">Оператор массива</span><span class="sxs-lookup"><span data-stu-id="d2cb7-152">Array Operator</span></span>

<span data-ttu-id="d2cb7-153">Оператор выбора члена массива " \[ i \] " выбирает один или несколько компонентов в массиве.</span><span class="sxs-lookup"><span data-stu-id="d2cb7-153">The array member selection operator "\[i\]" selects one or more components in an array.</span></span> <span data-ttu-id="d2cb7-154">Это набор квадратных скобок, содержащих Отсчитываемый от нуля индекс.</span><span class="sxs-lookup"><span data-stu-id="d2cb7-154">It is a set of square brackets that contain a zero-based index.</span></span>


```
int arrayOfInts[4] = { 0,1,2,3 };
arrayOfInts[0] = 2;
arrayOfInts[1] = arrayOfInts[0];
```



<span data-ttu-id="d2cb7-155">Оператор Array также может использоваться для доступа к вектору.</span><span class="sxs-lookup"><span data-stu-id="d2cb7-155">The array operator can also be used to access a vector.</span></span>


```
float4 4D_Vector = { 0.0f, 1.0f, 2.0f, 3.0f  };         
float 1DFloat = 4D_Vector[1];          // 1.0f
```



<span data-ttu-id="d2cb7-156">Добавив дополнительный индекс, оператор Array также может получить доступ к матрице.</span><span class="sxs-lookup"><span data-stu-id="d2cb7-156">By adding an additional index, the array operator can also access a matrix.</span></span>


```
float4x4 mat4x4 = {{0,0,0,0}, {1,1,1,1}, {2,2,2,2}, {3,3,3,3} };
mat4x4[0][1] = 1.1f;
float 1DFloat = mat4x4[0][1];      // 0.0f
```



<span data-ttu-id="d2cb7-157">Первый индекс — это Отсчитываемый от нуля индекс строки.</span><span class="sxs-lookup"><span data-stu-id="d2cb7-157">The first index is the zero-based row index.</span></span> <span data-ttu-id="d2cb7-158">Второй индекс — это Отсчитываемый от нуля индекс столбца.</span><span class="sxs-lookup"><span data-stu-id="d2cb7-158">The second index is the zero-based column index.</span></span>

## <a name="assignment-operators"></a><span data-ttu-id="d2cb7-159">Операторы присваивания</span><span class="sxs-lookup"><span data-stu-id="d2cb7-159">Assignment Operators</span></span>

<span data-ttu-id="d2cb7-160">Операторы присваивания: =, + =,-=, \* =,/=</span><span class="sxs-lookup"><span data-stu-id="d2cb7-160">The assignment operators are: =, +=, -=, \*=, /=</span></span>

<span data-ttu-id="d2cb7-161">Переменным могут быть присвоены литеральные значения:</span><span class="sxs-lookup"><span data-stu-id="d2cb7-161">Variables can be assigned literal values:</span></span>


```
int i = 1;            
float f2 = 3.1f; 
bool b = false;
string str = "string";
```



<span data-ttu-id="d2cb7-162">Переменным также можно назначить результат математической операции:</span><span class="sxs-lookup"><span data-stu-id="d2cb7-162">Variables can also be assigned the result of a mathematical operation:</span></span>


```
int i1 = 1;
i1 += 2;           // i1 = 1 + 2 = 3
```



<span data-ttu-id="d2cb7-163">Переменную можно использовать с любой стороны знака равенства:</span><span class="sxs-lookup"><span data-stu-id="d2cb7-163">A variable can be used on either side of the equals sign:</span></span>


```
float f3 = 0.5f;
f3 *= f3;          // f3 = 0.5 * 0.5 = 0.25
```



<span data-ttu-id="d2cb7-164">Деление переменных с плавающей запятой является ожидаемым, так как десятичные остатки не являются проблемой.</span><span class="sxs-lookup"><span data-stu-id="d2cb7-164">Division for floating-point variables is as expected because decimal remainders are not a problem.</span></span>


```
float f1 = 1.0;
f1 /= 3.0f;        // f1 = 1.0/3.0 = 0.333
```



<span data-ttu-id="d2cb7-165">Будьте внимательны, если используете целые числа, которые могут быть разделены, особенно если усечение влияет на результат.</span><span class="sxs-lookup"><span data-stu-id="d2cb7-165">Be careful if you are using integers that may get divided, especially when truncation affects the result.</span></span> <span data-ttu-id="d2cb7-166">Этот пример идентичен предыдущему примеру, за исключением типа данных.</span><span class="sxs-lookup"><span data-stu-id="d2cb7-166">This example is identical to the previous example, except for the data type.</span></span> <span data-ttu-id="d2cb7-167">Усечение приводит к совершенно другому результату.</span><span class="sxs-lookup"><span data-stu-id="d2cb7-167">The truncation causes a very different result.</span></span>


```
int i1 = 1;
i1 /= 3;           // i1 = 1/3 = 0.333, which gets truncated to 0
```



## <a name="binary-casts"></a><span data-ttu-id="d2cb7-168">Двоичные приведения</span><span class="sxs-lookup"><span data-stu-id="d2cb7-168">Binary Casts</span></span>

<span data-ttu-id="d2cb7-169">Операция приведения между int и float Преобразует числовое значение в соответствующие представления ниже правил C для усечения типа int.</span><span class="sxs-lookup"><span data-stu-id="d2cb7-169">Casting operation between int and float will convert the numeric value into the appropriate representations following C rules for truncating an int type.</span></span> <span data-ttu-id="d2cb7-170">Приведение значения с плавающей запятой к типу int и обратно в тип float приведет к преобразованию потери на основе точности целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="d2cb7-170">Casting a value from a float to an int and back to a float will result in a lossy conversion based on the precision of the target.</span></span>

<span data-ttu-id="d2cb7-171">Двоичные приведения также можно выполнять с помощью [**встроенных функций (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md), которые повторно преобразуют битовое представление числа в целевой тип данных.</span><span class="sxs-lookup"><span data-stu-id="d2cb7-171">Binary casts may also be performed using [**Intrinsic Functions (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md), which reinterpret the bit representation of a number into the target data type.</span></span>


```
asfloat() // Cast to float
asint()   // Cast to int 
asuint()  // Cast to uint
```



## <a name="bitwise-operators"></a><span data-ttu-id="d2cb7-172">Побитовые операторы</span><span class="sxs-lookup"><span data-stu-id="d2cb7-172">Bitwise Operators</span></span>

<span data-ttu-id="d2cb7-173">HLSL поддерживает следующие битовые операторы, имеющие тот же приоритет, что и C, в отношении других операторов.</span><span class="sxs-lookup"><span data-stu-id="d2cb7-173">HLSL supports the following bitwise operators, which follow the same precedence as C with regard to other operators.</span></span> <span data-ttu-id="d2cb7-174">В следующей таблице описаны операторы.</span><span class="sxs-lookup"><span data-stu-id="d2cb7-174">The following table describes the operators.</span></span>

> [!Note]  
> <span data-ttu-id="d2cb7-175">Побитовым операторам требуется [модель шейдера 4 \_ 0](dx-graphics-hlsl-sm4.md) с Direct3D 10 и более высоким оборудованием.</span><span class="sxs-lookup"><span data-stu-id="d2cb7-175">Bitwise operators require [Shader Model 4\_0](dx-graphics-hlsl-sm4.md) with Direct3D 10 and higher hardware.</span></span>

 



|           |                   |
|-----------|-------------------|
| <span data-ttu-id="d2cb7-176">Оператор</span><span class="sxs-lookup"><span data-stu-id="d2cb7-176">Operator</span></span>  | <span data-ttu-id="d2cb7-177">Функция</span><span class="sxs-lookup"><span data-stu-id="d2cb7-177">Function</span></span>          |
| ~         | <span data-ttu-id="d2cb7-178">Логическое не</span><span class="sxs-lookup"><span data-stu-id="d2cb7-178">Logical Not</span></span>       |
| <<  | <span data-ttu-id="d2cb7-179">Сдвиг влево</span><span class="sxs-lookup"><span data-stu-id="d2cb7-179">Left Shift</span></span>        |
| >>  | <span data-ttu-id="d2cb7-180">Сдвиг вправо</span><span class="sxs-lookup"><span data-stu-id="d2cb7-180">Right Shift</span></span>       |
| &         | <span data-ttu-id="d2cb7-181">Логическое и</span><span class="sxs-lookup"><span data-stu-id="d2cb7-181">Logical And</span></span>       |
| \|        | <span data-ttu-id="d2cb7-182">Логическое "или".</span><span class="sxs-lookup"><span data-stu-id="d2cb7-182">Logical Or</span></span>        |
| ^         | <span data-ttu-id="d2cb7-183">Логическое исключающее или</span><span class="sxs-lookup"><span data-stu-id="d2cb7-183">Logical Xor</span></span>       |
| <<= | <span data-ttu-id="d2cb7-184">Сдвиг влево равен</span><span class="sxs-lookup"><span data-stu-id="d2cb7-184">Left Shift Equal</span></span>  |
| >>= | <span data-ttu-id="d2cb7-185">Сдвиг вправо равно</span><span class="sxs-lookup"><span data-stu-id="d2cb7-185">Right Shift Equal</span></span> |
| &=        | <span data-ttu-id="d2cb7-186">И равно</span><span class="sxs-lookup"><span data-stu-id="d2cb7-186">And Equal</span></span>         |
| \|=       | <span data-ttu-id="d2cb7-187">Или равно</span><span class="sxs-lookup"><span data-stu-id="d2cb7-187">Or Equal</span></span>          |
| ^=        | <span data-ttu-id="d2cb7-188">XOR равно</span><span class="sxs-lookup"><span data-stu-id="d2cb7-188">Xor Equal</span></span>         |



 

<span data-ttu-id="d2cb7-189">Битовые операторы определяются только для типов данных int и uint.</span><span class="sxs-lookup"><span data-stu-id="d2cb7-189">Bitwise operators are defined to operate only on int and uint data types.</span></span> <span data-ttu-id="d2cb7-190">Попытка использовать побитовые операторы для типов данных float или struct приведет к ошибке.</span><span class="sxs-lookup"><span data-stu-id="d2cb7-190">Attempting to use bitwise operators on float, or struct data types will result in an error.</span></span>

## <a name="boolean-math-operators"></a><span data-ttu-id="d2cb7-191">Логические математические операторы</span><span class="sxs-lookup"><span data-stu-id="d2cb7-191">Boolean Math Operators</span></span>

<span data-ttu-id="d2cb7-192">Логические математические операторы:  &&, \| \| ,?:</span><span class="sxs-lookup"><span data-stu-id="d2cb7-192">The Boolean math operators are: &&, \|\|, ?:</span></span>


```
bool b1 = true;
bool b2 = false;
bool b3 = b1 && b2 // b3 = true AND false = false
b3 = b1 || b2                // b3 = true OR false = true
```



<span data-ttu-id="d2cb7-193">В отличие от сокращенного вычисления &&, \| \| и?: в C выражения HLSL никогда не являются коротким вычислением, так как они являются векторными операциями.</span><span class="sxs-lookup"><span data-stu-id="d2cb7-193">Unlike short-circuit evaluation of &&, \|\|, and ?: in C, HLSL expressions never short-circuit an evaluation because they are vector operations.</span></span> <span data-ttu-id="d2cb7-194">Все стороны выражения всегда оцениваются.</span><span class="sxs-lookup"><span data-stu-id="d2cb7-194">All sides of the expression are always evaluated.</span></span>

<span data-ttu-id="d2cb7-195">Логические операторы работают с каждым компонентом.</span><span class="sxs-lookup"><span data-stu-id="d2cb7-195">Boolean operators function on a per-component basis.</span></span> <span data-ttu-id="d2cb7-196">Это означает, что при сравнении двух векторов результат будет вектором, содержащим логический результат сравнения для каждого компонента.</span><span class="sxs-lookup"><span data-stu-id="d2cb7-196">This means that if you compare two vectors, the result is a vector containing the Boolean result of the comparison for each component.</span></span>

<span data-ttu-id="d2cb7-197">Для выражений, использующих логические операторы, размер и тип компонента каждой переменной становятся одинаковыми до выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="d2cb7-197">For expressions that use Boolean operators, the size and component type of each variable are promoted to be the same before the operation occurs.</span></span> <span data-ttu-id="d2cb7-198">Повышенный тип определяет разрешение, при котором выполняется операция, а также тип результата выражения.</span><span class="sxs-lookup"><span data-stu-id="d2cb7-198">The promoted type determines the resolution at which the operation takes place, as well as the result type of the expression.</span></span> <span data-ttu-id="d2cb7-199">Например, выражение с плавающей запятой + + + будет преобразовано в float3 + float3 для оценки, и его результат будет иметь тип float3.</span><span class="sxs-lookup"><span data-stu-id="d2cb7-199">For example an int3 + float expression would be promoted to float3 + float3 for evaluation, and its result would be of type float3.</span></span>

## <a name="cast-operator"></a><span data-ttu-id="d2cb7-200">Оператор приведения</span><span class="sxs-lookup"><span data-stu-id="d2cb7-200">Cast Operator</span></span>

<span data-ttu-id="d2cb7-201">Выражение с префиксом имени типа в круглых скобках является явным приведением типов.</span><span class="sxs-lookup"><span data-stu-id="d2cb7-201">An expression preceded by a type name in parenthesis is an explicit type cast.</span></span> <span data-ttu-id="d2cb7-202">Приведение типа преобразует исходное выражение в тип данных приведения.</span><span class="sxs-lookup"><span data-stu-id="d2cb7-202">A type cast converts the original expression to the data type of the cast.</span></span> <span data-ttu-id="d2cb7-203">В целом, простые типы данных можно привести к более сложным типам данных (с приведением повышения), но только некоторые сложные типы данных можно привести к простым типам данных (с помощью приведения понижения).</span><span class="sxs-lookup"><span data-stu-id="d2cb7-203">In general, the simple data types can be cast to the more complex data types (with a promotion cast), but only some complex data types can be cast into simple data types (with a demotion cast).</span></span>

<span data-ttu-id="d2cb7-204">Допустимо только приведение типа с правой стороны.</span><span class="sxs-lookup"><span data-stu-id="d2cb7-204">Only right hand side type casting is legal.</span></span> <span data-ttu-id="d2cb7-205">Например, такие выражения, как, `(int)myFloat = myInt;` являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="d2cb7-205">For example, expressions such as `(int)myFloat = myInt;` are illegal.</span></span> <span data-ttu-id="d2cb7-206">Используйте вместо этого `myFloat = (float)myInt;`.</span><span class="sxs-lookup"><span data-stu-id="d2cb7-206">Use `myFloat = (float)myInt;` instead.</span></span>

<span data-ttu-id="d2cb7-207">Компилятор также выполняет неявное приведение типов.</span><span class="sxs-lookup"><span data-stu-id="d2cb7-207">The compiler also performs implicit type cast.</span></span> <span data-ttu-id="d2cb7-208">Например, следующие два выражения эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="d2cb7-208">For example, the following two expressions are equivalent:</span></span>


```
int2 b = int2(1,2) + 2;
int2 b = int2(1,2) + int2(2,2);
```



## <a name="comma-operator"></a><span data-ttu-id="d2cb7-209">Запятая, оператор</span><span class="sxs-lookup"><span data-stu-id="d2cb7-209">Comma Operator</span></span>

<span data-ttu-id="d2cb7-210">Оператор запятой (,) разделяет одно или несколько выражений, которые должны вычисляться по порядку.</span><span class="sxs-lookup"><span data-stu-id="d2cb7-210">The comma operator (,) separates one or more expressions that are to be evaluated in order.</span></span> <span data-ttu-id="d2cb7-211">Значение последнего выражения в последовательности используется в качестве значения последовательности.</span><span class="sxs-lookup"><span data-stu-id="d2cb7-211">The value of the last expression in the sequence is used as the value of the sequence.</span></span>

<span data-ttu-id="d2cb7-212">В этом случае стоит обратить внимание на.</span><span class="sxs-lookup"><span data-stu-id="d2cb7-212">Here is one case worth calling attention to.</span></span> <span data-ttu-id="d2cb7-213">Если тип конструктора случайно не находится справа от знака равенства, в правой части теперь содержится четыре выражения, разделенные тремя запятыми.</span><span class="sxs-lookup"><span data-stu-id="d2cb7-213">If the constructor type is accidentally left off the right side of the equals sign, the right side now contains four expressions, separated by three commas.</span></span>


```
// Instead of using a constructor
float4 x = float4(0,0,0,1); 

// The type on the right side is accidentally left off
float4 x = (0,0,0,1); 
```



<span data-ttu-id="d2cb7-214">Оператор "запятая" вычисляет выражение слева направо.</span><span class="sxs-lookup"><span data-stu-id="d2cb7-214">The comma operator evaluates an expression from left to right.</span></span> <span data-ttu-id="d2cb7-215">Это сокращает правую часть до:</span><span class="sxs-lookup"><span data-stu-id="d2cb7-215">This reduces the right hand side to:</span></span>


```
float4 x = 1; 
```



<span data-ttu-id="d2cb7-216">В этом случае в HLSL используется скалярное продвижение, поэтому результат будет таким же, как если бы он был написан следующим образом:</span><span class="sxs-lookup"><span data-stu-id="d2cb7-216">HLSL uses scalar promotion in this case, so the result is as if this were written as follows:</span></span>


```
float4 x = float4(1,1,1,1);
```



<span data-ttu-id="d2cb7-217">В этом случае выход из типа float4 с правой стороны, вероятно, является ошибкой, которую компилятору не удается обнаружить, поскольку это допустимая инструкция.</span><span class="sxs-lookup"><span data-stu-id="d2cb7-217">In this instance, leaving off the float4 type from the right side is probably a mistake that the compiler is unable to detect because this is a valid statement.</span></span>

## <a name="comparison-operators"></a><span data-ttu-id="d2cb7-218">Операторы сравнения</span><span class="sxs-lookup"><span data-stu-id="d2cb7-218">Comparison Operators</span></span>

<span data-ttu-id="d2cb7-219">Операторы сравнения: <, >, = =,! =, <=, >=.</span><span class="sxs-lookup"><span data-stu-id="d2cb7-219">The comparison operators are: <, >, ==, !=, <=, >=.</span></span>

<span data-ttu-id="d2cb7-220">Сравните значения, которые больше (или меньше) любого скалярного значения:</span><span class="sxs-lookup"><span data-stu-id="d2cb7-220">Compare values that are greater than (or less than) any scalar value:</span></span>


```
if( dot(lightDirection, normalVector) > 0 )
   // Do something; the face is lit
```




```
if( dot(lightDirection, normalVector) < 0 )
   // Do nothing; the face is backwards
```



<span data-ttu-id="d2cb7-221">Или Сравните значения, равные (или не равные) любому скалярному значению:</span><span class="sxs-lookup"><span data-stu-id="d2cb7-221">Or, compare values equal to (or not equal to) any scalar value:</span></span>


```
if(color.a == 0)
   // Skip processing because the face is invisible

if(color.a != 0)
   // Blend two colors together using the alpha value
```



<span data-ttu-id="d2cb7-222">Или объединить и сравнить значения, которые больше или равны (или меньше или равны) любому скалярному значению:</span><span class="sxs-lookup"><span data-stu-id="d2cb7-222">Or combine both and compare values that are greater than or equal to (or less than or equal to) any scalar value:</span></span>


```
if( position.z >= oldPosition.z )
   // Skip the new face because it is behind the existing face
```




```
if( currentValue <= someInitialCondition )
   // Reset the current value to its initial condition
```



<span data-ttu-id="d2cb7-223">Каждое из этих сравнений можно выполнить с любым скалярным типом данных.</span><span class="sxs-lookup"><span data-stu-id="d2cb7-223">Each of these comparisons can be done with any scalar data type.</span></span>

<span data-ttu-id="d2cb7-224">Чтобы использовать операторы сравнения с типами Vector и Matrix, используйте встроенную функцию [**ALL**](dx-graphics-hlsl-all.md) или [**ANY**](dx-graphics-hlsl-any.md) .</span><span class="sxs-lookup"><span data-stu-id="d2cb7-224">To use comparison operators with vector and matrix types, use the [**all**](dx-graphics-hlsl-all.md) or [**any**](dx-graphics-hlsl-any.md) intrinsic function.</span></span>

<span data-ttu-id="d2cb7-225">Эта операция завершается ошибкой, так как оператор If требует один bool, но получает bool4:</span><span class="sxs-lookup"><span data-stu-id="d2cb7-225">This operation fails because the if statement requires a single bool but receives a bool4:</span></span>


```
if (A4 < B4)
```



<span data-ttu-id="d2cb7-226">Эти операции выполнены.</span><span class="sxs-lookup"><span data-stu-id="d2cb7-226">These operations succeed:</span></span>


```
if ( any(A4 < B4) )
if ( all(A4 < B4) )
```



## <a name="prefix-or-postfix-operators"></a><span data-ttu-id="d2cb7-227">Операторы префикса или постфикс</span><span class="sxs-lookup"><span data-stu-id="d2cb7-227">Prefix or Postfix Operators</span></span>

<span data-ttu-id="d2cb7-228">Префиксные и постфиксные операторы: + +,--.</span><span class="sxs-lookup"><span data-stu-id="d2cb7-228">The prefix and postfix operators are: ++, --.</span></span> <span data-ttu-id="d2cb7-229">Операторы префикса изменяют содержимое переменной перед вычислением выражения.</span><span class="sxs-lookup"><span data-stu-id="d2cb7-229">Prefix operators change the contents of the variable before the expression is evaluated.</span></span> <span data-ttu-id="d2cb7-230">Постфиксные операторы изменяют содержимое переменной после вычисления выражения.</span><span class="sxs-lookup"><span data-stu-id="d2cb7-230">Postfix operators change the contents of the variable after the expression is evaluated.</span></span>

<span data-ttu-id="d2cb7-231">В этом случае цикл использует содержимое i для наблюдения за числом циклов.</span><span class="sxs-lookup"><span data-stu-id="d2cb7-231">In this case, a loop uses the contents of i to keep track of the loop count.</span></span>


```
float4 arrayOfFloats[4] = { 1.0f, 2.0f, 3.0f, 4.4f };

for (int i = 0; i<4; )
{
    arrayOfFloats[i++] *= 2; 
}
```



<span data-ttu-id="d2cb7-232">Так как используется постфиксный оператор инкремента (+ +), Аррайоффлоатс \[ i \] умножается на 2 до увеличения.</span><span class="sxs-lookup"><span data-stu-id="d2cb7-232">Because the postfix increment operator (++) is used, arrayOfFloats\[i\] is multiplied by 2 before i is incremented.</span></span> <span data-ttu-id="d2cb7-233">Это может быть немного Переупорядочено для использования оператора префикса инкремента.</span><span class="sxs-lookup"><span data-stu-id="d2cb7-233">This could be slightly rearranged to use the prefix increment operator.</span></span> <span data-ttu-id="d2cb7-234">Это труднее читать, хотя оба примера эквивалентны.</span><span class="sxs-lookup"><span data-stu-id="d2cb7-234">This one is harder to read, although both examples are equivalent.</span></span>


```
float4 arrayOfFloats[4] = { 1.0f, 2.0f, 3.0f, 4.4f };

for (int i = 0; i<4; )
{
    arrayOfFloats[++i - 1] *= 2; 
}
```



<span data-ttu-id="d2cb7-235">Поскольку используется префиксный оператор (+ +), Аррайоффлоатс \[ i + 1-1 \] умножается на 2 после увеличения.</span><span class="sxs-lookup"><span data-stu-id="d2cb7-235">Because the prefix operator (++) is used, arrayOfFloats\[i+1 - 1\] is multiplied by 2 after i is incremented.</span></span>

<span data-ttu-id="d2cb7-236">Операторы декремента и постфикса префикса (--) применяются в той же последовательности, что и оператор инкремента.</span><span class="sxs-lookup"><span data-stu-id="d2cb7-236">The prefix decrement and postfix decrement operator (--) are applied in the same sequence as the increment operator.</span></span> <span data-ttu-id="d2cb7-237">Разница заключается в том, что уменьшение вычитает 1 вместо сложения 1.</span><span class="sxs-lookup"><span data-stu-id="d2cb7-237">The difference is that decrement subtracts 1 instead of adding 1.</span></span>

## <a name="structure-operator"></a><span data-ttu-id="d2cb7-238">Оператор Structure</span><span class="sxs-lookup"><span data-stu-id="d2cb7-238">Structure Operator</span></span>

<span data-ttu-id="d2cb7-239">Оператор выбора члена структуры (.) — это точка.</span><span class="sxs-lookup"><span data-stu-id="d2cb7-239">The structure member selection operator (.) is a period.</span></span> <span data-ttu-id="d2cb7-240">С учетом этой структуры:</span><span class="sxs-lookup"><span data-stu-id="d2cb7-240">Given this structure:</span></span>


```
struct position
{
float4 x;
float4 y;
float4 z;
};
```



<span data-ttu-id="d2cb7-241">Его можно прочитать следующим образом:</span><span class="sxs-lookup"><span data-stu-id="d2cb7-241">It can be read like this:</span></span>


```
struct position pos = { 1,2,3 };

float 1D_Float = pos.x
1D_Float = pos.y
```



<span data-ttu-id="d2cb7-242">Каждый элемент может быть считан или записан с помощью оператора Structure:</span><span class="sxs-lookup"><span data-stu-id="d2cb7-242">Each member can be read or written with the structure operator:</span></span>


```
struct position pos = { 1,2,3 };
pos.x = 2.0f;
pos.z = 1.0f;       // z = 1.0f
pos.z = pos.x      // z = 2.0f
```



## <a name="unary-operators"></a><span data-ttu-id="d2cb7-243">Унарные операторы</span><span class="sxs-lookup"><span data-stu-id="d2cb7-243">Unary Operators</span></span>

<span data-ttu-id="d2cb7-244">Унарные операторы:!,-, +</span><span class="sxs-lookup"><span data-stu-id="d2cb7-244">The unary operators are: !, -, +</span></span>

<span data-ttu-id="d2cb7-245">Унарные операторы работают с одним операндом.</span><span class="sxs-lookup"><span data-stu-id="d2cb7-245">Unary operators operate on a single operand.</span></span>


```
bool b = false;
bool b2 = !b;      // b2 = true
int i = 2;
int i2 = -i;       // i2 = -2
int j = +i2;       // j = +2
```



## <a name="operator-precedence"></a><span data-ttu-id="d2cb7-246">Приоритет операторов</span><span class="sxs-lookup"><span data-stu-id="d2cb7-246">Operator Precedence</span></span>

<span data-ttu-id="d2cb7-247">Если выражение содержит более одного оператора, порядок вычисления определяется приоритетом операторов.</span><span class="sxs-lookup"><span data-stu-id="d2cb7-247">When an expression contains more than one operator, operator precedence determines the order of evaluation.</span></span> <span data-ttu-id="d2cb7-248">Приоритет операторов для HLSL соответствует тому же приоритету, что и в языке C.</span><span class="sxs-lookup"><span data-stu-id="d2cb7-248">Operator precedence for HLSL follows the same precedence as C.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2cb7-249">Примечания</span><span class="sxs-lookup"><span data-stu-id="d2cb7-249">Remarks</span></span>

<span data-ttu-id="d2cb7-250">Фигурные скобки ( {,} ) начинаются и заканчиваются блоком операторов.</span><span class="sxs-lookup"><span data-stu-id="d2cb7-250">Curly braces ({,}) start and end a statement block.</span></span> <span data-ttu-id="d2cb7-251">Если блок операторов использует один оператор, фигурные скобки являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="d2cb7-251">When a statement block uses a single statement, the curly braces are optional.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d2cb7-252">См. также</span><span class="sxs-lookup"><span data-stu-id="d2cb7-252">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2cb7-253">Инструкции (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d2cb7-253">Statements (DirectX HLSL)</span></span>](dx-graphics-hlsl-statements.md)
</dt> </dl>

 

 




