---
title: Реализация наборов свойств в COM
description: Реализация наборов свойств в COM
ms.assetid: 52d7b534-f81a-4cc9-b5ea-9538bfff056c
keywords:
- Структурированное хранилище Стрктд STG, using, использование набора свойств в COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb8ee68fcd36958e0b7b0648e40f6e3c480f31d3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987612"
---
# <a name="property-set-implementations-in-com"></a>Реализация наборов свойств в COM

Хотя возможность использования постоянных наборов свойств не была полностью нажата, в настоящее время существует два основных применения:

-   Хранение сводных данных с помощью объекта, например документа
-   Передача данных свойств между объектами

Наборы свойств COM предназначены для хранения данных, которые предназначены для представления в виде коллекции детализированных значений с умеренным размером. Слишком большие наборы данных должны разбиваться на отдельные потоки, хранилища и/или наборы свойств. Формат данных "набор свойств COM" не предназначен для замены базы данных с множеством маленьких объектов.

COM предоставляет реализации интерфейсов набора свойств для различных объектов, а также три вспомогательные функции. В следующем разделе описываются некоторые характеристики производительности этих реализаций. Дополнительные сведения о конкретных интерфейсах и о том, как получить указатель на эти интерфейсы, см. в разделе Справочник по COM:

-   [IPropertySetStorage — реализация составного файла](ipropertysetstorage-compound-file-implementation.md)

    Реализация составного файла, которая предоставляет интерфейсы [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) и [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) , также предоставляет интерфейсы [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) и [**ипропертистораже**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) . Учитывая реализацию составного файла **IStorage**, интерфейс **IPropertySetStorage** можно получить, вызвав [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).

-   [IPropertySetStorage — реализация файловой системы NTFS](ipropertysetstorage-ntfs-file-system-implementation.md)

    Интерфейсы [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) и [**ипропертистораже**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) также можно получить для файлов NTFS, которые не являются составными файлами. Таким образом, эти интерфейсы можно получить для всех файлов на томе NTFS.

-   [IPropertySetStorage — изолированная реализация](ipropertysetstorage-stand-alone-implementation.md)

    При создании этой реализации [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) и [**ипропертистораже**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) ему присваивается указатель на объект, поддерживающий интерфейс [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) . Затем он управляет хранилищами наборов свойств в пределах этого объекта хранилища. Таким же доступом к наборам свойств можно обращаться к любому объекту, который поддерживает.

-   [Рекомендации по реализации IPropertySetStorage](ipropertysetstorage-implementation-considerations.md)

    Существует несколько вопросов, которые следует учитывать при предоставлении реализации интерфейса [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) . Дополнительные *сведения о реализации* см. в разделе Справочник по com.

Кроме того, существует четыре вспомогательные функции, предназначенные для работы со свойствами, считанными из набора свойств в память (в структуру [**пропвариант**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) ):

-   [**пропвариантинит**](/windows/desktop/api/PropIdl/nf-propidl-propvariantinit)
-   [**пропвариантклеар**](/windows/win32/api/combaseapi/nf-combaseapi-propvariantclear)
-   [**фрипропвариантаррай**](/windows/win32/api/combaseapi/nf-combaseapi-freepropvariantarray)
-   [**пропварианткопи**](/windows/win32/api/combaseapi/nf-combaseapi-propvariantcopy)

В следующих разделах более подробно обсуждаются реализации наборов свойств в COM:

-   [Управление наборами свойств](managing-property-sets.md)
-   [Рекомендации по установке свойств](property-set-considerations.md)
-   [Хранение наборов свойств](storing-property-sets.md)
-   [Характеристики производительности](performance-characteristics.md)
-   [Реализация набора свойств сводных данных](implementing-the-summary-information-property-set.md)
-   [Рекомендации по реализации IPropertySetStorage](ipropertysetstorage-implementation-considerations.md)

 

 