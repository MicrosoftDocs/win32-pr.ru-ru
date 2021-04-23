---
description: Столбцы, хранящиеся в индексе содержимого, могут иметь несколько значений, и эти Многозначные столбцы можно сравнивать с помощью предиката сравнения МАССИВов.
ms.assetid: bc3de1bd-b833-459d-81a3-c6b08314e26f
title: Сравнения с несколькими значениями (МАССИВы)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77710ecdddcf289c9a5c64d0c5f57ca449311097
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808932"
---
# <a name="multi-valued-array-comparisons"></a><span data-ttu-id="8fdd0-103">Сравнения с несколькими значениями (МАССИВы)</span><span class="sxs-lookup"><span data-stu-id="8fdd0-103">Multi-Valued (ARRAY) Comparisons</span></span>

<span data-ttu-id="8fdd0-104">Столбцы, хранящиеся в индексе содержимого, могут иметь несколько значений, и эти Многозначные столбцы можно сравнивать с помощью предиката сравнения МАССИВов.</span><span class="sxs-lookup"><span data-stu-id="8fdd0-104">Columns stored in the content index can have multiple values, and those multivalued columns can be compared by using the ARRAY comparison predicate.</span></span>

<span data-ttu-id="8fdd0-105">Предикат сравнения МАССИВов имеет следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="8fdd0-105">The ARRAY comparison predicate has the following syntax:</span></span>


```
...WHERE <column> <comp_op> [<quantifier>] <comparison_list>
                
...WHERE <column> <comp_op> <value>
```



<span data-ttu-id="8fdd0-106">Если ссылка на столбец не является многозначным столбцом, возвращается ошибка.</span><span class="sxs-lookup"><span data-stu-id="8fdd0-106">An error is returned if the column reference is not a multivalued column.</span></span> <span data-ttu-id="8fdd0-107">Тип данных столбца должен быть совместим с элементами списка сравнения.</span><span class="sxs-lookup"><span data-stu-id="8fdd0-107">The column data type must be compatible with the elements of the comparison list.</span></span> <span data-ttu-id="8fdd0-108">При необходимости ссылка на столбец может быть [приведена](-search-sql-castingdatacolumntype.md) к другому типу данных.</span><span class="sxs-lookup"><span data-stu-id="8fdd0-108">If necessary, the column reference can be [cast](-search-sql-castingdatacolumntype.md) as another data type.</span></span>

<span data-ttu-id="8fdd0-109">Оператор сравнения (Comp \_ op) может быть любым из обычных операторов сравнения.</span><span class="sxs-lookup"><span data-stu-id="8fdd0-109">The comparison operator (comp\_op) can be any of the normal comparison operators.</span></span> <span data-ttu-id="8fdd0-110">В многозначном сравнении операторы сравнения имеют немного разные значения в зависимости от того, используется ли квантификатор.</span><span class="sxs-lookup"><span data-stu-id="8fdd0-110">In a multivalued comparison, the comparison operators have slightly different meanings depending on whether a quantifier is used.</span></span> <span data-ttu-id="8fdd0-111">Кванторы указывают, следует ли выполнять сравнение для всех или некоторых значений в списке сравнения.</span><span class="sxs-lookup"><span data-stu-id="8fdd0-111">Quantifiers identify whether a comparison should be made against all or some of the values in the comparison list.</span></span> <span data-ttu-id="8fdd0-112">Функции операторов сравнения задаются в таблицах, описывающих каждый квантификатор (все и некоторые) далее в этом документе.</span><span class="sxs-lookup"><span data-stu-id="8fdd0-112">The functions of the comparison operators are given in the tables describing each quantifier (ALL and SOME) later in this document.</span></span>

<span data-ttu-id="8fdd0-113">Значение после оператора указывает одно литеральное значение, которое сравнивается со всеми элементами многозначного столбца.</span><span class="sxs-lookup"><span data-stu-id="8fdd0-113">The value after the operator specifies a single literal value that is compared against all elements of the multivalued column.</span></span> <span data-ttu-id="8fdd0-114">Если какой-либо элемент соответствует значению, предикат имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="8fdd0-114">If any element matches the value, the predicate is true.</span></span>

