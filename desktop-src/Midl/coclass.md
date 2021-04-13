---
title: coclass - атрибут
description: Оператор CoClass предоставляет список поддерживаемых интерфейсов для объекта компонента.
ms.assetid: 2c636327-ad18-4087-b495-d1aa84a07f48
keywords:
- атрибут coclass MIDL
topic_type:
- apiref
api_name:
- coclass
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ba95b38675869637c679a2409a82fb812709ec8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104412897"
---
# <a name="coclass-attribute"></a>coclass - атрибут

Оператор **coclass** предоставляет список поддерживаемых интерфейсов для объекта компонента.

``` syntax
[
    coclass-attribute-list
]
coclass classname
{
    [
        interface-attributes
    ] 
    [interface | dispinterface] interfacename 
    {
  . . . 
    }
}
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*Список атрибутов coclass* 
</dt> <dd>

Атрибут **\[** [**UUID**](uuid.md) **\]** является обязательным для **компонентного класса**. Это тот же **\[ UUID \]** , который зарегистрирован в качестве идентификатора CLSID в системной базе данных регистрации. Атрибуты **\[** [**helpString**](helpstring.md) **\]** , **\[** [**HelpContext**](helpcontext.md) **\]** , **\[** [**License**](licensed.md) **\]** , **\[** [**Version**](version.md) **\]** , **\[** [**Control**](control.md) **\]** , **\[** [**Hidden**](hidden.md) **\]** и **\[** [**аппобжект**](appobject.md) **\]** принимаются, но не являются обязательными, перед определением **компонентного класса** .

</dd> <dt>

*classname* 
</dt> <dd>

Имя, по которому известен общий объект в библиотеке типов.

</dd> <dt>

*атрибуты интерфейса* 
</dt> <dd>

Необязательные атрибуты для интерфейса или DISP. Атрибуты **\[** [**Source**](source.md) **\]** , **\[** [**Default**](default.md) **\]** и **\[** [**Restricted**](restricted.md) **\]** принимаются в интерфейсе или DISP в **компонентном классе**.

</dd> <dt>

*InterfaceName* 
</dt> <dd>

Либо интерфейс, объявленный с помощью ключевого слова [**Interface**](interface.md) , либо disp-интерфейс, объявленный с ключевым словом [**DISP**](dispinterface.md) .

</dd> </dl>

## <a name="remarks"></a>Комментарии

Объектная модель компонента Microsoft определяет класс как реализацию, которая разрешает **QueryInterface** между наборами интерфейсов.

## <a name="examples"></a>Примеры

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676), 
    version(1.0), 
    helpstring("A class"), 
    helpcontext(2481), appobject
] 
coclass myapp 
{ 
    [source] interface IMydocfuncs : IUnknown; 
    dispinterface DMydocfuncs; 
}; 
 
[
    uuid(12345678-1234-1234-1234-123456789ABC)
] 
coclass mycoclass 
{ 
    [restricted] interface iface1; 
    interface iface2; 
}
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**appobject**](appobject.md)
</dt> <dt>

[**элемента**](control.md)
</dt> <dt>

[**параметры**](default.md)
</dt> <dt>

[**интерфейса**](dispinterface.md)
</dt> <dt>

[Создание библиотеки типов с помощью MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[Пример файла ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[**helpstring**](helpstring.md)
</dt> <dt>

[**helpcontext**](helpcontext.md)
</dt> <dt>

[**служеб**](hidden.md)
</dt> <dt>

[**взаимодействия**](interface.md)
</dt> <dt>

[**обладателем**](licensed.md)
</dt> <dt>

[Синтаксис файла ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**зона**](restricted.md)
</dt> <dt>

[**источника**](source.md)
</dt> <dt>

[типефлагс](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**UUID**](uuid.md)
</dt> <dt>

[**Версия**](version.md)
</dt> </dl>

 

 