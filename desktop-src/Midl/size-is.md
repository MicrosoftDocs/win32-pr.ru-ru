---
title: size_is - атрибут
description: Используйте атрибут \ size = \_ \, чтобы указать размер памяти в элементах, выделенных для указателей размера, указателей на размеры указателей и одностраничные или многомерные массивы.
ms.assetid: 1f3f3629-f668-460d-86fd-16ef22449973
keywords:
- size_is атрибута MIDL
topic_type:
- apiref
api_name:
- size_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f65a4c3ea93ea9ed55ce4f6f9ce846c81b60fa40
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103789859"
---
# <a name="size_is-attribute"></a><span data-ttu-id="33f83-104">Size \_ — атрибут</span><span class="sxs-lookup"><span data-stu-id="33f83-104">size\_is attribute</span></span>

<span data-ttu-id="33f83-105">Используйте атрибут \[ **size \_** , \] чтобы указать размер памяти в элементах, выделенных для указателей размера, указателей на размеры указателей и единичных или многомерных массивов.</span><span class="sxs-lookup"><span data-stu-id="33f83-105">Use the \[**size\_is**\] attribute to specify the size of memory, in elements, allocated for sized pointers, sized pointers to sized pointers, and single- or multidimensional arrays.</span></span>

``` syntax
[ size_is(limited-expression-list) ]
```

## <a name="parameters"></a><span data-ttu-id="33f83-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="33f83-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33f83-107">*список ограниченных выражений*</span><span class="sxs-lookup"><span data-stu-id="33f83-107">*limited-expression-list*</span></span> 
</dt> <dd>

<span data-ttu-id="33f83-108">Указывает одно или несколько выражений языка C.</span><span class="sxs-lookup"><span data-stu-id="33f83-108">Specifies one or more C-language expressions.</span></span> <span data-ttu-id="33f83-109">Каждое выражение принимает неотрицательное целое число, представляющее объем памяти, выделенной для указателя размера или массива.</span><span class="sxs-lookup"><span data-stu-id="33f83-109">Each expression evaluates to a non-negative integer that represents the amount of memory allocated to a sized pointer or an array.</span></span> <span data-ttu-id="33f83-110">В случае массива задает одно выражение, представляющее размер выделения в элементах первого измерения этого массива.</span><span class="sxs-lookup"><span data-stu-id="33f83-110">In the case of an array, specifies a single expression that represents the allocation size, in elements, of the first dimension of that array.</span></span> <span data-ttu-id="33f83-111">Компилятор MIDL поддерживает условные выражения, логические выражения, реляционные выражения и арифметические выражения.</span><span class="sxs-lookup"><span data-stu-id="33f83-111">The MIDL compiler supports conditional expressions, logical expressions, relational expressions, and arithmetic expressions.</span></span> <span data-ttu-id="33f83-112">MIDL не разрешает вызовы функций в выражениях и не поддерживает операторы инкремента и декремента.</span><span class="sxs-lookup"><span data-stu-id="33f83-112">MIDL does not allow function invocations in expressions and does not allow increment and decrement operators.</span></span> <span data-ttu-id="33f83-113">Используйте запятые в качестве заполнителей для неявных параметров или для разделения нескольких выражений.</span><span class="sxs-lookup"><span data-stu-id="33f83-113">Use commas as placeholders for implicit parameters, or to separate multiple expressions.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="33f83-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="33f83-114">Remarks</span></span>

