---
title: Класс Organizational-Person
description: Этот класс используется для объектов, содержащих организационную информацию о пользователе, например номер сотрудника, отдел, руководителя, название, адрес офиса и т. д.
ms.assetid: dbcecb0d-e7ab-4005-82ad-5ffe9b06a380
ms.tgt_platform: multiple
keywords:
- Схема AD Organizational-Person класса
- Схема AD класса Организатионалперсон
topic_type:
- apiref
api_name:
- Organizational-Person
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba9be35cfca3d08336c8b75bcb9a7f21fc2139e835fc6b74686e7f1e0a8a4202
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753204"
---
# <a name="organizational-person-class"></a>Класс Organizational-Person

Этот класс используется для объектов, содержащих организационную информацию о пользователе, например номер сотрудника, отдел, руководителя, название, адрес офиса и т. д.



| Ввод | Значение |
|-------------------|--------------------------------------|
| CN                | Organizational-Person                |
| LDAP-отображаемое имя | организатионалперсон                 |
| Привилегия обновления  | Кто угодно может обновить этот объект.       |
| Частота обновления  | \-                                   |
| Schema-ID-GUID    | bf967aa4-0de6-11d0-a285-00aa003049e2 |



## <a name="implementations"></a>Варианты реализации решения

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server

-   [Атрибуты](#windows-2000-server-attributes)



| Ввод | Значение |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Нет                                                                                        |
| Object-Category             | 2                                                                                            |
| По умолчанию — объект — Категория     | [**Человек**](c-person.md)<br/>                                                        |
| Governs-Id                  | 2.5.6.7                                                                                      |
| По умолчанию-скрытие значения        | 0                                                                                            |
| RDN-Атри-ID                  | [**Common-Name**](a-cn.md)<br/>                                                       |
| Подкласс                 | [**Человек**](c-person.md)<br/>                                                        |
| Возможные старшие          | [**Контейнер**](c-container.md)                                                             |
| Вспомогательные классы           | \-                                                                                           |
| NT-Security-дескриптор      | О:БАГ: BAD: S:                                                                                 |
| Дескриптор безопасности по умолчанию | D: (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;;D А) (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;; SY) (A;; РПЛКЛОРК;;; СЛУЖБЫ |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-2000-server-attributes"></a>атрибуты сервера Windows 2000

этот класс содержит следующие атрибуты для сервера Windows 2000:



| attribute                                                                 | Обязательный | Унаследован от                                                          |
|---------------------------------------------------------------------------|-----------|-----------------------------------------------------------------------|
| [**Адрес**](a-streetaddress.md)                                        | Нет     | **Organizational-Person**                                             |
| [**Адрес — Домашняя страница**](a-homepostaladdress.md)                               | Нет     | **Organizational-Person**                                             |
| [**Описание администратора**](a-admindescription.md)                           | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Имя администратора-отображение**](a-admindisplayname.md)                          | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Allowed-Attributes**](a-allowedattributes.md)                         | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Allowed-Attributes-эффективен**](a-allowedattributeseffective.md)      | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Allowed-Child-classes**](a-allowedchildclasses.md)                    | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Allowed-Child-classes-эффективен**](a-allowedchildclasseseffective.md) | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Средство**](a-assistant.md)                                          | Нет     | **Organizational-Person**                                             |
| [**Плацдарм-Server-List-BL**](a-bridgeheadserverlistbl.md)             | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Каноническое имя**](a-canonicalname.md)                                 | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Common-Name**](a-cn.md)                                               | Верно      | [**Человек**](c-person.md)<br/> [**Вверх**](c-top.md)<br/> |
| [**Company**](a-company.md)                                              | Нет     | **Organizational-Person**                                             |
| [**Код страны**](a-countrycode.md)                                     | Нет     | **Organizational-Person**                                             |
| [**Название страны**](a-c.md)                                               | Нет     | **Organizational-Person**                                             |
| [**Метка времени создания**](a-createtimestamp.md)                            | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Отдел**](a-department.md)                                        | Нет     | **Organizational-Person**                                             |
| [**Описание**](a-description.md)                                      | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Целевой индикатор**](a-destinationindicator.md)                   | Нет     | **Organizational-Person**                                             |
| [**Отображаемое имя**](a-displayname.md)                                     | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Отображаемое имя — печатаемое**](a-displaynameprintable.md)                  | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Отдел**](a-division.md)                                            | Нет     | **Organizational-Person**                                             |
| [**DSA-Signature**](a-dsasignature.md)                                   | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**DS-Core-распространение-данные**](a-dscorepropagationdata.md)               | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Адреса электронной почты**](a-mail.md)                                        | Нет     | **Organizational-Person**                                             |
| [**Идентификатор сотрудника**](a-employeeid.md)                                       | Нет     | **Organizational-Person**                                             |
| [**Имя расширения**](a-extensionname.md)                                 | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Факс-телефон — номер**](a-facsimiletelephonenumber.md)          | Нет     | **Organizational-Person**                                             |
| [**Метки**](a-flags.md)                                                  | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Из записи**](a-fromentry.md)                                         | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)             | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                 | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Квалификатор поколения**](a-generationqualifier.md)                     | Нет     | **Organizational-Person**                                             |
| [**Заданное имя**](a-givenname.md)                                         | Нет     | **Organizational-Person**                                             |
| [**Инициалы**](a-initials.md)                                            | Нет     | **Organizational-Person**                                             |
| [**Тип экземпляра**](a-instancetype.md)                                   | Верно      | [**Вверх**](c-top.md)<br/>                                       |
| [**Международный-ISDN-номер**](a-internationalisdnnumber.md)            | Нет     | **Organizational-Person**                                             |
| [**Является критически важным — системный объект**](a-iscriticalsystemobject.md)             | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Удалено**](a-isdeleted.md)                                         | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Входит в состав списка рассылки**](a-memberof.md)                                     | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Имеет права владельца**](a-isprivilegeholder.md)                        | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Последний-известный-родительский**](a-lastknownparent.md)                            | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Локальное имя**](a-l.md)                                              | Нет     | **Organizational-Person**                                             |
| [**Эмблема**](a-thumbnaillogo.md)                                           | Нет     | **Organizational-Person**                                             |
| [**Управляемые объекты**](a-managedobjects.md)                               | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Manager**](a-manager.md)                                              | Нет     | **Organizational-Person**                                             |
| [**В основном**](a-masteredby.md)                                       | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**МХС-или-Address**](a-mhsoraddress.md)                                  | Нет     | **Organizational-Person**                                             |
| [**Метка времени изменения**](a-modifytimestamp.md)                            | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-целостность-дочерняя — количество**](a-ms-ds-consistencychildcount.md)    | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-Consistencу-Guid**](a-ms-ds-consistencyguid.md)                 | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**нетбут-SCP-BL**](a-netbootscpbl.md)                                  | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Не-Security-Member-BL**](a-nonsecuritymemberbl.md)                   | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**NT-Security-дескриптор**](a-ntsecuritydescriptor.md)                  | Верно      | [**Вверх**](c-top.md)<br/>                                       |
| [**Obj-расп-имя**](a-distinguishedname.md)                              | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Объект — Категория**](a-objectcategory.md)                               | Верно      | [**Вверх**](c-top.md)<br/>                                       |
| [**Объектный класс**](a-objectclass.md)                                     | Верно      | [**Вверх**](c-top.md)<br/>                                       |
| [**Объект — GUID**](a-objectguid.md)                                       | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Версия объекта**](a-objectversion.md)                                 | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Организация — имя подразделения**](a-ou.md)                                  | Нет     | **Organizational-Person**                                             |
| [**Название организации**](a-o.md)                                          | Нет     | **Organizational-Person**                                             |
| [**Другие — почтовый ящик**](a-othermailbox.md)                                   | Нет     | **Organizational-Person**                                             |
| [**Другое имя**](a-middlename.md)                                        | Нет     | **Organizational-Person**                                             |
| [**Другие хорошо известные объекты**](a-otherwellknownobjects.md)               | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Разделяемый атрибут-удаление-список**](a-partialattributedeletionlist.md) | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Разделяемый атрибут-set**](a-partialattributeset.md)                    | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Личный заголовок**](a-personaltitle.md)                                 | Нет     | **Organizational-Person**                                             |
| [**Телефон-Fax — другие**](a-otherfacsimiletelephonenumber.md)                | Нет     | **Organizational-Person**                                             |
| [**Телефон-Home — другие**](a-otherhomephone.md)                              | Нет     | **Organizational-Person**                                             |
| [**Телефон-Home — основной**](a-homephone.md)                                 | Нет     | **Organizational-Person**                                             |
| [**Телефон-Ip — другие**](a-otheripphone.md)                                  | Нет     | **Organizational-Person**                                             |
| [**Телефон-Ip-Primary**](a-ipphone.md)                                     | Нет     | **Organizational-Person**                                             |
| [**Телефон-ISDN-Primary**](a-primaryinternationalisdnnumber.md)            | Нет     | **Organizational-Person**                                             |
| [**Телефон-Mobile — другие**](a-othermobile.md)                               | Нет     | **Organizational-Person**                                             |
| [**Телефон — Mobile — Primary**](a-mobile.md)                                  | Нет     | **Organizational-Person**                                             |
| [**Телефон-Office-Other**](a-othertelephone.md)                            | Нет     | **Organizational-Person**                                             |
| [**Телефон-пейджер — другие**](a-otherpager.md)                                 | Нет     | **Organizational-Person**                                             |
| [**Телефон-пейджер-основной**](a-pager.md)                                    | Нет     | **Organizational-Person**                                             |
| [**физическая доставка — Office-имя**](a-physicaldeliveryofficename.md)     | Нет     | **Organizational-Person**                                             |
| [**Снимки**](a-thumbnailphoto.md)                                       | Нет     | **Organizational-Person**                                             |
| [**Возможно — подстрочные**](a-possibleinferiors.md)                         | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Почтовый адрес**](a-postaladdress.md)                                 | Нет     | **Organizational-Person**                                             |
| [**Почтовый код**](a-postalcode.md)                                       | Нет     | **Organizational-Person**                                             |
| [**флажок после Office**](a-postofficebox.md)                                | Нет     | **Organizational-Person**                                             |
| [**Предпочтительный метод доставки**](a-preferreddeliverymethod.md)            | Нет     | **Organizational-Person**                                             |
| [**Прокси-объект-имя**](a-proxiedobjectname.md)                        | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Прокси-адреса**](a-proxyaddresses.md)                               | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Запрос — политика — BL**](a-querypolicybl.md)                                | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**RDN**](a-name.md)                                                     | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Зарегистрированный адрес**](a-registeredaddress.md)                         | Нет     | **Organizational-Person**                                             |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                 | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**REPL-Уптодате-Vector**](a-repluptodatevector.md)                      | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Отчеты**](a-directreports.md)                                        | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Представители — от**](a-repsfrom.md)                                           | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Представители — кому**](a-repsto.md)                                               | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Редакции**](a-revision.md)                                            | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**SD-Rights-эффективен**](a-sdrightseffective.md)                        | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**См. также**](a-seealso.md)                                             | Нет     | [**Человек**](c-person.md)<br/>                                 |
| [**Server-Reference-BL**](a-serverreferencebl.md)                        | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**"Показать" — "Расширенный просмотр"**](a-showinadvancedviewonly.md)            | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Site-Object-BL**](a-siteobjectbl.md)                                  | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**State-или-провинция-Name**](a-st.md)                                    | Нет     | **Organizational-Person**                                             |
| [**Улица-адрес**](a-street.md)                                        | Нет     | **Organizational-Person**                                             |
| [**Подразделы-ReFS**](a-subrefs.md)                                             | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**субсчемасубентри**](a-subschemasubentry.md)                          | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Образование**](a-sn.md)                                                   | Нет     | [**Человек**](c-person.md)<br/>                                 |
| [**Системные флаги**](a-systemflags.md)                                     | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Номер телефона**](a-telephonenumber.md)                             | Нет     | [**Человек**](c-person.md)<br/>                                 |
| [**Teletex — идентификатор терминала**](a-teletexterminalidentifier.md)        | Нет     | **Organizational-Person**                                             |
| [**Номер телекса**](a-telexnumber.md)                                     | Нет     | **Organizational-Person**                                             |
| [**Номер телекса (первичный)**](a-primarytelexnumber.md)                             | Нет     | **Organizational-Person**                                             |
| [**Текст — страна**](a-co.md)                                              | Нет     | **Organizational-Person**                                             |
| [**Название**](a-title.md)                                                  | Нет     | **Organizational-Person**                                             |
| [**Комментарий пользователя**](a-comment.md)                                         | Нет     | **Organizational-Person**                                             |
| [**Пароль пользователя**](a-userpassword.md)                                   | Нет     | [**Человек**](c-person.md)<br/>                                 |
| [**USN-изменено**](a-usnchanged.md)                                       | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Созданный USN**](a-usncreated.md)                                       | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**USN-DSA-Last-obj-removed**](a-usndsalastobjremoved.md)                | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**USN — межсайтовая**](a-usnintersite.md)                                   | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                               | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Источник USN**](a-usnsource.md)                                         | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**WBEM — путь**](a-wbempath.md)                                           | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Хорошо известные объекты**](a-wellknownobjects.md)                          | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**При изменении**](a-whenchanged.md)                                     | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**При создании**](a-whencreated.md)                                     | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**WWW — Главная страница**](a-wwwhomepage.md)                                    | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**WWW-Page — другие**](a-url.md)                                           | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**X121 — адрес**](a-x121address.md)                                     | Нет     | **Organizational-Person**                                             |



