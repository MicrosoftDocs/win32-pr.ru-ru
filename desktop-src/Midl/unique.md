---
title: unique - атрибут
description: Атрибут \ Unique \ задает уникальный указатель.
ms.assetid: 0d668148-e65a-478f-9e47-2528d3caa84c
keywords:
- уникальный атрибут MIDL
topic_type:
- apiref
api_name:
- unique
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95b839a2abdd546842ef0d33d45a31428af840f7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105661687"
---
# <a name="unique-attribute"></a><span data-ttu-id="58464-104">unique - атрибут</span><span class="sxs-lookup"><span data-stu-id="58464-104">unique attribute</span></span>

<span data-ttu-id="58464-105">Атрибут **\[ Unique \]** задает уникальный указатель.</span><span class="sxs-lookup"><span data-stu-id="58464-105">The **\[unique\]** attribute specifies a unique pointer.</span></span>

``` syntax
pointer_default(unique)

typedef [ unique [[ , type-attribute-list ]] ] type-specifier declarator-list; 

typedef struct-or-union-declarator 
{
    [ unique [[ , field-attribute-list ]] ] type-specifier declarator-list;
    ...}

[ unique [[ , function-attribute-list ]] ] type-specifier ptr-decl function-name(
    [[ [ parameter-attribute-list ] ]] type-specifier [[declarator]]
    , ...);

[[ [ function-attribute-list ] ]] type-specifier [[ptr-decl]] function-name(
    [ unique [[ , parameter-attribute-list ]] ] type-specifier [[declarator]]
    , ...);
```

## <a name="parameters"></a><span data-ttu-id="58464-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="58464-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58464-107">*Type-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="58464-107">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="58464-108">Указывает один или несколько атрибутов, применяемых к типу.</span><span class="sxs-lookup"><span data-stu-id="58464-108">Specifies one or more attributes that apply to the type.</span></span> <span data-ttu-id="58464-109">К допустимым атрибутам типа относятся **\[** [**Handle**](handle.md), **\]** **\[** [**Switch \_ Type**](switch-type.md) **\]** , **\[** [**передает \_ as**](transmit-as.md) **\]** ; атрибут указателя **\[** [**ref**](ref.md) **\]** , **\[ Unique \]** или **\[** [**ptr**](ptr.md) **\]** ;, а также **\[** [**\_ маркер контекста**](context-handle.md)атрибутов использования **\]** , **\[** [**String**](string.md) **\]** и **\[** [**Ignore**](ignore.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="58464-109">Valid type attributes include **\[**[**handle**](handle.md)**\]**, **\[**[**switch\_type**](switch-type.md)**\]**, **\[**[**transmit\_as**](transmit-as.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[unique\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**context\_handle**](context-handle.md)**\]**, **\[**[**string**](string.md)**\]**, and **\[**[**ignore**](ignore.md)**\]**.</span></span> <span data-ttu-id="58464-110">Несколько атрибутов разделяются запятыми.</span><span class="sxs-lookup"><span data-stu-id="58464-110">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="58464-111">*Описатель типа*</span><span class="sxs-lookup"><span data-stu-id="58464-111">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="58464-112">Задает [базовый тип](midl-base-types.md), [**структуру**](struct.md), [**объединение**](union.md), тип [**перечисления**](enum.md) или идентификатор типа.</span><span class="sxs-lookup"><span data-stu-id="58464-112">Specifies a [base type](midl-base-types.md), [**struct**](struct.md), [**union**](union.md), [**enum**](enum.md) type, or type identifier.</span></span> <span data-ttu-id="58464-113">Дополнительная спецификация хранилища может предшествовать *спецификатору типа*.</span><span class="sxs-lookup"><span data-stu-id="58464-113">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="58464-114">*декларатор и декларатор-список*</span><span class="sxs-lookup"><span data-stu-id="58464-114">*declarator and declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="58464-115">Задает стандартные деклараторы C, такие как идентификаторы, деклараторы указателей и деклараторы массивов.</span><span class="sxs-lookup"><span data-stu-id="58464-115">Specifies standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="58464-116">Дополнительные сведения см. в разделе [атрибуты Array и Sized-Pointer](array-and-sized-pointer-attributes.md), [**массивы**](arrays-1.md). и [массивы и указатели](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="58464-116">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md)., and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="58464-117">*Список деклараторов* состоит из одного или нескольких деклараторов, разделенных запятыми.</span><span class="sxs-lookup"><span data-stu-id="58464-117">The *declarator-list* consists of one or more declarators separated by commas.</span></span> <span data-ttu-id="58464-118">Идентификатор параметра-Name в деклараторе функции является необязательным.</span><span class="sxs-lookup"><span data-stu-id="58464-118">The parameter-name identifier in the function declarator is optional.</span></span>

