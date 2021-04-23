---
title: ref - атрибут
description: Атрибут \ ref \ определяет указатель ссылки. Он используется просто для представления уровня косвенного обращения.
ms.assetid: db4ff938-0f38-4f77-bb65-f728ffd609e0
keywords:
- ref Attribute, MIDL
topic_type:
- apiref
api_name:
- ref
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82bc5762eea78b3ce73ab3db58e9bb567b051675
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103890505"
---
# <a name="ref-attribute"></a><span data-ttu-id="a48a8-105">ref - атрибут</span><span class="sxs-lookup"><span data-stu-id="a48a8-105">ref attribute</span></span>

<span data-ttu-id="a48a8-106">Атрибут **\[ ref \]** определяет указатель ссылки.</span><span class="sxs-lookup"><span data-stu-id="a48a8-106">The **\[ref\]** attribute identifies a reference pointer.</span></span> <span data-ttu-id="a48a8-107">Он используется просто для представления уровня косвенного обращения.</span><span class="sxs-lookup"><span data-stu-id="a48a8-107">It is used simply to represent a level of indirection.</span></span>

``` syntax
pointer_default(ref)

typedef [ ref [[ , type-attribute-list ]] ] type-specifier declarator-list; 

typedef [ struct | union ] 
{
    [ ref [[ , field-attribute-list ]] ] type-specifier declarator-list;
    ...}

[[ [ function-attribute-list ] ]] type-specifier [[ptr-decl]] function-name(
    [ ref [[ , parameter-attribute-list ]] ] type-specifier [[standard-declarator]]
    , ...);
```

## <a name="parameters"></a><span data-ttu-id="a48a8-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a48a8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a48a8-109">*Type-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="a48a8-109">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="a48a8-110">Указывает один или несколько атрибутов, применяемых к типу.</span><span class="sxs-lookup"><span data-stu-id="a48a8-110">Specifies one or more attributes that apply to the type.</span></span> <span data-ttu-id="a48a8-111">К допустимым атрибутам типа относятся **\[** [**Handle**](handle.md), **\]** **\[** [**Switch \_ Type**](switch-type.md) **\]** , **\[** [**передает \_ as**](transmit-as.md) **\]** ; атрибуты указателя **\[ \] ref**, **\[** [**UNIQUE**](unique.md) **\]** или **\[** [**ptr**](ptr.md) **\]** ;, а также **\[** [**\_ маркер контекста**](context-handle.md)атрибутов использования **\]** , **\[** [**String**](string.md) **\]** и **\[** [**Ignore**](ignore.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="a48a8-111">Valid type attributes include **\[**[**handle**](handle.md)**\]**, **\[**[**switch\_type**](switch-type.md)**\]**, **\[**[**transmit\_as**](transmit-as.md)**\]**; the pointer attributes **\[ref\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**context\_handle**](context-handle.md)**\]**, **\[**[**string**](string.md)**\]**, and **\[**[**ignore**](ignore.md)**\]**.</span></span> <span data-ttu-id="a48a8-112">Несколько атрибутов разделяются запятыми.</span><span class="sxs-lookup"><span data-stu-id="a48a8-112">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="a48a8-113">*Описатель типа*</span><span class="sxs-lookup"><span data-stu-id="a48a8-113">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="a48a8-114">Задает [базовый тип](midl-base-types.md), [**структуру**](struct.md), [**объединение**](union.md)или тип [**перечисления**](enum.md) или идентификатор типа.</span><span class="sxs-lookup"><span data-stu-id="a48a8-114">Specifies a [base type](midl-base-types.md), [**struct**](struct.md), [**union**](union.md), or [**enum**](enum.md) type or type identifier.</span></span> <span data-ttu-id="a48a8-115">Дополнительная спецификация хранилища может предшествовать *спецификатору типа*.</span><span class="sxs-lookup"><span data-stu-id="a48a8-115">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="a48a8-116">*стандартные-деклараторы*</span><span class="sxs-lookup"><span data-stu-id="a48a8-116">*standard-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="a48a8-117">Задает стандартный декларатор C, например идентификатор, декларатор указателя или декларатор массива.</span><span class="sxs-lookup"><span data-stu-id="a48a8-117">Specifies a standard C declarator, such as an identifier, a pointer declarator, or an array declarator.</span></span> <span data-ttu-id="a48a8-118">Дополнительные сведения см. в разделе [атрибуты Array и Sized-Pointer](array-and-sized-pointer-attributes.md), [**массивы**](arrays-1.md), [массивы и указатели](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="a48a8-118">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span>

