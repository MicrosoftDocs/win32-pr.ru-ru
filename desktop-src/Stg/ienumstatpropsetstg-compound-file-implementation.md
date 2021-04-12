---
title: Реализация файла IEnumSTATPROPSETSTG-Compound
description: Реализация составного файла интерфейса Иенумстатпропсетстг используется для перечисления массива структур СТАТПРОПСЕТСТГ, содержащих данные статистических свойств.
ms.assetid: 1ce36e40-518c-411b-be5a-835a2dd0995e
keywords:
- Иенумстатпропсетстг Стрктд STG, реализация составного файла
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9566af1a1956b3a951a996b6198f4a3161680042
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337740"
---
# <a name="ienumstatpropsetstg-compound-file-implementation"></a>Реализация файла IEnumSTATPROPSETSTG-Compound

Реализация составного файла интерфейса [**иенумстатпропсетстг**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) используется для перечисления массива структур [**статпропсетстг**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) , содержащих данные статистических свойств. Реализация [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) управляет статистическими данными и связывается с текущим объектом хранилища составных файлов.

## <a name="when-to-use"></a>Назначение

Вызывайте методы [**иенумстатпропсетстг**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) для перечисления структур [**статпропсетстг**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) , каждый из которых предоставляет данные о одном из наборов свойств, связанных с объектом хранилища составного файла.

## <a name="remarks"></a>Комментарии

<dl> <dt>

<span id="IEnumSTATPROPSETSTG__Next"></span><span id="ienumstatpropsetstg__next"></span><span id="IENUMSTATPROPSETSTG__NEXT"></span>[**Иенумстатпропсетстг:: Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)
</dt> <dd>

Возвращает следующую одну или несколько структур [**статпропсетстг**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) (число определяется параметром *celt* ). Элементы **статпропсетстг** , предоставляемые через вызов реализации составного файла [**Иенумстатпропсетстг:: Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) , следуют следующим правилам.

-   Если [**иенумстатпропсетстг:: Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) не может предоставить статпропсетстг. fmtid, то нули записываются в этот элемент. Это происходит, когда набор свойств не имеет предопределенного имени (например, \\ 005SummaryInformation) и не является допустимым значением.
-   Набор свойств Документсуммаринформатион и Пользователяопределенные является специальным, в том, что он может иметь два раздела набора свойств. Этот набор свойств описан в разделе, посвященном [наборам свойств документсуммаринформатион и пользователяопределенные](the-documentsummaryinformation-and-userdefined-property-sets.md). Второй раздел называется User-Defined свойствами. Каждый раздел идентифицируется с помощью уникального идентификатора формата (FMTID). Если для перечисления наборов свойств используется [**IPropertySetStorage:: Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-enum) , набор свойств User-Defined не будет перечислен.

> [!Note]  
> Если вы всегда создаете набор свойств с помощью [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create), а затем, так как для имени хранилища создается "символьный GUID", [**Иенумстатпропсетстг:: Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) вернет ненулевое, допустимое FMTID для свойства Set \[ статпропсетстг. FMTID \] .

 

-   Элемент СТАТПРОПСЕТСТГ. Грффлагс не обязательно отражает, имеет ли свойство значение ANSI. Если \_ задано значение пропсетфлаг ANSI, свойство устанавливается в определенном формате ANSI. Если ПРОПСЕТФЛАГ \_ ANSI является четким, набор свойств может быть либо в Юникоде, либо в формате, отличном от Юникода, так как невозможно определить, является ли он ANSI без открытия.
-   Член СТАТПРОПСЕТСТГ. Грффлагс отражает, является ли набор свойств простым или нет, поэтому параметр \_ непростой флага пропсетфлаг всегда является допустимым.
-   Если [**иенумстатпропсетстг:: Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) не может предоставить статпропсетстг. CLSID, ему присваивается значение все НУЛИ (CLSID \_ null). В реализации составного файла COM это происходит, когда набор свойств является простым ( \_ непростой флаг пропсетфлаг не задан) или является непростым, но CLSID не задан явно. Для непростых наборов свойств полученный CLSID — это тот, который поддерживается базовым [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage).
-   Если [**иенумстатпропсетстг:: Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) не может предоставить поля времени \[ **CTime**, **мтиме**, **времени atime** \] , для каждого неподдерживаемого времени будет установлено нулевое значение. В реализации составного файла COM получение этих значений зависит от их извлечения из базовой реализации [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) .

</dd> <dt>

<span id="IEnumSTATPROPSETSTG__Skip"></span><span id="ienumstatpropsetstg__skip"></span><span id="IENUMSTATPROPSETSTG__SKIP"></span>[**Иенумстатпропсетстг:: Skip**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg)
</dt> <dd>

Пропускает количество элементов, указанное в параметре *celt*. Возвращает значение S \_ ОК, если заданное число элементов пропущено, возвращает S \_ false, если меньше элементов, чем запрошено, пропускаются. В любом другом случае возвращает соответствующую ошибку.

</dd> <dt>

<span id="IEnumSTATPROPSETSTG__Reset"></span><span id="ienumstatpropsetstg__reset"></span><span id="IENUMSTATPROPSETSTG__RESET"></span>[**Иенумстатпропсетстг:: Reset**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg)
</dt> <dd>

Устанавливает курсор в начало перечисления. В случае успеха возвращает S \_ ОК, в противном случае ВОЗВРАЩАЕТ STG \_ E \_ инвалидхандле.

</dd> <dt>

<span id="IEnumSTATPROPSETSTG__Clone"></span><span id="ienumstatpropsetstg__clone"></span><span id="IENUMSTATPROPSETSTG__CLONE"></span>[**Иенумстатпропсетстг:: Clone**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg)
</dt> <dd>

Копирует текущее состояние перечисления этого перечислителя.

</dd> </dl>

 

 