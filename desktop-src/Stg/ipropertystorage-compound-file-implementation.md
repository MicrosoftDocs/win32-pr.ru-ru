---
title: Реализация файла IPropertyStorage-Compound
description: реализация структурированной служба хранилища архитектуры COM называется составными файлами.
ms.assetid: c4b4f313-de58-44f2-8ce1-a07cc187d8ca
keywords:
- Ипропертистораже Стрктд STG, реализации, составной файл
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa3c4fffe98c4bfb896f346f25ce988f75bacf1fbb194b9ec27f50e22095c8cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119662614"
---
# <a name="ipropertystorage-compound-file-implementation"></a>Реализация файла IPropertyStorage-Compound

реализация структурированной служба хранилища архитектуры COM называется [составными файлами](istorage-compound-file-implementation.md). служба хранилища объекты, реализованные в составных файлах, включают реализацию обоих [**ипропертистораже**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage), интерфейс, управляющий одним набором постоянных свойств, и [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage), интерфейс, который управляет группами постоянных наборов свойств. дополнительные сведения об интерфейсе **ипропертистораже** см. в разделе рекомендации по **ипропертистораже** и [свойствам служба хранилища](property-storage-considerations.md).

Чтобы получить указатель на реализацию составного файла [**ипропертистораже**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage), вызовите [**стгкреатесторажеекс**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) , чтобы создать новый объект составного файла, или [**стгопенсторажеекс**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) , чтобы открыть ранее созданный объект составного файла. В случае с **стгкреатесторажеекс** параметр *стгфмт* должен иметь значение стгфмт \_ Storage. В случае с **стгопенсторажеекс** параметр *стгфмт* должен иметь значение стгфмт \_ Storage или стгфмт \_ ANY. В обоих случаях параметр *riid* должен иметь значение IID \_ IPropertySetStorage. Обе функции предоставляют указатель на интерфейс [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) объекта. Вызвав метод [**создания**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) или [**открытия**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) этого интерфейса, вы получите указатель на интерфейс **ипропертистораже** , который можно использовать для вызова любого из его методов.

Альтернативный способ получения указателя на реализацию составного файла [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) заключается в вызове более старых функций [**стгкреатедокфиле**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) и [**стгопенстораже**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage) или при указании параметра *riid* IID \_ IStorage для функции [**стгкреатесторажеекс**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) или [**стгопенсторажеекс**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) . В любом случае возвращается указатель на интерфейс [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) объекта. С помощью постоянных наборов свойств вызовите [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) для интерфейса **IPropertySetStorage** , указав определенное заголовком имя для идентификатора интерфейса IID \_ IPropertySetStorage.

## <a name="when-to-use"></a>Назначение

Используйте [**ипропертистораже**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) для управления свойствами в пределах одного набора свойств. Его методы поддерживают чтение, запись и удаление обоих свойств, а также необязательные имена строк, которые могут быть связаны с идентификаторами свойств. Другие методы поддерживают стандартные операции фиксации и отката хранилища. Существует также метод, который позволяет задать время, связанное с хранилищем свойств, и другое, которое позволяет назначить идентификатор CLSID, который может использоваться для связывания другого кода, например кода пользовательского интерфейса, с набором свойств. Вызов метода [**enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum) предоставляет указатель на реализацию составного файла [**иенумстатпропстг**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg), который позволяет перечислить свойства в наборе.

> [!Note]  
> Если вы получаете указатель на [**ипропертистораже**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) , вызывая [**стгкреатедокфиле**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile), [**стгкреатесторажеекс**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex), [**стгопенстораже**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage) или [**стгопенсторажеекс**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) в хранилище с набором свойств простого режима, методы **IPropertyStorage** соответствуют правилам потоков простого режима. Свойство хранилище устанавливается в простом режиме, если оно было получено для файла, который был создан или открыт с помощью \_ простого флага стгм. В этом случае не всегда можно сделать базовый поток большим, и нельзя заменить существующие свойства более крупными свойствами. Дополнительные сведения см. в разделе [реализация составного файла IPropertySetStorage](ipropertysetstorage-compound-file-implementation.md).

 

## <a name="ipropertystorage-and-caching"></a>Ипропертистораже и кэширование

Реализация составного файла в кэше [**ипропертистораже**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) открывает наборы свойств в памяти, чтобы повысить производительность. В результате изменения набора свойств не записываются в составной файл до тех пор, пока не будут вызваны методы [**фиксации**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit) или **выпуска** (последняя ссылка).

## <a name="simple-mode-property-sets"></a>Наборы свойств простого режима