## <a name="windows-server-2003"></a>Windows Server 2003

-   [Атрибуты](#windows-server-2003-attributes)



| Ввод | Значение |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Нет                                                                                                                     |
| Object-Category             | 0                                                                                                                         |
| По умолчанию — объект — Категория     | [**Человек**](c-person.md)<br/>                                                                                     |
| Governs-Id                  | 2.5.6.7                                                                                                                   |
| По умолчанию-скрытие значения        | 1                                                                                                                         |
| RDN-Атри-ID                  | [**Common-Name**](a-cn.md)<br/>                                                                                    |
| Подкласс                 | [**Человек**](c-person.md)<br/>                                                                                     |
| Возможные старшие          | [](c-container.md)[](c-organization.md)[**Организационная единица**](c-organizationalunit.md) Организации контейнера |
| Вспомогательные классы           | \-                                                                                                                        |
| NT-Security-дескриптор      | О:БАГ: BAD: S:                                                                                                              |
| Дескриптор безопасности по умолчанию | D: (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;;D А) (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;; SY) (A;; РПЛКЛОРК;;; СЛУЖБЫ                              |
| System-Flags                | 0x00000010                                                                                                                |



## <a name="windows-server-2003-attributes"></a>Windows Атрибуты сервера 2003

этот класс содержит следующие атрибуты для Windows Server 2003:



| attribute                                                                   | Обязательный | Унаследован от                                                          |
|-----------------------------------------------------------------------------|-----------|-----------------------------------------------------------------------|
| [**Адрес**](a-streetaddress.md)                                          | Нет     | **Organizational-Person**                                             |
| [**Адрес — Домашняя страница**](a-homepostaladdress.md)                                 | Нет     | **Organizational-Person**                                             |
| [**Описание администратора**](a-admindescription.md)                             | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Имя администратора-отображение**](a-admindisplayname.md)                            | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Allowed-Attributes**](a-allowedattributes.md)                           | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Allowed-Attributes-эффективен**](a-allowedattributeseffective.md)        | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Allowed-Child-classes**](a-allowedchildclasses.md)                      | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Allowed-Child-classes-эффективен**](a-allowedchildclasseseffective.md)   | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Средство**](a-assistant.md)                                            | Нет     | **Organizational-Person**                                             |
| [**аттрибутецертификатеаттрибуте**](a-attributecertificateattribute.md)    | Нет     | [**Человек**](c-person.md)<br/>                                 |
| [**Плацдарм-Server-List-BL**](a-bridgeheadserverlistbl.md)               | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Каноническое имя**](a-canonicalname.md)                                   | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Common-Name**](a-cn.md)                                                 | Верно      | [**Человек**](c-person.md)<br/> [**Вверх**](c-top.md)<br/> |
| [**Company**](a-company.md)                                                | Нет     | **Organizational-Person**                                             |
| [**Код страны**](a-countrycode.md)                                       | Нет     | **Organizational-Person**                                             |
| [**Название страны**](a-c.md)                                                 | Нет     | **Organizational-Person**                                             |
| [**Метка времени создания**](a-createtimestamp.md)                              | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Отдел**](a-department.md)                                          | Нет     | **Organizational-Person**                                             |
| [**Описание**](a-description.md)                                        | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Целевой индикатор**](a-destinationindicator.md)                     | Нет     | **Organizational-Person**                                             |
| [**Отображаемое имя**](a-displayname.md)                                       | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Отображаемое имя — печатаемое**](a-displaynameprintable.md)                    | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Отдел**](a-division.md)                                              | Нет     | **Organizational-Person**                                             |
| [**DSA-Signature**](a-dsasignature.md)                                     | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**DS-Core-распространение-данные**](a-dscorepropagationdata.md)                 | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Адреса электронной почты**](a-mail.md)                                          | Нет     | **Organizational-Person**                                             |
| [**Идентификатор сотрудника**](a-employeeid.md)                                         | Нет     | **Organizational-Person**                                             |
| [**Имя расширения**](a-extensionname.md)                                   | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Факс-телефон — номер**](a-facsimiletelephonenumber.md)            | Нет     | **Organizational-Person**                                             |
| [**Метки**](a-flags.md)                                                    | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Из записи**](a-fromentry.md)                                           | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Квалификатор поколения**](a-generationqualifier.md)                       | Нет     | **Organizational-Person**                                             |
| [**Заданное имя**](a-givenname.md)                                           | Нет     | **Organizational-Person**                                             |
| [**хаусеидентифиер**](a-houseidentifier.md)                                | Нет     | **Organizational-Person**                                             |
| [**Инициалы**](a-initials.md)                                              | Нет     | **Organizational-Person**                                             |
| [**Тип экземпляра**](a-instancetype.md)                                     | Верно      | [**Вверх**](c-top.md)<br/>                                       |
| [**Международный-ISDN-номер**](a-internationalisdnnumber.md)              | Нет     | **Organizational-Person**                                             |
| [**Является критически важным — системный объект**](a-iscriticalsystemobject.md)               | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Удалено**](a-isdeleted.md)                                           | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Входит в состав списка рассылки**](a-memberof.md)                                       | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Имеет права владельца**](a-isprivilegeholder.md)                          | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Последний-известный-родительский**](a-lastknownparent.md)                              | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Локальное имя**](a-l.md)                                                | Нет     | **Organizational-Person**                                             |
| [**Эмблема**](a-thumbnaillogo.md)                                             | Нет     | **Organizational-Person**                                             |
| [**Управляемые объекты**](a-managedobjects.md)                                 | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Manager**](a-manager.md)                                                | Нет     | **Organizational-Person**                                             |
| [**В основном**](a-masteredby.md)                                         | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**МХС-или-Address**](a-mhsoraddress.md)                                    | Нет     | **Organizational-Person**                                             |
| [**Метка времени изменения**](a-modifytimestamp.md)                              | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-COM-Партитионсетлинк**](a-mscom-partitionsetlink.md)                 | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-COM-Усерлинк**](a-mscom-userlink.md)                                 | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-Allowed-to-Delegate-to**](a-msds-allowedtodelegateto.md)          | Нет     | **Organizational-Person**                                             |
| [**MS-DS-примерно-Иммед-подчиненные**](a-msds-approx-immed-subordinates.md) | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-целостность-дочерняя — количество**](a-ms-ds-consistencychildcount.md)      | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-Consistencу-Guid**](a-ms-ds-consistencyguid.md)                   | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-Masterd-by**](a-msds-masteredby.md)                              | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)           | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-NC-REPL-курсоры**](a-msds-ncreplcursors.md)                       | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-NC-REPL-Inbound-соседи**](a-msds-ncreplinboundneighbors.md)    | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-NC-REPL-Outbound-соседи**](a-msds-ncreploutboundneighbors.md)  | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-не-Members-BL**](a-msds-nonmembersbl.md)                         | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-Operations-для-AZ-Role-BL**](a-msds-operationsforazrolebl.md)     | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)     | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-REPL-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)              | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-Tasks-для-AZ-Role-BL**](a-msds-tasksforazrolebl.md)               | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)               | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-дов-House-identifier**](a-msexchhouseidentifier.md)                 | Нет     | **Organizational-Person**                                             |
| [**MS-дов-Owner-BL**](a-ownerbl.md)                                       | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**нетбут-SCP-BL**](a-netbootscpbl.md)                                    | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Не-Security-Member-BL**](a-nonsecuritymemberbl.md)                     | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**NT-Security-дескриптор**](a-ntsecuritydescriptor.md)                    | Верно      | [**Вверх**](c-top.md)<br/>                                       |
| [**Obj-расп-имя**](a-distinguishedname.md)                                | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Объект — Категория**](a-objectcategory.md)                                 | Верно      | [**Вверх**](c-top.md)<br/>                                       |
| [**Объектный класс**](a-objectclass.md)                                       | Верно      | [**Вверх**](c-top.md)<br/>                                       |
| [**Объект — GUID**](a-objectguid.md)                                         | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Версия объекта**](a-objectversion.md)                                   | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Организация — имя подразделения**](a-ou.md)                                    | Нет     | **Organizational-Person**                                             |
| [**Название организации**](a-o.md)                                            | Нет     | **Organizational-Person**                                             |
| [**Другие — почтовый ящик**](a-othermailbox.md)                                     | Нет     | **Organizational-Person**                                             |
| [**Другое имя**](a-middlename.md)                                          | Нет     | **Organizational-Person**                                             |
| [**Другие хорошо известные объекты**](a-otherwellknownobjects.md)                 | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Разделяемый атрибут-удаление-список**](a-partialattributedeletionlist.md)   | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Разделяемый атрибут-set**](a-partialattributeset.md)                      | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Личный заголовок**](a-personaltitle.md)                                   | Нет     | **Organizational-Person**                                             |
| [**Телефон-Fax — другие**](a-otherfacsimiletelephonenumber.md)                  | Нет     | **Organizational-Person**                                             |
| [**Телефон-Home — другие**](a-otherhomephone.md)                                | Нет     | **Organizational-Person**                                             |
| [**Телефон-Home — основной**](a-homephone.md)                                   | Нет     | **Organizational-Person**                                             |
| [**Телефон-Ip — другие**](a-otheripphone.md)                                    | Нет     | **Organizational-Person**                                             |
| [**Телефон-Ip-Primary**](a-ipphone.md)                                       | Нет     | **Organizational-Person**                                             |
| [**Телефон-ISDN-Primary**](a-primaryinternationalisdnnumber.md)              | Нет     | **Organizational-Person**                                             |
| [**Телефон-Mobile — другие**](a-othermobile.md)                                 | Нет     | **Organizational-Person**                                             |
| [**Телефон — Mobile — Primary**](a-mobile.md)                                    | Нет     | **Organizational-Person**                                             |
| [**Телефон-Office-Other**](a-othertelephone.md)                              | Нет     | **Organizational-Person**                                             |
| [**Телефон-пейджер — другие**](a-otherpager.md)                                   | Нет     | **Organizational-Person**                                             |
| [**Телефон-пейджер-основной**](a-pager.md)                                      | Нет     | **Organizational-Person**                                             |
| [**физическая доставка — Office-имя**](a-physicaldeliveryofficename.md)       | Нет     | **Organizational-Person**                                             |
| [**Снимки**](a-thumbnailphoto.md)                                         | Нет     | **Organizational-Person**                                             |
| [**Возможно — подстрочные**](a-possibleinferiors.md)                           | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Почтовый адрес**](a-postaladdress.md)                                   | Нет     | **Organizational-Person**                                             |
| [**Почтовый код**](a-postalcode.md)                                         | Нет     | **Organizational-Person**                                             |
| [**флажок после Office**](a-postofficebox.md)                                  | Нет     | **Organizational-Person**                                             |
| [**Предпочтительный метод доставки**](a-preferreddeliverymethod.md)              | Нет     | **Organizational-Person**                                             |
| [**Прокси-объект-имя**](a-proxiedobjectname.md)                          | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Прокси-адреса**](a-proxyaddresses.md)                                 | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Запрос — политика — BL**](a-querypolicybl.md)                                  | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**RDN**](a-name.md)                                                       | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Зарегистрированный адрес**](a-registeredaddress.md)                           | Нет     | **Organizational-Person**                                             |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                   | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**REPL-Уптодате-Vector**](a-repluptodatevector.md)                        | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Отчеты**](a-directreports.md)                                          | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Представители — от**](a-repsfrom.md)                                             | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Представители — кому**](a-repsto.md)                                                 | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Редакции**](a-revision.md)                                              | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**SD-Rights-эффективен**](a-sdrightseffective.md)                          | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**См. также**](a-seealso.md)                                               | Нет     | [**Человек**](c-person.md)<br/>                                 |
| [**Серийный номер**](a-serialnumber.md)                                     | Нет     | [**Человек**](c-person.md)<br/>                                 |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**"Показать" — "Расширенный просмотр"**](a-showinadvancedviewonly.md)              | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**State-или-провинция-Name**](a-st.md)                                      | Нет     | **Organizational-Person**                                             |
| [**Улица-адрес**](a-street.md)                                          | Нет     | **Organizational-Person**                                             |
| [**Структурный объектный класс**](a-structuralobjectclass.md)                  | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Подразделы-ReFS**](a-subrefs.md)                                               | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**субсчемасубентри**](a-subschemasubentry.md)                            | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Образование**](a-sn.md)                                                     | Нет     | [**Человек**](c-person.md)<br/>                                 |
| [**Системные флаги**](a-systemflags.md)                                       | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Номер телефона**](a-telephonenumber.md)                               | Нет     | [**Человек**](c-person.md)<br/>                                 |
| [**Teletex — идентификатор терминала**](a-teletexterminalidentifier.md)          | Нет     | **Organizational-Person**                                             |
| [**Номер телекса**](a-telexnumber.md)                                       | Нет     | **Organizational-Person**                                             |
| [**Номер телекса (первичный)**](a-primarytelexnumber.md)                               | Нет     | **Organizational-Person**                                             |
| [**Текст — страна**](a-co.md)                                                | Нет     | **Organizational-Person**                                             |
| [**Название**](a-title.md)                                                    | Нет     | **Organizational-Person**                                             |
| [**Комментарий пользователя**](a-comment.md)                                           | Нет     | **Organizational-Person**                                             |
| [**Пароль пользователя**](a-userpassword.md)                                     | Нет     | [**Человек**](c-person.md)<br/>                                 |
| [**USN-изменено**](a-usnchanged.md)                                         | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Созданный USN**](a-usncreated.md)                                         | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**USN-DSA-Last-obj-removed**](a-usndsalastobjremoved.md)                  | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**USN — межсайтовая**](a-usnintersite.md)                                     | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                 | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Источник USN**](a-usnsource.md)                                           | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**WBEM — путь**](a-wbempath.md)                                             | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Хорошо известные объекты**](a-wellknownobjects.md)                            | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**При изменении**](a-whenchanged.md)                                       | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**При создании**](a-whencreated.md)                                       | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**WWW — Главная страница**](a-wwwhomepage.md)                                      | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**WWW-Page — другие**](a-url.md)                                             | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**X121 — адрес**](a-x121address.md)                                       | Нет     | **Organizational-Person**                                             |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2

