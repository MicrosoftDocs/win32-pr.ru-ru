---
title: Group - класс
description: Хранит список имен пользователей. Используется для применения субъектов безопасности к ресурсам.
ms.assetid: e8ce5c43-d0fb-4c67-a6ef-7094fb7e7669
ms.tgt_platform: multiple
keywords:
- Схема AD класса Group
- Схема AD класса Group
topic_type:
- apiref
api_name:
- Group
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 618adb97220f4cc1b1e4af7f42fd043c7bb1e6c5
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138043"
---
# <a name="group-class"></a>Group - класс

Хранит список имен пользователей. Используется для применения субъектов безопасности к ресурсам.



| Ввод | Значение |
|-------------------|------------------------------------------------|
| CN                | Группа                                          |
| LDAP-отображаемое имя | group                                          |
| Привилегия обновления  | Это значение задается администратором домена. |
| Частота обновления  | \-                                             |
| Schema-ID-GUID    | bf967a9c-0de6-11d0-a285-00aa003049e2           |



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
-   [Расширенные права](#windows-2000-server-extended-rights)
-   [Проверенные записи](#windows-2000-server-validated-writes)
-   [Наборы свойств](#windows-2000-server-property-sets)



| Ввод | Значение |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Неверно                                                                                                                                                                                               |
| Object-Category             | 1                                                                                                                                                                                                   |
| По умолчанию — объект — Категория     | \-                                                                                                                                                                                                  |
| Governs-Id                  | 1.2.840.113556.1.5.8                                                                                                                                                                                |
| По умолчанию-скрытие значения        | 0                                                                                                                                                                                                   |
| RDN-Атри-ID                  | [**Common-Name**](a-cn.md)<br/>                                                                                                                                                              |
| Подкласс                 | [**Вверх**](c-top.md)<br/>                                                                                                                                                                     |
| Возможные старшие          | [**Контейнер**](c-container.md) [](c-organizationalunit.md)[**встроенного**](c-builtindomain.md)подразделения [**домена DNS**](c-domaindns.md)                                       |
| Вспомогательные классы           | [**Безопасность-основной**](c-securityprincipal.md) (системный)[**mail — получатель**](c-mailrecipient.md) (система)                                                                                        |
| NT-Security-дескриптор      | О:БАГ: BAD: S:                                                                                                                                                                                        |
| Дескриптор безопасности по умолчанию | D: (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;;D А) (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;; SY) (A;; РПЛКЛОРК;;; AU) (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;; AO) (A;; РПЛКЛОРК;;; PS) (OA;; CR; ab721a55-1e2f-11D0-9819-00aa0040529b;; СЛУЖБЫ |
| System-Flags                | 0x00000010                                                                                                                                                                                          |



## <a name="windows-2000-server-attributes"></a>Атрибуты сервера Windows 2000

Этот класс содержит следующие атрибуты для сервера Windows 2000:



| attribute                                                                    | Обязательный | Унаследован от                                                                                 |
|------------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------|
| [**Имя учетной записи — журнал**](a-accountnamehistory.md)                         | Неверно     | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                 |
| [**Число администраторов**](a-admincount.md)                                          | Неверно     | **Группа**                                                                                    |
| [**Описание администратора**](a-admindescription.md)                              | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Имя администратора-отображение**](a-admindisplayname.md)                             | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Allowed-Attributes**](a-allowedattributes.md)                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Allowed-Attributes-эффективен**](a-allowedattributeseffective.md)         | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Allowed-Child-classes**](a-allowedchildclasses.md)                       | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Allowed-Child-classes-эффективен**](a-allowedchildclasseseffective.md)    | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Alt-Security — удостоверения**](a-altsecurityidentities.md)                   | Неверно     | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                 |
| [**Плацдарм-Server-List-BL**](a-bridgeheadserverlistbl.md)                | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Каноническое имя**](a-canonicalname.md)                                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Комментировать**](a-info.md)                                                    | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                         |
| [**Common-Name**](a-cn.md)                                                  | True      | [**Вверх**](c-top.md)<br/> [**Получатель почты**](c-mailrecipient.md)<br/>         |
| [**Управление — права доступа**](a-controlaccessrights.md)                       | Неверно     | **Группа**                                                                                    |
| [**Метка времени создания**](a-createtimestamp.md)                               | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Описание**](a-description.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Рабочий стол — профиль**](a-desktopprofile.md)                                  | Неверно     | **Группа**                                                                                    |
| [**Отображаемое имя**](a-displayname.md)                                        | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Отображаемое имя — печатаемое**](a-displaynameprintable.md)                     | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**DSA-Signature**](a-dsasignature.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**DS-Core-распространение-данные**](a-dscorepropagationdata.md)                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Адреса электронной почты**](a-mail.md)                                           | Неверно     | **Группа**                                                                                    |
| [**Имя расширения**](a-extensionname.md)                                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Метки**](a-flags.md)                                                     | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Из записи**](a-fromentry.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Мусор-Coll-период**](a-garbagecollperiod.md)                           | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                         |
| [**Атрибуты группы**](a-groupattributes.md)                                | Неверно     | **Группа**                                                                                    |
| [**Group-Membership-SAM**](a-groupmembershipsam.md)                         | Неверно     | **Группа**                                                                                    |
| [**Тип группы**](a-grouptype.md)                                            | True      | **Группа**                                                                                    |
| [**Тип экземпляра**](a-instancetype.md)                                      | True      | [**Вверх**](c-top.md)<br/>                                                              |
| [**Является критически важным — системный объект**](a-iscriticalsystemobject.md)                | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Удалено**](a-isdeleted.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Входит в состав списка рассылки**](a-memberof.md)                                        | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Имеет права владельца**](a-isprivilegeholder.md)                           | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Последний-известный-родительский**](a-lastknownparent.md)                               | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Устаревший — Exchange-DN**](a-legacyexchangedn.md)                             | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                         |
| [**Под управлением**](a-managedby.md)                                            | Неверно     | **Группа**                                                                                    |
| [**Управляемые объекты**](a-managedobjects.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**В основном**](a-masteredby.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Член**](a-member.md)                                                   | Неверно     | **Группа**                                                                                    |
| [**Метка времени изменения**](a-modifytimestamp.md)                               | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**MS-DS-целостность-дочерняя — количество**](a-ms-ds-consistencychildcount.md)       | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**MS-DS-Consistencу-Guid**](a-ms-ds-consistencyguid.md)                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**нетбут-SCP-BL**](a-netbootscpbl.md)                                     | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Не-Security-Member**](a-nonsecuritymember.md)                           | Неверно     | **Группа**                                                                                    |
| [**Не-Security-Member-BL**](a-nonsecuritymemberbl.md)                      | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**NT-Group-Members**](a-ntgroupmembers.md)                                 | Неверно     | **Группа**                                                                                    |
| [**NT-Security-дескриптор**](a-ntsecuritydescriptor.md)                     | True      | [**Вверх**](c-top.md)<br/> [**Безопасность — участник**](c-securityprincipal.md)<br/> |
| [**Obj-расп-имя**](a-distinguishedname.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Объект — Категория**](a-objectcategory.md)                                  | True      | [**Вверх**](c-top.md)<br/>                                                              |
| [**Объектный класс**](a-objectclass.md)                                        | True      | [**Вверх**](c-top.md)<br/>                                                              |
| [**Объект — GUID**](a-objectguid.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Идентификатор безопасности объекта**](a-objectsid.md)                                            | True      | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                 |
| [**Версия объекта**](a-objectversion.md)                                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Оператор Count**](a-operatorcount.md)                                    | Неверно     | **Группа**                                                                                    |
| [**Другие хорошо известные объекты**](a-otherwellknownobjects.md)                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Разделяемый атрибут-удаление-список**](a-partialattributedeletionlist.md)    | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Разделяемый атрибут-set**](a-partialattributeset.md)                       | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Возможно — подстрочные**](a-possibleinferiors.md)                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Маркер первичной группы**](a-primarygrouptoken.md)                           | Неверно     | **Группа**                                                                                    |
| [**Прокси-объект-имя**](a-proxiedobjectname.md)                           | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Прокси-адреса**](a-proxyaddresses.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Запрос — политика — BL**](a-querypolicybl.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**RDN**](a-name.md)                                                        | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**REPL-Уптодате-Vector**](a-repluptodatevector.md)                         | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Отчеты**](a-directreports.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Представители — от**](a-repsfrom.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Представители — кому**](a-repsto.md)                                                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Редакции**](a-revision.md)                                               | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Избежать**](a-rid.md)                                                         | Неверно     | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                 |
| [**SAM-имя учетной записи**](a-samaccountname.md)                                 | True      | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                 |
| [**SAM-тип учетной записи**](a-samaccounttype.md)                                 | Неверно     | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                 |
| [**SD-Rights-эффективен**](a-sdrightseffective.md)                           | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Безопасность — идентификатор**](a-securityidentifier.md)                          | Неверно     | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                 |
| [**Server-Reference-BL**](a-serverreferencebl.md)                           | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Отображение в адресной книге**](a-showinaddressbook.md)                          | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                         |
| [**"Показать" — "Расширенный просмотр"**](a-showinadvancedviewonly.md)               | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**SID — журнал**](a-sidhistory.md)                                          | Неверно     | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                 |
| [**Site-Object-BL**](a-siteobjectbl.md)                                     | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Подразделы-ReFS**](a-subrefs.md)                                                | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**субсчемасубентри**](a-subschemasubentry.md)                             | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Дополнительные учетные данные**](a-supplementalcredentials.md)                | Неверно     | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                 |
| [**Системные флаги**](a-systemflags.md)                                        | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Номер телефона**](a-telephonenumber.md)                                | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                         |
| [**С текстовым кодированием или адресом**](a-textencodedoraddress.md)                    | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                         |
| [**Группы токенов**](a-tokengroups.md)                                        | Неверно     | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                 |
| [**Группы токенов — глобальные и универсальные**](a-tokengroupsglobalanduniversal.md) | Неверно     | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                 |
| [**Токены-группы-No-GC-приемлемые**](a-tokengroupsnogcacceptable.md)         | Неверно     | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                 |
| [**User-CERT**](a-usercert.md)                                              | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                         |
| [**Пользователь-SMIME-Certificate**](a-usersmimecertificate.md)                     | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                         |
| [**USN-изменено**](a-usnchanged.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Созданный USN**](a-usncreated.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**USN-DSA-Last-obj-removed**](a-usndsalastobjremoved.md)                   | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**USN — межсайтовая**](a-usnintersite.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Источник USN**](a-usnsource.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**WBEM — путь**](a-wbempath.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Хорошо известные объекты**](a-wellknownobjects.md)                             | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**При изменении**](a-whenchanged.md)                                        | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**При создании**](a-whencreated.md)                                        | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**WWW — Главная страница**](a-wwwhomepage.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**WWW-Page — другие**](a-url.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**X509 — CERT**](a-usercertificate.md)                                       | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                         |



## <a name="windows-2000-server-extended-rights"></a>Расширенные права сервера Windows 2000

Этот класс содержит следующие расширенные права для сервера Windows 2000:



| Общее имя                  |
|------------------------------|
| [**Send-to**](r-send-to.md) |



## <a name="windows-2000-server-validated-writes"></a>Проверенные записи сервера Windows 2000

Этот класс содержит следующие проверенные операции записи для сервера Windows 2000.



| Общее имя                                  |
|----------------------------------------------|
| [**Самостоятельное членство**](r-self-membership.md) |



## <a name="windows-2000-server-property-sets"></a>Наборы свойств сервера Windows 2000

Этот класс содержит следующие наборы свойств для сервера Windows 2000:



| Общее имя                                      |
|--------------------------------------------------|
| [**Электронная почта — сведения**](r-email-information.md) |



## <a name="windows-server-2003"></a>Windows Server 2003

