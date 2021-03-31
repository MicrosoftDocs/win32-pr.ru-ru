---
title: ptr - атрибут
description: Атрибут \ PTR \ обозначает указатель в качестве полного указателя.
ms.assetid: a1233a25-b651-4a01-8abf-a64dc9ee168e
keywords:
- атрибут PTR MIDL
topic_type:
- apiref
api_name:
- ptr
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2d8b2ee2e3ea4daccd1c4fa37ff1c1f1899dd3c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337028"
---
# <a name="ptr-attribute"></a><span data-ttu-id="965d8-104">ptr - атрибут</span><span class="sxs-lookup"><span data-stu-id="965d8-104">ptr attribute</span></span>

<span data-ttu-id="965d8-105">Атрибут **\[ ptr \]** обозначает указатель в качестве полного указателя.</span><span class="sxs-lookup"><span data-stu-id="965d8-105">The **\[ptr\]** attribute designates a pointer as a full pointer.</span></span>

``` syntax
pointer_default(ptr)

typedef [ ptr [ , type-attribute-list ] ] type-specifier declarator-list; 

typedef [ struct | union ]
{
    [ ptr [ , field-attribute-list ] ] type-specifier declarator-list;
    ...
}

[ ptr [ , function-attribute-list ] ] type-specifier ptr-decl function-name(
    [ [ parameter-attribute-list ] ] type-specifier [standard-declarator]
    , ...);

[[ [ function-attribute-list ] ]] type-specifier [[ptr-decl]] function-name(
    [ ptr [[ , parameter-attribute-list ]] ] type-specifier [[standard-declarator]]
    , ...);
```

## <a name="parameters"></a><span data-ttu-id="965d8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="965d8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="965d8-107">*Type-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="965d8-107">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="965d8-108">Указывает один или несколько атрибутов, применяемых к типу.</span><span class="sxs-lookup"><span data-stu-id="965d8-108">Specifies one or more attributes that apply to the type.</span></span> <span data-ttu-id="965d8-109">К допустимым атрибутам типа относятся **\[** [**Handle**](handle.md), **\]** **\[** [**Switch \_ Type**](switch-type.md) **\]** , **\[** [**передает \_ as**](transmit-as.md) **\]** ; атрибут указателя **\[** [**ref**](ref.md) **\]** , **\[** [**UNIQUE**](unique.md)или **\[ \] ptr**;, а также **\[** [**\_ маркер контекста**](context-handle.md)атрибутов использования **\]** , **\[** [**String**](string.md) **\]** и **\[** [**Ignore**](ignore.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="965d8-109">Valid type attributes include **\[**[**handle**](handle.md)**\]**, **\[**[**switch\_type**](switch-type.md)**\]**, **\[**[**transmit\_as**](transmit-as.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md), or **\[ptr\]**; and the usage attributes **\[**[**context\_handle**](context-handle.md)**\]**, **\[**[**string**](string.md)**\]**, and **\[**[**ignore**](ignore.md)**\]**.</span></span> <span data-ttu-id="965d8-110">Несколько атрибутов разделяются запятыми.</span><span class="sxs-lookup"><span data-stu-id="965d8-110">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="965d8-111">*Описатель типа*</span><span class="sxs-lookup"><span data-stu-id="965d8-111">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="965d8-112">Задает [базовый тип](midl-base-types.md), [**структуру**](struct.md), [**объединение**](union.md)или тип [**перечисления**](enum.md) или идентификатор типа.</span><span class="sxs-lookup"><span data-stu-id="965d8-112">Specifies a [base type](midl-base-types.md), [**struct**](struct.md), [**union**](union.md), or [**enum**](enum.md) type or type identifier.</span></span> <span data-ttu-id="965d8-113">Дополнительная спецификация хранилища может предшествовать *спецификатору типа*.</span><span class="sxs-lookup"><span data-stu-id="965d8-113">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="965d8-114">*стандартные-деклараторы*</span><span class="sxs-lookup"><span data-stu-id="965d8-114">*standard-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="965d8-115">Задает стандартный декларатор C, например идентификатор, декларатор указателя или декларатор массива.</span><span class="sxs-lookup"><span data-stu-id="965d8-115">Specifies a standard C declarator, such as an identifier, a pointer declarator, or an array declarator.</span></span> <span data-ttu-id="965d8-116">Дополнительные сведения см. в разделе [атрибуты Array и Sized-Pointer](array-and-sized-pointer-attributes.md), [**массивы**](arrays-1.md), [массивы и указатели](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="965d8-116">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span>

</dd> <dt>

