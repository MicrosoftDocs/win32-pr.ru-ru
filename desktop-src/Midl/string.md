---
title: string - атрибут
description: Атрибут \ String \ указывает, что одномерный массив char, WCHAR \_ t, Byte (или эквивалентный) или указатель на такой массив должен рассматриваться как строка.
ms.assetid: 379cd59e-7540-4188-9b5c-6c25a8928999
keywords:
- строковый атрибут MIDL
topic_type:
- apiref
api_name:
- string
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae2bd3c56bcf09d1c47343f903653e9d83113b1d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103987460"
---
# <a name="string-attribute"></a><span data-ttu-id="90c0e-104">string - атрибут</span><span class="sxs-lookup"><span data-stu-id="90c0e-104">string attribute</span></span>

<span data-ttu-id="90c0e-105">Атрибут **\[ String \]** указывает, что одномерный массив [**char**](char-idl.md), [**WCHAR \_ t**](wchar-t.md), [**Byte**](byte.md) (или эквивалентный) или указатель на такой массив должен рассматриваться как строка.</span><span class="sxs-lookup"><span data-stu-id="90c0e-105">The **\[string\]** attribute indicates that the one-dimensional [**char**](char-idl.md), [**wchar\_t**](wchar-t.md), [**byte**](byte.md) (or equivalent) array or the pointer to such an array must be treated as a string.</span></span> <span data-ttu-id="90c0e-106">Строка может также быть массивом (или указателем на массив) конструкций, поля которых имеют тип **Byte**.</span><span class="sxs-lookup"><span data-stu-id="90c0e-106">The string can also be an array (or a pointer to an array) of constructs whose fields are all of the type **byte**.</span></span>

``` syntax
typedef [ string [[ , type-attribute-list ]] ] type-specifier declarator-list; 

typedef [ struct | union ] 
{
    [ string [[ , field-attribute-list ]] ] type-specifier declarator-list;
    ...
};

[ string [[ , function-attribute-list ]] ] type-specifier ptr-decl function-name(
  [[ [ parameter-attribute-list ] ]] type-specifier [[standard-declarator]]
  , ...);

[[ [ function-attribute-list ] ]] type-specifier [[ptr-decl]] function-name(
    [ string [[ , parameter-attribute-list ]] ] type-specifier [[standard-declarator]]
  , ...);
```

## <a name="parameters"></a><span data-ttu-id="90c0e-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="90c0e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90c0e-108">*Type-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="90c0e-108">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="90c0e-109">Указывает один или несколько атрибутов, применяемых к типу.</span><span class="sxs-lookup"><span data-stu-id="90c0e-109">Specifies one or more attributes that apply to a type.</span></span> <span data-ttu-id="90c0e-110">К допустимым атрибутам типа относятся **\[** [**Handle**](handle.md), **\]** **\[** [**Switch \_ Type**](switch-type.md) **\]** , **\[** [**передает \_ as**](transmit-as.md) **\]** ; атрибут указателя **\[** [**ref**](ref.md) **\]** , **\[** [**UNIQUE**](unique.md) **\]** или **\[** [**ptr**](ptr.md) **\]** ;, а также **\[** [**\_ маркер контекста**](context-handle.md)атрибутов использования **\]** , **\[ String \]** и **\[** [**Ignore**](ignore.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="90c0e-110">Valid type attributes include **\[**[**handle**](handle.md)**\]**, **\[**[**switch\_type**](switch-type.md)**\]**, **\[**[**transmit\_as**](transmit-as.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**context\_handle**](context-handle.md)**\]**, **\[string\]**, and **\[**[**ignore**](ignore.md)**\]**.</span></span> <span data-ttu-id="90c0e-111">Несколько атрибутов разделяются запятыми.</span><span class="sxs-lookup"><span data-stu-id="90c0e-111">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="90c0e-112">*Описатель типа*</span><span class="sxs-lookup"><span data-stu-id="90c0e-112">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="90c0e-113">Указывает [базовый тип](midl-base-types.md), тип [**структуры**](struct.md) или идентификатор типа.</span><span class="sxs-lookup"><span data-stu-id="90c0e-113">Specifies a [base type](midl-base-types.md), [**struct**](struct.md) type, or type identifier.</span></span> <span data-ttu-id="90c0e-114">Дополнительная спецификация хранилища может предшествовать *спецификатору типа*.</span><span class="sxs-lookup"><span data-stu-id="90c0e-114">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="90c0e-115">*стандартные-деклараторы*</span><span class="sxs-lookup"><span data-stu-id="90c0e-115">*standard-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="90c0e-116">Задает стандартный декларатор C, например идентификатор, декларатор указателя или декларатор массива.</span><span class="sxs-lookup"><span data-stu-id="90c0e-116">Specifies a standard C declarator, such as an identifier, a pointer declarator, or an array declarator.</span></span> <span data-ttu-id="90c0e-117">Дополнительные сведения см. в разделе [атрибуты Array и Sized-Pointer](array-and-sized-pointer-attributes.md), [**массивы**](arrays-1.md). и [массивы и указатели](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="90c0e-117">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md)., and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span>