-   [Атрибуты](#windows-server-2003-attributes)
-   [Расширенные права](#windows-server-2003-extended-rights)
-   [Проверенные записи](#windows-server-2003-validated-writes)
-   [Наборы свойств](#windows-server-2003-property-sets)



| Ввод | Значение |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Неверно                                                                                                                                                                                                                                                                                                            |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                                |
| По умолчанию — объект — Категория     | \-                                                                                                                                                                                                                                                                                                               |
| Governs-Id                  | 1.2.840.113556.1.5.8                                                                                                                                                                                                                                                                                             |
| По умолчанию-скрытие значения        | 0                                                                                                                                                                                                                                                                                                                |
| RDN-Атри-ID                  | [**Common-Name**](a-cn.md)<br/>                                                                                                                                                                                                                                                                           |
| Подкласс                 | [**Вверх**](c-top.md)<br/>                                                                                                                                                                                                                                                                                  |
| Возможные старшие          | [**Доменное**](c-domaindns.md)[**подразделение**](c-organizationalunit.md)Domain-DNS контейнер [**встроенных**](c-builtindomain.md)[**контейнеров**](c-container.md)[**MS-DS-AZ-Admin-Manager**](c-msds-azadminmanager.md)[**MS-DS-AZ-Application**](c-msds-azapplication.md)[**MS-DS-AZ-Scope**](c-msds-azscope.md) |
| Вспомогательные классы           | [**Безопасность-основной**](c-securityprincipal.md) (системный)[**mail — получатель**](c-mailrecipient.md) (система)                                                                                                                                                                                                     |
| NT-Security-дескриптор      | О:БАГ: BAD: S:                                                                                                                                                                                                                                                                                                     |
| Дескриптор безопасности по умолчанию | D: (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;;D А) (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;; SY) (A;; РПЛКЛОРК;;; AU) (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;; AO) (A;; РПЛКЛОРК;;; PS) (OA;; CR; ab721a55-1e2f-11D0-9819-00aa0040529b;; AU) (OA;; RP; 46a9b11d-60ae-405a-b7e8-ff8a58d456d2;; S-1-5-32-560)                                                   |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                       |



## <a name="windows-server-2003-attributes"></a>Атрибуты Windows Server 2003

Этот класс содержит следующие атрибуты для Windows Server 2003:



| attribute                                                                    | Обязательный | Унаследован от                                                                                 |
|------------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------|
| [**Имя учетной записи — журнал**](a-accountnamehistory.md)                         | Неверно     | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                 |
| [**Число администраторов**](a-admincount.md)                                          | Неверно     | **Группа**                                                                                    |
| [**Описание администратора**](a-admindescription.md)                              | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Имя администратора-отображение**](a-admindisplayname.md)                             | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Allowed-Attributes**](a-allowedattributes.md)                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Allowed-Attributes-эффективен**](a-allowedattributeseffective.md)         | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Allowed-Child-classes**](a-allowedchildclasses.md)                       | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Allowed-Child-classes-эффективен**](a-allowedchildclasseseffective.md)    | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Alt-Security — удостоверения**](a-altsecurityidentities.md)                   | Неверно     | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                 |
| [**Плацдарм-Server-List-BL**](a-bridgeheadserverlistbl.md)                | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Каноническое имя**](a-canonicalname.md)                                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Комментировать**](a-info.md)                                                    | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                         |
| [**Common-Name**](a-cn.md)                                                  | True      | [**Вверх**](c-top.md)<br/> [**Получатель почты**](c-mailrecipient.md)<br/>         |
| [**Управление — права доступа**](a-controlaccessrights.md)                       | Неверно     | **Группа**                                                                                    |
| [**Метка времени создания**](a-createtimestamp.md)                               | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Описание**](a-description.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Рабочий стол — профиль**](a-desktopprofile.md)                                  | Неверно     | **Группа**                                                                                    |
| [**Отображаемое имя**](a-displayname.md)                                        | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Отображаемое имя — печатаемое**](a-displaynameprintable.md)                     | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**DSA-Signature**](a-dsasignature.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**DS-Core-распространение-данные**](a-dscorepropagationdata.md)                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Адреса электронной почты**](a-mail.md)                                           | Неверно     | **Группа**                                                                                    |
| [**Имя расширения**](a-extensionname.md)                                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Метки**](a-flags.md)                                                     | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Из записи**](a-fromentry.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Мусор-Coll-период**](a-garbagecollperiod.md)                           | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                         |
| [**Атрибуты группы**](a-groupattributes.md)                                | Неверно     | **Группа**                                                                                    |
| [**Group-Membership-SAM**](a-groupmembershipsam.md)                         | Неверно     | **Группа**                                                                                    |
| [**Тип группы**](a-grouptype.md)                                            | True      | **Группа**                                                                                    |
| [**Тип экземпляра**](a-instancetype.md)                                      | True      | [**Вверх**](c-top.md)<br/>                                                              |
| [**Является критически важным — системный объект**](a-iscriticalsystemobject.md)                | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Удалено**](a-isdeleted.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Входит в состав списка рассылки**](a-memberof.md)                                        | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Имеет права владельца**](a-isprivilegeholder.md)                           | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**лабеледури**](a-labeleduri.md)                                           | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                         |
| [**Последний-известный-родительский**](a-lastknownparent.md)                               | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Устаревший — Exchange-DN**](a-legacyexchangedn.md)                             | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                         |
| [**Под управлением**](a-managedby.md)                                            | Неверно     | **Группа**                                                                                    |
| [**Управляемые объекты**](a-managedobjects.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**В основном**](a-masteredby.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Член**](a-member.md)                                                   | Неверно     | **Группа**                                                                                    |
| [**Метка времени изменения**](a-modifytimestamp.md)                               | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**MS-COM-Партитионсетлинк**](a-mscom-partitionsetlink.md)                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**MS-COM-Усерлинк**](a-mscom-userlink.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**MS-DS-примерно-Иммед-подчиненные**](a-msds-approx-immed-subordinates.md)  | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**MS-DS-AZ-LDAP-Query**](a-msds-azldapquery.md)                            | Неверно     | **Группа**                                                                                    |
| [**MS-DS-целостность-дочерняя — количество**](a-ms-ds-consistencychildcount.md)       | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**MS-DS-Consistencу-Guid**](a-ms-ds-consistencyguid.md)                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**MS-DS-Кэйверсионнумбер**](a-msds-keyversionnumber.md)                    | Неверно     | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                 |
| [**MS-DS-Masterd-by**](a-msds-masteredby.md)                               | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**MS-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)            | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**MS-DS-NC-REPL-курсоры**](a-msds-ncreplcursors.md)                        | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**MS-DS-NC-REPL-Inbound-соседи**](a-msds-ncreplinboundneighbors.md)     | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**MS-DS-NC-REPL-Outbound-соседи**](a-msds-ncreploutboundneighbors.md)   | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**MS-DS-не-члены**](a-msds-nonmembers.md)                               | Неверно     | **Группа**                                                                                    |
| [**MS-DS-не-Members-BL**](a-msds-nonmembersbl.md)                          | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**MS-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**MS-DS-Operations-для-AZ-Role-BL**](a-msds-operationsforazrolebl.md)      | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**MS-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)      | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**MS-DS-REPL-Attribute-Meta-Data**](a-msds-replattributemetadata.md)       | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**MS-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)               | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**MS-DS-Tasks-для-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**MS-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**MS-дов-Assistant-Name**](a-msexchassistantname.md)                      | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                         |
| [**MS-дов-Лабеледури**](a-msexchlabeleduri.md)                             | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                         |
| [**MS-дов-Owner-BL**](a-ownerbl.md)                                        | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**нетбут-SCP-BL**](a-netbootscpbl.md)                                     | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Не-Security-Member**](a-nonsecuritymember.md)                           | Неверно     | **Группа**                                                                                    |
| [**Не-Security-Member-BL**](a-nonsecuritymemberbl.md)                      | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**NT-Group-Members**](a-ntgroupmembers.md)                                 | Неверно     | **Группа**                                                                                    |
| [**NT-Security-дескриптор**](a-ntsecuritydescriptor.md)                     | True      | [**Вверх**](c-top.md)<br/> [**Безопасность — участник**](c-securityprincipal.md)<br/> |
| [**Obj-расп-имя**](a-distinguishedname.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Объект — Категория**](a-objectcategory.md)                                  | True      | [**Вверх**](c-top.md)<br/>                                                              |
| [**Объектный класс**](a-objectclass.md)                                        | True      | [**Вверх**](c-top.md)<br/>                                                              |
| [**Объект — GUID**](a-objectguid.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Идентификатор безопасности объекта**](a-objectsid.md)                                            | True      | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                 |
| [**Версия объекта**](a-objectversion.md)                                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Оператор Count**](a-operatorcount.md)                                    | Неверно     | **Группа**                                                                                    |
| [**Другие хорошо известные объекты**](a-otherwellknownobjects.md)                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Разделяемый атрибут-удаление-список**](a-partialattributedeletionlist.md)    | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Разделяемый атрибут-set**](a-partialattributeset.md)                       | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Возможно — подстрочные**](a-possibleinferiors.md)                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Маркер первичной группы**](a-primarygrouptoken.md)                           | Неверно     | **Группа**                                                                                    |
| [**Прокси-объект-имя**](a-proxiedobjectname.md)                           | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Прокси-адреса**](a-proxyaddresses.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Запрос — политика — BL**](a-querypolicybl.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**RDN**](a-name.md)                                                        | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**REPL-Уптодате-Vector**](a-repluptodatevector.md)                         | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Отчеты**](a-directreports.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Представители — от**](a-repsfrom.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Представители — кому**](a-repsto.md)                                                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Редакции**](a-revision.md)                                               | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Избежать**](a-rid.md)                                                         | Неверно     | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                 |
| [**SAM-имя учетной записи**](a-samaccountname.md)                                 | True      | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                 |
| [**SAM-тип учетной записи**](a-samaccounttype.md)                                 | Неверно     | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                 |
| [**SD-Rights-эффективен**](a-sdrightseffective.md)                           | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**секретарь**](a-secretary.md)                                             | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                         |
| [**Безопасность — идентификатор**](a-securityidentifier.md)                          | Неверно     | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                 |
| [**Server-Reference-BL**](a-serverreferencebl.md)                           | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Отображение в адресной книге**](a-showinaddressbook.md)                          | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                         |
| [**"Показать" — "Расширенный просмотр"**](a-showinadvancedviewonly.md)               | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**SID — журнал**](a-sidhistory.md)                                          | Неверно     | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                 |
| [**Site-Object-BL**](a-siteobjectbl.md)                                     | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Структурный объектный класс**](a-structuralobjectclass.md)                   | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Подразделы-ReFS**](a-subrefs.md)                                                | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**субсчемасубентри**](a-subschemasubentry.md)                             | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Дополнительные учетные данные**](a-supplementalcredentials.md)                | Неверно     | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                 |
| [**Системные флаги**](a-systemflags.md)                                        | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Номер телефона**](a-telephonenumber.md)                                | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                         |
| [**С текстовым кодированием или адресом**](a-textencodedoraddress.md)                    | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                         |
| [**Группы токенов**](a-tokengroups.md)                                        | Неверно     | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                 |
| [**Группы токенов — глобальные и универсальные**](a-tokengroupsglobalanduniversal.md) | Неверно     | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                 |
| [**Токены-группы-No-GC-приемлемые**](a-tokengroupsnogcacceptable.md)         | Неверно     | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                 |
| [**User-CERT**](a-usercert.md)                                              | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                         |
| [**Пользователь-SMIME-Certificate**](a-usersmimecertificate.md)                     | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                         |
| [**USN-изменено**](a-usnchanged.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Созданный USN**](a-usncreated.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**USN-DSA-Last-obj-removed**](a-usndsalastobjremoved.md)                   | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**USN — межсайтовая**](a-usnintersite.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Источник USN**](a-usnsource.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**WBEM — путь**](a-wbempath.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Хорошо известные объекты**](a-wellknownobjects.md)                             | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**При изменении**](a-whenchanged.md)                                        | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**При создании**](a-whencreated.md)                                        | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**WWW — Главная страница**](a-wwwhomepage.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**WWW-Page — другие**](a-url.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**X509 — CERT**](a-usercertificate.md)                                       | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                         |



## <a name="windows-server-2003-extended-rights"></a>Расширенные права Windows Server 2003

Этот класс содержит следующие расширенные права для Windows Server 2003:



| Общее имя                  |
|------------------------------|
| [**Send-to**](r-send-to.md) |



