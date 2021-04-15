---
title: out - атрибут
description: Атрибут \ out \ определяет параметры указателя, возвращаемые из вызванной процедуры в вызывающую процедуру (от сервера клиенту).
ms.assetid: f92ef78a-321b-460e-a18a-b63a5e199ad0
keywords:
- атрибут Out MIDL
topic_type:
- apiref
api_name:
- out
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b590cadeb12a77cff859991efb6356393072823
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105661714"
---
# <a name="out-attribute"></a><span data-ttu-id="da56e-104">out - атрибут</span><span class="sxs-lookup"><span data-stu-id="da56e-104">out attribute</span></span>

<span data-ttu-id="da56e-105">Атрибут \[ **out** \] определяет параметры указателя, возвращаемые из вызванной процедуры в вызывающую процедуру (от сервера клиенту).</span><span class="sxs-lookup"><span data-stu-id="da56e-105">The \[**out**\] attribute identifies pointer parameters that are returned from the called procedure to the calling procedure (from the server to the client).</span></span>

``` syntax
[ [function-attribute-list] ] type-specifier [pointer-declarator] function-name(
    [ out [ , parameter-attribute-list ] ] type-specifier [declarator]
    , ...
);
```

## <a name="parameters"></a><span data-ttu-id="da56e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="da56e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da56e-107">*Function-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="da56e-107">*function-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="da56e-108">Указывает ноль или более атрибутов, которые применяются к функции.</span><span class="sxs-lookup"><span data-stu-id="da56e-108">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="da56e-109">Допустимые атрибуты функции — \[ [**обратный вызов**](callback.md) \] , \[ [**локальный**](local.md) \] объект, атрибут указателя \[ [**ref**](ref.md) \] , \[ [**UNIQUE**](unique.md) \] или \[ [**ptr**](ptr.md) \] ; и атрибуты использования \[ [**строка**](string.md) \] , \[ [**Ignore**](ignore.md) \] и \[ [**Контекстный \_ маркер**](context-handle.md) \] .</span><span class="sxs-lookup"><span data-stu-id="da56e-109">Valid function attributes are \[[**callback**](callback.md)\], \[[**local**](local.md)\]; the pointer attribute \[[**ref**](ref.md)\], \[[**unique**](unique.md)\], or \[[**ptr**](ptr.md)\]; and the usage attributes \[[**string**](string.md)\], \[[**ignore**](ignore.md)\], and \[[**context\_handle**](context-handle.md)\].</span></span>

</dd> <dt>

<span data-ttu-id="da56e-110">*Описатель типа*</span><span class="sxs-lookup"><span data-stu-id="da56e-110">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="da56e-111">Задает [Базовый \_ тип](midl-base-types.md), [**структуру**](struct.md), [**объединение**](union.md)или тип [**перечисления**](enum.md) или идентификатор типа.</span><span class="sxs-lookup"><span data-stu-id="da56e-111">Specifies a [base\_type](midl-base-types.md), [**struct**](struct.md), [**union**](union.md), or [**enum**](enum.md) type or type identifier.</span></span> <span data-ttu-id="da56e-112">Дополнительная спецификация хранилища может предшествовать *спецификатору типа*.</span><span class="sxs-lookup"><span data-stu-id="da56e-112">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="da56e-113">*декларатор указателя*</span><span class="sxs-lookup"><span data-stu-id="da56e-113">*pointer-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="da56e-114">Указывает ноль или несколько деклараторов указателей.</span><span class="sxs-lookup"><span data-stu-id="da56e-114">Specifies zero or more pointer declarators.</span></span> <span data-ttu-id="da56e-115">Декларатор указателя аналогичен декларатору указателя, используемому в C; Он создается из \* указателя, модификаторов, таких как **FAR**, и квалификатора [**const**](const.md).</span><span class="sxs-lookup"><span data-stu-id="da56e-115">A pointer declarator is the same as the pointer declarator used in C; it is constructed from the \* designator, modifiers such as **far**, and the qualifier [**const**](const.md).</span></span>

</dd> <dt>

