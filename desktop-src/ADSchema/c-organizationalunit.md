---
title: Класс Organizational-Unit
description: Контейнер для хранения пользователей, компьютеров и других объектов учетной записи.
ms.assetid: a5a99dc7-9000-478c-9545-473cfb6ddf6c
ms.tgt_platform: multiple
keywords:
- Схема AD Organizational-Unit класса
- Схема AD класса organizationalUnit
topic_type:
- apiref
api_name:
- Organizational-Unit
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79807cc71f5e7690aca04b80f0d5560399b8b5415fc1d7f3cf9654884b7b9c1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120065294"
---
# <a name="organizational-unit-class"></a>Класс Organizational-Unit

Контейнер для хранения пользователей, компьютеров и других объектов учетной записи.



| Ввод | Значение |
|-------------------|--------------------------------------|
| CN                | Organizational-Unit                  |
| LDAP-отображаемое имя | organizationalUnit                   |
| Привилегия обновления  | Кто угодно может обновить этот объект.       |
| Частота обновления  | \-                                   |
| Schema-ID-GUID    | bf967aa5-0de6-11d0-a285-00aa003049e2 |



## <a name="implementations"></a>Варианты реализации решения

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**ADAM**](#adam-attributes)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server

-   [Атрибуты](#windows-2000-server-attributes)



| Ввод | Значение |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Неверно                                                                                                                                                                                                                                                                                                    |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                        |
| По умолчанию — объект — Категория     | \-                                                                                                                                                                                                                                                                                                       |
| Governs-Id                  | 2.5.6.5                                                                                                                                                                                                                                                                                                  |
| По умолчанию-скрытие значения        | 0                                                                                                                                                                                                                                                                                                        |
| RDN-Атри-ID                  | [**Организация — имя подразделения**](a-ou.md)<br/>                                                                                                                                                                                                                                                      |
| Подкласс                 | [**Вверх**](c-top.md)<br/>                                                                                                                                                                                                                                                                          |
| Возможные старшие          | [**Домен —**](c-domaindns.md)[**Организация**](c-organization.md) подразделения DNS                                                                                                                                                                                                           |
| Вспомогательные классы           | \-                                                                                                                                                                                                                                                                                                       |
| NT-Security-дескриптор      | О:БАГ: BAD: S:                                                                                                                                                                                                                                                                                             |
| Дескриптор безопасности по умолчанию | D: (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;; SY) (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;;D A) (OA;; ККДК; bf967a86-0de6-11D0-a285-00aa003049e2;; AO) (OA;; ККДК; bf967aba-0de6-11D0-a285-00aa003049e2;; AO) (OA;; ККДК; bf967a9c-0de6-11D0-a285-00aa003049e2;; AO) (OA;; ККДК; bf967aa8-0de6-11D0-a285-00aa003049e2;; ЗП) (A;; РПЛКЛОРК;;; СЛУЖБЫ |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                               |



## <a name="windows-2000-server-attributes"></a>атрибуты сервера Windows 2000

этот класс содержит следующие атрибуты для сервера Windows 2000:



| attribute                                                                 | Обязательный | Унаследован от                    |
|---------------------------------------------------------------------------|-----------|---------------------------------|
| [**Описание администратора**](a-admindescription.md)                           | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Имя администратора-отображение**](a-admindisplayname.md)                          | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Allowed-Attributes**](a-allowedattributes.md)                         | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Allowed-Attributes-эффективен**](a-allowedattributeseffective.md)      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Allowed-Child-classes**](a-allowedchildclasses.md)                    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Allowed-Child-classes-эффективен**](a-allowedchildclasseseffective.md) | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Плацдарм-Server-List-BL**](a-bridgeheadserverlistbl.md)             | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Бизнес — Категория**](a-businesscategory.md)                           | Неверно     | **Организационная единица**         |
| [**Каноническое имя**](a-canonicalname.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Common-Name**](a-cn.md)                                               | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Код страны**](a-countrycode.md)                                     | Неверно     | **Организационная единица**         |
| [**Название страны**](a-c.md)                                               | Неверно     | **Организационная единица**         |
| [**Метка времени создания**](a-createtimestamp.md)                            | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Группа по умолчанию**](a-defaultgroup.md)                                   | Неверно     | **Организационная единица**         |
| [**Описание**](a-description.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Рабочий стол — профиль**](a-desktopprofile.md)                               | Неверно     | **Организационная единица**         |
| [**Целевой индикатор**](a-destinationindicator.md)                   | Неверно     | **Организационная единица**         |
| [**Отображаемое имя**](a-displayname.md)                                     | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Отображаемое имя — печатаемое**](a-displaynameprintable.md)                  | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**DSA-Signature**](a-dsasignature.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**DS-Core-распространение-данные**](a-dscorepropagationdata.md)               | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Имя расширения**](a-extensionname.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Факс-телефон — номер**](a-facsimiletelephonenumber.md)          | Неверно     | **Организационная единица**         |
| [**Метки**](a-flags.md)                                                  | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Из записи**](a-fromentry.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)             | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**GP — ссылка**](a-gplink.md)                                               | Неверно     | **Организационная единица**         |
| [**GP — параметры**](a-gpoptions.md)                                         | Неверно     | **Организационная единица**         |
| [**Тип экземпляра**](a-instancetype.md)                                   | Верно      | [**Вверх**](c-top.md)<br/> |
| [**Международный-ISDN-номер**](a-internationalisdnnumber.md)            | Неверно     | **Организационная единица**         |
| [**Является критически важным — системный объект**](a-iscriticalsystemobject.md)             | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Удалено**](a-isdeleted.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Входит в состав списка рассылки**](a-memberof.md)                                     | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Имеет права владельца**](a-isprivilegeholder.md)                        | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Последний-известный-родительский**](a-lastknownparent.md)                            | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Локальное имя**](a-l.md)                                              | Неверно     | **Организационная единица**         |
| [**Эмблема**](a-thumbnaillogo.md)                                           | Неверно     | **Организационная единица**         |
| [**Под управлением**](a-managedby.md)                                         | Неверно     | **Организационная единица**         |
| [**Управляемые объекты**](a-managedobjects.md)                               | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**В основном**](a-masteredby.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Метка времени изменения**](a-modifytimestamp.md)                            | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-целостность-дочерняя — количество**](a-ms-ds-consistencychildcount.md)    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Consistencу-Guid**](a-ms-ds-consistencyguid.md)                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**нетбут-SCP-BL**](a-netbootscpbl.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Не-Security-Member-BL**](a-nonsecuritymemberbl.md)                   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**NT-Security-дескриптор**](a-ntsecuritydescriptor.md)                  | Верно      | [**Вверх**](c-top.md)<br/> |
| [**Obj-расп-имя**](a-distinguishedname.md)                              | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Объект — Категория**](a-objectcategory.md)                               | Верно      | [**Вверх**](c-top.md)<br/> |
| [**Объектный класс**](a-objectclass.md)                                     | Верно      | [**Вверх**](c-top.md)<br/> |
| [**Объект — GUID**](a-objectguid.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Версия объекта**](a-objectversion.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Организация — имя подразделения**](a-ou.md)                                  | Верно      | **Организационная единица**         |
| [**Другие хорошо известные объекты**](a-otherwellknownobjects.md)               | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Разделяемый атрибут-удаление-список**](a-partialattributedeletionlist.md) | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Разделяемый атрибут-set**](a-partialattributeset.md)                    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**физическая доставка — Office-имя**](a-physicaldeliveryofficename.md)     | Неверно     | **Организационная единица**         |
| [**Возможно — подстрочные**](a-possibleinferiors.md)                         | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Почтовый адрес**](a-postaladdress.md)                                 | Неверно     | **Организационная единица**         |
| [**Почтовый код**](a-postalcode.md)                                       | Неверно     | **Организационная единица**         |
| [**флажок после Office**](a-postofficebox.md)                                | Неверно     | **Организационная единица**         |
| [**Предпочтительный метод доставки**](a-preferreddeliverymethod.md)            | Неверно     | **Организационная единица**         |
| [**Прокси-объект-имя**](a-proxiedobjectname.md)                        | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Прокси-адреса**](a-proxyaddresses.md)                               | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Запрос — политика — BL**](a-querypolicybl.md)                                | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**RDN**](a-name.md)                                                     | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Зарегистрированный адрес**](a-registeredaddress.md)                         | Неверно     | **Организационная единица**         |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**REPL-Уптодате-Vector**](a-repluptodatevector.md)                      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Отчеты**](a-directreports.md)                                        | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Представители — от**](a-repsfrom.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Представители — кому**](a-repsto.md)                                               | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Редакции**](a-revision.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**SD-Rights-эффективен**](a-sdrightseffective.md)                        | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Поиск — Обзор**](a-searchguide.md)                                     | Неверно     | **Организационная единица**         |
| [**См. также**](a-seealso.md)                                             | Неверно     | **Организационная единица**         |
| [**Server-Reference-BL**](a-serverreferencebl.md)                        | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**"Показать" — "Расширенный просмотр"**](a-showinadvancedviewonly.md)            | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Site-Object-BL**](a-siteobjectbl.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**State-или-провинция-Name**](a-st.md)                                    | Неверно     | **Организационная единица**         |
| [**Улица-адрес**](a-street.md)                                        | Неверно     | **Организационная единица**         |
| [**Подразделы-ReFS**](a-subrefs.md)                                             | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**субсчемасубентри**](a-subschemasubentry.md)                          | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Системные флаги**](a-systemflags.md)                                     | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Номер телефона**](a-telephonenumber.md)                             | Неверно     | **Организационная единица**         |
| [**Teletex — идентификатор терминала**](a-teletexterminalidentifier.md)        | Неверно     | **Организационная единица**         |
| [**Номер телекса**](a-telexnumber.md)                                     | Неверно     | **Организационная единица**         |
| [**Текст — страна**](a-co.md)                                              | Неверно     | **Организационная единица**         |
| [**UPN-суффиксы**](a-upnsuffixes.md)                                     | Неверно     | **Организационная единица**         |
| [**Пароль пользователя**](a-userpassword.md)                                   | Неверно     | **Организационная единица**         |
| [**USN-изменено**](a-usnchanged.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Созданный USN**](a-usncreated.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**USN-DSA-Last-obj-removed**](a-usndsalastobjremoved.md)                | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**USN — межсайтовая**](a-usnintersite.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                               | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Источник USN**](a-usnsource.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**WBEM — путь**](a-wbempath.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Хорошо известные объекты**](a-wellknownobjects.md)                          | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**При изменении**](a-whenchanged.md)                                     | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**При создании**](a-whencreated.md)                                     | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**WWW — Главная страница**](a-wwwhomepage.md)                                    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**WWW-Page — другие**](a-url.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**X121 — адрес**](a-x121address.md)                                     | Неверно     | **Организационная единица**         |