## <a name="windows-server-2003-validated-writes"></a>Проверенные записи Windows Server 2003

Этот класс содержит следующие проверенные операции записи для Windows Server 2003:



| Общее имя                                  |
|----------------------------------------------|
| [**Самостоятельное членство**](r-self-membership.md) |



## <a name="windows-server-2003-property-sets"></a>Наборы свойств Windows Server 2003

Этот класс содержит следующие наборы свойств для Windows Server 2003:



| Общее имя                                      |
|--------------------------------------------------|
| [**Электронная почта — сведения**](r-email-information.md) |



## <a name="adam"></a>ADAM

-   [Атрибуты](#adam-attributes)
-   [Проверенные записи](#adam-validated-writes)
-   [Наборы свойств](#adam-property-sets)



| Ввод | Значение |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Неверно                                                                                                                |
| Object-Category             | 1                                                                                                                    |
| По умолчанию — объект — Категория     | \-                                                                                                                   |
| Governs-Id                  | 1.2.840.113556.1.5.8                                                                                                 |
| По умолчанию-скрытие значения        | 0                                                                                                                    |
| RDN-Атри-ID                  | [**Common-Name**](a-cn.md)<br/>                                                                               |
| Подкласс                 | [**Вверх**](c-top.md)<br/>                                                                                      |
| Возможные старшие          | [**Домен —**](c-domaindns.md)[](c-organizationalunit.md)[**контейнер**](c-container.md) подразделения DNS |
| Вспомогательные классы           | [**Безопасность-субъект**](c-securityprincipal.md) (система)                                                           |
| NT-Security-дескриптор      | О:БАГ: BAD: S:                                                                                                         |
| Дескриптор безопасности по умолчанию | Д:С:                                                                                                                 |
| System-Flags                | 0x00000010                                                                                                           |



## <a name="adam-attributes"></a>Атрибуты ADAM

Этот класс содержит следующие атрибуты для ADAM:



| attribute                                                                   | Обязательный | Унаследован от                                                                                 |
|-----------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------|
| [**Описание администратора**](a-admindescription.md)                             | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Имя администратора-отображение**](a-admindisplayname.md)                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Allowed-Attributes**](a-allowedattributes.md)                           | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Allowed-Attributes-эффективен**](a-allowedattributeseffective.md)        | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Allowed-Child-classes**](a-allowedchildclasses.md)                      | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Allowed-Child-classes-эффективен**](a-allowedchildclasseseffective.md)   | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Плацдарм-Server-List-BL**](a-bridgeheadserverlistbl.md)               | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Каноническое имя**](a-canonicalname.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Common-Name**](a-cn.md)                                                 | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Метка времени создания**](a-createtimestamp.md)                              | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Описание**](a-description.md)                                        | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Рабочий стол — профиль**](a-desktopprofile.md)                                 | Неверно     | **Группа**                                                                                    |
| [**Отображаемое имя**](a-displayname.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**DSA-Signature**](a-dsasignature.md)                                     | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**DS-Core-распространение-данные**](a-dscorepropagationdata.md)                 | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Из записи**](a-fromentry.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Тип группы**](a-grouptype.md)                                           | True      | **Группа**                                                                                    |
| [**Тип экземпляра**](a-instancetype.md)                                     | True      | [**Вверх**](c-top.md)<br/>                                                              |
| [**Является критически важным — системный объект**](a-iscriticalsystemobject.md)               | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Удалено**](a-isdeleted.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Входит в состав списка рассылки**](a-memberof.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Последний-известный-родительский**](a-lastknownparent.md)                              | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Под управлением**](a-managedby.md)                                           | Неверно     | **Группа**                                                                                    |
| [**Управляемые объекты**](a-managedobjects.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**В основном**](a-masteredby.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Член**](a-member.md)                                                  | Неверно     | **Группа**                                                                                    |
| [**Метка времени изменения**](a-modifytimestamp.md)                              | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**MS-DS-примерно-Иммед-подчиненные**](a-msds-approx-immed-subordinates.md) | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**MS-DS-целостность-дочерняя — количество**](a-ms-ds-consistencychildcount.md)      | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**MS-DS-Consistencу-Guid**](a-ms-ds-consistencyguid.md)                   | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**MS-DS-Disabled-for-Instances-BL**](a-msds-disableforinstancesbl.md)      | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**MS-DS-Masterd-by**](a-msds-masteredby.md)                              | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**MS-DS-NC-REPL-курсоры**](a-msds-ncreplcursors.md)                       | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**MS-DS-NC-REPL-Inbound-соседи**](a-msds-ncreplinboundneighbors.md)    | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**MS-DS-NC-REPL-Outbound-соседи**](a-msds-ncreploutboundneighbors.md)  | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**MS-DS-REPL-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**MS-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)              | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**MS-DS-Service-Account-BL**](a-msds-serviceaccountbl.md)                 | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**NT-Security-дескриптор**](a-ntsecuritydescriptor.md)                    | True      | [**Вверх**](c-top.md)<br/> [**Безопасность — участник**](c-securityprincipal.md)<br/> |
| [**Obj-расп-имя**](a-distinguishedname.md)                                | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Объект — Категория**](a-objectcategory.md)                                 | True      | [**Вверх**](c-top.md)<br/>                                                              |
| [**Объектный класс**](a-objectclass.md)                                       | True      | [**Вверх**](c-top.md)<br/>                                                              |
| [**Объект — GUID**](a-objectguid.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Идентификатор безопасности объекта**](a-objectsid.md)                                           | True      | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                 |
| [**Версия объекта**](a-objectversion.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Другие хорошо известные объекты**](a-otherwellknownobjects.md)                 | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Разделяемый атрибут-удаление-список**](a-partialattributedeletionlist.md)   | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Разделяемый атрибут-set**](a-partialattributeset.md)                      | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Возможно — подстрочные**](a-possibleinferiors.md)                           | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Маркер первичной группы**](a-primarygrouptoken.md)                          | Неверно     | **Группа**                                                                                    |
| [**Прокси-объект-имя**](a-proxiedobjectname.md)                          | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Прокси-адреса**](a-proxyaddresses.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Запрос — политика — BL**](a-querypolicybl.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**RDN**](a-name.md)                                                       | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                   | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**REPL-Уптодате-Vector**](a-repluptodatevector.md)                        | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Представители — от**](a-repsfrom.md)                                             | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Представители — кому**](a-repsto.md)                                                 | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Редакции**](a-revision.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**SD-Rights-эффективен**](a-sdrightseffective.md)                          | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**"Показать" — "Расширенный просмотр"**](a-showinadvancedviewonly.md)              | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Структурный объектный класс**](a-structuralobjectclass.md)                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Подразделы-ReFS**](a-subrefs.md)                                               | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**субсчемасубентри**](a-subschemasubentry.md)                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Дополнительные учетные данные**](a-supplementalcredentials.md)               | Неверно     | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                 |
| [**Системные флаги**](a-systemflags.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Группы токенов**](a-tokengroups.md)                                       | Неверно     | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                 |
| [**USN-изменено**](a-usnchanged.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Созданный USN**](a-usncreated.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**USN-DSA-Last-obj-removed**](a-usndsalastobjremoved.md)                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**USN — межсайтовая**](a-usnintersite.md)                                     | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Источник USN**](a-usnsource.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**WBEM — путь**](a-wbempath.md)                                             | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Хорошо известные объекты**](a-wellknownobjects.md)                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**При изменении**](a-whenchanged.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**При создании**](a-whencreated.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**WWW — Главная страница**](a-wwwhomepage.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**WWW-Page — другие**](a-url.md)                                             | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |



## <a name="adam-validated-writes"></a>Проверенные записи ADAM

Этот класс содержит следующие проверенные операции записи для ADAM:



| Общее имя                                  |
|----------------------------------------------|
| [**Самостоятельное членство**](r-self-membership.md) |



## <a name="adam-property-sets"></a>Наборы свойств ADAM

Этот класс содержит следующие наборы свойств для ADAM:



| Общее имя                                      |
|--------------------------------------------------|
| [**Электронная почта — сведения**](r-email-information.md) |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2

