---
title: Использование доменных служб Active Directory
description: В этом разделе приводятся рекомендации по написанию приложений, использующих или публикующих данные в службе Active Directory Directory.
ms.assetid: 2ae20169-08a5-4e15-8430-ea99a917725f
ms.tgt_platform: multiple
keywords:
- Active Directory Active Directory с помощью
- Службы домен Active Directory Services Active Directory, использование
- Active Directory примеры Active Directory
- Примеры домен Active Directory Services Active Directory
- Примеры Active Directory
- Active Directory Active Directory, примеры см. в статье примеры домен Active Directory служб.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 540b9004311db320decbd15c4f0a29e52ec1302a
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/09/2020
ms.locfileid: "103797059"
---
# <a name="using-active-directory-domain-services"></a>Использование доменных служб Active Directory

В этом разделе приводятся рекомендации по написанию приложений, использующих или публикующих данные в службе Active Directory Directory.

> [!Note]  
> Следующая документация предназначена для компьютерных программистов. Если вы пытаетесь устранить ошибку Active Directory домашней печати, см. [следующие предложения](https://answers.microsoft.com/windows/forum/all/clicking-find-printer-shows-error-the-active/52bfd961-ff62-4397-b8cf-a0708f0cb3d2) на страницах сообщества Майкрософт. Если это не поможет, воспользуйтесь приведенными ниже рекомендациями на [сайте TechNet](https://social.technet.microsoft.com/Forums/windowsserver/d6212275-24d6-4168-830a-9441f861cb76/error-message-when-attempting-to-print-active-directory-domain-service-is-currently-unavailable?forum=winserverprint).

 

Службы домен Active Directory Services совместимы с протоколом упрощенного доступа к каталогу 3,0, который определяется RFC 2251 и другими RFC. Для доступа к домен Active Directory службам можно использовать любой из следующих наборов API. Каждый набор API имеет свои преимущества и недостатки, которые зависят от языка программирования, среды программирования и предполагаемого метода выполнения. Большинство примеров в этом пошаговом руководству используют интерфейсы ADSI, которые поддерживаются такими языками, как C и C++, а также поддерживающими автоматизацией языками, такими как Microsoft Visual Basic и Visual Basic Scripting Edition.

Дополнительные сведения о конкретных технологиях домен Active Directory Services см. в следующих статьях:

-   [протокол LDAP](/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api)
-   [Интерфейсы служб Active Directory](../adsi/active-directory-service-interfaces-adsi.md)
-   [System.DirectoryServices](/dotnet/api/system.directoryservices)

В этом разделе рассматриваются следующие темы:

-   [Привязка к службам домен Active Directory](binding-to-active-directory-domain-services.md)
-   [Поиск в домен Active Directory Services](searching-in-active-directory-domain-services.md)
-   [Создание и удаление объектов в службах домен Active Directory Services](creating-and-deleting-objects-in-active-directory-domain-services.md)
-   [Перемещение объектов](moving-objects.md)
-   [Чтение и запись атрибутов объектов в службах домен Active Directory Services](reading-and-writing-attributes-of-objects-in-active-directory-domain-services.md)
-   [Управление доступом к объектам в службах домен Active Directory Services](controlling-access-to-objects-in-active-directory-domain-services.md)
-   [Расширение схемы](extending-the-schema.md)
-   [Расширение пользовательского интерфейса для объектов каталога](extending-the-user-interface-for-directory-objects.md)
-   [Управление пользователями](managing-users.md)
-   [Управление группами](managing-groups.md)
-   [Отслеживание изменений](tracking-changes.md)
-   [Публикация службы](service-publication.md)
-   [Учетные записи входа в службу](service-logon-accounts.md)
-   [Взаимная проверка подлинности с помощью Kerberos](mutual-authentication-using-kerberos.md)
-   [Резервное копирование и восстановление Active Directory](backing-up-and-restoring-an-active-directory-server.md)
-   [Сохранение платформа динамических данных](storing-dynamic-data.md)
-   [Разделы каталога приложений](application-directory-partitions.md)
-   [Обнаружение режима работы домена](detecting-the-operation-mode-of-a-domain.md)

 

 