</dd> <dt>

<span data-ttu-id="a48a8-119">*декларатор-список*</span><span class="sxs-lookup"><span data-stu-id="a48a8-119">*declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="a48a8-120">Задает стандартные деклараторы C, такие как идентификаторы, деклараторы указателей и деклараторы массивов.</span><span class="sxs-lookup"><span data-stu-id="a48a8-120">Specifies standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="a48a8-121">Дополнительные сведения см. в разделе [атрибуты Array и Sized-Pointer](array-and-sized-pointer-attributes.md), [**массивы**](arrays-1.md), [массивы и указатели](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="a48a8-121">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="a48a8-122">*Список деклараторов* состоит из одного или нескольких деклараторов, разделенных запятыми.</span><span class="sxs-lookup"><span data-stu-id="a48a8-122">The *declarator-list* consists of one or more declarators separated by commas.</span></span> <span data-ttu-id="a48a8-123">Идентификатор параметра-Name в деклараторе функции является необязательным.</span><span class="sxs-lookup"><span data-stu-id="a48a8-123">The parameter-name identifier in the function declarator is optional.</span></span>

</dd> <dt>

<span data-ttu-id="a48a8-124">*Список атрибутов Field*</span><span class="sxs-lookup"><span data-stu-id="a48a8-124">*field-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="a48a8-125">Указывает ноль или более атрибутов полей, применимых к структуре, члену объединения или параметру функции.</span><span class="sxs-lookup"><span data-stu-id="a48a8-125">Specifies zero or more field attributes that apply to the structure, union member, or function parameter.</span></span> <span data-ttu-id="a48a8-126">К допустимым атрибутам полей относятся: **\[** [**First \_**](first-is.md)—, **\]** **\[** [**Last \_ —**](last-is.md), **\]** **\[** [**length \_ —**](length-is.md) **\]** , **\[** [**Max \_ —**](max-is.md) **\]** , **\[** [**size \_ —**](size-is.md), **\]** строка атрибутов использования **\[** [](string.md) **\]** , **\[** [**Ignore**](ignore.md) **\]** и **\[** [**контекст контекста \_**](context-handle.md) **\]** ; атрибут указателя **\[ \] ref**, **\[** [**UNIQUE**](unique.md) **\]** , **\[** [**ptr**](ptr.md), **\]** и **\[** [**\_ Тип переключателя**](switch-type.md)атрибута Union **\]** .</span><span class="sxs-lookup"><span data-stu-id="a48a8-126">Valid field attributes include **\[**[**first\_is**](first-is.md)**\]**, **\[**[**last\_is**](last-is.md)**\]**, **\[**[**length\_is**](length-is.md)**\]**, **\[**[**max\_is**](max-is.md)**\]**, **\[**[**size\_is**](size-is.md)**\]**; the usage attributes **\[**[**string**](string.md)**\]**, **\[**[**ignore**](ignore.md)**\]**, and **\[**[**context\_handle**](context-handle.md)**\]**; the pointer attribute **\[ref\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the union attribute **\[**[**switch\_type**](switch-type.md)**\]**.</span></span> <span data-ttu-id="a48a8-127">Несколько атрибутов полей разделяются запятыми.</span><span class="sxs-lookup"><span data-stu-id="a48a8-127">Separate multiple field attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="a48a8-128">*Function-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="a48a8-128">*function-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="a48a8-129">Указывает ноль или более атрибутов, которые применяются к функции.</span><span class="sxs-lookup"><span data-stu-id="a48a8-129">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="a48a8-130">Допустимые атрибуты функции — **\[** [**обратный вызов**](callback.md) **\]** , **\[** [**локальный**](local.md) **\]** объект, атрибут указателя **\[ ref \]**, **\[** [**UNIQUE**](unique.md) **\]** или **\[** [**ptr**](ptr.md) **\]** ; и атрибуты использования **\[** [**строка**](string.md) **\]** , **\[** [**Ignore**](ignore.md) **\]** и **\[** [**Контекстный \_ маркер**](context-handle.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="a48a8-130">Valid function attributes are **\[**[**callback**](callback.md)**\]**, **\[**[**local**](local.md)**\]**; the pointer attribute **\[ref\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**string**](string.md)**\]**, **\[**[**ignore**](ignore.md)**\]**, and **\[**[**context\_handle**](context-handle.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="a48a8-131">*PTR-decl*</span><span class="sxs-lookup"><span data-stu-id="a48a8-131">*ptr-decl*</span></span> 
</dt> <dd>

<span data-ttu-id="a48a8-132">Указывает по крайней мере один декларатор указателя, к которому применяется атрибут **\[ ref \]** .</span><span class="sxs-lookup"><span data-stu-id="a48a8-132">Specifies at least one pointer declarator to which the **\[ref\]** attribute applies.</span></span> <span data-ttu-id="a48a8-133">Декларатор указателя аналогичен декларатору указателя, используемому в C; Он создается из \* указателя, модификаторов, таких как **FAR**, и квалификатора [**const**](const.md).</span><span class="sxs-lookup"><span data-stu-id="a48a8-133">A pointer declarator is the same as the pointer declarator used in C; it is constructed from the \* designator, modifiers such as **far**, and the qualifier [**const**](const.md).</span></span>

</dd> <dt>

<span data-ttu-id="a48a8-134">*имя функции*</span><span class="sxs-lookup"><span data-stu-id="a48a8-134">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="a48a8-135">Задает имя удаленной процедуры.</span><span class="sxs-lookup"><span data-stu-id="a48a8-135">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="a48a8-136">*Parameter-список атрибутов*</span><span class="sxs-lookup"><span data-stu-id="a48a8-136">*parameter-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="a48a8-137">Состоит из нуля или более атрибутов, подходящих для указанного типа параметра.</span><span class="sxs-lookup"><span data-stu-id="a48a8-137">Consists of zero or more attributes appropriate for the specified parameter type.</span></span> <span data-ttu-id="a48a8-138">Атрибуты параметров могут принимать и исключать **\[** [**атрибуты направления**](in.md) **\]** **\[** [](out-idl.md) **\]** . сначала атрибуты полей **\[** [**\_ :**](first-is.md) **\]** , **\[** [**Last \_ -**](last-is.md), **\]** **\[** [**length \_ —**](length-is.md) **\]** , **\[** [**Max \_ —**](max-is.md) **\]** , **\[** [**size \_ —**](size-is.md) **\]** и **\[** [**\_ Тип переключателя**](switch-type.md) **\]** ; атрибут указателя **\[ ref \]**, **\[** [**UNIQUE**](unique.md) **\]** или **\[** [**ptr**](ptr.md), **\]** а также **\[** [**\_ маркер контекста**](context-handle.md) атрибутов использования **\]** и **\[** [**строка**](string.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="a48a8-138">Parameter attributes can take the directional attributes **\[**[**in**](in.md)**\]** and **\[**[**out**](out-idl.md)**\]**; the field attributes **\[**[**first\_is**](first-is.md)**\]**, **\[**[**last\_is**](last-is.md)**\]**, **\[**[**length\_is**](length-is.md)**\]**, **\[**[**max\_is**](max-is.md)**\]**, **\[**[**size\_is**](size-is.md)**\]**, and **\[**[**switch\_type**](switch-type.md)**\]**; the pointer attribute **\[ref\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**context\_handle**](context-handle.md)**\]** and **\[**[**string**](string.md)**\]**.</span></span> <span data-ttu-id="a48a8-139">Атрибут использования **\[** [**Ignore**](ignore.md) **\]** не может использоваться в качестве атрибута параметра.</span><span class="sxs-lookup"><span data-stu-id="a48a8-139">The usage attribute **\[**[**ignore**](ignore.md)**\]** cannot be used as a parameter attribute.</span></span> <span data-ttu-id="a48a8-140">Несколько атрибутов разделяются запятыми.</span><span class="sxs-lookup"><span data-stu-id="a48a8-140">Separate multiple attributes with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a48a8-141">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a48a8-141">Remarks</span></span>

<span data-ttu-id="a48a8-142">Атрибут указателя может быть применен как атрибут типа, как атрибут поля, применяемый к члену структуры, члену объединения или параметру. или в качестве атрибута функции, который применяется к возвращаемому типу функции.</span><span class="sxs-lookup"><span data-stu-id="a48a8-142">A pointer attribute can be applied as a type attribute, as a field attribute that applies to a structure member, union member, or parameter; or as a function attribute that applies to the function return type.</span></span> <span data-ttu-id="a48a8-143">Атрибут указателя также может присутствовать с **\[** ключевым словом [**указателя \_ по умолчанию**](pointer-default.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="a48a8-143">The pointer attribute can also appear with the **\[**[**pointer\_default**](pointer-default.md)**\]** keyword.</span></span>

<span data-ttu-id="a48a8-144">Ссылочный указатель имеет следующие характеристики.</span><span class="sxs-lookup"><span data-stu-id="a48a8-144">A reference pointer has the following characteristics:</span></span>

-   <span data-ttu-id="a48a8-145">Всегда указывает на допустимое хранилище; никогда не имеет значения **null**.</span><span class="sxs-lookup"><span data-stu-id="a48a8-145">Always points to valid storage; never has the value **NULL**.</span></span> <span data-ttu-id="a48a8-146">Указатель ссылки всегда может быть разыменован.</span><span class="sxs-lookup"><span data-stu-id="a48a8-146">A reference pointer can always be dereferenced.</span></span>
-   <span data-ttu-id="a48a8-147">Никогда не изменяются во время вызова.</span><span class="sxs-lookup"><span data-stu-id="a48a8-147">Never changes during a call.</span></span> <span data-ttu-id="a48a8-148">Указатель ссылки всегда указывает на то же хранилище на клиенте до и после вызова.</span><span class="sxs-lookup"><span data-stu-id="a48a8-148">A reference pointer always points to the same storage on the client before and after the call.</span></span>
-   <span data-ttu-id="a48a8-149">Не выделяет новую память на клиенте.</span><span class="sxs-lookup"><span data-stu-id="a48a8-149">Does not allocate new memory on the client.</span></span> <span data-ttu-id="a48a8-150">Данные, возвращаемые с сервера, записываются в существующее хранилище, указанное значением указателя ссылки перед вызовом.</span><span class="sxs-lookup"><span data-stu-id="a48a8-150">Data returned from the server is written into existing storage specified by the value of the reference pointer before the call.</span></span>
-   <span data-ttu-id="a48a8-151">Не вызывает присвоение псевдонимов.</span><span class="sxs-lookup"><span data-stu-id="a48a8-151">Does not cause aliasing.</span></span> <span data-ttu-id="a48a8-152">К хранилищу, на которое указывает указатель ссылки, нельзя обратиться с любого другого имени в функции.</span><span class="sxs-lookup"><span data-stu-id="a48a8-152">Storage pointed to by a reference pointer cannot be reached from any other name in the function.</span></span>

<span data-ttu-id="a48a8-153">Указатель ссылки не может использоваться в качестве типа указателя, возвращаемого функцией.</span><span class="sxs-lookup"><span data-stu-id="a48a8-153">A reference pointer cannot be used as the type of a pointer returned by a function.</span></span>

<span data-ttu-id="a48a8-154">Если для параметра указателя верхнего уровня не задан атрибут, он рассматривается как указатель ссылки.</span><span class="sxs-lookup"><span data-stu-id="a48a8-154">If no attribute is specified for a top-level pointer parameter, it is treated as a reference pointer.</span></span>

## <a name="examples"></a><span data-ttu-id="a48a8-155">Примеры</span><span class="sxs-lookup"><span data-stu-id="a48a8-155">Examples</span></span>

``` syntax
[unique] char * GetFirstName( 
    [in, ref] char * pszFullName);
```

## <a name="see-also"></a><span data-ttu-id="a48a8-156">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a48a8-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a48a8-157">**массивы**</span><span class="sxs-lookup"><span data-stu-id="a48a8-157">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="a48a8-158">Массивы и указатели</span><span class="sxs-lookup"><span data-stu-id="a48a8-158">Arrays and Pointers</span></span>](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[<span data-ttu-id="a48a8-159">Атрибуты массива и Sized-Pointer</span><span class="sxs-lookup"><span data-stu-id="a48a8-159">Array and Sized-Pointer Attributes</span></span>](array-and-sized-pointer-attributes.md)
</dt> <dt>

[<span data-ttu-id="a48a8-160">Базовые типы MIDL</span><span class="sxs-lookup"><span data-stu-id="a48a8-160">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="a48a8-161">**обратный вызов**</span><span class="sxs-lookup"><span data-stu-id="a48a8-161">**callback**</span></span>](callback.md)
</dt> <dt>

[<span data-ttu-id="a48a8-162">**const**</span><span class="sxs-lookup"><span data-stu-id="a48a8-162">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="a48a8-163">**Контекстный \_ маркер**</span><span class="sxs-lookup"><span data-stu-id="a48a8-163">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="a48a8-164">**перечисления**</span><span class="sxs-lookup"><span data-stu-id="a48a8-164">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="a48a8-165">**первый \_ —**</span><span class="sxs-lookup"><span data-stu-id="a48a8-165">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="a48a8-166">**справиться**</span><span class="sxs-lookup"><span data-stu-id="a48a8-166">**handle**</span></span>](handle.md)
</dt> <dt>

[<span data-ttu-id="a48a8-167">**обращать**</span><span class="sxs-lookup"><span data-stu-id="a48a8-167">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="a48a8-168">**Последний \_ —**</span><span class="sxs-lookup"><span data-stu-id="a48a8-168">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="a48a8-169">**Длина \_ равна**</span><span class="sxs-lookup"><span data-stu-id="a48a8-169">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="a48a8-170">**Языковые**</span><span class="sxs-lookup"><span data-stu-id="a48a8-170">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="a48a8-171">**Максимальное \_ число**</span><span class="sxs-lookup"><span data-stu-id="a48a8-171">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="a48a8-172">**заполняет**</span><span class="sxs-lookup"><span data-stu-id="a48a8-172">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="a48a8-173">**ptr**</span><span class="sxs-lookup"><span data-stu-id="a48a8-173">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="a48a8-174">**размер \_ равен**</span><span class="sxs-lookup"><span data-stu-id="a48a8-174">**size\_is**</span></span>](size-is.md)
</dt> <dt>

[<span data-ttu-id="a48a8-175">**Строка**</span><span class="sxs-lookup"><span data-stu-id="a48a8-175">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="a48a8-176">**struct**</span><span class="sxs-lookup"><span data-stu-id="a48a8-176">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="a48a8-177">**Тип коммутатора \_**</span><span class="sxs-lookup"><span data-stu-id="a48a8-177">**switch\_type**</span></span>](switch-type.md)
</dt> <dt>

[<span data-ttu-id="a48a8-178">**передать \_ как**</span><span class="sxs-lookup"><span data-stu-id="a48a8-178">**transmit\_as**</span></span>](transmit-as.md)
</dt> <dt>

[<span data-ttu-id="a48a8-179">**наборов**</span><span class="sxs-lookup"><span data-stu-id="a48a8-179">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="a48a8-180">**однозначно**</span><span class="sxs-lookup"><span data-stu-id="a48a8-180">**unique**</span></span>](unique.md)
</dt> </dl>

 

 