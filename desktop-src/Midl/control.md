---
title: атрибут элемента управления
description: Атрибут \ Control \ определяет компонентный класс или библиотеку как элемент управления COM, из которого сайт контейнера будет наследовать дополнительные библиотеки типов или классы объектов компонентов.
ms.assetid: c39dd4b6-743f-4888-8954-8b83584bdea5
keywords:
- атрибут элемента управления MIDL
topic_type:
- apiref
api_name:
- control
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 982327d581ddb606f733e9efbbcb89e2f9972cf4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103789865"
---
# <a name="control-attribute"></a>атрибут элемента управления

Атрибут **\[ Control \]** определяет компонентный [**класс**](coclass.md) или [**библиотеку**](library.md) как элемент управления COM, из которого сайт контейнера будет наследовать дополнительные библиотеки типов или классы объектов компонентов.

``` syntax
[
    uuid, 
    control 
    [, attribute-list]
] 
library | coclass lib-or-coclassname 
{ 
    definitions 
}
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*Список атрибутов* 
</dt> <dd>

Указывает ноль или более атрибутов, применимых к оператору [**Library**](library.md) или [**coclass**](coclass.md) . Несколько атрибутов разделяются запятыми.

</dd> <dt>

*lib-или-коclassname* 
</dt> <dd>

Указывает имя [**библиотеки**](library.md) или [**компонентного класса**](coclass.md).

</dd> <dt>

*вирус* 
</dt> <dd>

Операторы MIDL, задающих члены [**библиотеки**](library.md) или [**coclass**](coclass.md).

</dd> </dl>

## <a name="remarks"></a>Комментарии

Этот атрибут позволяет помечать библиотеки типов, описывающие элементы управления, так что они не будут отображаться в браузерах типов, предназначенных для невизуальных объектов.

### <a name="flags"></a>Флаги

ТИПЕФЛАГ \_ фконтрол, либфлаг \_ фконтрол

## <a name="examples"></a>Примеры

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC),
    helpstring("Hello 2.1 COM Control Library"), 
    control,version(2.1)
] 
library Hello 
{ 
    /* library definitions */
}
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Синтаксис файла ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Пример файла ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Создание библиотеки типов с помощью MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[типефлагс](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**кокласс**](coclass.md)
</dt> <dt>

[**библиотека**](library.md)
</dt> </dl>

 

 