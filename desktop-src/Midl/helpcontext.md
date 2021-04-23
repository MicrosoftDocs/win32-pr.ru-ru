---
title: helpcontext - атрибут
description: Атрибут \ HelpContext \ задает идентификатор контекста, позволяющий пользователю просматривать сведения об этом элементе в файле справки.
ms.assetid: 44a60c75-be69-4cd9-afb0-5eb988830e6c
keywords:
- атрибут HelpContext MIDL
topic_type:
- apiref
api_name:
- helpcontext
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75a8811a73515528981a8214caba3fe2778e2ea9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103987412"
---
# <a name="helpcontext-attribute"></a><span data-ttu-id="5dbb3-104">helpcontext - атрибут</span><span class="sxs-lookup"><span data-stu-id="5dbb3-104">helpcontext attribute</span></span>

<span data-ttu-id="5dbb3-105">Атрибут \[ **HelpContext** \] задает идентификатор контекста, позволяющий пользователю просматривать сведения об этом элементе в файле справки.</span><span class="sxs-lookup"><span data-stu-id="5dbb3-105">The \[**helpcontext**\] attribute specifies a context identifier that lets the user view information about this element in the Help file.</span></span>

``` syntax
[
    uuid(uuid-number), 
    helpcontext(helpcontext-value)
    [, attribute-list]
] 
element element-name
{
    definitions
}
```

## <a name="parameters"></a><span data-ttu-id="5dbb3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5dbb3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5dbb3-107">*UUID — номер*</span><span class="sxs-lookup"><span data-stu-id="5dbb3-107">*uuid-number*</span></span> 
</dt> <dd>

<span data-ttu-id="5dbb3-108">Задает универсальный уникальный идентификационный номер для [**библиотеки**](library.md), \[ [**importlib**](importlib.md) \] , [**интерфейса**](interface.md), [**DISP**](dispinterface.md), [**модуля**](module.md), [**определения типа**](typedef.md), **методов**, **\[ \] свойств** или [**coclass**](coclass.md).</span><span class="sxs-lookup"><span data-stu-id="5dbb3-108">Specifies a universally unique identification number for the [**library**](library.md), \[[**importlib**](importlib.md)\], [**interface**](interface.md), [**dispinterface**](dispinterface.md), [**module**](module.md), [**typedef**](typedef.md), **methods**, **\[property\]**, or [**coclass**](coclass.md).</span></span>

</dd> <dt>

<span data-ttu-id="5dbb3-109">*HelpContext — значение*</span><span class="sxs-lookup"><span data-stu-id="5dbb3-109">*helpcontext-value*</span></span> 
</dt> <dd>

<span data-ttu-id="5dbb3-110">Уникальное целое число, определяющее текст справки, связанный с текущим элементом MIDL.</span><span class="sxs-lookup"><span data-stu-id="5dbb3-110">A unique integer that identifies the help text associated with the current MIDL element.</span></span>

</dd> <dt>

<span data-ttu-id="5dbb3-111">*Список атрибутов*</span><span class="sxs-lookup"><span data-stu-id="5dbb3-111">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="5dbb3-112">Указывает список из одного или нескольких атрибутов, которые применяются к элементу MIDL в целом.</span><span class="sxs-lookup"><span data-stu-id="5dbb3-112">Specifies a list of one or more attributes that apply to the MIDL element as a whole.</span></span>

</dd> <dt>

<span data-ttu-id="5dbb3-113">*дерев*</span><span class="sxs-lookup"><span data-stu-id="5dbb3-113">*element*</span></span> 
</dt> <dd>

<span data-ttu-id="5dbb3-114">Одна из следующих директив: [**Библиотека**](library.md), \[ [**importlib**](importlib.md) \] , [**интерфейс**](interface.md), [**DISP**](dispinterface.md), [**модуль**](module.md), [**Определение типа**](typedef.md), **метод**, **свойство** или [**coclass**](coclass.md).</span><span class="sxs-lookup"><span data-stu-id="5dbb3-114">One of the following directives: [**library**](library.md), \[[**importlib**](importlib.md)\], [**interface**](interface.md), [**dispinterface**](dispinterface.md), [**module**](module.md), [**typedef**](typedef.md), **method**, **property**, or [**coclass**](coclass.md).</span></span>

</dd> <dt>

<span data-ttu-id="5dbb3-115">*имя элемента*</span><span class="sxs-lookup"><span data-stu-id="5dbb3-115">*element-name*</span></span> 
</dt> <dd>

