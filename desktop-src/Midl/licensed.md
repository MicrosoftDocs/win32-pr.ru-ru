---
title: лицензированный атрибут
description: Атрибут \ Licensed указывает, что компонент, к которому он применяется, имеет лицензию и должен быть создан с помощью IClassFactory2.
ms.assetid: c4789ea2-8ff6-423e-8b69-22a7a5392854
keywords:
- лицензированный атрибут MIDL
topic_type:
- apiref
api_name:
- licensed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b4320157216db18f595d67e172bc49de2d6050551732265060cb5a21339c908
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067213"
---
# <a name="licensed-attribute"></a>лицензированный атрибут

Атрибут **\[ Licensed \]** указывает, что [**компонент**](coclass.md) , к которому он применяется, имеет лицензию и должен быть создан с помощью [**IClassFactory2**](/windows/win32/api/ocidl/nn-ocidl-iclassfactory2).

``` syntax
[
    licensed
    [ , attribute-list ] 
]
coclass classname 
{
  coclass-definition
};
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*Список атрибутов* 
</dt> <dd>

Указывает ноль или более атрибутов, которые применяются к оператору [**coclass**](coclass.md) . Допустимыми атрибутами **coclass** являются **\[** [**helpString**](helpstring.md) **\]** , **\[** [**HelpContext**](helpcontext.md) **\]** , **\[ License \]**, **\[** [**Version**](version.md) **\]** , **\[** [**Control**](control.md) **\]** и **\[** [**Hidden**](hidden.md) **\]** .

</dd> <dt>

*classname* 
</dt> <dd>

Указывает имя, по которому объект компонента известен в библиотеке типов.

</dd> <dt>

*определение кокласса* 
</dt> <dd>

Указывает инструкции, составляющие определение [**класса**](coclass.md) .

</dd> </dl>

## <a name="remarks"></a>Remarks

Лицензирование — это функция COM, которая обеспечивает контроль над созданием объектов. Лицензированные объекты могут создаваться только клиентами, которым разрешено их использовать. Лицензирование реализуется в COM через интерфейс [**IClassFactory2**](/windows/win32/api/ocidl/nn-ocidl-iclassfactory2) и с помощью поддержки лицензионного ключа, который может быть передан во время выполнения.

### <a name="flags"></a>Флаги

ТИПЕФЛАГ \_ флиценсед

## <a name="examples"></a>Примеры

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    licensed, 
    helpstring("A meaningfulcomment"
]
coclass MyClass
{
    // coclass definition statements
};
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**кокласс**](coclass.md)
</dt> <dt>

[Содержимое библиотеки типов](/previous-versions/windows/desktop/automat/contents-of-a-type-library)
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

[Синтаксис файла ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[типефлагс](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**Версия**](version.md)
</dt> </dl>

 

 