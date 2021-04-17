---
title: Array, атрибут
description: Массивы представляют собой однородные коллекции данных, доступ к которым осуществляется по индексу или номеру элемента.
ms.assetid: 375fb795-8f18-45b7-898c-99f1273746d8
keywords:
- массив с атрибутом MIDL
topic_type:
- apiref
api_name:
- arrays
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e189eb1784a4ff24b799c7a4d4482d0f56b20e3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "105681536"
---
# <a name="arrays-attribute"></a><span data-ttu-id="c1d29-104">Array, атрибут</span><span class="sxs-lookup"><span data-stu-id="c1d29-104">arrays attribute</span></span>

<span data-ttu-id="c1d29-105">Массивы представляют собой однородные коллекции данных, доступ к которым осуществляется по индексу или номеру элемента.</span><span class="sxs-lookup"><span data-stu-id="c1d29-105">Arrays are homogenous collections of data accessed by an index or element number.</span></span>

``` syntax
typedef [ [type-attr-list] ] type-specifier [pointer-decl] array-declarator;

typedef [ [type-attr-list] ] struct [ tag ] 
{
    [ [ field-attribute-list ] ] type-specifier [pointer-decl] array-declarator;
    ...
};

typedef [ [type-attr-list] ] union [ tag ] 
{
    [ case (limited-expression [ , ... ] ) ]
  [ [ field-attribute-list ] ] type-specifier [pointer-decl] array-declarator;
  [ [ default ]
  [ [ field-attribute-list ] ] type-specifier [pointer-decl] array-declarator;
  ]
};

[[ [function-attribute-list] ]] type-specifier [[pointer-decl]] function-name(
        [[ [param-attr-list] ]] type-specifier [[pointer-decl]] array-declarator
        , ...);
```

## <a name="parameters"></a><span data-ttu-id="c1d29-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c1d29-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1d29-107">*Тип-attr-список*</span><span class="sxs-lookup"><span data-stu-id="c1d29-107">*type-attr-list*</span></span> 
</dt> <dd>

<span data-ttu-id="c1d29-108">Указывает ноль или более атрибутов, которые применяются к типу.</span><span class="sxs-lookup"><span data-stu-id="c1d29-108">Specifies zero or more attributes that apply to the type.</span></span> <span data-ttu-id="c1d29-109">К допустимым атрибутам типа относятся [**\[ \] Handle**](handle.md), [**\[ Switch \_ Type \]**](switch-type.md), [**\[ передает \_ As \]**](transmit-as.md); атрибут указателя [**\[ ref \]**](ref.md), [**\[ Unique \]**](unique.md)или [**\[ ptr \]**](ptr.md);, а также [**\[ \_ маркер \] контекста**](context-handle.md)атрибутов использования, [**\[ String \]**](string.md)и [**\[ Ignore \]**](ignore.md).</span><span class="sxs-lookup"><span data-stu-id="c1d29-109">Valid type attributes include [**\[handle\]**](handle.md), [**\[switch\_type\]**](switch-type.md), [**\[transmit\_as\]**](transmit-as.md); the pointer attribute [**\[ref\]**](ref.md), [**\[unique\]**](unique.md), or [**\[ptr\]**](ptr.md); and the usage attributes [**\[context\_handle\]**](context-handle.md), [**\[string\]**](string.md), and [**\[ignore\]**](ignore.md).</span></span> <span data-ttu-id="c1d29-110">Несколько атрибутов разделяются запятыми.</span><span class="sxs-lookup"><span data-stu-id="c1d29-110">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="c1d29-111">*Описатель типа*</span><span class="sxs-lookup"><span data-stu-id="c1d29-111">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="c1d29-112">Задает идентификатор типа, базовый тип, [**структуру**](struct.md), [**объединение**](union.md)или тип [**перечисления**](enum.md) .</span><span class="sxs-lookup"><span data-stu-id="c1d29-112">Specifies the type identifier, base type, [**struct**](struct.md), [**union**](union.md), or [**enum**](enum.md) type.</span></span> <span data-ttu-id="c1d29-113">Спецификация типа может включать в себя дополнительную спецификацию хранилища.</span><span class="sxs-lookup"><span data-stu-id="c1d29-113">The type specification can include an optional storage specification.</span></span>