## <a name="windows-server-2003"></a>Windows Server 2003

-   [Атрибуты](#windows-server-2003-attributes)
-   [Расширенные права](#windows-server-2003-extended-rights)



| Ввод | Значение |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Неверно                                                                                                                                                                                                                                                                                                                                                                         |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                                                                                             |
| По умолчанию — объект — Категория     | \-                                                                                                                                                                                                                                                                                                                                                                            |
| Governs-Id                  | 2.5.6.5                                                                                                                                                                                                                                                                                                                                                                       |
| По умолчанию-скрытие значения        | 0                                                                                                                                                                                                                                                                                                                                                                             |
| RDN-Атри-ID                  | [**Организация — имя подразделения**](a-ou.md)<br/>                                                                                                                                                                                                                                                                                                                           |
| Подкласс                 | [**Вверх**](c-top.md)<br/>                                                                                                                                                                                                                                                                                                                                               |
| Возможные старшие          | [**Домен —**](c-domaindns.md)[**страна**](c-country.md) [**Организации**](c-organization.md)**подразделений** DNS                                                                                                                                                                                                                                                    |
| Вспомогательные классы           | \-                                                                                                                                                                                                                                                                                                                                                                            |
| NT-Security-дескриптор      | О:БАГ: BAD: S:                                                                                                                                                                                                                                                                                                                                                                  |
| Дескриптор безопасности по умолчанию | D: (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;; SY) (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;;D A) (OA;; ККДК; bf967a86-0de6-11D0-a285-00aa003049e2;; AO) (OA;; ККДК; bf967aba-0de6-11D0-a285-00aa003049e2;; AO) (OA;; ККДК; bf967a9c-0de6-11D0-a285-00aa003049e2;; AO) (OA;; ККДК; bf967aa8-0de6-11D0-a285-00aa003049e2;; ЗП) (A;; РПЛКЛОРК;;; AU) (A;; ЛКРПЛОРК;;; ED) (OA;; ККДК; 4828CC14-1437-45bc-9B07-AD6F015E5F28;; AO |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                                                                                    |



## <a name="windows-server-2003-attributes"></a>Windows Атрибуты сервера 2003

этот класс содержит следующие атрибуты для Windows Server 2003:



| attribute                                                                   | Обязательный | Унаследован от                    |
|-----------------------------------------------------------------------------|-----------|---------------------------------|
| [**Описание администратора**](a-admindescription.md)                             | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Имя администратора-отображение**](a-admindisplayname.md)                            | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Allowed-Attributes**](a-allowedattributes.md)                           | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Allowed-Attributes-эффективен**](a-allowedattributeseffective.md)        | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Allowed-Child-classes**](a-allowedchildclasses.md)                      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Allowed-Child-classes-эффективен**](a-allowedchildclasseseffective.md)   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Плацдарм-Server-List-BL**](a-bridgeheadserverlistbl.md)               | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Бизнес — Категория**](a-businesscategory.md)                             | Неверно     | **Организационная единица**         |
| [**Каноническое имя**](a-canonicalname.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Common-Name**](a-cn.md)                                                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Код страны**](a-countrycode.md)                                       | Неверно     | **Организационная единица**         |
| [**Название страны**](a-c.md)                                                 | Неверно     | **Организационная единица**         |
| [**Метка времени создания**](a-createtimestamp.md)                              | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Группа по умолчанию**](a-defaultgroup.md)                                     | Неверно     | **Организационная единица**         |
| [**Описание**](a-description.md)                                        | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Рабочий стол — профиль**](a-desktopprofile.md)                                 | Неверно     | **Организационная единица**         |
| [**Целевой индикатор**](a-destinationindicator.md)                     | Неверно     | **Организационная единица**         |
| [**Отображаемое имя**](a-displayname.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Отображаемое имя — печатаемое**](a-displaynameprintable.md)                    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**DSA-Signature**](a-dsasignature.md)                                     | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**DS-Core-распространение-данные**](a-dscorepropagationdata.md)                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Имя расширения**](a-extensionname.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Факс-телефон — номер**](a-facsimiletelephonenumber.md)            | Неверно     | **Организационная единица**         |
| [**Метки**](a-flags.md)                                                    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Из записи**](a-fromentry.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**GP — ссылка**](a-gplink.md)                                                 | Неверно     | **Организационная единица**         |
| [**GP — параметры**](a-gpoptions.md)                                           | Неверно     | **Организационная единица**         |
| [**Тип экземпляра**](a-instancetype.md)                                     | Верно      | [**Вверх**](c-top.md)<br/> |
| [**Международный-ISDN-номер**](a-internationalisdnnumber.md)              | Неверно     | **Организационная единица**         |
| [**Является критически важным — системный объект**](a-iscriticalsystemobject.md)               | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Удалено**](a-isdeleted.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Входит в состав списка рассылки**](a-memberof.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Имеет права владельца**](a-isprivilegeholder.md)                          | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Последний-известный-родительский**](a-lastknownparent.md)                              | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Локальное имя**](a-l.md)                                                | Неверно     | **Организационная единица**         |
| [**Эмблема**](a-thumbnaillogo.md)                                             | Неверно     | **Организационная единица**         |
| [**Под управлением**](a-managedby.md)                                           | Неверно     | **Организационная единица**         |
| [**Управляемые объекты**](a-managedobjects.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**В основном**](a-masteredby.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Метка времени изменения**](a-modifytimestamp.md)                              | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-COM-Партитионсетлинк**](a-mscom-partitionsetlink.md)                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-COM-Усерлинк**](a-mscom-userlink.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-COM-Усерпартитионсетлинк**](a-mscom-userpartitionsetlink.md)         | Неверно     | **Организационная единица**         |
| [**MS-DS-примерно-Иммед-подчиненные**](a-msds-approx-immed-subordinates.md) | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-целостность-дочерняя — количество**](a-ms-ds-consistencychildcount.md)      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Consistencу-Guid**](a-ms-ds-consistencyguid.md)                   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Masterd-by**](a-msds-masteredby.md)                              | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)           | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-NC-REPL-курсоры**](a-msds-ncreplcursors.md)                       | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-NC-REPL-Inbound-соседи**](a-msds-ncreplinboundneighbors.md)    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-NC-REPL-Outbound-соседи**](a-msds-ncreploutboundneighbors.md)  | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-не-Members-BL**](a-msds-nonmembersbl.md)                         | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Operations-для-AZ-Role-BL**](a-msds-operationsforazrolebl.md)     | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)     | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-REPL-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)              | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Tasks-для-AZ-Role-BL**](a-msds-tasksforazrolebl.md)               | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)               | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-дов-Owner-BL**](a-ownerbl.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**нетбут-SCP-BL**](a-netbootscpbl.md)                                    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Не-Security-Member-BL**](a-nonsecuritymemberbl.md)                     | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**NT-Security-дескриптор**](a-ntsecuritydescriptor.md)                    | Верно      | [**Вверх**](c-top.md)<br/> |
| [**Obj-расп-имя**](a-distinguishedname.md)                                | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Объект — Категория**](a-objectcategory.md)                                 | Верно      | [**Вверх**](c-top.md)<br/> |
| [**Объектный класс**](a-objectclass.md)                                       | Верно      | [**Вверх**](c-top.md)<br/> |
| [**Объект — GUID**](a-objectguid.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Версия объекта**](a-objectversion.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Организация — имя подразделения**](a-ou.md)                                    | Верно      | **Организационная единица**         |
| [**Другие хорошо известные объекты**](a-otherwellknownobjects.md)                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Разделяемый атрибут-удаление-список**](a-partialattributedeletionlist.md)   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Разделяемый атрибут-set**](a-partialattributeset.md)                      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**физическая доставка — Office-имя**](a-physicaldeliveryofficename.md)       | Неверно     | **Организационная единица**         |
| [**Возможно — подстрочные**](a-possibleinferiors.md)                           | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Почтовый адрес**](a-postaladdress.md)                                   | Неверно     | **Организационная единица**         |
| [**Почтовый код**](a-postalcode.md)                                         | Неверно     | **Организационная единица**         |
| [**флажок после Office**](a-postofficebox.md)                                  | Неверно     | **Организационная единица**         |
| [**Предпочтительный метод доставки**](a-preferreddeliverymethod.md)              | Неверно     | **Организационная единица**         |
| [**Прокси-объект-имя**](a-proxiedobjectname.md)                          | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Прокси-адреса**](a-proxyaddresses.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Запрос — политика — BL**](a-querypolicybl.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**RDN**](a-name.md)                                                       | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Зарегистрированный адрес**](a-registeredaddress.md)                           | Неверно     | **Организационная единица**         |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**REPL-Уптодате-Vector**](a-repluptodatevector.md)                        | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Отчеты**](a-directreports.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Представители — от**](a-repsfrom.md)                                             | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Представители — кому**](a-repsto.md)                                                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Редакции**](a-revision.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**SD-Rights-эффективен**](a-sdrightseffective.md)                          | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Поиск — Обзор**](a-searchguide.md)                                       | Неверно     | **Организационная единица**         |
| [**См. также**](a-seealso.md)                                               | Неверно     | **Организационная единица**         |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**"Показать" — "Расширенный просмотр"**](a-showinadvancedviewonly.md)              | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**State-или-провинция-Name**](a-st.md)                                      | Неверно     | **Организационная единица**         |
| [**Улица-адрес**](a-street.md)                                          | Неверно     | **Организационная единица**         |
| [**Структурный объектный класс**](a-structuralobjectclass.md)                  | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Подразделы-ReFS**](a-subrefs.md)                                               | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**субсчемасубентри**](a-subschemasubentry.md)                            | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Системные флаги**](a-systemflags.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Номер телефона**](a-telephonenumber.md)                               | Неверно     | **Организационная единица**         |
| [**Teletex — идентификатор терминала**](a-teletexterminalidentifier.md)          | Неверно     | **Организационная единица**         |
| [**Номер телекса**](a-telexnumber.md)                                       | Неверно     | **Организационная единица**         |
| [**Текст — страна**](a-co.md)                                                | Неверно     | **Организационная единица**         |
| [**UPN-суффиксы**](a-upnsuffixes.md)                                       | Неверно     | **Организационная единица**         |
| [**Пароль пользователя**](a-userpassword.md)                                     | Неверно     | **Организационная единица**         |
| [**USN-изменено**](a-usnchanged.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Созданный USN**](a-usncreated.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**USN-DSA-Last-obj-removed**](a-usndsalastobjremoved.md)                  | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**USN — межсайтовая**](a-usnintersite.md)                                     | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Источник USN**](a-usnsource.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**WBEM — путь**](a-wbempath.md)                                             | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Хорошо известные объекты**](a-wellknownobjects.md)                            | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**При изменении**](a-whenchanged.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**При создании**](a-whencreated.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**WWW — Главная страница**](a-wwwhomepage.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**WWW-Page — другие**](a-url.md)                                             | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**X121 — адрес**](a-x121address.md)                                       | Неверно     | **Организационная единица**         |