-   [Атрибуты](#windows-server-2003-r2-attributes)



| Ввод | Значение |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Нет                                                                                                                     |
| Object-Category             | 0                                                                                                                         |
| По умолчанию — объект — Категория     | [**Человек**](c-person.md)<br/>                                                                                     |
| Governs-Id                  | 2.5.6.7                                                                                                                   |
| По умолчанию-скрытие значения        | 1                                                                                                                         |
| RDN-Атри-ID                  | [**Common-Name**](a-cn.md)<br/>                                                                                    |
| Подкласс                 | [**Человек**](c-person.md)<br/>                                                                                     |
| Возможные старшие          | [](c-container.md)[](c-organization.md)[**Организационная единица**](c-organizationalunit.md) Организации контейнера |
| Вспомогательные классы           | \-                                                                                                                        |
| NT-Security-дескриптор      | О:БАГ: BAD: S:                                                                                                              |
| Дескриптор безопасности по умолчанию | D: (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;;D А) (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;; SY) (A;; РПЛКЛОРК;;; СЛУЖБЫ                              |
| System-Flags                | 0x00000010                                                                                                                |



## <a name="windows-server-2003-r2-attributes"></a>Windows Атрибуты сервера 2003 R2

этот класс содержит следующие атрибуты для Windows Server 2003 R2:



| attribute                                                                   | Обязательный | Унаследован от                                                          |
|-----------------------------------------------------------------------------|-----------|-----------------------------------------------------------------------|
| [**Адрес**](a-streetaddress.md)                                          | Нет     | **Organizational-Person**                                             |
| [**Адрес — Домашняя страница**](a-homepostaladdress.md)                                 | Нет     | **Organizational-Person**                                             |
| [**Описание администратора**](a-admindescription.md)                             | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Имя администратора-отображение**](a-admindisplayname.md)                            | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Allowed-Attributes**](a-allowedattributes.md)                           | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Allowed-Attributes-эффективен**](a-allowedattributeseffective.md)        | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Allowed-Child-classes**](a-allowedchildclasses.md)                      | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Allowed-Child-classes-эффективен**](a-allowedchildclasseseffective.md)   | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Средство**](a-assistant.md)                                            | Нет     | **Organizational-Person**                                             |
| [**аттрибутецертификатеаттрибуте**](a-attributecertificateattribute.md)    | Нет     | [**Человек**](c-person.md)<br/>                                 |
| [**Плацдарм-Server-List-BL**](a-bridgeheadserverlistbl.md)               | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Каноническое имя**](a-canonicalname.md)                                   | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Common-Name**](a-cn.md)                                                 | Верно      | [**Человек**](c-person.md)<br/> [**Вверх**](c-top.md)<br/> |
| [**Company**](a-company.md)                                                | Нет     | **Organizational-Person**                                             |
| [**Код страны**](a-countrycode.md)                                       | Нет     | **Organizational-Person**                                             |
| [**Название страны**](a-c.md)                                                 | Нет     | **Organizational-Person**                                             |
| [**Метка времени создания**](a-createtimestamp.md)                              | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Отдел**](a-department.md)                                          | Нет     | **Organizational-Person**                                             |
| [**Описание**](a-description.md)                                        | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Целевой индикатор**](a-destinationindicator.md)                     | Нет     | **Organizational-Person**                                             |
| [**Отображаемое имя**](a-displayname.md)                                       | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Отображаемое имя — печатаемое**](a-displaynameprintable.md)                    | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Отдел**](a-division.md)                                              | Нет     | **Organizational-Person**                                             |
| [**DSA-Signature**](a-dsasignature.md)                                     | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**DS-Core-распространение-данные**](a-dscorepropagationdata.md)                 | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Адреса электронной почты**](a-mail.md)                                          | Нет     | **Organizational-Person**                                             |
| [**Идентификатор сотрудника**](a-employeeid.md)                                         | Нет     | **Organizational-Person**                                             |
| [**Имя расширения**](a-extensionname.md)                                   | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Факс-телефон — номер**](a-facsimiletelephonenumber.md)            | Нет     | **Organizational-Person**                                             |
| [**Метки**](a-flags.md)                                                    | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Из записи**](a-fromentry.md)                                           | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Квалификатор поколения**](a-generationqualifier.md)                       | Нет     | **Organizational-Person**                                             |
| [**Заданное имя**](a-givenname.md)                                           | Нет     | **Organizational-Person**                                             |
| [**хаусеидентифиер**](a-houseidentifier.md)                                | Нет     | **Organizational-Person**                                             |
| [**Инициалы**](a-initials.md)                                              | Нет     | **Organizational-Person**                                             |
| [**Тип экземпляра**](a-instancetype.md)                                     | Верно      | [**Вверх**](c-top.md)<br/>                                       |
| [**Международный-ISDN-номер**](a-internationalisdnnumber.md)              | Нет     | **Organizational-Person**                                             |
| [**Является критически важным — системный объект**](a-iscriticalsystemobject.md)               | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Удалено**](a-isdeleted.md)                                           | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Входит в состав списка рассылки**](a-memberof.md)                                       | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Имеет права владельца**](a-isprivilegeholder.md)                          | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Последний-известный-родительский**](a-lastknownparent.md)                              | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Локальное имя**](a-l.md)                                                | Нет     | **Organizational-Person**                                             |
| [**Эмблема**](a-thumbnaillogo.md)                                             | Нет     | **Organizational-Person**                                             |
| [**Управляемые объекты**](a-managedobjects.md)                                 | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Manager**](a-manager.md)                                                | Нет     | **Organizational-Person**                                             |
| [**В основном**](a-masteredby.md)                                         | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**МХС-или-Address**](a-mhsoraddress.md)                                    | Нет     | **Organizational-Person**                                             |
| [**Метка времени изменения**](a-modifytimestamp.md)                              | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-COM-Партитионсетлинк**](a-mscom-partitionsetlink.md)                 | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-COM-Усерлинк**](a-mscom-userlink.md)                                 | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DFSR-Компутерреференцебл**](a-msdfsr-computerreferencebl.md)         | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DFSR-Мемберреференцебл**](a-msdfsr-memberreferencebl.md)             | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-Allowed-to-Delegate-to**](a-msds-allowedtodelegateto.md)          | Нет     | **Organizational-Person**                                             |
| [**MS-DS-примерно-Иммед-подчиненные**](a-msds-approx-immed-subordinates.md) | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-целостность-дочерняя — количество**](a-ms-ds-consistencychildcount.md)      | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-Consistencу-Guid**](a-ms-ds-consistencyguid.md)                   | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-Masterd-by**](a-msds-masteredby.md)                              | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)           | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-NC-REPL-курсоры**](a-msds-ncreplcursors.md)                       | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-NC-REPL-Inbound-соседи**](a-msds-ncreplinboundneighbors.md)    | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-NC-REPL-Outbound-соседи**](a-msds-ncreploutboundneighbors.md)  | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-не-Members-BL**](a-msds-nonmembersbl.md)                         | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-Operations-для-AZ-Role-BL**](a-msds-operationsforazrolebl.md)     | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)     | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-REPL-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)              | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-Tasks-для-AZ-Role-BL**](a-msds-tasksforazrolebl.md)               | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)               | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-дов-House-identifier**](a-msexchhouseidentifier.md)                 | Нет     | **Organizational-Person**                                             |
| [**MS-дов-Owner-BL**](a-ownerbl.md)                                       | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Мссфу-30-POSIX-член-of**](a-mssfu30posixmemberof.md)                  | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**нетбут-SCP-BL**](a-netbootscpbl.md)                                    | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Не-Security-Member-BL**](a-nonsecuritymemberbl.md)                     | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**NT-Security-дескриптор**](a-ntsecuritydescriptor.md)                    | Верно      | [**Вверх**](c-top.md)<br/>                                       |
| [**Obj-расп-имя**](a-distinguishedname.md)                                | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Объект — Категория**](a-objectcategory.md)                                 | Верно      | [**Вверх**](c-top.md)<br/>                                       |
| [**Объектный класс**](a-objectclass.md)                                       | Верно      | [**Вверх**](c-top.md)<br/>                                       |
| [**Объект — GUID**](a-objectguid.md)                                         | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Версия объекта**](a-objectversion.md)                                   | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Организация — имя подразделения**](a-ou.md)                                    | Нет     | **Organizational-Person**                                             |
| [**Название организации**](a-o.md)                                            | Нет     | **Organizational-Person**                                             |
| [**Другие — почтовый ящик**](a-othermailbox.md)                                     | Нет     | **Organizational-Person**                                             |
| [**Другое имя**](a-middlename.md)                                          | Нет     | **Organizational-Person**                                             |
| [**Другие хорошо известные объекты**](a-otherwellknownobjects.md)                 | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Разделяемый атрибут-удаление-список**](a-partialattributedeletionlist.md)   | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Разделяемый атрибут-set**](a-partialattributeset.md)                      | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Личный заголовок**](a-personaltitle.md)                                   | Нет     | **Organizational-Person**                                             |
| [**Телефон-Fax — другие**](a-otherfacsimiletelephonenumber.md)                  | Нет     | **Organizational-Person**                                             |
| [**Телефон-Home — другие**](a-otherhomephone.md)                                | Нет     | **Organizational-Person**                                             |
| [**Телефон-Home — основной**](a-homephone.md)                                   | Нет     | **Organizational-Person**                                             |
| [**Телефон-Ip — другие**](a-otheripphone.md)                                    | Нет     | **Organizational-Person**                                             |
| [**Телефон-Ip-Primary**](a-ipphone.md)                                       | Нет     | **Organizational-Person**                                             |
| [**Телефон-ISDN-Primary**](a-primaryinternationalisdnnumber.md)              | Нет     | **Organizational-Person**                                             |
| [**Телефон-Mobile — другие**](a-othermobile.md)                                 | Нет     | **Organizational-Person**                                             |
| [**Телефон — Mobile — Primary**](a-mobile.md)                                    | Нет     | **Organizational-Person**                                             |
| [**Телефон-Office-Other**](a-othertelephone.md)                              | Нет     | **Organizational-Person**                                             |
| [**Телефон-пейджер — другие**](a-otherpager.md)                                   | Нет     | **Organizational-Person**                                             |
| [**Телефон-пейджер-основной**](a-pager.md)                                      | Нет     | **Organizational-Person**                                             |
| [**физическая доставка — Office-имя**](a-physicaldeliveryofficename.md)       | Нет     | **Organizational-Person**                                             |
| [**Снимки**](a-thumbnailphoto.md)                                         | Нет     | **Organizational-Person**                                             |
| [**Возможно — подстрочные**](a-possibleinferiors.md)                           | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Почтовый адрес**](a-postaladdress.md)                                   | Нет     | **Organizational-Person**                                             |
| [**Почтовый код**](a-postalcode.md)                                         | Нет     | **Organizational-Person**                                             |
| [**флажок после Office**](a-postofficebox.md)                                  | Нет     | **Organizational-Person**                                             |
| [**Предпочтительный метод доставки**](a-preferreddeliverymethod.md)              | Нет     | **Organizational-Person**                                             |
| [**Прокси-объект-имя**](a-proxiedobjectname.md)                          | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Прокси-адреса**](a-proxyaddresses.md)                                 | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Запрос — политика — BL**](a-querypolicybl.md)                                  | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**RDN**](a-name.md)                                                       | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Зарегистрированный адрес**](a-registeredaddress.md)                           | Нет     | **Organizational-Person**                                             |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                   | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**REPL-Уптодате-Vector**](a-repluptodatevector.md)                        | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Отчеты**](a-directreports.md)                                          | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Представители — от**](a-repsfrom.md)                                             | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Представители — кому**](a-repsto.md)                                                 | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Редакции**](a-revision.md)                                              | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**SD-Rights-эффективен**](a-sdrightseffective.md)                          | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**См. также**](a-seealso.md)                                               | Нет     | [**Человек**](c-person.md)<br/>                                 |
| [**Серийный номер**](a-serialnumber.md)                                     | Нет     | [**Человек**](c-person.md)<br/>                                 |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**"Показать" — "Расширенный просмотр"**](a-showinadvancedviewonly.md)              | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**State-или-провинция-Name**](a-st.md)                                      | Нет     | **Organizational-Person**                                             |
| [**Улица-адрес**](a-street.md)                                          | Нет     | **Organizational-Person**                                             |
| [**Структурный объектный класс**](a-structuralobjectclass.md)                  | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Подразделы-ReFS**](a-subrefs.md)                                               | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**субсчемасубентри**](a-subschemasubentry.md)                            | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Образование**](a-sn.md)                                                     | Нет     | [**Человек**](c-person.md)<br/>                                 |
| [**Системные флаги**](a-systemflags.md)                                       | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Номер телефона**](a-telephonenumber.md)                               | Нет     | [**Человек**](c-person.md)<br/>                                 |
| [**Teletex — идентификатор терминала**](a-teletexterminalidentifier.md)          | Нет     | **Organizational-Person**                                             |
| [**Номер телекса**](a-telexnumber.md)                                       | Нет     | **Organizational-Person**                                             |
| [**Номер телекса (первичный)**](a-primarytelexnumber.md)                               | Нет     | **Organizational-Person**                                             |
| [**Текст — страна**](a-co.md)                                                | Нет     | **Organizational-Person**                                             |
| [**Название**](a-title.md)                                                    | Нет     | **Organizational-Person**                                             |
| [**Комментарий пользователя**](a-comment.md)                                           | Нет     | **Organizational-Person**                                             |
| [**Пароль пользователя**](a-userpassword.md)                                     | Нет     | [**Человек**](c-person.md)<br/>                                 |
| [**USN-изменено**](a-usnchanged.md)                                         | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Созданный USN**](a-usncreated.md)                                         | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**USN-DSA-Last-obj-removed**](a-usndsalastobjremoved.md)                  | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**USN — межсайтовая**](a-usnintersite.md)                                     | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                 | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Источник USN**](a-usnsource.md)                                           | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**WBEM — путь**](a-wbempath.md)                                             | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Хорошо известные объекты**](a-wellknownobjects.md)                            | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**При изменении**](a-whenchanged.md)                                       | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**При создании**](a-whencreated.md)                                       | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**WWW — Главная страница**](a-wwwhomepage.md)                                      | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**WWW-Page — другие**](a-url.md)                                             | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**X121 — адрес**](a-x121address.md)                                       | Нет     | **Organizational-Person**                                             |



