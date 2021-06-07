---
title: атрибут const
description: Ключевое слово const изменяет тип объявления типа или типа параметра функции, предотвращая изменение значения.
ms.assetid: 398fab76-93f3-4d5a-9223-1c57c612b2d7
keywords:
- Константный атрибут MIDL
topic_type:
- apiref
api_name:
- const
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7095e29daf18dc111caf37038b06b0beff5245a8
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387063"
---
# <a name="const-attribute"></a><span data-ttu-id="7c6a6-104">атрибут const</span><span class="sxs-lookup"><span data-stu-id="7c6a6-104">const attribute</span></span>

<span data-ttu-id="7c6a6-105">Ключевое слово **const** изменяет тип объявления типа или типа параметра функции, предотвращая изменение значения.</span><span class="sxs-lookup"><span data-stu-id="7c6a6-105">The **const** keyword modifies the type of a type declaration or the type of a function parameter, preventing the value from varying.</span></span>

``` syntax
const const-type identifier = const-expression ;

[ typedef [ , type-attribute-list ] ] const const-type declarator-list;

[ typedef [ , type-attribute-list ] ] pointer-type const declarator-list;

[ [ function-attr-list ] ] type-specifier [ ptr-decl ] function-name(
    [ [ parameter-attribute-list ] ] ) const; 

const-type [declarator], [ [ parameter-attribute-list ] ] pointer-type const [declarator], ...);
```

## <a name="parameters"></a><span data-ttu-id="7c6a6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7c6a6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c6a6-107">*Const-тип*</span><span class="sxs-lookup"><span data-stu-id="7c6a6-107">*const-type*</span></span> 
</dt> <dd>

<span data-ttu-id="7c6a6-108">Задает допустимое целое число, символ, строка или логический тип MIDL.</span><span class="sxs-lookup"><span data-stu-id="7c6a6-108">Specifies a valid MIDL integer, character, string, or Boolean type.</span></span> <span data-ttu-id="7c6a6-109">Допустимые типы MIDL включают [**небольшие**](small.md), [**короткие**](short.md), [**длинные**](long.md), [**char**](char-idl.md),\*\* \* чарâ\* _, [_ \* *WCHAR \_ t*](wchar-t.md), \**WCHAR \_ тâ \**_, [_ *Byte* \*](byte.md), \**битеâ \** _ и [_*воидâ \**_](void.md).</span><span class="sxs-lookup"><span data-stu-id="7c6a6-109">Valid MIDL types include [**small**](small.md), [**short**](short.md), [**long**](long.md), [**char**](char-idl.md), \**charÂ \**_, [_ *wchar\_t*\*](wchar-t.md), \**wchar\_tÂ \**_, [_ *byte*\*](byte.md), \**byteÂ \** _, and [_*voidÂ \**_](void.md).</span></span> <span data-ttu-id="7c6a6-110">Типы integer и character могут быть знаками [ \* _](signed.md) или [**без знака**](unsigned.md).</span><span class="sxs-lookup"><span data-stu-id="7c6a6-110">The integer and character types can be [_ *signed*\*](signed.md) or [**unsigned**](unsigned.md).</span></span>

</dd> <dt>

<span data-ttu-id="7c6a6-111">*identifier*</span><span class="sxs-lookup"><span data-stu-id="7c6a6-111">*identifier*</span></span> 
</dt> <dd>

<span data-ttu-id="7c6a6-112">Указывает допустимый идентификатор MIDL.</span><span class="sxs-lookup"><span data-stu-id="7c6a6-112">Specifies a valid MIDL identifier.</span></span> <span data-ttu-id="7c6a6-113">Допустимые идентификаторы MIDL состоят из символов длиной до 31 алфавитно-цифровых и знаков подчеркивания и должны начинаться с символа алфавита или знака подчеркивания.</span><span class="sxs-lookup"><span data-stu-id="7c6a6-113">Valid MIDL identifiers consist of up to 31 alphanumeric and/or underscore characters and must start with an alphabetic or underscore character.</span></span>

</dd> <dt>

<span data-ttu-id="7c6a6-114">*const-выражение*</span><span class="sxs-lookup"><span data-stu-id="7c6a6-114">*const-expression*</span></span> 
</dt> <dd>

