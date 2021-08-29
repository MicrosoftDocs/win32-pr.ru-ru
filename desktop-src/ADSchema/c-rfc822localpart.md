---
title: класс rFC822LocalPart
description: Используется для определения записей, представляющих локальную часть адресов электронной почты.
ms.assetid: 1df90e93-d7eb-42c8-b216-6046a83d0ada
ms.tgt_platform: multiple
keywords:
- Схема AD класса rFC822LocalPart
topic_type:
- apiref
api_name:
- rFC822LocalPart
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24d948a759dbbf593a40b8335e4c7e64506d14af88cc97dfe8c1a900037a3fee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118959583"
---
# <a name="rfc822localpart-class"></a>класс rFC822LocalPart

Используется для определения записей, представляющих локальную часть адресов электронной почты.



| Ввод | Значение |
|-------------------|--------------------------------------|
| CN                | rFC822LocalPart                      |
| LDAP-отображаемое имя | rFC822LocalPart                      |
| Привилегия обновления  | \-                                   |
| Частота обновления  | \-                                   |
| Schema-ID-GUID    | b93e3a78-cbae-485e-a07b-5ef4ae505686 |



## <a name="implementations"></a>Варианты реализации решения

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003

-   [Атрибуты](#windows-server-2003-attributes)



| Ввод | Значение |
|-----------------------------|--------------------------------------------------------------------------------------------------|
| System-Only                 | Неверно                                                                                            |
| Object-Category             | 1                                                                                                |
| По умолчанию — объект — Категория     | \-                                                                                               |
| Governs-Id                  | 0.9.2342.19200300.100.4.14                                                                       |
| По умолчанию-скрытие значения        | 1                                                                                                |
| RDN-Атри-ID                  | [**Common-Name**](a-cn.md)<br/>                                                           |
| Подкласс                 | [**Домен**](c-domain.md)<br/>                                                            |
| Возможные старшие          | [](c-container.md)[**Организационная единица** контейнера](c-organizationalunit.md)              |
| Вспомогательные классы           | \-                                                                                               |
| NT-Security-дескриптор      | О:БАГ: BAD: S:                                                                                     |
| Дескриптор безопасности по умолчанию | D: (A;; РПВПКРККДКЛКЛОЛОРКВОВДСДДТДТСВ;;;D А) (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;; SY) (A;; РПЛКЛОРК;;; СЛУЖБЫ |
| System-Flags                | 0x00000000                                                                                       |



## <a name="windows-server-2003-attributes"></a>Windows Атрибуты сервера 2003

этот класс содержит следующие атрибуты для Windows Server 2003:



| attribute                                                                   | Обязательный | Унаследован от                                        |
|-----------------------------------------------------------------------------|-----------|-----------------------------------------------------|
| [**Описание администратора**](a-admindescription.md)                             | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Имя администратора-отображение**](a-admindisplayname.md)                            | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Allowed-Attributes**](a-allowedattributes.md)                           | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Allowed-Attributes-эффективен**](a-allowedattributeseffective.md)        | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Allowed-Child-classes**](a-allowedchildclasses.md)                      | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Allowed-Child-classes-эффективен**](a-allowedchildclasseseffective.md)   | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Плацдарм-Server-List-BL**](a-bridgeheadserverlistbl.md)               | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Каноническое имя**](a-canonicalname.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Common-Name**](a-cn.md)                                                 | Неверно     | **rFC822LocalPart** [ **сверху**](c-top.md)<br/> |
| [**Метка времени создания**](a-createtimestamp.md)                              | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Описание**](a-description.md)                                        | Неверно     | **rFC822LocalPart** [ **сверху**](c-top.md)<br/> |
| [**Целевой индикатор**](a-destinationindicator.md)                     | Неверно     | **rFC822LocalPart**                                 |
| [**Отображаемое имя**](a-displayname.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Отображаемое имя — печатаемое**](a-displaynameprintable.md)                    | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Компонент домена**](a-dc.md)                                            | Верно      | [**Домен**](c-domain.md)<br/>               |
| [**DSA-Signature**](a-dsasignature.md)                                     | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**DS-Core-распространение-данные**](a-dscorepropagationdata.md)                 | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Имя расширения**](a-extensionname.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Факс-телефон — номер**](a-facsimiletelephonenumber.md)            | Неверно     | **rFC822LocalPart**                                 |
| [**Метки**](a-flags.md)                                                    | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Из записи**](a-fromentry.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Тип экземпляра**](a-instancetype.md)                                     | Верно      | [**Вверх**](c-top.md)<br/>                     |
| [**Международный-ISDN-номер**](a-internationalisdnnumber.md)              | Неверно     | **rFC822LocalPart**                                 |
| [**Является критически важным — системный объект**](a-iscriticalsystemobject.md)               | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Удалено**](a-isdeleted.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Входит в состав списка рассылки**](a-memberof.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Имеет права владельца**](a-isprivilegeholder.md)                          | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Последний-известный-родительский**](a-lastknownparent.md)                              | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Управляемые объекты**](a-managedobjects.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**В основном**](a-masteredby.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Метка времени изменения**](a-modifytimestamp.md)                              | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-COM-Партитионсетлинк**](a-mscom-partitionsetlink.md)                 | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-COM-Усерлинк**](a-mscom-userlink.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-примерно-Иммед-подчиненные**](a-msds-approx-immed-subordinates.md) | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-целостность-дочерняя — количество**](a-ms-ds-consistencychildcount.md)      | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-Consistencу-Guid**](a-ms-ds-consistencyguid.md)                   | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-Masterd-by**](a-msds-masteredby.md)                              | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)           | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-NC-REPL-курсоры**](a-msds-ncreplcursors.md)                       | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-NC-REPL-Inbound-соседи**](a-msds-ncreplinboundneighbors.md)    | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-NC-REPL-Outbound-соседи**](a-msds-ncreploutboundneighbors.md)  | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-не-Members-BL**](a-msds-nonmembersbl.md)                         | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-Operations-для-AZ-Role-BL**](a-msds-operationsforazrolebl.md)     | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)     | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-REPL-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)              | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-Tasks-для-AZ-Role-BL**](a-msds-tasksforazrolebl.md)               | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)               | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-дов-Owner-BL**](a-ownerbl.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**нетбут-SCP-BL**](a-netbootscpbl.md)                                    | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Не-Security-Member-BL**](a-nonsecuritymemberbl.md)                     | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**NT-Security-дескриптор**](a-ntsecuritydescriptor.md)                    | Верно      | [**Вверх**](c-top.md)<br/>                     |
| [**Obj-расп-имя**](a-distinguishedname.md)                                | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Объект — Категория**](a-objectcategory.md)                                 | Верно      | [**Вверх**](c-top.md)<br/>                     |
| [**Объектный класс**](a-objectclass.md)                                       | Верно      | [**Вверх**](c-top.md)<br/>                     |
| [**Объект — GUID**](a-objectguid.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Версия объекта**](a-objectversion.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Другие хорошо известные объекты**](a-otherwellknownobjects.md)                 | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Разделяемый атрибут-удаление-список**](a-partialattributedeletionlist.md)   | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Разделяемый атрибут-set**](a-partialattributeset.md)                      | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**физическая доставка — Office-имя**](a-physicaldeliveryofficename.md)       | Неверно     | **rFC822LocalPart**                                 |
| [**Возможно — подстрочные**](a-possibleinferiors.md)                           | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Почтовый адрес**](a-postaladdress.md)                                   | Неверно     | **rFC822LocalPart**                                 |
| [**Почтовый код**](a-postalcode.md)                                         | Неверно     | **rFC822LocalPart**                                 |
| [**флажок после Office**](a-postofficebox.md)                                  | Неверно     | **rFC822LocalPart**                                 |
| [**Предпочтительный метод доставки**](a-preferreddeliverymethod.md)              | Неверно     | **rFC822LocalPart**                                 |
| [**Прокси-объект-имя**](a-proxiedobjectname.md)                          | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Прокси-адреса**](a-proxyaddresses.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Запрос — политика — BL**](a-querypolicybl.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**RDN**](a-name.md)                                                       | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Зарегистрированный адрес**](a-registeredaddress.md)                           | Неверно     | **rFC822LocalPart**                                 |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                   | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**REPL-Уптодате-Vector**](a-repluptodatevector.md)                        | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Отчеты**](a-directreports.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Представители — от**](a-repsfrom.md)                                             | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Представители — кому**](a-repsto.md)                                                 | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Редакции**](a-revision.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**SD-Rights-эффективен**](a-sdrightseffective.md)                          | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**См. также**](a-seealso.md)                                               | Неверно     | **rFC822LocalPart**                                 |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**"Показать" — "Расширенный просмотр"**](a-showinadvancedviewonly.md)              | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Улица-адрес**](a-street.md)                                          | Неверно     | **rFC822LocalPart**                                 |
| [**Структурный объектный класс**](a-structuralobjectclass.md)                  | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Подразделы-ReFS**](a-subrefs.md)                                               | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**субсчемасубентри**](a-subschemasubentry.md)                            | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Образование**](a-sn.md)                                                     | Неверно     | **rFC822LocalPart**                                 |
| [**Системные флаги**](a-systemflags.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Номер телефона**](a-telephonenumber.md)                               | Неверно     | **rFC822LocalPart**                                 |
| [**Teletex — идентификатор терминала**](a-teletexterminalidentifier.md)          | Неверно     | **rFC822LocalPart**                                 |
| [**Номер телекса**](a-telexnumber.md)                                       | Неверно     | **rFC822LocalPart**                                 |
| [**USN-изменено**](a-usnchanged.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Созданный USN**](a-usncreated.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**USN-DSA-Last-obj-removed**](a-usndsalastobjremoved.md)                  | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**USN — межсайтовая**](a-usnintersite.md)                                     | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Источник USN**](a-usnsource.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**WBEM — путь**](a-wbempath.md)                                             | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Хорошо известные объекты**](a-wellknownobjects.md)                            | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**При изменении**](a-whenchanged.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**При создании**](a-whencreated.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**WWW — Главная страница**](a-wwwhomepage.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**WWW-Page — другие**](a-url.md)                                             | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**X121 — адрес**](a-x121address.md)                                       | Неверно     | **rFC822LocalPart**                                 |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2

