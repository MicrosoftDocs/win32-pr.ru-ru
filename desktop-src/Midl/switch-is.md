---
title: switch_is - атрибут
description: Параметр \ Switch \_ имеет атрибут \ задает выражение или идентификатор, выступающий в качестве discriminant объединения, который выбирает элемент объединения.
ms.assetid: 93552bdf-6a14-47ce-877e-32ed976bb895
keywords:
- switch_is атрибута MIDL
topic_type:
- apiref
api_name:
- switch_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c52661c4fa1ebce57011f4424901dd1ec18250f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103986982"
---
# <a name="switch_is-attribute"></a><span data-ttu-id="63387-104">параметр \_ имеет атрибут</span><span class="sxs-lookup"><span data-stu-id="63387-104">switch\_is attribute</span></span>

<span data-ttu-id="63387-105">**\[ \_ Параметр \]** Attribute указывает выражение или идентификатор, выступающий в качестве discriminant объединения, который выбирает элемент объединения.</span><span class="sxs-lookup"><span data-stu-id="63387-105">The **\[switch\_is\]** attribute specifies the expression or identifier acting as the union discriminant that selects the union member.</span></span>

``` syntax
typedef struct [[ struct-tag ]] 
{
    [ switch_is(limited-expr) [[ , field-attr-list ]] ] union-type-specifier declarator;
    ...
}

[[ [function-attribute-list] ]] type-specifier [[pointer-declarator]] function-name(
    [ switch_is(limited-expr) [[ , param-attr-list ]] ] union-type [[declarator]]
    , ...);
```

## <a name="parameters"></a><span data-ttu-id="63387-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="63387-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63387-107">*Тег struct*</span><span class="sxs-lookup"><span data-stu-id="63387-107">*struct-tag*</span></span> 
</dt> <dd>

<span data-ttu-id="63387-108">Указывает необязательный тег для структуры.</span><span class="sxs-lookup"><span data-stu-id="63387-108">Specifies an optional tag for a structure.</span></span>

</dd> <dt>

<span data-ttu-id="63387-109">*Limited-expr*</span><span class="sxs-lookup"><span data-stu-id="63387-109">*limited-expr*</span></span> 
</dt> <dd>

<span data-ttu-id="63387-110">Указывает выражение языка C, поддерживаемое MIDL.</span><span class="sxs-lookup"><span data-stu-id="63387-110">Specifies a C-language expression supported by MIDL.</span></span> <span data-ttu-id="63387-111">Поддерживаются почти все выражения языка C.</span><span class="sxs-lookup"><span data-stu-id="63387-111">Almost all C-language expressions are supported.</span></span> <span data-ttu-id="63387-112">Компилятор MIDL поддерживает условные выражения, логические выражения, реляционные выражения и арифметические выражения.</span><span class="sxs-lookup"><span data-stu-id="63387-112">The MIDL compiler supports conditional expressions, logical expressions, relational expressions, and arithmetic expressions.</span></span> <span data-ttu-id="63387-113">MIDL не разрешает вызовы функций в выражениях и не допускает операторы pre и POST и до и после приращения.</span><span class="sxs-lookup"><span data-stu-id="63387-113">MIDL does not allow function invocations in expressions and does not allow pre- and post-increment and pre- and post-decrement operators.</span></span>

</dd> <dt>

<span data-ttu-id="63387-114">*поле-attr-список*</span><span class="sxs-lookup"><span data-stu-id="63387-114">*field-attr-list*</span></span> 
</dt> <dd>

