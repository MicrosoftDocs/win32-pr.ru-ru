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
ms.openlocfilehash: 3caa5dd32257fb5d75bbf77cde4ae5e71c6e97574cd1c263ead47aacedccadc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895254"
---
# <a name="helpcontext-attribute"></a>helpcontext - атрибут

Атрибут \[ **HelpContext** \] задает идентификатор контекста, позволяющий пользователю просматривать сведения об этом элементе в файле справки.

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

## <a name="parameters"></a>Параметры

<dl> <dt>

*UUID — номер* 
</dt> <dd>

Задает универсальный уникальный идентификационный номер для [**библиотеки**](library.md), \[ [**importlib**](importlib.md) \] , [**интерфейса**](interface.md), [**DISP**](dispinterface.md), [**модуля**](module.md), [**определения типа**](typedef.md), **методов**, **\[ \] свойств** или [**coclass**](coclass.md).

</dd> <dt>

*HelpContext — значение* 
</dt> <dd>

Уникальное целое число, определяющее текст справки, связанный с текущим элементом MIDL.

</dd> <dt>

*Список атрибутов* 
</dt> <dd>

Указывает список из одного или нескольких атрибутов, которые применяются к элементу MIDL в целом.

</dd> <dt>

*дерев* 
</dt> <dd>

Одна из следующих директив: [**Библиотека**](library.md), \[ [**importlib**](importlib.md) \] , [**интерфейс**](interface.md), [**DISP**](dispinterface.md), [**модуль**](module.md), [**Определение типа**](typedef.md), **метод**, **свойство** или [**coclass**](coclass.md).

</dd> <dt>

*имя элемента* 
</dt> <dd>

Имя, которое другие программные компоненты могут использовать для отделения текущего элемента.

</dd> <dt>

*вирус* 
</dt> <dd>

Указывает инструкции, которые составляют определение элемента.

</dd> </dl>

## <a name="remarks"></a>Remarks

Атрибут \[ **HelpContext** \] может применяться к следующим элементам: [**Library**](library.md), \[ [**importlib**](importlib.md) \] , [**интерфейс**](interface.md), [**DISP**](dispinterface.md), [**module**](module.md), [**typedef**](typedef.md), **метод**, **свойство** или [**coclass**](coclass.md).

*Параметр HelpContext-value* — это 32-разрядный идентификатор контекста в файле справки, который можно получить с помощью функций функции- [**документации**](/windows/win32/api/oaidl/nf-oaidl-itypelib-getdocumentation) в интерфейсах [**ITypeLib**](/windows/win32/api/oaidl/nn-oaidl-itypelib) и [**ITypeInfo**](/windows/win32/api/oaidl/nn-oaidl-itypeinfo) .

## <a name="examples"></a>Примеры

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

## <a name="see-also"></a>См. также

<dl> <dt>

[**кокласс**](coclass.md)
</dt> <dt>

[**интерфейса**](dispinterface.md)
</dt> <dt>

[Создание библиотеки типов с помощью MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**importlib**](importlib.md)
</dt> <dt>

[**взаимодействия**](interface.md)
</dt> <dt>

[**Библиотечная**](library.md)
</dt> <dt>

[**модуль**](module.md)
</dt> <dt>

[Синтаксис файла ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Пример файла ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[**определение**](typedef.md)
</dt> </dl>

 

 