-   [Атрибуты](#windows-server-2003-r2-attributes)



| Ввод | Значение |
|-----------------------------|--------------------------------------------------------------------------------------------------|
| System-Only                 | Неверно                                                                                            |
| Object-Category             | 1                                                                                                |
| По умолчанию — объект — Категория     | \-                                                                                               |
| Governs-Id                  | 0.9.2342.19200300.100.4.14                                                                       |
| По умолчанию-скрытие значения        | 1                                                                                                |
| RDN-Атри-ID                  | [**Common-Name**](a-cn.md)<br/>                                                           |
| Подкласс                 | [**Домен**](c-domain.md)<br/>                                                            |
| Возможные старшие          | [](c-container.md)[**Организационная единица** контейнера](c-organizationalunit.md)              |
| Вспомогательные классы           | \-                                                                                               |
| NT-Security-дескриптор      | О:БАГ: BAD: S:                                                                                     |
| Дескриптор безопасности по умолчанию | D: (A;; РПВПКРККДКЛКЛОЛОРКВОВДСДДТДТСВ;;;D А) (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;; SY) (A;; РПЛКЛОРК;;; СЛУЖБЫ |
| System-Flags                | 0x00000000                                                                                       |



## <a name="windows-server-2003-r2-attributes"></a>Windows Атрибуты сервера 2003 R2

этот класс содержит следующие атрибуты для Windows Server 2003 R2:



| attribute                                                                   | Обязательный | Унаследован от                                        |
|-----------------------------------------------------------------------------|-----------|-----------------------------------------------------|
| [**Описание администратора**](a-admindescription.md)                             | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Имя администратора-отображение**](a-admindisplayname.md)                            | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Allowed-Attributes**](a-allowedattributes.md)                           | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Allowed-Attributes-эффективен**](a-allowedattributeseffective.md)        | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Allowed-Child-classes**](a-allowedchildclasses.md)                      | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Allowed-Child-classes-эффективен**](a-allowedchildclasseseffective.md)   | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Плацдарм-Server-List-BL**](a-bridgeheadserverlistbl.md)               | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Каноническое имя**](a-canonicalname.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Common-Name**](a-cn.md)                                                 | Неверно     | **rFC822LocalPart** [ **сверху**](c-top.md)<br/> |
| [**Метка времени создания**](a-createtimestamp.md)                              | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Описание**](a-description.md)                                        | Неверно     | **rFC822LocalPart** [ **сверху**](c-top.md)<br/> |
| [**Целевой индикатор**](a-destinationindicator.md)                     | Неверно     | **rFC822LocalPart**                                 |
| [**Отображаемое имя**](a-displayname.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Отображаемое имя — печатаемое**](a-displaynameprintable.md)                    | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Компонент домена**](a-dc.md)                                            | Верно      | [**Домен**](c-domain.md)<br/>               |
| [**DSA-Signature**](a-dsasignature.md)                                     | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**DS-Core-распространение-данные**](a-dscorepropagationdata.md)                 | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Имя расширения**](a-extensionname.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Факс-телефон — номер**](a-facsimiletelephonenumber.md)            | Неверно     | **rFC822LocalPart**                                 |
| [**Метки**](a-flags.md)                                                    | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Из записи**](a-fromentry.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Тип экземпляра**](a-instancetype.md)                                     | Верно      | [**Вверх**](c-top.md)<br/>                     |
| [**Международный-ISDN-номер**](a-internationalisdnnumber.md)              | Неверно     | **rFC822LocalPart**                                 |
| [**Является критически важным — системный объект**](a-iscriticalsystemobject.md)               | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Удалено**](a-isdeleted.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Входит в состав списка рассылки**](a-memberof.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Имеет права владельца**](a-isprivilegeholder.md)                          | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Последний-известный-родительский**](a-lastknownparent.md)                              | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Управляемые объекты**](a-managedobjects.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**В основном**](a-masteredby.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Метка времени изменения**](a-modifytimestamp.md)                              | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-COM-Партитионсетлинк**](a-mscom-partitionsetlink.md)                 | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-COM-Усерлинк**](a-mscom-userlink.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DFSR-Компутерреференцебл**](a-msdfsr-computerreferencebl.md)         | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DFSR-Мемберреференцебл**](a-msdfsr-memberreferencebl.md)             | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-примерно-Иммед-подчиненные**](a-msds-approx-immed-subordinates.md) | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-целостность-дочерняя — количество**](a-ms-ds-consistencychildcount.md)      | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-Consistencу-Guid**](a-ms-ds-consistencyguid.md)                   | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-Masterd-by**](a-msds-masteredby.md)                              | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)           | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-NC-REPL-курсоры**](a-msds-ncreplcursors.md)                       | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-NC-REPL-Inbound-соседи**](a-msds-ncreplinboundneighbors.md)    | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-NC-REPL-Outbound-соседи**](a-msds-ncreploutboundneighbors.md)  | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-не-Members-BL**](a-msds-nonmembersbl.md)                         | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-Operations-для-AZ-Role-BL**](a-msds-operationsforazrolebl.md)     | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)     | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-REPL-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)              | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-Tasks-для-AZ-Role-BL**](a-msds-tasksforazrolebl.md)               | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)               | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-дов-Owner-BL**](a-ownerbl.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Мссфу-30-POSIX-член-of**](a-mssfu30posixmemberof.md)                  | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**нетбут-SCP-BL**](a-netbootscpbl.md)                                    | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Не-Security-Member-BL**](a-nonsecuritymemberbl.md)                     | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**NT-Security-дескриптор**](a-ntsecuritydescriptor.md)                    | Верно      | [**Вверх**](c-top.md)<br/>                     |
| [**Obj-расп-имя**](a-distinguishedname.md)                                | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Объект — Категория**](a-objectcategory.md)                                 | Верно      | [**Вверх**](c-top.md)<br/>                     |
| [**Объектный класс**](a-objectclass.md)                                       | Верно      | [**Вверх**](c-top.md)<br/>                     |
| [**Объект — GUID**](a-objectguid.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Версия объекта**](a-objectversion.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Другие хорошо известные объекты**](a-otherwellknownobjects.md)                 | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Разделяемый атрибут-удаление-список**](a-partialattributedeletionlist.md)   | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Разделяемый атрибут-set**](a-partialattributeset.md)                      | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**физическая доставка — Office-имя**](a-physicaldeliveryofficename.md)       | Неверно     | **rFC822LocalPart**                                 |
| [**Возможно — подстрочные**](a-possibleinferiors.md)                           | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Почтовый адрес**](a-postaladdress.md)                                   | Неверно     | **rFC822LocalPart**                                 |
| [**Почтовый код**](a-postalcode.md)                                         | Неверно     | **rFC822LocalPart**                                 |
| [**флажок после Office**](a-postofficebox.md)                                  | Неверно     | **rFC822LocalPart**                                 |
| [**Предпочтительный метод доставки**](a-preferreddeliverymethod.md)              | Неверно     | **rFC822LocalPart**                                 |
| [**Прокси-объект-имя**](a-proxiedobjectname.md)                          | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Прокси-адреса**](a-proxyaddresses.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Запрос — политика — BL**](a-querypolicybl.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**RDN**](a-name.md)                                                       | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Зарегистрированный адрес**](a-registeredaddress.md)                           | Неверно     | **rFC822LocalPart**                                 |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                   | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**REPL-Уптодате-Vector**](a-repluptodatevector.md)                        | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Отчеты**](a-directreports.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Представители — от**](a-repsfrom.md)                                             | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Представители — кому**](a-repsto.md)                                                 | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Редакции**](a-revision.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**SD-Rights-эффективен**](a-sdrightseffective.md)                          | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**См. также**](a-seealso.md)                                               | Неверно     | **rFC822LocalPart**                                 |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**"Показать" — "Расширенный просмотр"**](a-showinadvancedviewonly.md)              | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Улица-адрес**](a-street.md)                                          | Неверно     | **rFC822LocalPart**                                 |
| [**Структурный объектный класс**](a-structuralobjectclass.md)                  | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Подразделы-ReFS**](a-subrefs.md)                                               | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**субсчемасубентри**](a-subschemasubentry.md)                            | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Образование**](a-sn.md)                                                     | Неверно     | **rFC822LocalPart**                                 |
| [**Системные флаги**](a-systemflags.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Номер телефона**](a-telephonenumber.md)                               | Неверно     | **rFC822LocalPart**                                 |
| [**Teletex — идентификатор терминала**](a-teletexterminalidentifier.md)          | Неверно     | **rFC822LocalPart**                                 |
| [**Номер телекса**](a-telexnumber.md)                                       | Неверно     | **rFC822LocalPart**                                 |
| [**USN-изменено**](a-usnchanged.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Созданный USN**](a-usncreated.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**USN-DSA-Last-obj-removed**](a-usndsalastobjremoved.md)                  | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**USN — межсайтовая**](a-usnintersite.md)                                     | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Источник USN**](a-usnsource.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**WBEM — путь**](a-wbempath.md)                                             | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Хорошо известные объекты**](a-wellknownobjects.md)                            | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**При изменении**](a-whenchanged.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**При создании**](a-whencreated.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**WWW — Главная страница**](a-wwwhomepage.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**WWW-Page — другие**](a-url.md)                                             | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**X121 — адрес**](a-x121address.md)                                       | Неверно     | **rFC822LocalPart**                                 |



