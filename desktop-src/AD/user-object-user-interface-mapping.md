---
title: Сопоставление пользовательского интерфейса и объекта-пользователя
description: В следующих таблицах указываются страницы свойств, предоставляемые оснасткой «Active Directory пользователи и компьютеры».
ms.assetid: f309c139-c957-40c4-b369-f527aa87157c
ms.tgt_platform: multiple
keywords:
- Сопоставление пользовательского интерфейса объекта "пользователь"
- Сопоставление пользовательского интерфейса (AD), объект User
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 656e8071b558b730ecb1fc0463834f6fbadb7eb9bf4c56b11640e2b95209735f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024503"
---
# <a name="user-object-user-interface-mapping"></a>Сопоставление пользовательского интерфейса и объекта-пользователя

В следующих таблицах указываются страницы свойств, предоставляемые оснасткой «Active Directory пользователи и компьютеры». Каждая таблица определяет элементы пользовательского интерфейса страницы свойств и атрибут, связанный с этим элементом пользовательского интерфейса. Поскольку страницы свойств, отображаемые оснасткой "пользователи и компьютеры Active Directory", могут быть расширены, невозможно предоставить эти данные для всех страниц, отображаемых на странице свойств.

## <a name="general-property-page"></a>Страница свойств "Общие"

В следующей таблице перечислены метки пользовательского интерфейса на странице свойств **Общие** .



| Метка пользовательского интерфейса         | Атрибут в домен Active Directory Services                           |
|------------------|-------------------------------------------------------------------------|
| Имя       | [**givenName**](/windows/desktop/ADSchema/a-givenname)                                   |
| Фамилия        | [**СН**](/windows/desktop/ADSchema/a-sn)                                                 |
| Инициалы         | [**инициалы**](/windows/desktop/ADSchema/a-initials)                                     |
| Отображаемое имя     | [**displayName**](/windows/desktop/ADSchema/a-displayname)                               |
| Описание      | [**nописание**](/windows/desktop/ADSchema/a-description)                               |
| Office           | [**physicalDeliveryOfficeName**](/windows/desktop/ADSchema/a-physicaldeliveryofficename) |
| Номер телефона | [**TelephoneNumber**](/windows/desktop/ADSchema/a-telephonenumber)                       |
| Телефон: другие | [**otherTelephone**](/windows/desktop/ADSchema/a-othertelephone)                         |
| E-Mail           | [**Адреса электронной почты**](/windows/desktop/ADSchema/a-mail)                                 |
| Веб-страница         | [**wWWHomePage**](/windows/desktop/ADSchema/a-wwwhomepage)                               |
| Веб-страница: другие  | [**URL-адрес**](/windows/desktop/ADSchema/a-url)                                               |



 

## <a name="account-property-page"></a>Страница свойств учетной записи

В следующей таблице перечислены метки пользовательского интерфейса на странице свойств **учетной записи** .