Объект хранилища свойств находится в простом режиме, если он создается из объекта хранилища, установленного в простом режиме. Например, объект хранилища, заданный свойством, будет находиться в простом режиме, если он был получен из функции [**стгопенсторажеекс**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) с \_ установленным в параметре *грфмоде* флагом стгм Simple. Обратите внимание, что "простой режим" не связан с "простыми наборами свойств". Набор свойств является простым, если он создается путем вызова [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) с \_ непростым флагом пропсетфлаг, установленным в параметре *грффлагс* . дополнительные сведения о простых и непростых наборах свойств см. [в разделе служба хранилища и потоковые объекты для набора свойств](storage-vs--stream-for-a-property-set.md).

При создании объекта хранилища свойств простого режима ограничения его использования отсутствуют. При открытии существующего объекта хранилища свойств простого режима его базовый объект потока, хранящий набор свойств, не может быть увеличен. Следовательно, не всегда можно изменить такой объект хранилища свойств, если это изменение требует большого потока.

## <a name="property-set-formats"></a>Форматы набора свойств

Реализация составного файла [**ипропертистораже**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) поддерживает свойства версии 0 и версии 1, устанавливающие форматы сериализации. формат версии 1 поддерживается на компьютерах, работающих на Windows 2000. Дополнительные сведения см. в разделе [Свойства Сериализация набора свойств](version-0-vs--version-1-property-set-serialization.md). Наборы свойств создаются в формате версии 0 и остаются в этом формате, если не запрашиваются новые функции. В этом случае формат обновляется до версии 1.

Например, если набор свойств создается с \_ флагом пропсетфлаг по умолчанию, его формат имеет версию 0. При условии, что типы свойств, соответствующие формату версии 0, записываются и считываются из этого набора свойств, набор свойств остается в формате версии 0. Если тип свойства версии 1 записывается в набор свойств, набор свойств автоматически обновляется до версии 1. Впоследствии этот набор свойств больше не может быть прочитан реализациями, которые распознают только версию 0.

## <a name="ipropertystorage-and-variant-types"></a>Типы Ипропертистораже и Variant