</dd> <dt>

<span data-ttu-id="c1d29-114">*pointer-decl*</span><span class="sxs-lookup"><span data-stu-id="c1d29-114">*pointer-decl*</span></span> 
</dt> <dd>

<span data-ttu-id="c1d29-115">Указывает ноль или несколько деклараторов указателей.</span><span class="sxs-lookup"><span data-stu-id="c1d29-115">Specifies zero or more pointer declarators.</span></span> <span data-ttu-id="c1d29-116">Декларатор указателя аналогичен декларатору указателя, используемому в языке C, созданному из **\*** указателя, модификаторов, таких как **FAR**, и квалификатора [**const**](const.md).</span><span class="sxs-lookup"><span data-stu-id="c1d29-116">A pointer declarator is the same as the pointer declarator used in C, constructed from the **\*** designator, modifiers such as **far**, and the qualifier [**const**](const.md).</span></span>

</dd> <dt>

<span data-ttu-id="c1d29-117">*декларатор массива*</span><span class="sxs-lookup"><span data-stu-id="c1d29-117">*array-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="c1d29-118">Задает имя массива, за которым следуют одна из следующих конструкций для каждого измерения массива: "**\[ \]**", " **\[\*\]** ", "**\[ ***Const1*** \]**" или "**\[ ***Lower...*** Upper \]**", где" *снизу* "и" *верхний* "являются константными значениями, представляющими нижнюю и верхнюю границы.</span><span class="sxs-lookup"><span data-stu-id="c1d29-118">Specifies the name of the array, followed by one of the following constructs for each dimension of the array: "**\[ \]**", "**\[\*\]**", "**\[***const1***\]**", or "**\[***lower...upper***\]**" where *lower* and *upper* are constant values that represent the lower and upper bounds.</span></span> <span data-ttu-id="c1d29-119">Константа *ниже* должна иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="c1d29-119">The constant *lower* must evaluate to zero.</span></span>

</dd> <dt>

<span data-ttu-id="c1d29-120">*тегами*</span><span class="sxs-lookup"><span data-stu-id="c1d29-120">*tag*</span></span> 
</dt> <dd>

<span data-ttu-id="c1d29-121">Указывает необязательный тег для структуры или объединения.</span><span class="sxs-lookup"><span data-stu-id="c1d29-121">Specifies an optional tag for the structure or union.</span></span>

</dd> <dt>

<span data-ttu-id="c1d29-122">*Список атрибутов Field*</span><span class="sxs-lookup"><span data-stu-id="c1d29-122">*field-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="c1d29-123">Указывает ноль или более атрибутов полей, применимых к структуре, члену объединения или параметру функции.</span><span class="sxs-lookup"><span data-stu-id="c1d29-123">Specifies zero or more field attributes that apply to the structure, union member, or function parameter.</span></span> <span data-ttu-id="c1d29-124">К допустимым атрибутам полей относятся: [**\[ \_ \] First**](first-is.md)—, [**\[ Last \_ — \]**](last-is.md), [**\[ length \_ — \]**](length-is.md), [**\[ Max \_ — \]**](max-is.md), [**\[ size \_ — \]**](size-is.md), [**\[ строка \]**](string.md)атрибутов использования и [**\[ игнорируется \]**](ignore.md); атрибуты указателя [**\[ ref \]**](ref.md), [**\[ Unique \]**](unique.md)и [**\[ ptr \]**](ptr.md); и [**\[ \_ тип \] переключателя**](switch-type.md)атрибута объединения.</span><span class="sxs-lookup"><span data-stu-id="c1d29-124">Valid field attributes include [**\[first\_is\]**](first-is.md), [**\[last\_is\]**](last-is.md), [**\[length\_is\]**](length-is.md), [**\[max\_is\]**](max-is.md), [**\[size\_is\]**](size-is.md); the usage attributes [**\[string\]**](string.md), and [**\[ignore\]**](ignore.md); the pointer attributes [**\[ref\]**](ref.md), [**\[unique\]**](unique.md), and [**\[ptr\]**](ptr.md); and the union attribute [**\[switch\_type\]**](switch-type.md).</span></span> <span data-ttu-id="c1d29-125">Несколько атрибутов полей разделяются запятыми.</span><span class="sxs-lookup"><span data-stu-id="c1d29-125">Separate multiple field attributes with commas.</span></span> <span data-ttu-id="c1d29-126">Обратите внимание, что из перечисленных выше атрибутов, « **\[ первый \_ \]**», « **\[ последний \_ \]**» и « [**\[ игнорирует \]**](ignore.md) », недопустимы для объединений.</span><span class="sxs-lookup"><span data-stu-id="c1d29-126">Note that of the attributes listed above, **\[first\_is\]**, **\[last\_is\]**, and [**\[ignore\]**](ignore.md) are not valid for unions.</span></span>

