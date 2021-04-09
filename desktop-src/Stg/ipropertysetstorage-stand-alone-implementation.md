---
title: IPropertySetStorage — изолированная реализация
description: Предоставляемая системой изолированная реализация IPropertySetStorage включает реализацию как Ипропертистораже, так и IPropertySetStorage.
ms.assetid: 0ea5aadf-0b3f-44ac-9bb7-a7e8292f04c2
keywords:
- IPropertySetStorage Стрктд STG, реализации
- IPropertySetStorage Стрктд STG, реализации, автономные
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f9fd0afe31775b06b3a5f61f4c79939be976e98
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070111"
---
# <a name="ipropertysetstorage-stand-alone-implementation"></a>IPropertySetStorage — изолированная реализация

Предоставляемая системой изолированная реализация [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) включает реализацию как [**ипропертистораже**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) , так и **IPropertySetStorage**. [**Ипропертистораже**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) — это интерфейс, который считывает и записывает свойства в хранилище набора свойств. [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) — это интерфейс, который создает и открывает наборы свойств в хранилище. Интерфейсы [**иенумстатпропстг**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) и [**иенумстатпропсетстг**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) также предоставляются в изолированной реализации.

Чтобы использовать изолированную реализацию [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage), сначала получите указатель на предоставляемую системой изолированную реализацию и свяжите предоставленную системой реализацию с объектом хранилища. Чтобы получить указатель на изолированную реализацию **IPropertySetStorage**, вызовите функцию [**стгкреатепропсетстг**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropsetstg) и укажите параметр *пстораже* , указывающий объект хранилища, который будет содержать набор свойств. Эта функция предоставляет указатель на новый интерфейс **IPropertySetStorage** для указанного объекта хранилища.

Изолированная реализация [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) создает наборы свойств для любого объекта хранилища, а не только для хранилищ составных файлов. Изолированная реализация не зависит от составных файлов и может использоваться с любой реализацией структурированных хранилищ. Все ограничения на предоставляемые вызывающим объектом структурированные хранилища применяются к этой реализации наборов свойств. Например, если вы предоставляете хранилище в простом режиме для [**стгопенпропстг**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg), полученный **IPropertySetStorage** будет ограничен предоставленным [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage).

Дополнительные сведения о реализации составного файла этого интерфейса см. в разделе [IPropertySetStorage-составной реализации файла](ipropertysetstorage-compound-file-implementation.md).

## <a name="when-to-use"></a>Назначение

Вызывайте методы [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) для создания, открытия и удаления наборов свойств в любом структурированном хранилище. Существует также метод, который предоставляет указатель на перечислитель [**иенумстатпропсетстг**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) , который можно использовать для перечисления наборов свойств в хранилище.

Изолированная реализация также предоставляет вспомогательные функции [**стгкреатепропстг**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg) и [**стгопенпропстг**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg) в дополнение к методам [**CREATE**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) и [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) для создания и открытия наборов свойств. Эти две функции добавляют поддержку \_ НЕбуферизованного значения пропсетфлаг, поэтому вы можете записывать изменения непосредственно в набор свойств вместо их буферизации в кэше. Дополнительные сведения см. в разделе [**константы пропсетфлаг**](propsetflag-constants.md).

## <a name="methods"></a>Методы

Изолированная реализация [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) поддерживает следующие методы.

<dl> <dt>

<span id="IPropertySetStorage__Create"></span><span id="ipropertysetstorage__create"></span><span id="IPROPERTYSETSTORAGE__CREATE"></span>[**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)
</dt> <dd>

Создает новое свойство, заданное в хранилище, и возвращает указатель на интерфейс [**ипропертистораже**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) в наборе свойств.

Если вы планируете использовать значение без \_ буферизации пропсетфлаг, то вместо этого используйте функцию [**стгкреатепропстг**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg) , чтобы создать и открыть новый набор свойств и получить указатель на изолированную реализацию интерфейса [**ипропертистораже**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) в наборе свойств.

</dd> <dt>

<span id="IPropertySetStorage__Open"></span><span id="ipropertysetstorage__open"></span><span id="IPROPERTYSETSTORAGE__OPEN"></span>[**IPropertySetStorage:: Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open)
</dt> <dd>

Открывает существующий набор свойств в хранилище и возвращает указатель на интерфейс [**ипропертистораже**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) в наборе свойств.

Если вы планируете использовать значение без \_ буферизации пропсетфлаг, используйте функцию [**стгопенпропстг**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg) , чтобы получить указатель на изолированную реализацию [**ипропертистораже**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) для указанного набора свойств.

</dd> <dt>

<span id="IPropertySetStorage__Delete"></span><span id="ipropertysetstorage__delete"></span><span id="IPROPERTYSETSTORAGE__DELETE"></span>[**IPropertySetStorage::D удалить**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-delete)
</dt> <dd>

Удаляет свойство, заданное в этом свойстве хранилища.

</dd> <dt>

<span id="IPropertySetStorage__Enum"></span><span id="ipropertysetstorage__enum"></span><span id="IPROPERTYSETSTORAGE__ENUM"></span>[**IPropertySetStorage:: Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-enum)
</dt> <dd>

Создает объект, который можно использовать для перечисления структур [**статпропсетстг**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) . Каждая структура **статпропсетстг** предоставляет данные об отдельном наборе свойств.

> [!Note]  
> Набор свойств Документсуммаринформатион и Пользователяопределенные уникален в том, что в одном базовом потоке могут быть два раздела набора свойств. Дополнительные сведения см. в описании [наборов свойств документсуммаринформатион и пользователяопределенные](the-documentsummaryinformation-and-userdefined-property-sets.md) .

 

</dd> </dl>

## <a name="related-topics"></a>См. также

<dl> <dt>

[Ипропертистораже — изолированная реализация](ipropertystorage-stand-alone-implementation.md)
</dt> <dt>

[**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)
</dt> <dt>

[**ипропертистораже**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)
</dt> <dt>

[**IStorage:: Енумелементс**](/windows/desktop/api/Objidl/nf-objidl-istorage-enumelements)
</dt> <dt>

[**Константы ПРОПСЕТФЛАГ**](propsetflag-constants.md)
</dt> <dt>

[**статпропсетстг**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg)
</dt> <dt>

[**стгкреатепропсетстг**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropsetstg)
</dt> <dt>

[**стгкреатепропстг**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg)
</dt> <dt>

[**стгопенпропстг**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg)
</dt> <dt>

[**Константы СТГМ**](stgm-constants.md)
</dt> </dl>

 

 