Реализация составного файла [**ипропертистораже**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) не поддерживает типы Variant \_ неизвестные или VT \_ Dispatch в элементе **VT** структуры [**пропвариант**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .

В следующей таблице перечислены типы Variant, которые поддерживаются в массиве SafeArray. Это значит, что эти значения можно комбинировать с \_ массивом VT в элементе **VT** структуры [**пропвариант**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .



Типы Variant, поддерживаемые в SafeArray путем реализации составного файла для Ипропертистораже

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

Реализация составного файла [**ипропертистораже**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) поддерживает следующие методы:

<dl> <dt>

<span id="IPropertyStorage__ReadMultiple"></span><span id="ipropertystorage__readmultiple"></span><span id="IPROPERTYSTORAGE__READMULTIPLE"></span>[**Ипропертистораже:: Реадмултипле**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple)
</dt> <dd>

Считывает свойства, указанные в массиве *ргпспек* , и предоставляет значения всех допустимых свойств в массиве *ргвар* объекта пропвариантс. В реализации составного файла COM дублированные идентификаторы свойств, которые ссылаются на типы Stream или Storage, приводят к многократному вызову [**IStorage:: опенстреам**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) или [**IStorage:: опенстораже**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) , а успех или неудача **реадмултипле** зависят от возможности реализации базового хранилища для совместного использования операций открытия. Так как в составном файле СТГМ \_ общий ресурс с \_ монопольным доступом принудительно, несколько неудачных попыток открытия не удастся. Открытие одного и того же объекта хранилища более одного раза из одного родительского хранилища не поддерживается. \_ \_ Необходимо указать флаг монопольного доступа стгм.

Кроме того, чтобы обеспечить поточно-ориентированную операцию, если одно и то же свойство Stream или Storage-value запрашивается несколько раз с помощью одного и того же указателя [**ипропертистораже**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) в реализации составного файла com, операция открытия будет выполнена успешно или неудачно, в зависимости от того, открыто ли свойство, и является ли базовая файловая система, обрабатывающая несколько вакансий потока или хранилища. Таким образом, операция **реадмултипле** для потока или свойства, возвращающего хранение, всегда приводит к вызову [**IStorage:: опенстреам**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream)или [**IStorage:: опенстораже**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage), который передает доступ (стгм ReadWrite и т. д. \_ ) и используют флаги общего доступа (стгм \_ Share \_ монопольно и т. д.), указанные при открытии или создании исходного набора свойств.

Если метод завершается ошибкой, значения, записанные в *ргвар* , \[ \] не определяются. Если некоторые свойства потока или значения, возвращающие хранилище, успешно открыты, но перед завершением выполнения возникает ошибка, они должны быть освобождены перед возвратом из метода.

</dd> <dt>

<span id="IPropertyStorage__WriteMultiple"></span><span id="ipropertystorage__writemultiple"></span><span id="IPROPERTYSTORAGE__WRITEMULTIPLE"></span>[**Ипропертистораже:: Вритемултипле**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple)
</dt> <dd>

Записывает свойства, указанные в  \[ \] массиве ргпспек, присваивая им теги [**пропвариант**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) и значения, указанные в *ргвар* \[ \] . Свойства, которые уже существуют, присваиваются указанным значениям **пропвариант** . Создаются свойства, которые в настоящее время не существуют.

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

Удаляет имена свойств, указанных в  \[ \] массиве ргпропид.

</dd> <dt>

<span id="IPropertyStorage__SetClass"></span><span id="ipropertystorage__setclass"></span><span id="IPROPERTYSTORAGE__SETCLASS"></span>[**Ипропертистораже:: Сеткласс**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-setclass)
</dt> <dd>

Задает **идентификатор CLSID** потока набора свойств. В реализации составного файла установка идентификатора CLSID для непростого набора свойств (в котором может храниться значение свойства, возвращающего хранение или потоковые значения, как описано в разделе [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)) также задает идентификатор CLSID для базового подхранилища, чтобы его можно было получить с помощью вызова метода [**IStorage:: stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat).

</dd> <dt>

<span id="IPropertyStorage__Commit"></span><span id="ipropertystorage__commit"></span><span id="IPROPERTYSTORAGE__COMMIT"></span>[**Ипропертистораже:: Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit)
</dt> <dd>

Для простых и непростых наборов свойств очищает образ памяти, заданный свойством, в базовое хранилище. Кроме того, для непростых наборов свойств в режиме транзакций этот метод выполняет фиксацию (как в [**IStorage:: Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit)) для хранилища, содержащего набор свойств.

</dd> <dt>

<span id="IPropertyStorage__Revert"></span><span id="ipropertystorage__revert"></span><span id="IPROPERTYSTORAGE__REVERT"></span>[**Ипропертистораже:: revert**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-revert)
</dt> <dd>

Для непростых наборов свойств вызывает метод [**reopen**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-revert) базового хранилища и повторно открывает поток "содержимое". Для простых наборов свойств этот интерфейс всегда возвращает значение S \_ ОК. Непростые наборы свойств — это те, которые были созданы с помощью \_ НЕпростого флага пропсетфлаг в методе [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) . дополнительные сведения см. [в разделе служба хранилища и потоковые объекты для набора свойств](storage-vs--stream-for-a-property-set.md) .

</dd> <dt>

<span id="IPropertyStorage__Enum"></span><span id="ipropertystorage__enum"></span><span id="IPROPERTYSTORAGE__ENUM"></span>[**Ипропертистораже:: Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum)
</dt> <dd>

Конструирует экземпляр [**иенумстатпропстг**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg), методы которого могут быть вызваны для перечисления структур [**статпропстг**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) , предоставляющих сведения о каждом свойстве в наборе. Эта реализация создает массив, в который считывается весь набор свойств и который может использоваться совместно при вызове **иенумстатпропстг:: Clone** . Изменения в наборе свойств не отражаются в открытом экземпляре **иенумстатпропстг** . Чтобы увидеть такие изменения, необходимо создать новый экземпляр этого перечислителя.

</dd> <dt>

<span id="IPropertyStorage__Stat"></span><span id="ipropertystorage__stat"></span><span id="IPROPERTYSTORAGE__STAT"></span>[**Ипропертистораже:: stat**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-stat)
</dt> <dd>

Заполняет элементы структуры [**статпропсетстг**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) , которая содержит данные о свойстве, заданном в целом. При возврате предоставляет указатель на структуру. Для непростых наборов хранения Эта реализация вызывает метод [**IStorage:: stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat) (или [**IStream:: stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat)), чтобы получить время из базового хранилища или потока. Для простых наборов хранения время не поддерживается.

</dd> <dt>

<span id="IPropertyStorage__SetTimes"></span><span id="ipropertystorage__settimes"></span><span id="IPROPERTYSTORAGE__SETTIMES"></span>[**Ипропертистораже:: Сеттимес**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-settimes)
</dt> <dd>

Для непростых наборов свойств задает время, поддерживаемое базовым хранилищем. Реализация хранилища составных файлов поддерживает все три: изменение, доступ и создание. Эта реализация [**сеттимес**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-settimes) вызывает метод [**IStorage:: сетелементтимес**](/windows/desktop/api/Objidl/nf-objidl-istorage-setelementtimes) базового хранилища для получения этих значений.

</dd> </dl>

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**ипропертистораже**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)
</dt> <dt>

[**IStorage:: Сетелементтимес**](/windows/desktop/api/Objidl/nf-objidl-istorage-setelementtimes)
</dt> </dl>

 

 