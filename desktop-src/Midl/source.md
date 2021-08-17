---
title: source - атрибут
description: Атрибут \ Source \ указывает, что член класса, свойства или метода является источником событий. Для члена класса coclass этот атрибут означает, что элемент вызывается, а не реализован.
ms.assetid: fbd5411a-e614-4643-810a-f3765e7ec16d
keywords:
- Исходный атрибут MIDL
topic_type:
- apiref
api_name:
- source
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08f7039505846d7a35bbd0e077456905c0d29ad13be398fe673ca5c1f8da25e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066684"
---
# <a name="source-attribute"></a>source - атрибут

Атрибут **\[ source \]** указывает на то, что член [**класса**](coclass.md), свойства или метода является источником событий. Для члена **класса coclass** этот атрибут означает, что элемент вызывается, а не реализован.

``` syntax
[
    coclass-attributes
]
coclass coclass-name
{
    [source [, optional-attributes] ] statement-type statement-name; 
  [, ...]
}

[source] object-type function-name(optional-parameter-list);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*атрибуты coclass* 
</dt> <dd>

Ноль или более атрибутов, которые будут применены к [**компонентному классу**](coclass.md).

</dd> <dt>

*имя класса* 
</dt> <dd>

Идентификатор имени [**компонентного класса**](coclass.md).

</dd> <dt>

*необязательные атрибуты* 
</dt> <dd>

Ноль или несколько атрибутов MIDL.

</dd> <dt>

*оператор-тип* 
</dt> <dd>

Может быть [**интерфейсом**](interface.md) или [**DISP**](dispinterface.md).

</dd> <dt>

*имя оператора* 
</dt> <dd>

Имя [**интерфейса**](interface.md) или [**DISP**](dispinterface.md).

</dd> <dt>

*Object-Type* 
</dt> <dd>

Тип объекта, возвращаемого методом. Этот объект является источником событий.

</dd> <dt>

*имя функции* 
</dt> <dd>

Имя метода в [**интерфейсе**](interface.md) или [**DISP**](dispinterface.md).

</dd> <dt>

*список необязательных параметров* 
</dt> <dd>

Ноль или более параметров метода.

</dd> </dl>

## <a name="remarks"></a>Remarks

В свойстве или методе **\[ исходный \]** атрибут указывает, что член возвращает объект или вариант, являющийся источником событий. Объект реализует **IConnectionPointContainer**.

### <a name="flags"></a>Флаги

ИМПЛТИПЕФЛАГ \_ фсаурце, \_ источник варфлаг, \_ источник функфлаг

## <a name="examples"></a>Примеры

``` syntax
[default, source] dispinterface DIMyFaceAdviseSink;
[source]interface IMyFaceAdviseSink;
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**кокласс**](coclass.md)
</dt> <dt>

[**интерфейса**](dispinterface.md)
</dt> <dt>

[Создание библиотеки типов с помощью MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**взаимодействия**](interface.md)
</dt> <dt>

[Пример файла ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Синтаксис файла ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[типефлагс](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 