-   [Атрибуты](#windows-server-2003-r2-attributes)
-   [Расширенные права](#windows-server-2003-r2-extended-rights)
-   [Проверенные записи](#windows-server-2003-r2-validated-writes)
-   [Наборы свойств](#windows-server-2003-r2-property-sets)



| Ввод | Значение |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Неверно                                                                                                                                                                                                                                                                                                            |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                                |
| По умолчанию — объект — Категория     | \-                                                                                                                                                                                                                                                                                                               |
| Governs-Id                  | 1.2.840.113556.1.5.8                                                                                                                                                                                                                                                                                             |
| По умолчанию-скрытие значения        | 0                                                                                                                                                                                                                                                                                                                |
| RDN-Атри-ID                  | [**Common-Name**](a-cn.md)<br/>                                                                                                                                                                                                                                                                           |
| Подкласс                 | [**Вверх**](c-top.md)<br/>                                                                                                                                                                                                                                                                                  |
| Возможные старшие          | [**Доменное**](c-domaindns.md)[**подразделение**](c-organizationalunit.md)Domain-DNS контейнер [**встроенных**](c-builtindomain.md)[**контейнеров**](c-container.md)[**MS-DS-AZ-Admin-Manager**](c-msds-azadminmanager.md)[**MS-DS-AZ-Application**](c-msds-azapplication.md)[**MS-DS-AZ-Scope**](c-msds-azscope.md) |
| Вспомогательные классы           | [**посиксграуп**](c-posixgroup.md)[**Security-Principal**](c-securityprincipal.md) (система)[**mail-получател**](c-mailrecipient.md) (System)                                                                                                                                                                   |
| NT-Security-дескриптор      | О:БАГ: BAD: S:                                                                                                                                                                                                                                                                                                     |
| Дескриптор безопасности по умолчанию | D: (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;;D А) (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;; SY) (A;; РПЛКЛОРК;;; AU) (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;; AO) (A;; РПЛКЛОРК;;; PS) (OA;; CR; ab721a55-1e2f-11D0-9819-00aa0040529b;; AU) (OA;; RP; 46a9b11d-60ae-405a-b7e8-ff8a58d456d2;; S-1-5-32-560)                                                   |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                       |



## <a name="windows-server-2003-r2-attributes"></a>Атрибуты Windows Server 2003 R2

Этот класс содержит следующие атрибуты для Windows Server 2003 R2:



| attribute                                                                    | Обязательный | Унаследован от                                                                                                                       |
|------------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Имя учетной записи — журнал**](a-accountnamehistory.md)                         | Неверно     | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                                                       |
| [**Число администраторов**](a-admincount.md)                                          | Неверно     | **Группа**                                                                                                                          |
| [**Описание администратора**](a-admindescription.md)                              | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Имя администратора-отображение**](a-admindisplayname.md)                             | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Allowed-Attributes**](a-allowedattributes.md)                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Allowed-Attributes-эффективен**](a-allowedattributeseffective.md)         | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Allowed-Child-classes**](a-allowedchildclasses.md)                       | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Allowed-Child-classes-эффективен**](a-allowedchildclasseseffective.md)    | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Alt-Security — удостоверения**](a-altsecurityidentities.md)                   | Неверно     | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                                                       |
| [**Плацдарм-Server-List-BL**](a-bridgeheadserverlistbl.md)                | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Каноническое имя**](a-canonicalname.md)                                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Комментировать**](a-info.md)                                                    | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                               |
| [**Common-Name**](a-cn.md)                                                  | True      | [**Вверх**](c-top.md)<br/> [**посиксграуп**](c-posixgroup.md)<br/> [**Получатель почты**](c-mailrecipient.md)<br/> |
| [**Управление — права доступа**](a-controlaccessrights.md)                       | Неверно     | **Группа**                                                                                                                          |
| [**Метка времени создания**](a-createtimestamp.md)                               | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Описание**](a-description.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/> [**посиксграуп**](c-posixgroup.md)<br/>                                                      |
| [**Рабочий стол — профиль**](a-desktopprofile.md)                                  | Неверно     | **Группа**                                                                                                                          |
| [**Отображаемое имя**](a-displayname.md)                                        | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Отображаемое имя — печатаемое**](a-displaynameprintable.md)                     | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**DSA-Signature**](a-dsasignature.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**DS-Core-распространение-данные**](a-dscorepropagationdata.md)                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Адреса электронной почты**](a-mail.md)                                           | Неверно     | **Группа**                                                                                                                          |
| [**Имя расширения**](a-extensionname.md)                                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Метки**](a-flags.md)                                                     | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Из записи**](a-fromentry.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Мусор-Coll-период**](a-garbagecollperiod.md)                           | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                               |
| [**gidNumber**](a-gidnumber.md)                                             | Неверно     | [**посиксграуп**](c-posixgroup.md)<br/>                                                                                      |
| [**Атрибуты группы**](a-groupattributes.md)                                | Неверно     | **Группа**                                                                                                                          |
| [**Group-Membership-SAM**](a-groupmembershipsam.md)                         | Неверно     | **Группа**                                                                                                                          |
| [**Тип группы**](a-grouptype.md)                                            | True      | **Группа**                                                                                                                          |
| [**Тип экземпляра**](a-instancetype.md)                                      | True      | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Является критически важным — системный объект**](a-iscriticalsystemobject.md)                | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Удалено**](a-isdeleted.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Входит в состав списка рассылки**](a-memberof.md)                                        | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Имеет права владельца**](a-isprivilegeholder.md)                           | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**лабеледури**](a-labeleduri.md)                                           | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                               |
| [**Последний-известный-родительский**](a-lastknownparent.md)                               | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Устаревший — Exchange-DN**](a-legacyexchangedn.md)                             | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                               |
| [**Под управлением**](a-managedby.md)                                            | Неверно     | **Группа**                                                                                                                          |
| [**Управляемые объекты**](a-managedobjects.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**В основном**](a-masteredby.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Член**](a-member.md)                                                   | Неверно     | **Группа**                                                                                                                          |
| [**мемберуид**](a-memberuid.md)                                             | Неверно     | [**посиксграуп**](c-posixgroup.md)<br/>                                                                                      |
| [**Метка времени изменения**](a-modifytimestamp.md)                               | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-COM-Партитионсетлинк**](a-mscom-partitionsetlink.md)                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-COM-Усерлинк**](a-mscom-userlink.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DFSR-Компутерреференцебл**](a-msdfsr-computerreferencebl.md)          | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DFSR-Мемберреференцебл**](a-msdfsr-memberreferencebl.md)              | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-примерно-Иммед-подчиненные**](a-msds-approx-immed-subordinates.md)  | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-AZ-LDAP-Query**](a-msds-azldapquery.md)                            | Неверно     | **Группа**                                                                                                                          |
| [**MS-DS-целостность-дочерняя — количество**](a-ms-ds-consistencychildcount.md)       | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Consistencу-Guid**](a-ms-ds-consistencyguid.md)                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Кэйверсионнумбер**](a-msds-keyversionnumber.md)                    | Неверно     | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                                                       |
| [**MS-DS-Masterd-by**](a-msds-masteredby.md)                               | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)            | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-NC-REPL-курсоры**](a-msds-ncreplcursors.md)                        | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-NC-REPL-Inbound-соседи**](a-msds-ncreplinboundneighbors.md)     | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-NC-REPL-Outbound-соседи**](a-msds-ncreploutboundneighbors.md)   | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-не-члены**](a-msds-nonmembers.md)                               | Неверно     | **Группа**                                                                                                                          |
| [**MS-DS-не-Members-BL**](a-msds-nonmembersbl.md)                          | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Operations-для-AZ-Role-BL**](a-msds-operationsforazrolebl.md)      | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)      | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-REPL-Attribute-Meta-Data**](a-msds-replattributemetadata.md)       | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)               | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Tasks-для-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-дов-Assistant-Name**](a-msexchassistantname.md)                      | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                               |
| [**MS-дов-Лабеледури**](a-msexchlabeleduri.md)                             | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                               |
| [**MS-дов-Owner-BL**](a-ownerbl.md)                                        | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Мссфу-30 — имя**](a-mssfu30name.md)                                       | Неверно     | **Группа**                                                                                                                          |
| [**Мссфу-30-NIS-домен**](a-mssfu30nisdomain.md)                            | Неверно     | **Группа**                                                                                                                          |
| [**Мссфу-30-POSIX-Member**](a-mssfu30posixmember.md)                        | Неверно     | **Группа**                                                                                                                          |
| [**Мссфу-30-POSIX-член-of**](a-mssfu30posixmemberof.md)                   | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**нетбут-SCP-BL**](a-netbootscpbl.md)                                     | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Не-Security-Member**](a-nonsecuritymember.md)                           | Неверно     | **Группа**                                                                                                                          |
| [**Не-Security-Member-BL**](a-nonsecuritymemberbl.md)                      | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**NT-Group-Members**](a-ntgroupmembers.md)                                 | Неверно     | **Группа**                                                                                                                          |
| [**NT-Security-дескриптор**](a-ntsecuritydescriptor.md)                     | True      | [**Вверх**](c-top.md)<br/> [**Безопасность — участник**](c-securityprincipal.md)<br/>                                       |
| [**Obj-расп-имя**](a-distinguishedname.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Объект — Категория**](a-objectcategory.md)                                  | True      | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Объектный класс**](a-objectclass.md)                                        | True      | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Объект — GUID**](a-objectguid.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Идентификатор безопасности объекта**](a-objectsid.md)                                            | True      | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                                                       |
| [**Версия объекта**](a-objectversion.md)                                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Оператор Count**](a-operatorcount.md)                                    | Неверно     | **Группа**                                                                                                                          |
| [**Другие хорошо известные объекты**](a-otherwellknownobjects.md)                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Разделяемый атрибут-удаление-список**](a-partialattributedeletionlist.md)    | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Разделяемый атрибут-set**](a-partialattributeset.md)                       | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Возможно — подстрочные**](a-possibleinferiors.md)                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Маркер первичной группы**](a-primarygrouptoken.md)                           | Неверно     | **Группа**                                                                                                                          |
| [**Прокси-объект-имя**](a-proxiedobjectname.md)                           | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Прокси-адреса**](a-proxyaddresses.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Запрос — политика — BL**](a-querypolicybl.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**RDN**](a-name.md)                                                        | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**REPL-Уптодате-Vector**](a-repluptodatevector.md)                         | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Отчеты**](a-directreports.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Представители — от**](a-repsfrom.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Представители — кому**](a-repsto.md)                                                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Редакции**](a-revision.md)                                               | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Избежать**](a-rid.md)                                                         | Неверно     | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                                                       |
| [**SAM-имя учетной записи**](a-samaccountname.md)                                 | True      | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                                                       |
| [**SAM-тип учетной записи**](a-samaccounttype.md)                                 | Неверно     | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                                                       |
| [**SD-Rights-эффективен**](a-sdrightseffective.md)                           | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**секретарь**](a-secretary.md)                                             | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                               |
| [**Безопасность — идентификатор**](a-securityidentifier.md)                          | Неверно     | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                                                       |
| [**Server-Reference-BL**](a-serverreferencebl.md)                           | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Отображение в адресной книге**](a-showinaddressbook.md)                          | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                               |
| [**"Показать" — "Расширенный просмотр"**](a-showinadvancedviewonly.md)               | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**SID — журнал**](a-sidhistory.md)                                          | Неверно     | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                                                       |
| [**Site-Object-BL**](a-siteobjectbl.md)                                     | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Структурный объектный класс**](a-structuralobjectclass.md)                   | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Подразделы-ReFS**](a-subrefs.md)                                                | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**субсчемасубентри**](a-subschemasubentry.md)                             | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Дополнительные учетные данные**](a-supplementalcredentials.md)                | Неверно     | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                                                       |
| [**Системные флаги**](a-systemflags.md)                                        | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Номер телефона**](a-telephonenumber.md)                                | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                               |
| [**С текстовым кодированием или адресом**](a-textencodedoraddress.md)                    | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                               |
| [**Группы токенов**](a-tokengroups.md)                                        | Неверно     | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                                                       |
| [**Группы токенов — глобальные и универсальные**](a-tokengroupsglobalanduniversal.md) | Неверно     | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                                                       |
| [**Токены-группы-No-GC-приемлемые**](a-tokengroupsnogcacceptable.md)         | Неверно     | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                                                       |
| [**униксусерпассворд**](a-unixuserpassword.md)                               | Неверно     | [**посиксграуп**](c-posixgroup.md)<br/>                                                                                      |
| [**User-CERT**](a-usercert.md)                                              | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                               |
| [**Пароль пользователя**](a-userpassword.md)                                      | Неверно     | [**посиксграуп**](c-posixgroup.md)<br/>                                                                                      |
| [**Пользователь-SMIME-Certificate**](a-usersmimecertificate.md)                     | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                               |
| [**USN-изменено**](a-usnchanged.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Созданный USN**](a-usncreated.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**USN-DSA-Last-obj-removed**](a-usndsalastobjremoved.md)                   | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**USN — межсайтовая**](a-usnintersite.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Источник USN**](a-usnsource.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**WBEM — путь**](a-wbempath.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Хорошо известные объекты**](a-wellknownobjects.md)                             | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**При изменении**](a-whenchanged.md)                                        | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**При создании**](a-whencreated.md)                                        | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**WWW — Главная страница**](a-wwwhomepage.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**WWW-Page — другие**](a-url.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**X509 — CERT**](a-usercertificate.md)                                       | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                               |



## <a name="windows-server-2003-r2-extended-rights"></a>Расширенные права Windows Server 2003 R2

Этот класс содержит следующие расширенные права для Windows Server 2003 R2:



| Общее имя                  |
|------------------------------|
| [**Send-to**](r-send-to.md) |



## <a name="windows-server-2003-r2-validated-writes"></a>Проверенные операции записи в Windows Server 2003 R2

Этот класс содержит следующие проверенные операции записи для Windows Server 2003 R2:



| Общее имя                                  |
|----------------------------------------------|
| [**Самостоятельное членство**](r-self-membership.md) |



## <a name="windows-server-2003-r2-property-sets"></a>Наборы свойств Windows Server 2003 R2

Этот класс содержит следующие наборы свойств для Windows Server 2003 R2:



| Общее имя                                      |
|--------------------------------------------------|
| [**Электронная почта — сведения**](r-email-information.md) |



## <a name="windows-server-2008"></a>Windows Server 2008