## <a name="windows-server-2008"></a>Windows Server 2008

-   [Атрибуты](#windows-server-2008-attributes)



| Ввод | Значение |
|-----------------------------|--------------------------------------------------------------------------------------------------|
| System-Only                 | Неверно                                                                                            |
| Object-Category             | 1                                                                                                |
| По умолчанию — объект — Категория     | \-                                                                                               |
| Governs-Id                  | 0.9.2342.19200300.100.4.14                                                                       |
| По умолчанию-скрытие значения        | 1                                                                                                |
| RDN-Атри-ID                  | [**Common-Name**](a-cn.md)<br/>                                                           |
| Подкласс                 | [**Домен**](c-domain.md)<br/>                                                            |
| Возможные старшие          | [](c-container.md)[**Организационная единица** контейнера](c-organizationalunit.md)              |
| Вспомогательные классы           | \-                                                                                               |
| NT-Security-дескриптор      | О:БАГ: BAD: S:                                                                                     |
| Дескриптор безопасности по умолчанию | D: (A;; РПВПКРККДКЛКЛОЛОРКВОВДСДДТДТСВ;;;D А) (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;; SY) (A;; РПЛКЛОРК;;; СЛУЖБЫ |
| System-Flags                | 0x00000000                                                                                       |



## <a name="windows-server-2008-attributes"></a>Windows Атрибуты сервера 2008

этот класс содержит следующие атрибуты для Windows Server 2008:



| attribute                                                                      | Обязательный | Унаследован от                                        |
|--------------------------------------------------------------------------------|-----------|-----------------------------------------------------|
| [**Описание администратора**](a-admindescription.md)                                | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Имя администратора-отображение**](a-admindisplayname.md)                               | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Allowed-Attributes**](a-allowedattributes.md)                              | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Allowed-Attributes-эффективен**](a-allowedattributeseffective.md)           | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Allowed-Child-classes**](a-allowedchildclasses.md)                         | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Allowed-Child-classes-эффективен**](a-allowedchildclasseseffective.md)      | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Плацдарм-Server-List-BL**](a-bridgeheadserverlistbl.md)                  | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Каноническое имя**](a-canonicalname.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Common-Name**](a-cn.md)                                                    | Неверно     | **rFC822LocalPart** [ **сверху**](c-top.md)<br/> |
| [**Метка времени создания**](a-createtimestamp.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Описание**](a-description.md)                                           | Неверно     | **rFC822LocalPart** [ **сверху**](c-top.md)<br/> |
| [**Целевой индикатор**](a-destinationindicator.md)                        | Неверно     | **rFC822LocalPart**                                 |
| [**Отображаемое имя**](a-displayname.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Отображаемое имя — печатаемое**](a-displaynameprintable.md)                       | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Компонент домена**](a-dc.md)                                               | Верно      | [**Домен**](c-domain.md)<br/>               |
| [**DSA-Signature**](a-dsasignature.md)                                        | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**DS-Core-распространение-данные**](a-dscorepropagationdata.md)                    | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Имя расширения**](a-extensionname.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Факс-телефон — номер**](a-facsimiletelephonenumber.md)               | Неверно     | **rFC822LocalPart**                                 |
| [**Метки**](a-flags.md)                                                       | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Из записи**](a-fromentry.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                  | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                      | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                     | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Тип экземпляра**](a-instancetype.md)                                        | Верно      | [**Вверх**](c-top.md)<br/>                     |
| [**Международный-ISDN-номер**](a-internationalisdnnumber.md)                 | Неверно     | **rFC822LocalPart**                                 |
| [**Является критически важным — системный объект**](a-iscriticalsystemobject.md)                  | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Удалено**](a-isdeleted.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Входит в состав списка рассылки**](a-memberof.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Имеет права владельца**](a-isprivilegeholder.md)                             | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Последний-известный-родительский**](a-lastknownparent.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Управляемые объекты**](a-managedobjects.md)                                    | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**В основном**](a-masteredby.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Метка времени изменения**](a-modifytimestamp.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-COM-Партитионсетлинк**](a-mscom-partitionsetlink.md)                    | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-COM-Усерлинк**](a-mscom-userlink.md)                                    | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DFSR-Компутерреференцебл**](a-msdfsr-computerreferencebl.md)            | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DFSR-Мемберреференцебл**](a-msdfsr-memberreferencebl.md)                | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-примерно-Иммед-подчиненные**](a-msds-approx-immed-subordinates.md)    | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-Аусентикатедто-Аккаунтлист**](a-msds-authenticatedtoaccountlist.md) | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-целостность-дочерняя — количество**](a-ms-ds-consistencychildcount.md)         | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-Consistencу-Guid**](a-ms-ds-consistencyguid.md)                      | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS--домен — для**](a-msds-isdomainfor.md)                              | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-является-Full-реплика для**](a-msds-isfullreplicafor.md)                   | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-является-partial-реплика для**](a-msds-ispartialreplicafor.md)             | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                            | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-Masterd-by**](a-msds-masteredby.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)              | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-NC-REPL-курсоры**](a-msds-ncreplcursors.md)                          | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-NC-REPL-Inbound-соседи**](a-msds-ncreplinboundneighbors.md)       | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-NC-REPL-Outbound-соседи**](a-msds-ncreploutboundneighbors.md)     | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)  | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-NC-Type**](a-msds-nctype.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-не-Members-BL**](a-msds-nonmembersbl.md)                            | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                  | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-Operations-для-AZ-Role-BL**](a-msds-operationsforazrolebl.md)        | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)        | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-Principal-Name**](a-msds-principalname.md)                           | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-PSO — применяется**](a-msds-psoapplied.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-REPL-Attribute-Meta-Data**](a-msds-replattributemetadata.md)         | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)                 | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-выявил-DSA**](a-msds-revealeddsas.md)                             | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-выводит-List-BL**](a-msds-revealedlistbl.md)                        | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-Tasks-для-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                  | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                  | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-дов-Owner-BL**](a-ownerbl.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Мссфу-30-POSIX-член-of**](a-mssfu30posixmemberof.md)                     | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**нетбут-SCP-BL**](a-netbootscpbl.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Не-Security-Member-BL**](a-nonsecuritymemberbl.md)                        | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**NT-Security-дескриптор**](a-ntsecuritydescriptor.md)                       | Верно      | [**Вверх**](c-top.md)<br/>                     |
| [**Obj-расп-имя**](a-distinguishedname.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Объект — Категория**](a-objectcategory.md)                                    | Верно      | [**Вверх**](c-top.md)<br/>                     |
| [**Объектный класс**](a-objectclass.md)                                          | Верно      | [**Вверх**](c-top.md)<br/>                     |
| [**Объект — GUID**](a-objectguid.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Версия объекта**](a-objectversion.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Другие хорошо известные объекты**](a-otherwellknownobjects.md)                    | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Разделяемый атрибут-удаление-список**](a-partialattributedeletionlist.md)      | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Разделяемый атрибут-set**](a-partialattributeset.md)                         | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**физическая доставка — Office-имя**](a-physicaldeliveryofficename.md)          | Неверно     | **rFC822LocalPart**                                 |
| [**Возможно — подстрочные**](a-possibleinferiors.md)                              | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Почтовый адрес**](a-postaladdress.md)                                      | Неверно     | **rFC822LocalPart**                                 |
| [**Почтовый код**](a-postalcode.md)                                            | Неверно     | **rFC822LocalPart**                                 |
| [**флажок после Office**](a-postofficebox.md)                                     | Неверно     | **rFC822LocalPart**                                 |
| [**Предпочтительный метод доставки**](a-preferreddeliverymethod.md)                 | Неверно     | **rFC822LocalPart**                                 |
| [**Прокси-объект-имя**](a-proxiedobjectname.md)                             | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Прокси-адреса**](a-proxyaddresses.md)                                    | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Запрос — политика — BL**](a-querypolicybl.md)                                     | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**RDN**](a-name.md)                                                          | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Зарегистрированный адрес**](a-registeredaddress.md)                              | Неверно     | **rFC822LocalPart**                                 |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                      | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**REPL-Уптодате-Vector**](a-repluptodatevector.md)                           | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Отчеты**](a-directreports.md)                                             | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Представители — от**](a-repsfrom.md)                                                | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Представители — кому**](a-repsto.md)                                                    | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Редакции**](a-revision.md)                                                 | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**SD-Rights-эффективен**](a-sdrightseffective.md)                             | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**См. также**](a-seealso.md)                                                  | Неверно     | **rFC822LocalPart**                                 |
| [**Server-Reference-BL**](a-serverreferencebl.md)                             | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**"Показать" — "Расширенный просмотр"**](a-showinadvancedviewonly.md)                 | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Site-Object-BL**](a-siteobjectbl.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Улица-адрес**](a-street.md)                                             | Неверно     | **rFC822LocalPart**                                 |
| [**Структурный объектный класс**](a-structuralobjectclass.md)                     | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Подразделы-ReFS**](a-subrefs.md)                                                  | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**субсчемасубентри**](a-subschemasubentry.md)                               | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Образование**](a-sn.md)                                                        | Неверно     | **rFC822LocalPart**                                 |
| [**Системные флаги**](a-systemflags.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Номер телефона**](a-telephonenumber.md)                                  | Неверно     | **rFC822LocalPart**                                 |
| [**Teletex — идентификатор терминала**](a-teletexterminalidentifier.md)             | Неверно     | **rFC822LocalPart**                                 |
| [**Номер телекса**](a-telexnumber.md)                                          | Неверно     | **rFC822LocalPart**                                 |
| [**USN-изменено**](a-usnchanged.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Созданный USN**](a-usncreated.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**USN-DSA-Last-obj-removed**](a-usndsalastobjremoved.md)                     | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**USN — межсайтовая**](a-usnintersite.md)                                        | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                    | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Источник USN**](a-usnsource.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**WBEM — путь**](a-wbempath.md)                                                | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Хорошо известные объекты**](a-wellknownobjects.md)                               | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**При изменении**](a-whenchanged.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**При создании**](a-whencreated.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**WWW — Главная страница**](a-wwwhomepage.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**WWW-Page — другие**](a-url.md)                                                | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**X121 — адрес**](a-x121address.md)                                          | Неверно     | **rFC822LocalPart**                                 |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2