</dd> <dt>

<span data-ttu-id="90c0e-118">*декларатор-список*</span><span class="sxs-lookup"><span data-stu-id="90c0e-118">*declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="90c0e-119">Задает стандартные деклараторы C, такие как идентификаторы, деклараторы указателей и деклараторы массивов.</span><span class="sxs-lookup"><span data-stu-id="90c0e-119">Specifies standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="90c0e-120">Дополнительные сведения см. в разделе [атрибуты Array и Sized-Pointer](array-and-sized-pointer-attributes.md), [**массивы**](arrays-1.md). и [массивы и указатели](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="90c0e-120">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md)., and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="90c0e-121">*Список деклараторов* состоит из одного или нескольких деклараторов, разделенных запятыми.</span><span class="sxs-lookup"><span data-stu-id="90c0e-121">The *declarator-list* consists of one or more declarators separated by commas.</span></span> <span data-ttu-id="90c0e-122">Идентификатор параметра-Name в деклараторе функции является необязательным.</span><span class="sxs-lookup"><span data-stu-id="90c0e-122">The parameter-name identifier in the function declarator is optional.</span></span>

</dd> <dt>

<span data-ttu-id="90c0e-123">*Список атрибутов Field*</span><span class="sxs-lookup"><span data-stu-id="90c0e-123">*field-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="90c0e-124">Указывает ноль или более атрибутов полей, применимых к структуре, члену объединения или параметру функции.</span><span class="sxs-lookup"><span data-stu-id="90c0e-124">Specifies zero or more field attributes that apply to the structure, union member, or function parameter.</span></span> <span data-ttu-id="90c0e-125">Два допустимых атрибута поля — **\[** [**это \_ Max**](max-is.md) , **\]** а **\[** [**размер \_ —**](size-is.md) **\]** **\[ \] строка** атрибутов **\[ \] использования, атрибут Ignore**, модификатор **\[ контекста \_ , тип указателя ref, UNIQUE или PTR, а также переключатель атрибута Union. \]** **\[** [](ref.md) **\]** **\[ \]** **\[** [](ptr.md) **\]** **\[ \_ \]**</span><span class="sxs-lookup"><span data-stu-id="90c0e-125">The two valid field attributes are **\[**[**max\_is**](max-is.md)**\]** and **\[**[**size\_is**](size-is.md)**\]**; the usage attributes **\[string\]**, **\[ignore\]**, and **\[context\_handle\]**, the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[unique\]**, or **\[**[**ptr**](ptr.md)**\]**, and the union attribute **\[switch\_type\]**.</span></span> <span data-ttu-id="90c0e-126">Несколько атрибутов полей разделяются запятыми.</span><span class="sxs-lookup"><span data-stu-id="90c0e-126">Separate multiple field attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="90c0e-127">*Function-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="90c0e-127">*function-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="90c0e-128">Указывает ноль или более атрибутов, которые применяются к функции.</span><span class="sxs-lookup"><span data-stu-id="90c0e-128">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="90c0e-129">Допустимые атрибуты функции — **\[** [**обратный вызов**](callback.md) **\]** , **\[** [**локальный**](local.md) **\]** объект, атрибут указателя **\[ \] ref**, **\[ Unique \]** или **\[ ptr \]**; и атрибуты использования **\[ строка \]**, **\[ Ignore \]** и **\[ Контекстный \_ маркер \]**.</span><span class="sxs-lookup"><span data-stu-id="90c0e-129">Valid function attributes are **\[**[**callback**](callback.md)**\]**, **\[**[**local**](local.md)**\]**; the pointer attribute **\[ref\]**, **\[unique\]**, or **\[ptr\]**; and the usage attributes **\[string\]**, **\[ignore\]**, and **\[context\_handle\]**.</span></span>

</dd> <dt>

<span data-ttu-id="90c0e-130">*PTR-decl*</span><span class="sxs-lookup"><span data-stu-id="90c0e-130">*ptr-decl*</span></span> 
</dt> <dd>

<span data-ttu-id="90c0e-131">Задает необязательный декларатор указателя, к которому применяется атрибут **\[ String \]** .</span><span class="sxs-lookup"><span data-stu-id="90c0e-131">Specifies an optional pointer declarator to which the **\[string\]** attribute applies.</span></span> <span data-ttu-id="90c0e-132">Декларатор указателя аналогичен декларатору указателя, используемому в C; Он создается из \* указателя, модификаторов, таких как **FAR**, и квалификатора [**const**](const.md).</span><span class="sxs-lookup"><span data-stu-id="90c0e-132">A pointer declarator is the same as the pointer declarator used in C; it is constructed from the \* designator, modifiers such as **far**, and the qualifier [**const**](const.md).</span></span>