<span data-ttu-id="7c6a6-115">Указывает выражение, идентификатор или цифровую или символьную константу, подходящую для указанного типа: константные целочисленные литералы или константные целочисленные выражения для целочисленных констант. Логические выражения, которые могут быть вычислены при компиляции для [**логических**](boolean.md) типов; Односимвольные константы для типов [**char**](char-idl.md) ; и строковые константы для **\[** [**строковых**](string.md) **\]** типов.</span><span class="sxs-lookup"><span data-stu-id="7c6a6-115">Specifies an expression, identifier, or numeric or character constant appropriate for the specified type: constant integer literals or constant integer expressions for integer constants; Boolean expressions that can be computed at compilation for [**Boolean**](boolean.md) types; single-character constants for [**char**](char-idl.md) types; and string constants for **\[**[**string**](string.md)**\]** types.</span></span> <span data-ttu-id="7c6a6-116">Тип [ \* *воидâ \** _](void.md) может быть инициализирован только значением _ \* null \* \*.</span><span class="sxs-lookup"><span data-stu-id="7c6a6-116">The [\**voidÂ \** _](void.md) type can be initialized only to _\*NULL\*\*.</span></span>

</dd> <dt>

<span data-ttu-id="7c6a6-117">*Type-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="7c6a6-117">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="7c6a6-118">Указывает один или несколько атрибутов, применяемых к типу.</span><span class="sxs-lookup"><span data-stu-id="7c6a6-118">Specifies one or more attributes that apply to the type.</span></span>

</dd> <dt>

<span data-ttu-id="7c6a6-119">*pointer-type*</span><span class="sxs-lookup"><span data-stu-id="7c6a6-119">*pointer-type*</span></span> 
</dt> <dd>

<span data-ttu-id="7c6a6-120">Указывает допустимый тип указателя MIDL.</span><span class="sxs-lookup"><span data-stu-id="7c6a6-120">Specifies a valid MIDL pointer type.</span></span>

</dd> <dt>

