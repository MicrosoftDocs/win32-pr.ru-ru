---
title: typedef, атрибут
description: Ключевое слово IDL typedef позволяет объявлять typedef, которые очень похожи на объявления typedef языка C.
ms.assetid: 995a233e-0d07-4051-9f00-d1dc0b563f8f
keywords:
- typedef с атрибутом MIDL
topic_type:
- apiref
api_name:
- typedef
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecfce98e5a83f8d2a5e2499a5ceceba755e68f2c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790008"
---
# <a name="typedef-attribute"></a><span data-ttu-id="0d435-104">typedef, атрибут</span><span class="sxs-lookup"><span data-stu-id="0d435-104">typedef attribute</span></span>

<span data-ttu-id="0d435-105">Ключевое слово IDL **typedef** позволяет объявлять **typedef** , которые очень похожи на объявления **typedef** языка C.</span><span class="sxs-lookup"><span data-stu-id="0d435-105">The IDL **typedef** keyword allows **typedef** declarations that are very similar to C-language **typedef** declarations.</span></span>

``` syntax
/* IDL file typedef syntax */
typedef [[ [ idl-type-attribute-list ] ]] type-specifier declarator-list;

/* ACF typedef syntax */
typedef [ acf-type-attribute-list ] typename;
```

## <a name="parameters"></a><span data-ttu-id="0d435-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0d435-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d435-107">*Список IDL-Type-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="0d435-107">*idl-type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="0d435-108">Указывает один или несколько атрибутов, применяемых к типу.</span><span class="sxs-lookup"><span data-stu-id="0d435-108">Specifies one or more attributes that apply to the type.</span></span> <span data-ttu-id="0d435-109">Допустимые атрибуты типа в IDL-файле включают в себя **\[** [**Handle**](handle.md) **\]** , **\[** [**Switch \_ Type**](switch-type.md) **\]** , **\[** [**передает \_ as**](transmit-as.md) **\]** ; атрибут указателя **\[** [**ref**](ref.md) **\]** , **\[** [**UNIQUE**](unique.md) **\]** или **\[** [**ptr**](ptr.md), **\]** а также **\[** [**\_ маркер контекста**](context-handle.md)атрибутов использования **\]** , **\[** [**String**](string.md) **\]** и **\[** [**Ignore**](ignore.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="0d435-109">Valid type attributes in an IDL file include **\[**[**handle**](handle.md)**\]**, **\[**[**switch\_type**](switch-type.md)**\]**, **\[**[**transmit\_as**](transmit-as.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**context\_handle**](context-handle.md)**\]**, **\[**[**string**](string.md)**\]**, and **\[**[**ignore**](ignore.md)**\]**.</span></span> <span data-ttu-id="0d435-110">Несколько атрибутов разделяются запятыми.</span><span class="sxs-lookup"><span data-stu-id="0d435-110">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="0d435-111">*Описатель типа*</span><span class="sxs-lookup"><span data-stu-id="0d435-111">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="0d435-112">Задает [базовый тип](midl-base-types.md), [**структуру**](struct.md), [**объединение**](union.md), тип [**перечисления**](enum.md) или идентификатор типа.</span><span class="sxs-lookup"><span data-stu-id="0d435-112">Specifies a [base type](midl-base-types.md), [**struct**](struct.md), [**union**](union.md), [**enum**](enum.md) type, or type identifier.</span></span> <span data-ttu-id="0d435-113">Дополнительная спецификация хранилища может предшествовать *спецификатору типа*.</span><span class="sxs-lookup"><span data-stu-id="0d435-113">An optional storage specification can precede *type-specifier*.</span></span> <span data-ttu-id="0d435-114">Ключевое слово [**const**](const.md) может предшествовать *спецификатору типа*.</span><span class="sxs-lookup"><span data-stu-id="0d435-114">The [**const**](const.md) keyword can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="0d435-115">*декларатор-список*</span><span class="sxs-lookup"><span data-stu-id="0d435-115">*declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="0d435-116">Задает стандартные деклараторы MIDL, такие как идентификаторы, деклараторы указателей и деклараторы массивов.</span><span class="sxs-lookup"><span data-stu-id="0d435-116">Specifies standard MIDL declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="0d435-117">Дополнительные сведения см. в разделе [атрибуты Array и Sized-Pointer](array-and-sized-pointer-attributes.md), [**массивы**](arrays-1.md), [массивы и указатели](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="0d435-117">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="0d435-118">*Список деклараторов* состоит из одного или нескольких деклараторов, разделенных запятыми.</span><span class="sxs-lookup"><span data-stu-id="0d435-118">The *declarator-list* consists of one or more declarators, separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="0d435-119">*ACF-Type-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="0d435-119">*acf-type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="0d435-120">Указывает один или несколько атрибутов, применяемых к типу.</span><span class="sxs-lookup"><span data-stu-id="0d435-120">Specifies one or more attributes that apply to the type.</span></span> <span data-ttu-id="0d435-121">Допустимые атрибуты типа в ACF включают **\[** [**выделение**](allocate.md) **\]** , **\[** [**кодирование**](encode.md) **\]** и **\[** [**декодирование**](decode.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="0d435-121">Valid type attributes in an ACF include **\[**[**allocate**](allocate.md)**\]**, **\[**[**encode**](encode.md)**\]**, and **\[**[**decode**](decode.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="0d435-122">*имени*</span><span class="sxs-lookup"><span data-stu-id="0d435-122">*typename*</span></span> 
</dt> <dd>

<span data-ttu-id="0d435-123">Указывает тип, определенный в IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="0d435-123">Specifies a type defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0d435-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0d435-124">Remarks</span></span>