| Метка пользовательского интерфейса                                | Атрибут в домен Active Directory Services                                                   | Комментировать                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------------------------------|-------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Имя Усерлогон                          | [**userPrincipalName**](/windows/desktop/ADSchema/a-userprincipalname)                                           | Это поле берется из всех элементов атрибута [**userPrincipalName**](/windows/desktop/ADSchema/a-userprincipalname) , предшествующих последнему символу "@". Последний символ "@" и все после него помещаются в поле со списком суффиксов.                                                                                                                                                      |
| имя входа пользователя (до Windows 2000)      | [**sAMAccountname**](/windows/desktop/ADSchema/a-samaccountname)                                                 | Без комментариев.                                                                                                                                                                                                                                                                                                                                                                             |
| Время входа                             | [**логонхаурс**](/windows/desktop/ADSchema/a-logonhours)                                                         | Без комментариев.                                                                                                                                                                                                                                                                                                                                                                             |
| Вход в                               | [**логонворкстатион**](/windows/desktop/ADSchema/a-logonworkstation)                                             | Без комментариев.                                                                                                                                                                                                                                                                                                                                                                             |
| Учетная запись заблокирована                   | [**lockoutTime**](/windows/desktop/ADSchema/a-lockouttime) и [ **локкаутдуратион**](/windows/desktop/ADSchema/a-lockoutduration) | Если атрибут [**lockoutTime**](/windows/desktop/ADSchema/a-lockouttime) не равен нулю, атрибут [**локкаутдуратион**](/windows/desktop/ADSchema/a-lockoutduration) добавляется в **lockoutTime** и сравнивается с текущей датой и временем, чтобы определить, заблокирована ли учетная запись.                                                                                                                                |
| Требовать смену пароля при следующем входе в систему | [**pwdLastSet**](/windows/desktop/ADSchema/a-pwdlastset)                                                         | Без комментариев.                                                                                                                                                                                                                                                                                                                                                                             |
| Запретить смену пароля пользователем             | н/д                                                                                             | Это элемент управления "изменение пароля" в списке управления доступом.                                                                                                                                                                                                                                                                                                                                         |
| Другие параметры учетной записи                   | [**userAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol)                                         | Оставшиеся элементы в параметрах учетной записи переключают биты в битовой маске атрибута [**userAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol) (флаги в DWORD).                                                                                                                                                                                                                                 |
| Срок действия учетной записи истекает                         | [**accountExpires**](/windows/desktop/ADSchema/a-accountexpires)                                                 | Элемент Управление **сроком действия учетной записи** отображает дату истечения срока действия учетной записи в конце. Атрибут [**accountExpires**](/windows/desktop/ADSchema/a-accountexpires) хранится как дата истечения срока действия учетной записи. По этой причине Дата, отображаемая в элементе управления **срок действия учетной записи** , будет отображаться как один день раньше даты, содержащейся в атрибуте **accountExpires** . |



 

## <a name="address-property-page"></a>Страница свойств Address

В следующей таблице перечислены метки пользовательского интерфейса на странице свойств **адреса** .



| Метка пользовательского интерфейса        | Атрибут в домен Active Directory Services                                                 | Комментировать                                                   |
|-----------------|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| Улица          | [**streetAddress**](/windows/desktop/ADSchema/a-streetaddress)                                                 | Без комментариев.                                               |
| P. O. Box         | [**postOfficeBox**](/windows/desktop/ADSchema/a-postofficebox)                                                 | Без комментариев.                                               |
| City            | [**н**](/windows/desktop/ADSchema/a-l)                                                                         | Имя атрибута **l** — это строчная буква "l", как в языковом стандарте. |
| Область, республика, край, округ  | [**день**](/windows/desktop/ADSchema/a-st)                                                                       | Без комментариев.                                               |
| Почтовый индекс | [**postalCode**](/windows/desktop/ADSchema/a-postalcode)                                                       | Без комментариев.                                               |
| Страна или регион  | [**c**](/windows/desktop/ADSchema/a-c), [**Co**](/windows/desktop/ADSchema/a-co)и [**каунтрикоде**](/windows/desktop/ADSchema/a-countrycode) | Без комментариев.                                               |



 

## <a name="member-of-property-page"></a>Член страницы свойств

В следующей таблице перечислены метки пользовательского интерфейса для **элемента** страницы свойств.



| Метка пользовательского интерфейса          | Атрибут в домен Active Directory Services   | Комментировать                                                                                                                                                                    |
|-------------------|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Член групп         | [**Групп**](/windows/desktop/ADSchema/a-memberof)             | Включает все группы в списке пользовательского интерфейса, кроме первичной группы, представленной в AD с помощью атрибута [**примариграупид**](/windows/desktop/ADSchema/a-primarygroupid) . |
| Задать основную группу | [**примариграупид**](/windows/desktop/ADSchema/a-primarygroupid) | LDAP: связан с [**примариграуптокен**](/windows/desktop/ADSchema/a-primarygrouptoken) из основной группы.                                                                                  |



 

## <a name="organization-property-page"></a>Страница свойств Организации

В следующей таблице показаны метки пользовательского интерфейса на странице свойств **Организации** .



