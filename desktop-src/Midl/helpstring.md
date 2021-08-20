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
ms.openlocfilehash: 7abb433d7112bc4c3257345d086ccf308cc1892b61a99991b485ce4962b5851e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013872"
---
# <a name="helpstring-attribute"></a>атрибут helpstring

Атрибут **\[ helpString \]** задает символьную строку, используемую для описания элемента, к которому он применяется. Атрибут **\[ helpString \]** можно применить к операторам Library, importlib, Interface, DISP, Module или coclass, определениям типов, свойствам и методам.

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

## <a name="parameters"></a>Параметры

<dl> <dt>

*Справка-текстовая строка* 
</dt> <dd>

Строка символов, заканчивающаяся нулем и содержащая текст справки.

</dd> <dt>

*список необязательных атрибутов* 
</dt> <dd>

Ноль или несколько операторов атрибута MIDL.

</dd> <dt>

*дерев* 
</dt> <dd>

Одна из следующих директив: [**Библиотека**](library.md), **\[** [**importlib**](importlib.md) **\]** , [**интерфейс**](interface.md), [**DISP**](dispinterface.md), [**модуль**](module.md), [**Определение типа**](typedef.md), **метод**, **свойство** или [**coclass**](coclass.md).

</dd> <dt>

*имя элемента* 
</dt> <dd>

Имя, которое другие программные компоненты могут использовать для отделения текущего элемента

</dd> <dt>

*definition* 
</dt> <dd>

Указывает инструкции, которые составляют определение элемента.

</dd> <dt>

*IDL-оператор* 
</dt> <dd>

Инструкция определения интерфейса MIDL, например [**propget**](propget.md) или [**propput**](propput.md).

</dd> </dl>

## <a name="remarks"></a>Remarks

Используйте функции [**GetString в**](/windows/win32/api/oaidl/nf-oaidl-itypelib-getdocumentation) интерфейсах [**ITypeLib**](/windows/win32/api/oaidl/nn-oaidl-itypelib) и [**ITypeInfo**](/windows/win32/api/oaidl/nn-oaidl-itypeinfo) для получения строки справки.

## <a name="examples"></a>Примеры

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

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Библиотечная**](library.md)
</dt> <dt>

[**importlib**](importlib.md)
</dt> <dt>

[**взаимодействия**](interface.md)
</dt> <dt>

[**интерфейса**](dispinterface.md)
</dt> <dt>

[**модуль**](module.md)
</dt> <dt>

[**кокласс**](coclass.md)
</dt> <dt>

[**определение**](typedef.md)
</dt> <dt>

[Синтаксис файла ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Пример файла ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Создание библиотеки типов с помощью MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 