</dd> <dt>

<span data-ttu-id="58464-119">*декларатор структуры или объединения*</span><span class="sxs-lookup"><span data-stu-id="58464-119">*struct-or-union-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="58464-120">Задает объявление [**структуры**](struct.md) MIDL или [**объединения**](union.md) .</span><span class="sxs-lookup"><span data-stu-id="58464-120">Specifies a MIDL [**struct**](struct.md) or [**union**](union.md) declarator.</span></span>

</dd> <dt>

<span data-ttu-id="58464-121">*Список атрибутов Field*</span><span class="sxs-lookup"><span data-stu-id="58464-121">*field-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="58464-122">Указывает ноль или более атрибутов полей, применимых к члену структуры, члену объединения или параметру функции.</span><span class="sxs-lookup"><span data-stu-id="58464-122">Specifies zero or more field attributes that apply to the structure member, union member, or function parameter.</span></span> <span data-ttu-id="58464-123">К допустимым атрибутам полей относятся: **\[** [**First \_**](first-is.md)—, **\]** **\[** [**Last \_ —**](last-is.md), **\]** **\[** [**length \_ —**](length-is.md) **\]** , **\[** [**\_**](max-is.md) **\]** **\[** [**\_**](size-is.md) **\]** **\[ \]** **\[ \]** **\[ \]** **\[ \]** **\[ \]** **\[ \_ Max —, Size —, строка атрибутов использования, Ignore и контекст контекста; атрибут указателя ref, Unique, PTR, и тип переключателя атрибута Union. \]** **\[ \_ \]**</span><span class="sxs-lookup"><span data-stu-id="58464-123">Valid field attributes include **\[**[**first\_is**](first-is.md)**\]**, **\[**[**last\_is**](last-is.md)**\]**, **\[**[**length\_is**](length-is.md)**\]**, **\[**[**max\_is**](max-is.md)**\]**, **\[**[**size\_is**](size-is.md)**\]**; the usage attributes **\[string\]**, **\[ignore\]**, and **\[context\_handle\]**; the pointer attribute **\[ref\]**, **\[unique\]**, or **\[ptr\]**; and the union attribute **\[switch\_type\]**.</span></span> <span data-ttu-id="58464-124">Несколько атрибутов полей разделяются запятыми.</span><span class="sxs-lookup"><span data-stu-id="58464-124">Separate multiple field attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="58464-125">*Function-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="58464-125">*function-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="58464-126">Указывает ноль или более атрибутов, которые применяются к функции.</span><span class="sxs-lookup"><span data-stu-id="58464-126">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="58464-127">Допустимые атрибуты функции — **\[** [**обратный вызов**](callback.md) **\]** , **\[** [**локальный**](local.md) **\]** объект, атрибут указателя **\[ \] ref**, **\[ Unique \]** или **\[ ptr \]**; и атрибуты использования **\[ строка \]**, **\[ Ignore \]** и **\[ Контекстный \_ маркер \]**.</span><span class="sxs-lookup"><span data-stu-id="58464-127">Valid function attributes are **\[**[**callback**](callback.md)**\]**, **\[**[**local**](local.md)**\]**; the pointer attribute **\[ref\]**, **\[unique\]**, or **\[ptr\]**; and the usage attributes **\[string\]**, **\[ignore\]**, and **\[context\_handle\]**.</span></span>