## <a name="windows-server-2008"></a>Windows Server 2008

-   [Атрибуты](#windows-server-2008-attributes)



| Ввод | Значение |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Нет                                                                                                                     |
| Object-Category             | 0                                                                                                                         |
| По умолчанию — объект — Категория     | [**Человек**](c-person.md)<br/>                                                                                     |
| Governs-Id                  | 2.5.6.7                                                                                                                   |
| По умолчанию-скрытие значения        | 1                                                                                                                         |
| RDN-Атри-ID                  | [**Common-Name**](a-cn.md)<br/>                                                                                    |
| Подкласс                 | [**Человек**](c-person.md)<br/>                                                                                     |
| Возможные старшие          | [](c-container.md)[](c-organization.md)[**Организационная единица**](c-organizationalunit.md) Организации контейнера |
| Вспомогательные классы           | \-                                                                                                                        |
| NT-Security-дескриптор      | О:БАГ: BAD: S:                                                                                                              |
| Дескриптор безопасности по умолчанию | D: (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;;D А) (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;; SY) (A;; РПЛКЛОРК;;; СЛУЖБЫ                              |
| System-Flags                | 0x00000010                                                                                                                |



## <a name="windows-server-2008-attributes"></a>Windows Атрибуты сервера 2008

этот класс содержит следующие атрибуты для Windows Server 2008:



| attribute                                                                      | Обязательный | Унаследован от                                                          |
|--------------------------------------------------------------------------------|-----------|-----------------------------------------------------------------------|
| [**Адрес**](a-streetaddress.md)                                             | Нет     | **Organizational-Person**                                             |
| [**Адрес — Домашняя страница**](a-homepostaladdress.md)                                    | Нет     | **Organizational-Person**                                             |
| [**Описание администратора**](a-admindescription.md)                                | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Имя администратора-отображение**](a-admindisplayname.md)                               | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Allowed-Attributes**](a-allowedattributes.md)                              | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Allowed-Attributes-эффективен**](a-allowedattributeseffective.md)           | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Allowed-Child-classes**](a-allowedchildclasses.md)                         | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Allowed-Child-classes-эффективен**](a-allowedchildclasseseffective.md)      | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Средство**](a-assistant.md)                                               | Нет     | **Organizational-Person**                                             |
| [**аттрибутецертификатеаттрибуте**](a-attributecertificateattribute.md)       | Нет     | [**Человек**](c-person.md)<br/>                                 |
| [**Плацдарм-Server-List-BL**](a-bridgeheadserverlistbl.md)                  | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Каноническое имя**](a-canonicalname.md)                                      | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Common-Name**](a-cn.md)                                                    | Верно      | [**Человек**](c-person.md)<br/> [**Вверх**](c-top.md)<br/> |
| [**Company**](a-company.md)                                                   | Нет     | **Organizational-Person**                                             |
| [**Код страны**](a-countrycode.md)                                          | Нет     | **Organizational-Person**                                             |
| [**Название страны**](a-c.md)                                                    | Нет     | **Organizational-Person**                                             |
| [**Метка времени создания**](a-createtimestamp.md)                                 | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Отдел**](a-department.md)                                             | Нет     | **Organizational-Person**                                             |
| [**Описание**](a-description.md)                                           | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Целевой индикатор**](a-destinationindicator.md)                        | Нет     | **Organizational-Person**                                             |
| [**Отображаемое имя**](a-displayname.md)                                          | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Отображаемое имя — печатаемое**](a-displaynameprintable.md)                       | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Отдел**](a-division.md)                                                 | Нет     | **Organizational-Person**                                             |
| [**DSA-Signature**](a-dsasignature.md)                                        | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**DS-Core-распространение-данные**](a-dscorepropagationdata.md)                    | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Адреса электронной почты**](a-mail.md)                                             | Нет     | **Organizational-Person**                                             |
| [**Идентификатор сотрудника**](a-employeeid.md)                                            | Нет     | **Organizational-Person**                                             |
| [**Имя расширения**](a-extensionname.md)                                      | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Факс-телефон — номер**](a-facsimiletelephonenumber.md)               | Нет     | **Organizational-Person**                                             |
| [**Метки**](a-flags.md)                                                       | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Из записи**](a-fromentry.md)                                              | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                  | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                      | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                     | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Квалификатор поколения**](a-generationqualifier.md)                          | Нет     | **Organizational-Person**                                             |
| [**Заданное имя**](a-givenname.md)                                              | Нет     | **Organizational-Person**                                             |
| [**хаусеидентифиер**](a-houseidentifier.md)                                   | Нет     | **Organizational-Person**                                             |
| [**Инициалы**](a-initials.md)                                                 | Нет     | **Organizational-Person**                                             |
| [**Тип экземпляра**](a-instancetype.md)                                        | Верно      | [**Вверх**](c-top.md)<br/>                                       |
| [**Международный-ISDN-номер**](a-internationalisdnnumber.md)                 | Нет     | **Organizational-Person**                                             |
| [**Является критически важным — системный объект**](a-iscriticalsystemobject.md)                  | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Удалено**](a-isdeleted.md)                                              | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Входит в состав списка рассылки**](a-memberof.md)                                          | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Имеет права владельца**](a-isprivilegeholder.md)                             | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Последний-известный-родительский**](a-lastknownparent.md)                                 | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Локальное имя**](a-l.md)                                                   | Нет     | **Organizational-Person**                                             |
| [**Эмблема**](a-thumbnaillogo.md)                                                | Нет     | **Organizational-Person**                                             |
| [**Управляемые объекты**](a-managedobjects.md)                                    | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Manager**](a-manager.md)                                                   | Нет     | **Organizational-Person**                                             |
| [**В основном**](a-masteredby.md)                                            | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**МХС-или-Address**](a-mhsoraddress.md)                                       | Нет     | **Organizational-Person**                                             |
| [**Метка времени изменения**](a-modifytimestamp.md)                                 | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-COM-Партитионсетлинк**](a-mscom-partitionsetlink.md)                    | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-COM-Усерлинк**](a-mscom-userlink.md)                                    | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DFSR-Компутерреференцебл**](a-msdfsr-computerreferencebl.md)            | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DFSR-Мемберреференцебл**](a-msdfsr-memberreferencebl.md)                | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-Allowed-to-Delegate-to**](a-msds-allowedtodelegateto.md)             | Нет     | **Organizational-Person**                                             |
| [**MS-DS-примерно-Иммед-подчиненные**](a-msds-approx-immed-subordinates.md)    | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-Аусентикатедто-Аккаунтлист**](a-msds-authenticatedtoaccountlist.md) | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-целостность-дочерняя — количество**](a-ms-ds-consistencychildcount.md)         | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-Consistencу-Guid**](a-ms-ds-consistencyguid.md)                      | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-ИЕРАРХИя — старший стаж — индекс**](a-msds-habseniorityindex.md)                  | Нет     | **Organizational-Person**                                             |
| [**MS-DS--домен — для**](a-msds-isdomainfor.md)                              | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-является-Full-реплика для**](a-msds-isfullreplicafor.md)                   | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-является-partial-реплика для**](a-msds-ispartialreplicafor.md)             | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                            | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-Masterd-by**](a-msds-masteredby.md)                                 | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)              | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-NC-REPL-курсоры**](a-msds-ncreplcursors.md)                          | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-NC-REPL-Inbound-соседи**](a-msds-ncreplinboundneighbors.md)       | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-NC-REPL-Outbound-соседи**](a-msds-ncreploutboundneighbors.md)     | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)  | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-NC-Type**](a-msds-nctype.md)                                         | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-не-Members-BL**](a-msds-nonmembersbl.md)                            | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                  | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-Operations-для-AZ-Role-BL**](a-msds-operationsforazrolebl.md)        | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)        | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-Фонетическое название компании**](a-msds-phoneticcompanyname.md)              | Нет     | **Organizational-Person**                                             |
| [**MS-DS-фонетический отдел**](a-msds-phoneticdepartment.md)                 | Нет     | **Organizational-Person**                                             |
| [**MS-DS-фонетическо-отображаемое имя**](a-msds-phoneticdisplayname.md)              | Нет     | **Organizational-Person**                                             |
| [**MS-DS-фонетическо-First-Name**](a-msds-phoneticfirstname.md)                  | Нет     | **Organizational-Person**                                             |
| [**MS-DS-фонетическое имя (фамилия)**](a-msds-phoneticlastname.md)                    | Нет     | **Organizational-Person**                                             |
| [**MS-DS-Principal-Name**](a-msds-principalname.md)                           | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-PSO — применяется**](a-msds-psoapplied.md)                                 | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-REPL-Attribute-Meta-Data**](a-msds-replattributemetadata.md)         | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)                 | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-выявил-DSA**](a-msds-revealeddsas.md)                             | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-выводит-List-BL**](a-msds-revealedlistbl.md)                        | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-Tasks-для-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                  | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                  | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-дов-House-identifier**](a-msexchhouseidentifier.md)                    | Нет     | **Organizational-Person**                                             |
| [**MS-дов-Owner-BL**](a-ownerbl.md)                                          | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Мссфу-30-POSIX-член-of**](a-mssfu30posixmemberof.md)                     | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**нетбут-SCP-BL**](a-netbootscpbl.md)                                       | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Не-Security-Member-BL**](a-nonsecuritymemberbl.md)                        | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**NT-Security-дескриптор**](a-ntsecuritydescriptor.md)                       | Верно      | [**Вверх**](c-top.md)<br/>                                       |
| [**Obj-расп-имя**](a-distinguishedname.md)                                   | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Объект — Категория**](a-objectcategory.md)                                    | Верно      | [**Вверх**](c-top.md)<br/>                                       |
| [**Объектный класс**](a-objectclass.md)                                          | Верно      | [**Вверх**](c-top.md)<br/>                                       |
| [**Объект — GUID**](a-objectguid.md)                                            | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Версия объекта**](a-objectversion.md)                                      | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Организация — имя подразделения**](a-ou.md)                                       | Нет     | **Organizational-Person**                                             |
| [**Название организации**](a-o.md)                                               | Нет     | **Organizational-Person**                                             |
| [**Другие — почтовый ящик**](a-othermailbox.md)                                        | Нет     | **Organizational-Person**                                             |
| [**Другое имя**](a-middlename.md)                                             | Нет     | **Organizational-Person**                                             |
| [**Другие хорошо известные объекты**](a-otherwellknownobjects.md)                    | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Разделяемый атрибут-удаление-список**](a-partialattributedeletionlist.md)      | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Разделяемый атрибут-set**](a-partialattributeset.md)                         | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Личный заголовок**](a-personaltitle.md)                                      | Нет     | **Organizational-Person**                                             |
| [**Телефон-Fax — другие**](a-otherfacsimiletelephonenumber.md)                     | Нет     | **Organizational-Person**                                             |
| [**Телефон-Home — другие**](a-otherhomephone.md)                                   | Нет     | **Organizational-Person**                                             |
| [**Телефон-Home — основной**](a-homephone.md)                                      | Нет     | **Organizational-Person**                                             |
| [**Телефон-Ip — другие**](a-otheripphone.md)                                       | Нет     | **Organizational-Person**                                             |
| [**Телефон-Ip-Primary**](a-ipphone.md)                                          | Нет     | **Organizational-Person**                                             |
| [**Телефон-ISDN-Primary**](a-primaryinternationalisdnnumber.md)                 | Нет     | **Organizational-Person**                                             |
| [**Телефон-Mobile — другие**](a-othermobile.md)                                    | Нет     | **Organizational-Person**                                             |
| [**Телефон — Mobile — Primary**](a-mobile.md)                                       | Нет     | **Organizational-Person**                                             |
| [**Телефон-Office-Other**](a-othertelephone.md)                                 | Нет     | **Organizational-Person**                                             |
| [**Телефон-пейджер — другие**](a-otherpager.md)                                      | Нет     | **Organizational-Person**                                             |
| [**Телефон-пейджер-основной**](a-pager.md)                                         | Нет     | **Organizational-Person**                                             |
| [**физическая доставка — Office-имя**](a-physicaldeliveryofficename.md)          | Нет     | **Organizational-Person**                                             |
| [**Снимки**](a-thumbnailphoto.md)                                            | Нет     | **Organizational-Person**                                             |
| [**Возможно — подстрочные**](a-possibleinferiors.md)                              | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Почтовый адрес**](a-postaladdress.md)                                      | Нет     | **Organizational-Person**                                             |
| [**Почтовый код**](a-postalcode.md)                                            | Нет     | **Organizational-Person**                                             |
| [**флажок после Office**](a-postofficebox.md)                                     | Нет     | **Organizational-Person**                                             |
| [**Предпочтительный метод доставки**](a-preferreddeliverymethod.md)                 | Нет     | **Organizational-Person**                                             |
| [**Прокси-объект-имя**](a-proxiedobjectname.md)                             | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Прокси-адреса**](a-proxyaddresses.md)                                    | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Запрос — политика — BL**](a-querypolicybl.md)                                     | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**RDN**](a-name.md)                                                          | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Зарегистрированный адрес**](a-registeredaddress.md)                              | Нет     | **Organizational-Person**                                             |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                      | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**REPL-Уптодате-Vector**](a-repluptodatevector.md)                           | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Отчеты**](a-directreports.md)                                             | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Представители — от**](a-repsfrom.md)                                                | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Представители — кому**](a-repsto.md)                                                    | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Редакции**](a-revision.md)                                                 | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**SD-Rights-эффективен**](a-sdrightseffective.md)                             | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**См. также**](a-seealso.md)                                                  | Нет     | [**Человек**](c-person.md)<br/>                                 |
| [**Серийный номер**](a-serialnumber.md)                                        | Нет     | [**Человек**](c-person.md)<br/>                                 |
| [**Server-Reference-BL**](a-serverreferencebl.md)                             | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**"Показать" — "Расширенный просмотр"**](a-showinadvancedviewonly.md)                 | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Site-Object-BL**](a-siteobjectbl.md)                                       | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**State-или-провинция-Name**](a-st.md)                                         | Нет     | **Organizational-Person**                                             |
| [**Улица-адрес**](a-street.md)                                             | Нет     | **Organizational-Person**                                             |
| [**Структурный объектный класс**](a-structuralobjectclass.md)                     | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Подразделы-ReFS**](a-subrefs.md)                                                  | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**субсчемасубентри**](a-subschemasubentry.md)                               | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Образование**](a-sn.md)                                                        | Нет     | [**Человек**](c-person.md)<br/>                                 |
| [**Системные флаги**](a-systemflags.md)                                          | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Номер телефона**](a-telephonenumber.md)                                  | Нет     | [**Человек**](c-person.md)<br/>                                 |
| [**Teletex — идентификатор терминала**](a-teletexterminalidentifier.md)             | Нет     | **Organizational-Person**                                             |
| [**Номер телекса**](a-telexnumber.md)                                          | Нет     | **Organizational-Person**                                             |
| [**Номер телекса (первичный)**](a-primarytelexnumber.md)                                  | Нет     | **Organizational-Person**                                             |
| [**Текст — страна**](a-co.md)                                                   | Нет     | **Organizational-Person**                                             |
| [**Название**](a-title.md)                                                       | Нет     | **Organizational-Person**                                             |
| [**Комментарий пользователя**](a-comment.md)                                              | Нет     | **Organizational-Person**                                             |
| [**Пароль пользователя**](a-userpassword.md)                                        | Нет     | [**Человек**](c-person.md)<br/>                                 |
| [**USN-изменено**](a-usnchanged.md)                                            | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Созданный USN**](a-usncreated.md)                                            | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**USN-DSA-Last-obj-removed**](a-usndsalastobjremoved.md)                     | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**USN — межсайтовая**](a-usnintersite.md)                                        | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                    | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Источник USN**](a-usnsource.md)                                              | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**WBEM — путь**](a-wbempath.md)                                                | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Хорошо известные объекты**](a-wellknownobjects.md)                               | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**При изменении**](a-whenchanged.md)                                          | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**При создании**](a-whencreated.md)                                          | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**WWW — Главная страница**](a-wwwhomepage.md)                                         | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**WWW-Page — другие**](a-url.md)                                                | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**X121 — адрес**](a-x121address.md)                                          | Нет     | **Organizational-Person**                                             |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2