<span data-ttu-id="da56e-116">*имя функции*</span><span class="sxs-lookup"><span data-stu-id="da56e-116">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="da56e-117">Задает имя удаленной процедуры.</span><span class="sxs-lookup"><span data-stu-id="da56e-117">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="da56e-118">*Parameter-список атрибутов*</span><span class="sxs-lookup"><span data-stu-id="da56e-118">*parameter-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="da56e-119">Указывает ноль или более атрибутов, подходящих для указанного типа параметра.</span><span class="sxs-lookup"><span data-stu-id="da56e-119">Specifies zero or more attributes appropriate for a specified parameter type.</span></span> <span data-ttu-id="da56e-120">Атрибуты параметров с \[  \] атрибутом out также могут принимать атрибут Direction \[  \] . сначала атрибуты полей \[ [**\_**](first-is.md) \] , \[ [**Last \_ -**](last-is.md), \] \[ [**length \_ —**](length-is.md) \] , \[ [**Max \_ —**](max-is.md) \] , \[ [**size \_ —**](size-is.md) \] и \[ [**\_ Тип переключателя**](switch-type.md) \] ; атрибут указателя \[ [**ref**](ref.md) \] , \[ [**UNIQUE**](unique.md) \] или \[ [**ptr**](ptr.md), \] а также \[ [**\_ маркер контекста**](context-handle.md) атрибутов использования \] и \[ [**строка**](string.md) \] .</span><span class="sxs-lookup"><span data-stu-id="da56e-120">Parameter attributes with the \[**out**\] attribute can also take the directional attribute \[**out**\]; the field attributes \[[**first\_is**](first-is.md)\], \[[**last\_is**](last-is.md)\], \[[**length\_is**](length-is.md)\], \[[**max\_is**](max-is.md)\], \[[**size\_is**](size-is.md)\], and \[[**switch\_type**](switch-type.md)\]; the pointer attribute \[[**ref**](ref.md)\], \[[**unique**](unique.md)\], or \[[**ptr**](ptr.md)\]; and the usage attributes \[[**context\_handle**](context-handle.md)\] and \[[**string**](string.md)\].</span></span> <span data-ttu-id="da56e-121">Атрибут использования \[ [**Ignore**](ignore.md) \] не может использоваться в качестве атрибута параметра.</span><span class="sxs-lookup"><span data-stu-id="da56e-121">The usage attribute \[[**ignore**](ignore.md)\] cannot be used as a parameter attribute.</span></span> <span data-ttu-id="da56e-122">Несколько атрибутов разделяются запятыми.</span><span class="sxs-lookup"><span data-stu-id="da56e-122">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="da56e-123">*declarator*</span><span class="sxs-lookup"><span data-stu-id="da56e-123">*declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="da56e-124">Задает стандартные деклараторы, такие как идентификаторы, деклараторы указателей и деклараторы массивов.</span><span class="sxs-lookup"><span data-stu-id="da56e-124">Specifies the standard declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="da56e-125">Дополнительные сведения см. в разделе [атрибуты Array и Sized-Pointer](array-and-sized-pointer-attributes.md), [**массивы**](arrays-1.md), [массивы и указатели](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="da56e-125">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="da56e-126">Декларатор параметра в деклараторе функции, например имя параметра, является необязательным.</span><span class="sxs-lookup"><span data-stu-id="da56e-126">The parameter declarator in the function declarator, such as the parameter name, is optional.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="da56e-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="da56e-127">Remarks</span></span>

<span data-ttu-id="da56e-128">Атрибут \[ **out** \] указывает, что параметр, который выступает в качестве указателя и связанных с ним данных в памяти, передается обратно из вызванной процедуры в вызывающую процедуру.</span><span class="sxs-lookup"><span data-stu-id="da56e-128">The \[**out**\] attribute indicates that a parameter that acts as a pointer and its associated data in memory are to be passed back from the called procedure to the calling procedure.</span></span>

<span data-ttu-id="da56e-129">Атрибут \[ **out** \] должен быть указателем.</span><span class="sxs-lookup"><span data-stu-id="da56e-129">The \[**out**\] attribute must be a pointer.</span></span> <span data-ttu-id="da56e-130">Компиляторы устройства DCE на языке IDL должны иметь явный в \* качестве декларатора указателя в объявлении параметра.</span><span class="sxs-lookup"><span data-stu-id="da56e-130">DCE IDL compilers require the presence of an explicit \* as a pointer declarator in the parameter declaration.</span></span> <span data-ttu-id="da56e-131">Microsoft IDL предлагает расширение, которое удаляет это требование и позволяет массиву или ранее определенному типу указателя.</span><span class="sxs-lookup"><span data-stu-id="da56e-131">Microsoft IDL offers an extension that drops this requirement and allows an array or a previously defined pointer type.</span></span>

<span data-ttu-id="da56e-132">Связанный атрибут \[ [**в**](in.md) \] указывает, что параметр передается из вызывающей процедуры в вызываемую процедуру.</span><span class="sxs-lookup"><span data-stu-id="da56e-132">A related attribute, \[[**in**](in.md)\], indicates that the parameter is passed from the calling procedure to the called procedure.</span></span> <span data-ttu-id="da56e-133">Атрибуты \[ **in** \] и \[ **out** \] указывают направление, в котором передаются параметры.</span><span class="sxs-lookup"><span data-stu-id="da56e-133">The \[**in**\] and \[**out**\] attributes specify the direction in which the parameters are passed.</span></span> <span data-ttu-id="da56e-134">Параметр может быть определен как " \[ только **для** \] чтения", "только для \[ **выхода**" \] или " \[  **вне**" \] .</span><span class="sxs-lookup"><span data-stu-id="da56e-134">A parameter can be defined as \[**in**\]-only, \[**out**\]-only, or \[**in**, **out**\].</span></span>

