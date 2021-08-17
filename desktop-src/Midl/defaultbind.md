---
title: defaultbind - атрибут
description: Атрибут \ дефаултбинд \ указывает единственное, связываемое свойство, которое лучше соответствует объекту.
ms.assetid: 8cf0922a-3d7c-404d-b4fd-edbd772987bf
keywords:
- атрибут дефаултбинд MIDL
topic_type:
- apiref
api_name:
- defaultbind
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a981d0469219a32b5931507f5df6d742e84fa67e6676e44c24edfb823f521a3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117807300"
---
# <a name="defaultbind-attribute"></a>defaultbind - атрибут

Атрибут **\[ дефаултбинд \]** указывает единственное, связываемое свойство, которое лучше соответствует объекту.

``` syntax
[
    interface-attribute-list
] 
interface | dispinterface interface-name 
{
    [bindable, defaultbind [, attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*Interface-список атрибутов* 
</dt> <dd>

Указывает список из одного или нескольких атрибутов, которые применяются к интерфейсу в целом. При наличии двух или более атрибутов интерфейса они должны быть разделены запятыми.

</dd> <dt>

*имя интерфейса* 
</dt> <dd>

Указывает имя интерфейса.

</dd> <dt>

*Список атрибутов* 
</dt> <dd>

Указывает список из одного или нескольких атрибутов, которые применяются к функции. При наличии двух или более атрибутов интерфейса они должны быть разделены запятыми.

</dd> <dt>

*ReturnType* 
</dt> <dd>

Указывает тип возвращаемого значения функции.

</dd> <dt>

*имя функции* 
</dt> <dd>

Указывает имя функции, к которой будет применен атрибут **\[ дефаултбинд \]** .

</dd> <dt>

*params* 
</dt> <dd>

Список параметров функции.

</dd> </dl>

## <a name="remarks"></a>Remarks

Свойства, имеющие атрибут **\[ дефаултбинд \]** , также должны иметь атрибут **\[** [**BIND**](bindable.md) **\]** . Только одно свойство в интерфейсе или DISP может иметь атрибут **\[ дефаултбинд \]** .

Этот атрибут используется контейнерами, содержащими пользовательскую модель привязки к объекту, а не привязку к свойству объекта. Объект может поддерживать привязку данных, но не имеет этого атрибута.

### <a name="flags"></a>Флаги

ФУНКФЛАГ \_ фдефаултбинд, варфлаг \_ фдефаултбинд

## <a name="examples"></a>Примеры

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC)
] 
interface MyObject : IUnknown
{
    properties:
    methods:
        [id(1), propget, bindable, 
         defaultbind, displaybind] long Size(void);

        [id(1), propput, bindable, 
         defaultbind, displaybind] HRESULT Size([in]long lSize);
}
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**bindable**](bindable.md)
</dt> <dt>

[Создание библиотеки типов с помощью MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[Пример файла ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Синтаксис файла ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[типефлагс](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 