-   [Атрибуты](#windows-server-2008-attributes)
-   [Расширенные права](#windows-server-2008-extended-rights)
-   [Проверенные записи](#windows-server-2008-validated-writes)
-   [Наборы свойств](#windows-server-2008-property-sets)



| Ввод | Значение |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Неверно                                                                                                                                                                                                                                                                                                            |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                                |
| По умолчанию — объект — Категория     | \-                                                                                                                                                                                                                                                                                                               |
| Governs-Id                  | 1.2.840.113556.1.5.8                                                                                                                                                                                                                                                                                             |
| По умолчанию-скрытие значения        | 0                                                                                                                                                                                                                                                                                                                |
| RDN-Атри-ID                  | [**Common-Name**](a-cn.md)<br/>                                                                                                                                                                                                                                                                           |
| Подкласс                 | [**Вверх**](c-top.md)<br/>                                                                                                                                                                                                                                                                                  |
| Возможные старшие          | [**Доменное**](c-domaindns.md)[**подразделение**](c-organizationalunit.md)Domain-DNS контейнер [**встроенных**](c-builtindomain.md)[**контейнеров**](c-container.md)[**MS-DS-AZ-Admin-Manager**](c-msds-azadminmanager.md)[**MS-DS-AZ-Application**](c-msds-azapplication.md)[**MS-DS-AZ-Scope**](c-msds-azscope.md) |
| Вспомогательные классы           | [**посиксграуп**](c-posixgroup.md)[**Security-Principal**](c-securityprincipal.md) (система)[**mail-получател**](c-mailrecipient.md) (System)                                                                                                                                                                   |
| NT-Security-дескриптор      | О:БАГ: BAD: S:                                                                                                                                                                                                                                                                                                     |
| Дескриптор безопасности по умолчанию | D: (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;;D А) (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;; SY) (A;; РПЛКЛОРК;;; AU) (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;; AO) (A;; РПЛКЛОРК;;; PS) (OA;; CR; ab721a55-1e2f-11D0-9819-00aa0040529b;; AU) (OA;; RP; 46a9b11d-60ae-405a-b7e8-ff8a58d456d2;; S-1-5-32-560)                                                   |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                       |



## <a name="windows-server-2008-attributes"></a>Атрибуты Windows Server 2008

Этот класс содержит следующие атрибуты для Windows Server 2008:



| attribute                                                                        | Обязательный | Унаследован от                                                                                                                       |
|----------------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Имя учетной записи — журнал**](a-accountnamehistory.md)                             | Неверно     | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                                                       |
| [**Число администраторов**](a-admincount.md)                                              | Неверно     | **Группа**                                                                                                                          |
| [**Описание администратора**](a-admindescription.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Имя администратора-отображение**](a-admindisplayname.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Allowed-Attributes**](a-allowedattributes.md)                                | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Allowed-Attributes-эффективен**](a-allowedattributeseffective.md)             | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Allowed-Child-classes**](a-allowedchildclasses.md)                           | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Allowed-Child-classes-эффективен**](a-allowedchildclasseseffective.md)        | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Alt-Security — удостоверения**](a-altsecurityidentities.md)                       | Неверно     | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                                                       |
| [**Плацдарм-Server-List-BL**](a-bridgeheadserverlistbl.md)                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Каноническое имя**](a-canonicalname.md)                                        | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Комментировать**](a-info.md)                                                        | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                               |
| [**Common-Name**](a-cn.md)                                                      | True      | [**Вверх**](c-top.md)<br/> [**посиксграуп**](c-posixgroup.md)<br/> [**Получатель почты**](c-mailrecipient.md)<br/> |
| [**Управление — права доступа**](a-controlaccessrights.md)                           | Неверно     | **Группа**                                                                                                                          |
| [**Метка времени создания**](a-createtimestamp.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Описание**](a-description.md)                                             | Неверно     | [**Вверх**](c-top.md)<br/> [**посиксграуп**](c-posixgroup.md)<br/>                                                      |
| [**Рабочий стол — профиль**](a-desktopprofile.md)                                      | Неверно     | **Группа**                                                                                                                          |
| [**Отображаемое имя**](a-displayname.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Отображаемое имя — печатаемое**](a-displaynameprintable.md)                         | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**DSA-Signature**](a-dsasignature.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**DS-Core-распространение-данные**](a-dscorepropagationdata.md)                      | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Адреса электронной почты**](a-mail.md)                                               | Неверно     | **Группа**                                                                                                                          |
| [**Имя расширения**](a-extensionname.md)                                        | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Метки**](a-flags.md)                                                         | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Из записи**](a-fromentry.md)                                                | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                        | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Мусор-Coll-период**](a-garbagecollperiod.md)                               | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                               |
| [**gidNumber**](a-gidnumber.md)                                                 | Неверно     | [**посиксграуп**](c-posixgroup.md)<br/>                                                                                      |
| [**Атрибуты группы**](a-groupattributes.md)                                    | Неверно     | **Группа**                                                                                                                          |
| [**Group-Membership-SAM**](a-groupmembershipsam.md)                             | Неверно     | **Группа**                                                                                                                          |
| [**Тип группы**](a-grouptype.md)                                                | True      | **Группа**                                                                                                                          |
| [**Тип экземпляра**](a-instancetype.md)                                          | True      | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Является критически важным — системный объект**](a-iscriticalsystemobject.md)                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Удалено**](a-isdeleted.md)                                                | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Входит в состав списка рассылки**](a-memberof.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Имеет права владельца**](a-isprivilegeholder.md)                               | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**лабеледури**](a-labeleduri.md)                                               | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                               |
| [**Последний-известный-родительский**](a-lastknownparent.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Устаревший — Exchange-DN**](a-legacyexchangedn.md)                                 | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                               |
| [**Под управлением**](a-managedby.md)                                                | Неверно     | **Группа**                                                                                                                          |
| [**Управляемые объекты**](a-managedobjects.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**В основном**](a-masteredby.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Член**](a-member.md)                                                       | Неверно     | **Группа**                                                                                                                          |
| [**мемберуид**](a-memberuid.md)                                                 | Неверно     | [**посиксграуп**](c-posixgroup.md)<br/>                                                                                      |
| [**Метка времени изменения**](a-modifytimestamp.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-COM-Партитионсетлинк**](a-mscom-partitionsetlink.md)                      | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-COM-Усерлинк**](a-mscom-userlink.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DFSR-Компутерреференцебл**](a-msdfsr-computerreferencebl.md)              | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DFSR-Мемберреференцебл**](a-msdfsr-memberreferencebl.md)                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-примерно-Иммед-подчиненные**](a-msds-approx-immed-subordinates.md)      | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Аусентикатедто-Аккаунтлист**](a-msds-authenticatedtoaccountlist.md)   | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-AZ-Application-Data**](a-msds-azapplicationdata.md)                    | Неверно     | **Группа**                                                                                                                          |
| [**MS-DS-AZ-BizTalk-Rule**](a-msds-azbizrule.md)                                    | Неверно     | **Группа**                                                                                                                          |
| [**MS-DS-AZ-BizTalk-Language**](a-msds-azbizrulelanguage.md)                   | Неверно     | **Группа**                                                                                                                          |
| [**MS-DS-AZ-Generic-Data**](a-msds-azgenericdata.md)                            | Неверно     | **Группа**                                                                                                                          |
| [**MS-DS-AZ-Last-Imported-BizTalk-Rule-Path**](a-msds-azlastimportedbizrulepath.md) | Неверно     | **Группа**                                                                                                                          |
| [**MS-DS-AZ-LDAP-Query**](a-msds-azldapquery.md)                                | Неверно     | **Группа**                                                                                                                          |
| [**MS-DS-AZ-Object-GUID**](a-msds-azobjectguid.md)                              | Неверно     | **Группа**                                                                                                                          |
| [**MS-DS-целостность-дочерняя — количество**](a-ms-ds-consistencychildcount.md)           | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Consistencу-Guid**](a-ms-ds-consistencyguid.md)                        | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS--домен — для**](a-msds-isdomainfor.md)                                | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-является-Full-реплика для**](a-msds-isfullreplicafor.md)                     | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-является-partial-реплика для**](a-msds-ispartialreplicafor.md)               | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Кэйверсионнумбер**](a-msds-keyversionnumber.md)                        | Неверно     | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                                                       |
| [**MS-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                              | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Masterd-by**](a-msds-masteredby.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)                | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-NC-REPL-курсоры**](a-msds-ncreplcursors.md)                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-NC-REPL-Inbound-соседи**](a-msds-ncreplinboundneighbors.md)         | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-NC-REPL-Outbound-соседи**](a-msds-ncreploutboundneighbors.md)       | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)    | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-NC-Type**](a-msds-nctype.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-не-члены**](a-msds-nonmembers.md)                                   | Неверно     | **Группа**                                                                                                                          |
| [**MS-DS-не-Members-BL**](a-msds-nonmembersbl.md)                              | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Operations-для-AZ-Role-BL**](a-msds-operationsforazrolebl.md)          | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)          | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-фонетическо-отображаемое имя**](a-msds-phoneticdisplayname.md)                | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                               |
| [**MS-DS-Principal-Name**](a-msds-principalname.md)                             | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-PSO — применяется**](a-msds-psoapplied.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-REPL-Attribute-Meta-Data**](a-msds-replattributemetadata.md)           | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)                   | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-выявил-DSA**](a-msds-revealeddsas.md)                               | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-выводит-List-BL**](a-msds-revealedlistbl.md)                          | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Tasks-для-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-дов-Assistant-Name**](a-msexchassistantname.md)                          | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                               |
| [**MS-дов-Лабеледури**](a-msexchlabeleduri.md)                                 | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                               |
| [**MS-дов-Owner-BL**](a-ownerbl.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Мссфу-30 — имя**](a-mssfu30name.md)                                           | Неверно     | **Группа**                                                                                                                          |
| [**Мссфу-30-NIS-домен**](a-mssfu30nisdomain.md)                                | Неверно     | **Группа**                                                                                                                          |
| [**Мссфу-30-POSIX-Member**](a-mssfu30posixmember.md)                            | Неверно     | **Группа**                                                                                                                          |
| [**Мссфу-30-POSIX-член-of**](a-mssfu30posixmemberof.md)                       | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**нетбут-SCP-BL**](a-netbootscpbl.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Не-Security-Member**](a-nonsecuritymember.md)                               | Неверно     | **Группа**                                                                                                                          |
| [**Не-Security-Member-BL**](a-nonsecuritymemberbl.md)                          | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**NT-Group-Members**](a-ntgroupmembers.md)                                     | Неверно     | **Группа**                                                                                                                          |
| [**NT-Security-дескриптор**](a-ntsecuritydescriptor.md)                         | True      | [**Вверх**](c-top.md)<br/> [**Безопасность — участник**](c-securityprincipal.md)<br/>                                       |
| [**Obj-расп-имя**](a-distinguishedname.md)                                     | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Объект — Категория**](a-objectcategory.md)                                      | True      | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Объектный класс**](a-objectclass.md)                                            | True      | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Объект — GUID**](a-objectguid.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Идентификатор безопасности объекта**](a-objectsid.md)                                                | True      | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                                                       |
| [**Версия объекта**](a-objectversion.md)                                        | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Оператор Count**](a-operatorcount.md)                                        | Неверно     | **Группа**                                                                                                                          |
| [**Другие хорошо известные объекты**](a-otherwellknownobjects.md)                      | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Разделяемый атрибут-удаление-список**](a-partialattributedeletionlist.md)        | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Разделяемый атрибут-set**](a-partialattributeset.md)                           | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Возможно — подстрочные**](a-possibleinferiors.md)                                | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Маркер первичной группы**](a-primarygrouptoken.md)                               | Неверно     | **Группа**                                                                                                                          |
| [**Прокси-объект-имя**](a-proxiedobjectname.md)                               | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Прокси-адреса**](a-proxyaddresses.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Запрос — политика — BL**](a-querypolicybl.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**RDN**](a-name.md)                                                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                        | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**REPL-Уптодате-Vector**](a-repluptodatevector.md)                             | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Отчеты**](a-directreports.md)                                               | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Представители — от**](a-repsfrom.md)                                                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Представители — кому**](a-repsto.md)                                                      | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Редакции**](a-revision.md)                                                   | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Избежать**](a-rid.md)                                                             | Неверно     | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                                                       |
| [**SAM-имя учетной записи**](a-samaccountname.md)                                     | True      | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                                                       |
| [**SAM-тип учетной записи**](a-samaccounttype.md)                                     | Неверно     | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                                                       |
| [**SD-Rights-эффективен**](a-sdrightseffective.md)                               | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**секретарь**](a-secretary.md)                                                 | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                               |
| [**Безопасность — идентификатор**](a-securityidentifier.md)                              | Неверно     | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                                                       |
| [**Server-Reference-BL**](a-serverreferencebl.md)                               | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Отображение в адресной книге**](a-showinaddressbook.md)                              | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                               |
| [**"Показать" — "Расширенный просмотр"**](a-showinadvancedviewonly.md)                   | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**SID — журнал**](a-sidhistory.md)                                              | Неверно     | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                                                       |
| [**Site-Object-BL**](a-siteobjectbl.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Структурный объектный класс**](a-structuralobjectclass.md)                       | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Подразделы-ReFS**](a-subrefs.md)                                                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**субсчемасубентри**](a-subschemasubentry.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Дополнительные учетные данные**](a-supplementalcredentials.md)                    | Неверно     | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                                                       |
| [**Системные флаги**](a-systemflags.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Номер телефона**](a-telephonenumber.md)                                    | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                               |
| [**С текстовым кодированием или адресом**](a-textencodedoraddress.md)                        | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                               |
| [**Группы токенов**](a-tokengroups.md)                                            | Неверно     | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                                                       |
| [**Группы токенов — глобальные и универсальные**](a-tokengroupsglobalanduniversal.md)     | Неверно     | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                                                       |
| [**Токены-группы-No-GC-приемлемые**](a-tokengroupsnogcacceptable.md)             | Неверно     | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                                                       |
| [**униксусерпассворд**](a-unixuserpassword.md)                                   | Неверно     | [**посиксграуп**](c-posixgroup.md)<br/>                                                                                      |
| [**User-CERT**](a-usercert.md)                                                  | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                               |
| [**Пароль пользователя**](a-userpassword.md)                                          | Неверно     | [**посиксграуп**](c-posixgroup.md)<br/>                                                                                      |
| [**Пользователь-SMIME-Certificate**](a-usersmimecertificate.md)                         | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                               |
| [**USN-изменено**](a-usnchanged.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Созданный USN**](a-usncreated.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**USN-DSA-Last-obj-removed**](a-usndsalastobjremoved.md)                       | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**USN — межсайтовая**](a-usnintersite.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Источник USN**](a-usnsource.md)                                                | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**WBEM — путь**](a-wbempath.md)                                                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Хорошо известные объекты**](a-wellknownobjects.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**При изменении**](a-whenchanged.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**При создании**](a-whencreated.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**WWW — Главная страница**](a-wwwhomepage.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**WWW-Page — другие**](a-url.md)                                                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**X509 — CERT**](a-usercertificate.md)                                           | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                               |



