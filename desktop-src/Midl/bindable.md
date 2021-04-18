---
title: bindable - атрибут
description: Атрибут \ BIND \ указывает, что свойство поддерживает привязку данных.
ms.assetid: ba09096d-a2f7-4958-827c-0fba19ded26f
keywords:
- атрибут с возможностью привязки MIDL
topic_type:
- apiref
api_name:
- bindable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33911ba5ff55ef5e3dd377613dd98532ecd97486
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105681604"
---
# <a name="bindable-attribute"></a>bindable - атрибут

Атрибут **\[ BIND \]** указывает, что свойство поддерживает привязку данных.

``` syntax
[
    interface-attribute-list
] 
interface | dispinterface interface-name 
{
    [bindable[, attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*Interface-список атрибутов* 
</dt> <dd>

Задает список из нуля или нескольких атрибутов IDL, которые применяются к интерфейсу в целом. При наличии двух или более атрибутов интерфейса они должны быть разделены запятыми.

</dd> <dt>

*имя интерфейса* 
</dt> <dd>

Указывает имя интерфейса.

</dd> <dt>

*Список атрибутов* 
</dt> <dd>

Указывает ноль или более атрибутов, которые применяются к прототипу функции для свойства или метода в [**интерфейсе**](interface.md) или [**DISP**](dispinterface.md)-интерфейсы. Допустимы следующие атрибуты: [**\[ helpString \]**](helpstring.md), [**\[ \] HelpContext**](helpcontext.md), [**\[ \] String**](string.md), [**\[ дефаултбинд \]**](defaultbind.md), [**\[ дисплайбинд \]**](displaybind.md), [**\[ иммедиатебинд \]**](immediatebind.md), [**\[ propget \]**](propget.md), [**\[ propput \]**](propput.md), [**\[ propputref \]**](propputref.md)и [**\[ vararg \]**](vararg.md). Если указано **vararg** , последний параметр должен быть надежным массивом типа Variant. Несколько атрибутов разделяются запятыми.

</dd> <dt>

*ReturnType* 
</dt> <dd>

Указывает тип возвращаемого значения функции.

</dd> <dt>

*имя функции* 
</dt> <dd>

Указывает имя функции, к которой будет применен атрибут, **\[ допускающий привязку \]** .

</dd> <dt>

*params* 
</dt> <dd>

Список параметров функции.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Благодаря поддержке привязки данных атрибут **\[ BIND \]** позволяет клиенту получать уведомления при каждом изменении значения свойства. (Если требуется, чтобы клиент получал уведомления об ожидающих изменениях свойства, используйте атрибут [**\[ рекуестедит \]**](requestedit.md) .)

Поскольку атрибут, **\[ допускающий привязку \]** , ссылается на свойство в целом, его необходимо указывать везде, где определено свойство. Поэтому необходимо указать атрибут как для функции доступа к свойствам, так и для функции настройки свойства.

### <a name="flags"></a>Флаги

ФУНКФЛАГ \_ фбиндабле, варфлаг \_ фбиндабле

## <a name="examples"></a>Примеры

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676)
]
dispinterface MyObject 
{ 
    properties: 
    methods: 
        [id(1), propget, bindable, defaultbind, displaybind] long x(); 
        [id(1), propput, bindable, 
        defaultbind, displaybind] HRESULT x(long rhs); 
}
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**defaultbind**](defaultbind.md)
</dt> <dt>

[**интерфейса**](dispinterface.md)
</dt> <dt>

[**displaybind**](displaybind.md)
</dt> <dt>

[Создание библиотеки типов с помощью MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**helpstring**](helpstring.md)
</dt> <dt>

[**helpcontext**](helpcontext.md)
</dt> <dt>

[**immediatebind**](immediatebind.md)
</dt> <dt>

[**взаимодействия**](interface.md)
</dt> <dt>

[Пример файла ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Синтаксис файла ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**propget**](propget.md)
</dt> <dt>

[**propput**](propput.md)
</dt> <dt>

[**propputref**](propputref.md)
</dt> <dt>

[**requestedit**](requestedit.md)
</dt> <dt>

[**Строка**](string.md)
</dt> <dt>

[типефлагс](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**vararg**](vararg.md)
</dt> </dl>

 

 