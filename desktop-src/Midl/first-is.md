---
title: first_is - атрибут
description: Атрибут \ First \ \_ \ указывает индекс первого передаваемого элемента массива.
ms.assetid: 1de7821c-19e7-4b2c-98fc-2fae3563831c
keywords:
- first_is атрибута MIDL
topic_type:
- apiref
api_name:
- first_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1d8d1be33299354e77ef92d885bb3b092cccfb6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103890641"
---
# <a name="first_is-attribute"></a><span data-ttu-id="302d2-104">First \_ — атрибут</span><span class="sxs-lookup"><span data-stu-id="302d2-104">first\_is attribute</span></span>

<span data-ttu-id="302d2-105">\[ **Первый атрибут \_ —** \] указывает индекс первого передаваемого элемента массива.</span><span class="sxs-lookup"><span data-stu-id="302d2-105">The \[**first\_is**\] attribute specifies the index of the first array element to be transmitted.</span></span>

``` syntax
first_is(limited-expression-list)
```

## <a name="parameters"></a><span data-ttu-id="302d2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="302d2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="302d2-107">*список ограниченных выражений*</span><span class="sxs-lookup"><span data-stu-id="302d2-107">*limited-expression-list*</span></span> 
</dt> <dd>

<span data-ttu-id="302d2-108">Указывает одно или несколько выражений языка C.</span><span class="sxs-lookup"><span data-stu-id="302d2-108">Specifies one or more C-language expressions.</span></span> <span data-ttu-id="302d2-109">Каждое выражение оценивается как целое число, представляющее индекс массива первого передаваемого элемента массива.</span><span class="sxs-lookup"><span data-stu-id="302d2-109">Each expression evaluates to an integer that represents the array index of the first array element to be transmitted.</span></span> <span data-ttu-id="302d2-110">Компилятор MIDL поддерживает условные выражения, логические выражения, реляционные выражения и арифметические выражения.</span><span class="sxs-lookup"><span data-stu-id="302d2-110">The MIDL compiler supports conditional expressions, logical expressions, relational expressions, and arithmetic expressions.</span></span> <span data-ttu-id="302d2-111">MIDL не разрешает вызовы функций в выражениях и не поддерживает операторы инкремента и декремента.</span><span class="sxs-lookup"><span data-stu-id="302d2-111">MIDL does not allow function invocations in expressions and does not allow increment and decrement operators.</span></span> <span data-ttu-id="302d2-112">Несколько выражений разделяются запятыми.</span><span class="sxs-lookup"><span data-stu-id="302d2-112">Separate multiple expressions with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="302d2-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="302d2-113">Remarks</span></span>

<span data-ttu-id="302d2-114">Если **\[ первый \_ \]** атрибут отсутствует или если указанный индекс является отрицательным числом, то первый передаваемый элемент массива равен нулю.</span><span class="sxs-lookup"><span data-stu-id="302d2-114">If the **\[first\_is\]** attribute is not present, or if the specified index is a negative number, array element zero is the first element transmitted.</span></span>

<span data-ttu-id="302d2-115">**\[ Первый атрибут \_ — \]** может также помочь определить значения индексов массива, соответствующих **\[** [**последнему \_**](last-is.md) **\]** атрибуту, или **\[** [**length \_ ,**](length-is.md) **\]** Если эти атрибуты не указаны.</span><span class="sxs-lookup"><span data-stu-id="302d2-115">The **\[first\_is\]** attribute can also help determine the values of the array indexes corresponding to the **\[**[**last\_is**](last-is.md)**\]** or **\[**[**length\_is**](length-is.md)**\]** attribute when these attributes are not specified.</span></span> <span data-ttu-id="302d2-116">Отношения между этими индексами массива:</span><span class="sxs-lookup"><span data-stu-id="302d2-116">The relationship between these array indexes is:</span></span>

``` syntax
length = last - first + 1
```

<span data-ttu-id="302d2-117">Также должна храниться Следующая связь:</span><span class="sxs-lookup"><span data-stu-id="302d2-117">The following relationship must also hold:</span></span>

``` syntax
0 <= first_is <= max_is
```

<span data-ttu-id="302d2-118">Если **\[** [**\_ параметр max имеет значение**](max-is.md) **\] <= 0** , должно быть указано следующее отношение.</span><span class="sxs-lookup"><span data-stu-id="302d2-118">The following relationship must hold when **\[**[**max\_is**](max-is.md)**\] <= 0:**</span></span>

``` syntax
first_is == 0
```

<span data-ttu-id="302d2-119">**\[ Первый атрибут \_ является \] недопустимым** в то же время, что и **\[** атрибут [**String**](string.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="302d2-119">The **\[first\_is\]** attribute cannot be used at the same time as the **\[**[**string**](string.md)**\]** attribute.</span></span>

<span data-ttu-id="302d2-120">Использование константного выражения с первым атрибутом **\[ \_ является \]** недопустимым применением атрибута.</span><span class="sxs-lookup"><span data-stu-id="302d2-120">Using a constant expression with the **\[first\_is\]** attribute is an inappropriate use of the attribute.</span></span> <span data-ttu-id="302d2-121">Он является юридическим, но неэффективным и приведет к более медленному упаковке кода.</span><span class="sxs-lookup"><span data-stu-id="302d2-121">It is legal, but inefficient, and will result in slower marshaling code.</span></span>

## <a name="examples"></a><span data-ttu-id="302d2-122">Примеры</span><span class="sxs-lookup"><span data-stu-id="302d2-122">Examples</span></span>

``` syntax
HRESULT Proc1(
    [in] short First,
    [first_is(First)] Arr[10]);
```

## <a name="see-also"></a><span data-ttu-id="302d2-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="302d2-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="302d2-124">\_атрибуты поля</span><span class="sxs-lookup"><span data-stu-id="302d2-124">field\_attributes</span></span>](/windows/desktop/Rpc/field-attributes)
</dt> <dt>

[<span data-ttu-id="302d2-125">Файл определения интерфейса (IDL)</span><span class="sxs-lookup"><span data-stu-id="302d2-125">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="302d2-126">**Последний \_ —**</span><span class="sxs-lookup"><span data-stu-id="302d2-126">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="302d2-127">**Длина \_ равна**</span><span class="sxs-lookup"><span data-stu-id="302d2-127">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="302d2-128">**Максимальное \_ число**</span><span class="sxs-lookup"><span data-stu-id="302d2-128">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="302d2-129">**min \_ —**</span><span class="sxs-lookup"><span data-stu-id="302d2-129">**min\_is**</span></span>](min-is.md)
</dt> <dt>

[<span data-ttu-id="302d2-130">**размер \_ равен**</span><span class="sxs-lookup"><span data-stu-id="302d2-130">**size\_is**</span></span>](size-is.md)
</dt> <dt>

[<span data-ttu-id="302d2-131">**Строка**</span><span class="sxs-lookup"><span data-stu-id="302d2-131">**string**</span></span>](string.md)
</dt> </dl>

 

 