<span data-ttu-id="8fdd0-115">В списке сравнения указывается массив литеральных значений, сравниваемых с многозначным столбцом.</span><span class="sxs-lookup"><span data-stu-id="8fdd0-115">The comparison list specifies an array of literal values that are compared against the multivalued column.</span></span> <span data-ttu-id="8fdd0-116">Синтаксис для списка сравнения выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="8fdd0-116">The syntax for the comparison list follows:</span></span>


```
ARRAY '['<literal> [,<literal>]']'
```



> [!IMPORTANT]
> <span data-ttu-id="8fdd0-117">Обратите внимание на синтаксис списка сравнения.</span><span class="sxs-lookup"><span data-stu-id="8fdd0-117">Be aware of the comparison list syntax.</span></span> <span data-ttu-id="8fdd0-118">Группа литералов, составляющих список сравнения, должна быть заключена в квадратные скобки.</span><span class="sxs-lookup"><span data-stu-id="8fdd0-118">The group of literals that make up the comparison list must be surrounded by square brackets.</span></span> <span data-ttu-id="8fdd0-119">Не выключайте отдельные элементы списка сравнения квадратными скобками.</span><span class="sxs-lookup"><span data-stu-id="8fdd0-119">Do not surround individual elements of the comparison list by square brackets.</span></span> <span data-ttu-id="8fdd0-120">Следовательно, массив \[ 1 \] и массив \[ 1, 2, 3 \] являются ДОПУСТИМЫми, но массивы \[ 1 \[ , 2 \] \[ и 3 \] \] не имеют.</span><span class="sxs-lookup"><span data-stu-id="8fdd0-120">Therefore, ARRAY \[1\] and ARRAY \[1,2,3\] are valid, but ARRAY \[1\[,2\]\[,3\]\] is not.</span></span>

 

<span data-ttu-id="8fdd0-121">Метод, используемый для определения того, возвращает ли многозначное сравнение значение true или false, определяется необязательным квантор.</span><span class="sxs-lookup"><span data-stu-id="8fdd0-121">The method used to determine whether the multivalued comparison returns true or false is specified by the optional quantifier.</span></span> <span data-ttu-id="8fdd0-122">В следующих разделах описываются все кванторы и принципы работы каждого оператора сравнения при использовании квантификатора.</span><span class="sxs-lookup"><span data-stu-id="8fdd0-122">The following sections describe each quantifier, and how each comparison operator works when the quantifier is used.</span></span>

## <a name="absent-quantifier"></a><span data-ttu-id="8fdd0-123">Отсутствует квантификатор</span><span class="sxs-lookup"><span data-stu-id="8fdd0-123">Absent Quantifier</span></span>

<span data-ttu-id="8fdd0-124">Если квантификатор не указан, каждый элемент в левой части сравнения сравнивается с элементом в той же позицией справа.</span><span class="sxs-lookup"><span data-stu-id="8fdd0-124">If no quantifier is specified, each element on the left side of the comparison is compared to the element in the same position on the right side.</span></span> <span data-ttu-id="8fdd0-125">Сравнение начинается с первого элемента в массивах и проходит через последний элемент.</span><span class="sxs-lookup"><span data-stu-id="8fdd0-125">The comparison begins with the first element in the arrays, and progresses through the last element.</span></span> <span data-ttu-id="8fdd0-126">Если все элементы в левой части эквивалентны соответствующим элементам в правой части, то для определения большего массива используется число элементов массива.</span><span class="sxs-lookup"><span data-stu-id="8fdd0-126">If all the elements on the left side are equivalent to the corresponding elements on the right side, the number of array elements is used to determine which array is greater.</span></span>

<span data-ttu-id="8fdd0-127">В следующей таблице показаны операции операторов сравнения, если не указан квантификатор, и приводится краткое описание каждого из них.</span><span class="sxs-lookup"><span data-stu-id="8fdd0-127">The following table shows the operation of the comparison operators when no quantifier is specified and provides a brief description of each.</span></span>