</dd> <dt>

<span data-ttu-id="90c0e-133">*имя функции*</span><span class="sxs-lookup"><span data-stu-id="90c0e-133">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="90c0e-134">Задает имя удаленной процедуры.</span><span class="sxs-lookup"><span data-stu-id="90c0e-134">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="90c0e-135">*Parameter-список атрибутов*</span><span class="sxs-lookup"><span data-stu-id="90c0e-135">*parameter-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="90c0e-136">Состоит из нуля или более атрибутов, подходящих для указанного типа параметра.</span><span class="sxs-lookup"><span data-stu-id="90c0e-136">Consists of zero or more attributes appropriate for the specified parameter type.</span></span> <span data-ttu-id="90c0e-137">Атрибуты параметров могут **\[ \]** принимать и отменять **\[ атрибуты \]** направления; атрибуты поля **\[** [**Max \_ имеют**](max-is.md) значение, **\]** а **\[** [**размер \_ —**](size-is.md) **\]** атрибут указателя **\[ ref \]**, **\[ Unique \]** или **\[ ptr \]**, а также **\[ \_ маркер \] контекста** атрибутов использования и **\[ строка \]**.</span><span class="sxs-lookup"><span data-stu-id="90c0e-137">Parameter attributes can take the directional attributes **\[in\]** and **\[out\]**; the field attributes **\[**[**max\_is**](max-is.md)**\]** and **\[**[**size\_is**](size-is.md)**\]**; the pointer attribute **\[ref\]**, **\[unique\]**, or **\[ptr\]**; and the usage attributes **\[context\_handle\]** and **\[string\]**.</span></span> <span data-ttu-id="90c0e-138">Атрибут использования **\[ Ignore \]** не может использоваться в качестве атрибута параметра.</span><span class="sxs-lookup"><span data-stu-id="90c0e-138">The usage attribute **\[ignore\]** cannot be used as a parameter attribute.</span></span> <span data-ttu-id="90c0e-139">Несколько атрибутов разделяются запятыми.</span><span class="sxs-lookup"><span data-stu-id="90c0e-139">Separate multiple attributes with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="90c0e-140">Комментарии</span><span class="sxs-lookup"><span data-stu-id="90c0e-140">Remarks</span></span>

<span data-ttu-id="90c0e-141">Если **\[ строковый \]** атрибут используется с массивом, границы которого определяются во время выполнения, необходимо также указать атрибут **\[ \_ \]** **\[ size \_ \]** или Max, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="90c0e-141">If the **\[string\]** attribute is used with an array whose bounds are determined at run time, you must also specify a **\[size\_is\]** or **\[max\_is\]** attribute, as in the following example:</span></span>

``` syntax
/* a string that can hold up to MAX_STRING_LENGTH characters */
typedef [string, max_is(MAX_STRING_LENGTH)] char line[];
```

<span data-ttu-id="90c0e-142">Атрибут **\[ String \]** не может использоваться с атрибутами, задающих диапазон переданных элементов, например **\[ First \_ — \]**, **\[ Last \_ — \]** и **\[ length \_ — \]**.</span><span class="sxs-lookup"><span data-stu-id="90c0e-142">The **\[string\]** attribute cannot be used with attributes that specify the range of transmitted elements, such as **\[first\_is\]**, **\[last\_is\]**, and **\[length\_is\]**.</span></span>

<span data-ttu-id="90c0e-143">При использовании в многомерных массивах атрибут **\[ String \]** применяется к крайнему справа массиву.</span><span class="sxs-lookup"><span data-stu-id="90c0e-143">When used on multidimensional arrays, the **\[string\]** attribute applies to the rightmost array.</span></span>

<span data-ttu-id="90c0e-144">Чтобы определить подсчитанную строку, не используйте атрибут **\[ String \]** .</span><span class="sxs-lookup"><span data-stu-id="90c0e-144">To define a counted string, do not use the **\[string\]** attribute.</span></span> <span data-ttu-id="90c0e-145">Используйте массив символов или символьный указатель, подобный следующему:</span><span class="sxs-lookup"><span data-stu-id="90c0e-145">Use a character array or character-based pointer such as the following:</span></span>

``` syntax
typedef struct 
{ 
    unsigned short size; 
    unsigned short length; 
    [size_is(size), length_is(length)] char string[*]; 
} counted_string;
```

