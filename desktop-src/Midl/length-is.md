---
title: length_is - атрибут
description: Атрибут \ length = \_ \ указывает число передаваемых элементов массива. Необходимо указать неотрицательное значение.
ms.assetid: 060dbd4a-3078-4050-abfe-c1b633c06861
keywords:
- length_is атрибута MIDL
topic_type:
- apiref
api_name:
- length_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fac217bae01c6896c7dadd36bb18f15e425a0427
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487684"
---
# <a name="length_is-attribute"></a><span data-ttu-id="7da50-105">Length \_ — атрибут</span><span class="sxs-lookup"><span data-stu-id="7da50-105">length\_is attribute</span></span>

<span data-ttu-id="7da50-106">Атрибут **\[ \_ length \]** указывает количество передаваемых элементов массива.</span><span class="sxs-lookup"><span data-stu-id="7da50-106">The **\[length\_is\]** attribute specifies the number of array elements to be transmitted.</span></span> <span data-ttu-id="7da50-107">Необходимо указать неотрицательное значение.</span><span class="sxs-lookup"><span data-stu-id="7da50-107">You must specify a non-negative value.</span></span>

``` syntax
[length_is( limited-expression-list )]
```

## <a name="parameters"></a><span data-ttu-id="7da50-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7da50-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7da50-109">*список ограниченных выражений*</span><span class="sxs-lookup"><span data-stu-id="7da50-109">*limited-expression-list*</span></span> 
</dt> <dd>

<span data-ttu-id="7da50-110">Указывает одно или несколько выражений языка C.</span><span class="sxs-lookup"><span data-stu-id="7da50-110">Specifies one or more C-language expressions.</span></span> <span data-ttu-id="7da50-111">Каждое выражение оценивается как целое число, представляющее число передаваемых элементов массива.</span><span class="sxs-lookup"><span data-stu-id="7da50-111">Each expression evaluates to an integer that represents the number of array elements to be transmitted.</span></span> <span data-ttu-id="7da50-112">Компилятор MIDL поддерживает условные выражения, логические выражения, реляционные выражения и арифметические выражения.</span><span class="sxs-lookup"><span data-stu-id="7da50-112">The MIDL compiler supports conditional expressions, logical expressions, relational expressions, and arithmetic expressions.</span></span> <span data-ttu-id="7da50-113">MIDL не разрешает вызовы функций в выражениях и не поддерживает операторы инкремента и декремента.</span><span class="sxs-lookup"><span data-stu-id="7da50-113">MIDL does not allow function invocations in expressions and does not allow increment and decrement operators.</span></span> <span data-ttu-id="7da50-114">Несколько выражений разделяются запятыми.</span><span class="sxs-lookup"><span data-stu-id="7da50-114">Separate multiple expressions with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7da50-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7da50-115">Remarks</span></span>

<span data-ttu-id="7da50-116">Атрибут **\[ \_ length \]** определяет значение индексов массива, соответствующих **\[** [**\_**](last-is.md) **\]** **\[ \_ последнему атрибуту, если параметр Last не задан. \]**</span><span class="sxs-lookup"><span data-stu-id="7da50-116">The **\[length\_is\]** attribute determines the value of the array indexes corresponding to the **\[**[**last\_is**](last-is.md)**\]** attribute when **\[last\_is\]** is not specified.</span></span> <span data-ttu-id="7da50-117">Связь между этими индексами массива выглядит следующим образом: Length = Last-First + 1.</span><span class="sxs-lookup"><span data-stu-id="7da50-117">The relationship between these array indexes is as follows: length = last - first + 1.</span></span>

<span data-ttu-id="7da50-118">Атрибут **\[ \_ length \]** не может использоваться одновременно с атрибутом **\[** [**Last \_ -**](last-is.md) **\]** Attribute или **\[** [**строковым**](string.md) **\]** атрибутом.</span><span class="sxs-lookup"><span data-stu-id="7da50-118">The **\[length\_is\]** attribute cannot be used at the same time as the **\[**[**last\_is**](last-is.md)**\]** attribute or the **\[**[**string**](string.md)**\]** attribute.</span></span>