-   [Атрибуты](#windows-server-2008-r2-attributes)



| Ввод | Значение |
|-----------------------------|--------------------------------------------------------------------------------------------------|
| System-Only                 | Неверно                                                                                            |
| Object-Category             | 1                                                                                                |
| По умолчанию — объект — Категория     | \-                                                                                               |
| Governs-Id                  | 0.9.2342.19200300.100.4.14                                                                       |
| По умолчанию-скрытие значения        | 1                                                                                                |
| RDN-Атри-ID                  | [**Common-Name**](a-cn.md)<br/>                                                           |
| Подкласс                 | [**Домен**](c-domain.md)<br/>                                                            |
| Возможные старшие          | [](c-container.md)[**Организационная единица** контейнера](c-organizationalunit.md)              |
| Вспомогательные классы           | \-                                                                                               |
| NT-Security-дескриптор      | О:БАГ: BAD: S:                                                                                     |
| Дескриптор безопасности по умолчанию | D: (A;; РПВПКРККДКЛКЛОЛОРКВОВДСДДТДТСВ;;;D А) (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;; SY) (A;; РПЛКЛОРК;;; СЛУЖБЫ |
| System-Flags                | 0x00000000                                                                                       |



## <a name="windows-server-2008-r2-attributes"></a>Windows Атрибуты сервера 2008 R2

этот класс содержит следующие атрибуты для Windows Server 2008 R2:



| attribute                                                                        | Обязательный | Унаследован от                                        |
|----------------------------------------------------------------------------------|-----------|-----------------------------------------------------|
| [**Описание администратора**](a-admindescription.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Имя администратора-отображение**](a-admindisplayname.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Allowed-Attributes**](a-allowedattributes.md)                                | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Allowed-Attributes-эффективен**](a-allowedattributeseffective.md)             | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Allowed-Child-classes**](a-allowedchildclasses.md)                           | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Allowed-Child-classes-эффективен**](a-allowedchildclasseseffective.md)        | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Плацдарм-Server-List-BL**](a-bridgeheadserverlistbl.md)                    | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Каноническое имя**](a-canonicalname.md)                                        | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Common-Name**](a-cn.md)                                                      | Неверно     | **rFC822LocalPart** [ **сверху**](c-top.md)<br/> |
| [**Метка времени создания**](a-createtimestamp.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Описание**](a-description.md)                                             | Неверно     | **rFC822LocalPart** [ **сверху**](c-top.md)<br/> |
| [**Целевой индикатор**](a-destinationindicator.md)                          | Неверно     | **rFC822LocalPart**                                 |
| [**Отображаемое имя**](a-displayname.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Отображаемое имя — печатаемое**](a-displaynameprintable.md)                         | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Компонент домена**](a-dc.md)                                                 | Верно      | [**Домен**](c-domain.md)<br/>               |
| [**DSA-Signature**](a-dsasignature.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**DS-Core-распространение-данные**](a-dscorepropagationdata.md)                      | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Имя расширения**](a-extensionname.md)                                        | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Факс-телефон — номер**](a-facsimiletelephonenumber.md)                 | Неверно     | **rFC822LocalPart**                                 |
| [**Метки**](a-flags.md)                                                         | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Из записи**](a-fromentry.md)                                                | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                    | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                        | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Тип экземпляра**](a-instancetype.md)                                          | Верно      | [**Вверх**](c-top.md)<br/>                     |
| [**Международный-ISDN-номер**](a-internationalisdnnumber.md)                   | Неверно     | **rFC822LocalPart**                                 |
| [**Является критически важным — системный объект**](a-iscriticalsystemobject.md)                    | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Удалено**](a-isdeleted.md)                                                | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Входит в состав списка рассылки**](a-memberof.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Имеет права владельца**](a-isprivilegeholder.md)                               | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Является перезапущенным**](a-isrecycled.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Последний-известный-родительский**](a-lastknownparent.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Управляемые объекты**](a-managedobjects.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**В основном**](a-masteredby.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Метка времени изменения**](a-modifytimestamp.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-COM-Партитионсетлинк**](a-mscom-partitionsetlink.md)                      | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-COM-Усерлинк**](a-mscom-userlink.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DFSR-Компутерреференцебл**](a-msdfsr-computerreferencebl.md)              | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DFSR-Мемберреференцебл**](a-msdfsr-memberreferencebl.md)                  | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-примерно-Иммед-подчиненные**](a-msds-approx-immed-subordinates.md)      | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-Аусентикатедто-Аккаунтлист**](a-msds-authenticatedtoaccountlist.md)   | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-целостность-дочерняя — количество**](a-ms-ds-consistencychildcount.md)           | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-Consistencу-Guid**](a-ms-ds-consistencyguid.md)                        | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Поддержка MS-DS-Feature-BL**](a-msds-enabledfeaturebl.md)                      | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)             | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS--домен — для**](a-msds-isdomainfor.md)                                | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-является-Full-реплика для**](a-msds-isfullreplicafor.md)                     | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-является-partial-реплика для**](a-msds-ispartialreplicafor.md)               | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                              | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                              | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-локально-эффективное удаление — время**](a-msds-localeffectivedeletiontime.md) | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-Local-эффективен — время перезапуска**](a-msds-localeffectiverecycletime.md)   | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-Masterd-by**](a-msds-masteredby.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)                | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-NC-REPL-курсоры**](a-msds-ncreplcursors.md)                            | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-NC-REPL-Inbound-соседи**](a-msds-ncreplinboundneighbors.md)         | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-NC-REPL-Outbound-соседи**](a-msds-ncreploutboundneighbors.md)       | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)    | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-NC-Type**](a-msds-nctype.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-не-Members-BL**](a-msds-nonmembersbl.md)                              | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                    | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-Оидтограуп-Link-BL**](a-msds-oidtogrouplinkbl.md)                      | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-Operations-для-AZ-Role-BL**](a-msds-operationsforazrolebl.md)          | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)          | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-Principal-Name**](a-msds-principalname.md)                             | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-PSO — применяется**](a-msds-psoapplied.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-REPL-Attribute-Meta-Data**](a-msds-replattributemetadata.md)           | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)                   | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-выявил-DSA**](a-msds-revealeddsas.md)                               | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-выводит-List-BL**](a-msds-revealedlistbl.md)                          | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-Tasks-для-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                    | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                    | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-дов-Owner-BL**](a-ownerbl.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Мссфу-30-POSIX-член-of**](a-mssfu30posixmemberof.md)                       | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**нетбут-SCP-BL**](a-netbootscpbl.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Не-Security-Member-BL**](a-nonsecuritymemberbl.md)                          | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**NT-Security-дескриптор**](a-ntsecuritydescriptor.md)                         | Верно      | [**Вверх**](c-top.md)<br/>                     |
| [**Obj-расп-имя**](a-distinguishedname.md)                                     | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Объект — Категория**](a-objectcategory.md)                                      | Верно      | [**Вверх**](c-top.md)<br/>                     |
| [**Объектный класс**](a-objectclass.md)                                            | Верно      | [**Вверх**](c-top.md)<br/>                     |
| [**Объект — GUID**](a-objectguid.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Версия объекта**](a-objectversion.md)                                        | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Другие хорошо известные объекты**](a-otherwellknownobjects.md)                      | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Разделяемый атрибут-удаление-список**](a-partialattributedeletionlist.md)        | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Разделяемый атрибут-set**](a-partialattributeset.md)                           | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**физическая доставка — Office-имя**](a-physicaldeliveryofficename.md)            | Неверно     | **rFC822LocalPart**                                 |
| [**Возможно — подстрочные**](a-possibleinferiors.md)                                | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Почтовый адрес**](a-postaladdress.md)                                        | Неверно     | **rFC822LocalPart**                                 |
| [**Почтовый код**](a-postalcode.md)                                              | Неверно     | **rFC822LocalPart**                                 |
| [**флажок после Office**](a-postofficebox.md)                                       | Неверно     | **rFC822LocalPart**                                 |
| [**Предпочтительный метод доставки**](a-preferreddeliverymethod.md)                   | Неверно     | **rFC822LocalPart**                                 |
| [**Прокси-объект-имя**](a-proxiedobjectname.md)                               | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Прокси-адреса**](a-proxyaddresses.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Запрос — политика — BL**](a-querypolicybl.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**RDN**](a-name.md)                                                            | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Зарегистрированный адрес**](a-registeredaddress.md)                                | Неверно     | **rFC822LocalPart**                                 |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                        | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**REPL-Уптодате-Vector**](a-repluptodatevector.md)                             | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Отчеты**](a-directreports.md)                                               | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Представители — от**](a-repsfrom.md)                                                  | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Представители — кому**](a-repsto.md)                                                      | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Редакции**](a-revision.md)                                                   | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**SD-Rights-эффективен**](a-sdrightseffective.md)                               | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**См. также**](a-seealso.md)                                                    | Неверно     | **rFC822LocalPart**                                 |
| [**Server-Reference-BL**](a-serverreferencebl.md)                               | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**"Показать" — "Расширенный просмотр"**](a-showinadvancedviewonly.md)                   | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Site-Object-BL**](a-siteobjectbl.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Улица-адрес**](a-street.md)                                               | Неверно     | **rFC822LocalPart**                                 |
| [**Структурный объектный класс**](a-structuralobjectclass.md)                       | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Подразделы-ReFS**](a-subrefs.md)                                                    | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**субсчемасубентри**](a-subschemasubentry.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Образование**](a-sn.md)                                                          | Неверно     | **rFC822LocalPart**                                 |
| [**Системные флаги**](a-systemflags.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Номер телефона**](a-telephonenumber.md)                                    | Неверно     | **rFC822LocalPart**                                 |
| [**Teletex — идентификатор терминала**](a-teletexterminalidentifier.md)               | Неверно     | **rFC822LocalPart**                                 |
| [**Номер телекса**](a-telexnumber.md)                                            | Неверно     | **rFC822LocalPart**                                 |
| [**USN-изменено**](a-usnchanged.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Созданный USN**](a-usncreated.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**USN-DSA-Last-obj-removed**](a-usndsalastobjremoved.md)                       | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**USN — межсайтовая**](a-usnintersite.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Источник USN**](a-usnsource.md)                                                | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**WBEM — путь**](a-wbempath.md)                                                  | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Хорошо известные объекты**](a-wellknownobjects.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**При изменении**](a-whenchanged.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**При создании**](a-whencreated.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**WWW — Главная страница**](a-wwwhomepage.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**WWW-Page — другие**](a-url.md)                                                  | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**X121 — адрес**](a-x121address.md)                                            | Неверно     | **rFC822LocalPart**                                 |



