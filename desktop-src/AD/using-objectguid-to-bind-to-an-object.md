---
title: Использование objectGUID для привязки к объекту
description: Различающееся имя объекта изменяется при переименовании или перемещении объекта, поэтому различающееся имя не является надежным идентификатором объекта.
ms.assetid: 6c038005-3ecb-4c00-b1a3-a231d3aea64e
ms.tgt_platform: multiple
keywords:
- Использование objectGUID для привязки к объекту Active Directory
- objectGUID Active Directory
- objectGUID AD, использование для привязки к объекту
- Active Directory, использование, привязка, использование objectGUID для привязки к объекту
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 045c6194cf27b1697cc478b547105fb10335c219
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104069737"
---
# <a name="using-objectguid-to-bind-to-an-object"></a>Использование objectGUID для привязки к объекту

Различающееся имя объекта изменяется при переименовании или перемещении объекта, поэтому различающееся имя не является надежным идентификатором объекта. В домен Active Directory Services свойство **objectGUID** объекта никогда не изменяется, даже если объект переименован или перемещен. Дополнительные сведения об **objectGUID** и идентификаторах см. в разделе [имена объектов и удостоверения](object-names-and-identities.md).

Поставщик Active Directory LDAP предоставляет метод для привязки к объекту с помощью идентификатора GUID объекта. Формат строки привязки выглядит следующим образом:


```C++
LDAP://servername/<GUID=XXXXX>
```



В этом примере «ServerName» — это имя сервера каталогов, а «XXXXX» — строковое представление шестнадцатеричного значения GUID. "Servername" является необязательным. Строка GUID указывается в форме "КСКСКСКСКСКСКСКСКСКСКСКСКСКСКСКСКСКСКСКСКСКСКСКСКСКСКСКСКСКСКСКС". Строка GUID может также иметь форму "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX", которая является той же формой, что и строка, созданная функцией [**StringFromGUID2**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) , без окружающих фигурных скобок " {} ". Дополнительные сведения и пример кода, демонстрирующий создание связываемой строки из GUID, см. в разделе [пример кода для создания связываемого строкового представления GUID](example-code-for-creating-a-bindable-string-representation-of-a-guid.md). Свойство [**iAds. GUID**](/windows/desktop/ADSI/iads-property-methods) можно использовать для получения правильной строки идентификатора GUID.

При привязке с использованием идентификатора GUID объекта некоторые методы и свойства метода [**iAds**](/windows/desktop/api/iads/nn-iads-iads) и [**иадсконтаинер**](/windows/desktop/api/iads/nn-iads-iadscontainer) не поддерживаются. Следующие свойства **iAds** не поддерживаются объектами, полученными при помощи привязки с использованием идентификатора GUID объекта:

-   [**Действитель**](/windows/desktop/ADSI/iads-property-methods)
-   [**Имя**](/windows/desktop/ADSI/iads-property-methods)
-   [**Parent**](/windows/desktop/ADSI/iads-property-methods)

Следующие методы **иадсконтаинер** не поддерживаются объектами, полученными при помощи привязки с использованием идентификатора GUID объекта:

-   [**GetObject**](/windows/desktop/api/iads/nf-iads-iadscontainer-getobject)
-   [**Создать**](/windows/desktop/api/iads/nf-iads-iadscontainer-create)
-   [**Удалить**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete)
-   [**копихере**](/windows/desktop/api/iads/nf-iads-iadscontainer-copyhere)
-   [**мовехере**](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere)

Чтобы использовать эти методы и свойства после привязки к объекту с помощью идентификатора GUID объекта, используйте метод [**iAds. Get**](/windows/desktop/api/iads/nf-iads-iads-get) , чтобы получить различающееся имя объекта, а затем используйте различающееся имя для повторной привязки к объекту.

Если приложение хранит или кэширует идентификаторы или ссылки на объекты, хранящиеся в домен Active Directory Services, идентификатор GUID объекта лучше использовать по нескольким причинам:

-   Свойство **objectGUID** объекта On не изменяется даже при переименовании или перемещении объекта.
-   Можно легко выполнить привязку к объекту с помощью идентификатора GUID объекта.
-   Если объект переименовывается или перемещается, свойство **objectGUID** предоставляет единый идентификатор, который можно использовать для быстрого поиска и идентификации объекта, а не для создания запроса с условиями для всех свойств, которые определяли этот объект.

 

 