<span data-ttu-id="90c0e-146">Атрибут **\[ String \]** указывает, что заглушка должна использовать предоставляемый языком метод для определения длины строк.</span><span class="sxs-lookup"><span data-stu-id="90c0e-146">The **\[string\]** attribute specifies that the stub should use a language-supplied method to determine the length of strings.</span></span>

<span data-ttu-id="90c0e-147">При объявлении строк в языке C необходимо выделить место для дополнительного символа, который обозначает конец строки.</span><span class="sxs-lookup"><span data-stu-id="90c0e-147">When declaring strings in C, you must allocate space for an extra character that marks the end of the string.</span></span>

## <a name="examples"></a><span data-ttu-id="90c0e-148">Примеры</span><span class="sxs-lookup"><span data-stu-id="90c0e-148">Examples</span></span>

``` syntax
/* a string type that can hold up to 80 characters */ 
typedef [string] char line[81]; 
 
HRESULT Proc1([in, string] char * pszName);
```

## <a name="see-also"></a><span data-ttu-id="90c0e-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="90c0e-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90c0e-150">**массивы**</span><span class="sxs-lookup"><span data-stu-id="90c0e-150">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="90c0e-151">Базовые типы MIDL</span><span class="sxs-lookup"><span data-stu-id="90c0e-151">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="90c0e-152">**обратный вызов**</span><span class="sxs-lookup"><span data-stu-id="90c0e-152">**callback**</span></span>](callback.md)
</dt> <dt>

[<span data-ttu-id="90c0e-153">**char**</span><span class="sxs-lookup"><span data-stu-id="90c0e-153">**char**</span></span>](char-idl.md)
</dt> <dt>

[<span data-ttu-id="90c0e-154">**const**</span><span class="sxs-lookup"><span data-stu-id="90c0e-154">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="90c0e-155">**Контекстный \_ маркер**</span><span class="sxs-lookup"><span data-stu-id="90c0e-155">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="90c0e-156">**перечисления**</span><span class="sxs-lookup"><span data-stu-id="90c0e-156">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="90c0e-157">**первый \_ —**</span><span class="sxs-lookup"><span data-stu-id="90c0e-157">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="90c0e-158">**справиться**</span><span class="sxs-lookup"><span data-stu-id="90c0e-158">**handle**</span></span>](handle.md)
</dt> <dt>

[<span data-ttu-id="90c0e-159">Файл определения интерфейса (IDL)</span><span class="sxs-lookup"><span data-stu-id="90c0e-159">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="90c0e-160">**обращать**</span><span class="sxs-lookup"><span data-stu-id="90c0e-160">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="90c0e-161">**Последний \_ —**</span><span class="sxs-lookup"><span data-stu-id="90c0e-161">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="90c0e-162">**Длина \_ равна**</span><span class="sxs-lookup"><span data-stu-id="90c0e-162">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="90c0e-163">**Языковые**</span><span class="sxs-lookup"><span data-stu-id="90c0e-163">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="90c0e-164">**Максимальное \_ число**</span><span class="sxs-lookup"><span data-stu-id="90c0e-164">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="90c0e-165">**Указатель \_ по умолчанию**</span><span class="sxs-lookup"><span data-stu-id="90c0e-165">**pointer\_default**</span></span>](pointer-default.md)
</dt> <dt>

[<span data-ttu-id="90c0e-166">**ptr**</span><span class="sxs-lookup"><span data-stu-id="90c0e-166">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="90c0e-167">**ref**</span><span class="sxs-lookup"><span data-stu-id="90c0e-167">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="90c0e-168">**размер \_ равен**</span><span class="sxs-lookup"><span data-stu-id="90c0e-168">**size\_is**</span></span>](size-is.md)
</dt> <dt>

[<span data-ttu-id="90c0e-169">**struct**</span><span class="sxs-lookup"><span data-stu-id="90c0e-169">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="90c0e-170">**Тип коммутатора \_**</span><span class="sxs-lookup"><span data-stu-id="90c0e-170">**switch\_type**</span></span>](switch-type.md)
</dt> <dt>

[<span data-ttu-id="90c0e-171">**передать \_ как**</span><span class="sxs-lookup"><span data-stu-id="90c0e-171">**transmit\_as**</span></span>](transmit-as.md)
</dt> <dt>

[<span data-ttu-id="90c0e-172">**наборов**</span><span class="sxs-lookup"><span data-stu-id="90c0e-172">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="90c0e-173">**однозначно**</span><span class="sxs-lookup"><span data-stu-id="90c0e-173">**unique**</span></span>](unique.md)
</dt> <dt>

[<span data-ttu-id="90c0e-174">**WCHAR \_ t**</span><span class="sxs-lookup"><span data-stu-id="90c0e-174">**wchar\_t**</span></span>](wchar-t.md)
</dt> </dl>

 

 