## <a name="windows-server-2003-extended-rights"></a>Windows Расширенные права сервера 2003

этот класс содержит следующие расширенные права для Windows Server 2003:



| Общее имя                                                |
|------------------------------------------------------------|
| [**Создание-RSoP-планирование**](r-generate-rsop-planning.md) |
| [**Generate-RSoP — ведение журнала**](r-generate-rsop-logging.md)   |



## <a name="adam"></a>ADAM

-   [Атрибуты](#adam-attributes)



| Ввод | Значение |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Неверно                                                                                                                      |
| Object-Category             | 1                                                                                                                          |
| По умолчанию — объект — Категория     | \-                                                                                                                         |
| Governs-Id                  | 2.5.6.5                                                                                                                    |
| По умолчанию-скрытие значения        | 0                                                                                                                          |
| RDN-Атри-ID                  | [**Организация — имя подразделения**](a-ou.md)<br/>                                                                        |
| Подкласс                 | [**Вверх**](c-top.md)<br/>                                                                                            |
| Возможные старшие          | [**Домен —**](c-domaindns.md)[**страна**](c-country.md) [**Организации**](c-organization.md)**подразделений** DNS |
| Вспомогательные классы           | \-                                                                                                                         |
| NT-Security-дескриптор      | О:БАГ: BAD: S:                                                                                                               |
| Дескриптор безопасности по умолчанию | Д:С:                                                                                                                       |
| System-Flags                | 0x00000010                                                                                                                 |



## <a name="adam-attributes"></a>Атрибуты ADAM

Этот класс содержит следующие атрибуты для ADAM:



| attribute                                                                   | Обязательный | Унаследован от                    |
|-----------------------------------------------------------------------------|-----------|---------------------------------|
| [**Описание администратора**](a-admindescription.md)                             | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Имя администратора-отображение**](a-admindisplayname.md)                            | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Allowed-Attributes**](a-allowedattributes.md)                           | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Allowed-Attributes-эффективен**](a-allowedattributeseffective.md)        | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Allowed-Child-classes**](a-allowedchildclasses.md)                      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Allowed-Child-classes-эффективен**](a-allowedchildclasseseffective.md)   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Плацдарм-Server-List-BL**](a-bridgeheadserverlistbl.md)               | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Бизнес — Категория**](a-businesscategory.md)                             | Неверно     | **Организационная единица**         |
| [**Каноническое имя**](a-canonicalname.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Common-Name**](a-cn.md)                                                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Код страны**](a-countrycode.md)                                       | Неверно     | **Организационная единица**         |
| [**Название страны**](a-c.md)                                                 | Неверно     | **Организационная единица**         |
| [**Метка времени создания**](a-createtimestamp.md)                              | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Группа по умолчанию**](a-defaultgroup.md)                                     | Неверно     | **Организационная единица**         |
| [**Описание**](a-description.md)                                        | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Рабочий стол — профиль**](a-desktopprofile.md)                                 | Неверно     | **Организационная единица**         |
| [**Целевой индикатор**](a-destinationindicator.md)                     | Неверно     | **Организационная единица**         |
| [**Отображаемое имя**](a-displayname.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**DSA-Signature**](a-dsasignature.md)                                     | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**DS-Core-распространение-данные**](a-dscorepropagationdata.md)                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Факс-телефон — номер**](a-facsimiletelephonenumber.md)            | Неверно     | **Организационная единица**         |
| [**Из записи**](a-fromentry.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Тип экземпляра**](a-instancetype.md)                                     | Верно      | [**Вверх**](c-top.md)<br/> |
| [**Международный-ISDN-номер**](a-internationalisdnnumber.md)              | Неверно     | **Организационная единица**         |
| [**Является критически важным — системный объект**](a-iscriticalsystemobject.md)               | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Удалено**](a-isdeleted.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Входит в состав списка рассылки**](a-memberof.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Последний-известный-родительский**](a-lastknownparent.md)                              | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Локальное имя**](a-l.md)                                                | Неверно     | **Организационная единица**         |
| [**Эмблема**](a-thumbnaillogo.md)                                             | Неверно     | **Организационная единица**         |
| [**Под управлением**](a-managedby.md)                                           | Неверно     | **Организационная единица**         |
| [**Управляемые объекты**](a-managedobjects.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**В основном**](a-masteredby.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Метка времени изменения**](a-modifytimestamp.md)                              | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-примерно-Иммед-подчиненные**](a-msds-approx-immed-subordinates.md) | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-целостность-дочерняя — количество**](a-ms-ds-consistencychildcount.md)      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Consistencу-Guid**](a-ms-ds-consistencyguid.md)                   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Disabled-for-Instances-BL**](a-msds-disableforinstancesbl.md)      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Masterd-by**](a-msds-masteredby.md)                              | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-NC-REPL-курсоры**](a-msds-ncreplcursors.md)                       | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-NC-REPL-Inbound-соседи**](a-msds-ncreplinboundneighbors.md)    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-NC-REPL-Outbound-соседи**](a-msds-ncreploutboundneighbors.md)  | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-REPL-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)              | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Service-Account-BL**](a-msds-serviceaccountbl.md)                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**NT-Security-дескриптор**](a-ntsecuritydescriptor.md)                    | Верно      | [**Вверх**](c-top.md)<br/> |
| [**Obj-расп-имя**](a-distinguishedname.md)                                | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Объект — Категория**](a-objectcategory.md)                                 | Верно      | [**Вверх**](c-top.md)<br/> |
| [**Объектный класс**](a-objectclass.md)                                       | Верно      | [**Вверх**](c-top.md)<br/> |
| [**Объект — GUID**](a-objectguid.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Версия объекта**](a-objectversion.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Организация — имя подразделения**](a-ou.md)                                    | Верно      | **Организационная единица**         |
| [**Другие хорошо известные объекты**](a-otherwellknownobjects.md)                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Разделяемый атрибут-удаление-список**](a-partialattributedeletionlist.md)   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Разделяемый атрибут-set**](a-partialattributeset.md)                      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**физическая доставка — Office-имя**](a-physicaldeliveryofficename.md)       | Неверно     | **Организационная единица**         |
| [**Возможно — подстрочные**](a-possibleinferiors.md)                           | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Почтовый адрес**](a-postaladdress.md)                                   | Неверно     | **Организационная единица**         |
| [**Почтовый код**](a-postalcode.md)                                         | Неверно     | **Организационная единица**         |
| [**флажок после Office**](a-postofficebox.md)                                  | Неверно     | **Организационная единица**         |
| [**Предпочтительный метод доставки**](a-preferreddeliverymethod.md)              | Неверно     | **Организационная единица**         |
| [**Прокси-объект-имя**](a-proxiedobjectname.md)                          | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Прокси-адреса**](a-proxyaddresses.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Запрос — политика — BL**](a-querypolicybl.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**RDN**](a-name.md)                                                       | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Зарегистрированный адрес**](a-registeredaddress.md)                           | Неверно     | **Организационная единица**         |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**REPL-Уптодате-Vector**](a-repluptodatevector.md)                        | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Представители — от**](a-repsfrom.md)                                             | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Представители — кому**](a-repsto.md)                                                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Редакции**](a-revision.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**SD-Rights-эффективен**](a-sdrightseffective.md)                          | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Поиск — Обзор**](a-searchguide.md)                                       | Неверно     | **Организационная единица**         |
| [**См. также**](a-seealso.md)                                               | Неверно     | **Организационная единица**         |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**"Показать" — "Расширенный просмотр"**](a-showinadvancedviewonly.md)              | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**State-или-провинция-Name**](a-st.md)                                      | Неверно     | **Организационная единица**         |
| [**Улица-адрес**](a-street.md)                                          | Неверно     | **Организационная единица**         |
| [**Структурный объектный класс**](a-structuralobjectclass.md)                  | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Подразделы-ReFS**](a-subrefs.md)                                               | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**субсчемасубентри**](a-subschemasubentry.md)                            | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Системные флаги**](a-systemflags.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Номер телефона**](a-telephonenumber.md)                               | Неверно     | **Организационная единица**         |
| [**Teletex — идентификатор терминала**](a-teletexterminalidentifier.md)          | Неверно     | **Организационная единица**         |
| [**Номер телекса**](a-telexnumber.md)                                       | Неверно     | **Организационная единица**         |
| [**Текст — страна**](a-co.md)                                                | Неверно     | **Организационная единица**         |
| [**UPN-суффиксы**](a-upnsuffixes.md)                                       | Неверно     | **Организационная единица**         |
| [**Пароль пользователя**](a-userpassword.md)                                     | Неверно     | **Организационная единица**         |
| [**USN-изменено**](a-usnchanged.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Созданный USN**](a-usncreated.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**USN-DSA-Last-obj-removed**](a-usndsalastobjremoved.md)                  | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**USN — межсайтовая**](a-usnintersite.md)                                     | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Источник USN**](a-usnsource.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**WBEM — путь**](a-wbempath.md)                                             | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Хорошо известные объекты**](a-wellknownobjects.md)                            | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**При изменении**](a-whenchanged.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**При создании**](a-whencreated.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**WWW — Главная страница**](a-wwwhomepage.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**WWW-Page — другие**](a-url.md)                                             | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**X121 — адрес**](a-x121address.md)                                       | Неверно     | **Организационная единица**         |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2