| <span data-ttu-id="8fdd0-128">Оператор</span><span class="sxs-lookup"><span data-stu-id="8fdd0-128">Operator</span></span>       | <span data-ttu-id="8fdd0-129">Описание</span><span class="sxs-lookup"><span data-stu-id="8fdd0-129">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| =              | <span data-ttu-id="8fdd0-130">"Equal to" возвращает значение true, если каждый левый элемент имеет то же значение, что и соответствующий правый элемент, и оба массива имеют одинаковое число элементов.</span><span class="sxs-lookup"><span data-stu-id="8fdd0-130">'Equal to' returns true when each left-side element has the same value as the corresponding right-side element, and both arrays have the same number of elements.</span></span>                                                                                                                                                                                                                     |
| <span data-ttu-id="8fdd0-131">! = или <></span><span class="sxs-lookup"><span data-stu-id="8fdd0-131">!= or <></span></span> | <span data-ttu-id="8fdd0-132">"Не равно" возвращает значение true, если один или несколько элементов левой части имеют значения, отличающиеся от соответствующих правых элементов, или если массивы слева и справа не имеют одинакового количества элементов.</span><span class="sxs-lookup"><span data-stu-id="8fdd0-132">'Not equal to' returns true when one or more left-side elements have values that differ from the corresponding right-side elements, or when the left-side and right-side arrays do not have the same number of elements.</span></span>                                                                                                                                                              |
| >           | <span data-ttu-id="8fdd0-133">"Больше" возвращает значение true, если значение каждого левого элемента больше значения соответствующего правого элемента.</span><span class="sxs-lookup"><span data-stu-id="8fdd0-133">'Greater than' returns true when the value of each left-side element is greater than the value of the corresponding right-side element.</span></span> <span data-ttu-id="8fdd0-134">Если все значения элементов на левой стороне точно соответствуют соответствующим правым элементам, а массив слева содержит больше элементов, чем правый массив, "больше чем" возвращает значение true.</span><span class="sxs-lookup"><span data-stu-id="8fdd0-134">If all the left-side element values exactly match the corresponding right-side elements and the left-side array has more elements than the right-side array, 'greater than' returns true.</span></span>                                                     |
| >=          | <span data-ttu-id="8fdd0-135">"Больше или равно" возвращает значение true, если значение каждого левого элемента больше или равно значению соответствующего правого элемента.</span><span class="sxs-lookup"><span data-stu-id="8fdd0-135">'Greater than or equal to' returns true when the value of every left-side element is greater than or equal to the value of the corresponding right-side element.</span></span> <span data-ttu-id="8fdd0-136">Если все значения элементов на левой стороне равны или больше соответствующих правых элементов, а массив слева содержит те же элементы, что и правый массив, функция "больше" возвращает значение true.</span><span class="sxs-lookup"><span data-stu-id="8fdd0-136">If all the left-side element values are equal to or greater than the corresponding right-side elements and the left-side array has the same or more elements than the right-side array, 'greater than' returns true.</span></span> |
| <           | <span data-ttu-id="8fdd0-137">"Меньше" возвращает значение true, если значение каждого левого элемента меньше значения соответствующего правого элемента.</span><span class="sxs-lookup"><span data-stu-id="8fdd0-137">'Less than' returns true when the value of each left-side element is less than the value of the corresponding right-side element.</span></span> <span data-ttu-id="8fdd0-138">"Меньше" также возвращает значение true, если у левой стороны меньше элементов, чем у правой стороны.</span><span class="sxs-lookup"><span data-stu-id="8fdd0-138">'Less than' also returns true when the left-side side has fewer elements than the right-side side.</span></span>                                                                                                                                                  |
| <=          | <span data-ttu-id="8fdd0-139">"Меньше или равно" возвращает значение true, если значение каждого левого элемента меньше или равно значению соответствующего правого элемента.</span><span class="sxs-lookup"><span data-stu-id="8fdd0-139">'Less than or equal to' returns true when the value of every left-side element is less than or equal to the value of the corresponding right-side element.</span></span> <span data-ttu-id="8fdd0-140">Если все значения элементов на левой стороне равны или меньше соответствующих правых элементов, а массив слева имеет то же или меньше элементов, что и правый массив, "больше чем" возвращает значение true.</span><span class="sxs-lookup"><span data-stu-id="8fdd0-140">If all the left-side element values are equal to or less than the corresponding right-side elements and the left-side array has the same or fewer elements than the right-side array, 'greater than' returns true.</span></span>         |



 

