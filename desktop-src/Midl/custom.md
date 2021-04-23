---
title: настраиваемый атрибут
description: Атрибут \ Custom \ создает определяемый пользователем атрибут.
ms.assetid: 63c93eca-c9c1-4c14-9f46-aa78b01d9ff8
keywords:
- пользовательский атрибут MIDL
topic_type:
- apiref
api_name:
- custom
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef7c4210091cc028d7724cb40724f22a91eb7d74
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105681596"
---
# <a name="custom-attribute"></a><span data-ttu-id="f6f34-104">настраиваемый атрибут</span><span class="sxs-lookup"><span data-stu-id="f6f34-104">custom attribute</span></span>

<span data-ttu-id="f6f34-105">**\[ Настраиваемый \]** атрибут создает определяемый пользователем атрибут.</span><span class="sxs-lookup"><span data-stu-id="f6f34-105">The **\[custom\]** attribute creates a user-defined attribute.</span></span>

``` syntax
[custom(attribute-id, attribute-value),attribute-list] element-type element-name
```

## <a name="parameters"></a><span data-ttu-id="f6f34-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f6f34-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6f34-107">*Attribute-ID*</span><span class="sxs-lookup"><span data-stu-id="f6f34-107">*attribute-id*</span></span> 
</dt> <dd>

<span data-ttu-id="f6f34-108">Идентификатор GUID для настраиваемого атрибута.</span><span class="sxs-lookup"><span data-stu-id="f6f34-108">The GUID for the custom attribute.</span></span>

</dd> <dt>

<span data-ttu-id="f6f34-109">*атрибут-значение*</span><span class="sxs-lookup"><span data-stu-id="f6f34-109">*attribute-value*</span></span> 
</dt> <dd>

<span data-ttu-id="f6f34-110">Значение, которое содержит атрибут.</span><span class="sxs-lookup"><span data-stu-id="f6f34-110">The value that the attribute holds.</span></span> <span data-ttu-id="f6f34-111">Значение должно быть значением, которое может быть помещается в тип VARIANT.</span><span class="sxs-lookup"><span data-stu-id="f6f34-111">The value must be one that can be put into a VARIANT type.</span></span>

</dd> <dt>

<span data-ttu-id="f6f34-112">*Список атрибутов*</span><span class="sxs-lookup"><span data-stu-id="f6f34-112">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="f6f34-113">Другие атрибуты, такие как **\[** [**UUID**](uuid.md) **\]** и **\[** [**helpString**](helpstring.md) **\]** , которые применяются к этому элементу.</span><span class="sxs-lookup"><span data-stu-id="f6f34-113">Other attributes, such as **\[**[**uuid**](uuid.md)**\]** and **\[**[**helpstring**](helpstring.md)**\]**, that apply to this element.</span></span>

</dd> <dt>

<span data-ttu-id="f6f34-114">*Element-Type*</span><span class="sxs-lookup"><span data-stu-id="f6f34-114">*element-type*</span></span> 
</dt> <dd>

<span data-ttu-id="f6f34-115">Тип элемента, к которому применяется настраиваемый атрибут.</span><span class="sxs-lookup"><span data-stu-id="f6f34-115">The type of element to which the custom attribute applies.</span></span> <span data-ttu-id="f6f34-116">Это может быть оператор библиотеки, сведения о типе, переменная, функция или параметр.</span><span class="sxs-lookup"><span data-stu-id="f6f34-116">This can be a library statement, type information, a variable, a function, or a parameter.</span></span> <span data-ttu-id="f6f34-117">Нельзя использовать настраиваемый атрибут для члена класса coclass.</span><span class="sxs-lookup"><span data-stu-id="f6f34-117">You cannot use a custom attribute on a member of a coclass.</span></span>

</dd> <dt>

<span data-ttu-id="f6f34-118">*имя элемента*</span><span class="sxs-lookup"><span data-stu-id="f6f34-118">*element-name*</span></span> 
</dt> <dd>

<span data-ttu-id="f6f34-119">Имя элемента.</span><span class="sxs-lookup"><span data-stu-id="f6f34-119">The name of the element.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f6f34-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f6f34-120">Remarks</span></span>

<span data-ttu-id="f6f34-121">Используйте **\[ настраиваемый \]** атрибут для определения собственного атрибута.</span><span class="sxs-lookup"><span data-stu-id="f6f34-121">Use the **\[custom\]** attribute to define your own attribute.</span></span> <span data-ttu-id="f6f34-122">Например, можно создать атрибут с строковыми значениями, который предоставляет идентификатор ProgID для класса.</span><span class="sxs-lookup"><span data-stu-id="f6f34-122">For example, you might create a string-valued attribute that gives the ProgID for a class.</span></span>

<span data-ttu-id="f6f34-123">Чтобы получить значение настраиваемого атрибута, вызовите один из следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="f6f34-123">To retrieve a custom attribute value call one of the following:</span></span>

-   <span data-ttu-id="f6f34-124">ITypeLib2:: Жеткустдата (ргуид, Пварвал)</span><span class="sxs-lookup"><span data-stu-id="f6f34-124">ITypeLib2::GetCustData(rguid, pvarVal)</span></span>
-   <span data-ttu-id="f6f34-125">ITypeInfo2:: Жеткустдата (ргуид, Пварвал)</span><span class="sxs-lookup"><span data-stu-id="f6f34-125">ITypeInfo2::GetCustData(rguid, pvarVal)</span></span>
-   <span data-ttu-id="f6f34-126">ITypeInfo2:: Жетфунккустдата (index, ргуид, Пварвал)</span><span class="sxs-lookup"><span data-stu-id="f6f34-126">ITypeInfo2::GetFuncCustData(index, rguid, pvarVal)</span></span>
-   <span data-ttu-id="f6f34-127">ITypeInfo2:: Жетваркустдата (index, ргуид, пварвал)</span><span class="sxs-lookup"><span data-stu-id="f6f34-127">ITypeInfo2::GetVarCustData(index, rguid, pvarval)</span></span>
-   <span data-ttu-id="f6f34-128">ITypeInfo2:: Жетпарамкустдата (Индексфунк, Индекспарам, ргуид, Пварвал)</span><span class="sxs-lookup"><span data-stu-id="f6f34-128">ITypeInfo2::GetParamCustData(indexFunc, indexParam, rguid, pvarVal)</span></span>

## <a name="see-also"></a><span data-ttu-id="f6f34-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f6f34-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6f34-130">Создание библиотеки типов с помощью MIDL</span><span class="sxs-lookup"><span data-stu-id="f6f34-130">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="f6f34-131">**helpstring**</span><span class="sxs-lookup"><span data-stu-id="f6f34-131">**helpstring**</span></span>](helpstring.md)
</dt> <dt>

[<span data-ttu-id="f6f34-132">**библиотека**</span><span class="sxs-lookup"><span data-stu-id="f6f34-132">**library**</span></span>](library.md)
</dt> <dt>

[<span data-ttu-id="f6f34-133">Пример файла ODL</span><span class="sxs-lookup"><span data-stu-id="f6f34-133">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="f6f34-134">Синтаксис файла ODL</span><span class="sxs-lookup"><span data-stu-id="f6f34-134">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="f6f34-135">**UUID**</span><span class="sxs-lookup"><span data-stu-id="f6f34-135">**uuid**</span></span>](uuid.md)
</dt> </dl>

 

 