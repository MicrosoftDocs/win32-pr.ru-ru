---
title: атрибут библиотеки
description: Оператор Library содержит все сведения, используемые компилятором MIDL для создания библиотеки типов.
ms.assetid: d73acb17-abe4-4c31-a264-a131d1f9fa51
keywords:
- атрибут библиотеки MIDL
topic_type:
- apiref
api_name:
- library
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 100c901c6b5d86ed3420d51e459627bdb5b461b8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105661727"
---
# <a name="library-attribute"></a><span data-ttu-id="71cb1-104">атрибут библиотеки</span><span class="sxs-lookup"><span data-stu-id="71cb1-104">library attribute</span></span>

<span data-ttu-id="71cb1-105">Оператор **Library** содержит все сведения, используемые компилятором MIDL для создания библиотеки типов.</span><span class="sxs-lookup"><span data-stu-id="71cb1-105">The **library** statement contains all the information that the MIDL compiler uses to generate a type library.</span></span>

``` syntax
[
    uuid(uuid-number), 
    [, optional-attribute-list]
] 
library library-name
{ 
    library-definition-statements
}
```

## <a name="parameters"></a><span data-ttu-id="71cb1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="71cb1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71cb1-107">*UUID — номер*</span><span class="sxs-lookup"><span data-stu-id="71cb1-107">*uuid-number*</span></span> 
</dt> <dd>

<span data-ttu-id="71cb1-108">Задает универсальный уникальный идентификационный номер для библиотеки.</span><span class="sxs-lookup"><span data-stu-id="71cb1-108">Specifies a universally unique identification number for the library.</span></span>

</dd> <dt>