<span data-ttu-id="965d8-117">*декларатор-список*</span><span class="sxs-lookup"><span data-stu-id="965d8-117">*declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="965d8-118">Задает стандартные деклараторы C, такие как идентификаторы, деклараторы указателей и деклараторы массивов.</span><span class="sxs-lookup"><span data-stu-id="965d8-118">Specifies standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="965d8-119">Дополнительные сведения см. в разделе [атрибуты Array и Sized-Pointer](array-and-sized-pointer-attributes.md), [**массивы**](arrays-1.md), [массивы и указатели](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="965d8-119">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="965d8-120">*Список деклараторов* состоит из одного или нескольких деклараторов, разделенных запятыми.</span><span class="sxs-lookup"><span data-stu-id="965d8-120">The *declarator-list* consists of one or more declarators separated by commas.</span></span> <span data-ttu-id="965d8-121">Идентификатор параметра-Name в деклараторе функции является необязательным.</span><span class="sxs-lookup"><span data-stu-id="965d8-121">The parameter-name identifier in the function declarator is optional.</span></span>

</dd> <dt>

<span data-ttu-id="965d8-122">*Список атрибутов Field*</span><span class="sxs-lookup"><span data-stu-id="965d8-122">*field-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="965d8-123">Указывает ноль или более атрибутов полей, применимых к структуре, элементу объединения или параметру функции.</span><span class="sxs-lookup"><span data-stu-id="965d8-123">Specifies zero or more field attributes that apply to the structure or union member or function parameter.</span></span> <span data-ttu-id="965d8-124">К допустимым атрибутам полей относятся: **\[** [**First \_**](first-is.md)—, **\]** **\[** [**Last \_ —**](last-is.md), **\]** **\[** [**length \_ —**](length-is.md) **\]** , **\[** [**Max \_ —**](max-is.md) **\]** , **\[** [**size \_ —**](size-is.md), **\]** строка атрибутов использования **\[** [](string.md) **\]** , **\[** [**Ignore**](ignore.md) **\]** и **\[** [**контекст контекста \_**](context-handle.md) **\]** ; атрибут указателя **\[** [**ref**](ref.md) **\]** , **\[** [**UNIQUE**](unique.md) **\]** , **\[ ptr \]**, и **\[** [**\_ Тип переключателя**](switch-type.md)атрибута Union **\]** .</span><span class="sxs-lookup"><span data-stu-id="965d8-124">Valid field attributes include **\[**[**first\_is**](first-is.md)**\]**, **\[**[**last\_is**](last-is.md)**\]**, **\[**[**length\_is**](length-is.md)**\]**, **\[**[**max\_is**](max-is.md)**\]**, **\[**[**size\_is**](size-is.md)**\]**; the usage attributes **\[**[**string**](string.md)**\]**, **\[**[**ignore**](ignore.md)**\]**, and **\[**[**context\_handle**](context-handle.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[ptr\]**; and the union attribute **\[**[**switch\_type**](switch-type.md)**\]**.</span></span> <span data-ttu-id="965d8-125">Несколько атрибутов полей разделяются запятыми.</span><span class="sxs-lookup"><span data-stu-id="965d8-125">Separate multiple field attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="965d8-126">*Function-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="965d8-126">*function-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="965d8-127">Указывает ноль или более атрибутов, которые применяются к функции.</span><span class="sxs-lookup"><span data-stu-id="965d8-127">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="965d8-128">Допустимые атрибуты функции — **\[** [**обратный вызов**](callback.md) **\]** , **\[** [**локальный**](local.md) **\]** объект, атрибут указателя **\[** [**ref**](ref.md) **\]** , **\[** [**UNIQUE**](unique.md) **\]** или **\[ ptr \]**; и атрибуты использования **\[** [**строка**](string.md) **\]** , **\[** [**Ignore**](ignore.md) **\]** и **\[** [**Контекстный \_ маркер**](context-handle.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="965d8-128">Valid function attributes are **\[**[**callback**](callback.md)**\]**, **\[**[**local**](local.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[ptr\]**; and the usage attributes **\[**[**string**](string.md)**\]**, **\[**[**ignore**](ignore.md)**\]**, and **\[**[**context\_handle**](context-handle.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="965d8-129">*PTR-decl*</span><span class="sxs-lookup"><span data-stu-id="965d8-129">*ptr-decl*</span></span> 
</dt> <dd>

<span data-ttu-id="965d8-130">Указывает по крайней мере один декларатор указателя, к которому применяется атрибут **\[ ptr \]** .</span><span class="sxs-lookup"><span data-stu-id="965d8-130">Specifies at least one pointer declarator to which the **\[ptr\]** attribute applies.</span></span> <span data-ttu-id="965d8-131">Декларатор указателя аналогичен декларатору указателя, используемому в C; Он создается из \* указателя, модификаторов, таких как **FAR**, и квалификатора [**const**](const.md).</span><span class="sxs-lookup"><span data-stu-id="965d8-131">A pointer declarator is the same as the pointer declarator used in C; it is constructed from the \* designator, modifiers such as **far**, and the qualifier [**const**](const.md).</span></span>

</dd> <dt>

<span data-ttu-id="965d8-132">*имя функции*</span><span class="sxs-lookup"><span data-stu-id="965d8-132">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="965d8-133">Задает имя удаленной процедуры.</span><span class="sxs-lookup"><span data-stu-id="965d8-133">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="965d8-134">*Parameter-список атрибутов*</span><span class="sxs-lookup"><span data-stu-id="965d8-134">*parameter-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="965d8-135">Состоит из нуля или более атрибутов, подходящих для указанного типа параметра.</span><span class="sxs-lookup"><span data-stu-id="965d8-135">Consists of zero or more attributes appropriate for the specified parameter type.</span></span> <span data-ttu-id="965d8-136">[**Атрибуты параметров могут принимать и**](in.md) отменять атрибуты направления [**.**](out-idl.md) Сначала атрибуты поля [**\_ —**](first-is.md), [**Last \_ —**](last-is.md), [**length \_ —**](length-is.md), [**Max \_ —**](max-is.md), [**size \_ —**](size-is.md)и [**\_ Тип переключателя**](switch-type.md); атрибут указателя [**ref**](ref.md), [**UNIQUE**](unique.md)или **\[ ptr \]**, а также [**\_ маркер контекста**](context-handle.md) атрибутов использования и [**строка**](string.md).</span><span class="sxs-lookup"><span data-stu-id="965d8-136">Parameter attributes can take the directional attributes [**in**](in.md) and [**out**](out-idl.md); the field attributes [**first\_is**](first-is.md), [**last\_is**](last-is.md), [**length\_is**](length-is.md), [**max\_is**](max-is.md), [**size\_is**](size-is.md), and [**switch\_type**](switch-type.md); the pointer attribute [**ref**](ref.md), [**unique**](unique.md), or **\[ptr\]**; and the usage attributes [**context\_handle**](context-handle.md) and [**string**](string.md).</span></span> <span data-ttu-id="965d8-137">Атрибут использования [**Ignore**](ignore.md) не может использоваться в качестве атрибута параметра.</span><span class="sxs-lookup"><span data-stu-id="965d8-137">The usage attribute [**ignore**](ignore.md) cannot be used as a parameter attribute.</span></span> <span data-ttu-id="965d8-138">Несколько атрибутов разделяются запятыми.</span><span class="sxs-lookup"><span data-stu-id="965d8-138">Separate multiple attributes with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="965d8-139">Комментарии</span><span class="sxs-lookup"><span data-stu-id="965d8-139">Remarks</span></span>

<span data-ttu-id="965d8-140">Полный указатель, указанный атрибутом **\[ ptr \]** , приближается к полной функциональности указателя языка C.</span><span class="sxs-lookup"><span data-stu-id="965d8-140">The full pointer designated by the **\[ptr\]** attribute approaches the full functionality of the C-language pointer.</span></span> <span data-ttu-id="965d8-141">Полный указатель может иметь значение **null** и может изменяться во время вызова от **null** к значению, отличному от **null**.</span><span class="sxs-lookup"><span data-stu-id="965d8-141">The full pointer can have the value **NULL** and can change during the call from **NULL** to non-**NULL**.</span></span> <span data-ttu-id="965d8-142">Хранилище, на которое указывают полные указатели, может быть достигнуто другими именами в приложении, поддерживающим псевдонимы и циклы.</span><span class="sxs-lookup"><span data-stu-id="965d8-142">Storage pointed to by full pointers can be reached by other names in the application supporting aliasing and cycles.</span></span> <span data-ttu-id="965d8-143">Эта функциональность требует дополнительных издержек при удаленном вызове процедуры для определения данных, на которые ссылается указатель, определения того, является ли значение **нулевым**, и обнаруживать, указывают ли два указателя на одни и те же данные.</span><span class="sxs-lookup"><span data-stu-id="965d8-143">This functionality requires more overhead during a remote procedure call to identify the data referred to by the pointer, determine whether the value is **NULL**, and to discover if two pointers point to the same data.</span></span>

<span data-ttu-id="965d8-144">Использовать полные указатели для:</span><span class="sxs-lookup"><span data-stu-id="965d8-144">Use full pointers for:</span></span>

-   <span data-ttu-id="965d8-145">Удаленные возвращаемые значения.</span><span class="sxs-lookup"><span data-stu-id="965d8-145">Remote return values.</span></span>
-   <span data-ttu-id="965d8-146">Двойные указатели, если размер выходного параметра не известен.</span><span class="sxs-lookup"><span data-stu-id="965d8-146">Double pointers, when the size of an output parameter is not known.</span></span>
-   <span data-ttu-id="965d8-147">Указатели **null** .</span><span class="sxs-lookup"><span data-stu-id="965d8-147">**NULL** pointers.</span></span>

<span data-ttu-id="965d8-148">Полные (и уникальные) указатели не могут использоваться для описания размера массива или объединения, так как эти указатели могут иметь значение **null**.</span><span class="sxs-lookup"><span data-stu-id="965d8-148">Full (and unique) pointers cannot be used to describe the size of an array or union because these pointers can have the value **NULL**.</span></span> <span data-ttu-id="965d8-149">Это ограничение с помощью MIDL предотвращает ошибку, которая может возникать, если в качестве размера используется значение **null** .</span><span class="sxs-lookup"><span data-stu-id="965d8-149">This restriction by MIDL prevents an error that can result when a **NULL** value is used as the size.</span></span>

<span data-ttu-id="965d8-150">Предполагается, что ссылки и уникальные указатели не являются псевдонимами данных.</span><span class="sxs-lookup"><span data-stu-id="965d8-150">Reference and unique pointers are assumed to cause no aliasing of data.</span></span> <span data-ttu-id="965d8-151">Направленный граф, полученный с помощью уникального или ссылочного указателя, и следующие только уникальные указатели или ссылочные классы не содержат ни пересхождение, ни циклов.</span><span class="sxs-lookup"><span data-stu-id="965d8-151">A directed graph obtained by starting from a unique or reference pointer and following only unique or reference pointers contains neither reconvergence nor cycles.</span></span>

<span data-ttu-id="965d8-152">Чтобы избежать присвоения псевдонимов, все значения указателей должны быть получены из указателя ввода того же класса указателя.</span><span class="sxs-lookup"><span data-stu-id="965d8-152">To avoid aliasing, all pointer values should be obtained from an input pointer of the same class of pointer.</span></span> <span data-ttu-id="965d8-153">Если несколько указателей указывают на одно и то же расположение в памяти, все эти указатели должны быть полными указателями.</span><span class="sxs-lookup"><span data-stu-id="965d8-153">If more than one pointer points to the same memory location, all such pointers must be full pointers.</span></span>

<span data-ttu-id="965d8-154">В некоторых случаях полные и уникальные указатели могут быть смешанными.</span><span class="sxs-lookup"><span data-stu-id="965d8-154">In some cases, full and unique pointers can be mixed.</span></span> <span data-ttu-id="965d8-155">Полному указателю может быть присвоено значение уникального указателя, если оно не нарушает ограничения на изменение значения уникального указателя.</span><span class="sxs-lookup"><span data-stu-id="965d8-155">A full pointer can be assigned the value of a unique pointer, as long as the assignment does not violate the restrictions on changing the value of a unique pointer.</span></span> <span data-ttu-id="965d8-156">Однако при присвоении уникального указателя значению полного указателя может быть вызвано Присвоение псевдонимов.</span><span class="sxs-lookup"><span data-stu-id="965d8-156">However, when you assign a unique pointer the value of a full pointer, you may cause aliasing.</span></span>

<span data-ttu-id="965d8-157">Смешивание полных и уникальных указателей может привести к присвоению псевдонимов, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="965d8-157">Mixing full and unique pointers can cause aliasing, as demonstrated in the following example:</span></span>

``` syntax
typedef struct 
{ 
    [ptr] short * pdata;          // full pointer  
} GRAPH_NODE_TYPE; 
 
typedef struct 
{ 
    [unique] graph_node * left;   // unique pointer  
    [unique] graph_node * right;  // unique pointer 
} TREE_NODE_TYPE; 
 
// application code: 
short a = 5; 
TREE_NODE_TYPE * t; 
GRAPH_NODE_TYPE g, h; 
 
g.pdata = h.pdata = &a; 
t->left = &g; 
t->right = &h; 
// t->left->pdata == t->right->pdata == &a
```

<span data-ttu-id="965d8-158">Хотя "t->Left" и "t->right" указывают на уникальные расположения в памяти, "t->Left->pData" и "t->right->pData" имеют псевдонимы.</span><span class="sxs-lookup"><span data-stu-id="965d8-158">Although "t->left" and "t->right" point to unique memory locations, "t->left->pdata" and "t->right->pdata" are aliased.</span></span> <span data-ttu-id="965d8-159">По этой причине алгоритмы поддержки псевдонимов должны следовать всем указателям (включая уникальные и ссылочные указатели), которые в конечном итоге могут обращаться к полному указателю.</span><span class="sxs-lookup"><span data-stu-id="965d8-159">For this reason, aliasing-support algorithms must follow all pointers (including unique and reference pointers) that may eventually reach a full pointer.</span></span>

## <a name="examples"></a><span data-ttu-id="965d8-160">Примеры</span><span class="sxs-lookup"><span data-stu-id="965d8-160">Examples</span></span>

``` syntax
pointer_default(ptr) 
 
typedef [ptr, string] unsigned char * MY_STRING_TYPE; 
 
[ptr] char * MyFunction([in, out, unique] long * plNumber);
```

## <a name="see-also"></a><span data-ttu-id="965d8-161">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="965d8-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="965d8-162">**массивы**</span><span class="sxs-lookup"><span data-stu-id="965d8-162">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="965d8-163">Массивы и указатели</span><span class="sxs-lookup"><span data-stu-id="965d8-163">Arrays and Pointers</span></span>](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[<span data-ttu-id="965d8-164">Атрибуты массива и Sized-Pointer</span><span class="sxs-lookup"><span data-stu-id="965d8-164">Array and Sized-Pointer Attributes</span></span>](array-and-sized-pointer-attributes.md)
</dt> <dt>

[<span data-ttu-id="965d8-165">Базовые типы MIDL</span><span class="sxs-lookup"><span data-stu-id="965d8-165">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="965d8-166">**обратный вызов**</span><span class="sxs-lookup"><span data-stu-id="965d8-166">**callback**</span></span>](callback.md)
</dt> <dt>

[<span data-ttu-id="965d8-167">**const**</span><span class="sxs-lookup"><span data-stu-id="965d8-167">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="965d8-168">**Контекстный \_ маркер**</span><span class="sxs-lookup"><span data-stu-id="965d8-168">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="965d8-169">**перечисления**</span><span class="sxs-lookup"><span data-stu-id="965d8-169">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="965d8-170">**первый \_ —**</span><span class="sxs-lookup"><span data-stu-id="965d8-170">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="965d8-171">**справиться**</span><span class="sxs-lookup"><span data-stu-id="965d8-171">**handle**</span></span>](handle.md)
</dt> <dt>

[<span data-ttu-id="965d8-172">Файл определения интерфейса (IDL)</span><span class="sxs-lookup"><span data-stu-id="965d8-172">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="965d8-173">**обращать**</span><span class="sxs-lookup"><span data-stu-id="965d8-173">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="965d8-174">**Последний \_ —**</span><span class="sxs-lookup"><span data-stu-id="965d8-174">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="965d8-175">**Длина \_ равна**</span><span class="sxs-lookup"><span data-stu-id="965d8-175">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="965d8-176">**Языковые**</span><span class="sxs-lookup"><span data-stu-id="965d8-176">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="965d8-177">**Максимальное \_ число**</span><span class="sxs-lookup"><span data-stu-id="965d8-177">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="965d8-178">**Указатель \_ по умолчанию**</span><span class="sxs-lookup"><span data-stu-id="965d8-178">**pointer\_default**</span></span>](pointer-default.md)
</dt> <dt>

[<span data-ttu-id="965d8-179">**ref**</span><span class="sxs-lookup"><span data-stu-id="965d8-179">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="965d8-180">**размер \_ равен**</span><span class="sxs-lookup"><span data-stu-id="965d8-180">**size\_is**</span></span>](size-is.md)
</dt> <dt>

[<span data-ttu-id="965d8-181">**Строка**</span><span class="sxs-lookup"><span data-stu-id="965d8-181">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="965d8-182">**struct**</span><span class="sxs-lookup"><span data-stu-id="965d8-182">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="965d8-183">**Тип коммутатора \_**</span><span class="sxs-lookup"><span data-stu-id="965d8-183">**switch\_type**</span></span>](switch-type.md)
</dt> <dt>

[<span data-ttu-id="965d8-184">**передать \_ как**</span><span class="sxs-lookup"><span data-stu-id="965d8-184">**transmit\_as**</span></span>](transmit-as.md)
</dt> <dt>

[<span data-ttu-id="965d8-185">**наборов**</span><span class="sxs-lookup"><span data-stu-id="965d8-185">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="965d8-186">**однозначно**</span><span class="sxs-lookup"><span data-stu-id="965d8-186">**unique**</span></span>](unique.md)
</dt> </dl>

 

 