<span data-ttu-id="0d435-125">Объявление **TYPEDEF** IDL дополняется, позволяя связывать атрибуты типа с определенными типами.</span><span class="sxs-lookup"><span data-stu-id="0d435-125">The IDL **typedef** declaration is augmented to allow you to associate type attributes with the defined types.</span></span> <span data-ttu-id="0d435-126">К допустимым атрибутам типа относятся **\[** [**Handle**](handle.md), **\]** **\[** [**Switch \_ Type**](switch-type.md) **\]** , **\[** [**передает \_ as**](transmit-as.md) **\]** ; атрибут указателя **\[** [**ref**](ref.md) **\]** , **\[** [**UNIQUE**](unique.md) **\]** или **\[** [**ptr**](ptr.md) **\]** ;, а также **\[** [**\_ маркер контекста**](context-handle.md)атрибутов использования **\]** , **\[** [**String**](string.md) **\]** и **\[** [**Ignore**](ignore.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="0d435-126">Valid type attributes include **\[**[**handle**](handle.md)**\]**, **\[**[**switch\_type**](switch-type.md)**\]**, **\[**[**transmit\_as**](transmit-as.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**context\_handle**](context-handle.md)**\]**, **\[**[**string**](string.md)**\]**, and **\[**[**ignore**](ignore.md)**\]**.</span></span>

<span data-ttu-id="0d435-127">Ключевое слово **typedef** в ACF применяет атрибуты к типам, определенным в СООТВЕТСТВУЮЩем IDL-файле.</span><span class="sxs-lookup"><span data-stu-id="0d435-127">The **typedef** keyword in an ACF applies attributes to types that are defined in the corresponding IDL file.</span></span> <span data-ttu-id="0d435-128">Например, атрибут [**выделения**](allocate.md) типа позволяет настраивать выделение и освобождение памяти как приложением, так и заглушками.</span><span class="sxs-lookup"><span data-stu-id="0d435-128">For example, the [**allocate**](allocate.md) type attribute allows you to customize memory allocation and deallocation by both the application and the stubs.</span></span>

<span data-ttu-id="0d435-129">Инструкция ACF **typedef** отображается как часть тела ACF.</span><span class="sxs-lookup"><span data-stu-id="0d435-129">The ACF **typedef** statement appears as part of the ACF body.</span></span> <span data-ttu-id="0d435-130">Обратите внимание, что синтаксис **TYPEDEF** ACF отличается от синтаксиса **typedef языка IDL и** синтаксиса **typedef** языка C.</span><span class="sxs-lookup"><span data-stu-id="0d435-130">Note that the ACF **typedef** syntax is different from the IDL **typedef** syntax and the C-language **typedef** syntax.</span></span> <span data-ttu-id="0d435-131">Новые типы не могут быть введены в ACF.</span><span class="sxs-lookup"><span data-stu-id="0d435-131">No new types can be introduced in the ACF.</span></span>

## <a name="see-also"></a><span data-ttu-id="0d435-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0d435-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d435-133">Файл конфигурации приложения (ACF)</span><span class="sxs-lookup"><span data-stu-id="0d435-133">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="0d435-134">**allocate**</span><span class="sxs-lookup"><span data-stu-id="0d435-134">**allocate**</span></span>](allocate.md)
</dt> <dt>

[<span data-ttu-id="0d435-135">**массивы**</span><span class="sxs-lookup"><span data-stu-id="0d435-135">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="0d435-136">**const**</span><span class="sxs-lookup"><span data-stu-id="0d435-136">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="0d435-137">**Контекстный \_ маркер**</span><span class="sxs-lookup"><span data-stu-id="0d435-137">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="0d435-138">**декодировать**</span><span class="sxs-lookup"><span data-stu-id="0d435-138">**decode**</span></span>](decode.md)
</dt> <dt>

[<span data-ttu-id="0d435-139">**шифровать**</span><span class="sxs-lookup"><span data-stu-id="0d435-139">**encode**</span></span>](encode.md)
</dt> <dt>

[<span data-ttu-id="0d435-140">**перечисления**</span><span class="sxs-lookup"><span data-stu-id="0d435-140">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="0d435-141">**справиться**</span><span class="sxs-lookup"><span data-stu-id="0d435-141">**handle**</span></span>](handle.md)
</dt> <dt>

[<span data-ttu-id="0d435-142">Файл определения интерфейса (IDL)</span><span class="sxs-lookup"><span data-stu-id="0d435-142">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="0d435-143">**обращать**</span><span class="sxs-lookup"><span data-stu-id="0d435-143">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="0d435-144">**ptr**</span><span class="sxs-lookup"><span data-stu-id="0d435-144">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="0d435-145">**ref**</span><span class="sxs-lookup"><span data-stu-id="0d435-145">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="0d435-146">**Строка**</span><span class="sxs-lookup"><span data-stu-id="0d435-146">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="0d435-147">**struct**</span><span class="sxs-lookup"><span data-stu-id="0d435-147">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="0d435-148">**Тип коммутатора \_**</span><span class="sxs-lookup"><span data-stu-id="0d435-148">**switch\_type**</span></span>](switch-type.md)
</dt> <dt>

[<span data-ttu-id="0d435-149">**передать \_ как**</span><span class="sxs-lookup"><span data-stu-id="0d435-149">**transmit\_as**</span></span>](transmit-as.md)
</dt> <dt>

[<span data-ttu-id="0d435-150">**наборов**</span><span class="sxs-lookup"><span data-stu-id="0d435-150">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="0d435-151">**однозначно**</span><span class="sxs-lookup"><span data-stu-id="0d435-151">**unique**</span></span>](unique.md)
</dt> </dl>

 

 