-   [Атрибуты](#windows-server-2003-r2-attributes)
-   [Расширенные права](#windows-server-2003-r2-extended-rights)



| Ввод | Значение |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Неверно                                                                                                                                                                                                                                                                                                                                                                         |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                                                                                             |
| По умолчанию — объект — Категория     | \-                                                                                                                                                                                                                                                                                                                                                                            |
| Governs-Id                  | 2.5.6.5                                                                                                                                                                                                                                                                                                                                                                       |
| По умолчанию-скрытие значения        | 0                                                                                                                                                                                                                                                                                                                                                                             |
| RDN-Атри-ID                  | [**Организация — имя подразделения**](a-ou.md)<br/>                                                                                                                                                                                                                                                                                                                           |
| Подкласс                 | [**Вверх**](c-top.md)<br/>                                                                                                                                                                                                                                                                                                                                               |
| Возможные старшие          | [**Домен —**](c-domaindns.md)[**страна**](c-country.md) [**Организации**](c-organization.md)**подразделений** DNS                                                                                                                                                                                                                                                    |
| Вспомогательные классы           | \-                                                                                                                                                                                                                                                                                                                                                                            |
| NT-Security-дескриптор      | О:БАГ: BAD: S:                                                                                                                                                                                                                                                                                                                                                                  |
| Дескриптор безопасности по умолчанию | D: (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;; SY) (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;;D A) (OA;; ККДК; bf967a86-0de6-11D0-a285-00aa003049e2;; AO) (OA;; ККДК; bf967aba-0de6-11D0-a285-00aa003049e2;; AO) (OA;; ККДК; bf967a9c-0de6-11D0-a285-00aa003049e2;; AO) (OA;; ККДК; bf967aa8-0de6-11D0-a285-00aa003049e2;; ЗП) (A;; РПЛКЛОРК;;; AU) (A;; ЛКРПЛОРК;;; ED) (OA;; ККДК; 4828CC14-1437-45bc-9B07-AD6F015E5F28;; AO |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                                                                                    |



## <a name="windows-server-2003-r2-attributes"></a>Windows Атрибуты сервера 2003 R2

этот класс содержит следующие атрибуты для Windows Server 2003 R2:



| attribute                                                                   | Обязательный | Унаследован от                    |
|-----------------------------------------------------------------------------|-----------|---------------------------------|
| [**Описание администратора**](a-admindescription.md)                             | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Имя администратора-отображение**](a-admindisplayname.md)                            | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Allowed-Attributes**](a-allowedattributes.md)                           | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Allowed-Attributes-эффективен**](a-allowedattributeseffective.md)        | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Allowed-Child-classes**](a-allowedchildclasses.md)                      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Allowed-Child-classes-эффективен**](a-allowedchildclasseseffective.md)   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Плацдарм-Server-List-BL**](a-bridgeheadserverlistbl.md)               | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Бизнес — Категория**](a-businesscategory.md)                             | Неверно     | **Организационная единица**         |
| [**Каноническое имя**](a-canonicalname.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Common-Name**](a-cn.md)                                                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Код страны**](a-countrycode.md)                                       | Неверно     | **Организационная единица**         |
| [**Название страны**](a-c.md)                                                 | Неверно     | **Организационная единица**         |
| [**Метка времени создания**](a-createtimestamp.md)                              | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Группа по умолчанию**](a-defaultgroup.md)                                     | Неверно     | **Организационная единица**         |
| [**Описание**](a-description.md)                                        | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Рабочий стол — профиль**](a-desktopprofile.md)                                 | Неверно     | **Организационная единица**         |
| [**Целевой индикатор**](a-destinationindicator.md)                     | Неверно     | **Организационная единица**         |
| [**Отображаемое имя**](a-displayname.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Отображаемое имя — печатаемое**](a-displaynameprintable.md)                    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**DSA-Signature**](a-dsasignature.md)                                     | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**DS-Core-распространение-данные**](a-dscorepropagationdata.md)                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Имя расширения**](a-extensionname.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Факс-телефон — номер**](a-facsimiletelephonenumber.md)            | Неверно     | **Организационная единица**         |
| [**Метки**](a-flags.md)                                                    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Из записи**](a-fromentry.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**GP — ссылка**](a-gplink.md)                                                 | Неверно     | **Организационная единица**         |
| [**GP — параметры**](a-gpoptions.md)                                           | Неверно     | **Организационная единица**         |
| [**Тип экземпляра**](a-instancetype.md)                                     | Верно      | [**Вверх**](c-top.md)<br/> |
| [**Международный-ISDN-номер**](a-internationalisdnnumber.md)              | Неверно     | **Организационная единица**         |
| [**Является критически важным — системный объект**](a-iscriticalsystemobject.md)               | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Удалено**](a-isdeleted.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Входит в состав списка рассылки**](a-memberof.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Имеет права владельца**](a-isprivilegeholder.md)                          | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Последний-известный-родительский**](a-lastknownparent.md)                              | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Локальное имя**](a-l.md)                                                | Неверно     | **Организационная единица**         |
| [**Эмблема**](a-thumbnaillogo.md)                                             | Неверно     | **Организационная единица**         |
| [**Под управлением**](a-managedby.md)                                           | Неверно     | **Организационная единица**         |
| [**Управляемые объекты**](a-managedobjects.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**В основном**](a-masteredby.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Метка времени изменения**](a-modifytimestamp.md)                              | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-COM-Партитионсетлинк**](a-mscom-partitionsetlink.md)                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-COM-Усерлинк**](a-mscom-userlink.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-COM-Усерпартитионсетлинк**](a-mscom-userpartitionsetlink.md)         | Неверно     | **Организационная единица**         |
| [**MS-DFSR-Компутерреференцебл**](a-msdfsr-computerreferencebl.md)         | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DFSR-Мемберреференцебл**](a-msdfsr-memberreferencebl.md)             | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-примерно-Иммед-подчиненные**](a-msds-approx-immed-subordinates.md) | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-целостность-дочерняя — количество**](a-ms-ds-consistencychildcount.md)      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Consistencу-Guid**](a-ms-ds-consistencyguid.md)                   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Masterd-by**](a-msds-masteredby.md)                              | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)           | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-NC-REPL-курсоры**](a-msds-ncreplcursors.md)                       | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-NC-REPL-Inbound-соседи**](a-msds-ncreplinboundneighbors.md)    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-NC-REPL-Outbound-соседи**](a-msds-ncreploutboundneighbors.md)  | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-не-Members-BL**](a-msds-nonmembersbl.md)                         | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Operations-для-AZ-Role-BL**](a-msds-operationsforazrolebl.md)     | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)     | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-REPL-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)              | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Tasks-для-AZ-Role-BL**](a-msds-tasksforazrolebl.md)               | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)               | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-дов-Owner-BL**](a-ownerbl.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Мссфу-30-POSIX-член-of**](a-mssfu30posixmemberof.md)                  | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**нетбут-SCP-BL**](a-netbootscpbl.md)                                    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Не-Security-Member-BL**](a-nonsecuritymemberbl.md)                     | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**NT-Security-дескриптор**](a-ntsecuritydescriptor.md)                    | Верно      | [**Вверх**](c-top.md)<br/> |
| [**Obj-расп-имя**](a-distinguishedname.md)                                | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Объект — Категория**](a-objectcategory.md)                                 | Верно      | [**Вверх**](c-top.md)<br/> |
| [**Объектный класс**](a-objectclass.md)                                       | Верно      | [**Вверх**](c-top.md)<br/> |
| [**Объект — GUID**](a-objectguid.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Версия объекта**](a-objectversion.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Организация — имя подразделения**](a-ou.md)                                    | Верно      | **Организационная единица**         |
| [**Другие хорошо известные объекты**](a-otherwellknownobjects.md)                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Разделяемый атрибут-удаление-список**](a-partialattributedeletionlist.md)   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Разделяемый атрибут-set**](a-partialattributeset.md)                      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**физическая доставка — Office-имя**](a-physicaldeliveryofficename.md)       | Неверно     | **Организационная единица**         |
| [**Возможно — подстрочные**](a-possibleinferiors.md)                           | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Почтовый адрес**](a-postaladdress.md)                                   | Неверно     | **Организационная единица**         |
| [**Почтовый код**](a-postalcode.md)                                         | Неверно     | **Организационная единица**         |
| [**флажок после Office**](a-postofficebox.md)                                  | Неверно     | **Организационная единица**         |
| [**Предпочтительный метод доставки**](a-preferreddeliverymethod.md)              | Неверно     | **Организационная единица**         |
| [**Прокси-объект-имя**](a-proxiedobjectname.md)                          | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Прокси-адреса**](a-proxyaddresses.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Запрос — политика — BL**](a-querypolicybl.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**RDN**](a-name.md)                                                       | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Зарегистрированный адрес**](a-registeredaddress.md)                           | Неверно     | **Организационная единица**         |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**REPL-Уптодате-Vector**](a-repluptodatevector.md)                        | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Отчеты**](a-directreports.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Представители — от**](a-repsfrom.md)                                             | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Представители — кому**](a-repsto.md)                                                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Редакции**](a-revision.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**SD-Rights-эффективен**](a-sdrightseffective.md)                          | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Поиск — Обзор**](a-searchguide.md)                                       | Неверно     | **Организационная единица**         |
| [**См. также**](a-seealso.md)                                               | Неверно     | **Организационная единица**         |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**"Показать" — "Расширенный просмотр"**](a-showinadvancedviewonly.md)              | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**State-или-провинция-Name**](a-st.md)                                      | Неверно     | **Организационная единица**         |
| [**Улица-адрес**](a-street.md)                                          | Неверно     | **Организационная единица**         |
| [**Структурный объектный класс**](a-structuralobjectclass.md)                  | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Подразделы-ReFS**](a-subrefs.md)                                               | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**субсчемасубентри**](a-subschemasubentry.md)                            | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Системные флаги**](a-systemflags.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Номер телефона**](a-telephonenumber.md)                               | Неверно     | **Организационная единица**         |
| [**Teletex — идентификатор терминала**](a-teletexterminalidentifier.md)          | Неверно     | **Организационная единица**         |
| [**Номер телекса**](a-telexnumber.md)                                       | Неверно     | **Организационная единица**         |
| [**Текст — страна**](a-co.md)                                                | Неверно     | **Организационная единица**         |
| [**UPN-суффиксы**](a-upnsuffixes.md)                                       | Неверно     | **Организационная единица**         |
| [**Пароль пользователя**](a-userpassword.md)                                     | Неверно     | **Организационная единица**         |
| [**USN-изменено**](a-usnchanged.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Созданный USN**](a-usncreated.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**USN-DSA-Last-obj-removed**](a-usndsalastobjremoved.md)                  | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**USN — межсайтовая**](a-usnintersite.md)                                     | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Источник USN**](a-usnsource.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**WBEM — путь**](a-wbempath.md)                                             | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Хорошо известные объекты**](a-wellknownobjects.md)                            | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**При изменении**](a-whenchanged.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**При создании**](a-whencreated.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**WWW — Главная страница**](a-wwwhomepage.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**WWW-Page — другие**](a-url.md)                                             | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**X121 — адрес**](a-x121address.md)                                       | Неверно     | **Организационная единица**         |



