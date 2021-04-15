---
title: Сопоставление свойств IADsUser и атрибутов Active Directory
description: Если применимо, свойство объекта пользователя ADSI сопоставляется с соответствующим атрибутом Active Directory. Свойства объекта пользователя ADSI связаны с методами свойства IADsUser.
ms.assetid: 9b568084-5a6b-4a73-be88-9d9cd8007824
ms.tgt_platform: multiple
keywords:
- Сопоставление свойств IADsUser и атрибутов Active Directory ADSI
- ADSI поставщика LDAP, объект User, сопоставление свойств IADsUser и атрибутов Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17b817a8c56e2c74c846e1343e0ed7803427f4a2
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104413729"
---
# <a name="mapping-between-iadsuser-properties-and-active-directory-attributes"></a>Сопоставление свойств IADsUser и атрибутов Active Directory

Если применимо, свойство объекта пользователя ADSI сопоставляется с соответствующим атрибутом Active Directory. Свойства объекта пользователя ADSI связаны с методами свойства [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) .

В следующей таблице приведено сопоставление свойств [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) для поставщика LDAP и соответствующего атрибута Active Directory.



| IADsUser, свойство                                           | Атрибут Active Directory                                                                                  |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**аккаунтдисаблед**](iadsuser-property-methods.md)        | **Реклама \_ Флаг УФ \_ аккаунтдисабле** в атрибуте [**userAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol) .  |
| [**аккаунтекспиратиондате**](iadsuser-property-methods.md)  | [**accountExpires**](/windows/desktop/ADSchema/a-accountexpires)                                                             |
| [**бадлогинаддресс**](iadsuser-property-methods.md)        | Не поддерживается.                                                                                              |
| [**бадлогинкаунт**](iadsuser-property-methods.md)          | [**badPwdCount**](/windows/desktop/ADSchema/a-badpwdcount)                                                                   |
| [**Название**](iadsuser-property-methods.md)             | [**department**](/windows/desktop/ADSchema/a-department)                                                                     |
| [**Описание**](iadsuser-property-methods.md)            | [**nописание**](/windows/desktop/ADSchema/a-description)                                                                   |
| [**Отдел**](iadsuser-property-methods.md)               | [**Категория**](/windows/desktop/ADSchema/a-division)                                                                         |
| [**EmailAddress**](iadsuser-property-methods.md)           | [**mail**](/windows/desktop/ADSchema/a-mail)                                                                                 |
| [**КодСотрудника**](iadsuser-property-methods.md)             | [**КодСотрудника**](/windows/desktop/ADSchema/a-employeeid)                                                                     |
| [**факснумбер**](iadsuser-property-methods.md)              | [**facsimileTelephoneNumber**](/windows/desktop/ADSchema/a-facsimiletelephonenumber)                                         |
| [**FirstName**](iadsuser-property-methods.md)              | [**givenName**](/windows/desktop/ADSchema/a-givenname)                                                                       |
| [**FullName**](iadsuser-property-methods.md)               | [**displayName**](/windows/desktop/ADSchema/a-displayname)                                                                   |
| [**грацелогинсалловед**](iadsuser-property-methods.md)     | Не поддерживается.                                                                                              |
| [**грацелогинсремаининг**](iadsuser-property-methods.md)   | Не поддерживается.                                                                                              |
| [**HomeDirectory**](iadsuser-property-methods.md)          | [**хомедиректори**](/windows/desktop/ADSchema/a-homedirectory)                                                               |
| [**Домашней**](iadsuser-property-methods.md)               | [**вввхомепаже**](/windows/desktop/ADSchema/a-wwwhomepage)                                                                   |
| [**исаккаунтлоккед**](iadsuser-property-methods.md)        | [**lockoutTime**](/windows/desktop/ADSchema/a-lockouttime)                                                                   |
| [**Языки**](iadsuser-property-methods.md)              | Не поддерживается.                                                                                              |
| [**ластфаиледлогин**](iadsuser-property-methods.md)        | [**Аргументы badPasswordTime**](/windows/desktop/ADSchema/a-badpasswordtime)                                                           |
| [**LastLogin**](iadsuser-property-methods.md)              | [**ластлогон**](/windows/desktop/ADSchema/a-lastlogon)                                                                       |
| [**ластлогофф**](iadsuser-property-methods.md)             | [**ластлогофф**](/windows/desktop/ADSchema/a-lastlogoff)                                                                     |
| [**LastName**](iadsuser-property-methods.md)               | [**sn**](/windows/desktop/ADSchema/a-sn)                                                                                     |
| [**логинхаурс**](iadsuser-property-methods.md)             | [**логонхаурс**](/windows/desktop/ADSchema/a-logonhours)                                                                     |
| [**логинскрипт**](iadsuser-property-methods.md)            | [**scriptPath**](/windows/desktop/ADSchema/a-scriptpath)                                                                     |
| [**логинворкстатионс**](iadsuser-property-methods.md)      | [**усерворкстатионс**](/windows/desktop/ADSchema/a-userworkstations)                                                         |
| [**Configuration**](iadsuser-property-methods.md)                | [**Configuration**](/windows/desktop/ADSchema/a-manager)                                                                           |
| [**макслогинс**](iadsuser-property-methods.md)              | Не поддерживается.                                                                                              |
| [**максстораже**](iadsuser-property-methods.md)             | [**максстораже**](/windows/desktop/ADSchema/a-maxstorage)                                                                     |
| [**NamePrefix**](iadsuser-property-methods.md)             | [**персоналтитле**](/windows/desktop/ADSchema/a-personaltitle)                                                               |
| [**NameSuffix**](iadsuser-property-methods.md)             | [**женератионкуалифиер**](/windows/desktop/ADSchema/a-generationqualifier)                                                   |
| [**оффицелокатионс**](iadsuser-property-methods.md)        | [**physicalDeliveryOfficeName**](/windows/desktop/ADSchema/a-physicaldeliveryofficename)                                     |
| [**осернаме**](iadsuser-property-methods.md)              | [**middleName**](/windows/desktop/ADSchema/a-middlename)                                                                     |
| [**пассвордекспиратиондате**](iadsuser-property-methods.md) | Задать с помощью редактора групповая политика                                                                               |
| [**пассвордластчанжед**](iadsuser-property-methods.md)    | [**pwdLastSet**](/windows/desktop/ADSchema/a-pwdlastset)                                                                     |
| [**пассвордминимумленгс**](iadsuser-property-methods.md)  | Задать с помощью редактора групповая политика                                                                               |
| [**пассвордрекуиред**](iadsuser-property-methods.md)       | **Реклама \_ Флаг УФ \_ PASSWD \_ нотрекд** в атрибуте [**userAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol) . |
| [**Picture**](iadsuser-property-methods.md)                | [**thumbnailPhoto;**](/windows/desktop/ADSchema/a-thumbnailphoto)                                                             |
| [**посталаддрессес**](iadsuser-property-methods.md)        | [**посталаддресс**](/windows/desktop/ADSchema/a-postaladdress)                                                               |
| [**посталкодес**](iadsuser-property-methods.md)            | [**postalCode**](/windows/desktop/ADSchema/a-postalcode)                                                                     |
| [**Профиль**](iadsuser-property-methods.md)                | [**Путь к пути**](/windows/desktop/ADSchema/a-profilepath)                                                                   |
| [**рекуиреуникуепассворд**](iadsuser-property-methods.md)  | Задать с помощью редактора групповая политика                                                                               |
| [**SeeAlso**](iadsuser-property-methods.md)                | [**seeAlso**](/windows/desktop/ADSchema/a-seealso)                                                                           |
| [**телефонехоме**](iadsuser-property-methods.md)          | [**homePhone**](/windows/desktop/ADSchema/a-homephone)                                                                       |
| [**телефонемобиле**](iadsuser-property-methods.md)        | [**сети**](/windows/desktop/ADSchema/a-mobile)                                                                             |
| [**TelephoneNumber**](iadsuser-property-methods.md)        | [**TelephoneNumber**](/windows/desktop/ADSchema/a-telephonenumber)                                                           |
| [**телефонепажер**](iadsuser-property-methods.md)         | [**расписан**](/windows/desktop/ADSchema/a-pager)                                                                               |
| [**Заголовок**](iadsuser-property-methods.md)                  | [**Титуль**](/windows/desktop/ADSchema/a-title)                                                                               |



 

 

 