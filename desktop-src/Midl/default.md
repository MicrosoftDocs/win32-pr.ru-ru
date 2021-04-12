---
title: default - атрибут
description: Атрибут \ Default \ указывает, что интерфейс или DISP, определенные в компонентном классе, представляют интерфейс программирования по умолчанию. Этот атрибут предназначен для использования в языках макросов.
ms.assetid: 66769dff-60a0-4e6e-9357-c4339c0bfa3f
keywords:
- атрибут по умолчанию MIDL
topic_type:
- apiref
api_name:
- default
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2171515bffc41abf2b5fe9a25826c2a71d3939c2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487585"
---
# <a name="default-attribute"></a>default - атрибут

Атрибут **\[ по \] умолчанию** указывает, что [**интерфейс**](interface.md) или [**DISP**](dispinterface.md), определенный в [**компонентном классе**](coclass.md), представляет интерфейс программирования по умолчанию. Этот атрибут предназначен для использования в языках макросов.

``` syntax
[
    uuid(uuid-number) 
    [, attribute-list]
] 
coclass coclass-name
{
    [ default [, optional-interface-attribute] ]; 
    interface | dispinterface interface-name;
}
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*UUID — номер* 
</dt> <dd>

Задает универсальный уникальный идентификационный номер для [**компонентного класса**](coclass.md).

</dd> <dt>

*Список атрибутов* 
</dt> <dd>

Задает дополнительные атрибуты [**coclass**](coclass.md) . Несколько атрибутов разделяются запятыми.

</dd> <dt>

*имя класса* 
</dt> <dd>

Указывает имя, по которому другие программные компоненты могут ссылаться [**на этот компонент**](coclass.md).

</dd> <dt>

*Необязательный атрибут-Interface-* 
</dt> <dd>

**\[** [**Исходный**](source.md) **\]** атрибут, указывающий, что интерфейс или DISP-интерфейсы является исходящим, является единственным другим атрибутом, который можно использовать здесь.

</dd> <dt>

*имя интерфейса* 
</dt> <dd>

Указывает имя интерфейса.

</dd> </dl>

## <a name="remarks"></a>Комментарии

[**Компонентный класс**](coclass.md) может иметь не более двух элементов **\[ по умолчанию \]** . Один представляет исходящий (исходный) интерфейс, а другой — входящий (приемник) интерфейс или DISP. Если атрибут **\[ по \] умолчанию** не указан ни для одного члена **класса coclass** или **котипа**, то первые исходящие и входящие члены, не имеющие **\[** атрибута [**Restricted**](restricted.md) , **\]** рассматриваются как значения по умолчанию.

### <a name="flags"></a>Флаги

ИМПЛТИПЕФЛАГ \_ фдефаулт

## <a name="examples"></a>Примеры

``` syntax
[ 
    uuid(12345678-1234-1234-1234-123456789ABC), 
    helpstring("Hello Class"),appobject
]  
coclass Hello
{
    [default] interface IHello:IUnknown;
    interface IDispatch;
};
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**кокласс**](coclass.md)
</dt> <dt>

[типефлагс](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[Синтаксис файла ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Пример файла ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Создание библиотеки типов с помощью MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**зона**](restricted.md)
</dt> <dt>

[**источника**](source.md)
</dt> </dl>

 

 