<span data-ttu-id="33f83-115">Если используется \[ атрибут **size \_** \] для выделения памяти для многомерного массива и используется \[ \] нотация массива, следует помнить, что только первое измерение многомерного массива может быть динамически определено во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="33f83-115">If you are using the \[**size\_is**\] attribute to allocate memory for a multidimensional array and you are using array \[ \] notation, keep in mind that only the first dimension of a multidimensional array can be dynamically determined at run time.</span></span> <span data-ttu-id="33f83-116">Другие измерения должны быть заданы статически.</span><span class="sxs-lookup"><span data-stu-id="33f83-116">The other dimensions must be statically specified.</span></span> <span data-ttu-id="33f83-117">Дополнительные сведения об использовании \[ **size \_ — это** \] атрибут с несколькими уровнями указателей, позволяющий серверу возвращать клиенту динамически изменяемый массив данных, как показано в примере Proc7, см. раздел [множественные уровни указателей](/windows/desktop/Rpc/multiple-levels-of-pointers).</span><span class="sxs-lookup"><span data-stu-id="33f83-117">For more information on using the \[**size\_is**\] attribute with multiple levels of pointers to enable a server to return a dynamically-sized array of data to a client, as shown in the example Proc7, see [Multiple Levels of Pointers](/windows/desktop/Rpc/multiple-levels-of-pointers).</span></span>

<span data-ttu-id="33f83-118">Можно использовать либо \[ **размер \_ ,** \] либо [**Max ( \_**](max-is.md) но не оба в одном списке атрибутов), чтобы указать размер массива, верхняя граница которого определяется во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="33f83-118">You can use either \[**size\_is**\] or [**max\_is**](max-is.md) (but not both in the same attribute list) to specify the size of an array whose upper bounds are determined at run time.</span></span> <span data-ttu-id="33f83-119">Однако обратите внимание, что \[ **атрибут \_ size** не \] может использоваться для фиксированных измерений массива.</span><span class="sxs-lookup"><span data-stu-id="33f83-119">Note, however, that the \[**size\_is**\] attribute cannot be used on array dimensions that are fixed.</span></span> <span data-ttu-id="33f83-120">Атрибут \[ **Max \_ —** \] указывает максимальный допустимый индекс массива.</span><span class="sxs-lookup"><span data-stu-id="33f83-120">The \[**max\_is**\] attribute specifies the maximum valid array index.</span></span> <span data-ttu-id="33f83-121">В результате указание \[ size \_ равно (n) \] эквивалентно указанию параметра \[ Max \_ равно (n-1) \] .</span><span class="sxs-lookup"><span data-stu-id="33f83-121">As a result, specifying \[size\_is(n)\] is equivalent to specifying \[max\_is(n-1)\].</span></span>