## <a name="windows-server-2012"></a>Windows Server 2012

-   [Атрибуты](#windows-server-2012-attributes)



| Ввод | Значение |
|-----------------------------|--------------------------------------------------------------------------------------------------|
| System-Only                 | Неверно                                                                                            |
| Object-Category             | 1                                                                                                |
| По умолчанию — объект — Категория     | \-                                                                                               |
| Governs-Id                  | 0.9.2342.19200300.100.4.14                                                                       |
| По умолчанию-скрытие значения        | 1                                                                                                |
| RDN-Атри-ID                  | [**Common-Name**](a-cn.md)<br/>                                                           |
| Подкласс                 | [**Домен**](c-domain.md)<br/>                                                            |
| Возможные старшие          | [](c-container.md)[**Организационная единица** контейнера](c-organizationalunit.md)              |
| Вспомогательные классы           | \-                                                                                               |
| NT-Security-дескриптор      | О:БАГ: BAD: S:                                                                                     |
| Дескриптор безопасности по умолчанию | D: (A;; РПВПКРККДКЛКЛОЛОРКВОВДСДДТДТСВ;;;D А) (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;; SY) (A;; РПЛКЛОРК;;; СЛУЖБЫ |
| System-Flags                | 0x00000000                                                                                       |



## <a name="windows-server-2012-attributes"></a>Windows Server 2012 Атрибута

Этот класс содержит следующие атрибуты для Windows Server 2012:



| attribute                                                                                    | Обязательный | Унаследован от                                        |
|----------------------------------------------------------------------------------------------|-----------|-----------------------------------------------------|
| [**Описание администратора**](a-admindescription.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Имя администратора-отображение**](a-admindisplayname.md)                                             | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Allowed-Attributes**](a-allowedattributes.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Allowed-Attributes-эффективен**](a-allowedattributeseffective.md)                         | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Allowed-Child-classes**](a-allowedchildclasses.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Allowed-Child-classes-эффективен**](a-allowedchildclasseseffective.md)                    | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Плацдарм-Server-List-BL**](a-bridgeheadserverlistbl.md)                                | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Каноническое имя**](a-canonicalname.md)                                                    | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Common-Name**](a-cn.md)                                                                  | Неверно     | **rFC822LocalPart** [ **сверху**](c-top.md)<br/> |
| [**Метка времени создания**](a-createtimestamp.md)                                               | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Описание**](a-description.md)                                                         | Неверно     | **rFC822LocalPart** [ **сверху**](c-top.md)<br/> |
| [**Целевой индикатор**](a-destinationindicator.md)                                      | Неверно     | **rFC822LocalPart**                                 |
| [**Отображаемое имя**](a-displayname.md)                                                        | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Отображаемое имя — печатаемое**](a-displaynameprintable.md)                                     | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Компонент домена**](a-dc.md)                                                             | Верно      | [**Домен**](c-domain.md)<br/>               |
| [**DSA-Signature**](a-dsasignature.md)                                                      | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**DS-Core-распространение-данные**](a-dscorepropagationdata.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Имя расширения**](a-extensionname.md)                                                    | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Факс-телефон — номер**](a-facsimiletelephonenumber.md)                             | Неверно     | **rFC822LocalPart**                                 |
| [**Метки**](a-flags.md)                                                                     | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Из записи**](a-fromentry.md)                                                            | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                                | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                                    | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                                   | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Тип экземпляра**](a-instancetype.md)                                                      | Верно      | [**Вверх**](c-top.md)<br/>                     |
| [**Международный-ISDN-номер**](a-internationalisdnnumber.md)                               | Неверно     | **rFC822LocalPart**                                 |
| [**Является критически важным — системный объект**](a-iscriticalsystemobject.md)                                | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Удалено**](a-isdeleted.md)                                                            | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Входит в состав списка рассылки**](a-memberof.md)                                                        | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Имеет права владельца**](a-isprivilegeholder.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Является перезапущенным**](a-isrecycled.md)                                                          | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Последний-известный-родительский**](a-lastknownparent.md)                                               | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Управляемые объекты**](a-managedobjects.md)                                                  | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**В основном**](a-masteredby.md)                                                          | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Метка времени изменения**](a-modifytimestamp.md)                                               | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-COM-Партитионсетлинк**](a-mscom-partitionsetlink.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-COM-Усерлинк**](a-mscom-userlink.md)                                                  | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DFSR-Компутерреференцебл**](a-msdfsr-computerreferencebl.md)                          | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DFSR-Мемберреференцебл**](a-msdfsr-memberreferencebl.md)                              | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-примерно-Иммед-подчиненные**](a-msds-approx-immed-subordinates.md)                  | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-Аусентикатедто-Аккаунтлист**](a-msds-authenticatedtoaccountlist.md)               | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-ClaimSet-shares-возможные значения-with-BL**](a-msds-claimsharespossiblevalueswithbl.md) | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-целостность-дочерняя — количество**](a-ms-ds-consistencychildcount.md)                       | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-Consistencу-Guid**](a-ms-ds-consistencyguid.md)                                    | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Поддержка MS-DS-Feature-BL**](a-msds-enabledfeaturebl.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)                         | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS--домен — для**](a-msds-isdomainfor.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-является-Full-реплика для**](a-msds-isfullreplicafor.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-является-partial-реплика для**](a-msds-ispartialreplicafor.md)                           | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-является-PRIMARY-Computer-для**](a-msds-isprimarycomputerfor.md)                         | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-локально-эффективное удаление — время**](a-msds-localeffectivedeletiontime.md)             | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-Local-эффективен — время перезапуска**](a-msds-localeffectiverecycletime.md)               | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-Masterd-by**](a-msds-masteredby.md)                                               | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)                            | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-Members-of-Resource-Property-List-BL**](a-msds-membersofresourcepropertylistbl.md) | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-NC-REPL-курсоры**](a-msds-ncreplcursors.md)                                        | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-NC-REPL-Inbound-соседи**](a-msds-ncreplinboundneighbors.md)                     | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-NC-REPL-Outbound-соседи**](a-msds-ncreploutboundneighbors.md)                   | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)                | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-NC-Type**](a-msds-nctype.md)                                                       | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-не-Members-BL**](a-msds-nonmembersbl.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                                | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-Оидтограуп-Link-BL**](a-msds-oidtogrouplinkbl.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-Operations-для-AZ-Role-BL**](a-msds-operationsforazrolebl.md)                      | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)                      | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-Principal-Name**](a-msds-principalname.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-PSO — применяется**](a-msds-psoapplied.md)                                               | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-REPL-Attribute-Meta-Data**](a-msds-replattributemetadata.md)                       | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)                               | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-выявил-DSA**](a-msds-revealeddsas.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-выводит-List-BL**](a-msds-revealedlistbl.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-Tasks-для-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                                | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                                | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**ms-DS-TDO-Egress-BL**](a-msds-tdoegressbl.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-TDO-входящий трафик — BL**](a-msds-tdoingressbl.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-DS-value-type-Reference-BL**](a-msds-valuetypereferencebl.md)                         | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**MS-дов-Owner-BL**](a-ownerbl.md)                                                        | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Мссфу-30-POSIX-член-of**](a-mssfu30posixmemberof.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**нетбут-SCP-BL**](a-netbootscpbl.md)                                                     | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Не-Security-Member-BL**](a-nonsecuritymemberbl.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**NT-Security-дескриптор**](a-ntsecuritydescriptor.md)                                     | Верно      | [**Вверх**](c-top.md)<br/>                     |
| [**Obj-расп-имя**](a-distinguishedname.md)                                                 | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Объект — Категория**](a-objectcategory.md)                                                  | Верно      | [**Вверх**](c-top.md)<br/>                     |
| [**Объектный класс**](a-objectclass.md)                                                        | Верно      | [**Вверх**](c-top.md)<br/>                     |
| [**Объект — GUID**](a-objectguid.md)                                                          | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Версия объекта**](a-objectversion.md)                                                    | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Другие хорошо известные объекты**](a-otherwellknownobjects.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Разделяемый атрибут-удаление-список**](a-partialattributedeletionlist.md)                    | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Разделяемый атрибут-set**](a-partialattributeset.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**физическая доставка — Office-имя**](a-physicaldeliveryofficename.md)                        | Неверно     | **rFC822LocalPart**                                 |
| [**Возможно — подстрочные**](a-possibleinferiors.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Почтовый адрес**](a-postaladdress.md)                                                    | Неверно     | **rFC822LocalPart**                                 |
| [**Почтовый код**](a-postalcode.md)                                                          | Неверно     | **rFC822LocalPart**                                 |
| [**флажок после Office**](a-postofficebox.md)                                                   | Неверно     | **rFC822LocalPart**                                 |
| [**Предпочтительный метод доставки**](a-preferreddeliverymethod.md)                               | Неверно     | **rFC822LocalPart**                                 |
| [**Прокси-объект-имя**](a-proxiedobjectname.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Прокси-адреса**](a-proxyaddresses.md)                                                  | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Запрос — политика — BL**](a-querypolicybl.md)                                                   | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**RDN**](a-name.md)                                                                        | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Зарегистрированный адрес**](a-registeredaddress.md)                                            | Неверно     | **rFC822LocalPart**                                 |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                                    | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**REPL-Уптодате-Vector**](a-repluptodatevector.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Отчеты**](a-directreports.md)                                                           | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Представители — от**](a-repsfrom.md)                                                              | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Представители — кому**](a-repsto.md)                                                                  | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Редакции**](a-revision.md)                                                               | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**SD-Rights-эффективен**](a-sdrightseffective.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**См. также**](a-seealso.md)                                                                | Неверно     | **rFC822LocalPart**                                 |
| [**Server-Reference-BL**](a-serverreferencebl.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**"Показать" — "Расширенный просмотр"**](a-showinadvancedviewonly.md)                               | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                     | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Улица-адрес**](a-street.md)                                                           | Неверно     | **rFC822LocalPart**                                 |
| [**Структурный объектный класс**](a-structuralobjectclass.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Подразделы-ReFS**](a-subrefs.md)                                                                | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**субсчемасубентри**](a-subschemasubentry.md)                                             | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Образование**](a-sn.md)                                                                      | Неверно     | **rFC822LocalPart**                                 |
| [**Системные флаги**](a-systemflags.md)                                                        | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Номер телефона**](a-telephonenumber.md)                                                | Неверно     | **rFC822LocalPart**                                 |
| [**Teletex — идентификатор терминала**](a-teletexterminalidentifier.md)                           | Неверно     | **rFC822LocalPart**                                 |
| [**Номер телекса**](a-telexnumber.md)                                                        | Неверно     | **rFC822LocalPart**                                 |
| [**USN-изменено**](a-usnchanged.md)                                                          | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Созданный USN**](a-usncreated.md)                                                          | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**USN-DSA-Last-obj-removed**](a-usndsalastobjremoved.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**USN — межсайтовая**](a-usnintersite.md)                                                      | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                                  | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Источник USN**](a-usnsource.md)                                                            | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**WBEM — путь**](a-wbempath.md)                                                              | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**Хорошо известные объекты**](a-wellknownobjects.md)                                             | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**При изменении**](a-whenchanged.md)                                                        | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**При создании**](a-whencreated.md)                                                        | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**WWW — Главная страница**](a-wwwhomepage.md)                                                       | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**WWW-Page — другие**](a-url.md)                                                              | Неверно     | [**Вверх**](c-top.md)<br/>                     |
| [**X121 — адрес**](a-x121address.md)                                                        | Неверно     | **rFC822LocalPart**                                 |



 

 