<span data-ttu-id="63387-115">Указывает ноль или более атрибутов полей, применимых к элементу объединения.</span><span class="sxs-lookup"><span data-stu-id="63387-115">Specifies zero or more field attributes that apply to a union member.</span></span> <span data-ttu-id="63387-116">К допустимым атрибутам полей относятся: **\[** [**First \_**](first-is.md)—, **\]** **\[** [**Last \_ —**](last-is.md), **\]** **\[** [**length \_ —**](length-is.md) **\]** , **\[** [**Max \_ —**](max-is.md) **\]** , **\[** [**size \_ —**](size-is.md), **\]** String атрибуты использования **\[** [](string.md) **\]** , **\[** [**Ignore**](ignore.md) **\]** и **\[** [**Контекстный \_ маркер**](context-handle.md) **\]** ; атрибут указателя **\[** [**ref**](ref.md) **\]** , **\[** [**UNIQUE**](unique.md) **\]** или **\[** [**ptr**](ptr.md), **\]** а также для членов, которые сами являются членами, **\[** [**\_ Тип переключателя**](switch-type.md)атрибута объединения **\]** .</span><span class="sxs-lookup"><span data-stu-id="63387-116">Valid field attributes include **\[**[**first\_is**](first-is.md)**\]**, **\[**[**last\_is**](last-is.md)**\]**, **\[**[**length\_is**](length-is.md)**\]**, **\[**[**max\_is**](max-is.md)**\]**, **\[**[**size\_is**](size-is.md)**\]**; the usage attributes **\[**[**string**](string.md)**\]**, **\[**[**ignore**](ignore.md)**\]**, and **\[**[**context\_handle**](context-handle.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and for members that are themselves unions, the union attribute **\[**[**switch\_type**](switch-type.md)**\]**.</span></span> <span data-ttu-id="63387-117">Несколько атрибутов полей разделяются запятыми.</span><span class="sxs-lookup"><span data-stu-id="63387-117">Separate multiple field attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="63387-118">*спецификатор Union-Type*</span><span class="sxs-lookup"><span data-stu-id="63387-118">*union-type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="63387-119">Указывает идентификатор типа [**объединения**](union.md) .</span><span class="sxs-lookup"><span data-stu-id="63387-119">Specifies the [**union**](union.md) type identifier.</span></span> <span data-ttu-id="63387-120">Дополнительная спецификация хранилища может предшествовать *спецификатору типа*.</span><span class="sxs-lookup"><span data-stu-id="63387-120">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="63387-121">*декларатор и декларатор-список*</span><span class="sxs-lookup"><span data-stu-id="63387-121">*declarator and declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="63387-122">Задает стандартный декларатор C, например идентификатор, декларатор указателя и декларатор массива.</span><span class="sxs-lookup"><span data-stu-id="63387-122">Specifies a standard C declarator, such as an identifier, pointer declarator, and array declarator.</span></span> <span data-ttu-id="63387-123">(Деклараторы функций и объявления битовых полей не допускаются в объединениях, передаваемых в удаленных вызовах процедур.</span><span class="sxs-lookup"><span data-stu-id="63387-123">(Function declarators and bit-field declarations are not allowed in unions that are transmitted in remote procedure calls.</span></span> <span data-ttu-id="63387-124">Эти деклараторы разрешены в объединениях, которые не передаются.) Несколько деклараторов разделяются запятыми.</span><span class="sxs-lookup"><span data-stu-id="63387-124">These declarators are allowed in unions that are not transmitted.) Separate multiple declarators with commas.</span></span>

</dd> <dt>

<span data-ttu-id="63387-125">*Function-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="63387-125">*function-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="63387-126">Указывает ноль или более атрибутов, которые применяются к функции.</span><span class="sxs-lookup"><span data-stu-id="63387-126">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="63387-127">Допустимые атрибуты функции — **\[** [**обратный вызов**](callback.md) **\]** , **\[** [**локальный**](local.md) **\]** объект, атрибут указателя **\[ \] ref**, **\[ Unique \]** или **\[ ptr \]**; и атрибуты использования **\[ строка \]**, **\[ Ignore \]** и **\[ Контекстный \_ маркер \]**.</span><span class="sxs-lookup"><span data-stu-id="63387-127">Valid function attributes are **\[**[**callback**](callback.md)**\]**, **\[**[**local**](local.md)**\]**; the pointer attribute **\[ref\]**, **\[unique\]**, or **\[ptr\]**; and the usage attributes **\[string\]**, **\[ignore\]**, and **\[context\_handle\]**.</span></span>

</dd> <dt>

<span data-ttu-id="63387-128">*Описатель типа*</span><span class="sxs-lookup"><span data-stu-id="63387-128">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="63387-129">Задает [базовый тип](midl-base-types.md), [**структуру**](struct.md), [**объединение**](union.md), тип [**перечисления**](enum.md) или идентификатор типа.</span><span class="sxs-lookup"><span data-stu-id="63387-129">Specifies a [base type](midl-base-types.md), [**struct**](struct.md), [**union**](union.md), [**enum**](enum.md) type, or type identifier.</span></span> <span data-ttu-id="63387-130">Дополнительная спецификация хранилища может предшествовать *спецификатору типа*.</span><span class="sxs-lookup"><span data-stu-id="63387-130">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="63387-131">*декларатор указателя*</span><span class="sxs-lookup"><span data-stu-id="63387-131">*pointer-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="63387-132">Указывает ноль или несколько деклараторов указателей.</span><span class="sxs-lookup"><span data-stu-id="63387-132">Specifies zero or more pointer declarators.</span></span> <span data-ttu-id="63387-133">Декларатор указателя аналогичен декларатору указателя, используемому в C; Он создается из \* указателя, модификаторов, таких как **FAR**, и квалификатора [**const**](const.md).</span><span class="sxs-lookup"><span data-stu-id="63387-133">A pointer declarator is the same as the pointer declarator used in C; it is constructed from the \* designator, modifiers such as **far**, and the qualifier [**const**](const.md).</span></span>

</dd> <dt>

<span data-ttu-id="63387-134">*имя функции*</span><span class="sxs-lookup"><span data-stu-id="63387-134">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="63387-135">Задает имя удаленной процедуры.</span><span class="sxs-lookup"><span data-stu-id="63387-135">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="63387-136">*Param-attr-список*</span><span class="sxs-lookup"><span data-stu-id="63387-136">*param-attr-list*</span></span> 
</dt> <dd>

<span data-ttu-id="63387-137">Указывает ноль или более атрибутов, подходящих для указанного типа параметра.</span><span class="sxs-lookup"><span data-stu-id="63387-137">Specifies zero or more attributes appropriate for the specified parameter type.</span></span> <span data-ttu-id="63387-138">Атрибуты параметров могут **\[ \]** принимать и исключать **\[ атрибуты \]** направления, атрибуты полей **\[ \_ \] —**, **\[ Last \_ — \]**, **\[ length \_ — \]**, **\[ Max \_ — \]**, **\[ size \_ — \]** и **\[ \_ тип \] переключателя**; атрибут указателя **\[ ref \]**, **\[ Unique \]** или **\[ ptr \]**, а также **\[ \_ маркер \] контекста** атрибутов использования и **\[ строка \]**.</span><span class="sxs-lookup"><span data-stu-id="63387-138">Parameter attributes can take the directional attributes **\[in\]** and **\[out\]**, the field attributes **\[first\_is\]**, **\[last\_is\]**, **\[length\_is\]**, **\[max\_is\]**, **\[size\_is\]**, and **\[switch\_type\]**; the pointer attribute **\[ref\]**, **\[unique\]**, or **\[ptr\]**; and the usage attributes **\[context\_handle\]** and **\[string\]**.</span></span> <span data-ttu-id="63387-139">Атрибут использования **\[ Ignore \]** не может использоваться в качестве атрибута параметра.</span><span class="sxs-lookup"><span data-stu-id="63387-139">The usage attribute **\[ignore\]** cannot be used as a parameter attribute.</span></span> <span data-ttu-id="63387-140">Несколько атрибутов разделяются запятыми.</span><span class="sxs-lookup"><span data-stu-id="63387-140">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="63387-141">*Тип объединения*</span><span class="sxs-lookup"><span data-stu-id="63387-141">*union-type*</span></span> 
</dt> <dd>

<span data-ttu-id="63387-142">Определяет спецификатор типа [**объединения**](union.md) .</span><span class="sxs-lookup"><span data-stu-id="63387-142">Identifies the [**union**](union.md) type specifier.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="63387-143">Комментарии</span><span class="sxs-lookup"><span data-stu-id="63387-143">Remarks</span></span>

<span data-ttu-id="63387-144">Discriminant, связанный с **\[ параметром \_ \]** , должен быть определен на том же логическом уровне, что и объединение:</span><span class="sxs-lookup"><span data-stu-id="63387-144">The discriminant associated with the **\[switch\_is\]** attribute must be defined at the same logical level as the union:</span></span>

-   <span data-ttu-id="63387-145">Если Union является параметром, discriminant объединения должен быть другим параметром.</span><span class="sxs-lookup"><span data-stu-id="63387-145">When the union is a parameter, the union discriminant must be another parameter.</span></span>
-   <span data-ttu-id="63387-146">Если объединение является полем структуры, discriminant должно быть другим полем той же структуры.</span><span class="sxs-lookup"><span data-stu-id="63387-146">When the union is a field of a structure, the discriminant must be another field of the same structure.</span></span>

<span data-ttu-id="63387-147">Последовательность в структуре или списке параметров функции не имеет значения.</span><span class="sxs-lookup"><span data-stu-id="63387-147">The sequence in a structure or a function parameter list is not significant.</span></span> <span data-ttu-id="63387-148">Объединение может предшествовать discriminant или следовать за ним.</span><span class="sxs-lookup"><span data-stu-id="63387-148">The union can either precede or follow the discriminant.</span></span>

<span data-ttu-id="63387-149">Атрибут **\[ \_ Switch \]** может использоваться в качестве атрибута поля или в качестве атрибута параметра.</span><span class="sxs-lookup"><span data-stu-id="63387-149">The **\[switch\_is\]** attribute can appear as a field attribute or as a parameter attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="63387-150">Примеры</span><span class="sxs-lookup"><span data-stu-id="63387-150">Examples</span></span>

``` syntax
typedef [switch_type(short)] union _WILLIE_UNION_TYPE 
{ 
    [case(24)] 
        float fMays; 
    [case(25)] 
        double dMcCovey; 
    [default] 
        ; 
} WILLIE_UNION_TYPE; 
 
typedef struct _WINNER_TYPE 
{ 
    [switch_is(sUniformNumber)] WILLIE_UNION_TYPE w; 
    short sUniformNumber; 
} WINNER_TYPE;
```

## <a name="see-also"></a><span data-ttu-id="63387-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="63387-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63387-152">Базовые типы MIDL</span><span class="sxs-lookup"><span data-stu-id="63387-152">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="63387-153">**обратный вызов**</span><span class="sxs-lookup"><span data-stu-id="63387-153">**callback**</span></span>](callback.md)
</dt> <dt>

[<span data-ttu-id="63387-154">**const**</span><span class="sxs-lookup"><span data-stu-id="63387-154">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="63387-155">**Контекстный \_ маркер**</span><span class="sxs-lookup"><span data-stu-id="63387-155">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="63387-156">Инкапсулированные объединения</span><span class="sxs-lookup"><span data-stu-id="63387-156">Encapsulated Unions</span></span>](encapsulated-unions.md)
</dt> <dt>

[<span data-ttu-id="63387-157">**перечисления**</span><span class="sxs-lookup"><span data-stu-id="63387-157">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="63387-158">**первый \_ —**</span><span class="sxs-lookup"><span data-stu-id="63387-158">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="63387-159">**обращать**</span><span class="sxs-lookup"><span data-stu-id="63387-159">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="63387-160">**Последний \_ —**</span><span class="sxs-lookup"><span data-stu-id="63387-160">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="63387-161">**Длина \_ равна**</span><span class="sxs-lookup"><span data-stu-id="63387-161">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="63387-162">**Языковые**</span><span class="sxs-lookup"><span data-stu-id="63387-162">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="63387-163">**Максимальное \_ число**</span><span class="sxs-lookup"><span data-stu-id="63387-163">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="63387-164">Неинкапсулированные объединения</span><span class="sxs-lookup"><span data-stu-id="63387-164">Nonencapsulated Unions</span></span>](nonencapsulated-unions.md)
</dt> <dt>

[<span data-ttu-id="63387-165">**ptr**</span><span class="sxs-lookup"><span data-stu-id="63387-165">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="63387-166">**ref**</span><span class="sxs-lookup"><span data-stu-id="63387-166">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="63387-167">**размер \_ равен**</span><span class="sxs-lookup"><span data-stu-id="63387-167">**size\_is**</span></span>](size-is.md)
</dt> <dt>

[<span data-ttu-id="63387-168">**Строка**</span><span class="sxs-lookup"><span data-stu-id="63387-168">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="63387-169">**struct**</span><span class="sxs-lookup"><span data-stu-id="63387-169">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="63387-170">**Тип коммутатора \_**</span><span class="sxs-lookup"><span data-stu-id="63387-170">**switch\_type**</span></span>](switch-type.md)
</dt> <dt>

[<span data-ttu-id="63387-171">**наборов**</span><span class="sxs-lookup"><span data-stu-id="63387-171">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="63387-172">**однозначно**</span><span class="sxs-lookup"><span data-stu-id="63387-172">**unique**</span></span>](unique.md)
</dt> </dl>

 

 




