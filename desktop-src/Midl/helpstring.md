---
title: атрибут helpstring
description: Атрибут \ helpString \ задает символьную строку, используемую для описания элемента, к которому он применяется.
ms.assetid: f05d3fdd-d975-4f0e-8181-07e16288ff48
keywords:
- атрибут helpString MIDL
topic_type:
- apiref
api_name:
- helpstring
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c58bbe61b10e2f223cf9f662f10d95ca72819b02
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103987399"
---
# <a name="helpstring-attribute"></a><span data-ttu-id="6fab6-104">атрибут helpstring</span><span class="sxs-lookup"><span data-stu-id="6fab6-104">helpstring attribute</span></span>

<span data-ttu-id="6fab6-105">Атрибут **\[ helpString \]** задает символьную строку, используемую для описания элемента, к которому он применяется.</span><span class="sxs-lookup"><span data-stu-id="6fab6-105">The **\[helpstring\]** attribute specifies a character string that is used to describe the element to which it applies.</span></span> <span data-ttu-id="6fab6-106">Атрибут **\[ helpString \]** можно применить к операторам Library, importlib, Interface, DISP, Module или coclass, определениям типов, свойствам и методам.</span><span class="sxs-lookup"><span data-stu-id="6fab6-106">You can apply the **\[helpstring\]** attribute to library, importlib, interface, dispinterface, module, or coclass statements, typedefs, properties, and methods.</span></span>

``` syntax
[
    helpstring(help-text-string)
    [, optional-attribute-list]
] 
element element-name
{
    definition
}

[idl-statement, helpstring(help-text-string)]
```

## <a name="parameters"></a><span data-ttu-id="6fab6-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="6fab6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6fab6-108">*Справка-текстовая строка*</span><span class="sxs-lookup"><span data-stu-id="6fab6-108">*help-text-string*</span></span> 
</dt> <dd>

<span data-ttu-id="6fab6-109">Строка символов, заканчивающаяся нулем и содержащая текст справки.</span><span class="sxs-lookup"><span data-stu-id="6fab6-109">A zero-terminated string of characters containing help text.</span></span>

</dd> <dt>

<span data-ttu-id="6fab6-110">*список необязательных атрибутов*</span><span class="sxs-lookup"><span data-stu-id="6fab6-110">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="6fab6-111">Ноль или несколько операторов атрибута MIDL.</span><span class="sxs-lookup"><span data-stu-id="6fab6-111">Zero or more MIDL attribute statements.</span></span>

</dd> <dt>

<span data-ttu-id="6fab6-112">*дерев*</span><span class="sxs-lookup"><span data-stu-id="6fab6-112">*element*</span></span> 
</dt> <dd>

<span data-ttu-id="6fab6-113">Одна из следующих директив: [**Библиотека**](library.md), **\[** [**importlib**](importlib.md) **\]** , [**интерфейс**](interface.md), [**DISP**](dispinterface.md), [**модуль**](module.md), [**Определение типа**](typedef.md), **метод**, **свойство** или [**coclass**](coclass.md).</span><span class="sxs-lookup"><span data-stu-id="6fab6-113">One of the following directives: [**library**](library.md), **\[**[**importlib**](importlib.md)**\]**, [**interface**](interface.md), [**dispinterface**](dispinterface.md), [**module**](module.md), [**typedef**](typedef.md), **method**, **property**, or [**coclass**](coclass.md).</span></span>

</dd> <dt>

<span data-ttu-id="6fab6-114">*имя элемента*</span><span class="sxs-lookup"><span data-stu-id="6fab6-114">*element-name*</span></span> 
</dt> <dd>

<span data-ttu-id="6fab6-115">Имя, которое другие программные компоненты могут использовать для отделения текущего элемента</span><span class="sxs-lookup"><span data-stu-id="6fab6-115">The name that other software components can use to delineate the current element</span></span>

</dd> <dt>

<span data-ttu-id="6fab6-116">*definition*</span><span class="sxs-lookup"><span data-stu-id="6fab6-116">*definition*</span></span> 
</dt> <dd>

