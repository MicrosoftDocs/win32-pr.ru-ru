---
title: Ипропертистораже — изолированная реализация
description: Предоставляемая системой изолированная реализация IPropertySetStorage включает реализацию Ипропертистораже, интерфейс, считывающий и записывающий свойства в хранилище набора свойств.
ms.assetid: 8de32538-de11-4e4d-9269-145b2accb099
keywords:
- Ипропертистораже — изолированная реализация
- Ипропертистораже Стрктд STG, реализации, автономные
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 200d7f328670b8945807b7db7f742feabe58ad32847e3c56aa98a34278a71fbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119662554"
---
# <a name="ipropertystorage-stand-alone-implementation"></a>Ипропертистораже — изолированная реализация

Предоставляемая системой изолированная реализация [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) включает реализацию [**ипропертистораже**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage), интерфейс, считывающий и записывающий свойства в хранилище набора свойств. Интерфейс **IPropertySetStorage** создает и открывает наборы свойств в хранилище. Интерфейсы [**иенумстатпропстг**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) и [**иенумстатпропсетстг**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) также предоставляются в изолированной реализации.

Чтобы получить указатель на изолированную реализацию [**ипропертистораже**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage), вызовите функцию [**стгкреатепропстг**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg) , чтобы создать новый набор свойств или [**стгопенпропстг**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg) , чтобы получить указатель интерфейса на существующем наборе свойств (или вызовите методы [**CREATE**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) или [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) в изолированной реализации [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) ).

Изолированная реализация [**ипропертистораже**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) создает наборы свойств для любого объекта хранилища или потока, а не только для хранения составных файлов и потоков. Изолированная реализация не зависит от составных файлов и может использоваться с любой реализацией структурированных хранилищ. Дополнительные сведения о реализации составного файла этого интерфейса см. в разделе [ипропертистораже-составной реализации файла](ipropertystorage-compound-file-implementation.md).

## <a name="when-to-use"></a>Назначение

Используйте [**ипропертистораже**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) для управления свойствами в пределах одного набора свойств. Его методы поддерживают чтение, запись и удаление обоих свойств, а также необязательные имена строк, которые могут быть связаны с идентификаторами свойств. Другие методы поддерживают стандартные операции фиксации и отката хранилища. Существует также метод, который задает время, связанное с хранилищем свойств, и другой, который разрешает использовать присваивание CLSID для связывания другого кода, например кода пользовательского интерфейса, с набором свойств. Метод [**enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum) предоставляет указатель на изолированную реализацию [**иенумстатпропстг**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg), которая перечисляет свойства в наборе.

## <a name="version-0-and-version-1-property-set-formats"></a>Форматы набора свойств версий 0 и 1

Изолированная реализация [**ипропертистораже**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) поддерживает свойства версии 0 и версии 1, устанавливая форматы сериализации. Дополнительные сведения см. в разделе [Свойства Сериализация набора свойств](version-0-vs--version-1-property-set-serialization.md). Наборы свойств создаются в формате версии 0 и остаются в этом формате, если не запрашиваются новые функции. В этот момент формат обновляется до версии 1.

Например, если набор свойств создается с \_ флагом пропсетфлаг по умолчанию, его формат имеет версию 0. При условии, что типы свойств, соответствующие формату версии 0, записываются и считываются из этого набора свойств, набор свойств остается в формате версии 0. Если тип свойства версии 1 записывается в набор свойств, набор свойств автоматически обновляется до версии 1. Впоследствии этот набор свойств больше не может быть прочитан реализациями, которые только понимают версию 0.

## <a name="ipropertystorage-and-variant-types"></a>Типы Ипропертистораже и Variant