## <a name="windows-server-2003-r2-extended-rights"></a>Windows Расширенные права сервера 2003 R2

этот класс содержит следующие расширенные права для Windows Server 2003 R2:



| Общее имя                                                |
|------------------------------------------------------------|
| [**Создание-RSoP-планирование**](r-generate-rsop-planning.md) |
| [**Generate-RSoP — ведение журнала**](r-generate-rsop-logging.md)   |



## <a name="windows-server-2008"></a>Windows Server 2008

-   [Атрибуты](#windows-server-2008-attributes)
-   [Расширенные права](#windows-server-2008-extended-rights)



| Ввод | Значение |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Неверно                                                                                                                                                                                                                                                                                                                                                                         |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                                                                                             |
| По умолчанию — объект — Категория     | \-                                                                                                                                                                                                                                                                                                                                                                            |
| Governs-Id                  | 2.5.6.5                                                                                                                                                                                                                                                                                                                                                                       |
| По умолчанию-скрытие значения        | 0                                                                                                                                                                                                                                                                                                                                                                             |
| RDN-Атри-ID                  | [**Организация — имя подразделения**](a-ou.md)<br/>                                                                                                                                                                                                                                                                                                                           |
| Подкласс                 | [**Вверх**](c-top.md)<br/>                                                                                                                                                                                                                                                                                                                                               |
| Возможные старшие          | [**Домен —**](c-domaindns.md)[**страна**](c-country.md) [**Организации**](c-organization.md)**подразделений** DNS                                                                                                                                                                                                                                                    |
| Вспомогательные классы           | \-                                                                                                                                                                                                                                                                                                                                                                            |
| NT-Security-дескриптор      | О:БАГ: BAD: S:                                                                                                                                                                                                                                                                                                                                                                  |
| Дескриптор безопасности по умолчанию | D: (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;; SY) (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;;D A) (OA;; ККДК; bf967a86-0de6-11D0-a285-00aa003049e2;; AO) (OA;; ККДК; bf967aba-0de6-11D0-a285-00aa003049e2;; AO) (OA;; ККДК; bf967a9c-0de6-11D0-a285-00aa003049e2;; AO) (OA;; ККДК; bf967aa8-0de6-11D0-a285-00aa003049e2;; ЗП) (A;; РПЛКЛОРК;;; AU) (A;; ЛКРПЛОРК;;; ED) (OA;; ККДК; 4828CC14-1437-45bc-9B07-AD6F015E5F28;; AO |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                                                                                    |



## <a name="windows-server-2008-attributes"></a>Windows Атрибуты сервера 2008

этот класс содержит следующие атрибуты для Windows Server 2008:



| attribute                                                                      | Обязательный | Унаследован от                    |
|--------------------------------------------------------------------------------|-----------|---------------------------------|
| [**Описание администратора**](a-admindescription.md)                                | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Имя администратора-отображение**](a-admindisplayname.md)                               | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Allowed-Attributes**](a-allowedattributes.md)                              | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Allowed-Attributes-эффективен**](a-allowedattributeseffective.md)           | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Allowed-Child-classes**](a-allowedchildclasses.md)                         | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Allowed-Child-classes-эффективен**](a-allowedchildclasseseffective.md)      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Плацдарм-Server-List-BL**](a-bridgeheadserverlistbl.md)                  | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Бизнес — Категория**](a-businesscategory.md)                                | Неверно     | **Организационная единица**         |
| [**Каноническое имя**](a-canonicalname.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Common-Name**](a-cn.md)                                                    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Код страны**](a-countrycode.md)                                          | Неверно     | **Организационная единица**         |
| [**Название страны**](a-c.md)                                                    | Неверно     | **Организационная единица**         |
| [**Метка времени создания**](a-createtimestamp.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Группа по умолчанию**](a-defaultgroup.md)                                        | Неверно     | **Организационная единица**         |
| [**Описание**](a-description.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Рабочий стол — профиль**](a-desktopprofile.md)                                    | Неверно     | **Организационная единица**         |
| [**Целевой индикатор**](a-destinationindicator.md)                        | Неверно     | **Организационная единица**         |
| [**Отображаемое имя**](a-displayname.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Отображаемое имя — печатаемое**](a-displaynameprintable.md)                       | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**DSA-Signature**](a-dsasignature.md)                                        | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**DS-Core-распространение-данные**](a-dscorepropagationdata.md)                    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Имя расширения**](a-extensionname.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Факс-телефон — номер**](a-facsimiletelephonenumber.md)               | Неверно     | **Организационная единица**         |
| [**Метки**](a-flags.md)                                                       | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Из записи**](a-fromentry.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                  | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                     | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**GP — ссылка**](a-gplink.md)                                                    | Неверно     | **Организационная единица**         |
| [**GP — параметры**](a-gpoptions.md)                                              | Неверно     | **Организационная единица**         |
| [**Тип экземпляра**](a-instancetype.md)                                        | Верно      | [**Вверх**](c-top.md)<br/> |
| [**Международный-ISDN-номер**](a-internationalisdnnumber.md)                 | Неверно     | **Организационная единица**         |
| [**Является критически важным — системный объект**](a-iscriticalsystemobject.md)                  | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Удалено**](a-isdeleted.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Входит в состав списка рассылки**](a-memberof.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Имеет права владельца**](a-isprivilegeholder.md)                             | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Последний-известный-родительский**](a-lastknownparent.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Локальное имя**](a-l.md)                                                   | Неверно     | **Организационная единица**         |
| [**Эмблема**](a-thumbnaillogo.md)                                                | Неверно     | **Организационная единица**         |
| [**Под управлением**](a-managedby.md)                                              | Неверно     | **Организационная единица**         |
| [**Управляемые объекты**](a-managedobjects.md)                                    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**В основном**](a-masteredby.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Метка времени изменения**](a-modifytimestamp.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-COM-Партитионсетлинк**](a-mscom-partitionsetlink.md)                    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-COM-Усерлинк**](a-mscom-userlink.md)                                    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-COM-Усерпартитионсетлинк**](a-mscom-userpartitionsetlink.md)            | Неверно     | **Организационная единица**         |
| [**MS-DFSR-Компутерреференцебл**](a-msdfsr-computerreferencebl.md)            | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DFSR-Мемберреференцебл**](a-msdfsr-memberreferencebl.md)                | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-примерно-Иммед-подчиненные**](a-msds-approx-immed-subordinates.md)    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Аусентикатедто-Аккаунтлист**](a-msds-authenticatedtoaccountlist.md) | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-целостность-дочерняя — количество**](a-ms-ds-consistencychildcount.md)         | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Consistencу-Guid**](a-ms-ds-consistencyguid.md)                      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS--домен — для**](a-msds-isdomainfor.md)                              | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-является-Full-реплика для**](a-msds-isfullreplicafor.md)                   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-является-partial-реплика для**](a-msds-ispartialreplicafor.md)             | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                            | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Masterd-by**](a-msds-masteredby.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)              | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-NC-REPL-курсоры**](a-msds-ncreplcursors.md)                          | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-NC-REPL-Inbound-соседи**](a-msds-ncreplinboundneighbors.md)       | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-NC-REPL-Outbound-соседи**](a-msds-ncreploutboundneighbors.md)     | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)  | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-NC-Type**](a-msds-nctype.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-не-Members-BL**](a-msds-nonmembersbl.md)                            | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                  | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Operations-для-AZ-Role-BL**](a-msds-operationsforazrolebl.md)        | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)        | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Principal-Name**](a-msds-principalname.md)                           | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-PSO — применяется**](a-msds-psoapplied.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-REPL-Attribute-Meta-Data**](a-msds-replattributemetadata.md)         | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-выявил-DSA**](a-msds-revealeddsas.md)                             | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-выводит-List-BL**](a-msds-revealedlistbl.md)                        | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Tasks-для-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                  | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                  | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-дов-Owner-BL**](a-ownerbl.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Мссфу-30-POSIX-член-of**](a-mssfu30posixmemberof.md)                     | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**нетбут-SCP-BL**](a-netbootscpbl.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Не-Security-Member-BL**](a-nonsecuritymemberbl.md)                        | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**NT-Security-дескриптор**](a-ntsecuritydescriptor.md)                       | Верно      | [**Вверх**](c-top.md)<br/> |
| [**Obj-расп-имя**](a-distinguishedname.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Объект — Категория**](a-objectcategory.md)                                    | Верно      | [**Вверх**](c-top.md)<br/> |
| [**Объектный класс**](a-objectclass.md)                                          | Верно      | [**Вверх**](c-top.md)<br/> |
| [**Объект — GUID**](a-objectguid.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Версия объекта**](a-objectversion.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Организация — имя подразделения**](a-ou.md)                                       | Верно      | **Организационная единица**         |
| [**Другие хорошо известные объекты**](a-otherwellknownobjects.md)                    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Разделяемый атрибут-удаление-список**](a-partialattributedeletionlist.md)      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Разделяемый атрибут-set**](a-partialattributeset.md)                         | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**физическая доставка — Office-имя**](a-physicaldeliveryofficename.md)          | Неверно     | **Организационная единица**         |
| [**Возможно — подстрочные**](a-possibleinferiors.md)                              | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Почтовый адрес**](a-postaladdress.md)                                      | Неверно     | **Организационная единица**         |
| [**Почтовый код**](a-postalcode.md)                                            | Неверно     | **Организационная единица**         |
| [**флажок после Office**](a-postofficebox.md)                                     | Неверно     | **Организационная единица**         |
| [**Предпочтительный метод доставки**](a-preferreddeliverymethod.md)                 | Неверно     | **Организационная единица**         |
| [**Прокси-объект-имя**](a-proxiedobjectname.md)                             | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Прокси-адреса**](a-proxyaddresses.md)                                    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Запрос — политика — BL**](a-querypolicybl.md)                                     | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**RDN**](a-name.md)                                                          | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Зарегистрированный адрес**](a-registeredaddress.md)                              | Неверно     | **Организационная единица**         |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**REPL-Уптодате-Vector**](a-repluptodatevector.md)                           | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Отчеты**](a-directreports.md)                                             | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Представители — от**](a-repsfrom.md)                                                | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Представители — кому**](a-repsto.md)                                                    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Редакции**](a-revision.md)                                                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**SD-Rights-эффективен**](a-sdrightseffective.md)                             | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Поиск — Обзор**](a-searchguide.md)                                          | Неверно     | **Организационная единица**         |
| [**См. также**](a-seealso.md)                                                  | Неверно     | **Организационная единица**         |
| [**Server-Reference-BL**](a-serverreferencebl.md)                             | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**"Показать" — "Расширенный просмотр"**](a-showinadvancedviewonly.md)                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Site-Object-BL**](a-siteobjectbl.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**State-или-провинция-Name**](a-st.md)                                         | Неверно     | **Организационная единица**         |
| [**Улица-адрес**](a-street.md)                                             | Неверно     | **Организационная единица**         |
| [**Структурный объектный класс**](a-structuralobjectclass.md)                     | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Подразделы-ReFS**](a-subrefs.md)                                                  | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**субсчемасубентри**](a-subschemasubentry.md)                               | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Системные флаги**](a-systemflags.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Номер телефона**](a-telephonenumber.md)                                  | Неверно     | **Организационная единица**         |
| [**Teletex — идентификатор терминала**](a-teletexterminalidentifier.md)             | Неверно     | **Организационная единица**         |
| [**Номер телекса**](a-telexnumber.md)                                          | Неверно     | **Организационная единица**         |
| [**Текст — страна**](a-co.md)                                                   | Неверно     | **Организационная единица**         |
| [**UPN-суффиксы**](a-upnsuffixes.md)                                          | Неверно     | **Организационная единица**         |
| [**Пароль пользователя**](a-userpassword.md)                                        | Неверно     | **Организационная единица**         |
| [**USN-изменено**](a-usnchanged.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Созданный USN**](a-usncreated.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**USN-DSA-Last-obj-removed**](a-usndsalastobjremoved.md)                     | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**USN — межсайтовая**](a-usnintersite.md)                                        | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Источник USN**](a-usnsource.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**WBEM — путь**](a-wbempath.md)                                                | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Хорошо известные объекты**](a-wellknownobjects.md)                               | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**При изменении**](a-whenchanged.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**При создании**](a-whencreated.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**WWW — Главная страница**](a-wwwhomepage.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**WWW-Page — другие**](a-url.md)                                                | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**X121 — адрес**](a-x121address.md)                                          | Неверно     | **Организационная единица**         |



