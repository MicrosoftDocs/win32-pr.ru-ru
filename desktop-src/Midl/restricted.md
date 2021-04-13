---
title: restricted - атрибут
description: Атрибут \ Restricted указывает, что библиотека, или член модуля, интерфейса или DISP, не может вызываться произвольным образом.
ms.assetid: ad1ae84f-77f4-4028-bd71-ff01414e474e
keywords:
- ограниченный атрибут MIDL
topic_type:
- apiref
api_name:
- restricted
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eca610c0dcf29ebc3a767005b4c22e3231947e88
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104412895"
---
# <a name="restricted-attribute"></a>restricted - атрибут

Атрибут **\[ Restricted \]** указывает, что библиотеку, член модуля, интерфейса или disp-интерфейсов, нельзя вызывать произвольным образом.

``` syntax
[
    restricted
    [, other-attributes]
] 
statement-type statement-name 
{
    definitions
};
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*другие атрибуты* 
</dt> <dd>

Ноль или несколько атрибутов MIDL.

</dd> <dt>

*оператор-тип* 
</dt> <dd>

Один из следующих: [**Библиотека**](library.md), [**модуль**](module.md), [**интерфейс**](interface.md), [**DISP**](dispinterface.md).

</dd> <dt>

*имя оператора* 
</dt> <dd>

Идентификатор, по которому программное обеспечение ссылается на эту инструкцию.

</dd> <dt>

*вирус* 
</dt> <dd>

Языковые элементы MIDL, определяющие содержимое этой инструкции.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Этот атрибут позволяет управлять доступом к элементам интерфейсов, библиотек, модулей и диспетчерских интерфейсов. Например, это может препятствовать тому, что элемент данных будет использоваться программистом макроса. Этот атрибут можно применить к члену [**класса coclass**](coclass.md), независимо от того, является ли элемент DISP или интерфейсом, и независимо от того, является ли элемент приемником (входящим) или источником (исходящим). Член **coclass** не может иметь как **\[ ограниченный \]** атрибут, так и атрибуты **\[ по умолчанию \]** .

### <a name="flags"></a>Флаги

ИМПЛТИПЕФЛАГ \_ фрестриктед, функфлаг \_ фрестриктед

## <a name="examples"></a>Примеры

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    version (1.0), 
    restricted
] 
library MyLibrary
{
    // Library definition statements.
};

[propget, restricted] HRESULT MyProc(void);
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[типефлагс](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**библиотека**](library.md)
</dt> <dt>

[**взаимодействия**](interface.md)
</dt> <dt>

[**интерфейса**](dispinterface.md)
</dt> <dt>

[**модуль**](module.md)
</dt> <dt>

[Синтаксис файла ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Пример файла ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Создание библиотеки типов с помощью MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 