<span data-ttu-id="7da50-119">Чтобы определить подсчитанную строку с атрибутом **\[ length \_ \]** или **\[** [**Last \_ -**](last-is.md) **\]** Attribute, используйте массив символов или указатель без атрибута **\[** [**String**](string.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="7da50-119">To define a counted string with a **\[length\_is\]** or **\[**[**last\_is**](last-is.md)**\]** attribute, use a character array or pointer without the **\[**[**string**](string.md)**\]** attribute.</span></span>

<span data-ttu-id="7da50-120">Использование константного выражения с атрибутом **\[ length \_ является \]** недопустимым применением атрибута.</span><span class="sxs-lookup"><span data-stu-id="7da50-120">Using a constant expression with the **\[length\_is\]** attribute is an inappropriate use of the attribute.</span></span> <span data-ttu-id="7da50-121">Он является юридическим, но неэффективным и приведет к более медленному упаковке кода.</span><span class="sxs-lookup"><span data-stu-id="7da50-121">It is legal, but inefficient, and will result in slower marshaling code.</span></span>

<span data-ttu-id="7da50-122">Можно использовать **\[** [**размер \_**](size-is.md) , **\]** а **\[ длина \_ \] —** атрибуты вместе.</span><span class="sxs-lookup"><span data-stu-id="7da50-122">You can use the **\[**[**size\_is**](size-is.md)**\]** and **\[length\_is\]** attributes together.</span></span> <span data-ttu-id="7da50-123">При этом **\[ размер \_ — \]** атрибут определяет объем памяти, выделенной для данных.</span><span class="sxs-lookup"><span data-stu-id="7da50-123">When you do, the **\[size\_is\]** attribute controls the amount of memory allocated for the data.</span></span> <span data-ttu-id="7da50-124">Атрибут **\[ \_ length \]** определяет количество передаваемых элементов.</span><span class="sxs-lookup"><span data-stu-id="7da50-124">The **\[length\_is\]** attribute specifies how many elements are transmitted.</span></span> <span data-ttu-id="7da50-125">Объем памяти, указанный в параметре **\[ size \_ , \] имеет** значение, и **\[ длина \_ \]** атрибута не должна совпадать.</span><span class="sxs-lookup"><span data-stu-id="7da50-125">The amount of memory specified by the **\[size\_is\]** and **\[length\_is\]** attributes need not be the same.</span></span> <span data-ttu-id="7da50-126">Например, клиент может передать **выходной \]** **\[ параметр на сервер** и указать большой объем **\[ \_ \]** памяти с размером, даже если он указывает небольшое **\[ \_ \]** количество элементов данных, которые должны быть переданы с длиной.</span><span class="sxs-lookup"><span data-stu-id="7da50-126">For instance, your client may pass an **\[in**, **out\]** parameter to a server and specify a large memory allocation with **\[size\_is\]**, even though it specifies a small number of data elements to be passed with **\[length\_is\]**.</span></span> <span data-ttu-id="7da50-127">Это позволяет серверу заполнить массив большим количеством данных, чем получено, который затем можно отправить обратно клиенту.</span><span class="sxs-lookup"><span data-stu-id="7da50-127">This enables the server to fill the array with more data than it received, which it can then send back to the client.</span></span>

<span data-ttu-id="7da50-128">Как правило, нецелесообразно указывать оба **\[** [**размера, \_**](size-is.md) **\]** а **\[ длина \_ — \]** **\[** [**в**](in.md) **\]** параметрах in и **\[** [**out**](out-idl.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="7da50-128">In general, it isn't useful to specify both **\[**[**size\_is**](size-is.md)**\]** and **\[length\_is\]** on **\[**[**in**](in.md)**\]** or **\[**[**out**](out-idl.md)**\]** parameters.</span></span> <span data-ttu-id="7da50-129">В обоих случаях **\[ размер \_ \]** управляет выделением памяти.</span><span class="sxs-lookup"><span data-stu-id="7da50-129">In both cases, **\[size\_is\]** controls memory allocation.</span></span> <span data-ttu-id="7da50-130">Приложение может использовать **\[ размер \_ — \]** выделить больше элементов массива, чем передается (как **\[ \_ \]** указано в параметре length).</span><span class="sxs-lookup"><span data-stu-id="7da50-130">Your application could use **\[size\_is\]** to allocate more array elements than it transmits (as specified by **\[length\_is\]**).</span></span> <span data-ttu-id="7da50-131">Однако это будет неэффективно.</span><span class="sxs-lookup"><span data-stu-id="7da50-131">However, this would be inefficient.</span></span> <span data-ttu-id="7da50-132">Также было бы неэффективно указывать идентичные значения **\[ размера \_ \]** , а **\[ длина \_ — \]**.</span><span class="sxs-lookup"><span data-stu-id="7da50-132">It would also be inefficient to specify identical values for **\[size\_is\]** and **\[length\_is\]**.</span></span> <span data-ttu-id="7da50-133">Так как при маршалировании параметров будет создаваться дополнительная нагрузка.</span><span class="sxs-lookup"><span data-stu-id="7da50-133">Because it would create extra overhead during parameter marshaling.</span></span> <span data-ttu-id="7da50-134">Если значения **\[ size \_ \]** и **\[ length \_ не \]** совпадают, то параметр **\[ length \_ имеет \]** значение Attribute.</span><span class="sxs-lookup"><span data-stu-id="7da50-134">When the values of **\[size\_is\]** and **\[length\_is\]** are always the same, omit the **\[length\_is\]** attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="7da50-135">Примеры</span><span class="sxs-lookup"><span data-stu-id="7da50-135">Examples</span></span>

``` syntax
/* counted string holding at most "size" characters */ 
typedef struct 
{ 
    unsigned short size; 
    unsigned short length; 
    [size_is(size), length_is(length)] char string[*]; 
 } COUNTED_STRING_TYPE; 
 
/* counted string holding at most 80 characters */ 
typedef struct 
{ 
    unsigned short length; 
    [length_is(length)] char string[80]; 
} STATIC_COUNTED_STRING_TYPE; 
 
HRESULT Proc1(
    [in] short iLength; 
    [in, length_is(iLength)] short asNumbers[10]);
```

## <a name="see-also"></a><span data-ttu-id="7da50-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7da50-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7da50-137">Атрибуты поля</span><span class="sxs-lookup"><span data-stu-id="7da50-137">Field Attributes</span></span>](/windows/desktop/Rpc/field-attributes)
</dt> <dt>

[<span data-ttu-id="7da50-138">**первый \_ —**</span><span class="sxs-lookup"><span data-stu-id="7da50-138">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="7da50-139">Файл определения интерфейса (IDL)</span><span class="sxs-lookup"><span data-stu-id="7da50-139">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="7da50-140">**Последний \_ —**</span><span class="sxs-lookup"><span data-stu-id="7da50-140">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="7da50-141">**Максимальное \_ число**</span><span class="sxs-lookup"><span data-stu-id="7da50-141">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="7da50-142">**min \_ —**</span><span class="sxs-lookup"><span data-stu-id="7da50-142">**min\_is**</span></span>](min-is.md)
</dt> <dt>

[<span data-ttu-id="7da50-143">**размер \_ равен**</span><span class="sxs-lookup"><span data-stu-id="7da50-143">**size\_is**</span></span>](size-is.md)
</dt> <dt>

[<span data-ttu-id="7da50-144">**Строка**</span><span class="sxs-lookup"><span data-stu-id="7da50-144">**string**</span></span>](string.md)
</dt> </dl>

 

 