## <a name="all-quantifier"></a><span data-ttu-id="8fdd0-141">ВСЕ кванторы</span><span class="sxs-lookup"><span data-stu-id="8fdd0-141">ALL Quantifier</span></span>

<span data-ttu-id="8fdd0-142">Квантификатор ALL указывает, что каждый элемент в левой части сравнивается с каждым элементом в правой части.</span><span class="sxs-lookup"><span data-stu-id="8fdd0-142">The ALL quantifier specifies that each element in the left side is compared against every element on the right side.</span></span> <span data-ttu-id="8fdd0-143">Чтобы вернуть значение true, при сравнении с каждым элементом в правой части сравнение должно иметь значение true для каждого элемента в левой части.</span><span class="sxs-lookup"><span data-stu-id="8fdd0-143">To return true, the comparison must be true for each element on the left side when compared to every element on the right side.</span></span> <span data-ttu-id="8fdd0-144">Число элементов в левой и правой сторонах массива не влияет на результат.</span><span class="sxs-lookup"><span data-stu-id="8fdd0-144">The number of elements in the left and right array sides has no effect on the result.</span></span>

<span data-ttu-id="8fdd0-145">В следующей таблице показано, как каждый оператор сравнения работает с квантификатором ALL.</span><span class="sxs-lookup"><span data-stu-id="8fdd0-145">The following table shows how each comparison operator functions with the ALL quantifier.</span></span>



| <span data-ttu-id="8fdd0-146">Оператор</span><span class="sxs-lookup"><span data-stu-id="8fdd0-146">Operator</span></span>       | <span data-ttu-id="8fdd0-147">Описание</span><span class="sxs-lookup"><span data-stu-id="8fdd0-147">Description</span></span>                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------|
| =              | <span data-ttu-id="8fdd0-148">"Equal to" возвращает значение true, если каждое значение элемента слева совпадает с каждым значением элемента, расположенного справа.</span><span class="sxs-lookup"><span data-stu-id="8fdd0-148">'Equal to' returns true when each left-side element value is the same as every right-side element value.</span></span>                              |
| <span data-ttu-id="8fdd0-149">! = или <></span><span class="sxs-lookup"><span data-stu-id="8fdd0-149">!= or <></span></span> | <span data-ttu-id="8fdd0-150">"Не равно" возвращает значение true, если хотя бы одно из значений элементов на левой стороне отличается от любого из значений элементов на стороне справа.</span><span class="sxs-lookup"><span data-stu-id="8fdd0-150">'Not equal to' returns true when at least one of the left-side element values is different from any of the right-side element values.</span></span> |
| >           | <span data-ttu-id="8fdd0-151">"Больше" возвращает значение true, если каждое значение элемента в левой части больше, чем каждое значение элемента справа.</span><span class="sxs-lookup"><span data-stu-id="8fdd0-151">'Greater than' returns true when each left-side element value is greater than every right-side element value.</span></span>                         |
| >=          | <span data-ttu-id="8fdd0-152">"Больше или равно" возвращает значение true, если каждое значение элемента в левой части больше или равно значению каждого правого элемента.</span><span class="sxs-lookup"><span data-stu-id="8fdd0-152">'Greater than or equal to' returns true when each left-side element value is greater than or equal to every right-side element value.</span></span> |
| <           | <span data-ttu-id="8fdd0-153">"Меньше" возвращает значение true, если каждое значение элемента в левой части меньше, чем каждое значение элемента справа.</span><span class="sxs-lookup"><span data-stu-id="8fdd0-153">'Less than' returns true when each left-side element value is less than every right-side element value.</span></span>                               |
| <=          | <span data-ttu-id="8fdd0-154">"Меньше или равно" возвращает значение true, если каждое значение элемента слева меньше или равно значению каждого из значений элементов на стороне справа.</span><span class="sxs-lookup"><span data-stu-id="8fdd0-154">'Less than or equal to' returns true when each left-side element value is less than or equal to every right-side element value.</span></span>       |



 