-   [Атрибуты](#windows-server-2008-r2-attributes)



| Ввод | Значение |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Нет                                                                                                                     |
| Object-Category             | 0                                                                                                                         |
| По умолчанию — объект — Категория     | [**Человек**](c-person.md)<br/>                                                                                     |
| Governs-Id                  | 2.5.6.7                                                                                                                   |
| По умолчанию-скрытие значения        | 1                                                                                                                         |
| RDN-Атри-ID                  | [**Common-Name**](a-cn.md)<br/>                                                                                    |
| Подкласс                 | [**Человек**](c-person.md)<br/>                                                                                     |
| Возможные старшие          | [](c-container.md)[](c-organization.md)[**Организационная единица**](c-organizationalunit.md) Организации контейнера |
| Вспомогательные классы           | \-                                                                                                                        |
| NT-Security-дескриптор      | О:БАГ: BAD: S:                                                                                                              |
| Дескриптор безопасности по умолчанию | D: (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;;D А) (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;; SY) (A;; РПЛКЛОРК;;; СЛУЖБЫ                              |
| System-Flags                | 0x00000010                                                                                                                |



## <a name="windows-server-2008-r2-attributes"></a>Windows Атрибуты сервера 2008 R2

этот класс содержит следующие атрибуты для Windows Server 2008 R2:



| attribute                                                                        | Обязательный | Унаследован от                                                          |
|----------------------------------------------------------------------------------|-----------|-----------------------------------------------------------------------|
| [**Адрес**](a-streetaddress.md)                                               | Нет     | **Organizational-Person**                                             |
| [**Адрес — Домашняя страница**](a-homepostaladdress.md)                                      | Нет     | **Organizational-Person**                                             |
| [**Описание администратора**](a-admindescription.md)                                  | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Имя администратора-отображение**](a-admindisplayname.md)                                 | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Allowed-Attributes**](a-allowedattributes.md)                                | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Allowed-Attributes-эффективен**](a-allowedattributeseffective.md)             | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Allowed-Child-classes**](a-allowedchildclasses.md)                           | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Allowed-Child-classes-эффективен**](a-allowedchildclasseseffective.md)        | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Средство**](a-assistant.md)                                                 | Нет     | **Organizational-Person**                                             |
| [**аттрибутецертификатеаттрибуте**](a-attributecertificateattribute.md)         | Нет     | [**Человек**](c-person.md)<br/>                                 |
| [**Плацдарм-Server-List-BL**](a-bridgeheadserverlistbl.md)                    | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Каноническое имя**](a-canonicalname.md)                                        | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Common-Name**](a-cn.md)                                                      | Верно      | [**Человек**](c-person.md)<br/> [**Вверх**](c-top.md)<br/> |
| [**Company**](a-company.md)                                                     | Нет     | **Organizational-Person**                                             |
| [**Код страны**](a-countrycode.md)                                            | Нет     | **Organizational-Person**                                             |
| [**Название страны**](a-c.md)                                                      | Нет     | **Organizational-Person**                                             |
| [**Метка времени создания**](a-createtimestamp.md)                                   | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Отдел**](a-department.md)                                               | Нет     | **Organizational-Person**                                             |
| [**Описание**](a-description.md)                                             | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Целевой индикатор**](a-destinationindicator.md)                          | Нет     | **Organizational-Person**                                             |
| [**Отображаемое имя**](a-displayname.md)                                            | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Отображаемое имя — печатаемое**](a-displaynameprintable.md)                         | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Отдел**](a-division.md)                                                   | Нет     | **Organizational-Person**                                             |
| [**DSA-Signature**](a-dsasignature.md)                                          | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**DS-Core-распространение-данные**](a-dscorepropagationdata.md)                      | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Адреса электронной почты**](a-mail.md)                                               | Нет     | **Organizational-Person**                                             |
| [**Идентификатор сотрудника**](a-employeeid.md)                                              | Нет     | **Organizational-Person**                                             |
| [**Имя расширения**](a-extensionname.md)                                        | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Факс-телефон — номер**](a-facsimiletelephonenumber.md)                 | Нет     | **Organizational-Person**                                             |
| [**Метки**](a-flags.md)                                                         | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Из записи**](a-fromentry.md)                                                | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                    | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                        | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                       | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Квалификатор поколения**](a-generationqualifier.md)                            | Нет     | **Organizational-Person**                                             |
| [**Заданное имя**](a-givenname.md)                                                | Нет     | **Organizational-Person**                                             |
| [**хаусеидентифиер**](a-houseidentifier.md)                                     | Нет     | **Organizational-Person**                                             |
| [**Инициалы**](a-initials.md)                                                   | Нет     | **Organizational-Person**                                             |
| [**Тип экземпляра**](a-instancetype.md)                                          | Верно      | [**Вверх**](c-top.md)<br/>                                       |
| [**Международный-ISDN-номер**](a-internationalisdnnumber.md)                   | Нет     | **Organizational-Person**                                             |
| [**Является критически важным — системный объект**](a-iscriticalsystemobject.md)                    | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Удалено**](a-isdeleted.md)                                                | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Входит в состав списка рассылки**](a-memberof.md)                                            | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Имеет права владельца**](a-isprivilegeholder.md)                               | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Является перезапущенным**](a-isrecycled.md)                                              | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Последний-известный-родительский**](a-lastknownparent.md)                                   | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Локальное имя**](a-l.md)                                                     | Нет     | **Organizational-Person**                                             |
| [**Эмблема**](a-thumbnaillogo.md)                                                  | Нет     | **Organizational-Person**                                             |
| [**Управляемые объекты**](a-managedobjects.md)                                      | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Manager**](a-manager.md)                                                     | Нет     | **Organizational-Person**                                             |
| [**В основном**](a-masteredby.md)                                              | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**МХС-или-Address**](a-mhsoraddress.md)                                         | Нет     | **Organizational-Person**                                             |
| [**Метка времени изменения**](a-modifytimestamp.md)                                   | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-COM-Партитионсетлинк**](a-mscom-partitionsetlink.md)                      | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-COM-Усерлинк**](a-mscom-userlink.md)                                      | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DFSR-Компутерреференцебл**](a-msdfsr-computerreferencebl.md)              | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DFSR-Мемберреференцебл**](a-msdfsr-memberreferencebl.md)                  | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-Allowed-to-Delegate-to**](a-msds-allowedtodelegateto.md)               | Нет     | **Organizational-Person**                                             |
| [**MS-DS-примерно-Иммед-подчиненные**](a-msds-approx-immed-subordinates.md)      | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-Аусентикатедто-Аккаунтлист**](a-msds-authenticatedtoaccountlist.md)   | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-целостность-дочерняя — количество**](a-ms-ds-consistencychildcount.md)           | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-Consistencу-Guid**](a-ms-ds-consistencyguid.md)                        | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Поддержка MS-DS-Feature-BL**](a-msds-enabledfeaturebl.md)                      | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-ИЕРАРХИя — старший стаж — индекс**](a-msds-habseniorityindex.md)                    | Нет     | **Organizational-Person**                                             |
| [**MS-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)             | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS--домен — для**](a-msds-isdomainfor.md)                                | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-является-Full-реплика для**](a-msds-isfullreplicafor.md)                     | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-является-partial-реплика для**](a-msds-ispartialreplicafor.md)               | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                              | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                              | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-локально-эффективное удаление — время**](a-msds-localeffectivedeletiontime.md) | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-Local-эффективен — время перезапуска**](a-msds-localeffectiverecycletime.md)   | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-Masterd-by**](a-msds-masteredby.md)                                   | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)                | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-NC-REPL-курсоры**](a-msds-ncreplcursors.md)                            | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-NC-REPL-Inbound-соседи**](a-msds-ncreplinboundneighbors.md)         | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-NC-REPL-Outbound-соседи**](a-msds-ncreploutboundneighbors.md)       | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)    | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-NC-Type**](a-msds-nctype.md)                                           | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-не-Members-BL**](a-msds-nonmembersbl.md)                              | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                    | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-Оидтограуп-Link-BL**](a-msds-oidtogrouplinkbl.md)                      | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-Operations-для-AZ-Role-BL**](a-msds-operationsforazrolebl.md)          | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)          | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-Фонетическое название компании**](a-msds-phoneticcompanyname.md)                | Нет     | **Organizational-Person**                                             |
| [**MS-DS-фонетический отдел**](a-msds-phoneticdepartment.md)                   | Нет     | **Organizational-Person**                                             |
| [**MS-DS-фонетическо-отображаемое имя**](a-msds-phoneticdisplayname.md)                | Нет     | **Organizational-Person**                                             |
| [**MS-DS-фонетическо-First-Name**](a-msds-phoneticfirstname.md)                    | Нет     | **Organizational-Person**                                             |
| [**MS-DS-фонетическое имя (фамилия)**](a-msds-phoneticlastname.md)                      | Нет     | **Organizational-Person**                                             |
| [**MS-DS-Principal-Name**](a-msds-principalname.md)                             | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-PSO — применяется**](a-msds-psoapplied.md)                                   | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-REPL-Attribute-Meta-Data**](a-msds-replattributemetadata.md)           | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)                   | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-выявил-DSA**](a-msds-revealeddsas.md)                               | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-выводит-List-BL**](a-msds-revealedlistbl.md)                          | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-Tasks-для-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                    | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                    | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-дов-House-identifier**](a-msexchhouseidentifier.md)                      | Нет     | **Organizational-Person**                                             |
| [**MS-дов-Owner-BL**](a-ownerbl.md)                                            | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Мссфу-30-POSIX-член-of**](a-mssfu30posixmemberof.md)                       | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**нетбут-SCP-BL**](a-netbootscpbl.md)                                         | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Не-Security-Member-BL**](a-nonsecuritymemberbl.md)                          | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**NT-Security-дескриптор**](a-ntsecuritydescriptor.md)                         | Верно      | [**Вверх**](c-top.md)<br/>                                       |
| [**Obj-расп-имя**](a-distinguishedname.md)                                     | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Объект — Категория**](a-objectcategory.md)                                      | Верно      | [**Вверх**](c-top.md)<br/>                                       |
| [**Объектный класс**](a-objectclass.md)                                            | Верно      | [**Вверх**](c-top.md)<br/>                                       |
| [**Объект — GUID**](a-objectguid.md)                                              | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Версия объекта**](a-objectversion.md)                                        | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Организация — имя подразделения**](a-ou.md)                                         | Нет     | **Organizational-Person**                                             |
| [**Название организации**](a-o.md)                                                 | Нет     | **Organizational-Person**                                             |
| [**Другие — почтовый ящик**](a-othermailbox.md)                                          | Нет     | **Organizational-Person**                                             |
| [**Другое имя**](a-middlename.md)                                               | Нет     | **Organizational-Person**                                             |
| [**Другие хорошо известные объекты**](a-otherwellknownobjects.md)                      | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Разделяемый атрибут-удаление-список**](a-partialattributedeletionlist.md)        | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Разделяемый атрибут-set**](a-partialattributeset.md)                           | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Личный заголовок**](a-personaltitle.md)                                        | Нет     | **Organizational-Person**                                             |
| [**Телефон-Fax — другие**](a-otherfacsimiletelephonenumber.md)                       | Нет     | **Organizational-Person**                                             |
| [**Телефон-Home — другие**](a-otherhomephone.md)                                     | Нет     | **Organizational-Person**                                             |
| [**Телефон-Home — основной**](a-homephone.md)                                        | Нет     | **Organizational-Person**                                             |
| [**Телефон-Ip — другие**](a-otheripphone.md)                                         | Нет     | **Organizational-Person**                                             |
| [**Телефон-Ip-Primary**](a-ipphone.md)                                            | Нет     | **Organizational-Person**                                             |
| [**Телефон-ISDN-Primary**](a-primaryinternationalisdnnumber.md)                   | Нет     | **Organizational-Person**                                             |
| [**Телефон-Mobile — другие**](a-othermobile.md)                                      | Нет     | **Organizational-Person**                                             |
| [**Телефон — Mobile — Primary**](a-mobile.md)                                         | Нет     | **Organizational-Person**                                             |
| [**Телефон-Office-Other**](a-othertelephone.md)                                   | Нет     | **Organizational-Person**                                             |
| [**Телефон-пейджер — другие**](a-otherpager.md)                                        | Нет     | **Organizational-Person**                                             |
| [**Телефон-пейджер-основной**](a-pager.md)                                           | Нет     | **Organizational-Person**                                             |
| [**физическая доставка — Office-имя**](a-physicaldeliveryofficename.md)            | Нет     | **Organizational-Person**                                             |
| [**Снимки**](a-thumbnailphoto.md)                                              | Нет     | **Organizational-Person**                                             |
| [**Возможно — подстрочные**](a-possibleinferiors.md)                                | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Почтовый адрес**](a-postaladdress.md)                                        | Нет     | **Organizational-Person**                                             |
| [**Почтовый код**](a-postalcode.md)                                              | Нет     | **Organizational-Person**                                             |
| [**флажок после Office**](a-postofficebox.md)                                       | Нет     | **Organizational-Person**                                             |
| [**Предпочтительный метод доставки**](a-preferreddeliverymethod.md)                   | Нет     | **Organizational-Person**                                             |
| [**Прокси-объект-имя**](a-proxiedobjectname.md)                               | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Прокси-адреса**](a-proxyaddresses.md)                                      | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Запрос — политика — BL**](a-querypolicybl.md)                                       | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**RDN**](a-name.md)                                                            | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Зарегистрированный адрес**](a-registeredaddress.md)                                | Нет     | **Organizational-Person**                                             |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                        | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**REPL-Уптодате-Vector**](a-repluptodatevector.md)                             | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Отчеты**](a-directreports.md)                                               | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Представители — от**](a-repsfrom.md)                                                  | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Представители — кому**](a-repsto.md)                                                      | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Редакции**](a-revision.md)                                                   | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**SD-Rights-эффективен**](a-sdrightseffective.md)                               | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**См. также**](a-seealso.md)                                                    | Нет     | [**Человек**](c-person.md)<br/>                                 |
| [**Серийный номер**](a-serialnumber.md)                                          | Нет     | [**Человек**](c-person.md)<br/>                                 |
| [**Server-Reference-BL**](a-serverreferencebl.md)                               | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**"Показать" — "Расширенный просмотр"**](a-showinadvancedviewonly.md)                   | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Site-Object-BL**](a-siteobjectbl.md)                                         | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**State-или-провинция-Name**](a-st.md)                                           | Нет     | **Organizational-Person**                                             |
| [**Улица-адрес**](a-street.md)                                               | Нет     | **Organizational-Person**                                             |
| [**Структурный объектный класс**](a-structuralobjectclass.md)                       | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Подразделы-ReFS**](a-subrefs.md)                                                    | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**субсчемасубентри**](a-subschemasubentry.md)                                 | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Образование**](a-sn.md)                                                          | Нет     | [**Человек**](c-person.md)<br/>                                 |
| [**Системные флаги**](a-systemflags.md)                                            | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Номер телефона**](a-telephonenumber.md)                                    | Нет     | [**Человек**](c-person.md)<br/>                                 |
| [**Teletex — идентификатор терминала**](a-teletexterminalidentifier.md)               | Нет     | **Organizational-Person**                                             |
| [**Номер телекса**](a-telexnumber.md)                                            | Нет     | **Organizational-Person**                                             |
| [**Номер телекса (первичный)**](a-primarytelexnumber.md)                                    | Нет     | **Organizational-Person**                                             |
| [**Текст — страна**](a-co.md)                                                     | Нет     | **Organizational-Person**                                             |
| [**Название**](a-title.md)                                                         | Нет     | **Organizational-Person**                                             |
| [**Комментарий пользователя**](a-comment.md)                                                | Нет     | **Organizational-Person**                                             |
| [**Пароль пользователя**](a-userpassword.md)                                          | Нет     | [**Человек**](c-person.md)<br/>                                 |
| [**USN-изменено**](a-usnchanged.md)                                              | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Созданный USN**](a-usncreated.md)                                              | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**USN-DSA-Last-obj-removed**](a-usndsalastobjremoved.md)                       | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**USN — межсайтовая**](a-usnintersite.md)                                          | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                      | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Источник USN**](a-usnsource.md)                                                | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**WBEM — путь**](a-wbempath.md)                                                  | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Хорошо известные объекты**](a-wellknownobjects.md)                                 | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**При изменении**](a-whenchanged.md)                                            | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**При создании**](a-whencreated.md)                                            | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**WWW — Главная страница**](a-wwwhomepage.md)                                           | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**WWW-Page — другие**](a-url.md)                                                  | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**X121 — адрес**](a-x121address.md)                                            | Нет     | **Organizational-Person**                                             |



