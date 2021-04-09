---
title: displaybind - атрибут
description: Атрибут \ дисплайбинд \ указывает свойство, которое должно быть отображено пользователю как связываемое.
ms.assetid: 047a58b2-3ae2-437a-992f-a9d1541decbe
keywords:
- атрибут дисплайбинд MIDL
topic_type:
- apiref
api_name:
- displaybind
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f015954a7b1fe07d4ecf61e9a4ba4da4c932e65c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790225"
---
# <a name="displaybind-attribute"></a>displaybind - атрибут

Атрибут **\[ дисплайбинд \]** указывает свойство, которое должно быть отображено пользователю как связываемое.

``` syntax
[
  [interface-attribute-list]
]
interface | dispinterface interface-name
{
    [bindable, displaybind [ , attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*Interface-список атрибутов* 
</dt> <dd>

Указывает необязательный список атрибутов интерфейса.

</dd> <dt>

*имя интерфейса* 
</dt> <dd>

Имя интерфейса.

</dd> <dt>

*Список атрибутов* 
</dt> <dd>

Задает список из одного или нескольких атрибутов, разделенных запятыми, которые применяются к типу возвращаемых функцией значений.

</dd> <dt>

*ReturnType* 
</dt> <dd>

Указывает тип возвращаемого значения функции.

</dd> <dt>

*имя функции* 
</dt> <dd>

Указывает имя функции, к которой будет применен атрибут **\[ дисплайбинд \]** .

</dd> <dt>

*params* 
</dt> <dd>

Список параметров функции.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Свойства, имеющие атрибут **\[ дисплайбинд \]** , также должны иметь атрибут **\[** [**BIND**](bindable.md) **\]** . Объект может поддерживать привязку данных, но не имеет этого атрибута.

### <a name="flags"></a>Флаги

ФУНКФЛАГ \_ фдисплайбинд, варфлаг \_ фдисплайбинд

## <a name="examples"></a>Примеры

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676)
] 
interface MyObject : IUnknown
{
    properties:
    methods:
        [id(1), propget, bindable, defaultbind, 
         displaybind] long Size(void);

        [id(1), propput, bindable, defaultbind, 
         displaybind] HRESULT Size([in]long lSize);
}
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**bindable**](bindable.md)
</dt> <dt>

[типефлагс](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[Синтаксис файла ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Пример файла ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Создание библиотеки типов с помощью MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 