<span data-ttu-id="33f83-122">\[ [**В**](in.md) \] \[ параметре "in" или " [**out**](out-idl.md) \] " параметра-массива с \[ [](string.md) \] атрибутом String не должно быть \[ **атрибута \_ size** \] или \[ [**Max \_**](max-is.md) \] .</span><span class="sxs-lookup"><span data-stu-id="33f83-122">An \[ [**in**](in.md)\] or \[in, [**out**](out-idl.md)\] conformant-array parameter with the \[ [**string**](string.md)\] attribute need not have the \[**size\_is**\] or \[[**max\_is**](max-is.md)\] attribute.</span></span> <span data-ttu-id="33f83-123">В этом случае размер выделения определяется на основе НУЛЕВого терминатора входной строки.</span><span class="sxs-lookup"><span data-stu-id="33f83-123">In this case, the size of the allocation is determined from the NULL terminator of the input string.</span></span> <span data-ttu-id="33f83-124">Все остальные согласованные массивы с \[ \] атрибутом String должны иметь атрибут \[ **size \_** \] или \[ **Max \_** \] .</span><span class="sxs-lookup"><span data-stu-id="33f83-124">All other conformant arrays with the \[string\] attribute must have a \[**size\_is**\] or \[**max\_is**\] attribute.</span></span>

<span data-ttu-id="33f83-125">Несмотря на то, что допускается использование \[ **размера \_** \] атрибута с константой, это неэффективно и не требуется.</span><span class="sxs-lookup"><span data-stu-id="33f83-125">While it is legal to use the \[**size\_is**\] attribute with a constant, doing so is inefficient and unnecessary.</span></span> <span data-ttu-id="33f83-126">Например, используйте массив фиксированного размера:</span><span class="sxs-lookup"><span data-stu-id="33f83-126">For example, use a fixed size array:</span></span>

``` syntax
HRESULT Proc3([in] short Arr[MAX_SIZE]);
```

<span data-ttu-id="33f83-127">вместо</span><span class="sxs-lookup"><span data-stu-id="33f83-127">instead of:</span></span>

``` syntax
// legal but marshaling code is much slower
HRESULT Proc3([in size_is(MAX_SIZE)] short Arr[] );
```

<span data-ttu-id="33f83-128">Можно использовать \[ **размер \_** , \] а \[ [**длина \_ —**](length-is.md) \] атрибуты вместе.</span><span class="sxs-lookup"><span data-stu-id="33f83-128">You can use the \[**size\_is**\] and \[[**length\_is**](length-is.md)\] attributes together.</span></span> <span data-ttu-id="33f83-129">При этом \[ **размер \_ —** \] атрибут определяет объем памяти, выделенной для данных.</span><span class="sxs-lookup"><span data-stu-id="33f83-129">When you do, the \[**size\_is**\] attribute controls the amount of memory allocated for the data.</span></span> <span data-ttu-id="33f83-130">Атрибут \[ **length \_** \] определяет количество передаваемых элементов.</span><span class="sxs-lookup"><span data-stu-id="33f83-130">The \[**length\_is**\] attribute specifies how many elements are transmitted.</span></span> <span data-ttu-id="33f83-131">Объем памяти, указанный в параметре \[ **size, \_ имеет** значение \] , и \[ **длина \_** \] атрибута не должна совпадать.</span><span class="sxs-lookup"><span data-stu-id="33f83-131">The amount of memory specified by the \[**size\_is**\] and \[**length\_is**\] attributes need not be the same.</span></span> <span data-ttu-id="33f83-132">Например, клиент может передать \[ выходной \] параметр на сервер и указать большой объем памяти с \[ **размером \_** \] , даже если он указывает небольшое количество элементов данных, которые должны быть переданы с \[ **длиной \_** \] .</span><span class="sxs-lookup"><span data-stu-id="33f83-132">For instance, your client may pass an \[in,out\] parameter to a server and specify a large memory allocation with \[**size\_is**\], even though it specifies a small number of data elements to be passed with \[**length\_is**\].</span></span> <span data-ttu-id="33f83-133">Это позволяет серверу заполнить массив большим количеством данных, чем получено, который затем можно отправить обратно клиенту.</span><span class="sxs-lookup"><span data-stu-id="33f83-133">This enables the server to fill the array with more data than it received, which it can then send back to the client.</span></span>

<span data-ttu-id="33f83-134">Как правило, нецелесообразно указывать оба \[ **размера \_** , \] а \[ [**длина \_ —**](length-is.md) \] \[ в \] параметрах in и \[ out \] .</span><span class="sxs-lookup"><span data-stu-id="33f83-134">In general, it isn't useful to specify both \[**size\_is**\] and \[[**length\_is**](length-is.md)\] on \[in\] or \[out\] parameters.</span></span> <span data-ttu-id="33f83-135">В обоих случаях \[ **размер \_** \] управляет выделением памяти.</span><span class="sxs-lookup"><span data-stu-id="33f83-135">In both cases, \[**size\_is**\] controls memory allocation.</span></span> <span data-ttu-id="33f83-136">Приложение может использовать \[ **размер \_ —** \] выделить больше элементов массива, чем передается (как указано в параметре \[ **length \_** \] ).</span><span class="sxs-lookup"><span data-stu-id="33f83-136">Your application could use \[**size\_is**\] to allocate more array elements than it transmits (as specified by \[**length\_is**\]).</span></span> <span data-ttu-id="33f83-137">Однако это будет неэффективно.</span><span class="sxs-lookup"><span data-stu-id="33f83-137">However, this would be inefficient.</span></span> <span data-ttu-id="33f83-138">Также было бы неэффективно указывать идентичные значения \[ **размера \_** , \] а \[ **длина \_ —** \] .</span><span class="sxs-lookup"><span data-stu-id="33f83-138">It would also be inefficient to specify identical values for \[**size\_is**\] and \[**length\_is**\].</span></span> <span data-ttu-id="33f83-139">При маршалировании параметров будет создаваться дополнительная нагрузка.</span><span class="sxs-lookup"><span data-stu-id="33f83-139">It would create extra overhead during parameter marshaling.</span></span> <span data-ttu-id="33f83-140">Если значения \[ **size \_** \] и \[ **length \_ не** \] совпадают, то параметр \[ **length \_ имеет** значение \] Attribute.</span><span class="sxs-lookup"><span data-stu-id="33f83-140">If the values of \[**size\_is**\] and \[**length\_is**\] are always the same, omit the \[**length\_is**\] attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="33f83-141">Примеры</span><span class="sxs-lookup"><span data-stu-id="33f83-141">Examples</span></span>

``` syntax
HRESULT Proc1(
    [in] short m;
    [in, size_is(m)] short a[]);  // If m = 10, a[10]
HRESULT Proc2(
    [in] short m;
    [in, size_is(m)] short b[][20]);  // If m = 10, b[10][20]
HRESULT Proc3(
    [in] short m;
    [size_is(m)] short * pshort); /* Specifies a pointer
                                  to an m-sized block of shorts */
HRESULT Proc4(
    [in] short m;
    [size_is( , m)] short ** ppshort); /* Specifies a pointer 
                                       to a pointer to an m-sized 
                                       block of shorts */
HRESULT Proc5(
    [in] short m;
    [size_is(m ,)] short ** ppshort); /* Specifies an
                                      m-sized block of pointers 
                                      to shorts */
HRESULT Proc6(
    [in] short m;
    [in] short n;
    [size_is(m,n)] short ** ppshort); /* Specifies a pointer to an 
                                      m-sized block of pointers, each 
                                      of which points to an n-sized 
                                      block of shorts. m associates with
                                      the pointer closeest to the identifer
                                      it decorates. n associates with rest.*/
 HRESULT Proc7(
     [out] long  * pSize,
     [out, size_is( , *pSize)] my_type ** ppMyType); /* Specifies a pointer 
                                              to a sized pointer, 
                                              which points to a block 
                                              of my_types, whose size is
                                              unknown when the stub 
                                              calls the server. */
```

## <a name="see-also"></a><span data-ttu-id="33f83-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="33f83-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33f83-143">**массивы**</span><span class="sxs-lookup"><span data-stu-id="33f83-143">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="33f83-144">Атрибуты поля</span><span class="sxs-lookup"><span data-stu-id="33f83-144">Field Attributes</span></span>](/windows/desktop/Rpc/field-attributes)
</dt> <dt>

[<span data-ttu-id="33f83-145">**первый \_ —**</span><span class="sxs-lookup"><span data-stu-id="33f83-145">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="33f83-146">Файл определения интерфейса (IDL)</span><span class="sxs-lookup"><span data-stu-id="33f83-146">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="33f83-147">**окне**</span><span class="sxs-lookup"><span data-stu-id="33f83-147">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="33f83-148">**Последний \_ —**</span><span class="sxs-lookup"><span data-stu-id="33f83-148">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="33f83-149">**Длина \_ равна**</span><span class="sxs-lookup"><span data-stu-id="33f83-149">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="33f83-150">**Максимальное \_ число**</span><span class="sxs-lookup"><span data-stu-id="33f83-150">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="33f83-151">**min \_ —**</span><span class="sxs-lookup"><span data-stu-id="33f83-151">**min\_is**</span></span>](min-is.md)
</dt> <dt>

[<span data-ttu-id="33f83-152">**заполняет**</span><span class="sxs-lookup"><span data-stu-id="33f83-152">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="33f83-153">**Строка**</span><span class="sxs-lookup"><span data-stu-id="33f83-153">**string**</span></span>](string.md)
</dt> </dl>

 

 