<span data-ttu-id="7c6a6-121">*декларатор и декларатор-список*</span><span class="sxs-lookup"><span data-stu-id="7c6a6-121">*declarator and declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="7c6a6-122">Задает стандартные деклараторы C, такие как идентификаторы, деклараторы указателей и деклараторы массивов.</span><span class="sxs-lookup"><span data-stu-id="7c6a6-122">Specifies standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="7c6a6-123">Дополнительные сведения см. в разделе [атрибуты Array и Sized-Pointer](array-and-sized-pointer-attributes.md), [**массивы**](arrays-1.md), [массивы и указатели](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="7c6a6-123">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="7c6a6-124">*Список деклараторов* состоит из одного или нескольких деклараторов, разделенных запятыми.</span><span class="sxs-lookup"><span data-stu-id="7c6a6-124">The *declarator-list* consists of one or more declarators, separated by commas.</span></span> <span data-ttu-id="7c6a6-125">Идентификатор параметра-Name в деклараторе функции является необязательным.</span><span class="sxs-lookup"><span data-stu-id="7c6a6-125">The parameter-name identifier in the function declarator is optional.</span></span>

</dd> <dt>

<span data-ttu-id="7c6a6-126">*Function-attr-список*</span><span class="sxs-lookup"><span data-stu-id="7c6a6-126">*function-attr-list*</span></span> 
</dt> <dd>

<span data-ttu-id="7c6a6-127">Указывает ноль или более атрибутов, которые применяются к функции.</span><span class="sxs-lookup"><span data-stu-id="7c6a6-127">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="7c6a6-128">Допустимые атрибуты функции — **\[** [**обратный вызов**](callback.md) **\]** , **\[** [**локальный**](local.md) **\]** объект, атрибут указателя **\[** [**ref**](ref.md) **\]** , **\[** [**UNIQUE**](unique.md) **\]** или **\[** [**ptr**](ptr.md) **\]** ; и атрибуты использования **\[** [**строка**](string.md) **\]** , **\[** [**Ignore**](ignore.md) **\]** и **\[** [**Контекстный \_ маркер**](context-handle.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="7c6a6-128">Valid function attributes are **\[**[**callback**](callback.md)**\]**, **\[**[**local**](local.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**string**](string.md)**\]**, **\[**[**ignore**](ignore.md)**\]**, and **\[**[**context\_handle**](context-handle.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="7c6a6-129">*Описатель типа*</span><span class="sxs-lookup"><span data-stu-id="7c6a6-129">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="7c6a6-130">Задает [Базовый \_ тип](midl-base-types.md), [**структуру**](struct.md), [**объединение**](union.md), тип [**перечисления**](enum.md) или идентификатор типа.</span><span class="sxs-lookup"><span data-stu-id="7c6a6-130">Specifies a [base\_type](midl-base-types.md), [**struct**](struct.md), [**union**](union.md), [**enum**](enum.md) type, or type identifier.</span></span> <span data-ttu-id="7c6a6-131">Дополнительная спецификация хранилища может предшествовать *спецификатору типа*.</span><span class="sxs-lookup"><span data-stu-id="7c6a6-131">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="7c6a6-132">*PTR-decl*</span><span class="sxs-lookup"><span data-stu-id="7c6a6-132">*ptr-decl*</span></span> 
</dt> <dd>

<span data-ttu-id="7c6a6-133">Указывает ноль или несколько деклараторов указателей.</span><span class="sxs-lookup"><span data-stu-id="7c6a6-133">Specifies zero or more pointer declarators.</span></span> <span data-ttu-id="7c6a6-134">Декларатор указателя аналогичен декларатору указателя, используемому в C. Он состоит из **\* *_ указателя, модификаторов, таких как _* FAR**, и квалификатора **const**.</span><span class="sxs-lookup"><span data-stu-id="7c6a6-134">A pointer declarator is the same as the pointer declarator used in C. It is constructed from the \**\**_ designator, modifiers such as _\* far\*\*, and the qualifier **const**.</span></span>

</dd> <dt>

<span data-ttu-id="7c6a6-135">*имя функции*</span><span class="sxs-lookup"><span data-stu-id="7c6a6-135">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="7c6a6-136">Задает имя удаленной процедуры.</span><span class="sxs-lookup"><span data-stu-id="7c6a6-136">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="7c6a6-137">*Parameter-список атрибутов*</span><span class="sxs-lookup"><span data-stu-id="7c6a6-137">*parameter-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="7c6a6-138">Указывает ноль или более атрибутов направления, атрибутов полей, атрибутов использования и атрибутов указателя, подходящих для указанного типа параметра.</span><span class="sxs-lookup"><span data-stu-id="7c6a6-138">Specifies zero or more directional attributes, field attributes, usage attributes, and pointer attributes appropriate for the specified parameter type.</span></span> <span data-ttu-id="7c6a6-139">Несколько атрибутов разделяются запятыми.</span><span class="sxs-lookup"><span data-stu-id="7c6a6-139">Separate multiple attributes with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7c6a6-140">Remarks</span><span class="sxs-lookup"><span data-stu-id="7c6a6-140">Remarks</span></span>

<span data-ttu-id="7c6a6-141">MIDL позволяет объявлять константные целочисленные, символьные, строковые и логические типы в теле интерфейса IDL-файла.</span><span class="sxs-lookup"><span data-stu-id="7c6a6-141">MIDL allows you to declare constant integer, character, string, and Boolean types in the interface body of the IDL file.</span></span> <span data-ttu-id="7c6a6-142">Объявления типов **const** воссоздаются в создаваемом файле заголовка как директивы **\# define** .</span><span class="sxs-lookup"><span data-stu-id="7c6a6-142">**Const** type declarations are reproduced in the generated header file as **\#define** directives.</span></span>

<span data-ttu-id="7c6a6-143">Компиляторы DCE IDL не поддерживают константные выражения.</span><span class="sxs-lookup"><span data-stu-id="7c6a6-143">DCE IDL compilers do not support constant expressions.</span></span> <span data-ttu-id="7c6a6-144">Поэтому эта функция недоступна при использовании параметра компилятора MIDL [**/ОСФ**](-osf.md) .</span><span class="sxs-lookup"><span data-stu-id="7c6a6-144">Therefore, this feature is not available when you use the MIDL compiler [**/osf**](-osf.md) switch.</span></span>

<span data-ttu-id="7c6a6-145">Ранее определенная константа может использоваться как присвоенное значение последующей константы.</span><span class="sxs-lookup"><span data-stu-id="7c6a6-145">A previously defined constant can be used as the assigned value of a subsequent constant.</span></span> <span data-ttu-id="7c6a6-146">Значение константного целочисленного выражения автоматически преобразуется в соответствующий целочисленный тип в соответствии с правилами преобразования C.</span><span class="sxs-lookup"><span data-stu-id="7c6a6-146">The value of a constant integral expression is automatically converted to the respective integer type in accordance with C conversion rules.</span></span>

<span data-ttu-id="7c6a6-147">Значение символьной константы должно быть символом ASCII с одинарной кавычкой.</span><span class="sxs-lookup"><span data-stu-id="7c6a6-147">The value of a character constant must be a single-quoted ASCII character.</span></span> <span data-ttu-id="7c6a6-148">Если символьная константа является самой одинарной кавычкой ('), символ обратной косой черты ( \\ ) должен предшествовать символу одинарной кавычки, как в \\ .</span><span class="sxs-lookup"><span data-stu-id="7c6a6-148">When the character constant is the single-quote character itself ('), the backslash character (\\) must precede the single-quote character, as in \\'.</span></span>

<span data-ttu-id="7c6a6-149">Значение константы символьной строки должно быть строкой, заключенной в двойные кавычки.</span><span class="sxs-lookup"><span data-stu-id="7c6a6-149">The value of a character-string constant must be a double-quoted string.</span></span> <span data-ttu-id="7c6a6-150">В строке символ обратной косой черты ( **\\** ) должен предшествовать символу двойной кавычки ( **"** ), как в **\\ "**.</span><span class="sxs-lookup"><span data-stu-id="7c6a6-150">Within a string, the backslash (**\\**) character must precede a literal double-quote character ( **"** ), as in **\\"**.</span></span> <span data-ttu-id="7c6a6-151">В строке символ обратной косой черты ( **\\** ) представляет escape-символ.</span><span class="sxs-lookup"><span data-stu-id="7c6a6-151">Within a string, the backslash character (**\\**) represents an escape character.</span></span> <span data-ttu-id="7c6a6-152">Строковые константы могут состоять не более чем из 255 символов.</span><span class="sxs-lookup"><span data-stu-id="7c6a6-152">String constants can consist of up to 255 characters.</span></span>

<span data-ttu-id="7c6a6-153">Значение **null** является единственным допустимым значением для констант типа [ \* *\* воидâ* _](void.md).</span><span class="sxs-lookup"><span data-stu-id="7c6a6-153">The value **NULL** is the only valid value for constants of type [\**voidÂ \** _](void.md).</span></span> <span data-ttu-id="7c6a6-154">Все атрибуты, связанные с объявлением _ \*const\*\*, игнорируются.</span><span class="sxs-lookup"><span data-stu-id="7c6a6-154">Any attributes associated with the _ *const*\* declaration are ignored.</span></span>

<span data-ttu-id="7c6a6-155">Компилятор MIDL не проверяет наличие ошибок диапазона при инициализации **константы** .</span><span class="sxs-lookup"><span data-stu-id="7c6a6-155">The MIDL compiler does not check for range errors in **const** initialization.</span></span> <span data-ttu-id="7c6a6-156">Например, при указании "const Short x = 0xFFFFFFFF;" компилятор MIDL не сообщает об ошибке, а инициализатор воспроизводится в создаваемом файле заголовка.</span><span class="sxs-lookup"><span data-stu-id="7c6a6-156">For example, when you specify "const short x = 0xFFFFFFFF;" the MIDL compiler does not report an error and the initializer is reproduced in the generated header file.</span></span>

## <a name="examples"></a><span data-ttu-id="7c6a6-157">Примеры</span><span class="sxs-lookup"><span data-stu-id="7c6a6-157">Examples</span></span>

``` syntax
const void *  p1        = NULL; 
const char    my_char1  = 'a'; 
const char    my_char2  = my_char1; 
const wchar_t my_wchar3 = L'a'; 
const wchar_t * pszNote = L"Note"; 
const unsigned short int x = 123; 
 
typedef [string] const char *LPCSTR; 
 
HRESULT GetName([out] wchar_t * const pszName );
```

## <a name="see-also"></a><span data-ttu-id="7c6a6-158">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7c6a6-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c6a6-159">**массивы**</span><span class="sxs-lookup"><span data-stu-id="7c6a6-159">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="7c6a6-160">Базовые типы MIDL</span><span class="sxs-lookup"><span data-stu-id="7c6a6-160">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="7c6a6-161">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="7c6a6-161">**Boolean**</span></span>](boolean.md)
</dt> <dt>

[<span data-ttu-id="7c6a6-162">**двухбайтовых**</span><span class="sxs-lookup"><span data-stu-id="7c6a6-162">**byte**</span></span>](byte.md)
</dt> <dt>

[<span data-ttu-id="7c6a6-163">**обратный вызов**</span><span class="sxs-lookup"><span data-stu-id="7c6a6-163">**callback**</span></span>](callback.md)
</dt> <dt>

[<span data-ttu-id="7c6a6-164">**типа**</span><span class="sxs-lookup"><span data-stu-id="7c6a6-164">**char**</span></span>](char-idl.md)
</dt> <dt>

[<span data-ttu-id="7c6a6-165">**Контекстный \_ маркер**</span><span class="sxs-lookup"><span data-stu-id="7c6a6-165">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="7c6a6-166">**перечисления**</span><span class="sxs-lookup"><span data-stu-id="7c6a6-166">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="7c6a6-167">Файл определения интерфейса (IDL)</span><span class="sxs-lookup"><span data-stu-id="7c6a6-167">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="7c6a6-168">**обращать**</span><span class="sxs-lookup"><span data-stu-id="7c6a6-168">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="7c6a6-169">**Языковые**</span><span class="sxs-lookup"><span data-stu-id="7c6a6-169">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="7c6a6-170">**поддерживаем**</span><span class="sxs-lookup"><span data-stu-id="7c6a6-170">**long**</span></span>](long.md)
</dt> <dt>

[<span data-ttu-id="7c6a6-171">**/осф**</span><span class="sxs-lookup"><span data-stu-id="7c6a6-171">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="7c6a6-172">**указатель**</span><span class="sxs-lookup"><span data-stu-id="7c6a6-172">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="7c6a6-173">**ref**</span><span class="sxs-lookup"><span data-stu-id="7c6a6-173">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="7c6a6-174">**short**</span><span class="sxs-lookup"><span data-stu-id="7c6a6-174">**short**</span></span>](short.md)
</dt> <dt>

[<span data-ttu-id="7c6a6-175">**входил**</span><span class="sxs-lookup"><span data-stu-id="7c6a6-175">**signed**</span></span>](signed.md)
</dt> <dt>

[<span data-ttu-id="7c6a6-176">**значительные**</span><span class="sxs-lookup"><span data-stu-id="7c6a6-176">**small**</span></span>](small.md)
</dt> <dt>

[<span data-ttu-id="7c6a6-177">**Строка**</span><span class="sxs-lookup"><span data-stu-id="7c6a6-177">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="7c6a6-178">**struct**</span><span class="sxs-lookup"><span data-stu-id="7c6a6-178">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="7c6a6-179">**наборов**</span><span class="sxs-lookup"><span data-stu-id="7c6a6-179">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="7c6a6-180">**unique**</span><span class="sxs-lookup"><span data-stu-id="7c6a6-180">**unique**</span></span>](unique.md)
</dt> <dt>

[<span data-ttu-id="7c6a6-181">**без знака**</span><span class="sxs-lookup"><span data-stu-id="7c6a6-181">**unsigned**</span></span>](unsigned.md)
</dt> <dt>

[<span data-ttu-id="7c6a6-182">**void**</span><span class="sxs-lookup"><span data-stu-id="7c6a6-182">**void**</span></span>](void.md)
</dt> <dt>

[<span data-ttu-id="7c6a6-183">**WCHAR \_ t**</span><span class="sxs-lookup"><span data-stu-id="7c6a6-183">**wchar\_t**</span></span>](wchar-t.md)
</dt> </dl>

 

 