<span data-ttu-id="6fab6-117">Указывает инструкции, которые составляют определение элемента.</span><span class="sxs-lookup"><span data-stu-id="6fab6-117">Specifies statements that make up the element definition.</span></span>

</dd> <dt>

<span data-ttu-id="6fab6-118">*IDL-оператор*</span><span class="sxs-lookup"><span data-stu-id="6fab6-118">*idl-statement*</span></span> 
</dt> <dd>

<span data-ttu-id="6fab6-119">Инструкция определения интерфейса MIDL, например [**propget**](propget.md) или [**propput**](propput.md).</span><span class="sxs-lookup"><span data-stu-id="6fab6-119">A MIDL interface definition statement such as [**propget**](propget.md) or [**propput**](propput.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6fab6-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6fab6-120">Remarks</span></span>

<span data-ttu-id="6fab6-121">Используйте функции [**GetString в**](/windows/win32/api/oaidl/nf-oaidl-itypelib-getdocumentation) интерфейсах [**ITypeLib**](/windows/win32/api/oaidl/nn-oaidl-itypelib) и [**ITypeInfo**](/windows/win32/api/oaidl/nn-oaidl-itypeinfo) для получения строки справки.</span><span class="sxs-lookup"><span data-stu-id="6fab6-121">Use the [**GetDocumentation**](/windows/win32/api/oaidl/nf-oaidl-itypelib-getdocumentation) functions in the [**ITypeLib**](/windows/win32/api/oaidl/nn-oaidl-itypelib) and [**ITypeInfo**](/windows/win32/api/oaidl/nn-oaidl-itypeinfo) interfaces to retrieve the help string.</span></span>

## <a name="examples"></a><span data-ttu-id="6fab6-122">Примеры</span><span class="sxs-lookup"><span data-stu-id="6fab6-122">Examples</span></span>

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    helpstring("Lines 1.0 Type Library"),
    version(1.0)
]
library Lines
{
     [
         uuid(1e123456-1f3c-1069-996b-00dd010fe676), 
         helpstring("Line object."),
         oleautomation,
         dual
     ]
     interface ILine : IDispatch                         
     {
         [propget, helpstring("Returns and sets RGB color.")]
         HRESULT Color([out, retval] long* ReturnVal); 
         [propput, helpstring("Returns and sets RGB color.")]
         HRESULT Color([in] long rgb);
     }
};
```

## <a name="see-also"></a><span data-ttu-id="6fab6-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6fab6-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fab6-124">**библиотека**</span><span class="sxs-lookup"><span data-stu-id="6fab6-124">**library**</span></span>](library.md)
</dt> <dt>

[<span data-ttu-id="6fab6-125">**importlib**</span><span class="sxs-lookup"><span data-stu-id="6fab6-125">**importlib**</span></span>](importlib.md)
</dt> <dt>

[<span data-ttu-id="6fab6-126">**взаимодействия**</span><span class="sxs-lookup"><span data-stu-id="6fab6-126">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="6fab6-127">**интерфейса**</span><span class="sxs-lookup"><span data-stu-id="6fab6-127">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="6fab6-128">**модуль**</span><span class="sxs-lookup"><span data-stu-id="6fab6-128">**module**</span></span>](module.md)
</dt> <dt>

[<span data-ttu-id="6fab6-129">**кокласс**</span><span class="sxs-lookup"><span data-stu-id="6fab6-129">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="6fab6-130">**определение**</span><span class="sxs-lookup"><span data-stu-id="6fab6-130">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="6fab6-131">Синтаксис файла ODL</span><span class="sxs-lookup"><span data-stu-id="6fab6-131">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="6fab6-132">Пример файла ODL</span><span class="sxs-lookup"><span data-stu-id="6fab6-132">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="6fab6-133">Создание библиотеки типов с помощью MIDL</span><span class="sxs-lookup"><span data-stu-id="6fab6-133">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 