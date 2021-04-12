---
title: max_is - атрибут
description: Атрибут \ Max = \_ \ задает максимальное значение для допустимого индекса массива.
ms.assetid: 8d09f610-cae6-45f6-815c-5ba916d8a5e7
keywords:
- max_is атрибута MIDL
topic_type:
- apiref
api_name:
- max_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27f2e2040acbc0e8f65c02f4f4ec7c3ad329959b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337044"
---
# <a name="max_is-attribute"></a><span data-ttu-id="a055f-104">Max \_ — атрибут</span><span class="sxs-lookup"><span data-stu-id="a055f-104">max\_is attribute</span></span>

<span data-ttu-id="a055f-105">Атрибут **\[ Max \_ — \]** указывает максимальное значение для допустимого индекса массива.</span><span class="sxs-lookup"><span data-stu-id="a055f-105">The **\[max\_is\]** attribute designates the maximum value for a valid array index.</span></span>

``` syntax
[max_is(limited-expression-list )]
```

## <a name="parameters"></a><span data-ttu-id="a055f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a055f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a055f-107">*список ограниченных выражений*</span><span class="sxs-lookup"><span data-stu-id="a055f-107">*limited-expression-list*</span></span> 
</dt> <dd>

<span data-ttu-id="a055f-108">Указывает одно или несколько выражений языка C.</span><span class="sxs-lookup"><span data-stu-id="a055f-108">Specifies one or more C-language expressions.</span></span> <span data-ttu-id="a055f-109">Каждое выражение оценивается как целое число, представляющее наибольший допустимый индекс массива.</span><span class="sxs-lookup"><span data-stu-id="a055f-109">Each expression evaluates to an integer that represents the highest valid array index.</span></span> <span data-ttu-id="a055f-110">Компилятор MIDL поддерживает условные выражения, логические выражения, реляционные выражения и арифметические выражения.</span><span class="sxs-lookup"><span data-stu-id="a055f-110">The MIDL compiler supports conditional expressions, logical expressions, relational expressions, and arithmetic expressions.</span></span> <span data-ttu-id="a055f-111">MIDL не разрешает вызовы функций в выражениях и не поддерживает операторы инкремента и декремента.</span><span class="sxs-lookup"><span data-stu-id="a055f-111">MIDL does not allow function invocations in expressions and does not allow increment and decrement operators.</span></span> <span data-ttu-id="a055f-112">Несколько выражений разделяются запятыми.</span><span class="sxs-lookup"><span data-stu-id="a055f-112">Separate multiple expressions with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a055f-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a055f-113">Remarks</span></span>

<span data-ttu-id="a055f-114">Атрибут **\[ \_ Max \]** не обязательно соответствует количеству элементов в массиве.</span><span class="sxs-lookup"><span data-stu-id="a055f-114">The **\[max\_is\]** attribute does not necessarily correspond to the number of elements in the array.</span></span> <span data-ttu-id="a055f-115">Для массива размером *n* в C, где первый элемент массива является нулевым числом элементов, максимальное значение для допустимого индекса массива равно *n*– 1.</span><span class="sxs-lookup"><span data-stu-id="a055f-115">For an array of size *n* in C, where the first array element is element number zero, the maximum value for a valid array index is *n*–1.</span></span>

<span data-ttu-id="a055f-116">Атрибут **\[ Max \_ не \]** может использоваться в качестве атрибута поля одновременно с **\[** [**\_**](size-is.md) **\]** атрибутом Size.</span><span class="sxs-lookup"><span data-stu-id="a055f-116">The **\[max\_is\]** attribute cannot be used as a field attribute at the same time as the **\[**[**size\_is**](size-is.md)**\]** attribute.</span></span>

<span data-ttu-id="a055f-117">Хотя допускается использование атрибута **\[ Max \_ \]** с константным выражением, это неэффективно и не требуется.</span><span class="sxs-lookup"><span data-stu-id="a055f-117">While it is legal to use the **\[max\_is\]** attribute with a constant expression, doing so is inefficient and unnecessary.</span></span> <span data-ttu-id="a055f-118">Например, используйте массив фиксированного размера:</span><span class="sxs-lookup"><span data-stu-id="a055f-118">For example, use a fixed size array:</span></span>

``` syntax
/* transmits values of a[0]... a[MAX_SIZE-1] */ 
HRESULT Proc3([in] short Arr[MAX_SIZE]); 
```

<span data-ttu-id="a055f-119">вместо</span><span class="sxs-lookup"><span data-stu-id="a055f-119">instead of:</span></span>

``` syntax
/* legal but marshaling code is much slower */ 
HRESULT Proc3([in max_is(MAX_SIZE-1)] short Arr[] );
```

## <a name="examples"></a><span data-ttu-id="a055f-120">Примеры</span><span class="sxs-lookup"><span data-stu-id="a055f-120">Examples</span></span>

``` syntax
/* if m = 10, there are 11 transmitted elements (a[0]...a[10])*/ 
HRESULT Proc1( 
    [in] short m, 
    [in, max_is(m)] short a[]);  
 
/* if m = 10, the valid range for b is b[0...10][20] */ 
HRESULT Proc2( 
    [in] short m, 
    [in, max_is(m)] short b[][20];
```

## <a name="see-also"></a><span data-ttu-id="a055f-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a055f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a055f-122">Атрибуты поля</span><span class="sxs-lookup"><span data-stu-id="a055f-122">Field Attributes</span></span>](/windows/desktop/Rpc/field-attributes)
</dt> <dt>

[<span data-ttu-id="a055f-123">Файл определения интерфейса (IDL)</span><span class="sxs-lookup"><span data-stu-id="a055f-123">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="a055f-124">**min \_ —**</span><span class="sxs-lookup"><span data-stu-id="a055f-124">**min\_is**</span></span>](min-is.md)
</dt> <dt>

[<span data-ttu-id="a055f-125">**размер \_ равен**</span><span class="sxs-lookup"><span data-stu-id="a055f-125">**size\_is**</span></span>](size-is.md)
</dt> </dl>

 

 