| Метка пользовательского интерфейса       | Атрибут в домен Active Directory Services | Комментировать     |
|----------------|-----------------------------------------------|-------------|
| Название          | [**Титуль**](/windows/desktop/ADSchema/a-title)                 | Без комментариев. |
| Отдел     | [**Название**](/windows/desktop/ADSchema/a-department)       | Без комментариев. |
| Company        | [**во**](/windows/desktop/ADSchema/a-company)             | Без комментариев. |
| Руководитель: имя   | [**Configuration**](/windows/desktop/ADSchema/a-manager)             | Без комментариев. |
| Прямые отчеты | [**directReports**](/windows/desktop/ADSchema/a-directreports) | Без комментариев. |



 

## <a name="profile-property-page"></a>Страница свойств профиля

В следующей таблице перечислены метки пользовательского интерфейса на странице свойств **профиля** .



| Метка пользовательского интерфейса                | Атрибут в домен Active Directory Services | Комментировать                                                                                                                 |
|-------------------------|-----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Путь к профилю            | [**Путь к пути**](/windows/desktop/ADSchema/a-profilepath)     | Без комментариев.                                                                                                             |
| Сценарий входа            | [**scriptPath**](/windows/desktop/ADSchema/a-scriptpath)       | Без комментариев.                                                                                                             |
| Домашняя папка: локальный путь | [**хомедиректори**](/windows/desktop/ADSchema/a-homedirectory) | Если выбран **локальный путь** , локальный путь хранится в атрибуте [**хомедиректори**](/windows/desktop/ADSchema/a-homedirectory) . |
| домашняя папка: Подключение    | [**хомедриве**](/windows/desktop/ADSchema/a-homedrive)         | если выбран параметр **Подключение** , сопоставленный диск хранится в атрибуте [**хомедриве**](/windows/desktop/ADSchema/a-homedrive) .          |
| Домашняя папка: до         | [**хомедиректори**](/windows/desktop/ADSchema/a-homedirectory) | если выбран параметр **Подключение** , путь хранится в атрибуте [**хомедиректори**](/windows/desktop/ADSchema/a-homedirectory) .          |



 

## <a name="telephones-property-page"></a>Страница свойств телефона для телефонов

В следующей таблице перечислены элементы пользовательского интерфейса страницы свойств « **телефоны** » и соответствующие атрибуты Active Directory.



| Метка пользовательского интерфейса        | Атрибут в домен Active Directory Services                                 |
|-----------------|-------------------------------------------------------------------------------|
| Главная            | [**homePhone**](/windows/desktop/ADSchema/a-homephone)                                         |
| Главная: другие     | [**otherHomePhone**](/windows/desktop/ADSchema/a-otherhomephone)                               |
| Пейджер           | [**расписан**](/windows/desktop/ADSchema/a-pager)                                                 |
| Пейджер: другие    | [**otherPager**](/windows/desktop/ADSchema/a-otherpager)                                       |
| Мобильные службы          | [**сети**](/windows/desktop/ADSchema/a-mobile)                                               |
| Мобильные: другие   | [**otherMobile**](/windows/desktop/ADSchema/a-othermobile)                                     |
| Факс             | [**факсимилетелефоненумбер**](/windows/desktop/ADSchema/a-facsimiletelephonenumber)           |
| Факс: другие      | [**осерфаксимилетелефоненумбер**](/windows/desktop/ADSchema/a-otherfacsimiletelephonenumber) |
| IP-телефон        | [**ipPhone**](/windows/desktop/ADSchema/a-ipphone)                                             |
| IP-телефон: другой | [**otherIpPhone**](/windows/desktop/ADSchema/a-otheripphone)                                   |
| Примечания           | [**контактные**](/windows/desktop/ADSchema/a-info)                                                   |



 

## <a name="environment-sessions-remote-control-and-terminal-services-profile-property-pages"></a>Страницы свойств "среда", "сеансы", "удаленное управление" и "Профиль служб терминалов"

Страницы " **Среда**", " **сеансы**", " **Удаленное управление**" и " **Профиль служб терминалов** " предоставляются для объекта пользователя, поддерживающего службы терминалов. Элементы пользовательского интерфейса для этих страниц не соответствуют отдельным атрибутам. Вместо этого параметры хранятся в личных данных в службах домен Active Directory. Доступ к параметрам служб терминалов можно получить с помощью интерфейса [**иадстсусерекс**](/windows/desktop/api/tsuserex/nn-tsuserex-iadstsuserex) .

 

 