## <a name="windows-server-2012"></a>Windows Server 2012

-   [Атрибуты](#windows-server-2012-attributes)



| Ввод | Значение |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Нет                                                                                                                     |
| Object-Category             | 0                                                                                                                         |
| По умолчанию — объект — Категория     | [**Человек**](c-person.md)<br/>                                                                                     |
| Governs-Id                  | 2.5.6.7                                                                                                                   |
| По умолчанию-скрытие значения        | 1                                                                                                                         |
| RDN-Атри-ID                  | [**Common-Name**](a-cn.md)<br/>                                                                                    |
| Подкласс                 | [**Человек**](c-person.md)<br/>                                                                                     |
| Возможные старшие          | [](c-container.md)[](c-organization.md)[**Организационная единица**](c-organizationalunit.md) Организации контейнера |
| Вспомогательные классы           | \-                                                                                                                        |
| NT-Security-дескриптор      | О:БАГ: BAD: S:                                                                                                              |
| Дескриптор безопасности по умолчанию | D: (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;;D А) (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;; SY) (A;; РПЛКЛОРК;;; СЛУЖБЫ                              |
| System-Flags                | 0x00000010                                                                                                                |



## <a name="windows-server-2012-attributes"></a>Windows Server 2012 Атрибута

Этот класс содержит следующие атрибуты для Windows Server 2012:



| attribute                                                                                              | Обязательный | Унаследован от                                                          |
|--------------------------------------------------------------------------------------------------------|-----------|-----------------------------------------------------------------------|
| [**Адрес**](a-streetaddress.md)                                                                     | Нет     | **Organizational-Person**                                             |
| [**Адрес — Домашняя страница**](a-homepostaladdress.md)                                                            | Нет     | **Organizational-Person**                                             |
| [**Описание администратора**](a-admindescription.md)                                                        | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Имя администратора-отображение**](a-admindisplayname.md)                                                       | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Allowed-Attributes**](a-allowedattributes.md)                                                      | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Allowed-Attributes-эффективен**](a-allowedattributeseffective.md)                                   | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Allowed-Child-classes**](a-allowedchildclasses.md)                                                 | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Allowed-Child-classes-эффективен**](a-allowedchildclasseseffective.md)                              | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Средство**](a-assistant.md)                                                                       | Нет     | **Organizational-Person**                                             |
| [**аттрибутецертификатеаттрибуте**](a-attributecertificateattribute.md)                               | Нет     | [**Человек**](c-person.md)<br/>                                 |
| [**Плацдарм-Server-List-BL**](a-bridgeheadserverlistbl.md)                                          | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Каноническое имя**](a-canonicalname.md)                                                              | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Common-Name**](a-cn.md)                                                                            | Верно      | [**Человек**](c-person.md)<br/> [**Вверх**](c-top.md)<br/> |
| [**Company**](a-company.md)                                                                           | Нет     | **Organizational-Person**                                             |
| [**Код страны**](a-countrycode.md)                                                                  | Нет     | **Organizational-Person**                                             |
| [**Название страны**](a-c.md)                                                                            | Нет     | **Organizational-Person**                                             |
| [**Метка времени создания**](a-createtimestamp.md)                                                         | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Отдел**](a-department.md)                                                                     | Нет     | **Organizational-Person**                                             |
| [**Описание**](a-description.md)                                                                   | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Целевой индикатор**](a-destinationindicator.md)                                                | Нет     | **Organizational-Person**                                             |
| [**Отображаемое имя**](a-displayname.md)                                                                  | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Отображаемое имя — печатаемое**](a-displaynameprintable.md)                                               | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Отдел**](a-division.md)                                                                         | Нет     | **Organizational-Person**                                             |
| [**DSA-Signature**](a-dsasignature.md)                                                                | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**DS-Core-распространение-данные**](a-dscorepropagationdata.md)                                            | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Адреса электронной почты**](a-mail.md)                                                                     | Нет     | **Organizational-Person**                                             |
| [**Идентификатор сотрудника**](a-employeeid.md)                                                                    | Нет     | **Organizational-Person**                                             |
| [**Имя расширения**](a-extensionname.md)                                                              | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Факс-телефон — номер**](a-facsimiletelephonenumber.md)                                       | Нет     | **Organizational-Person**                                             |
| [**Метки**](a-flags.md)                                                                               | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Из записи**](a-fromentry.md)                                                                      | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                                          | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                                              | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                                             | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Квалификатор поколения**](a-generationqualifier.md)                                                  | Нет     | **Organizational-Person**                                             |
| [**Заданное имя**](a-givenname.md)                                                                      | Нет     | **Organizational-Person**                                             |
| [**хаусеидентифиер**](a-houseidentifier.md)                                                           | Нет     | **Organizational-Person**                                             |
| [**Инициалы**](a-initials.md)                                                                         | Нет     | **Organizational-Person**                                             |
| [**Тип экземпляра**](a-instancetype.md)                                                                | Верно      | [**Вверх**](c-top.md)<br/>                                       |
| [**Международный-ISDN-номер**](a-internationalisdnnumber.md)                                         | Нет     | **Organizational-Person**                                             |
| [**Является критически важным — системный объект**](a-iscriticalsystemobject.md)                                          | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Удалено**](a-isdeleted.md)                                                                      | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Входит в состав списка рассылки**](a-memberof.md)                                                                  | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Имеет права владельца**](a-isprivilegeholder.md)                                                     | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Является перезапущенным**](a-isrecycled.md)                                                                    | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Последний-известный-родительский**](a-lastknownparent.md)                                                         | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Локальное имя**](a-l.md)                                                                           | Нет     | **Organizational-Person**                                             |
| [**Эмблема**](a-thumbnaillogo.md)                                                                        | Нет     | **Organizational-Person**                                             |
| [**Управляемые объекты**](a-managedobjects.md)                                                            | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Manager**](a-manager.md)                                                                           | Нет     | **Organizational-Person**                                             |
| [**В основном**](a-masteredby.md)                                                                    | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**МХС-или-Address**](a-mhsoraddress.md)                                                               | Нет     | **Organizational-Person**                                             |
| [**Метка времени изменения**](a-modifytimestamp.md)                                                         | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-COM-Партитионсетлинк**](a-mscom-partitionsetlink.md)                                            | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-COM-Усерлинк**](a-mscom-userlink.md)                                                            | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DFSR-Компутерреференцебл**](a-msdfsr-computerreferencebl.md)                                    | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DFSR-Мемберреференцебл**](a-msdfsr-memberreferencebl.md)                                        | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-Allowed-to-"Active-on-чужое удостоверение"**](a-msds-allowedtoactonbehalfofotheridentity.md) | Нет     | **Organizational-Person**                                             |
| [**MS-DS-Allowed-to-Delegate-to**](a-msds-allowedtodelegateto.md)                                     | Нет     | **Organizational-Person**                                             |
| [**MS-DS-примерно-Иммед-подчиненные**](a-msds-approx-immed-subordinates.md)                            | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-Аусентикатедто-Аккаунтлист**](a-msds-authenticatedtoaccountlist.md)                         | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-ClaimSet-shares-возможные значения-with-BL**](a-msds-claimsharespossiblevalueswithbl.md)           | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-целостность-дочерняя — количество**](a-ms-ds-consistencychildcount.md)                                 | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-Consistencу-Guid**](a-ms-ds-consistencyguid.md)                                              | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Поддержка MS-DS-Feature-BL**](a-msds-enabledfeaturebl.md)                                            | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-ИЕРАРХИя — старший стаж — индекс**](a-msds-habseniorityindex.md)                                          | Нет     | **Organizational-Person**                                             |
| [**MS-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)                                   | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS--домен — для**](a-msds-isdomainfor.md)                                                      | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-является-Full-реплика для**](a-msds-isfullreplicafor.md)                                           | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-является-partial-реплика для**](a-msds-ispartialreplicafor.md)                                     | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-является-PRIMARY-Computer-для**](a-msds-isprimarycomputerfor.md)                                   | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                                    | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                                                    | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-локально-эффективное удаление — время**](a-msds-localeffectivedeletiontime.md)                       | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-Local-эффективен — время перезапуска**](a-msds-localeffectiverecycletime.md)                         | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-Masterd-by**](a-msds-masteredby.md)                                                         | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)                                      | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-Members-of-Resource-Property-List-BL**](a-msds-membersofresourcepropertylistbl.md)           | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-NC-REPL-курсоры**](a-msds-ncreplcursors.md)                                                  | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-NC-REPL-Inbound-соседи**](a-msds-ncreplinboundneighbors.md)                               | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-NC-REPL-Outbound-соседи**](a-msds-ncreploutboundneighbors.md)                             | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)                          | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-NC-Type**](a-msds-nctype.md)                                                                 | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-не-Members-BL**](a-msds-nonmembersbl.md)                                                    | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                                          | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-Оидтограуп-Link-BL**](a-msds-oidtogrouplinkbl.md)                                            | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-Operations-для-AZ-Role-BL**](a-msds-operationsforazrolebl.md)                                | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)                                | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-Фонетическое название компании**](a-msds-phoneticcompanyname.md)                                      | Нет     | **Organizational-Person**                                             |
| [**MS-DS-фонетический отдел**](a-msds-phoneticdepartment.md)                                         | Нет     | **Organizational-Person**                                             |
| [**MS-DS-фонетическо-отображаемое имя**](a-msds-phoneticdisplayname.md)                                      | Нет     | **Organizational-Person**                                             |
| [**MS-DS-фонетическо-First-Name**](a-msds-phoneticfirstname.md)                                          | Нет     | **Organizational-Person**                                             |
| [**MS-DS-фонетическое имя (фамилия)**](a-msds-phoneticlastname.md)                                            | Нет     | **Organizational-Person**                                             |
| [**MS-DS-Principal-Name**](a-msds-principalname.md)                                                   | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-PSO — применяется**](a-msds-psoapplied.md)                                                         | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-REPL-Attribute-Meta-Data**](a-msds-replattributemetadata.md)                                 | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)                                         | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-выявил-DSA**](a-msds-revealeddsas.md)                                                     | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-выводит-List-BL**](a-msds-revealedlistbl.md)                                                | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-Tasks-для-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                                          | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                                          | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**ms-DS-TDO-Egress-BL**](a-msds-tdoegressbl.md)                                                      | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-TDO-входящий трафик — BL**](a-msds-tdoingressbl.md)                                                    | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-DS-value-type-Reference-BL**](a-msds-valuetypereferencebl.md)                                   | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**MS-дов-House-identifier**](a-msexchhouseidentifier.md)                                            | Нет     | **Organizational-Person**                                             |
| [**MS-дов-Owner-BL**](a-ownerbl.md)                                                                  | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Мссфу-30-POSIX-член-of**](a-mssfu30posixmemberof.md)                                             | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**нетбут-SCP-BL**](a-netbootscpbl.md)                                                               | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Не-Security-Member-BL**](a-nonsecuritymemberbl.md)                                                | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**NT-Security-дескриптор**](a-ntsecuritydescriptor.md)                                               | Верно      | [**Вверх**](c-top.md)<br/>                                       |
| [**Obj-расп-имя**](a-distinguishedname.md)                                                           | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Объект — Категория**](a-objectcategory.md)                                                            | Верно      | [**Вверх**](c-top.md)<br/>                                       |
| [**Объектный класс**](a-objectclass.md)                                                                  | Верно      | [**Вверх**](c-top.md)<br/>                                       |
| [**Объект — GUID**](a-objectguid.md)                                                                    | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Версия объекта**](a-objectversion.md)                                                              | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Организация — имя подразделения**](a-ou.md)                                                               | Нет     | **Organizational-Person**                                             |
| [**Название организации**](a-o.md)                                                                       | Нет     | **Organizational-Person**                                             |
| [**Другие — почтовый ящик**](a-othermailbox.md)                                                                | Нет     | **Organizational-Person**                                             |
| [**Другое имя**](a-middlename.md)                                                                     | Нет     | **Organizational-Person**                                             |
| [**Другие хорошо известные объекты**](a-otherwellknownobjects.md)                                            | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Разделяемый атрибут-удаление-список**](a-partialattributedeletionlist.md)                              | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Разделяемый атрибут-set**](a-partialattributeset.md)                                                 | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Личный заголовок**](a-personaltitle.md)                                                              | Нет     | **Organizational-Person**                                             |
| [**Телефон-Fax — другие**](a-otherfacsimiletelephonenumber.md)                                             | Нет     | **Organizational-Person**                                             |
| [**Телефон-Home — другие**](a-otherhomephone.md)                                                           | Нет     | **Organizational-Person**                                             |
| [**Телефон-Home — основной**](a-homephone.md)                                                              | Нет     | **Organizational-Person**                                             |
| [**Телефон-Ip — другие**](a-otheripphone.md)                                                               | Нет     | **Organizational-Person**                                             |
| [**Телефон-Ip-Primary**](a-ipphone.md)                                                                  | Нет     | **Organizational-Person**                                             |
| [**Телефон-ISDN-Primary**](a-primaryinternationalisdnnumber.md)                                         | Нет     | **Organizational-Person**                                             |
| [**Телефон-Mobile — другие**](a-othermobile.md)                                                            | Нет     | **Organizational-Person**                                             |
| [**Телефон — Mobile — Primary**](a-mobile.md)                                                               | Нет     | **Organizational-Person**                                             |
| [**Телефон-Office-Other**](a-othertelephone.md)                                                         | Нет     | **Organizational-Person**                                             |
| [**Телефон-пейджер — другие**](a-otherpager.md)                                                              | Нет     | **Organizational-Person**                                             |
| [**Телефон-пейджер-основной**](a-pager.md)                                                                 | Нет     | **Organizational-Person**                                             |
| [**физическая доставка — Office-имя**](a-physicaldeliveryofficename.md)                                  | Нет     | **Organizational-Person**                                             |
| [**Снимки**](a-thumbnailphoto.md)                                                                    | Нет     | **Organizational-Person**                                             |
| [**Возможно — подстрочные**](a-possibleinferiors.md)                                                      | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Почтовый адрес**](a-postaladdress.md)                                                              | Нет     | **Organizational-Person**                                             |
| [**Почтовый код**](a-postalcode.md)                                                                    | Нет     | **Organizational-Person**                                             |
| [**флажок после Office**](a-postofficebox.md)                                                             | Нет     | **Organizational-Person**                                             |
| [**Предпочтительный метод доставки**](a-preferreddeliverymethod.md)                                         | Нет     | **Organizational-Person**                                             |
| [**Прокси-объект-имя**](a-proxiedobjectname.md)                                                     | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Прокси-адреса**](a-proxyaddresses.md)                                                            | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Запрос — политика — BL**](a-querypolicybl.md)                                                             | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**RDN**](a-name.md)                                                                                  | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Зарегистрированный адрес**](a-registeredaddress.md)                                                      | Нет     | **Organizational-Person**                                             |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                                              | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**REPL-Уптодате-Vector**](a-repluptodatevector.md)                                                   | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Отчеты**](a-directreports.md)                                                                     | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Представители — от**](a-repsfrom.md)                                                                        | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Представители — кому**](a-repsto.md)                                                                            | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Редакции**](a-revision.md)                                                                         | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**SD-Rights-эффективен**](a-sdrightseffective.md)                                                     | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**См. также**](a-seealso.md)                                                                          | Нет     | [**Человек**](c-person.md)<br/>                                 |
| [**Серийный номер**](a-serialnumber.md)                                                                | Нет     | [**Человек**](c-person.md)<br/>                                 |
| [**Server-Reference-BL**](a-serverreferencebl.md)                                                     | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**"Показать" — "Расширенный просмотр"**](a-showinadvancedviewonly.md)                                         | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                               | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**State-или-провинция-Name**](a-st.md)                                                                 | Нет     | **Organizational-Person**                                             |
| [**Улица-адрес**](a-street.md)                                                                     | Нет     | **Organizational-Person**                                             |
| [**Структурный объектный класс**](a-structuralobjectclass.md)                                             | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Подразделы-ReFS**](a-subrefs.md)                                                                          | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**субсчемасубентри**](a-subschemasubentry.md)                                                       | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Образование**](a-sn.md)                                                                                | Нет     | [**Человек**](c-person.md)<br/>                                 |
| [**Системные флаги**](a-systemflags.md)                                                                  | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Номер телефона**](a-telephonenumber.md)                                                          | Нет     | [**Человек**](c-person.md)<br/>                                 |
| [**Teletex — идентификатор терминала**](a-teletexterminalidentifier.md)                                     | Нет     | **Organizational-Person**                                             |
| [**Номер телекса**](a-telexnumber.md)                                                                  | Нет     | **Organizational-Person**                                             |
| [**Номер телекса (первичный)**](a-primarytelexnumber.md)                                                          | Нет     | **Organizational-Person**                                             |
| [**Текст — страна**](a-co.md)                                                                           | Нет     | **Organizational-Person**                                             |
| [**Название**](a-title.md)                                                                               | Нет     | **Organizational-Person**                                             |
| [**Комментарий пользователя**](a-comment.md)                                                                      | Нет     | **Organizational-Person**                                             |
| [**Пароль пользователя**](a-userpassword.md)                                                                | Нет     | [**Человек**](c-person.md)<br/>                                 |
| [**USN-изменено**](a-usnchanged.md)                                                                    | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Созданный USN**](a-usncreated.md)                                                                    | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**USN-DSA-Last-obj-removed**](a-usndsalastobjremoved.md)                                             | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**USN — межсайтовая**](a-usnintersite.md)                                                                | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                                            | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Источник USN**](a-usnsource.md)                                                                      | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**WBEM — путь**](a-wbempath.md)                                                                        | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**Хорошо известные объекты**](a-wellknownobjects.md)                                                       | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**При изменении**](a-whenchanged.md)                                                                  | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**При создании**](a-whencreated.md)                                                                  | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**WWW — Главная страница**](a-wwwhomepage.md)                                                                 | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**WWW-Page — другие**](a-url.md)                                                                        | Нет     | [**Вверх**](c-top.md)<br/>                                       |
| [**X121 — адрес**](a-x121address.md)                                                                  | Нет     | **Organizational-Person**                                             |



 

 





