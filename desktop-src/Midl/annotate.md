---
title: атрибут аннотации
description: Атрибут \ Annotations позволяет указать строку аннотации SAL для указанного метода, параметра или поля структуры.
ms.assetid: D0A35DCD-BD2F-455B-A040-5D63E4572D83
keywords:
- атрибут аннотации MIDL
topic_type:
- apiref
api_name:
- annotate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 820310c6aca0e5269d6febff5dc7d3208413110c
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/08/2020
ms.locfileid: "103795216"
---
# <a name="annotate-attribute"></a><span data-ttu-id="4eb44-104">атрибут аннотации</span><span class="sxs-lookup"><span data-stu-id="4eb44-104">annotate attribute</span></span>

<span data-ttu-id="4eb44-105">Атрибут **\[ аннотации \]** позволяет указать строку аннотации SAL для указанного метода, параметра или поля структуры.</span><span class="sxs-lookup"><span data-stu-id="4eb44-105">The **\[annotate\]** attribute allows you to specify a SAL annotation string for the specified method, parameter, or structure field.</span></span>

``` syntax
[ annotation(â€œstringâ€0,  [, function-attribute-list] ] function-declarator ;
[ [function-attribute-list] ] type-specifier [pointer-declarator] function-name(
    [ annotation(â€œstringâ€) [ , parameter-attribute-list ] ] type-specifier [declarator]
    , ...);
```

## <a name="parameters"></a><span data-ttu-id="4eb44-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4eb44-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4eb44-107">*string*</span><span class="sxs-lookup"><span data-stu-id="4eb44-107">*string*</span></span> 
</dt> <dd>

<span data-ttu-id="4eb44-108">Указанная строка аннотации SAL.</span><span class="sxs-lookup"><span data-stu-id="4eb44-108">Specified SAL annotation string.</span></span>

</dd> <dt>

<span data-ttu-id="4eb44-109">*Function-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="4eb44-109">*function-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="4eb44-110">Указывает ноль или более атрибутов, которые применяются к функции.</span><span class="sxs-lookup"><span data-stu-id="4eb44-110">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="4eb44-111">Допустимые атрибуты функции включают [**\[ \] обратный вызов**](callback.md), атрибуты указателя [**\[ ref \]**](ref.md), [**\[ Unique \]**](unique.md)или [**\[ ptr \]**](ptr.md); и атрибуты использования [**\[ строка \]**](string.md), [**\[ Ignore \]**](ignore.md)и [**\[ Контекстный \_ маркер \]**](context-handle.md).</span><span class="sxs-lookup"><span data-stu-id="4eb44-111">Valid function attributes include [**\[callback\]**](callback.md); the pointer attributes [**\[ref\]**](ref.md), [**\[unique\]**](unique.md), or [**\[ptr\]**](ptr.md); and the usage attributes [**\[string\]**](string.md), [**\[ignore\]**](ignore.md), and [**\[context\_handle\]**](context-handle.md).</span></span> <span data-ttu-id="4eb44-112">Несколько атрибутов должны быть разделены запятыми.</span><span class="sxs-lookup"><span data-stu-id="4eb44-112">Multiple attributes must be separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="4eb44-113">*декларатор функции*</span><span class="sxs-lookup"><span data-stu-id="4eb44-113">*function-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="4eb44-114">Указывает спецификатор типа, имя функции и список параметров для функции.</span><span class="sxs-lookup"><span data-stu-id="4eb44-114">Specifies the type specifier, function name, and parameter list for the function.</span></span>

</dd> <dt>

<span data-ttu-id="4eb44-115">*Описатель типа*</span><span class="sxs-lookup"><span data-stu-id="4eb44-115">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="4eb44-116">Задает **Базовый \_ тип**, [**\[ структуру \]**](struct.md), [**объединение**](union.md)или тип [**\[ перечисления \]**](enum.md) или идентификатор типа.</span><span class="sxs-lookup"><span data-stu-id="4eb44-116">Specifies a **base\_type**, [**\[struct\]**](struct.md), [**union**](union.md), or [**\[enum\]**](enum.md) type or type identifier.</span></span> <span data-ttu-id="4eb44-117">Дополнительная спецификация хранилища может предшествовать *спецификатору типа*.</span><span class="sxs-lookup"><span data-stu-id="4eb44-117">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="4eb44-118">*декларатор указателя*</span><span class="sxs-lookup"><span data-stu-id="4eb44-118">*pointer-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="4eb44-119">Указывает ноль или несколько деклараторов указателей.</span><span class="sxs-lookup"><span data-stu-id="4eb44-119">Specifies zero or more pointer declarators.</span></span> <span data-ttu-id="4eb44-120">Декларатор указателя аналогичен декларатору указателя, используемому в C; Он создается из \* указателя, модификаторов, таких как **FAR**, и квалификатора [**\[ const \]**](const.md).</span><span class="sxs-lookup"><span data-stu-id="4eb44-120">A pointer declarator is the same as a pointer declarator used in C; it is constructed from the \* designator, modifiers such as **far**, and the qualifier [**\[const\]**](const.md).</span></span>

