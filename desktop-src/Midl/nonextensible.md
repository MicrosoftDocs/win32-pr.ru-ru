---
title: Атрибут nonextensible
description: Атрибут \ "\ нерасширяемый \" указывает, что реализация IDispatch включает только свойства и методы, перечисленные в описании интерфейса, и не может быть расширена с помощью дополнительных элементов во время выполнения.
ms.assetid: 5fcffa65-4f0c-4180-a6c2-f68d63ff99ae
keywords:
- нерасширяемый атрибут MIDL
topic_type:
- apiref
api_name:
- nonextensible
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e591ea4ab0647449ca9296b3b14a4aab9fff6991
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105650330"
---
# <a name="nonextensible-attribute"></a>Атрибут nonextensible

**\[ Нерасширяемый \]** атрибут указывает, что реализация [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) включает только свойства и методы, перечисленные в описании интерфейса, и не может быть расширена с помощью дополнительных элементов во время выполнения. (По умолчанию Автоматизация предполагает, что интерфейсы могут добавлять членов во время выполнения, то есть предполагается, что они являются расширяемыми.)

``` syntax
[
    uuid(uuid-number), 
    nonextensible 
    [, optional-attribute-list]
] 
interface | dispinterface interface-name 
{
    interface-definition
}
```

## <a name="parameters"></a>Параметры

<dl> <dt>

*UUID — номер* 
</dt> <dd>

Задает универсальный уникальный идентификационный номер для [**интерфейса**](interface.md).

</dd> <dt>

*список необязательных атрибутов* 
</dt> <dd>

Указывает список атрибутов интерфейса MIDL, отданных от нуля или более.

</dd> <dt>

*имя интерфейса* 
</dt> <dd>

Указывает имя [**интерфейса**](interface.md) или [**DISP**](dispinterface.md).

</dd> <dt>

*определение интерфейса* 
</dt> <dd>

Задает инструкции IDL, которые формируют определение интерфейса или [**DISP**](dispinterface.md)- [**интерфейсов**](interface.md) .

</dd> </dl>

## <a name="remarks"></a>Комментарии

**\[ Нерасширяемый \]** атрибут можно применить как к интерфейсу, так и к диспетчеру интерфейса. Однако интерфейс также должен иметь **\[** [**сдвоенные**](dual.md) **\]** и **\[** [**oleautomation**](oleautomation.md) **\]** атрибуты.

### <a name="flags"></a>Флаги

ТИПЕФЛАГ \_ фнонекстенсибле

## <a name="examples"></a>Примеры

``` syntax
library Hello
{
    [
        uuid(12345678-1234-1234-1234-123456789ABC), 
        helpstring("A helpful description."),
        oleautomation, 
        dual, 
        nonextensible
    ] 
    interface IHello : IDispatch
    {
        // Interface definition statements.
    }
}
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Содержимое библиотеки типов](/previous-versions/windows/desktop/automat/contents-of-a-type-library)
</dt> <dt>

[**интерфейса**](dispinterface.md)
</dt> <dt>

[**двойной**](dual.md)
</dt> <dt>

[Создание библиотеки типов с помощью MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**взаимодействия**](interface.md)
</dt> <dt>

[Синтаксис файла ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**oleautomation**](oleautomation.md)
</dt> <dt>

[**типефлагс**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 