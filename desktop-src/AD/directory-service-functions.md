---
title: Функции службы каталогов (AD DS)
description: Функции службы каталогов предоставляют служебную программу для поиска контроллера домена в домене Windows NT или Windows 2000.
ms.assetid: 7b519c81-5a6c-470a-a525-1894efd53305
ms.tgt_platform: multiple
keywords:
- Функции службы каталогов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75b071128806926e07cf61d62e53b823d8e7e1ac
ms.sourcegitcommit: 8ea1a82717bd3dbb3457be0697329aa37fb13f08
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2019
ms.locfileid: "104069459"
---
# <a name="directory-service-functions-ad-ds"></a>Функции службы каталогов (AD DS)

Функции службы каталогов предоставляют служебную программу для поиска контроллера домена в домене Windows NT или Windows 2000. Архитектура взаимодействует с клиентами, а также с серверами во всех версиях Windows NT и Windows 2000. Следующие функции позволяют разработчикам работать с контроллером домена и членством в домене в службе каталогов:

-   [**дсаддресстоситенамес**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsaddresstositenamesa)
-   [**дсаддресстоситенамесекс**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsaddresstositenamesexa)
-   [**дсдерегистердншострекордс**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsderegisterdnshostrecordsa)
-   [**дсенумератедомаинтрустс**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsenumeratedomaintrustsa)
-   [**дсжетдкклосе**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew)
-   [**Процедуру**](/windows/desktop/api/DsGetDC/nf-dsgetdc-dsgetdcnamea)
-   [**дсжетдкнекст**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta)
-   [**дсжетдкопен**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena)
-   [**дсжетдкситековераже**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcsitecoveragea)
-   [**дсжетфоресттрустинформатионв**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetforesttrustinformationw)
-   [**дсжетситенаме**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetsitenamea)
-   [**дсмержефоресттрустинформатионв**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsmergeforesttrustinformationw)
-   [**дсролефримемори**](/windows/desktop/api/Dsrole/nf-dsrole-dsrolefreememory)
-   [**дсролежетпримаридомаининформатион**](/windows/desktop/api/Dsrole/nf-dsrole-dsrolegetprimarydomaininformation)
-   [**дсвалидатесубнетнаме**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsvalidatesubnetnamea)

Указатель контроллера домена ( [**DsGetDcName**](/windows/desktop/api/DsGetDC/nf-dsgetdc-dsgetdcnamea)) реализуется службой Netlogon. Каждый контроллер домена регистрирует свое имя DNS на DNS-сервере и его NetBIOS-имя с помощью механизма, зависящего от транспорта, например, в службе WINS. Локатор контроллера домена находит имя, затем отправляет датаграмму или проверку связи с контроллером домена, который зарегистрировал имя. Для NetBIOS-имен доменов датаграмма является сообщением в слоте. Для доменных имен DNS датаграмма — это поиск по протоколу LDAP. Каждый такой контроллер отвечает, указывая, что в настоящее время работает. Первый отвечающий контроллер домена возвращается вызывающему объекту.

Возвращенный контроллер домена кэшируется, поэтому последующим вызывающим объектам не нужно повторять предыдущий алгоритм и, чтобы все вызывающие объекты использовали тот же контроллер домена. Это гарантирует, что один клиент будет иметь единообразное представление содержимого контроллера домена.

При поиске контроллера домена по доменному имени DNS локатор контроллера домена пытается найти контроллер домена на "ближайшем" сайте. Каждый контроллер домена регистрирует дополнительные записи DNS, указывающие, какой сайт входит в состав контроллера домена и какие сайты он включает. Локатор контроллера домена сначала ищет эту запись DNS для конкретного сайта перед поиском записи DNS, не относящейся к конкретному сайту, тем самым предоставляя контроллер домена на этом сайте. Когда локатор контроллера домена отправляет датаграмму на контроллер домена, контроллер домена ищет IP-адрес клиента в контейнере Configuration/Sites/Subnet в DS для поиска объекта подсети. Свойство **ситеобжект** объекта Subnet определяет имя сайта, содержащего клиент. Контроллер домена отвечает на запрос проверки связи с именем сайта, содержащего клиент, а также указывает, охватывает ли контроллер домена этот сайт. Если контроллер домена не включает этот сайт и локатор контроллеров домена еще не пытался найти контроллер домена на этом сайте, локатор контроллера домена пытается выполнить поиск контроллера домена на сайте.

Чтобы найти имя сайта, содержащего клиент, используйте функцию [**дсжетситенаме**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetsitenamea) . Имена объектов в контейнере Configuration/Sites/Subnet должны быть допустимыми именами подсетей. Функция [**дсвалидатесубнетнаме**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsvalidatesubnetnamea) указывает, является ли указанное имя подсети допустимым.

 

 




