---
title: атрибут библиотеки
description: Оператор Library содержит все сведения, используемые компилятором MIDL для создания библиотеки типов.
ms.assetid: d73acb17-abe4-4c31-a264-a131d1f9fa51
keywords:
- атрибут библиотеки MIDL
topic_type:
- apiref
api_name:
- library
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fc1f836174a57f6edfddd0575a10d40367c061c034369a1582cc8bf8ce17a53
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086374"
---
# <a name="library-attribute"></a>атрибут библиотеки

Оператор **Library** содержит все сведения, используемые компилятором MIDL для создания библиотеки типов.

``` syntax
[
    uuid(uuid-number), 
    [, optional-attribute-list]
] 
library library-name
{ 
    library-definition-statements
}
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*UUID — номер* 
</dt> <dd>

Задает универсальный уникальный идентификационный номер для библиотеки.

</dd> <dt>

*список необязательных атрибутов* 
</dt> <dd>

Задает дополнительные атрибуты, которые применяются ко всей инструкции **Library** . К допустимым атрибутам относятся **\[** [**Control**](control.md) **\]** , **\[** [**HelpContext**](helpcontext.md) **\]** , **\[** [**HelpFile**](helpfile.md) **\]** , **\[** [**helpString**](helpstring.md) **\]** , **\[** [**Hidden**](hidden.md) **\]** , **\[** [**LCID**](lcid.md) **\]** , **\[** [**Restricted**](restricted.md) **\]** и **\[** [**Version**](version.md) **\]** .

</dd> <dt>

*имя библиотеки* 
</dt> <dd>

Имя, по которому программные компоненты ссылаются на **библиотеку**.

</dd> <dt>

*Library-операторы определения* 
</dt> <dd>

Одна или несколько инструкций MIDL, которые определяют содержимое **библиотеки**.

</dd> </dl>

## <a name="remarks"></a>Remarks

Инструкции в блоке библиотеки могут использовать элементы, объявленные внутри или вне блока библиотеки. Операторы библиотеки могут использовать эти элементы как базовые типы, наследовать от этих элементов или просто ссылаться на них в строке следующим образом:

``` syntax
interface MyFace 
{
    // Interface definition statements
};

[
    // library attributes
] 
library
{
    interface MyFace;

    // Other library definition statements.
};
```

Компилятор MIDL создаст библиотеку типов, которая включает определения для каждого элемента внутри блока библиотеки, а также определения всех элементов, определенных вне и упоминаемых в блоке библиотеки.

Сведения о создании библиотеки типов и заглушек прокси и заголовков из одного IDL-файла см. в разделе [Создание прокси-библиотеки DLL и библиотеки типов из одного файла IDL](generating-a-proxy-dll-and-a-type-library-from-a-single-idl-file-2.md).

## <a name="examples"></a>Примеры

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    helpstring("Hello 2.0 Type Library"), 
    lcid(0x0409), 
    version(2.0)
] 
library Hello 
{
    /* Library definition statements */
};
```

## <a name="see-also"></a>См. также

<dl> <dt>

[Содержимое библиотеки типов](/previous-versions/windows/desktop/automat/contents-of-a-type-library)
</dt> <dt>

[**элемента**](control.md)
</dt> <dt>

[Создание библиотеки типов с помощью MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**helpcontext**](helpcontext.md)
</dt> <dt>

[**helpfile**](helpfile.md)
</dt> <dt>

[**helpstring**](helpstring.md)
</dt> <dt>

[**служеб**](hidden.md)
</dt> <dt>

[**намного**](lcid.md)
</dt> <dt>

[Синтаксис файла ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**зона**](restricted.md)
</dt> <dt>

[**Версия**](version.md)
</dt> </dl>

 

 