## <a name="some-or-any-quantifier"></a><span data-ttu-id="8fdd0-155">КАКОЙ-либо квантор (или любой)</span><span class="sxs-lookup"><span data-stu-id="8fdd0-155">SOME (or ANY) Quantifier</span></span>

<span data-ttu-id="8fdd0-156">Некоторые кванторы и кванторы могут использоваться взаимозаменяемыми.</span><span class="sxs-lookup"><span data-stu-id="8fdd0-156">The SOME quantifier and the ANY quantifier can be used interchangeably.</span></span> <span data-ttu-id="8fdd0-157">Как и квантификатор «все», квантор определяет, что каждый элемент в левой части сравнивается с каждым элементом в правой части.</span><span class="sxs-lookup"><span data-stu-id="8fdd0-157">Like the ALL quantifier, the SOME quantifier specifies that each element in the left side is compared against every element on the right side.</span></span> <span data-ttu-id="8fdd0-158">Для возврата значения true сравнение должно выполняться по крайней мере для одного из элементов в левой части по сравнению с любым элементом в правой части.</span><span class="sxs-lookup"><span data-stu-id="8fdd0-158">To return true, the comparison must be true for at least one of the elements on the left side when compared to any element on the right side.</span></span> <span data-ttu-id="8fdd0-159">Число элементов в левом и правом массивах не влияет на результат.</span><span class="sxs-lookup"><span data-stu-id="8fdd0-159">The number of elements on the left and right side arrays has no effect on the result.</span></span>

<span data-ttu-id="8fdd0-160">В следующей таблице показано, как каждый оператор сравнения работает с НЕКОТОРЫМ квантификатор.</span><span class="sxs-lookup"><span data-stu-id="8fdd0-160">The following table shows how each comparison operator functions with the SOME quantifier.</span></span>



| <span data-ttu-id="8fdd0-161">Оператор</span><span class="sxs-lookup"><span data-stu-id="8fdd0-161">Operator</span></span>       | <span data-ttu-id="8fdd0-162">Описание</span><span class="sxs-lookup"><span data-stu-id="8fdd0-162">Description</span></span>                                                                                                                                                     |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| =              | <span data-ttu-id="8fdd0-163">"Equal to" возвращает значение true, если хотя бы одно из значений элементов на левой стороне совпадает с любым из значений элементов на стороне справа.</span><span class="sxs-lookup"><span data-stu-id="8fdd0-163">'Equal to' returns true when at least one of the left-side element values is the same as any of the right-side element values.</span></span>                                  |
| <span data-ttu-id="8fdd0-164">! = или <></span><span class="sxs-lookup"><span data-stu-id="8fdd0-164">!= or <></span></span> | <span data-ttu-id="8fdd0-165">"Не равно" возвращает значение true, если ни одно из значений элементов левого края не совпадает с любым из значений элементов на стороне справа.</span><span class="sxs-lookup"><span data-stu-id="8fdd0-165">'Not equal to' returns true when none of the left-side element values is the same as any of the right-side element values.</span></span>                                      |
| >           | <span data-ttu-id="8fdd0-166">"Больше чем" возвращает значение true, если хотя бы одно из значений элементов на левой стороне больше любого из значений элементов на стороне справа.</span><span class="sxs-lookup"><span data-stu-id="8fdd0-166">'Greater than' returns true when at least one of the left-side element values is greater than any one of the right-side element values.</span></span>                         |
| >=          | <span data-ttu-id="8fdd0-167">"Больше или равно" возвращает значение true, если хотя бы одно из значений элементов на левой стороне больше или равно любому из значений элементов на стороне справа.</span><span class="sxs-lookup"><span data-stu-id="8fdd0-167">'Greater than or equal to' returns true when at least one of the left-side element values is greater than or equal to any one of the right-side element values.</span></span> |
| <           | <span data-ttu-id="8fdd0-168">"Меньше" возвращает значение true, если по крайней мере одно из значений элементов на левой стороне меньше любого из значений элементов на стороне справа.</span><span class="sxs-lookup"><span data-stu-id="8fdd0-168">'Less than' returns true when at least one of the left-side element values is less than any one of the right-side element values.</span></span>                               |
| <=          | <span data-ttu-id="8fdd0-169">"Меньше или равно" возвращает значение true, если хотя бы одно из значений элементов на левой стороне меньше или равно любому из значений элементов на стороне справа.</span><span class="sxs-lookup"><span data-stu-id="8fdd0-169">'Less than or equal to' returns true when at least one of the left-side element values is less than or equal to any one of the right-side element values.</span></span>       |



 