## <a name="windows-server-2008-extended-rights"></a>Windows Расширенные права сервера 2008

этот класс содержит следующие расширенные права для Windows Server 2008:



| Общее имя                                                |
|------------------------------------------------------------|
| [**Создание-RSoP-планирование**](r-generate-rsop-planning.md) |
| [**Generate-RSoP — ведение журнала**](r-generate-rsop-logging.md)   |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2

-   [Атрибуты](#windows-server-2008-r2-attributes)
-   [Расширенные права](#windows-server-2008-r2-extended-rights)



| Ввод | Значение |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Неверно                                                                                                                                                                                                                                                                                                                                                                         |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                                                                                             |
| По умолчанию — объект — Категория     | \-                                                                                                                                                                                                                                                                                                                                                                            |
| Governs-Id                  | 2.5.6.5                                                                                                                                                                                                                                                                                                                                                                       |
| По умолчанию-скрытие значения        | 0                                                                                                                                                                                                                                                                                                                                                                             |
| RDN-Атри-ID                  | [**Организация — имя подразделения**](a-ou.md)<br/>                                                                                                                                                                                                                                                                                                                           |
| Подкласс                 | [**Вверх**](c-top.md)<br/>                                                                                                                                                                                                                                                                                                                                               |
| Возможные старшие          | [**Домен —**](c-domaindns.md)[**страна**](c-country.md) [**Организации**](c-organization.md)**подразделений** DNS                                                                                                                                                                                                                                                    |
| Вспомогательные классы           | \-                                                                                                                                                                                                                                                                                                                                                                            |
| NT-Security-дескриптор      | О:БАГ: BAD: S:                                                                                                                                                                                                                                                                                                                                                                  |
| Дескриптор безопасности по умолчанию | D: (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;; SY) (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;;D A) (OA;; ККДК; bf967a86-0de6-11D0-a285-00aa003049e2;; AO) (OA;; ККДК; bf967aba-0de6-11D0-a285-00aa003049e2;; AO) (OA;; ККДК; bf967a9c-0de6-11D0-a285-00aa003049e2;; AO) (OA;; ККДК; bf967aa8-0de6-11D0-a285-00aa003049e2;; ЗП) (A;; РПЛКЛОРК;;; AU) (A;; ЛКРПЛОРК;;; ED) (OA;; ККДК; 4828CC14-1437-45bc-9B07-AD6F015E5F28;; AO |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                                                                                    |



## <a name="windows-server-2008-r2-attributes"></a>Windows Атрибуты сервера 2008 R2

этот класс содержит следующие атрибуты для Windows Server 2008 R2:



| attribute                                                                        | Обязательный | Унаследован от                    |
|----------------------------------------------------------------------------------|-----------|---------------------------------|
| [**Описание администратора**](a-admindescription.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Имя администратора-отображение**](a-admindisplayname.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Allowed-Attributes**](a-allowedattributes.md)                                | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Allowed-Attributes-эффективен**](a-allowedattributeseffective.md)             | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Allowed-Child-classes**](a-allowedchildclasses.md)                           | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Allowed-Child-classes-эффективен**](a-allowedchildclasseseffective.md)        | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Плацдарм-Server-List-BL**](a-bridgeheadserverlistbl.md)                    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Бизнес — Категория**](a-businesscategory.md)                                  | Неверно     | **Организационная единица**         |
| [**Каноническое имя**](a-canonicalname.md)                                        | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Common-Name**](a-cn.md)                                                      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Код страны**](a-countrycode.md)                                            | Неверно     | **Организационная единица**         |
| [**Название страны**](a-c.md)                                                      | Неверно     | **Организационная единица**         |
| [**Метка времени создания**](a-createtimestamp.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Группа по умолчанию**](a-defaultgroup.md)                                          | Неверно     | **Организационная единица**         |
| [**Описание**](a-description.md)                                             | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Рабочий стол — профиль**](a-desktopprofile.md)                                      | Неверно     | **Организационная единица**         |
| [**Целевой индикатор**](a-destinationindicator.md)                          | Неверно     | **Организационная единица**         |
| [**Отображаемое имя**](a-displayname.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Отображаемое имя — печатаемое**](a-displaynameprintable.md)                         | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**DSA-Signature**](a-dsasignature.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**DS-Core-распространение-данные**](a-dscorepropagationdata.md)                      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Имя расширения**](a-extensionname.md)                                        | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Факс-телефон — номер**](a-facsimiletelephonenumber.md)                 | Неверно     | **Организационная единица**         |
| [**Метки**](a-flags.md)                                                         | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Из записи**](a-fromentry.md)                                                | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                        | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**GP — ссылка**](a-gplink.md)                                                      | Неверно     | **Организационная единица**         |
| [**GP — параметры**](a-gpoptions.md)                                                | Неверно     | **Организационная единица**         |
| [**Тип экземпляра**](a-instancetype.md)                                          | Верно      | [**Вверх**](c-top.md)<br/> |
| [**Международный-ISDN-номер**](a-internationalisdnnumber.md)                   | Неверно     | **Организационная единица**         |
| [**Является критически важным — системный объект**](a-iscriticalsystemobject.md)                    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Удалено**](a-isdeleted.md)                                                | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Входит в состав списка рассылки**](a-memberof.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Имеет права владельца**](a-isprivilegeholder.md)                               | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Является перезапущенным**](a-isrecycled.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Последний-известный-родительский**](a-lastknownparent.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Локальное имя**](a-l.md)                                                     | Неверно     | **Организационная единица**         |
| [**Эмблема**](a-thumbnaillogo.md)                                                  | Неверно     | **Организационная единица**         |
| [**Под управлением**](a-managedby.md)                                                | Неверно     | **Организационная единица**         |
| [**Управляемые объекты**](a-managedobjects.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**В основном**](a-masteredby.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Метка времени изменения**](a-modifytimestamp.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-COM-Партитионсетлинк**](a-mscom-partitionsetlink.md)                      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-COM-Усерлинк**](a-mscom-userlink.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-COM-Усерпартитионсетлинк**](a-mscom-userpartitionsetlink.md)              | Неверно     | **Организационная единица**         |
| [**MS-DFSR-Компутерреференцебл**](a-msdfsr-computerreferencebl.md)              | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DFSR-Мемберреференцебл**](a-msdfsr-memberreferencebl.md)                  | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-примерно-Иммед-подчиненные**](a-msds-approx-immed-subordinates.md)      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Аусентикатедто-Аккаунтлист**](a-msds-authenticatedtoaccountlist.md)   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-целостность-дочерняя — количество**](a-ms-ds-consistencychildcount.md)           | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Consistencу-Guid**](a-ms-ds-consistencyguid.md)                        | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Поддержка MS-DS-Feature-BL**](a-msds-enabledfeaturebl.md)                      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)             | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS--домен — для**](a-msds-isdomainfor.md)                                | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-является-Full-реплика для**](a-msds-isfullreplicafor.md)                     | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-является-partial-реплика для**](a-msds-ispartialreplicafor.md)               | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                              | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                              | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-локально-эффективное удаление — время**](a-msds-localeffectivedeletiontime.md) | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Local-эффективен — время перезапуска**](a-msds-localeffectiverecycletime.md)   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Masterd-by**](a-msds-masteredby.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)                | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-NC-REPL-курсоры**](a-msds-ncreplcursors.md)                            | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-NC-REPL-Inbound-соседи**](a-msds-ncreplinboundneighbors.md)         | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-NC-REPL-Outbound-соседи**](a-msds-ncreploutboundneighbors.md)       | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-NC-Type**](a-msds-nctype.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-не-Members-BL**](a-msds-nonmembersbl.md)                              | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Оидтограуп-Link-BL**](a-msds-oidtogrouplinkbl.md)                      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Operations-для-AZ-Role-BL**](a-msds-operationsforazrolebl.md)          | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)          | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Principal-Name**](a-msds-principalname.md)                             | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-PSO — применяется**](a-msds-psoapplied.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-REPL-Attribute-Meta-Data**](a-msds-replattributemetadata.md)           | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)                   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-выявил-DSA**](a-msds-revealeddsas.md)                               | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-выводит-List-BL**](a-msds-revealedlistbl.md)                          | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Tasks-для-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-дов-Owner-BL**](a-ownerbl.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Мссфу-30-POSIX-член-of**](a-mssfu30posixmemberof.md)                       | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**нетбут-SCP-BL**](a-netbootscpbl.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Не-Security-Member-BL**](a-nonsecuritymemberbl.md)                          | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**NT-Security-дескриптор**](a-ntsecuritydescriptor.md)                         | Верно      | [**Вверх**](c-top.md)<br/> |
| [**Obj-расп-имя**](a-distinguishedname.md)                                     | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Объект — Категория**](a-objectcategory.md)                                      | Верно      | [**Вверх**](c-top.md)<br/> |
| [**Объектный класс**](a-objectclass.md)                                            | Верно      | [**Вверх**](c-top.md)<br/> |
| [**Объект — GUID**](a-objectguid.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Версия объекта**](a-objectversion.md)                                        | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Организация — имя подразделения**](a-ou.md)                                         | Верно      | **Организационная единица**         |
| [**Другие хорошо известные объекты**](a-otherwellknownobjects.md)                      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Разделяемый атрибут-удаление-список**](a-partialattributedeletionlist.md)        | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Разделяемый атрибут-set**](a-partialattributeset.md)                           | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**физическая доставка — Office-имя**](a-physicaldeliveryofficename.md)            | Неверно     | **Организационная единица**         |
| [**Возможно — подстрочные**](a-possibleinferiors.md)                                | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Почтовый адрес**](a-postaladdress.md)                                        | Неверно     | **Организационная единица**         |
| [**Почтовый код**](a-postalcode.md)                                              | Неверно     | **Организационная единица**         |
| [**флажок после Office**](a-postofficebox.md)                                       | Неверно     | **Организационная единица**         |
| [**Предпочтительный метод доставки**](a-preferreddeliverymethod.md)                   | Неверно     | **Организационная единица**         |
| [**Прокси-объект-имя**](a-proxiedobjectname.md)                               | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Прокси-адреса**](a-proxyaddresses.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Запрос — политика — BL**](a-querypolicybl.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**RDN**](a-name.md)                                                            | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Зарегистрированный адрес**](a-registeredaddress.md)                                | Неверно     | **Организационная единица**         |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                        | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**REPL-Уптодате-Vector**](a-repluptodatevector.md)                             | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Отчеты**](a-directreports.md)                                               | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Представители — от**](a-repsfrom.md)                                                  | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Представители — кому**](a-repsto.md)                                                      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Редакции**](a-revision.md)                                                   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**SD-Rights-эффективен**](a-sdrightseffective.md)                               | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Поиск — Обзор**](a-searchguide.md)                                            | Неверно     | **Организационная единица**         |
| [**См. также**](a-seealso.md)                                                    | Неверно     | **Организационная единица**         |
| [**Server-Reference-BL**](a-serverreferencebl.md)                               | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**"Показать" — "Расширенный просмотр"**](a-showinadvancedviewonly.md)                   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Site-Object-BL**](a-siteobjectbl.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**State-или-провинция-Name**](a-st.md)                                           | Неверно     | **Организационная единица**         |
| [**Улица-адрес**](a-street.md)                                               | Неверно     | **Организационная единица**         |
| [**Структурный объектный класс**](a-structuralobjectclass.md)                       | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Подразделы-ReFS**](a-subrefs.md)                                                    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**субсчемасубентри**](a-subschemasubentry.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Системные флаги**](a-systemflags.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Номер телефона**](a-telephonenumber.md)                                    | Неверно     | **Организационная единица**         |
| [**Teletex — идентификатор терминала**](a-teletexterminalidentifier.md)               | Неверно     | **Организационная единица**         |
| [**Номер телекса**](a-telexnumber.md)                                            | Неверно     | **Организационная единица**         |
| [**Текст — страна**](a-co.md)                                                     | Неверно     | **Организационная единица**         |
| [**UPN-суффиксы**](a-upnsuffixes.md)                                            | Неверно     | **Организационная единица**         |
| [**Пароль пользователя**](a-userpassword.md)                                          | Неверно     | **Организационная единица**         |
| [**USN-изменено**](a-usnchanged.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Созданный USN**](a-usncreated.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**USN-DSA-Last-obj-removed**](a-usndsalastobjremoved.md)                       | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**USN — межсайтовая**](a-usnintersite.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Источник USN**](a-usnsource.md)                                                | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**WBEM — путь**](a-wbempath.md)                                                  | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Хорошо известные объекты**](a-wellknownobjects.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**При изменении**](a-whenchanged.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**При создании**](a-whencreated.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**WWW — Главная страница**](a-wwwhomepage.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**WWW-Page — другие**](a-url.md)                                                  | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**X121 — адрес**](a-x121address.md)                                            | Неверно     | **Организационная единица**         |



