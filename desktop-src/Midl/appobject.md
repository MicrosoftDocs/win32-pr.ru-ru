---
title: appobject - атрибут
description: Атрибут \ аппобжект \ определяет компонент coclass как объект приложения, связанный с полноценным приложением EXE.
ms.assetid: f4fcdf55-7431-4d66-8a46-f741c52fbe56
keywords:
- атрибут аппобжект MIDL
topic_type:
- apiref
api_name:
- appobject
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0d937d4a83306bc0c29f3c8c806bc043febec6a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104412846"
---
# <a name="appobject-attribute"></a>appobject - атрибут

Атрибут **\[ аппобжект \]** идентифицирует [**компонентный класс**](coclass.md) как объект приложения, связанный с полноценным приложением exe.

``` syntax
[
    uuid(uuid-number), 
    appobject 
  [, coclass-attribute-list]
]
coclass classname 
{ 
    [coclass definition]
}
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*UUID — номер* 
</dt> <dd>

Задает универсальный уникальный идентификационный номер для [**компонентного класса**](coclass.md).

</dd> <dt>

*Список атрибутов coclass* 
</dt> <dd>

Указывает ноль или более атрибутов, которые применяются к оператору [**coclass**](coclass.md) . Допустимыми атрибутами **coclass** являются [**\[ helpString \]**](helpstring.md), [**\[ HelpContext \]**](helpcontext.md), [**\[ License \]**](licensed.md), [**\[ Version \]**](version.md), [**\[ Control \]**](control.md)и [**\[ Hidden \]**](hidden.md).

</dd> <dt>

*classname* 
</dt> <dd>

Указывает имя, по которому объект компонента известен в библиотеке типов.

</dd> <dt>

*определение coclass* 
</dt> <dd>

Указывает инструкции, составляющие определение [**класса**](coclass.md) .

</dd> </dl>

## <a name="remarks"></a>Комментарии

Атрибут **\[ аппобжект \]** также указывает, что функции и свойства [**компонентного класса**](coclass.md) глобально доступны в текущей библиотеке типов.

Представление типефлаг для этого атрибута — ТИПЕФЛАГ \_ фаппобжект

## <a name="examples"></a>Примеры

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    helpstring("Hello Class"),
    appobject
] 
coclass Hello
{
    [default] interface IHello : IUnknown;
    interface IDispatch;
}
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**кокласс**](coclass.md)
</dt> <dt>

[**элемента**](control.md)
</dt> <dt>

[Создание библиотеки типов с помощью MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**helpstring**](helpstring.md)
</dt> <dt>

[**helpcontext**](helpcontext.md)
</dt> <dt>

[**служеб**](hidden.md)
</dt> <dt>

[**обладателем**](licensed.md)
</dt> <dt>

[Пример файла ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Синтаксис файла ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[типефлагс](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**Версия**](version.md)
</dt> </dl>

 

 