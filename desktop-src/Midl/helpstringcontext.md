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
ms.openlocfilehash: e64e97ea0d7b41d87ef1d535d562f3b515dda4f59a67f6d5e35f97bed8b1f9ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117807239"
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

## <a name="remarks"></a>Remarks

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

 

 




