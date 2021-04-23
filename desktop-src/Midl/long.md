---
title: Long, атрибут
description: Ключевое слово Long обозначает 32-разрядное целое число.
ms.assetid: 5619e482-e3c3-4898-a70b-afd337d2749a
keywords:
- атрибут Long MIDL
topic_type:
- apiref
api_name:
- long
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47ea9af3bfac85ff375f6d5433b4e9f3ed37d8f7
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103986925"
---
# <a name="long-attribute"></a><span data-ttu-id="b043f-104">Long, атрибут</span><span class="sxs-lookup"><span data-stu-id="b043f-104">long attribute</span></span>

<span data-ttu-id="b043f-105">Ключевое слово **Long** обозначает 32-разрядное целое число.</span><span class="sxs-lookup"><span data-stu-id="b043f-105">The **long** keyword designates a 32-bit integer.</span></span>

``` syntax
[ signed | unsigned ] long [ int ] declarator-list;
```

## <a name="parameters"></a><span data-ttu-id="b043f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b043f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b043f-107">*декларатор-список*</span><span class="sxs-lookup"><span data-stu-id="b043f-107">*declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="b043f-108">Указывает один или несколько стандартных деклараторов C, таких как идентификаторы, деклараторы указателей и деклараторы массивов.</span><span class="sxs-lookup"><span data-stu-id="b043f-108">Specifies one or more standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="b043f-109">(Деклараторы функций и объявления битовых полей не допускаются в структурах, передаваемых в удаленных вызовах процедур.</span><span class="sxs-lookup"><span data-stu-id="b043f-109">(Function declarators and bit-field declarations are not allowed in structures that are transmitted in remote procedure calls.</span></span> <span data-ttu-id="b043f-110">Эти деклараторы разрешены в структурах, которые не передаются.) Несколько деклараторов разделяются запятыми.</span><span class="sxs-lookup"><span data-stu-id="b043f-110">These declarators are allowed in structures that are not transmitted.) Separate multiple declarators with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b043f-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b043f-111">Remarks</span></span>

<span data-ttu-id="b043f-112">Ключевому слову **Long** может предшествовать либо ключевое слово signed [**, либо**](signed.md) ключевое слово [**без знака**](unsigned.md).</span><span class="sxs-lookup"><span data-stu-id="b043f-112">The **long** keyword can be preceded by either the keyword [**signed**](signed.md) or the keyword [**unsigned**](unsigned.md).</span></span> <span data-ttu-id="b043f-113">Ключевое слово [**int**](int.md) является необязательным и может быть опущено.</span><span class="sxs-lookup"><span data-stu-id="b043f-113">The [**int**](int.md) keyword is optional and can be omitted.</span></span> <span data-ttu-id="b043f-114">В компиляторе MIDL длинное целое подписывается по умолчанию и является синонимом длинного целочисленного типа **со знаком**. На 32-разрядных платформах **Long** является синонимом **int**.</span><span class="sxs-lookup"><span data-stu-id="b043f-114">To the MIDL compiler, a long integer is signed by default and is synonymous with **signed long int**. On 32-bit platforms, **long** is synonymous with **int**.</span></span>

<span data-ttu-id="b043f-115">Целочисленный тип **Long** является одним из базовых типов языка IDL.</span><span class="sxs-lookup"><span data-stu-id="b043f-115">The **long** integer type is one of the base types of the IDL language.</span></span> <span data-ttu-id="b043f-116">Тип **длинного** целого числа может быть спецификатором типа в объявлениях [**const**](const.md) , объявлениях [**typedef**](typedef.md) , общих объявлениях и деклараторах функций (в виде спецификатора возврата функции и спецификатора типа параметра).</span><span class="sxs-lookup"><span data-stu-id="b043f-116">The **long** integer type can appear as a type specifier in [**const**](const.md) declarations, [**typedef**](typedef.md) declarations, general declarations, and function declarators (as a function return–type specifier and as a parameter-type specifier).</span></span> <span data-ttu-id="b043f-117">Контекст, в котором отображаются спецификаторы типов, см. в разделе [IDL-файл](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="b043f-117">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="b043f-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b043f-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b043f-119">**const**</span><span class="sxs-lookup"><span data-stu-id="b043f-119">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="b043f-120">Базовые типы MIDL</span><span class="sxs-lookup"><span data-stu-id="b043f-120">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="b043f-121">**Hyper**</span><span class="sxs-lookup"><span data-stu-id="b043f-121">**hyper**</span></span>](hyper.md)
</dt> <dt>

[<span data-ttu-id="b043f-122">**INT**</span><span class="sxs-lookup"><span data-stu-id="b043f-122">**int**</span></span>](int.md)
</dt> <dt>

[<span data-ttu-id="b043f-123">**short**</span><span class="sxs-lookup"><span data-stu-id="b043f-123">**short**</span></span>](short.md)
</dt> <dt>

[<span data-ttu-id="b043f-124">**входил**</span><span class="sxs-lookup"><span data-stu-id="b043f-124">**signed**</span></span>](signed.md)
</dt> <dt>

[<span data-ttu-id="b043f-125">**значительные**</span><span class="sxs-lookup"><span data-stu-id="b043f-125">**small**</span></span>](small.md)
</dt> <dt>

[<span data-ttu-id="b043f-126">**определение**</span><span class="sxs-lookup"><span data-stu-id="b043f-126">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="b043f-127">**без знака**</span><span class="sxs-lookup"><span data-stu-id="b043f-127">**unsigned**</span></span>](unsigned.md)
</dt> </dl>

 

 