## <a name="windows-server-2008-extended-rights"></a>Расширенные права Windows Server 2008

Этот класс содержит следующие расширенные права для Windows Server 2008:



| Общее имя                  |
|------------------------------|
| [**Send-to**](r-send-to.md) |



## <a name="windows-server-2008-validated-writes"></a>Проверенные записи Windows Server 2008

Этот класс содержит следующие проверенные операции записи для Windows Server 2008:



| Общее имя                                  |
|----------------------------------------------|
| [**Самостоятельное членство**](r-self-membership.md) |



## <a name="windows-server-2008-property-sets"></a>Наборы свойств Windows Server 2008

Этот класс содержит следующие наборы свойств для Windows Server 2008:



| Общее имя                                      |
|--------------------------------------------------|
| [**Электронная почта — сведения**](r-email-information.md) |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2

-   [Атрибуты](#windows-server-2008-r2-attributes)
-   [Расширенные права](#windows-server-2008-r2-extended-rights)
-   [Проверенные записи](#windows-server-2008-r2-validated-writes)
-   [Наборы свойств](#windows-server-2008-r2-property-sets)



| Ввод | Значение |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Неверно                                                                                                                                                                                                                                                                                                            |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                                |
| По умолчанию — объект — Категория     | \-                                                                                                                                                                                                                                                                                                               |
| Governs-Id                  | 1.2.840.113556.1.5.8                                                                                                                                                                                                                                                                                             |
| По умолчанию-скрытие значения        | 0                                                                                                                                                                                                                                                                                                                |
| RDN-Атри-ID                  | [**Common-Name**](a-cn.md)<br/>                                                                                                                                                                                                                                                                           |
| Подкласс                 | [**Вверх**](c-top.md)<br/>                                                                                                                                                                                                                                                                                  |
| Возможные старшие          | [**Доменное**](c-domaindns.md)[**подразделение**](c-organizationalunit.md)Domain-DNS контейнер [**встроенных**](c-builtindomain.md)[**контейнеров**](c-container.md)[**MS-DS-AZ-Admin-Manager**](c-msds-azadminmanager.md)[**MS-DS-AZ-Application**](c-msds-azapplication.md)[**MS-DS-AZ-Scope**](c-msds-azscope.md) |
| Вспомогательные классы           | [**посиксграуп**](c-posixgroup.md)[**Security-Principal**](c-securityprincipal.md) (система)[**mail-получател**](c-mailrecipient.md) (System)                                                                                                                                                                   |
| NT-Security-дескриптор      | О:БАГ: BAD: S:                                                                                                                                                                                                                                                                                                     |
| Дескриптор безопасности по умолчанию | D: (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;;D А) (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;; SY) (A;; РПЛКЛОРК;;; AU) (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;; AO) (A;; РПЛКЛОРК;;; PS) (OA;; CR; ab721a55-1e2f-11D0-9819-00aa0040529b;; AU) (OA;; RP; 46a9b11d-60ae-405a-b7e8-ff8a58d456d2;; S-1-5-32-560)                                                   |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                       |



## <a name="windows-server-2008-r2-attributes"></a>Атрибуты Windows Server 2008 R2

Этот класс содержит следующие атрибуты для Windows Server 2008 R2:



| attribute                                                                        | Обязательный | Унаследован от                                                                                                                       |
|----------------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Имя учетной записи — журнал**](a-accountnamehistory.md)                             | Неверно     | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                                                       |
| [**Число администраторов**](a-admincount.md)                                              | Неверно     | **Группа**                                                                                                                          |
| [**Описание администратора**](a-admindescription.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Имя администратора-отображение**](a-admindisplayname.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Allowed-Attributes**](a-allowedattributes.md)                                | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Allowed-Attributes-эффективен**](a-allowedattributeseffective.md)             | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Allowed-Child-classes**](a-allowedchildclasses.md)                           | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Allowed-Child-classes-эффективен**](a-allowedchildclasseseffective.md)        | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Alt-Security — удостоверения**](a-altsecurityidentities.md)                       | Неверно     | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                                                       |
| [**Плацдарм-Server-List-BL**](a-bridgeheadserverlistbl.md)                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Каноническое имя**](a-canonicalname.md)                                        | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Комментировать**](a-info.md)                                                        | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                               |
| [**Common-Name**](a-cn.md)                                                      | True      | [**Вверх**](c-top.md)<br/> [**посиксграуп**](c-posixgroup.md)<br/> [**Получатель почты**](c-mailrecipient.md)<br/> |
| [**Управление — права доступа**](a-controlaccessrights.md)                           | Неверно     | **Группа**                                                                                                                          |
| [**Метка времени создания**](a-createtimestamp.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Описание**](a-description.md)                                             | Неверно     | [**Вверх**](c-top.md)<br/> [**посиксграуп**](c-posixgroup.md)<br/>                                                      |
| [**Рабочий стол — профиль**](a-desktopprofile.md)                                      | Неверно     | **Группа**                                                                                                                          |
| [**Отображаемое имя**](a-displayname.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Отображаемое имя — печатаемое**](a-displaynameprintable.md)                         | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**DSA-Signature**](a-dsasignature.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**DS-Core-распространение-данные**](a-dscorepropagationdata.md)                      | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Адреса электронной почты**](a-mail.md)                                               | Неверно     | **Группа**                                                                                                                          |
| [**Имя расширения**](a-extensionname.md)                                        | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Метки**](a-flags.md)                                                         | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Из записи**](a-fromentry.md)                                                | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                        | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Мусор-Coll-период**](a-garbagecollperiod.md)                               | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                               |
| [**gidNumber**](a-gidnumber.md)                                                 | Неверно     | [**посиксграуп**](c-posixgroup.md)<br/>                                                                                      |
| [**Атрибуты группы**](a-groupattributes.md)                                    | Неверно     | **Группа**                                                                                                                          |
| [**Group-Membership-SAM**](a-groupmembershipsam.md)                             | Неверно     | **Группа**                                                                                                                          |
| [**Тип группы**](a-grouptype.md)                                                | True      | **Группа**                                                                                                                          |
| [**Тип экземпляра**](a-instancetype.md)                                          | True      | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Является критически важным — системный объект**](a-iscriticalsystemobject.md)                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Удалено**](a-isdeleted.md)                                                | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Входит в состав списка рассылки**](a-memberof.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Имеет права владельца**](a-isprivilegeholder.md)                               | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Является перезапущенным**](a-isrecycled.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**лабеледури**](a-labeleduri.md)                                               | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                               |
| [**Последний-известный-родительский**](a-lastknownparent.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Устаревший — Exchange-DN**](a-legacyexchangedn.md)                                 | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                               |
| [**Под управлением**](a-managedby.md)                                                | Неверно     | **Группа**                                                                                                                          |
| [**Управляемые объекты**](a-managedobjects.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**В основном**](a-masteredby.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Член**](a-member.md)                                                       | Неверно     | **Группа**                                                                                                                          |
| [**мемберуид**](a-memberuid.md)                                                 | Неверно     | [**посиксграуп**](c-posixgroup.md)<br/>                                                                                      |
| [**Метка времени изменения**](a-modifytimestamp.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-COM-Партитионсетлинк**](a-mscom-partitionsetlink.md)                      | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-COM-Усерлинк**](a-mscom-userlink.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DFSR-Компутерреференцебл**](a-msdfsr-computerreferencebl.md)              | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DFSR-Мемберреференцебл**](a-msdfsr-memberreferencebl.md)                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-примерно-Иммед-подчиненные**](a-msds-approx-immed-subordinates.md)      | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Аусентикатедто-Аккаунтлист**](a-msds-authenticatedtoaccountlist.md)   | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-AZ-Application-Data**](a-msds-azapplicationdata.md)                    | Неверно     | **Группа**                                                                                                                          |
| [**MS-DS-AZ-BizTalk-Rule**](a-msds-azbizrule.md)                                    | Неверно     | **Группа**                                                                                                                          |
| [**MS-DS-AZ-BizTalk-Language**](a-msds-azbizrulelanguage.md)                   | Неверно     | **Группа**                                                                                                                          |
| [**MS-DS-AZ-Generic-Data**](a-msds-azgenericdata.md)                            | Неверно     | **Группа**                                                                                                                          |
| [**MS-DS-AZ-Last-Imported-BizTalk-Rule-Path**](a-msds-azlastimportedbizrulepath.md) | Неверно     | **Группа**                                                                                                                          |
| [**MS-DS-AZ-LDAP-Query**](a-msds-azldapquery.md)                                | Неверно     | **Группа**                                                                                                                          |
| [**MS-DS-AZ-Object-GUID**](a-msds-azobjectguid.md)                              | Неверно     | **Группа**                                                                                                                          |
| [**MS-DS-целостность-дочерняя — количество**](a-ms-ds-consistencychildcount.md)           | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Consistencу-Guid**](a-ms-ds-consistencyguid.md)                        | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Поддержка MS-DS-Feature-BL**](a-msds-enabledfeaturebl.md)                      | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)             | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS--домен — для**](a-msds-isdomainfor.md)                                | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-является-Full-реплика для**](a-msds-isfullreplicafor.md)                     | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-является-partial-реплика для**](a-msds-ispartialreplicafor.md)               | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Кэйверсионнумбер**](a-msds-keyversionnumber.md)                        | Неверно     | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                                                       |
| [**MS-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                              | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                              | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-локально-эффективное удаление — время**](a-msds-localeffectivedeletiontime.md) | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Local-эффективен — время перезапуска**](a-msds-localeffectiverecycletime.md)   | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Masterd-by**](a-msds-masteredby.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)                | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-NC-REPL-курсоры**](a-msds-ncreplcursors.md)                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-NC-REPL-Inbound-соседи**](a-msds-ncreplinboundneighbors.md)         | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-NC-REPL-Outbound-соседи**](a-msds-ncreploutboundneighbors.md)       | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)    | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-NC-Type**](a-msds-nctype.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-не-члены**](a-msds-nonmembers.md)                                   | Неверно     | **Группа**                                                                                                                          |
| [**MS-DS-не-Members-BL**](a-msds-nonmembersbl.md)                              | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Оидтограуп-Link-BL**](a-msds-oidtogrouplinkbl.md)                      | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Operations-для-AZ-Role-BL**](a-msds-operationsforazrolebl.md)          | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)          | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-фонетическо-отображаемое имя**](a-msds-phoneticdisplayname.md)                | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                               |
| [**MS-DS-Principal-Name**](a-msds-principalname.md)                             | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-PSO — применяется**](a-msds-psoapplied.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-REPL-Attribute-Meta-Data**](a-msds-replattributemetadata.md)           | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)                   | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-выявил-DSA**](a-msds-revealeddsas.md)                               | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-выводит-List-BL**](a-msds-revealedlistbl.md)                          | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Tasks-для-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-дов-Assistant-Name**](a-msexchassistantname.md)                          | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                               |
| [**MS-дов-Лабеледури**](a-msexchlabeleduri.md)                                 | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                               |
| [**MS-дов-Owner-BL**](a-ownerbl.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Мссфу-30 — имя**](a-mssfu30name.md)                                           | Неверно     | **Группа**                                                                                                                          |
| [**Мссфу-30-NIS-домен**](a-mssfu30nisdomain.md)                                | Неверно     | **Группа**                                                                                                                          |
| [**Мссфу-30-POSIX-Member**](a-mssfu30posixmember.md)                            | Неверно     | **Группа**                                                                                                                          |
| [**Мссфу-30-POSIX-член-of**](a-mssfu30posixmemberof.md)                       | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**нетбут-SCP-BL**](a-netbootscpbl.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Не-Security-Member**](a-nonsecuritymember.md)                               | Неверно     | **Группа**                                                                                                                          |
| [**Не-Security-Member-BL**](a-nonsecuritymemberbl.md)                          | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**NT-Group-Members**](a-ntgroupmembers.md)                                     | Неверно     | **Группа**                                                                                                                          |
| [**NT-Security-дескриптор**](a-ntsecuritydescriptor.md)                         | True      | [**Вверх**](c-top.md)<br/> [**Безопасность — участник**](c-securityprincipal.md)<br/>                                       |
| [**Obj-расп-имя**](a-distinguishedname.md)                                     | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Объект — Категория**](a-objectcategory.md)                                      | True      | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Объектный класс**](a-objectclass.md)                                            | True      | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Объект — GUID**](a-objectguid.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Идентификатор безопасности объекта**](a-objectsid.md)                                                | True      | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                                                       |
| [**Версия объекта**](a-objectversion.md)                                        | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Оператор Count**](a-operatorcount.md)                                        | Неверно     | **Группа**                                                                                                                          |
| [**Другие хорошо известные объекты**](a-otherwellknownobjects.md)                      | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Разделяемый атрибут-удаление-список**](a-partialattributedeletionlist.md)        | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Разделяемый атрибут-set**](a-partialattributeset.md)                           | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Возможно — подстрочные**](a-possibleinferiors.md)                                | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Маркер первичной группы**](a-primarygrouptoken.md)                               | Неверно     | **Группа**                                                                                                                          |
| [**Прокси-объект-имя**](a-proxiedobjectname.md)                               | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Прокси-адреса**](a-proxyaddresses.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Запрос — политика — BL**](a-querypolicybl.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**RDN**](a-name.md)                                                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                        | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**REPL-Уптодате-Vector**](a-repluptodatevector.md)                             | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Отчеты**](a-directreports.md)                                               | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Представители — от**](a-repsfrom.md)                                                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Представители — кому**](a-repsto.md)                                                      | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Редакции**](a-revision.md)                                                   | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Избежать**](a-rid.md)                                                             | Неверно     | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                                                       |
| [**SAM-имя учетной записи**](a-samaccountname.md)                                     | True      | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                                                       |
| [**SAM-тип учетной записи**](a-samaccounttype.md)                                     | Неверно     | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                                                       |
| [**SD-Rights-эффективен**](a-sdrightseffective.md)                               | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**секретарь**](a-secretary.md)                                                 | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                               |
| [**Безопасность — идентификатор**](a-securityidentifier.md)                              | Неверно     | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                                                       |
| [**Server-Reference-BL**](a-serverreferencebl.md)                               | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Отображение в адресной книге**](a-showinaddressbook.md)                              | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                               |
| [**"Показать" — "Расширенный просмотр"**](a-showinadvancedviewonly.md)                   | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**SID — журнал**](a-sidhistory.md)                                              | Неверно     | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                                                       |
| [**Site-Object-BL**](a-siteobjectbl.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Структурный объектный класс**](a-structuralobjectclass.md)                       | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Подразделы-ReFS**](a-subrefs.md)                                                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**субсчемасубентри**](a-subschemasubentry.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Дополнительные учетные данные**](a-supplementalcredentials.md)                    | Неверно     | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                                                       |
| [**Системные флаги**](a-systemflags.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Номер телефона**](a-telephonenumber.md)                                    | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                               |
| [**С текстовым кодированием или адресом**](a-textencodedoraddress.md)                        | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                               |
| [**Группы токенов**](a-tokengroups.md)                                            | Неверно     | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                                                       |
| [**Группы токенов — глобальные и универсальные**](a-tokengroupsglobalanduniversal.md)     | Неверно     | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                                                       |
| [**Токены-группы-No-GC-приемлемые**](a-tokengroupsnogcacceptable.md)             | Неверно     | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                                                       |
| [**униксусерпассворд**](a-unixuserpassword.md)                                   | Неверно     | [**посиксграуп**](c-posixgroup.md)<br/>                                                                                      |
| [**User-CERT**](a-usercert.md)                                                  | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                               |
| [**Пароль пользователя**](a-userpassword.md)                                          | Неверно     | [**посиксграуп**](c-posixgroup.md)<br/>                                                                                      |
| [**Пользователь-SMIME-Certificate**](a-usersmimecertificate.md)                         | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                               |
| [**USN-изменено**](a-usnchanged.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Созданный USN**](a-usncreated.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**USN-DSA-Last-obj-removed**](a-usndsalastobjremoved.md)                       | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**USN — межсайтовая**](a-usnintersite.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Источник USN**](a-usnsource.md)                                                | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**WBEM — путь**](a-wbempath.md)                                                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Хорошо известные объекты**](a-wellknownobjects.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**При изменении**](a-whenchanged.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**При создании**](a-whencreated.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**WWW — Главная страница**](a-wwwhomepage.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**WWW-Page — другие**](a-url.md)                                                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**X509 — CERT**](a-usercertificate.md)                                           | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                               |