## <a name="examples"></a><span data-ttu-id="8fdd0-170">Примеры</span><span class="sxs-lookup"><span data-stu-id="8fdd0-170">Examples</span></span>

<span data-ttu-id="8fdd0-171">В следующем примере проверяется, находятся ли документы в категориях "Финансы" или "планирование":</span><span class="sxs-lookup"><span data-stu-id="8fdd0-171">The following example checks whether documents are in the "Finance" or "Planning" categories:</span></span>


```
SELECT System.ItemUrl FROM SystemIndex WHERE System.Category =
SOME ARRAY['Finance','Planning']
```



<span data-ttu-id="8fdd0-172">В следующих сравнениях вычисляется значение true.</span><span class="sxs-lookup"><span data-stu-id="8fdd0-172">The following comparisons all evaluate true.</span></span> <span data-ttu-id="8fdd0-173">Помните, что при фактическом использовании синтаксис запроса поиска требует, чтобы левая часть была свойством, а не литеральным значением.</span><span class="sxs-lookup"><span data-stu-id="8fdd0-173">Remember that in actual use, the search query syntax requires the left side to be a property, not a literal value.</span></span>


```
ARRAY [1,2] > ARRAY [1,1]
ARRAY [1,2] > ARRAY [1,1,2]
ARRAY [1,2] < ARRAY [1,2,3]
ARRAY [1,2] = SOME ARRAY [1,12,27,35,2]
ARRAY [1,1] != ALL ARRAY [1,2]
ARRAY [1,20,21,22] < SOME ARRAY [0,40]
ARRAY [1,20,21,22] < ANY ARRAY [0,40]
```



## <a name="related-topics"></a><span data-ttu-id="8fdd0-174">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="8fdd0-174">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="8fdd0-175">**Reference**</span><span class="sxs-lookup"><span data-stu-id="8fdd0-175">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8fdd0-176">Предикат LIKE</span><span class="sxs-lookup"><span data-stu-id="8fdd0-176">LIKE Predicate</span></span>](-search-sql-like.md)
</dt> <dt>

[<span data-ttu-id="8fdd0-177">Сравнение литеральных значений</span><span class="sxs-lookup"><span data-stu-id="8fdd0-177">Literal Value Comparison</span></span>](-search-sql-literalvaluecomparison.md)
</dt> <dt>

[<span data-ttu-id="8fdd0-178">Предикат NULL</span><span class="sxs-lookup"><span data-stu-id="8fdd0-178">NULL Predicate</span></span>](-search-sql-null.md)
</dt> <dt>

<span data-ttu-id="8fdd0-179">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="8fdd0-179">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="8fdd0-180">Полнотекстовые предикаты</span><span class="sxs-lookup"><span data-stu-id="8fdd0-180">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)
</dt> <dt>

[<span data-ttu-id="8fdd0-181">Неполнотекстовые предикаты</span><span class="sxs-lookup"><span data-stu-id="8fdd0-181">Non-Full-Text Predicates</span></span>](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



