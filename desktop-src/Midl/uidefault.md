---
title: uidefault - атрибут
description: Атрибут \ уидефаулт \ указывает, что элемент сведений о типе является элементом по умолчанию для вывода в пользовательском интерфейсе.
ms.assetid: e789be38-a509-437d-89c9-ebbc830e5ae2
keywords:
- атрибут уидефаулт MIDL
topic_type:
- apiref
api_name:
- uidefault
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcef39f36abad7c7cb5562b2d892761bd1bb7b5b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104412816"
---
# <a name="uidefault-attribute"></a>uidefault - атрибут

Атрибут **\[ уидефаулт \]** указывает, что элемент сведений о типе является элементом по умолчанию для вывода в пользовательском интерфейсе.

``` syntax
[method-attribute-list, uidefault]return-type method-name(method-parameter-list)
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*Method — список атрибутов* 
</dt> <dd>

Другие атрибуты, которые применяются к методу.

</dd> <dt>

*Тип возвращаемого значения* 
</dt> <dd>

Тип данных, возвращаемых методом при завершении выполнения.

</dd> <dt>

*имя метода* 
</dt> <dd>

Имя метода.

</dd> <dt>

*метод-Parameter-список* 
</dt> <dd>

Ноль или более параметров для метода.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Применение атрибута **\[ уидефаулт \]** к члену интерфейса или DISP-интерфейсу сообщает Visual Basic во время разработки, чтобы автоматически отображать это событие или свойство пользователю. Это означает, что когда пользователь дважды щелкает объект, Visual Basic переходит к событию в исходном интерфейсе по умолчанию с атрибутом **\[ уидефаулт \]** . Когда пользователь выбирает объект, браузер свойств Visual Basic отображает свойство в исходном интерфейсе по умолчанию, который имеет этот атрибут. Если событие или свойство не имеет атрибута **\[ уидефаулт \]** , Visual Basic отображает первое событие или свойство, перечисленные в интерфейсе по умолчанию.

### <a name="typeflag-representation"></a>Представление типефлаг

Присутствие ФУНКФЛАГ \_ фуидефаулт или варфлаг \_ фуидефаулт

## <a name="examples"></a>Примеры

``` syntax
[
    dual,
    uuid(12345678-1234-1234-1234-123456789ABC),
    restricted
]
interface IForm: IDispatch
{
    [propget]HRESULT Backcolor([out, retval] long *Value);
    [propput]HRESULT Backcolor([in] long Value);
    [propget, uidefault]HRESULT Name([out, retval] BSTR *Value);
    [propput, uidefault]HRESULT Name([in] BSTR Value);
}
[
    odl,
    dual,
    uuid(87654321-1234-1234-1234-123456789ABC),
    restricted
] 
interface IFormEvents: IDispatch
{
    [uidefault]HRESULT Click();
    HRESULT Resize();
}

[
    uuid(12345678-1234-1234-1234-987654321ABC)
]
coclass Form
{
    [default] interface IForm;
    [default, source] interface IFormEvents;
}
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Создание библиотеки типов с помощью MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[Пример файла ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Синтаксис файла ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> </dl>

 

 