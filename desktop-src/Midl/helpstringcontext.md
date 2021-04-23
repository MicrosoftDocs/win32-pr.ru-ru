---
title: атрибут хелпстрингконтекст
description: Атрибут \ хелпстрингконтекст \ задает идентификатор контекста справки 32-bit в файле справки. Атрибут \ хелпстрингконтекст \ можно применить к библиотеке, интерфейсу, DISP, модулю, соклассу, операторам typedef, свойствам, параметрам и методам.
ms.assetid: 0ac41bd9-ccc6-4b5c-b925-63bff9254eed
keywords:
- атрибут хелпстрингконтекст MIDL
topic_type:
- apiref
api_name:
- helpstringcontext
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72ddded3beb768543f2f990aa9d656fba1fa8b98
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "105650308"
---
# <a name="helpstringcontext-attribute"></a><span data-ttu-id="1a333-105">атрибут хелпстрингконтекст</span><span class="sxs-lookup"><span data-stu-id="1a333-105">helpstringcontext attribute</span></span>

<span data-ttu-id="1a333-106">Атрибут **\[ хелпстрингконтекст \]** задает 32-разрядный идентификатор контекста справки в файле справки.</span><span class="sxs-lookup"><span data-stu-id="1a333-106">The **\[helpstringcontext\]** attribute specifies a 32-bit Help context identifier in the Help file.</span></span> <span data-ttu-id="1a333-107">Атрибут **\[ хелпстрингконтекст \]** можно применить к [**библиотеке**](library.md), [**интерфейсу**](interface.md), [**DISP**](dispinterface.md), [**модулю**](module.md), [**соклассу**](coclass.md), операторам [**typedef**](typedef.md) , свойствам, параметрам и методам.</span><span class="sxs-lookup"><span data-stu-id="1a333-107">You can apply the **\[helpstringcontext\]** attribute to [**library**](library.md), [**interface**](interface.md), [**dispinterface**](dispinterface.md), [**module**](module.md), [**coclass**](coclass.md), [**typedef**](typedef.md) statements, properties, parameters and methods.</span></span>

``` syntax
[  helpstringcontext(contextid)[, optional-attribute-list]] idl-statement
```

## <a name="parameters"></a><span data-ttu-id="1a333-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="1a333-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a333-109">*ContextId*</span><span class="sxs-lookup"><span data-stu-id="1a333-109">*contextid*</span></span> 
</dt> <dd>

<span data-ttu-id="1a333-110">Уникальное целое число, определяющее текст справки, связанный с текущей инструкцией MIDL.</span><span class="sxs-lookup"><span data-stu-id="1a333-110">A unique integer that identifies the help text associated with the current MIDL statement.</span></span>

</dd> <dt>

<span data-ttu-id="1a333-111">*список необязательных атрибутов*</span><span class="sxs-lookup"><span data-stu-id="1a333-111">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="1a333-112">Ноль или несколько атрибутов MIDL.</span><span class="sxs-lookup"><span data-stu-id="1a333-112">Zero or more MIDL attributes.</span></span>

</dd> <dt>

<span data-ttu-id="1a333-113">*IDL-оператор*</span><span class="sxs-lookup"><span data-stu-id="1a333-113">*idl-statement*</span></span> 
</dt> <dd>

<span data-ttu-id="1a333-114">Оператор MIDL, к которому будет применен атрибут **\[ хелпстрингконтекст \]** .</span><span class="sxs-lookup"><span data-stu-id="1a333-114">The MIDL statement to which the **\[helpstringcontext\]** attribute will be applied.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1a333-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1a333-115">Remarks</span></span>

<span data-ttu-id="1a333-116">Используйте функции **GetDocumentation2** в интерфейсах **ITypeLib2** и **ITypeInfo2** , чтобы получить строку справки.</span><span class="sxs-lookup"><span data-stu-id="1a333-116">Use the **GetDocumentation2** functions in the **ITypeLib2** and **ITypeInfo2** interfaces to retrieve the help string.</span></span>

## <a name="examples"></a><span data-ttu-id="1a333-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="1a333-117">Examples</span></span>

``` syntax
[
    uuid(. . .),
    helpstringcontext(103),
    version(1.0)
]
library Lines
{
    [
        uuid(. . .), 
        helpstringcontext(102),
        oleautomation,
        dual
    ]
    interface ILine : IDispatch
    {
        [propget, helpstringcontext(100)] HRESULT Color([out, retval] long* ReturnVal); 
        [propput, helpstringcontext(101)] HRESULT Color([in] long rgb);
    }
};
```

 

 




