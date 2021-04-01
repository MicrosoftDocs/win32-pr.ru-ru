---
title: Интерфейсы API для работы с дескрипторами безопасности
description: Интерфейсы API для работы с дескрипторами безопасности
ms.assetid: eb5ee183-949c-41f5-9f74-f9c418fdf0a2
ms.tgt_platform: multiple
keywords:
- AD дескрипторов безопасности
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfb798e036d5e30ba58a83499b92340bf30ee3cb
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "103987357"
---
# <a name="apis-for-working-with-security-descriptors"></a>Интерфейсы API для работы с дескрипторами безопасности

Каждый объект в домен Active Directory Services имеет атрибут **нтсекуритидескриптор** , который содержит дескриптор безопасности объекта. Существует два основных способа чтения дескриптора безопасности объекта каталога и управления им:

-   Используйте метод [**iAds:: Get**](/windows/desktop/api/iads/nf-iads-iads-get) , чтобы получить дескриптор безопасности в виде COM-объекта ADSI с интерфейсом [**иадссекуритидескриптор**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) . Интерфейсы **иадссекуритидескриптор**, [**иадсакцессконтроллист**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrollist)и [**иадсакцессконтролентри**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) можно использовать для управления дескриптором безопасности и его компонентами (ACL, ACE и т. д.). Дополнительные сведения и пример кода см. в разделе [Использование функции iAds для получения дескриптора безопасности](using-iads-to-get-a-security-descriptor.md).
-   Используйте метод [**идиректорйобжект:: жетобжектаттрибутес**](/windows/desktop/api/iads/nf-iads-idirectoryobject-getobjectattributes) , чтобы получить дескриптор безопасности объекта в качестве указателя на структуру [**\_ дескриптора безопасности**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) . Используйте этот указатель с функцией управления доступом Win32, такой как [**AccessCheck**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheck) или [**буилдсекуритидескриптор**](/windows/desktop/api/aclapi/nf-aclapi-buildsecuritydescriptora). Дополнительные сведения и пример кода см. в разделе [Использование идиректорйобжект для получения дескриптора безопасности](using-idirectoryobject-to-get-a-security-descriptor.md).

Рекомендуемым методом, который используется большинством примеров кода в этом разделе, является использование интерфейсов **iAds \*** , поскольку они упрощают обработку дескрипторов безопасности, списков управления доступом и ACE. Для Visual Basic программистов интерфейсы **iAds \*** являются наиболее эффективным способом для работы с дескрипторами безопасности.

Метод [**идиректорйобжект**](/windows/desktop/api/iads/nn-iads-idirectoryobject) полезен, если требуется [**Структура \_ дескриптора безопасности**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) . Например, в примере кода для [проверки прав доступа к элементу управления в ACL объекта](checking-a-control-access-right-in-an-objectampaposs-acl.md) этот метод используется для получения дескриптора безопасности, передаваемого функции [**акцессчеккбитипересултлист**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) .

Дополнительные сведения можно найти в разделе

-   [Использование метода IADs для получения дескриптора безопасности](using-iads-to-get-a-security-descriptor.md)
-   [Использование Идиректорйобжект для получения дескриптора безопасности](using-idirectoryobject-to-get-a-security-descriptor.md)
-   [Компоненты дескриптора безопасности](security-descriptor-components.md)
-   [Получение списка DACL объекта](retrieving-an-objectampaposs-dacl.md)
-   [Получение списка SACL объекта](retrieving-an-objectampaposs-sacl.md)
-   [Считывание дескриптора безопасности объекта](reading-an-objectampaposs-security-descriptor.md)
-   [Пример кода для создания дескриптора безопасности](example-code-for-creating-a-security-descriptor.md)
-   [Пример кода для перечисления списка управления доступом объекта в службах домен Active Directory Services](example-code-for-enumerating-the-acl-of-an-active-directory-object.md)

 

 