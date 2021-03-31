---
title: immediatebind - атрибут
description: Атрибут \ иммедиатебинд \ указывает, что база данных будет уведомлена сразу обо всех изменениях свойства объекта, привязанного к данным.
ms.assetid: 1c08ddca-e273-43b3-a8f6-ed7f552e4e0e
keywords:
- атрибут иммедиатебинд MIDL
topic_type:
- apiref
api_name:
- immediatebind
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc8a797514c15f8d4c46bb6161946d5d0b6bd10b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104260479"
---
# <a name="immediatebind-attribute"></a>immediatebind - атрибут

Атрибут **\[ иммедиатебинд \]** указывает, что база данных будет уведомлена сразу обо всех изменениях свойства объекта, привязанного к данным.

``` syntax
[
    interface-attribute-list
] 
interface | dispinterface interface-name 
{
    [bindable, immediatebind[, optional-attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*Interface-список атрибутов* 
</dt> <dd>

Указывает список из одного или нескольких атрибутов, которые применяются к интерфейсу в целом.

</dd> <dt>

*имя интерфейса* 
</dt> <dd>

Указывает имя [**интерфейса**](interface.md) или [**DISP**](dispinterface.md).

</dd> <dt>

*список необязательных атрибутов* 
</dt> <dd>

Ноль или более атрибутов функций.

</dd> <dt>

*ReturnType* 
</dt> <dd>

Указывает тип возвращаемого значения функции.

</dd> <dt>

*имя функции* 
</dt> <dd>

Указывает имя функции в IDL-файле.

</dd> <dt>

*params* 
</dt> <dd>

Ноль или более параметров функции.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Атрибут **\[ иммедиатебинд \]** позволяет элементам управления различать свойства, которые должны уведомлять базу данных о каждом изменении, и те, которые не имеют. Например, каждое изменение элемента управления CheckBox должно быть немедленно отправлено в базовую базу данных, даже если элемент управления не потерял фокус. Однако для элемента управления ListBox изменение происходит при выделении другого выделения. Уведомление базы данных об изменении до того, как элемент управления теряет фокус, будет неэффективным и ненужным. Атрибут **\[ иммедиатебинд \]** позволяет указать, установив бит иммедиатебинд, отдельные свойства формы, изменения которых следует сообщить немедленно.

Свойства, имеющие атрибут **\[ иммедиатебинд \]** , также должны иметь атрибут **\[** [**BIND**](bindable.md) **\]** .

### <a name="flags"></a>Флаги

ФУНКФЛАГ \_ фиммедиатебинд, варфлаг \_ фиммедиатебинд

## <a name="examples"></a>Примеры

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC)
] 
interface MyObject : IUnknown
{
    properties:
    methods:
        [id(1), propget, bindable, immediatebind] long Size(void);

        [id(1), propput, bindable, 
         immediatebind] HRESULT Size([in]long lSize);
}
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**bindable**](bindable.md)
</dt> <dt>

[**типефлагс**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**взаимодействия**](interface.md)
</dt> <dt>

[**интерфейса**](dispinterface.md)
</dt> <dt>

[Синтаксис файла ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Пример файла ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Создание библиотеки типов с помощью MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 