<span data-ttu-id="5dbb3-116">Имя, которое другие программные компоненты могут использовать для отделения текущего элемента.</span><span class="sxs-lookup"><span data-stu-id="5dbb3-116">The name that other software components can use to delineate the current element.</span></span>

</dd> <dt>

<span data-ttu-id="5dbb3-117">*вирус*</span><span class="sxs-lookup"><span data-stu-id="5dbb3-117">*definitions*</span></span> 
</dt> <dd>

<span data-ttu-id="5dbb3-118">Указывает инструкции, которые составляют определение элемента.</span><span class="sxs-lookup"><span data-stu-id="5dbb3-118">Specifies statements that make up the element definition.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5dbb3-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5dbb3-119">Remarks</span></span>

<span data-ttu-id="5dbb3-120">Атрибут \[ **HelpContext** \] может применяться к следующим элементам: [**Library**](library.md), \[ [**importlib**](importlib.md) \] , [**интерфейс**](interface.md), [**DISP**](dispinterface.md), [**module**](module.md), [**typedef**](typedef.md), **метод**, **свойство** или [**coclass**](coclass.md).</span><span class="sxs-lookup"><span data-stu-id="5dbb3-120">The \[**helpcontext**\] attribute can be applied to the following elements: [**library**](library.md), \[[**importlib**](importlib.md)\], [**interface**](interface.md), [**dispinterface**](dispinterface.md), [**module**](module.md), [**typedef**](typedef.md), **method**, **property**, or [**coclass**](coclass.md).</span></span>

<span data-ttu-id="5dbb3-121">*Параметр HelpContext-value* — это 32-разрядный идентификатор контекста в файле справки, который можно получить с помощью функций функции- [**документации**](/windows/win32/api/oaidl/nf-oaidl-itypelib-getdocumentation) в интерфейсах [**ITypeLib**](/windows/win32/api/oaidl/nn-oaidl-itypelib) и [**ITypeInfo**](/windows/win32/api/oaidl/nn-oaidl-itypeinfo) .</span><span class="sxs-lookup"><span data-stu-id="5dbb3-121">The *helpcontext-value* is a 32-bit context identifier within the Help file that can be retrieved with the [**GetDocumentation**](/windows/win32/api/oaidl/nf-oaidl-itypelib-getdocumentation) functions in the [**ITypeLib**](/windows/win32/api/oaidl/nn-oaidl-itypelib) and [**ITypeInfo**](/windows/win32/api/oaidl/nn-oaidl-itypeinfo) interfaces.</span></span>

## <a name="examples"></a><span data-ttu-id="5dbb3-122">Примеры</span><span class="sxs-lookup"><span data-stu-id="5dbb3-122">Examples</span></span>

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    helpcontext(7035943),
    helpstring("Hello Class"),
    appobject
] 
coclass Hello
{
    [default, helpcontext(3914972)] interface IHello : IUnknown;
    interface IDispatch;
}
```

## <a name="see-also"></a><span data-ttu-id="5dbb3-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5dbb3-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5dbb3-124">**кокласс**</span><span class="sxs-lookup"><span data-stu-id="5dbb3-124">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="5dbb3-125">**интерфейса**</span><span class="sxs-lookup"><span data-stu-id="5dbb3-125">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="5dbb3-126">Создание библиотеки типов с помощью MIDL</span><span class="sxs-lookup"><span data-stu-id="5dbb3-126">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="5dbb3-127">**importlib**</span><span class="sxs-lookup"><span data-stu-id="5dbb3-127">**importlib**</span></span>](importlib.md)
</dt> <dt>

[<span data-ttu-id="5dbb3-128">**взаимодействия**</span><span class="sxs-lookup"><span data-stu-id="5dbb3-128">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="5dbb3-129">**библиотека**</span><span class="sxs-lookup"><span data-stu-id="5dbb3-129">**library**</span></span>](library.md)
</dt> <dt>

[<span data-ttu-id="5dbb3-130">**модуль**</span><span class="sxs-lookup"><span data-stu-id="5dbb3-130">**module**</span></span>](module.md)
</dt> <dt>

[<span data-ttu-id="5dbb3-131">Синтаксис файла ODL</span><span class="sxs-lookup"><span data-stu-id="5dbb3-131">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="5dbb3-132">Пример файла ODL</span><span class="sxs-lookup"><span data-stu-id="5dbb3-132">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="5dbb3-133">**определение**</span><span class="sxs-lookup"><span data-stu-id="5dbb3-133">**typedef**</span></span>](typedef.md)
</dt> </dl>

 

 