<span data-ttu-id="da56e-135">Предполагается, что \[ **исходящий** \] параметр должен быть не определен при вызове удаленной процедуры, а память для объекта выделяется сервером.</span><span class="sxs-lookup"><span data-stu-id="da56e-135">An \[**out**\]-only parameter is assumed to be undefined when the remote procedure is called and memory for the object is allocated by the server.</span></span> <span data-ttu-id="da56e-136">Так как указатель верхнего уровня или параметры должны всегда указывать на допустимое хранилище и, следовательно, не может иметь **значение NULL**, \[ **out** \] нельзя применять к \[ [**уникальным**](unique.md) \] \[ [](ptr.md) \] указателям или указателям типа "указатель" верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="da56e-136">Since top-level pointer/parameters must always point to valid storage, and therefore cannot be **NULL**, \[**out**\] cannot be applied to top-level \[[**unique**](unique.md)\] or \[[**ptr**](ptr.md)\] pointers.</span></span> <span data-ttu-id="da56e-137">Параметры, являющиеся \[ **уникальными** \] или \[ **ptr** - \] указатели, должны быть \[ [**в**](in.md) \] \[ параметрах или **в**, **out** \] .</span><span class="sxs-lookup"><span data-stu-id="da56e-137">Parameters that are \[**unique**\] or \[**ptr**\] pointers must be either \[[**in**](in.md)\] or \[**in**, **out**\] parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="da56e-138">Примеры</span><span class="sxs-lookup"><span data-stu-id="da56e-138">Examples</span></span>

``` syntax
HRESULT MyFunction([out] short * pcount);
```

## <a name="see-also"></a><span data-ttu-id="da56e-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="da56e-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da56e-140">**массивы**</span><span class="sxs-lookup"><span data-stu-id="da56e-140">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="da56e-141">Базовые типы MIDL</span><span class="sxs-lookup"><span data-stu-id="da56e-141">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="da56e-142">**обратный вызов**</span><span class="sxs-lookup"><span data-stu-id="da56e-142">**callback**</span></span>](callback.md)
</dt> <dt>

[<span data-ttu-id="da56e-143">**const**</span><span class="sxs-lookup"><span data-stu-id="da56e-143">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="da56e-144">**Контекстный \_ маркер**</span><span class="sxs-lookup"><span data-stu-id="da56e-144">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="da56e-145">**перечисления**</span><span class="sxs-lookup"><span data-stu-id="da56e-145">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="da56e-146">**первый \_ —**</span><span class="sxs-lookup"><span data-stu-id="da56e-146">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="da56e-147">**обращать**</span><span class="sxs-lookup"><span data-stu-id="da56e-147">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="da56e-148">**окне**</span><span class="sxs-lookup"><span data-stu-id="da56e-148">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="da56e-149">**Последний \_ —**</span><span class="sxs-lookup"><span data-stu-id="da56e-149">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="da56e-150">**Длина \_ равна**</span><span class="sxs-lookup"><span data-stu-id="da56e-150">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="da56e-151">**Языковые**</span><span class="sxs-lookup"><span data-stu-id="da56e-151">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="da56e-152">**Максимальное \_ число**</span><span class="sxs-lookup"><span data-stu-id="da56e-152">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="da56e-153">**ptr**</span><span class="sxs-lookup"><span data-stu-id="da56e-153">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="da56e-154">**ref**</span><span class="sxs-lookup"><span data-stu-id="da56e-154">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="da56e-155">**размер \_ равен**</span><span class="sxs-lookup"><span data-stu-id="da56e-155">**size\_is**</span></span>](size-is.md)
</dt> <dt>

[<span data-ttu-id="da56e-156">**Строка**</span><span class="sxs-lookup"><span data-stu-id="da56e-156">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="da56e-157">**struct**</span><span class="sxs-lookup"><span data-stu-id="da56e-157">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="da56e-158">**Тип коммутатора \_**</span><span class="sxs-lookup"><span data-stu-id="da56e-158">**switch\_type**</span></span>](switch-type.md)
</dt> <dt>

[<span data-ttu-id="da56e-159">**наборов**</span><span class="sxs-lookup"><span data-stu-id="da56e-159">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="da56e-160">**однозначно**</span><span class="sxs-lookup"><span data-stu-id="da56e-160">**unique**</span></span>](unique.md)
</dt> </dl>

 

 