</dd> <dt>

<span data-ttu-id="4eb44-121">*имя функции*</span><span class="sxs-lookup"><span data-stu-id="4eb44-121">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="4eb44-122">Задает имя удаленной процедуры.</span><span class="sxs-lookup"><span data-stu-id="4eb44-122">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="4eb44-123">*Parameter-список атрибутов*</span><span class="sxs-lookup"><span data-stu-id="4eb44-123">*parameter-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="4eb44-124">Указывает ноль или более атрибутов, подходящих для типа параметра.</span><span class="sxs-lookup"><span data-stu-id="4eb44-124">Specifies zero or more attributes appropriate for the parameter type.</span></span> <span data-ttu-id="4eb44-125">Атрибуты параметров с атрибутом [**\[ in \]**](in.md) также могут [**\[ \] принимать атрибут направления, а атрибуты**](out-idl.md)Field [**\[ \_ \] —**](first-is.md), [**\[ Last \_ - \]**](last-is.md), [**\[ length \_ — \]**](length-is.md), [**\[ Max \_ — \]**](max-is.md), [**\[ size \_ — \]**](size-is.md)и [**\[ \_ тип \] переключателя**](switch-type.md); атрибуты указателя [**\[ ref \]**](ref.md), [**\[ Unique \]**](unique.md)или [**\[ ptr \]**](ptr.md), а также [**\[ \_ описатель \] контекста**](context-handle.md) атрибутов использования и [**\[ строка \]**](string.md).</span><span class="sxs-lookup"><span data-stu-id="4eb44-125">Parameter attributes with the [**\[in\]**](in.md) attribute can also take the directional attribute [**\[out\]**](out-idl.md); the field attributes [**\[first\_is\]**](first-is.md), [**\[last\_is\]**](last-is.md), [**\[length\_is\]**](length-is.md), [**\[max\_is\]**](max-is.md), [**\[size\_is\]**](size-is.md), and [**\[switch\_type\]**](switch-type.md); the pointer attributes [**\[ref\]**](ref.md), [**\[unique\]**](unique.md), or [**\[ptr\]**](ptr.md); and the usage attributes [**\[context\_handle\]**](context-handle.md) and [**\[string\]**](string.md).</span></span> <span data-ttu-id="4eb44-126">Атрибут использования [**\[ Ignore \]**](ignore.md) не может использоваться в качестве атрибута параметра.</span><span class="sxs-lookup"><span data-stu-id="4eb44-126">The usage attribute [**\[ignore\]**](ignore.md) cannot be used as a parameter attribute.</span></span> <span data-ttu-id="4eb44-127">Несколько атрибутов должны быть разделены запятыми.</span><span class="sxs-lookup"><span data-stu-id="4eb44-127">Multiple attributes must be separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="4eb44-128">*declarator*</span><span class="sxs-lookup"><span data-stu-id="4eb44-128">*declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="4eb44-129">Задает стандартные деклараторы C, такие как идентификаторы, деклараторы указателей и деклараторы массивов.</span><span class="sxs-lookup"><span data-stu-id="4eb44-129">Specifies standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="4eb44-130">Дополнительные сведения см. в разделе [атрибуты Array и Sized-Pointer](array-and-sized-pointer-attributes.md), [**\[ массивы \]**](../rpc/arrays.md), [массивы и указатели](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="4eb44-130">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**\[arrays\]**](../rpc/arrays.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="4eb44-131">Декларатор параметра в деклараторе функции, например имя параметра, является необязательным.</span><span class="sxs-lookup"><span data-stu-id="4eb44-131">The parameter declarator in the function declarator, such as the parameter name, is optional.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4eb44-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4eb44-132">Remarks</span></span>

<span data-ttu-id="4eb44-133">Атрибут Annotations позволяет переопределять созданные с помощью MIDL аннотации SAL или добавлять их в местах, где MIDL не создает аннотацию явным образом. **\[ \]**</span><span class="sxs-lookup"><span data-stu-id="4eb44-133">The **\[annotate\]** attribute allows overriding MIDL-generated SAL annotations or adding them in places where MIDL does not explicitly generate an annotation.</span></span> <span data-ttu-id="4eb44-134">Если [**/Сал**](-sal.md) не указан в командной строке, этот атрибут игнорируется.</span><span class="sxs-lookup"><span data-stu-id="4eb44-134">If [**/sal**](-sal.md) is not specified on the command line, this attribute is ignored.</span></span>

## <a name="see-also"></a><span data-ttu-id="4eb44-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4eb44-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4eb44-136">Общий синтаксис командной строки MIDL</span><span class="sxs-lookup"><span data-stu-id="4eb44-136">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="4eb44-137">**/сал**</span><span class="sxs-lookup"><span data-stu-id="4eb44-137">**/sal**</span></span>](-sal.md)
</dt> <dt>

[<span data-ttu-id="4eb44-138">**/Сал \_ локальный**</span><span class="sxs-lookup"><span data-stu-id="4eb44-138">**/sal\_local**</span></span>](-sal-local.md)
</dt> </dl>

 

 