<span data-ttu-id="71cb1-109">*список необязательных атрибутов*</span><span class="sxs-lookup"><span data-stu-id="71cb1-109">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="71cb1-110">Задает дополнительные атрибуты, которые применяются ко всей инструкции **Library** .</span><span class="sxs-lookup"><span data-stu-id="71cb1-110">Specifies additional attributes that apply to the entire **library** statement.</span></span> <span data-ttu-id="71cb1-111">К допустимым атрибутам относятся **\[** [**Control**](control.md) **\]** , **\[** [**HelpContext**](helpcontext.md) **\]** , **\[** [**HelpFile**](helpfile.md) **\]** , **\[** [**helpString**](helpstring.md) **\]** , **\[** [**Hidden**](hidden.md) **\]** , **\[** [**LCID**](lcid.md) **\]** , **\[** [**Restricted**](restricted.md) **\]** и **\[** [**Version**](version.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="71cb1-111">Allowable attributes include **\[**[**control**](control.md)**\]**, **\[**[**helpcontext**](helpcontext.md)**\]**, **\[**[**helpfile**](helpfile.md)**\]**, **\[**[**helpstring**](helpstring.md)**\]**, **\[**[**hidden**](hidden.md)**\]**, **\[**[**lcid**](lcid.md)**\]**, **\[**[**restricted**](restricted.md)**\]**, and **\[**[**version**](version.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="71cb1-112">*имя библиотеки*</span><span class="sxs-lookup"><span data-stu-id="71cb1-112">*library-name*</span></span> 
</dt> <dd>

<span data-ttu-id="71cb1-113">Имя, по которому программные компоненты ссылаются на **библиотеку**.</span><span class="sxs-lookup"><span data-stu-id="71cb1-113">The name by which software components refer to the **library**.</span></span>

</dd> <dt>

<span data-ttu-id="71cb1-114">*Library-операторы определения*</span><span class="sxs-lookup"><span data-stu-id="71cb1-114">*library-definition-statements*</span></span> 
</dt> <dd>

<span data-ttu-id="71cb1-115">Одна или несколько инструкций MIDL, которые определяют содержимое **библиотеки**.</span><span class="sxs-lookup"><span data-stu-id="71cb1-115">One or more MIDL statements which define the contents of the **library**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="71cb1-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="71cb1-116">Remarks</span></span>

<span data-ttu-id="71cb1-117">Инструкции в блоке библиотеки могут использовать элементы, объявленные внутри или вне блока библиотеки.</span><span class="sxs-lookup"><span data-stu-id="71cb1-117">Statements inside the library block can use elements that are declared inside or outside of the library block.</span></span> <span data-ttu-id="71cb1-118">Операторы библиотеки могут использовать эти элементы как базовые типы, наследовать от этих элементов или просто ссылаться на них в строке следующим образом:</span><span class="sxs-lookup"><span data-stu-id="71cb1-118">Library statements can use those elements as base types, inheriting from those elements, or by simply referencing them on a line, as follows:</span></span>

``` syntax
interface MyFace 
{
    // Interface definition statements
};

[
    // library attributes
] 
library
{
    interface MyFace;

    // Other library definition statements.
};
```

<span data-ttu-id="71cb1-119">Компилятор MIDL создаст библиотеку типов, которая включает определения для каждого элемента внутри блока библиотеки, а также определения всех элементов, определенных вне и упоминаемых в блоке библиотеки.</span><span class="sxs-lookup"><span data-stu-id="71cb1-119">The MIDL compiler will create a type library that includes definitions for every element inside the library block, plus definitions for any elements defined outside and referenced from within the library block.</span></span>

<span data-ttu-id="71cb1-120">Сведения о создании библиотеки типов и заглушек прокси и заголовков из одного IDL-файла см. в разделе [Создание прокси-библиотеки DLL и библиотеки типов из одного файла IDL](generating-a-proxy-dll-and-a-type-library-from-a-single-idl-file-2.md).</span><span class="sxs-lookup"><span data-stu-id="71cb1-120">For information on generating both a type library and proxy stubs and headers from a single IDL file see [Generating a Proxy DLL and a Type Library From a Single IDL File](generating-a-proxy-dll-and-a-type-library-from-a-single-idl-file-2.md).</span></span>

## <a name="examples"></a><span data-ttu-id="71cb1-121">Примеры</span><span class="sxs-lookup"><span data-stu-id="71cb1-121">Examples</span></span>

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    helpstring("Hello 2.0 Type Library"), 
    lcid(0x0409), 
    version(2.0)
] 
library Hello 
{
    /* Library definition statements */
};
```

## <a name="see-also"></a><span data-ttu-id="71cb1-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="71cb1-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71cb1-123">Содержимое библиотеки типов</span><span class="sxs-lookup"><span data-stu-id="71cb1-123">Contents of a Type Library</span></span>](/previous-versions/windows/desktop/automat/contents-of-a-type-library)
</dt> <dt>

[<span data-ttu-id="71cb1-124">**элемента**</span><span class="sxs-lookup"><span data-stu-id="71cb1-124">**control**</span></span>](control.md)
</dt> <dt>

[<span data-ttu-id="71cb1-125">Создание библиотеки типов с помощью MIDL</span><span class="sxs-lookup"><span data-stu-id="71cb1-125">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="71cb1-126">**helpcontext**</span><span class="sxs-lookup"><span data-stu-id="71cb1-126">**helpcontext**</span></span>](helpcontext.md)
</dt> <dt>

[<span data-ttu-id="71cb1-127">**helpfile**</span><span class="sxs-lookup"><span data-stu-id="71cb1-127">**helpfile**</span></span>](helpfile.md)
</dt> <dt>

[<span data-ttu-id="71cb1-128">**helpstring**</span><span class="sxs-lookup"><span data-stu-id="71cb1-128">**helpstring**</span></span>](helpstring.md)
</dt> <dt>

[<span data-ttu-id="71cb1-129">**служеб**</span><span class="sxs-lookup"><span data-stu-id="71cb1-129">**hidden**</span></span>](hidden.md)
</dt> <dt>

[<span data-ttu-id="71cb1-130">**намного**</span><span class="sxs-lookup"><span data-stu-id="71cb1-130">**lcid**</span></span>](lcid.md)
</dt> <dt>

[<span data-ttu-id="71cb1-131">Синтаксис файла ODL</span><span class="sxs-lookup"><span data-stu-id="71cb1-131">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="71cb1-132">**зона**</span><span class="sxs-lookup"><span data-stu-id="71cb1-132">**restricted**</span></span>](restricted.md)
</dt> <dt>

[<span data-ttu-id="71cb1-133">**Версия**</span><span class="sxs-lookup"><span data-stu-id="71cb1-133">**version**</span></span>](version.md)
</dt> </dl>

 

 