## <a name="windows-server-2008-r2-extended-rights"></a>Windows Расширенные права сервера 2008 R2

этот класс содержит следующие расширенные права для Windows Server 2008 R2:



| Общее имя                                                |
|------------------------------------------------------------|
| [**Создание-RSoP-планирование**](r-generate-rsop-planning.md) |
| [**Generate-RSoP — ведение журнала**](r-generate-rsop-logging.md)   |



## <a name="windows-server-2012"></a>Windows Server 2012

-   [Атрибуты](#windows-server-2012-attributes)
-   [Расширенные права](#windows-server-2012-extended-rights)



| Ввод | Значение |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Неверно                                                                                                                                                                                                                                                                                                                                                                         |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                                                                                             |
| По умолчанию — объект — Категория     | \-                                                                                                                                                                                                                                                                                                                                                                            |
| Governs-Id                  | 2.5.6.5                                                                                                                                                                                                                                                                                                                                                                       |
| По умолчанию-скрытие значения        | 0                                                                                                                                                                                                                                                                                                                                                                             |
| RDN-Атри-ID                  | [**Организация — имя подразделения**](a-ou.md)<br/>                                                                                                                                                                                                                                                                                                                           |
| Подкласс                 | [**Вверх**](c-top.md)<br/>                                                                                                                                                                                                                                                                                                                                               |
| Возможные старшие          | [**Домен —**](c-domaindns.md)[**страна**](c-country.md) [**Организации**](c-organization.md)**подразделений** DNS                                                                                                                                                                                                                                                    |
| Вспомогательные классы           | \-                                                                                                                                                                                                                                                                                                                                                                            |
| NT-Security-дескриптор      | О:БАГ: BAD: S:                                                                                                                                                                                                                                                                                                                                                                  |
| Дескриптор безопасности по умолчанию | D: (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;; SY) (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;;D A) (OA;; ККДК; bf967a86-0de6-11D0-a285-00aa003049e2;; AO) (OA;; ККДК; bf967aba-0de6-11D0-a285-00aa003049e2;; AO) (OA;; ККДК; bf967a9c-0de6-11D0-a285-00aa003049e2;; AO) (OA;; ККДК; bf967aa8-0de6-11D0-a285-00aa003049e2;; ЗП) (A;; РПЛКЛОРК;;; AU) (A;; ЛКРПЛОРК;;; ED) (OA;; ККДК; 4828CC14-1437-45bc-9B07-AD6F015E5F28;; AO |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                                                                                    |



## <a name="windows-server-2012-attributes"></a>Windows Server 2012 Атрибута

Этот класс содержит следующие атрибуты для Windows Server 2012:



| attribute                                                                                    | Обязательный | Унаследован от                    |
|----------------------------------------------------------------------------------------------|-----------|---------------------------------|
| [**Описание администратора**](a-admindescription.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Имя администратора-отображение**](a-admindisplayname.md)                                             | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Allowed-Attributes**](a-allowedattributes.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Allowed-Attributes-эффективен**](a-allowedattributeseffective.md)                         | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Allowed-Child-classes**](a-allowedchildclasses.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Allowed-Child-classes-эффективен**](a-allowedchildclasseseffective.md)                    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Плацдарм-Server-List-BL**](a-bridgeheadserverlistbl.md)                                | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Бизнес — Категория**](a-businesscategory.md)                                              | Неверно     | **Организационная единица**         |
| [**Каноническое имя**](a-canonicalname.md)                                                    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Common-Name**](a-cn.md)                                                                  | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Код страны**](a-countrycode.md)                                                        | Неверно     | **Организационная единица**         |
| [**Название страны**](a-c.md)                                                                  | Неверно     | **Организационная единица**         |
| [**Метка времени создания**](a-createtimestamp.md)                                               | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Группа по умолчанию**](a-defaultgroup.md)                                                      | Неверно     | **Организационная единица**         |
| [**Описание**](a-description.md)                                                         | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Рабочий стол — профиль**](a-desktopprofile.md)                                                  | Неверно     | **Организационная единица**         |
| [**Целевой индикатор**](a-destinationindicator.md)                                      | Неверно     | **Организационная единица**         |
| [**Отображаемое имя**](a-displayname.md)                                                        | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Отображаемое имя — печатаемое**](a-displaynameprintable.md)                                     | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**DSA-Signature**](a-dsasignature.md)                                                      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**DS-Core-распространение-данные**](a-dscorepropagationdata.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Имя расширения**](a-extensionname.md)                                                    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Факс-телефон — номер**](a-facsimiletelephonenumber.md)                             | Неверно     | **Организационная единица**         |
| [**Метки**](a-flags.md)                                                                     | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Из записи**](a-fromentry.md)                                                            | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                                | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                                    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                                   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**GP — ссылка**](a-gplink.md)                                                                  | Неверно     | **Организационная единица**         |
| [**GP — параметры**](a-gpoptions.md)                                                            | Неверно     | **Организационная единица**         |
| [**Тип экземпляра**](a-instancetype.md)                                                      | Верно      | [**Вверх**](c-top.md)<br/> |
| [**Международный-ISDN-номер**](a-internationalisdnnumber.md)                               | Неверно     | **Организационная единица**         |
| [**Является критически важным — системный объект**](a-iscriticalsystemobject.md)                                | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Удалено**](a-isdeleted.md)                                                            | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Входит в состав списка рассылки**](a-memberof.md)                                                        | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Имеет права владельца**](a-isprivilegeholder.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Является перезапущенным**](a-isrecycled.md)                                                          | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Последний-известный-родительский**](a-lastknownparent.md)                                               | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Локальное имя**](a-l.md)                                                                 | Неверно     | **Организационная единица**         |
| [**Эмблема**](a-thumbnaillogo.md)                                                              | Неверно     | **Организационная единица**         |
| [**Под управлением**](a-managedby.md)                                                            | Неверно     | **Организационная единица**         |
| [**Управляемые объекты**](a-managedobjects.md)                                                  | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**В основном**](a-masteredby.md)                                                          | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Метка времени изменения**](a-modifytimestamp.md)                                               | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-COM-Партитионсетлинк**](a-mscom-partitionsetlink.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-COM-Усерлинк**](a-mscom-userlink.md)                                                  | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-COM-Усерпартитионсетлинк**](a-mscom-userpartitionsetlink.md)                          | Неверно     | **Организационная единица**         |
| [**MS-DFSR-Компутерреференцебл**](a-msdfsr-computerreferencebl.md)                          | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DFSR-Мемберреференцебл**](a-msdfsr-memberreferencebl.md)                              | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-примерно-Иммед-подчиненные**](a-msds-approx-immed-subordinates.md)                  | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Аусентикатедто-Аккаунтлист**](a-msds-authenticatedtoaccountlist.md)               | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-ClaimSet-shares-возможные значения-with-BL**](a-msds-claimsharespossiblevalueswithbl.md) | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-целостность-дочерняя — количество**](a-ms-ds-consistencychildcount.md)                       | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Consistencу-Guid**](a-ms-ds-consistencyguid.md)                                    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Поддержка MS-DS-Feature-BL**](a-msds-enabledfeaturebl.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)                         | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS--домен — для**](a-msds-isdomainfor.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-является-Full-реплика для**](a-msds-isfullreplicafor.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-является-partial-реплика для**](a-msds-ispartialreplicafor.md)                           | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-является-PRIMARY-Computer-для**](a-msds-isprimarycomputerfor.md)                         | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-локально-эффективное удаление — время**](a-msds-localeffectivedeletiontime.md)             | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Local-эффективен — время перезапуска**](a-msds-localeffectiverecycletime.md)               | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Masterd-by**](a-msds-masteredby.md)                                               | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)                            | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Members-of-Resource-Property-List-BL**](a-msds-membersofresourcepropertylistbl.md) | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-NC-REPL-курсоры**](a-msds-ncreplcursors.md)                                        | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-NC-REPL-Inbound-соседи**](a-msds-ncreplinboundneighbors.md)                     | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-NC-REPL-Outbound-соседи**](a-msds-ncreploutboundneighbors.md)                   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)                | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-NC-Type**](a-msds-nctype.md)                                                       | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-не-Members-BL**](a-msds-nonmembersbl.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                                | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Оидтограуп-Link-BL**](a-msds-oidtogrouplinkbl.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Operations-для-AZ-Role-BL**](a-msds-operationsforazrolebl.md)                      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)                      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Principal-Name**](a-msds-principalname.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-PSO — применяется**](a-msds-psoapplied.md)                                               | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-REPL-Attribute-Meta-Data**](a-msds-replattributemetadata.md)                       | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)                               | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-выявил-DSA**](a-msds-revealeddsas.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-выводит-List-BL**](a-msds-revealedlistbl.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Tasks-для-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                                | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                                | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**ms-DS-TDO-Egress-BL**](a-msds-tdoegressbl.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-TDO-входящий трафик — BL**](a-msds-tdoingressbl.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-value-type-Reference-BL**](a-msds-valuetypereferencebl.md)                         | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-дов-Owner-BL**](a-ownerbl.md)                                                        | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Мссфу-30-POSIX-член-of**](a-mssfu30posixmemberof.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**нетбут-SCP-BL**](a-netbootscpbl.md)                                                     | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Не-Security-Member-BL**](a-nonsecuritymemberbl.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**NT-Security-дескриптор**](a-ntsecuritydescriptor.md)                                     | Верно      | [**Вверх**](c-top.md)<br/> |
| [**Obj-расп-имя**](a-distinguishedname.md)                                                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Объект — Категория**](a-objectcategory.md)                                                  | Верно      | [**Вверх**](c-top.md)<br/> |
| [**Объектный класс**](a-objectclass.md)                                                        | Верно      | [**Вверх**](c-top.md)<br/> |
| [**Объект — GUID**](a-objectguid.md)                                                          | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Версия объекта**](a-objectversion.md)                                                    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Организация — имя подразделения**](a-ou.md)                                                     | Верно      | **Организационная единица**         |
| [**Другие хорошо известные объекты**](a-otherwellknownobjects.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Разделяемый атрибут-удаление-список**](a-partialattributedeletionlist.md)                    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Разделяемый атрибут-set**](a-partialattributeset.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**физическая доставка — Office-имя**](a-physicaldeliveryofficename.md)                        | Неверно     | **Организационная единица**         |
| [**Возможно — подстрочные**](a-possibleinferiors.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Почтовый адрес**](a-postaladdress.md)                                                    | Неверно     | **Организационная единица**         |
| [**Почтовый код**](a-postalcode.md)                                                          | Неверно     | **Организационная единица**         |
| [**флажок после Office**](a-postofficebox.md)                                                   | Неверно     | **Организационная единица**         |
| [**Предпочтительный метод доставки**](a-preferreddeliverymethod.md)                               | Неверно     | **Организационная единица**         |
| [**Прокси-объект-имя**](a-proxiedobjectname.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Прокси-адреса**](a-proxyaddresses.md)                                                  | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Запрос — политика — BL**](a-querypolicybl.md)                                                   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**RDN**](a-name.md)                                                                        | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Зарегистрированный адрес**](a-registeredaddress.md)                                            | Неверно     | **Организационная единица**         |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                                    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**REPL-Уптодате-Vector**](a-repluptodatevector.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Отчеты**](a-directreports.md)                                                           | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Представители — от**](a-repsfrom.md)                                                              | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Представители — кому**](a-repsto.md)                                                                  | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Редакции**](a-revision.md)                                                               | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**SD-Rights-эффективен**](a-sdrightseffective.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Поиск — Обзор**](a-searchguide.md)                                                        | Неверно     | **Организационная единица**         |
| [**См. также**](a-seealso.md)                                                                | Неверно     | **Организационная единица**         |
| [**Server-Reference-BL**](a-serverreferencebl.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**"Показать" — "Расширенный просмотр"**](a-showinadvancedviewonly.md)                               | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                     | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**State-или-провинция-Name**](a-st.md)                                                       | Неверно     | **Организационная единица**         |
| [**Улица-адрес**](a-street.md)                                                           | Неверно     | **Организационная единица**         |
| [**Структурный объектный класс**](a-structuralobjectclass.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Подразделы-ReFS**](a-subrefs.md)                                                                | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**субсчемасубентри**](a-subschemasubentry.md)                                             | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Системные флаги**](a-systemflags.md)                                                        | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Номер телефона**](a-telephonenumber.md)                                                | Неверно     | **Организационная единица**         |
| [**Teletex — идентификатор терминала**](a-teletexterminalidentifier.md)                           | Неверно     | **Организационная единица**         |
| [**Номер телекса**](a-telexnumber.md)                                                        | Неверно     | **Организационная единица**         |
| [**Текст — страна**](a-co.md)                                                                 | Неверно     | **Организационная единица**         |
| [**UPN-суффиксы**](a-upnsuffixes.md)                                                        | Неверно     | **Организационная единица**         |
| [**Пароль пользователя**](a-userpassword.md)                                                      | Неверно     | **Организационная единица**         |
| [**USN-изменено**](a-usnchanged.md)                                                          | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Созданный USN**](a-usncreated.md)                                                          | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**USN-DSA-Last-obj-removed**](a-usndsalastobjremoved.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**USN — межсайтовая**](a-usnintersite.md)                                                      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                                  | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Источник USN**](a-usnsource.md)                                                            | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**WBEM — путь**](a-wbempath.md)                                                              | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Хорошо известные объекты**](a-wellknownobjects.md)                                             | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**При изменении**](a-whenchanged.md)                                                        | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**При создании**](a-whencreated.md)                                                        | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**WWW — Главная страница**](a-wwwhomepage.md)                                                       | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**WWW-Page — другие**](a-url.md)                                                              | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**X121 — адрес**](a-x121address.md)                                                        | Неверно     | **Организационная единица**         |



## <a name="windows-server-2012-extended-rights"></a>Windows Server 2012 Расширенные права

Этот класс содержит следующие расширенные права для Windows Server 2012:



| Общее имя                                                |
|------------------------------------------------------------|
| [**Создание-RSoP-планирование**](r-generate-rsop-planning.md) |
| [**Generate-RSoP — ведение журнала**](r-generate-rsop-logging.md)   |



 

 





