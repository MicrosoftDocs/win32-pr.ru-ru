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
# <a name="helpstringcontext-attribute"></a>атрибут хелпстрингконтекст

Атрибут **\[ хелпстрингконтекст \]** задает 32-разрядный идентификатор контекста справки в файле справки. Атрибут **\[ хелпстрингконтекст \]** можно применить к [**библиотеке**](library.md), [**интерфейсу**](interface.md), [**DISP**](dispinterface.md), [**модулю**](module.md), [**соклассу**](coclass.md), операторам [**typedef**](typedef.md) , свойствам, параметрам и методам.

``` syntax
[  helpstringcontext(contextid)[, optional-attribute-list]] idl-statement
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*ContextId* 
</dt> <dd>

Уникальное целое число, определяющее текст справки, связанный с текущей инструкцией MIDL.

</dd> <dt>

*список необязательных атрибутов* 
</dt> <dd>

Ноль или несколько атрибутов MIDL.

</dd> <dt>

*IDL-оператор* 
</dt> <dd>

Оператор MIDL, к которому будет применен атрибут **\[ хелпстрингконтекст \]** .

</dd> </dl>

## <a name="remarks"></a>Комментарии

Используйте функции **GetDocumentation2** в интерфейсах **ITypeLib2** и **ITypeInfo2** , чтобы получить строку справки.

## <a name="examples"></a>Примеры

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

 

 




