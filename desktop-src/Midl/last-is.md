---
title: last_is - атрибут
description: Атрибут поля \ Last \_ имеет значение \ задает индекс последнего передаваемого элемента массива. Если указанный индекс равен нулю или отрицательен, элементы массива не передаются.
ms.assetid: 42a5cb0d-0887-4aa7-b34f-2fbad0f4c8ab
keywords:
- last_is атрибута MIDL
topic_type:
- apiref
api_name:
- last_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 453a51109452f3cdacb1a48e67b76ccbc9f2e257
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104533161"
---
# <a name="last_is-attribute"></a><span data-ttu-id="b889e-105">Last \_ — атрибут</span><span class="sxs-lookup"><span data-stu-id="b889e-105">last\_is attribute</span></span>

<span data-ttu-id="b889e-106">Атрибут поля **\[ Last \_ \]** указывает индекс последнего передаваемого элемента массива.</span><span class="sxs-lookup"><span data-stu-id="b889e-106">The field attribute **\[last\_is\]** specifies the index of the last array element to be transmitted.</span></span> <span data-ttu-id="b889e-107">Если указанный индекс равен нулю или отрицательен, элементы массива не передаются.</span><span class="sxs-lookup"><span data-stu-id="b889e-107">When the specified index is zero or negative, no array elements are transmitted.</span></span>

``` syntax
[last_is( limited-expression-list )]
```

## <a name="parameters"></a><span data-ttu-id="b889e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b889e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b889e-109">*список ограниченных выражений*</span><span class="sxs-lookup"><span data-stu-id="b889e-109">*limited-expression-list*</span></span> 
</dt> <dd>

<span data-ttu-id="b889e-110">Указывает одно или несколько выражений языка C.</span><span class="sxs-lookup"><span data-stu-id="b889e-110">Specifies one or more C-language expressions.</span></span> <span data-ttu-id="b889e-111">Каждое выражение оценивается как целое число, представляющее индекс массива последнего передаваемого элемента массива.</span><span class="sxs-lookup"><span data-stu-id="b889e-111">Each expression evaluates to an integer that represents the array index of the last array element to be transmitted.</span></span> <span data-ttu-id="b889e-112">Компилятор MIDL поддерживает условные выражения, логические выражения, реляционные выражения и арифметические выражения.</span><span class="sxs-lookup"><span data-stu-id="b889e-112">The MIDL compiler supports conditional expressions, logical expressions, relational expressions, and arithmetic expressions.</span></span> <span data-ttu-id="b889e-113">MIDL не разрешает вызовы функций в выражениях и не поддерживает операторы инкремента и декремента.</span><span class="sxs-lookup"><span data-stu-id="b889e-113">MIDL does not allow function invocations in expressions and does not allow increment and decrement operators.</span></span> <span data-ttu-id="b889e-114">Несколько выражений разделяются запятыми.</span><span class="sxs-lookup"><span data-stu-id="b889e-114">Separate multiple expressions with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b889e-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b889e-115">Remarks</span></span>

<span data-ttu-id="b889e-116">Атрибут **\[ Last \_ - \]** Attribute определяет значение индекса массива, соответствующего **\[** [**\_**](length-is.md) **\]** **\[ \_ \]** длине, если параметр length не указан.</span><span class="sxs-lookup"><span data-stu-id="b889e-116">The **\[last\_is\]** attribute determines the value of the array index corresponding to the **\[**[**length\_is**](length-is.md)**\]** attribute when **\[length\_is\]** is not specified.</span></span> <span data-ttu-id="b889e-117">Связь между этими индексами массива выглядит следующим образом: Length = Last-First + 1.</span><span class="sxs-lookup"><span data-stu-id="b889e-117">The relationship between these array indexes is as follows: length = last - first + 1.</span></span>

<span data-ttu-id="b889e-118">Если значение индекса массива, указанное в параметре **\[** [**First \_**](first-is.md) , больше **\]** , чем значение, **\[ \_ \]** заданное параметром Last, то передаются нулевые элементы.</span><span class="sxs-lookup"><span data-stu-id="b889e-118">If the value of the array index specified by **\[**[**first\_is**](first-is.md)**\]** is larger than the value specified by **\[last\_is\]**, zero elements are transmitted.</span></span>

<span data-ttu-id="b889e-119">Атрибут **\[ Last \_ - \]** Attribute не может использоваться в качестве атрибута поля одновременно с атрибутом **\[** [**length \_**](length-is.md) **\]** или **\[** [**строковым**](string.md) **\]** атрибутом.</span><span class="sxs-lookup"><span data-stu-id="b889e-119">The **\[last\_is\]** attribute cannot be used as a field attribute at the same time as the **\[**[**length\_is**](length-is.md)**\]** attribute or the **\[**[**string**](string.md)**\]** attribute.</span></span>

<span data-ttu-id="b889e-120">Использование константного выражения с атрибутом **\[ Last \_ является \]** неуместным применением атрибута.</span><span class="sxs-lookup"><span data-stu-id="b889e-120">Using a constant expression with the **\[last\_is\]** attribute is an inappropriate use of the attribute.</span></span> <span data-ttu-id="b889e-121">Он является юридическим, но неэффективным и приведет к более медленному упаковке кода.</span><span class="sxs-lookup"><span data-stu-id="b889e-121">It is legal, but inefficient, and will result in slower marshaling code.</span></span>

<span data-ttu-id="b889e-122">Если значение, указанное параметром **\[** [**Max \_**](max-is.md) , **\]** равно или больше нуля, следующее отношение должно иметь значение true: 0 <= Last \_ — <= Max \_ —.</span><span class="sxs-lookup"><span data-stu-id="b889e-122">When the value specified by **\[**[**max\_is**](max-is.md)**\]** is equal to or greater than zero, the following relationship must be true: 0 <= last\_is <= max\_is.</span></span>

## <a name="examples"></a><span data-ttu-id="b889e-123">Примеры</span><span class="sxs-lookup"><span data-stu-id="b889e-123">Examples</span></span>

``` syntax
proc1(
    [in] short Last,
    [in, last_is(Last)] short asNumbers[MAXSIZE]);
```

## <a name="see-also"></a><span data-ttu-id="b889e-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b889e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b889e-125">Атрибуты поля</span><span class="sxs-lookup"><span data-stu-id="b889e-125">Field Attributes</span></span>](/windows/desktop/Rpc/field-attributes)
</dt> <dt>

[<span data-ttu-id="b889e-126">**первый \_ —**</span><span class="sxs-lookup"><span data-stu-id="b889e-126">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="b889e-127">Файл определения интерфейса (IDL)</span><span class="sxs-lookup"><span data-stu-id="b889e-127">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="b889e-128">**Длина \_ равна**</span><span class="sxs-lookup"><span data-stu-id="b889e-128">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="b889e-129">**Максимальное \_ число**</span><span class="sxs-lookup"><span data-stu-id="b889e-129">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="b889e-130">**размер \_ равен**</span><span class="sxs-lookup"><span data-stu-id="b889e-130">**size\_is**</span></span>](size-is.md)
</dt> </dl>

 

 