Изолированная реализация [**ипропертистораже**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) не поддерживает варианты типов VT \_ Unknown или VT \_ Dispatch в элементе **VT** структуры [**пропвариант**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .

В SafeArray поддерживаются следующие типы вариантов. Это значит, что эти значения можно комбинировать с \_ массивом VT в элементе **VT** структуры [**пропвариант**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .



Типы Variant, поддерживаемые в SafeArray путем реализации составного файла для [ **ипропертистораже**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)

VT \_ I1

VT \_ UI1

VT \_ I2

VT \_ UI2

VT \_ I4

VT \_ UI4

VT \_ int

VT \_ uint

VT \_ R4

VT \_ R8

VT \_ CY

\_Дата VT

VT \_ BSTR

Логическое значение VT \_

VT \_ Decimal

\_Ошибка VT

\_вариант VT

 



 

Когда VT \_ Variant сочетается с \_ массивом VT, сам массив SafeArray содержит структуры [**пропвариант**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) . Тем не менее типы этих элементов должны быть взяты из предыдущего списка, не могут быть VT \_ и не могут включать \_ векторы VT, VT \_ или VT \_ ByRef.

## <a name="ipropertystorage-methods"></a>Методы Ипропертистораже

Изолированная реализация [**ипропертистораже**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) поддерживает следующие методы:

<dl> <dt>

<span id="IPropertyStorage__ReadMultiple"></span><span id="ipropertystorage__readmultiple"></span><span id="IPROPERTYSTORAGE__READMULTIPLE"></span>[**Ипропертистораже:: Реадмултипле**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple)
</dt> <dd>

Считывает свойства, указанные в массиве *ргпспек* , и предоставляет значения всех допустимых свойств в массиве *ргвар* элементов [**пропвариант**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .

В предоставляемой системой изолированной реализации дублированные идентификаторы свойств, которые ссылаются на Stream-или Storage-Types, приводят к созданию нескольких вызовов метода [**IStorage:: опенстреам**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) или [**IStorage:: опенстораже**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) , а успешное или неуспешное выполнение [**реадмултипле**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) зависит от возможности реализации базового хранилища для предоставления общего доступа к открытым хранилищам.

Кроме того, чтобы обеспечить поточно-ориентированную операцию, если одно и то же свойство Stream или Storage-value запрашивается несколько раз с помощью одного и того же указателя [**ипропертистораже**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) , открытие будет успешным или неудачным в зависимости от того, открыто ли свойство, а также от того, обрабатывает ли базовая файловая система множественное открытие потока или хранилища. Таким образом, операция [**реадмултипле**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) для потока или свойства, возвращающего хранение, всегда приводит к вызову [**IStorage:: опенстреам**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream)или [**IStorage:: опенстораже**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage), передаче доступа ( \_ например, стгм ReadWrite) и общим значениям ( \_ например, стгм общего доступа \_ ), указанным при первоначальном открытии или создании набора свойств.

Если метод завершается ошибкой, значения, записанные в *ргвар* , \[ \] не определяются. Если некоторые свойства, возвращающие поток или хранилище, успешно открыты, но перед завершением выполнения возникает ошибка, эти свойства должны быть освобождены до того, как метод возвратит значение.

</dd> <dt>

<span id="IPropertyStorage__WriteMultiple"></span><span id="ipropertystorage__writemultiple"></span><span id="IPROPERTYSTORAGE__WRITEMULTIPLE"></span>[**Ипропертистораже:: Вритемултипле**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple)
</dt> <dd>

Записывает свойства, указанные в  \[ \] массиве ргпспек, присваивая им теги [**пропвариант**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) и значения, указанные в *ргвар* \[ \] . Свойства, которые уже существуют, присваиваются указанным значениям **пропвариант** , а свойства, которые в настоящее время не существуют, создаются.

</dd> <dt>

<span id="IPropertyStorage__DeleteMultiple"></span><span id="ipropertystorage__deletemultiple"></span><span id="IPROPERTYSTORAGE__DELETEMULTIPLE"></span>[**Ипропертистораже::D Елетемултипле**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-deletemultiple)
</dt> <dd>

Удаляет свойства, указанные в параметре *ргпспек* \[ \] .

</dd> <dt>

<span id="IPropertyStorage__ReadPropertyNames"></span><span id="ipropertystorage__readpropertynames"></span><span id="IPROPERTYSTORAGE__READPROPERTYNAMES"></span>[**Ипропертистораже:: Реадпропертинамес**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readpropertynames)
</dt> <dd>

Считывает существующие имена строк, связанные с идентификаторами свойств, указанными в  \[ \] массиве ргпропид.

</dd> <dt>

<span id="IPropertyStorage__WritePropertyNames"></span><span id="ipropertystorage__writepropertynames"></span><span id="IPROPERTYSTORAGE__WRITEPROPERTYNAMES"></span>[**Ипропертистораже:: Вритепропертинамес**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writepropertynames)
</dt> <dd>

Присваивает строковые имена, указанные в массиве *рглпвстрнаме* , с идентификаторами свойств, указанными в массиве *ргпропид* .

</dd> <dt>

<span id="IPropertyStorage__DeletePropertyNames"></span><span id="ipropertystorage__deletepropertynames"></span><span id="IPROPERTYSTORAGE__DELETEPROPERTYNAMES"></span>[**Ипропертистораже::D Елетепропертинамес**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-deletepropertynames)
</dt> <dd>

Удаляет строки с идентификаторами свойств, указанными в массиве *ргпропид* , записывая **значение NULL** в имя свойства.

</dd> <dt>

<span id="IPropertyStorage__SetClass"></span><span id="ipropertystorage__setclass"></span><span id="IPROPERTYSTORAGE__SETCLASS"></span>[**Ипропертистораже:: Сеткласс**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-setclass)
</dt> <dd>

Задает **идентификатор CLSID** потока набора свойств. В изолированной реализации задание идентификатора CLSID для непростого набора свойств (в котором могут содержаться свойства, возвращающие потоковые значения, как описано в [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)) также задает идентификатор CLSID для базового подхранилища, чтобы его можно было получить с помощью вызова метода [**IStorage:: stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat).

</dd> <dt>

<span id="IPropertyStorage__Commit"></span><span id="ipropertystorage__commit"></span><span id="IPROPERTYSTORAGE__COMMIT"></span>[**Ипропертистораже:: Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit)
</dt> <dd>

Для простых и непростых наборов свойств очищает образ памяти с дисковой подсистемой. Кроме того, для непростых наборов свойств в режиме транзакций этот метод вызывает [**IStorage:: Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) для набора свойств.

</dd> <dt>

<span id="IPropertyStorage__Revert"></span><span id="ipropertystorage__revert"></span><span id="IPROPERTYSTORAGE__REVERT"></span>[**Ипропертистораже:: revert**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-revert)
</dt> <dd>

Для непростых наборов свойств вызывает метод [**reopen**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-revert) базового хранилища и повторно открывает поток "содержимое". Для простых наборов свойств возвращается только значение E \_ ОК.

</dd> <dt>

<span id="IPropertyStorage__Enum"></span><span id="ipropertystorage__enum"></span><span id="IPROPERTYSTORAGE__ENUM"></span>[**Ипропертистораже:: Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum)
</dt> <dd>

Создает объект перечислителя, который реализует [**иенумстатпропстг**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg), методы, которые могут быть вызваны для перечисления структур [**статпропстг**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) , предоставляющих сведения о каждом свойстве в наборе.

Эта реализация создает массив, в который считывается весь набор свойств и который может использоваться совместно при вызове [**иенумстатпропстг:: Clone**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) .

</dd> <dt>

<span id="IPropertyStorage__Stat"></span><span id="ipropertystorage__stat"></span><span id="IPROPERTYSTORAGE__STAT"></span>[**Ипропертистораже:: stat**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-stat)
</dt> <dd>

Заполняет элементы структуры [**статпропсетстг**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) , которая содержит сведения о свойстве, заданном в целом. При возврате предоставляет указатель на структуру.

Для непростых наборов хранения Эта реализация вызывает метод [**IStorage:: stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat) (или [**IStream:: stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat)) для получения сведений из базового хранилища или потока.

</dd> <dt>

<span id="IPropertyStorage__SetTimes"></span><span id="ipropertystorage__settimes"></span><span id="IPROPERTYSTORAGE__SETTIMES"></span>[**Ипропертистораже:: Сеттимес**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-settimes)
</dt> <dd>

Для непростых наборов свойств задает время, поддерживаемое базовым хранилищем. Эта реализация [**сеттимес**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-settimes) вызывает метод [**IStorage:: сетелементтимес**](/windows/desktop/api/Objidl/nf-objidl-istorage-setelementtimes) базового хранилища, чтобы изменить время. Он поддерживает время, поддерживаемое базовым методом, который может быть изменением времени, времени доступа или времени создания.

</dd> </dl>

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[IPropertySetStorage — изолированная реализация](ipropertysetstorage-stand-alone-implementation.md)
</dt> <dt>

[**ипропертистораже**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)
</dt> <dt>

[**IStorage:: Сетелементтимес**](/windows/desktop/api/Objidl/nf-objidl-istorage-setelementtimes)
</dt> <dt>

[**стгопенпропстг**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg)
</dt> <dt>

[**стгкреатепропстг**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg)
</dt> <dt>

[**стгкреатепропсетстг**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropsetstg)
</dt> </dl>

 

 