</dd> <dt>

<span data-ttu-id="c1d29-127">*ограниченное выражение*</span><span class="sxs-lookup"><span data-stu-id="c1d29-127">*limited-expression*</span></span> 
</dt> <dd>

<span data-ttu-id="c1d29-128">Указывает выражение языка C.</span><span class="sxs-lookup"><span data-stu-id="c1d29-128">Specifies a C-language expression.</span></span> <span data-ttu-id="c1d29-129">Компилятор MIDL поддерживает условные выражения, логические выражения, реляционные выражения и арифметические выражения.</span><span class="sxs-lookup"><span data-stu-id="c1d29-129">The MIDL compiler supports conditional expressions, logical expressions, relational expressions, and arithmetic expressions.</span></span> <span data-ttu-id="c1d29-130">MIDL не разрешает вызовы функций в выражениях и не поддерживает операторы инкремента и декремента.</span><span class="sxs-lookup"><span data-stu-id="c1d29-130">MIDL does not allow function invocations in expressions and does not allow increment and decrement operators.</span></span>

</dd> <dt>

<span data-ttu-id="c1d29-131">*Function-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="c1d29-131">*function-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="c1d29-132">Указывает ноль или более атрибутов, которые применяются к функции.</span><span class="sxs-lookup"><span data-stu-id="c1d29-132">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="c1d29-133">Допустимые атрибуты функции — [**\[ обратный \] вызов**](callback.md), [**\[ локальный \]**](local.md)объект, атрибут указателя [**\[ ref \]**](ref.md), [**\[ Unique \]**](unique.md)или [**\[ ptr \]**](ptr.md), а также [**\[ строка \]**](string.md)атрибутов использования и [**\[ Контекстный \_ маркер \]**](context-handle.md).</span><span class="sxs-lookup"><span data-stu-id="c1d29-133">Valid function attributes are [**\[callback\]**](callback.md), [**\[local\]**](local.md); the pointer attribute [**\[ref\]**](ref.md), [**\[unique\]**](unique.md), or [**\[ptr\]**](ptr.md); and the usage attributes [**\[string\]**](string.md), and [**\[context\_handle\]**](context-handle.md).</span></span>

</dd> <dt>

<span data-ttu-id="c1d29-134">*имя функции*</span><span class="sxs-lookup"><span data-stu-id="c1d29-134">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="c1d29-135">Задает имя удаленной процедуры.</span><span class="sxs-lookup"><span data-stu-id="c1d29-135">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="c1d29-136">*Param-attr-список*</span><span class="sxs-lookup"><span data-stu-id="c1d29-136">*param-attr-list*</span></span> 
</dt> <dd>