</dd> <dt>

<span data-ttu-id="58464-128">*PTR-decl*</span><span class="sxs-lookup"><span data-stu-id="58464-128">*ptr-decl*</span></span> 
</dt> <dd>

<span data-ttu-id="58464-129">Указывает по крайней мере один декларатор указателя, к которому применяется **\[ уникальный \]** атрибут.</span><span class="sxs-lookup"><span data-stu-id="58464-129">Specifies at least one pointer declarator to which the **\[unique\]** attribute applies.</span></span> <span data-ttu-id="58464-130">Декларатор указателя аналогичен декларатору указателя, используемому в C; Он создается из \* указателя, модификаторов, таких как **FAR**, и квалификатора [**const**](const.md).</span><span class="sxs-lookup"><span data-stu-id="58464-130">A pointer declarator is the same as the pointer declarator used in C; it is constructed from the \* designator, modifiers such as **far**, and the qualifier [**const**](const.md).</span></span>

</dd> <dt>

<span data-ttu-id="58464-131">*имя функции*</span><span class="sxs-lookup"><span data-stu-id="58464-131">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="58464-132">Задает имя удаленной процедуры.</span><span class="sxs-lookup"><span data-stu-id="58464-132">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="58464-133">*Parameter-список атрибутов*</span><span class="sxs-lookup"><span data-stu-id="58464-133">*parameter-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="58464-134">Состоит из нуля или более атрибутов, подходящих для указанного типа параметра.</span><span class="sxs-lookup"><span data-stu-id="58464-134">Consists of zero or more attributes appropriate for the specified parameter type.</span></span> <span data-ttu-id="58464-135">**Атрибуты параметров могут принимать и \[ \]** **\[ \]** исключать атрибуты направления. сначала атрибуты полей **\[ \_ \] :**, **\[ Last \_ \] -**, **\[ length \_ — \]**, **\[ Max \_ — \]**, **\[ size \_ — \]** и **\[ \_ тип \] переключателя**; атрибут указателя **\[ ref \]**, **UNIQUE** или [**ptr**](ptr.md), а также **\[ \_ маркер \] контекста** атрибутов использования и **\[ строка \]**.</span><span class="sxs-lookup"><span data-stu-id="58464-135">Parameter attributes can take the directional attributes **\[in\]** and **\[out\]**; the field attributes **\[first\_is\]**, **\[last\_is\]**, **\[length\_is\]**, **\[max\_is\]**, **\[size\_is\]**, and **\[switch\_type\]**; the pointer attribute **\[ref\]**, **unique**, or [**ptr**](ptr.md); and the usage attributes **\[context\_handle\]** and **\[string\]**.</span></span> <span data-ttu-id="58464-136">Атрибут использования **\[ Ignore \]** не может использоваться в качестве атрибута параметра.</span><span class="sxs-lookup"><span data-stu-id="58464-136">The usage attribute **\[ignore\]** cannot be used as a parameter attribute.</span></span> <span data-ttu-id="58464-137">Несколько атрибутов разделяются запятыми.</span><span class="sxs-lookup"><span data-stu-id="58464-137">Separate multiple attributes with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="58464-138">Комментарии</span><span class="sxs-lookup"><span data-stu-id="58464-138">Remarks</span></span>

