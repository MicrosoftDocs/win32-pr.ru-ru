---
title: Доступ к данным и управление ими с помощью ADSI
description: Все объекты имеют свойства.
ms.assetid: 366a1fbc-3089-406a-9819-cf2ba7636c5f
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, доступ к данным и управление ими
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03ed09c1717f4f9a9c1c75372e7efdc23d2cce1adb39242197346061ae4df00f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118181634"
---
# <a name="accessing-and-manipulating-data-with-adsi"></a>Доступ к данным и управление ими с помощью ADSI

Все объекты имеют свойства. Все COM-объекты Active Directory интерфейсов служб (ADSI) имеют один или несколько интерфейсов с методами, которые извлекают свойства объекта каталога, представляемого объектом COM. Существует несколько способов чтения свойств объекта.

-   Получить конкретное свойство по имени: интерфейс [**iAds**](/windows/desktop/api/Iads/nn-iads-iads) имеет два метода [**iAds:: Get**](/windows/desktop/api/Iads/nf-iads-iads-get) и [**iAds:: жетекс**](/windows/desktop/api/Iads/nf-iads-iads-getex) для чтения определенного свойства. Каждый COM-объект ADSI имеет интерфейс **iAds** .
-   Получить указанный список свойств: интерфейс [**идиректорйобжект**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) имеет метод [**Идиректорйобжект:: жетобжектаттрибутес**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) , который позволяет указать список, содержащий имена свойств для чтения, и возвращает массив структур, содержащих запрошенные значения свойств.
-   Перечисление всех свойств объекта. интерфейс [**иадспропертилист**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) позволяет перечислить все свойства объекта.
-   Получить специальные свойства: интерфейсы автоматизации ([**iAds**](/windows/desktop/api/Iads/nn-iads-iads) \* ) имеют методы свойств, позволяющие получать специальные свойства, которые не хранятся в объекте. Или методы свойств позволяют получить свойство объекта в формате данных, отличающемся от фактического типа данных. Например, интерфейс **iAds** имеет методы свойств, такие как [**iAds:: Get \_ Name**](iads-property-methods.md), который извлекает относительное различающееся имя объекта (RDN); **IAds:: Get \_ Класс**, который получает класс объекта и параметр **iAds:: Get \_ Parent**, который извлекает путь к родителю объекта.

ADSI позволяет локально кэшировать свойства после их чтения с сервера каталогов. Это позволяет считывать свойства из локального кэша свойств или получать свойства непосредственно с сервера каталогов. В ADSI также есть методы для обновления кэша, а также указано, будут ли кэшироваться все свойства объекта или только указанные.

После получения свойства вы читаете его значение. Тип данных свойства зависит от определения свойства (также известного как атрибут) в схеме Active Directory. Для каждого типа свойства, которое может существовать в Active Directory, существует объект **attributeSchema** в схеме Active Directory. Объект **attributeSchema** определяет характеристики атрибута. Одной из этих характеристик является синтаксис атрибута, который определяет тип данных значений атрибута. Дополнительные сведения см. в разделе [характеристики атрибутов](/windows/desktop/AD/characteristics-of-attributes) и [синтаксиса для Active Directoryных атрибутов](/windows/desktop/AD/syntaxes-for-attributes-in-active-directory-domain-services).

Интерфейсы автоматизации ([**iAds**](/windows/desktop/api/Iads/nn-iads-iads) \* ) возвращают значение свойства как [**вариант**](/windows/win32/api/oaidl/ns-oaidl-variant) или указатель на интерфейс автоматизации для COM-объекта, представляющего свойство. Интерфейсы [**идиректорйобжект**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) и [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) возвращают свойство в виде указателя на структуру, содержащую типизированное значение свойства или указатель на строку байтов. Кроме того, **идиректорйобжект** и **IDirectorySearch** получают свойства непосредственно с сервера каталогов, а не с помощью локального кэша свойств.

В этом разделе описаны следующие темы:

-   [Интерфейсы IADs и Идиректорйобжект](the-iads-and-idirectoryobject-interfaces.md)
-   [Доступ к атрибутам с помощью ADSI](accessing-attributes-with-adsi.md)
-   [Изменение атрибутов с помощью ADSI](modifying-attributes-with-adsi.md)
-   [Доступ к кэшу свойств напрямую с помощью интерфейсов Иадспроперти](accessing-the-property-cache-directly-with-the-iadsproperty-interfaces.md)
-   [Синтаксис атрибутов ADSI](adsi-attribute-syntax.md)

 

 