<span data-ttu-id="c1d29-137">Задает атрибуты направления и один или несколько необязательных атрибутов поля, которые применяются к параметру массива.</span><span class="sxs-lookup"><span data-stu-id="c1d29-137">Specifies the directional attributes and one or more optional field attributes that apply to the array parameter.</span></span> <span data-ttu-id="c1d29-138">Допустимые атрибуты поля включают [**\[ Max \_ — \]**](max-is.md), [**\[ size \_ \] —**](size-is.md), [**\[ length \_ — \]**](length-is.md), [**\[ First \_ — \]**](first-is.md), а [**\[ Last \_ — \]**](last-is.md).</span><span class="sxs-lookup"><span data-stu-id="c1d29-138">Valid field attributes include [**\[max\_is\]**](max-is.md), [**\[size\_is\]**](size-is.md), [**\[length\_is\]**](length-is.md), [**\[first\_is\]**](first-is.md), and [**\[last\_is\]**](last-is.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c1d29-139">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c1d29-139">Remarks</span></span>

<span data-ttu-id="c1d29-140">Массивы в MIDL используют стиль, похожий на, но не точно такой же, как C и C++.</span><span class="sxs-lookup"><span data-stu-id="c1d29-140">Arrays in MIDL use a style similar to but not exactly the same as C and C++.</span></span> <span data-ttu-id="c1d29-141">Дополнительные сведения см. в разделе [MIDL Arrays](midl-arrays.md).</span><span class="sxs-lookup"><span data-stu-id="c1d29-141">For more information, see [MIDL Arrays](midl-arrays.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="c1d29-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c1d29-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1d29-143">**обратный вызов**</span><span class="sxs-lookup"><span data-stu-id="c1d29-143">**callback**</span></span>](callback.md)
</dt> <dt>

[<span data-ttu-id="c1d29-144">**const**</span><span class="sxs-lookup"><span data-stu-id="c1d29-144">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="c1d29-145">**Контекстный \_ маркер**</span><span class="sxs-lookup"><span data-stu-id="c1d29-145">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="c1d29-146">**перечисления**</span><span class="sxs-lookup"><span data-stu-id="c1d29-146">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="c1d29-147">**первый \_ —**</span><span class="sxs-lookup"><span data-stu-id="c1d29-147">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="c1d29-148">**справиться**</span><span class="sxs-lookup"><span data-stu-id="c1d29-148">**handle**</span></span>](handle.md)
</dt> <dt>

[<span data-ttu-id="c1d29-149">Файл определения интерфейса (IDL)</span><span class="sxs-lookup"><span data-stu-id="c1d29-149">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="c1d29-150">**обращать**</span><span class="sxs-lookup"><span data-stu-id="c1d29-150">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="c1d29-151">**Последний \_ —**</span><span class="sxs-lookup"><span data-stu-id="c1d29-151">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="c1d29-152">**Длина \_ равна**</span><span class="sxs-lookup"><span data-stu-id="c1d29-152">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="c1d29-153">**Языковые**</span><span class="sxs-lookup"><span data-stu-id="c1d29-153">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="c1d29-154">**Максимальное \_ число**</span><span class="sxs-lookup"><span data-stu-id="c1d29-154">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="c1d29-155">**ptr**</span><span class="sxs-lookup"><span data-stu-id="c1d29-155">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="c1d29-156">**ref**</span><span class="sxs-lookup"><span data-stu-id="c1d29-156">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="c1d29-157">**размер \_ равен**</span><span class="sxs-lookup"><span data-stu-id="c1d29-157">**size\_is**</span></span>](size-is.md)
</dt> <dt>

[<span data-ttu-id="c1d29-158">**Строка**</span><span class="sxs-lookup"><span data-stu-id="c1d29-158">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="c1d29-159">**struct**</span><span class="sxs-lookup"><span data-stu-id="c1d29-159">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="c1d29-160">**Тип коммутатора \_**</span><span class="sxs-lookup"><span data-stu-id="c1d29-160">**switch\_type**</span></span>](switch-type.md)
</dt> <dt>

[<span data-ttu-id="c1d29-161">**передать \_ как**</span><span class="sxs-lookup"><span data-stu-id="c1d29-161">**transmit\_as**</span></span>](transmit-as.md)
</dt> <dt>

[<span data-ttu-id="c1d29-162">**наборов**</span><span class="sxs-lookup"><span data-stu-id="c1d29-162">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="c1d29-163">**однозначно**</span><span class="sxs-lookup"><span data-stu-id="c1d29-163">**unique**</span></span>](unique.md)
</dt> </dl>

 

 