<span data-ttu-id="58464-139">Атрибуты указателя можно применять как атрибут типа. в качестве атрибута поля, который применяется к члену структуры, члену объединения или параметру; или в качестве атрибута функции, который применяется к возвращаемому типу функции.</span><span class="sxs-lookup"><span data-stu-id="58464-139">Pointer attributes can be applied as a type attribute; as a field attribute that applies to a structure member, union member, or parameter; or as a function attribute that applies to the function return type.</span></span> <span data-ttu-id="58464-140">Атрибут указателя также может присутствовать с **\[** ключевым словом [**указателя \_ по умолчанию**](pointer-default.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="58464-140">The pointer attribute can also appear with the **\[**[**pointer\_default**](pointer-default.md)**\]** keyword.</span></span>

<span data-ttu-id="58464-141">Уникальный указатель имеет следующие характеристики.</span><span class="sxs-lookup"><span data-stu-id="58464-141">A unique pointer has the following characteristics:</span></span>

-   <span data-ttu-id="58464-142">Может иметь значение **null**.</span><span class="sxs-lookup"><span data-stu-id="58464-142">Can have the value **NULL**.</span></span>
-   <span data-ttu-id="58464-143">Может изменяться при вызове от **null** к значению, отличному от NULL, от **ненулевого** до **null** или от одного **значения,** отличного **от NULL,** к другому.</span><span class="sxs-lookup"><span data-stu-id="58464-143">Can change during a call from **NULL** to non-**NULL**, from non-**NULL** to **NULL**, or from one non-**NULL** value to another.</span></span>
-   <span data-ttu-id="58464-144">Может выделить новую память на клиенте.</span><span class="sxs-lookup"><span data-stu-id="58464-144">Can allocate new memory on the client.</span></span> <span data-ttu-id="58464-145">Когда уникальный указатель меняется со **значения NULL** на **значение**, отличное от NULL, данные, возвращаемые с сервера, записываются в новое хранилище.</span><span class="sxs-lookup"><span data-stu-id="58464-145">When the unique pointer changes from **NULL** to non-**NULL**, data returned from the server is written into new storage.</span></span>
-   <span data-ttu-id="58464-146">Может использовать имеющуюся память на клиенте без выделения новой памяти.</span><span class="sxs-lookup"><span data-stu-id="58464-146">Can use existing memory on the client without allocating new memory.</span></span> <span data-ttu-id="58464-147">Когда уникальный указатель изменяется во время вызова из одного значения, отличного от **null** , на другое, предполагается, что указатель указывает на объект данных того же типа.</span><span class="sxs-lookup"><span data-stu-id="58464-147">When a unique pointer changes during a call from one non-**NULL** value to another, the pointer is assumed to point to a data object of the same type.</span></span> <span data-ttu-id="58464-148">Данные, возвращаемые с сервера, записываются в существующее хранилище, заданное значением уникального указателя перед вызовом.</span><span class="sxs-lookup"><span data-stu-id="58464-148">Data returned from the server is written into existing storage specified by the value of the unique pointer before the call.</span></span>
-   <span data-ttu-id="58464-149">Может иметь потерянную память на клиенте.</span><span class="sxs-lookup"><span data-stu-id="58464-149">Can orphan memory on the client.</span></span> <span data-ttu-id="58464-150">Память, на которую ссылается уникальный указатель, не **равная NULL** , может никогда не освобождаться, если уникальный указатель изменяется на **null** во время вызова, а клиент не имеет другого способа разыменования хранилища.</span><span class="sxs-lookup"><span data-stu-id="58464-150">Memory referenced by a non-**NULL** unique pointer may never be freed if the unique pointer changes to **NULL** during a call and the client does not have another means of dereferencing the storage.</span></span>
-   <span data-ttu-id="58464-151">Не вызывает присвоение псевдонимов.</span><span class="sxs-lookup"><span data-stu-id="58464-151">Does not cause aliasing.</span></span> <span data-ttu-id="58464-152">Как и хранилище, на которое указывает указатель ссылки, хранилище, на которое указывает уникальный указатель, не может быть достигнуто из любого другого имени в функции.</span><span class="sxs-lookup"><span data-stu-id="58464-152">Like storage pointed to by a reference pointer, storage pointed to by a unique pointer cannot be reached from any other name in the function.</span></span>

<span data-ttu-id="58464-153">Заглушки вызывают предоставляемые пользователем функции управления памятью MIDL. пользователь самостоятельно [**\_ \_ выделяет**](/windows/desktop/Rpc/the-midl-user-allocate-function) и MIDL, чтобы выделить и освободить память, необходимую для уникальных указателей и их референтс. [**\_ \_**](/windows/desktop/Rpc/the-midl-user-free-function)</span><span class="sxs-lookup"><span data-stu-id="58464-153">The stubs call the user-supplied memory-management functions [**midl\_user\_allocate**](/windows/desktop/Rpc/the-midl-user-allocate-function) and [**midl\_user\_free**](/windows/desktop/Rpc/the-midl-user-free-function) to allocate and deallocate memory required for unique pointers and their referents.</span></span>

<span data-ttu-id="58464-154">К уникальным указателям применяются следующие ограничения.</span><span class="sxs-lookup"><span data-stu-id="58464-154">The following restrictions apply to unique pointers:</span></span>

-   <span data-ttu-id="58464-155">Атрибут **\[ Unique \]** не может применяться к параметрам обработчика привязки ( [**Handle \_ t**](handle-t.md)) и параметрам обработчика контекста.</span><span class="sxs-lookup"><span data-stu-id="58464-155">The **\[unique\]** attribute cannot be applied to binding-handle parameters ( [**handle\_t**](handle-t.md)) and context-handle parameters.</span></span>
-   <span data-ttu-id="58464-156">Атрибут **\[ Unique \]** не может применяться к **\[** [](out-idl.md) **\]** параметрам указателей верхнего уровня только для выхода **\[ \]** (параметрам, имеющим только атрибут Direction).</span><span class="sxs-lookup"><span data-stu-id="58464-156">The **\[unique\]** attribute cannot be applied to **\[**[**out**](out-idl.md)**\]**-only top-level pointer parameters (parameters that have only the **\[out\]** directional attribute).</span></span>
-   <span data-ttu-id="58464-157">По умолчанию указатели верхнего уровня в списках параметров являются **\[** [**ссылочными**](ref.md) **\]** указателями.</span><span class="sxs-lookup"><span data-stu-id="58464-157">By default, top-level pointers in parameter lists are **\[**[**ref**](ref.md)**\]** pointers.</span></span> <span data-ttu-id="58464-158">Это справедливо, даже если интерфейс указывает **указатель \_ по умолчанию (уникальный)**.</span><span class="sxs-lookup"><span data-stu-id="58464-158">This is true even if the interface specifies **pointer\_default(unique)**.</span></span> <span data-ttu-id="58464-159">Параметры верхнего уровня в списках параметров должны быть указаны с **\[ уникальным \]** атрибутом, который является уникальным указателем.</span><span class="sxs-lookup"><span data-stu-id="58464-159">Top-level parameters in parameter lists must be specified with the **\[unique\]** attribute to be a unique pointer.</span></span>
-   <span data-ttu-id="58464-160">Нельзя использовать уникальные указатели для описания размера массива или ARM-объединения, так как уникальные указатели могут иметь значение **null**.</span><span class="sxs-lookup"><span data-stu-id="58464-160">Unique pointers cannot be used to describe the size of an array or union arm because unique pointers can have the value **NULL**.</span></span> <span data-ttu-id="58464-161">Это ограничение предотвращает возникновение ошибки, которая возникает, если в качестве размера массива используется значение **null** или размер Union-ARM.</span><span class="sxs-lookup"><span data-stu-id="58464-161">This restriction prevents the error that results if a **NULL** value is used as the array size or the union-arm size.</span></span>

## <a name="examples"></a><span data-ttu-id="58464-162">Примеры</span><span class="sxs-lookup"><span data-stu-id="58464-162">Examples</span></span>

``` syntax
pointer_default(unique) 
 
typedef [unique, string] unsigned char * MY_STRING_TYPE; 
 
[unique] char * MyFunction([in, out, unique] long * plNumber);
```

## <a name="see-also"></a><span data-ttu-id="58464-163">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="58464-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58464-164">**массивы**</span><span class="sxs-lookup"><span data-stu-id="58464-164">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="58464-165">Массивы и указатели</span><span class="sxs-lookup"><span data-stu-id="58464-165">Arrays and Pointers</span></span>](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[<span data-ttu-id="58464-166">Атрибуты массива и Sized-Pointer</span><span class="sxs-lookup"><span data-stu-id="58464-166">Array and Sized-Pointer Attributes</span></span>](array-and-sized-pointer-attributes.md)
</dt> <dt>

[<span data-ttu-id="58464-167">Базовые типы MIDL</span><span class="sxs-lookup"><span data-stu-id="58464-167">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="58464-168">**обратный вызов**</span><span class="sxs-lookup"><span data-stu-id="58464-168">**callback**</span></span>](callback.md)
</dt> <dt>

[<span data-ttu-id="58464-169">**const**</span><span class="sxs-lookup"><span data-stu-id="58464-169">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="58464-170">**Контекстный \_ маркер**</span><span class="sxs-lookup"><span data-stu-id="58464-170">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="58464-171">**перечисления**</span><span class="sxs-lookup"><span data-stu-id="58464-171">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="58464-172">**первый \_ —**</span><span class="sxs-lookup"><span data-stu-id="58464-172">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="58464-173">**справиться**</span><span class="sxs-lookup"><span data-stu-id="58464-173">**handle**</span></span>](handle.md)
</dt> <dt>

[<span data-ttu-id="58464-174">**Handle \_ t**</span><span class="sxs-lookup"><span data-stu-id="58464-174">**handle\_t**</span></span>](handle-t.md)
</dt> <dt>

[<span data-ttu-id="58464-175">**обращать**</span><span class="sxs-lookup"><span data-stu-id="58464-175">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="58464-176">**Последний \_ —**</span><span class="sxs-lookup"><span data-stu-id="58464-176">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="58464-177">**Длина \_ равна**</span><span class="sxs-lookup"><span data-stu-id="58464-177">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="58464-178">**Языковые**</span><span class="sxs-lookup"><span data-stu-id="58464-178">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="58464-179">**Максимальное \_ число**</span><span class="sxs-lookup"><span data-stu-id="58464-179">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="58464-180">\_пользовательское \_ выделение MIDL</span><span class="sxs-lookup"><span data-stu-id="58464-180">midl\_user\_allocate</span></span>](/windows/desktop/Rpc/the-midl-user-allocate-function)
</dt> <dt>

[<span data-ttu-id="58464-181">\_бесплатный пользователь \_ MIDL</span><span class="sxs-lookup"><span data-stu-id="58464-181">midl\_user\_free</span></span>](/windows/desktop/Rpc/the-midl-user-free-function)
</dt> <dt>

[<span data-ttu-id="58464-182">**заполняет**</span><span class="sxs-lookup"><span data-stu-id="58464-182">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="58464-183">**Указатель \_ по умолчанию**</span><span class="sxs-lookup"><span data-stu-id="58464-183">**pointer\_default**</span></span>](pointer-default.md)
</dt> <dt>

[<span data-ttu-id="58464-184">**ptr**</span><span class="sxs-lookup"><span data-stu-id="58464-184">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="58464-185">**ref**</span><span class="sxs-lookup"><span data-stu-id="58464-185">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="58464-186">**размер \_ равен**</span><span class="sxs-lookup"><span data-stu-id="58464-186">**size\_is**</span></span>](size-is.md)
</dt> <dt>

[<span data-ttu-id="58464-187">**Строка**</span><span class="sxs-lookup"><span data-stu-id="58464-187">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="58464-188">**struct**</span><span class="sxs-lookup"><span data-stu-id="58464-188">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="58464-189">**Тип коммутатора \_**</span><span class="sxs-lookup"><span data-stu-id="58464-189">**switch\_type**</span></span>](switch-type.md)
</dt> <dt>

[<span data-ttu-id="58464-190">**передать \_ как**</span><span class="sxs-lookup"><span data-stu-id="58464-190">**transmit\_as**</span></span>](transmit-as.md)
</dt> <dt>

[<span data-ttu-id="58464-191">**наборов**</span><span class="sxs-lookup"><span data-stu-id="58464-191">**union**</span></span>](union.md)
</dt> </dl>

 

 