## <a name="windows-server-2008-r2-extended-rights"></a>Расширенные права Windows Server 2008 R2

Этот класс содержит следующие расширенные права для Windows Server 2008 R2:



| Общее имя                  |
|------------------------------|
| [**Send-to**](r-send-to.md) |



## <a name="windows-server-2008-r2-validated-writes"></a>Проверенные операции записи в Windows Server 2008 R2

Этот класс содержит следующие проверенные операции записи для Windows Server 2008 R2:



| Общее имя                                  |
|----------------------------------------------|
| [**Самостоятельное членство**](r-self-membership.md) |



## <a name="windows-server-2008-r2-property-sets"></a>Наборы свойств Windows Server 2008 R2

Этот класс содержит следующие наборы свойств для Windows Server 2008 R2:



| Общее имя                                      |
|--------------------------------------------------|
| [**Электронная почта — сведения**](r-email-information.md) |



## <a name="windows-server-2012"></a>Windows Server 2012

-   [Атрибуты](#windows-server-2012-attributes)
-   [Расширенные права](#windows-server-2012-extended-rights)
-   [Проверенные записи](#windows-server-2012-validated-writes)
-   [Наборы свойств](#windows-server-2012-property-sets)



| Ввод | Значение |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Неверно                                                                                                                                                                                                                                                                                                            |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                                |
| По умолчанию — объект — Категория     | \-                                                                                                                                                                                                                                                                                                               |
| Governs-Id                  | 1.2.840.113556.1.5.8                                                                                                                                                                                                                                                                                             |
| По умолчанию-скрытие значения        | 0                                                                                                                                                                                                                                                                                                                |
| RDN-Атри-ID                  | [**Common-Name**](a-cn.md)<br/>                                                                                                                                                                                                                                                                           |
| Подкласс                 | [**Вверх**](c-top.md)<br/>                                                                                                                                                                                                                                                                                  |
| Возможные старшие          | [**Доменное**](c-domaindns.md)[**подразделение**](c-organizationalunit.md)Domain-DNS контейнер [**встроенных**](c-builtindomain.md)[**контейнеров**](c-container.md)[**MS-DS-AZ-Admin-Manager**](c-msds-azadminmanager.md)[**MS-DS-AZ-Application**](c-msds-azapplication.md)[**MS-DS-AZ-Scope**](c-msds-azscope.md) |
| Вспомогательные классы           | [**посиксграуп**](c-posixgroup.md)[**Security-Principal**](c-securityprincipal.md) (система)[**mail-получател**](c-mailrecipient.md) (System)                                                                                                                                                                   |
| NT-Security-дескриптор      | О:БАГ: BAD: S:                                                                                                                                                                                                                                                                                                     |
| Дескриптор безопасности по умолчанию | D: (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;;D А) (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;; SY) (A;; РПЛКЛОРК;;; AU) (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;; AO) (A;; РПЛКЛОРК;;; PS) (OA;; CR; ab721a55-1e2f-11D0-9819-00aa0040529b;; AU) (OA;; RP; 46a9b11d-60ae-405a-b7e8-ff8a58d456d2;; S-1-5-32-560)                                                   |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                       |



## <a name="windows-server-2012-attributes"></a>Атрибуты Windows Server 2012

Этот класс содержит следующие атрибуты для Windows Server 2012:



| attribute                                                                                    | Обязательный | Унаследован от                                                                                                                       |
|----------------------------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Имя учетной записи — журнал**](a-accountnamehistory.md)                                         | Неверно     | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                                                       |
| [**Число администраторов**](a-admincount.md)                                                          | Неверно     | **Группа**                                                                                                                          |
| [**Описание администратора**](a-admindescription.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Имя администратора-отображение**](a-admindisplayname.md)                                             | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Allowed-Attributes**](a-allowedattributes.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Allowed-Attributes-эффективен**](a-allowedattributeseffective.md)                         | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Allowed-Child-classes**](a-allowedchildclasses.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Allowed-Child-classes-эффективен**](a-allowedchildclasseseffective.md)                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Alt-Security — удостоверения**](a-altsecurityidentities.md)                                   | Неверно     | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                                                       |
| [**Плацдарм-Server-List-BL**](a-bridgeheadserverlistbl.md)                                | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Каноническое имя**](a-canonicalname.md)                                                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Комментировать**](a-info.md)                                                                    | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                               |
| [**Common-Name**](a-cn.md)                                                                  | True      | [**Вверх**](c-top.md)<br/> [**посиксграуп**](c-posixgroup.md)<br/> [**Получатель почты**](c-mailrecipient.md)<br/> |
| [**Управление — права доступа**](a-controlaccessrights.md)                                       | Неверно     | **Группа**                                                                                                                          |
| [**Метка времени создания**](a-createtimestamp.md)                                               | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Описание**](a-description.md)                                                         | Неверно     | [**Вверх**](c-top.md)<br/> [**посиксграуп**](c-posixgroup.md)<br/>                                                      |
| [**Рабочий стол — профиль**](a-desktopprofile.md)                                                  | Неверно     | **Группа**                                                                                                                          |
| [**Отображаемое имя**](a-displayname.md)                                                        | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Отображаемое имя — печатаемое**](a-displaynameprintable.md)                                     | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**DSA-Signature**](a-dsasignature.md)                                                      | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**DS-Core-распространение-данные**](a-dscorepropagationdata.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Адреса электронной почты**](a-mail.md)                                                           | Неверно     | **Группа**                                                                                                                          |
| [**Имя расширения**](a-extensionname.md)                                                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Метки**](a-flags.md)                                                                     | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Из записи**](a-fromentry.md)                                                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                                | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                                   | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Мусор-Coll-период**](a-garbagecollperiod.md)                                           | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                               |
| [**gidNumber**](a-gidnumber.md)                                                             | Неверно     | [**посиксграуп**](c-posixgroup.md)<br/>                                                                                      |
| [**Атрибуты группы**](a-groupattributes.md)                                                | Неверно     | **Группа**                                                                                                                          |
| [**Group-Membership-SAM**](a-groupmembershipsam.md)                                         | Неверно     | **Группа**                                                                                                                          |
| [**Тип группы**](a-grouptype.md)                                                            | True      | **Группа**                                                                                                                          |
| [**Тип экземпляра**](a-instancetype.md)                                                      | True      | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Является критически важным — системный объект**](a-iscriticalsystemobject.md)                                | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Удалено**](a-isdeleted.md)                                                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Входит в состав списка рассылки**](a-memberof.md)                                                        | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Имеет права владельца**](a-isprivilegeholder.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Является перезапущенным**](a-isrecycled.md)                                                          | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**лабеледури**](a-labeleduri.md)                                                           | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                               |
| [**Последний-известный-родительский**](a-lastknownparent.md)                                               | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Устаревший — Exchange-DN**](a-legacyexchangedn.md)                                             | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                               |
| [**Под управлением**](a-managedby.md)                                                            | Неверно     | **Группа**                                                                                                                          |
| [**Управляемые объекты**](a-managedobjects.md)                                                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**В основном**](a-masteredby.md)                                                          | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Член**](a-member.md)                                                                   | Неверно     | **Группа**                                                                                                                          |
| [**мемберуид**](a-memberuid.md)                                                             | Неверно     | [**посиксграуп**](c-posixgroup.md)<br/>                                                                                      |
| [**Метка времени изменения**](a-modifytimestamp.md)                                               | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-COM-Партитионсетлинк**](a-mscom-partitionsetlink.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-COM-Усерлинк**](a-mscom-userlink.md)                                                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DFSR-Компутерреференцебл**](a-msdfsr-computerreferencebl.md)                          | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DFSR-Мемберреференцебл**](a-msdfsr-memberreferencebl.md)                              | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-примерно-Иммед-подчиненные**](a-msds-approx-immed-subordinates.md)                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Аусентикатедто-Аккаунтлист**](a-msds-authenticatedtoaccountlist.md)               | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-AZ-Application-Data**](a-msds-azapplicationdata.md)                                | Неверно     | **Группа**                                                                                                                          |
| [**MS-DS-AZ-BizTalk-Rule**](a-msds-azbizrule.md)                                                | Неверно     | **Группа**                                                                                                                          |
| [**MS-DS-AZ-BizTalk-Language**](a-msds-azbizrulelanguage.md)                               | Неверно     | **Группа**                                                                                                                          |
| [**MS-DS-AZ-Generic-Data**](a-msds-azgenericdata.md)                                        | Неверно     | **Группа**                                                                                                                          |
| [**MS-DS-AZ-Last-Imported-BizTalk-Rule-Path**](a-msds-azlastimportedbizrulepath.md)             | Неверно     | **Группа**                                                                                                                          |
| [**MS-DS-AZ-LDAP-Query**](a-msds-azldapquery.md)                                            | Неверно     | **Группа**                                                                                                                          |
| [**MS-DS-AZ-Object-GUID**](a-msds-azobjectguid.md)                                          | Неверно     | **Группа**                                                                                                                          |
| [**MS-DS-ClaimSet-shares-возможные значения-with-BL**](a-msds-claimsharespossiblevalueswithbl.md) | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-целостность-дочерняя — количество**](a-ms-ds-consistencychildcount.md)                       | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Consistencу-Guid**](a-ms-ds-consistencyguid.md)                                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Поддержка MS-DS-Feature-BL**](a-msds-enabledfeaturebl.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-геокоординаты — высота**](a-msds-geocoordinatesaltitude.md)                       | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                               |
| [**MS-DS-геокоординаты — Широта**](a-msds-geocoordinateslatitude.md)                       | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                               |
| [**MS-DS-геокоординаты — Долгота**](a-msds-geocoordinateslongitude.md)                     | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                               |
| [**MS-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)                         | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS--домен — для**](a-msds-isdomainfor.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-является-Full-реплика для**](a-msds-isfullreplicafor.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-является-partial-реплика для**](a-msds-ispartialreplicafor.md)                           | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-является-PRIMARY-Computer-для**](a-msds-isprimarycomputerfor.md)                         | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Кэйверсионнумбер**](a-msds-keyversionnumber.md)                                    | Неверно     | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                                                       |
| [**MS-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-локально-эффективное удаление — время**](a-msds-localeffectivedeletiontime.md)             | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Local-эффективен — время перезапуска**](a-msds-localeffectiverecycletime.md)               | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Masterd-by**](a-msds-masteredby.md)                                               | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Members-of-Resource-Property-List-BL**](a-msds-membersofresourcepropertylistbl.md) | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-NC-REPL-курсоры**](a-msds-ncreplcursors.md)                                        | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-NC-REPL-Inbound-соседи**](a-msds-ncreplinboundneighbors.md)                     | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-NC-REPL-Outbound-соседи**](a-msds-ncreploutboundneighbors.md)                   | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)                | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-NC-Type**](a-msds-nctype.md)                                                       | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-не-члены**](a-msds-nonmembers.md)                                               | Неверно     | **Группа**                                                                                                                          |
| [**MS-DS-не-Members-BL**](a-msds-nonmembersbl.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                                | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Оидтограуп-Link-BL**](a-msds-oidtogrouplinkbl.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Operations-для-AZ-Role-BL**](a-msds-operationsforazrolebl.md)                      | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)                      | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-фонетическо-отображаемое имя**](a-msds-phoneticdisplayname.md)                            | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                               |
| [**MS-DS-PRIMARY-Computer**](a-msds-primarycomputer.md)                                     | Неверно     | **Группа**                                                                                                                          |
| [**MS-DS-Principal-Name**](a-msds-principalname.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-PSO — применяется**](a-msds-psoapplied.md)                                               | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-REPL-Attribute-Meta-Data**](a-msds-replattributemetadata.md)                       | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)                               | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-выявил-DSA**](a-msds-revealeddsas.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-выводит-List-BL**](a-msds-revealedlistbl.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Tasks-для-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                                | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                                | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-TDO-исходящий трафик — BL**](a-msds-tdoegressbl.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-TDO-входящий трафик — BL**](a-msds-tdoingressbl.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-value-type-Reference-BL**](a-msds-valuetypereferencebl.md)                         | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**MS-дов-Assistant-Name**](a-msexchassistantname.md)                                      | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                               |
| [**MS-дов-Лабеледури**](a-msexchlabeleduri.md)                                             | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                               |
| [**MS-дов-Owner-BL**](a-ownerbl.md)                                                        | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Мссфу-30 — имя**](a-mssfu30name.md)                                                       | Неверно     | **Группа**                                                                                                                          |
| [**Мссфу-30-NIS-домен**](a-mssfu30nisdomain.md)                                            | Неверно     | **Группа**                                                                                                                          |
| [**Мссфу-30-POSIX-Member**](a-mssfu30posixmember.md)                                        | Неверно     | **Группа**                                                                                                                          |
| [**Мссфу-30-POSIX-член-of**](a-mssfu30posixmemberof.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**нетбут-SCP-BL**](a-netbootscpbl.md)                                                     | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Не-Security-Member**](a-nonsecuritymember.md)                                           | Неверно     | **Группа**                                                                                                                          |
| [**Не-Security-Member-BL**](a-nonsecuritymemberbl.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**NT-Group-Members**](a-ntgroupmembers.md)                                                 | Неверно     | **Группа**                                                                                                                          |
| [**NT-Security-дескриптор**](a-ntsecuritydescriptor.md)                                     | True      | [**Вверх**](c-top.md)<br/> [**Безопасность — участник**](c-securityprincipal.md)<br/>                                       |
| [**Obj-расп-имя**](a-distinguishedname.md)                                                 | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Объект — Категория**](a-objectcategory.md)                                                  | True      | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Объектный класс**](a-objectclass.md)                                                        | True      | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Объект — GUID**](a-objectguid.md)                                                          | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Идентификатор безопасности объекта**](a-objectsid.md)                                                            | True      | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                                                       |
| [**Версия объекта**](a-objectversion.md)                                                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Оператор Count**](a-operatorcount.md)                                                    | Неверно     | **Группа**                                                                                                                          |
| [**Другие хорошо известные объекты**](a-otherwellknownobjects.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Разделяемый атрибут-удаление-список**](a-partialattributedeletionlist.md)                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Разделяемый атрибут-set**](a-partialattributeset.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Возможно — подстрочные**](a-possibleinferiors.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Маркер первичной группы**](a-primarygrouptoken.md)                                           | Неверно     | **Группа**                                                                                                                          |
| [**Прокси-объект-имя**](a-proxiedobjectname.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Прокси-адреса**](a-proxyaddresses.md)                                                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Запрос — политика — BL**](a-querypolicybl.md)                                                   | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**RDN**](a-name.md)                                                                        | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**REPL-Уптодате-Vector**](a-repluptodatevector.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Отчеты**](a-directreports.md)                                                           | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Представители — от**](a-repsfrom.md)                                                              | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Представители — кому**](a-repsto.md)                                                                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Редакции**](a-revision.md)                                                               | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Избежать**](a-rid.md)                                                                         | Неверно     | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                                                       |
| [**SAM-имя учетной записи**](a-samaccountname.md)                                                 | True      | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                                                       |
| [**SAM-тип учетной записи**](a-samaccounttype.md)                                                 | Неверно     | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                                                       |
| [**SD-Rights-эффективен**](a-sdrightseffective.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**секретарь**](a-secretary.md)                                                             | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                               |
| [**Безопасность — идентификатор**](a-securityidentifier.md)                                          | Неверно     | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                                                       |
| [**Server-Reference-BL**](a-serverreferencebl.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Отображение в адресной книге**](a-showinaddressbook.md)                                          | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                               |
| [**"Показать" — "Расширенный просмотр"**](a-showinadvancedviewonly.md)                               | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**SID — журнал**](a-sidhistory.md)                                                          | Неверно     | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                                                       |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                     | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Структурный объектный класс**](a-structuralobjectclass.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Подразделы-ReFS**](a-subrefs.md)                                                                | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**субсчемасубентри**](a-subschemasubentry.md)                                             | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Дополнительные учетные данные**](a-supplementalcredentials.md)                                | Неверно     | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                                                       |
| [**Системные флаги**](a-systemflags.md)                                                        | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Номер телефона**](a-telephonenumber.md)                                                | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                               |
| [**С текстовым кодированием или адресом**](a-textencodedoraddress.md)                                    | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                               |
| [**Группы токенов**](a-tokengroups.md)                                                        | Неверно     | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                                                       |
| [**Группы токенов — глобальные и универсальные**](a-tokengroupsglobalanduniversal.md)                 | Неверно     | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                                                       |
| [**Токены-группы-No-GC-приемлемые**](a-tokengroupsnogcacceptable.md)                         | Неверно     | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                                                       |
| [**униксусерпассворд**](a-unixuserpassword.md)                                               | Неверно     | [**посиксграуп**](c-posixgroup.md)<br/>                                                                                      |
| [**User-CERT**](a-usercert.md)                                                              | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                               |
| [**Пароль пользователя**](a-userpassword.md)                                                      | Неверно     | [**посиксграуп**](c-posixgroup.md)<br/>                                                                                      |
| [**Пользователь-SMIME-Certificate**](a-usersmimecertificate.md)                                     | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                               |
| [**USN-изменено**](a-usnchanged.md)                                                          | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Созданный USN**](a-usncreated.md)                                                          | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**USN-DSA-Last-obj-removed**](a-usndsalastobjremoved.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**USN — межсайтовая**](a-usnintersite.md)                                                      | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Источник USN**](a-usnsource.md)                                                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**WBEM — путь**](a-wbempath.md)                                                              | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**Хорошо известные объекты**](a-wellknownobjects.md)                                             | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**При изменении**](a-whenchanged.md)                                                        | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**При создании**](a-whencreated.md)                                                        | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**WWW — Главная страница**](a-wwwhomepage.md)                                                       | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**WWW-Page — другие**](a-url.md)                                                              | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                    |
| [**X509 — CERT**](a-usercertificate.md)                                                       | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                               |



## <a name="windows-server-2012-extended-rights"></a>Расширенные права Windows Server 2012

Этот класс содержит следующие расширенные права для Windows Server 2012:



| Общее имя                  |
|------------------------------|
| [**Send-to**](r-send-to.md) |



## <a name="windows-server-2012-validated-writes"></a>Проверенные записи Windows Server 2012

Этот класс содержит следующие проверенные операции записи для Windows Server 2012:



| Общее имя                                  |
|----------------------------------------------|
| [**Самостоятельное членство**](r-self-membership.md) |



## <a name="windows-server-2012-property-sets"></a>Наборы свойств Windows Server 2012

Этот класс содержит следующие наборы свойств для Windows Server 2012:



| Общее имя                                      |
|--------------------------------------------------|
| [**Электронная почта — сведения**](r-email-information.md) |



 

 





