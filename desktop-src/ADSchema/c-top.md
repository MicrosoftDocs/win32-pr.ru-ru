---
title: Класс Top
description: Класс верхнего уровня, от которого производятся все классы.
ms.assetid: 025aff6c-1804-4141-accf-d50cfd50e90e
ms.tgt_platform: multiple
keywords:
- Схема AD верхнего класса
- Схема AD верхнего класса
topic_type:
- apiref
api_name:
- Top
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01cd6a72dfba6a80687081d503864c88fd1c5122
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104137934"
---
# <a name="top-class"></a>Класс Top

Класс верхнего уровня, от которого производятся все классы.



| Ввод | Значение |
|-------------------|--------------------------------------|
| CN                | Начало                                  |
| LDAP-отображаемое имя | top                                  |
| Привилегия обновления  | Администратор схемы                 |
| Частота обновления  | \-                                   |
| Schema-ID-GUID    | bf967ab7-0de6-11d0-a285-00aa003049e2 |



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
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | True                                                                                         |
| Object-Category             | 2                                                                                            |
| По умолчанию — объект — Категория     | \-                                                                                           |
| Governs-Id                  | 2.5.6.0                                                                                      |
| По умолчанию-скрытие значения        | 1                                                                                            |
| RDN-Атри-ID                  | [**Common-Name**](a-cn.md)<br/>                                                       |
| Подкласс                 | **Top**<br/>                                                                           |
| Возможные старшие          | [**Потерянные и найденные**](c-lostandfound.md)                                                     |
| Вспомогательные классы           | \-                                                                                           |
| NT-Security-дескриптор      | О:БАГ: BAD: S:                                                                                 |
| Дескриптор безопасности по умолчанию | D: (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;;D А) (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;; SY) (A;; РПЛКЛОРК;;; СЛУЖБЫ |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-2000-server-attributes"></a>Атрибуты сервера Windows 2000

Этот класс содержит следующие атрибуты для сервера Windows 2000:



| attribute                                                                 | Обязательный | Унаследован от |
|---------------------------------------------------------------------------|-----------|--------------|
| [**Описание администратора**](a-admindescription.md)                           | Неверно     | **Top**      |
| [**Имя администратора-отображение**](a-admindisplayname.md)                          | Неверно     | **Top**      |
| [**Allowed-Attributes**](a-allowedattributes.md)                         | Неверно     | **Top**      |
| [**Allowed-Attributes-эффективен**](a-allowedattributeseffective.md)      | Неверно     | **Top**      |
| [**Allowed-Child-classes**](a-allowedchildclasses.md)                    | Неверно     | **Top**      |
| [**Allowed-Child-classes-эффективен**](a-allowedchildclasseseffective.md) | Неверно     | **Top**      |
| [**Плацдарм-Server-List-BL**](a-bridgeheadserverlistbl.md)             | Неверно     | **Top**      |
| [**Каноническое имя**](a-canonicalname.md)                                 | Неверно     | **Top**      |
| [**Common-Name**](a-cn.md)                                               | Неверно     | **Top**      |
| [**Метка времени создания**](a-createtimestamp.md)                            | Неверно     | **Top**      |
| [**Описание**](a-description.md)                                      | Неверно     | **Top**      |
| [**Отображаемое имя**](a-displayname.md)                                     | Неверно     | **Top**      |
| [**Отображаемое имя — печатаемое**](a-displaynameprintable.md)                  | Неверно     | **Top**      |
| [**DSA-Signature**](a-dsasignature.md)                                   | Неверно     | **Top**      |
| [**DS-Core-распространение-данные**](a-dscorepropagationdata.md)               | Неверно     | **Top**      |
| [**Имя расширения**](a-extensionname.md)                                 | Неверно     | **Top**      |
| [**Метки**](a-flags.md)                                                  | Неверно     | **Top**      |
| [**Из записи**](a-fromentry.md)                                         | Неверно     | **Top**      |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)             | Неверно     | **Top**      |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                 | Неверно     | **Top**      |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                | Неверно     | **Top**      |
| [**Тип экземпляра**](a-instancetype.md)                                   | True      | **Top**      |
| [**Является критически важным — системный объект**](a-iscriticalsystemobject.md)             | Неверно     | **Top**      |
| [**Удалено**](a-isdeleted.md)                                         | Неверно     | **Top**      |
| [**Входит в состав списка рассылки**](a-memberof.md)                                     | Неверно     | **Top**      |
| [**Имеет права владельца**](a-isprivilegeholder.md)                        | Неверно     | **Top**      |
| [**Последний-известный-родительский**](a-lastknownparent.md)                            | Неверно     | **Top**      |
| [**Управляемые объекты**](a-managedobjects.md)                               | Неверно     | **Top**      |
| [**В основном**](a-masteredby.md)                                       | Неверно     | **Top**      |
| [**Метка времени изменения**](a-modifytimestamp.md)                            | Неверно     | **Top**      |
| [**MS-DS-целостность-дочерняя — количество**](a-ms-ds-consistencychildcount.md)    | Неверно     | **Top**      |
| [**MS-DS-Consistencу-Guid**](a-ms-ds-consistencyguid.md)                 | Неверно     | **Top**      |
| [**нетбут-SCP-BL**](a-netbootscpbl.md)                                  | Неверно     | **Top**      |
| [**Не-Security-Member-BL**](a-nonsecuritymemberbl.md)                   | Неверно     | **Top**      |
| [**NT-Security-дескриптор**](a-ntsecuritydescriptor.md)                  | True      | **Top**      |
| [**Obj-расп-имя**](a-distinguishedname.md)                              | Неверно     | **Top**      |
| [**Объект — Категория**](a-objectcategory.md)                               | True      | **Top**      |
| [**Объектный класс**](a-objectclass.md)                                     | True      | **Top**      |
| [**Объект — GUID**](a-objectguid.md)                                       | Неверно     | **Top**      |
| [**Версия объекта**](a-objectversion.md)                                 | Неверно     | **Top**      |
| [**Другие хорошо известные объекты**](a-otherwellknownobjects.md)               | Неверно     | **Top**      |
| [**Разделяемый атрибут-удаление-список**](a-partialattributedeletionlist.md) | Неверно     | **Top**      |
| [**Разделяемый атрибут-set**](a-partialattributeset.md)                    | Неверно     | **Top**      |
| [**Возможно — подстрочные**](a-possibleinferiors.md)                         | Неверно     | **Top**      |
| [**Прокси-объект-имя**](a-proxiedobjectname.md)                        | Неверно     | **Top**      |
| [**Прокси-адреса**](a-proxyaddresses.md)                               | Неверно     | **Top**      |
| [**Запрос — политика — BL**](a-querypolicybl.md)                                | Неверно     | **Top**      |
| [**RDN**](a-name.md)                                                     | Неверно     | **Top**      |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                 | Неверно     | **Top**      |
| [**REPL-Уптодате-Vector**](a-repluptodatevector.md)                      | Неверно     | **Top**      |
| [**Отчеты**](a-directreports.md)                                        | Неверно     | **Top**      |
| [**Представители — от**](a-repsfrom.md)                                           | Неверно     | **Top**      |
| [**Представители — кому**](a-repsto.md)                                               | Неверно     | **Top**      |
| [**Редакции**](a-revision.md)                                            | Неверно     | **Top**      |
| [**SD-Rights-эффективен**](a-sdrightseffective.md)                        | Неверно     | **Top**      |
| [**Server-Reference-BL**](a-serverreferencebl.md)                        | Неверно     | **Top**      |
| [**"Показать" — "Расширенный просмотр"**](a-showinadvancedviewonly.md)            | Неверно     | **Top**      |
| [**Site-Object-BL**](a-siteobjectbl.md)                                  | Неверно     | **Top**      |
| [**Подразделы-ReFS**](a-subrefs.md)                                             | Неверно     | **Top**      |
| [**субсчемасубентри**](a-subschemasubentry.md)                          | Неверно     | **Top**      |
| [**Системные флаги**](a-systemflags.md)                                     | Неверно     | **Top**      |
| [**USN-изменено**](a-usnchanged.md)                                       | Неверно     | **Top**      |
| [**Созданный USN**](a-usncreated.md)                                       | Неверно     | **Top**      |
| [**USN-DSA-Last-obj-removed**](a-usndsalastobjremoved.md)                | Неверно     | **Top**      |
| [**USN — межсайтовая**](a-usnintersite.md)                                   | Неверно     | **Top**      |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                               | Неверно     | **Top**      |
| [**Источник USN**](a-usnsource.md)                                         | Неверно     | **Top**      |
| [**WBEM — путь**](a-wbempath.md)                                           | Неверно     | **Top**      |
| [**Хорошо известные объекты**](a-wellknownobjects.md)                          | Неверно     | **Top**      |
| [**При изменении**](a-whenchanged.md)                                     | Неверно     | **Top**      |
| [**При создании**](a-whencreated.md)                                     | Неверно     | **Top**      |
| [**WWW — Главная страница**](a-wwwhomepage.md)                                    | Неверно     | **Top**      |
| [**WWW-Page — другие**](a-url.md)                                           | Неверно     | **Top**      |



## <a name="windows-server-2003"></a>Windows Server 2003

-   [Атрибуты](#windows-server-2003-attributes)



| Ввод | Значение |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | True                                                                                         |
| Object-Category             | 2                                                                                            |
| По умолчанию — объект — Категория     | \-                                                                                           |
| Governs-Id                  | 2.5.6.0                                                                                      |
| По умолчанию-скрытие значения        | 1                                                                                            |
| RDN-Атри-ID                  | [**Common-Name**](a-cn.md)<br/>                                                       |
| Подкласс                 | **Top**<br/>                                                                           |
| Возможные старшие          | [**Потерянные и найденные**](c-lostandfound.md)                                                     |
| Вспомогательные классы           | \-                                                                                           |
| NT-Security-дескриптор      | О:БАГ: BAD: S:                                                                                 |
| Дескриптор безопасности по умолчанию | D: (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;;D А) (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;; SY) (A;; РПЛКЛОРК;;; СЛУЖБЫ |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2003-attributes"></a>Атрибуты Windows Server 2003

Этот класс содержит следующие атрибуты для Windows Server 2003:



| attribute                                                                   | Обязательный | Унаследован от |
|-----------------------------------------------------------------------------|-----------|--------------|
| [**Описание администратора**](a-admindescription.md)                             | Неверно     | **Top**      |
| [**Имя администратора-отображение**](a-admindisplayname.md)                            | Неверно     | **Top**      |
| [**Allowed-Attributes**](a-allowedattributes.md)                           | Неверно     | **Top**      |
| [**Allowed-Attributes-эффективен**](a-allowedattributeseffective.md)        | Неверно     | **Top**      |
| [**Allowed-Child-classes**](a-allowedchildclasses.md)                      | Неверно     | **Top**      |
| [**Allowed-Child-classes-эффективен**](a-allowedchildclasseseffective.md)   | Неверно     | **Top**      |
| [**Плацдарм-Server-List-BL**](a-bridgeheadserverlistbl.md)               | Неверно     | **Top**      |
| [**Каноническое имя**](a-canonicalname.md)                                   | Неверно     | **Top**      |
| [**Common-Name**](a-cn.md)                                                 | Неверно     | **Top**      |
| [**Метка времени создания**](a-createtimestamp.md)                              | Неверно     | **Top**      |
| [**Описание**](a-description.md)                                        | Неверно     | **Top**      |
| [**Отображаемое имя**](a-displayname.md)                                       | Неверно     | **Top**      |
| [**Отображаемое имя — печатаемое**](a-displaynameprintable.md)                    | Неверно     | **Top**      |
| [**DSA-Signature**](a-dsasignature.md)                                     | Неверно     | **Top**      |
| [**DS-Core-распространение-данные**](a-dscorepropagationdata.md)                 | Неверно     | **Top**      |
| [**Имя расширения**](a-extensionname.md)                                   | Неверно     | **Top**      |
| [**Метки**](a-flags.md)                                                    | Неверно     | **Top**      |
| [**Из записи**](a-fromentry.md)                                           | Неверно     | **Top**      |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | Неверно     | **Top**      |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | Неверно     | **Top**      |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | Неверно     | **Top**      |
| [**Тип экземпляра**](a-instancetype.md)                                     | True      | **Top**      |
| [**Является критически важным — системный объект**](a-iscriticalsystemobject.md)               | Неверно     | **Top**      |
| [**Удалено**](a-isdeleted.md)                                           | Неверно     | **Top**      |
| [**Входит в состав списка рассылки**](a-memberof.md)                                       | Неверно     | **Top**      |
| [**Имеет права владельца**](a-isprivilegeholder.md)                          | Неверно     | **Top**      |
| [**Последний-известный-родительский**](a-lastknownparent.md)                              | Неверно     | **Top**      |
| [**Управляемые объекты**](a-managedobjects.md)                                 | Неверно     | **Top**      |
| [**В основном**](a-masteredby.md)                                         | Неверно     | **Top**      |
| [**Метка времени изменения**](a-modifytimestamp.md)                              | Неверно     | **Top**      |
| [**MS-COM-Партитионсетлинк**](a-mscom-partitionsetlink.md)                 | Неверно     | **Top**      |
| [**MS-COM-Усерлинк**](a-mscom-userlink.md)                                 | Неверно     | **Top**      |
| [**MS-DS-примерно-Иммед-подчиненные**](a-msds-approx-immed-subordinates.md) | Неверно     | **Top**      |
| [**MS-DS-целостность-дочерняя — количество**](a-ms-ds-consistencychildcount.md)      | Неверно     | **Top**      |
| [**MS-DS-Consistencу-Guid**](a-ms-ds-consistencyguid.md)                   | Неверно     | **Top**      |
| [**MS-DS-Masterd-by**](a-msds-masteredby.md)                              | Неверно     | **Top**      |
| [**MS-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)           | Неверно     | **Top**      |
| [**MS-DS-NC-REPL-курсоры**](a-msds-ncreplcursors.md)                       | Неверно     | **Top**      |
| [**MS-DS-NC-REPL-Inbound-соседи**](a-msds-ncreplinboundneighbors.md)    | Неверно     | **Top**      |
| [**MS-DS-NC-REPL-Outbound-соседи**](a-msds-ncreploutboundneighbors.md)  | Неверно     | **Top**      |
| [**MS-DS-не-Members-BL**](a-msds-nonmembersbl.md)                         | Неверно     | **Top**      |
| [**MS-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | Неверно     | **Top**      |
| [**MS-DS-Operations-для-AZ-Role-BL**](a-msds-operationsforazrolebl.md)     | Неверно     | **Top**      |
| [**MS-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)     | Неверно     | **Top**      |
| [**MS-DS-REPL-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | Неверно     | **Top**      |
| [**MS-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)              | Неверно     | **Top**      |
| [**MS-DS-Tasks-для-AZ-Role-BL**](a-msds-tasksforazrolebl.md)               | Неверно     | **Top**      |
| [**MS-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)               | Неверно     | **Top**      |
| [**MS-дов-Owner-BL**](a-ownerbl.md)                                       | Неверно     | **Top**      |
| [**нетбут-SCP-BL**](a-netbootscpbl.md)                                    | Неверно     | **Top**      |
| [**Не-Security-Member-BL**](a-nonsecuritymemberbl.md)                     | Неверно     | **Top**      |
| [**NT-Security-дескриптор**](a-ntsecuritydescriptor.md)                    | True      | **Top**      |
| [**Obj-расп-имя**](a-distinguishedname.md)                                | Неверно     | **Top**      |
| [**Объект — Категория**](a-objectcategory.md)                                 | True      | **Top**      |
| [**Объектный класс**](a-objectclass.md)                                       | True      | **Top**      |
| [**Объект — GUID**](a-objectguid.md)                                         | Неверно     | **Top**      |
| [**Версия объекта**](a-objectversion.md)                                   | Неверно     | **Top**      |
| [**Другие хорошо известные объекты**](a-otherwellknownobjects.md)                 | Неверно     | **Top**      |
| [**Разделяемый атрибут-удаление-список**](a-partialattributedeletionlist.md)   | Неверно     | **Top**      |
| [**Разделяемый атрибут-set**](a-partialattributeset.md)                      | Неверно     | **Top**      |
| [**Возможно — подстрочные**](a-possibleinferiors.md)                           | Неверно     | **Top**      |
| [**Прокси-объект-имя**](a-proxiedobjectname.md)                          | Неверно     | **Top**      |
| [**Прокси-адреса**](a-proxyaddresses.md)                                 | Неверно     | **Top**      |
| [**Запрос — политика — BL**](a-querypolicybl.md)                                  | Неверно     | **Top**      |
| [**RDN**](a-name.md)                                                       | Неверно     | **Top**      |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                   | Неверно     | **Top**      |
| [**REPL-Уптодате-Vector**](a-repluptodatevector.md)                        | Неверно     | **Top**      |
| [**Отчеты**](a-directreports.md)                                          | Неверно     | **Top**      |
| [**Представители — от**](a-repsfrom.md)                                             | Неверно     | **Top**      |
| [**Представители — кому**](a-repsto.md)                                                 | Неверно     | **Top**      |
| [**Редакции**](a-revision.md)                                              | Неверно     | **Top**      |
| [**SD-Rights-эффективен**](a-sdrightseffective.md)                          | Неверно     | **Top**      |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | Неверно     | **Top**      |
| [**"Показать" — "Расширенный просмотр"**](a-showinadvancedviewonly.md)              | Неверно     | **Top**      |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Неверно     | **Top**      |
| [**Структурный объектный класс**](a-structuralobjectclass.md)                  | Неверно     | **Top**      |
| [**Подразделы-ReFS**](a-subrefs.md)                                               | Неверно     | **Top**      |
| [**субсчемасубентри**](a-subschemasubentry.md)                            | Неверно     | **Top**      |
| [**Системные флаги**](a-systemflags.md)                                       | Неверно     | **Top**      |
| [**USN-изменено**](a-usnchanged.md)                                         | Неверно     | **Top**      |
| [**Созданный USN**](a-usncreated.md)                                         | Неверно     | **Top**      |
| [**USN-DSA-Last-obj-removed**](a-usndsalastobjremoved.md)                  | Неверно     | **Top**      |
| [**USN — межсайтовая**](a-usnintersite.md)                                     | Неверно     | **Top**      |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                 | Неверно     | **Top**      |
| [**Источник USN**](a-usnsource.md)                                           | Неверно     | **Top**      |
| [**WBEM — путь**](a-wbempath.md)                                             | Неверно     | **Top**      |
| [**Хорошо известные объекты**](a-wellknownobjects.md)                            | Неверно     | **Top**      |
| [**При изменении**](a-whenchanged.md)                                       | Неверно     | **Top**      |
| [**При создании**](a-whencreated.md)                                       | Неверно     | **Top**      |
| [**WWW — Главная страница**](a-wwwhomepage.md)                                      | Неверно     | **Top**      |
| [**WWW-Page — другие**](a-url.md)                                             | Неверно     | **Top**      |



## <a name="adam"></a>ADAM

-   [Атрибуты](#adam-attributes)



| Ввод | Значение |
|-----------------------------|------------------------------------------|
| System-Only                 | True                                     |
| Object-Category             | 2                                        |
| По умолчанию — объект — Категория     | \-                                       |
| Governs-Id                  | 2.5.6.0                                  |
| По умолчанию-скрытие значения        | 1                                        |
| RDN-Атри-ID                  | [**Common-Name**](a-cn.md)<br/>   |
| Подкласс                 | **Top**<br/>                       |
| Возможные старшие          | [**Потерянные и найденные**](c-lostandfound.md) |
| Вспомогательные классы           | \-                                       |
| NT-Security-дескриптор      | О:БАГ: BAD: S:                             |
| Дескриптор безопасности по умолчанию | Д:С:                                     |
| System-Flags                | 0x00000010                               |



## <a name="adam-attributes"></a>Атрибуты ADAM

Этот класс содержит следующие атрибуты для ADAM:



| attribute                                                                   | Обязательный | Унаследован от |
|-----------------------------------------------------------------------------|-----------|--------------|
| [**Описание администратора**](a-admindescription.md)                             | Неверно     | **Top**      |
| [**Имя администратора-отображение**](a-admindisplayname.md)                            | Неверно     | **Top**      |
| [**Allowed-Attributes**](a-allowedattributes.md)                           | Неверно     | **Top**      |
| [**Allowed-Attributes-эффективен**](a-allowedattributeseffective.md)        | Неверно     | **Top**      |
| [**Allowed-Child-classes**](a-allowedchildclasses.md)                      | Неверно     | **Top**      |
| [**Allowed-Child-classes-эффективен**](a-allowedchildclasseseffective.md)   | Неверно     | **Top**      |
| [**Плацдарм-Server-List-BL**](a-bridgeheadserverlistbl.md)               | Неверно     | **Top**      |
| [**Каноническое имя**](a-canonicalname.md)                                   | Неверно     | **Top**      |
| [**Common-Name**](a-cn.md)                                                 | Неверно     | **Top**      |
| [**Метка времени создания**](a-createtimestamp.md)                              | Неверно     | **Top**      |
| [**Описание**](a-description.md)                                        | Неверно     | **Top**      |
| [**Отображаемое имя**](a-displayname.md)                                       | Неверно     | **Top**      |
| [**DSA-Signature**](a-dsasignature.md)                                     | Неверно     | **Top**      |
| [**DS-Core-распространение-данные**](a-dscorepropagationdata.md)                 | Неверно     | **Top**      |
| [**Из записи**](a-fromentry.md)                                           | Неверно     | **Top**      |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | Неверно     | **Top**      |
| [**Тип экземпляра**](a-instancetype.md)                                     | True      | **Top**      |
| [**Является критически важным — системный объект**](a-iscriticalsystemobject.md)               | Неверно     | **Top**      |
| [**Удалено**](a-isdeleted.md)                                           | Неверно     | **Top**      |
| [**Входит в состав списка рассылки**](a-memberof.md)                                       | Неверно     | **Top**      |
| [**Последний-известный-родительский**](a-lastknownparent.md)                              | Неверно     | **Top**      |
| [**Управляемые объекты**](a-managedobjects.md)                                 | Неверно     | **Top**      |
| [**В основном**](a-masteredby.md)                                         | Неверно     | **Top**      |
| [**Метка времени изменения**](a-modifytimestamp.md)                              | Неверно     | **Top**      |
| [**MS-DS-примерно-Иммед-подчиненные**](a-msds-approx-immed-subordinates.md) | Неверно     | **Top**      |
| [**MS-DS-целостность-дочерняя — количество**](a-ms-ds-consistencychildcount.md)      | Неверно     | **Top**      |
| [**MS-DS-Consistencу-Guid**](a-ms-ds-consistencyguid.md)                   | Неверно     | **Top**      |
| [**MS-DS-Disabled-for-Instances-BL**](a-msds-disableforinstancesbl.md)      | Неверно     | **Top**      |
| [**MS-DS-Masterd-by**](a-msds-masteredby.md)                              | Неверно     | **Top**      |
| [**MS-DS-NC-REPL-курсоры**](a-msds-ncreplcursors.md)                       | Неверно     | **Top**      |
| [**MS-DS-NC-REPL-Inbound-соседи**](a-msds-ncreplinboundneighbors.md)    | Неверно     | **Top**      |
| [**MS-DS-NC-REPL-Outbound-соседи**](a-msds-ncreploutboundneighbors.md)  | Неверно     | **Top**      |
| [**MS-DS-REPL-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | Неверно     | **Top**      |
| [**MS-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)              | Неверно     | **Top**      |
| [**MS-DS-Service-Account-BL**](a-msds-serviceaccountbl.md)                 | Неверно     | **Top**      |
| [**NT-Security-дескриптор**](a-ntsecuritydescriptor.md)                    | True      | **Top**      |
| [**Obj-расп-имя**](a-distinguishedname.md)                                | Неверно     | **Top**      |
| [**Объект — Категория**](a-objectcategory.md)                                 | True      | **Top**      |
| [**Объектный класс**](a-objectclass.md)                                       | True      | **Top**      |
| [**Объект — GUID**](a-objectguid.md)                                         | Неверно     | **Top**      |
| [**Версия объекта**](a-objectversion.md)                                   | Неверно     | **Top**      |
| [**Другие хорошо известные объекты**](a-otherwellknownobjects.md)                 | Неверно     | **Top**      |
| [**Разделяемый атрибут-удаление-список**](a-partialattributedeletionlist.md)   | Неверно     | **Top**      |
| [**Разделяемый атрибут-set**](a-partialattributeset.md)                      | Неверно     | **Top**      |
| [**Возможно — подстрочные**](a-possibleinferiors.md)                           | Неверно     | **Top**      |
| [**Прокси-объект-имя**](a-proxiedobjectname.md)                          | Неверно     | **Top**      |
| [**Прокси-адреса**](a-proxyaddresses.md)                                 | Неверно     | **Top**      |
| [**Запрос — политика — BL**](a-querypolicybl.md)                                  | Неверно     | **Top**      |
| [**RDN**](a-name.md)                                                       | Неверно     | **Top**      |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                   | Неверно     | **Top**      |
| [**REPL-Уптодате-Vector**](a-repluptodatevector.md)                        | Неверно     | **Top**      |
| [**Представители — от**](a-repsfrom.md)                                             | Неверно     | **Top**      |
| [**Представители — кому**](a-repsto.md)                                                 | Неверно     | **Top**      |
| [**Редакции**](a-revision.md)                                              | Неверно     | **Top**      |
| [**SD-Rights-эффективен**](a-sdrightseffective.md)                          | Неверно     | **Top**      |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | Неверно     | **Top**      |
| [**"Показать" — "Расширенный просмотр"**](a-showinadvancedviewonly.md)              | Неверно     | **Top**      |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Неверно     | **Top**      |
| [**Структурный объектный класс**](a-structuralobjectclass.md)                  | Неверно     | **Top**      |
| [**Подразделы-ReFS**](a-subrefs.md)                                               | Неверно     | **Top**      |
| [**субсчемасубентри**](a-subschemasubentry.md)                            | Неверно     | **Top**      |
| [**Системные флаги**](a-systemflags.md)                                       | Неверно     | **Top**      |
| [**USN-изменено**](a-usnchanged.md)                                         | Неверно     | **Top**      |
| [**Созданный USN**](a-usncreated.md)                                         | Неверно     | **Top**      |
| [**USN-DSA-Last-obj-removed**](a-usndsalastobjremoved.md)                  | Неверно     | **Top**      |
| [**USN — межсайтовая**](a-usnintersite.md)                                     | Неверно     | **Top**      |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                 | Неверно     | **Top**      |
| [**Источник USN**](a-usnsource.md)                                           | Неверно     | **Top**      |
| [**WBEM — путь**](a-wbempath.md)                                             | Неверно     | **Top**      |
| [**Хорошо известные объекты**](a-wellknownobjects.md)                            | Неверно     | **Top**      |
| [**При изменении**](a-whenchanged.md)                                       | Неверно     | **Top**      |
| [**При создании**](a-whencreated.md)                                       | Неверно     | **Top**      |
| [**WWW — Главная страница**](a-wwwhomepage.md)                                      | Неверно     | **Top**      |
| [**WWW-Page — другие**](a-url.md)                                             | Неверно     | **Top**      |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2

-   [Атрибуты](#windows-server-2003-r2-attributes)



| Ввод | Значение |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | True                                                                                         |
| Object-Category             | 2                                                                                            |
| По умолчанию — объект — Категория     | \-                                                                                           |
| Governs-Id                  | 2.5.6.0                                                                                      |
| По умолчанию-скрытие значения        | 1                                                                                            |
| RDN-Атри-ID                  | [**Common-Name**](a-cn.md)<br/>                                                       |
| Подкласс                 | **Top**<br/>                                                                           |
| Возможные старшие          | [**Потерянные и найденные**](c-lostandfound.md)                                                     |
| Вспомогательные классы           | \-                                                                                           |
| NT-Security-дескриптор      | О:БАГ: BAD: S:                                                                                 |
| Дескриптор безопасности по умолчанию | D: (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;;D А) (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;; SY) (A;; РПЛКЛОРК;;; СЛУЖБЫ |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2003-r2-attributes"></a>Атрибуты Windows Server 2003 R2

Этот класс содержит следующие атрибуты для Windows Server 2003 R2:



| attribute                                                                   | Обязательный | Унаследован от |
|-----------------------------------------------------------------------------|-----------|--------------|
| [**Описание администратора**](a-admindescription.md)                             | Неверно     | **Top**      |
| [**Имя администратора-отображение**](a-admindisplayname.md)                            | Неверно     | **Top**      |
| [**Allowed-Attributes**](a-allowedattributes.md)                           | Неверно     | **Top**      |
| [**Allowed-Attributes-эффективен**](a-allowedattributeseffective.md)        | Неверно     | **Top**      |
| [**Allowed-Child-classes**](a-allowedchildclasses.md)                      | Неверно     | **Top**      |
| [**Allowed-Child-classes-эффективен**](a-allowedchildclasseseffective.md)   | Неверно     | **Top**      |
| [**Плацдарм-Server-List-BL**](a-bridgeheadserverlistbl.md)               | Неверно     | **Top**      |
| [**Каноническое имя**](a-canonicalname.md)                                   | Неверно     | **Top**      |
| [**Common-Name**](a-cn.md)                                                 | Неверно     | **Top**      |
| [**Метка времени создания**](a-createtimestamp.md)                              | Неверно     | **Top**      |
| [**Описание**](a-description.md)                                        | Неверно     | **Top**      |
| [**Отображаемое имя**](a-displayname.md)                                       | Неверно     | **Top**      |
| [**Отображаемое имя — печатаемое**](a-displaynameprintable.md)                    | Неверно     | **Top**      |
| [**DSA-Signature**](a-dsasignature.md)                                     | Неверно     | **Top**      |
| [**DS-Core-распространение-данные**](a-dscorepropagationdata.md)                 | Неверно     | **Top**      |
| [**Имя расширения**](a-extensionname.md)                                   | Неверно     | **Top**      |
| [**Метки**](a-flags.md)                                                    | Неверно     | **Top**      |
| [**Из записи**](a-fromentry.md)                                           | Неверно     | **Top**      |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | Неверно     | **Top**      |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | Неверно     | **Top**      |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | Неверно     | **Top**      |
| [**Тип экземпляра**](a-instancetype.md)                                     | True      | **Top**      |
| [**Является критически важным — системный объект**](a-iscriticalsystemobject.md)               | Неверно     | **Top**      |
| [**Удалено**](a-isdeleted.md)                                           | Неверно     | **Top**      |
| [**Входит в состав списка рассылки**](a-memberof.md)                                       | Неверно     | **Top**      |
| [**Имеет права владельца**](a-isprivilegeholder.md)                          | Неверно     | **Top**      |
| [**Последний-известный-родительский**](a-lastknownparent.md)                              | Неверно     | **Top**      |
| [**Управляемые объекты**](a-managedobjects.md)                                 | Неверно     | **Top**      |
| [**В основном**](a-masteredby.md)                                         | Неверно     | **Top**      |
| [**Метка времени изменения**](a-modifytimestamp.md)                              | Неверно     | **Top**      |
| [**MS-COM-Партитионсетлинк**](a-mscom-partitionsetlink.md)                 | Неверно     | **Top**      |
| [**MS-COM-Усерлинк**](a-mscom-userlink.md)                                 | Неверно     | **Top**      |
| [**MS-DFSR-Компутерреференцебл**](a-msdfsr-computerreferencebl.md)         | Неверно     | **Top**      |
| [**MS-DFSR-Мемберреференцебл**](a-msdfsr-memberreferencebl.md)             | Неверно     | **Top**      |
| [**MS-DS-примерно-Иммед-подчиненные**](a-msds-approx-immed-subordinates.md) | Неверно     | **Top**      |
| [**MS-DS-целостность-дочерняя — количество**](a-ms-ds-consistencychildcount.md)      | Неверно     | **Top**      |
| [**MS-DS-Consistencу-Guid**](a-ms-ds-consistencyguid.md)                   | Неверно     | **Top**      |
| [**MS-DS-Masterd-by**](a-msds-masteredby.md)                              | Неверно     | **Top**      |
| [**MS-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)           | Неверно     | **Top**      |
| [**MS-DS-NC-REPL-курсоры**](a-msds-ncreplcursors.md)                       | Неверно     | **Top**      |
| [**MS-DS-NC-REPL-Inbound-соседи**](a-msds-ncreplinboundneighbors.md)    | Неверно     | **Top**      |
| [**MS-DS-NC-REPL-Outbound-соседи**](a-msds-ncreploutboundneighbors.md)  | Неверно     | **Top**      |
| [**MS-DS-не-Members-BL**](a-msds-nonmembersbl.md)                         | Неверно     | **Top**      |
| [**MS-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | Неверно     | **Top**      |
| [**MS-DS-Operations-для-AZ-Role-BL**](a-msds-operationsforazrolebl.md)     | Неверно     | **Top**      |
| [**MS-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)     | Неверно     | **Top**      |
| [**MS-DS-REPL-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | Неверно     | **Top**      |
| [**MS-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)              | Неверно     | **Top**      |
| [**MS-DS-Tasks-для-AZ-Role-BL**](a-msds-tasksforazrolebl.md)               | Неверно     | **Top**      |
| [**MS-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)               | Неверно     | **Top**      |
| [**MS-дов-Owner-BL**](a-ownerbl.md)                                       | Неверно     | **Top**      |
| [**Мссфу-30-POSIX-член-of**](a-mssfu30posixmemberof.md)                  | Неверно     | **Top**      |
| [**нетбут-SCP-BL**](a-netbootscpbl.md)                                    | Неверно     | **Top**      |
| [**Не-Security-Member-BL**](a-nonsecuritymemberbl.md)                     | Неверно     | **Top**      |
| [**NT-Security-дескриптор**](a-ntsecuritydescriptor.md)                    | True      | **Top**      |
| [**Obj-расп-имя**](a-distinguishedname.md)                                | Неверно     | **Top**      |
| [**Объект — Категория**](a-objectcategory.md)                                 | True      | **Top**      |
| [**Объектный класс**](a-objectclass.md)                                       | True      | **Top**      |
| [**Объект — GUID**](a-objectguid.md)                                         | Неверно     | **Top**      |
| [**Версия объекта**](a-objectversion.md)                                   | Неверно     | **Top**      |
| [**Другие хорошо известные объекты**](a-otherwellknownobjects.md)                 | Неверно     | **Top**      |
| [**Разделяемый атрибут-удаление-список**](a-partialattributedeletionlist.md)   | Неверно     | **Top**      |
| [**Разделяемый атрибут-set**](a-partialattributeset.md)                      | Неверно     | **Top**      |
| [**Возможно — подстрочные**](a-possibleinferiors.md)                           | Неверно     | **Top**      |
| [**Прокси-объект-имя**](a-proxiedobjectname.md)                          | Неверно     | **Top**      |
| [**Прокси-адреса**](a-proxyaddresses.md)                                 | Неверно     | **Top**      |
| [**Запрос — политика — BL**](a-querypolicybl.md)                                  | Неверно     | **Top**      |
| [**RDN**](a-name.md)                                                       | Неверно     | **Top**      |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                   | Неверно     | **Top**      |
| [**REPL-Уптодате-Vector**](a-repluptodatevector.md)                        | Неверно     | **Top**      |
| [**Отчеты**](a-directreports.md)                                          | Неверно     | **Top**      |
| [**Представители — от**](a-repsfrom.md)                                             | Неверно     | **Top**      |
| [**Представители — кому**](a-repsto.md)                                                 | Неверно     | **Top**      |
| [**Редакции**](a-revision.md)                                              | Неверно     | **Top**      |
| [**SD-Rights-эффективен**](a-sdrightseffective.md)                          | Неверно     | **Top**      |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | Неверно     | **Top**      |
| [**"Показать" — "Расширенный просмотр"**](a-showinadvancedviewonly.md)              | Неверно     | **Top**      |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Неверно     | **Top**      |
| [**Структурный объектный класс**](a-structuralobjectclass.md)                  | Неверно     | **Top**      |
| [**Подразделы-ReFS**](a-subrefs.md)                                               | Неверно     | **Top**      |
| [**субсчемасубентри**](a-subschemasubentry.md)                            | Неверно     | **Top**      |
| [**Системные флаги**](a-systemflags.md)                                       | Неверно     | **Top**      |
| [**USN-изменено**](a-usnchanged.md)                                         | Неверно     | **Top**      |
| [**Созданный USN**](a-usncreated.md)                                         | Неверно     | **Top**      |
| [**USN-DSA-Last-obj-removed**](a-usndsalastobjremoved.md)                  | Неверно     | **Top**      |
| [**USN — межсайтовая**](a-usnintersite.md)                                     | Неверно     | **Top**      |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                 | Неверно     | **Top**      |
| [**Источник USN**](a-usnsource.md)                                           | Неверно     | **Top**      |
| [**WBEM — путь**](a-wbempath.md)                                             | Неверно     | **Top**      |
| [**Хорошо известные объекты**](a-wellknownobjects.md)                            | Неверно     | **Top**      |
| [**При изменении**](a-whenchanged.md)                                       | Неверно     | **Top**      |
| [**При создании**](a-whencreated.md)                                       | Неверно     | **Top**      |
| [**WWW — Главная страница**](a-wwwhomepage.md)                                      | Неверно     | **Top**      |
| [**WWW-Page — другие**](a-url.md)                                             | Неверно     | **Top**      |



## <a name="windows-server-2008"></a>Windows Server 2008

-   [Атрибуты](#windows-server-2008-attributes)



| Ввод | Значение |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | True                                                                                         |
| Object-Category             | 2                                                                                            |
| По умолчанию — объект — Категория     | \-                                                                                           |
| Governs-Id                  | 2.5.6.0                                                                                      |
| По умолчанию-скрытие значения        | 1                                                                                            |
| RDN-Атри-ID                  | [**Common-Name**](a-cn.md)<br/>                                                       |
| Подкласс                 | **Top**<br/>                                                                           |
| Возможные старшие          | [**Потерянные и найденные**](c-lostandfound.md)                                                     |
| Вспомогательные классы           | \-                                                                                           |
| NT-Security-дескриптор      | О:БАГ: BAD: S:                                                                                 |
| Дескриптор безопасности по умолчанию | D: (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;;D А) (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;; SY) (A;; РПЛКЛОРК;;; СЛУЖБЫ |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2008-attributes"></a>Атрибуты Windows Server 2008

Этот класс содержит следующие атрибуты для Windows Server 2008:



| attribute                                                                      | Обязательный | Унаследован от |
|--------------------------------------------------------------------------------|-----------|--------------|
| [**Описание администратора**](a-admindescription.md)                                | Неверно     | **Top**      |
| [**Имя администратора-отображение**](a-admindisplayname.md)                               | Неверно     | **Top**      |
| [**Allowed-Attributes**](a-allowedattributes.md)                              | Неверно     | **Top**      |
| [**Allowed-Attributes-эффективен**](a-allowedattributeseffective.md)           | Неверно     | **Top**      |
| [**Allowed-Child-classes**](a-allowedchildclasses.md)                         | Неверно     | **Top**      |
| [**Allowed-Child-classes-эффективен**](a-allowedchildclasseseffective.md)      | Неверно     | **Top**      |
| [**Плацдарм-Server-List-BL**](a-bridgeheadserverlistbl.md)                  | Неверно     | **Top**      |
| [**Каноническое имя**](a-canonicalname.md)                                      | Неверно     | **Top**      |
| [**Common-Name**](a-cn.md)                                                    | Неверно     | **Top**      |
| [**Метка времени создания**](a-createtimestamp.md)                                 | Неверно     | **Top**      |
| [**Описание**](a-description.md)                                           | Неверно     | **Top**      |
| [**Отображаемое имя**](a-displayname.md)                                          | Неверно     | **Top**      |
| [**Отображаемое имя — печатаемое**](a-displaynameprintable.md)                       | Неверно     | **Top**      |
| [**DSA-Signature**](a-dsasignature.md)                                        | Неверно     | **Top**      |
| [**DS-Core-распространение-данные**](a-dscorepropagationdata.md)                    | Неверно     | **Top**      |
| [**Имя расширения**](a-extensionname.md)                                      | Неверно     | **Top**      |
| [**Метки**](a-flags.md)                                                       | Неверно     | **Top**      |
| [**Из записи**](a-fromentry.md)                                              | Неверно     | **Top**      |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                  | Неверно     | **Top**      |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                      | Неверно     | **Top**      |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                     | Неверно     | **Top**      |
| [**Тип экземпляра**](a-instancetype.md)                                        | True      | **Top**      |
| [**Является критически важным — системный объект**](a-iscriticalsystemobject.md)                  | Неверно     | **Top**      |
| [**Удалено**](a-isdeleted.md)                                              | Неверно     | **Top**      |
| [**Входит в состав списка рассылки**](a-memberof.md)                                          | Неверно     | **Top**      |
| [**Имеет права владельца**](a-isprivilegeholder.md)                             | Неверно     | **Top**      |
| [**Последний-известный-родительский**](a-lastknownparent.md)                                 | Неверно     | **Top**      |
| [**Управляемые объекты**](a-managedobjects.md)                                    | Неверно     | **Top**      |
| [**В основном**](a-masteredby.md)                                            | Неверно     | **Top**      |
| [**Метка времени изменения**](a-modifytimestamp.md)                                 | Неверно     | **Top**      |
| [**MS-COM-Партитионсетлинк**](a-mscom-partitionsetlink.md)                    | Неверно     | **Top**      |
| [**MS-COM-Усерлинк**](a-mscom-userlink.md)                                    | Неверно     | **Top**      |
| [**MS-DFSR-Компутерреференцебл**](a-msdfsr-computerreferencebl.md)            | Неверно     | **Top**      |
| [**MS-DFSR-Мемберреференцебл**](a-msdfsr-memberreferencebl.md)                | Неверно     | **Top**      |
| [**MS-DS-примерно-Иммед-подчиненные**](a-msds-approx-immed-subordinates.md)    | Неверно     | **Top**      |
| [**MS-DS-Аусентикатедто-Аккаунтлист**](a-msds-authenticatedtoaccountlist.md) | Неверно     | **Top**      |
| [**MS-DS-целостность-дочерняя — количество**](a-ms-ds-consistencychildcount.md)         | Неверно     | **Top**      |
| [**MS-DS-Consistencу-Guid**](a-ms-ds-consistencyguid.md)                      | Неверно     | **Top**      |
| [**MS-DS--домен — для**](a-msds-isdomainfor.md)                              | Неверно     | **Top**      |
| [**MS-DS-является-Full-реплика для**](a-msds-isfullreplicafor.md)                   | Неверно     | **Top**      |
| [**MS-DS-является-partial-реплика для**](a-msds-ispartialreplicafor.md)             | Неверно     | **Top**      |
| [**MS-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                            | Неверно     | **Top**      |
| [**MS-DS-Masterd-by**](a-msds-masteredby.md)                                 | Неверно     | **Top**      |
| [**MS-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)              | Неверно     | **Top**      |
| [**MS-DS-NC-REPL-курсоры**](a-msds-ncreplcursors.md)                          | Неверно     | **Top**      |
| [**MS-DS-NC-REPL-Inbound-соседи**](a-msds-ncreplinboundneighbors.md)       | Неверно     | **Top**      |
| [**MS-DS-NC-REPL-Outbound-соседи**](a-msds-ncreploutboundneighbors.md)     | Неверно     | **Top**      |
| [**MS-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)  | Неверно     | **Top**      |
| [**MS-DS-NC-Type**](a-msds-nctype.md)                                         | Неверно     | **Top**      |
| [**MS-DS-не-Members-BL**](a-msds-nonmembersbl.md)                            | Неверно     | **Top**      |
| [**MS-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                  | Неверно     | **Top**      |
| [**MS-DS-Operations-для-AZ-Role-BL**](a-msds-operationsforazrolebl.md)        | Неверно     | **Top**      |
| [**MS-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)        | Неверно     | **Top**      |
| [**MS-DS-Principal-Name**](a-msds-principalname.md)                           | Неверно     | **Top**      |
| [**MS-DS-PSO — применяется**](a-msds-psoapplied.md)                                 | Неверно     | **Top**      |
| [**MS-DS-REPL-Attribute-Meta-Data**](a-msds-replattributemetadata.md)         | Неверно     | **Top**      |
| [**MS-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)                 | Неверно     | **Top**      |
| [**MS-DS-выявил-DSA**](a-msds-revealeddsas.md)                             | Неверно     | **Top**      |
| [**MS-DS-выводит-List-BL**](a-msds-revealedlistbl.md)                        | Неверно     | **Top**      |
| [**MS-DS-Tasks-для-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                  | Неверно     | **Top**      |
| [**MS-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                  | Неверно     | **Top**      |
| [**MS-дов-Owner-BL**](a-ownerbl.md)                                          | Неверно     | **Top**      |
| [**Мссфу-30-POSIX-член-of**](a-mssfu30posixmemberof.md)                     | Неверно     | **Top**      |
| [**нетбут-SCP-BL**](a-netbootscpbl.md)                                       | Неверно     | **Top**      |
| [**Не-Security-Member-BL**](a-nonsecuritymemberbl.md)                        | Неверно     | **Top**      |
| [**NT-Security-дескриптор**](a-ntsecuritydescriptor.md)                       | True      | **Top**      |
| [**Obj-расп-имя**](a-distinguishedname.md)                                   | Неверно     | **Top**      |
| [**Объект — Категория**](a-objectcategory.md)                                    | True      | **Top**      |
| [**Объектный класс**](a-objectclass.md)                                          | True      | **Top**      |
| [**Объект — GUID**](a-objectguid.md)                                            | Неверно     | **Top**      |
| [**Версия объекта**](a-objectversion.md)                                      | Неверно     | **Top**      |
| [**Другие хорошо известные объекты**](a-otherwellknownobjects.md)                    | Неверно     | **Top**      |
| [**Разделяемый атрибут-удаление-список**](a-partialattributedeletionlist.md)      | Неверно     | **Top**      |
| [**Разделяемый атрибут-set**](a-partialattributeset.md)                         | Неверно     | **Top**      |
| [**Возможно — подстрочные**](a-possibleinferiors.md)                              | Неверно     | **Top**      |
| [**Прокси-объект-имя**](a-proxiedobjectname.md)                             | Неверно     | **Top**      |
| [**Прокси-адреса**](a-proxyaddresses.md)                                    | Неверно     | **Top**      |
| [**Запрос — политика — BL**](a-querypolicybl.md)                                     | Неверно     | **Top**      |
| [**RDN**](a-name.md)                                                          | Неверно     | **Top**      |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                      | Неверно     | **Top**      |
| [**REPL-Уптодате-Vector**](a-repluptodatevector.md)                           | Неверно     | **Top**      |
| [**Отчеты**](a-directreports.md)                                             | Неверно     | **Top**      |
| [**Представители — от**](a-repsfrom.md)                                                | Неверно     | **Top**      |
| [**Представители — кому**](a-repsto.md)                                                    | Неверно     | **Top**      |
| [**Редакции**](a-revision.md)                                                 | Неверно     | **Top**      |
| [**SD-Rights-эффективен**](a-sdrightseffective.md)                             | Неверно     | **Top**      |
| [**Server-Reference-BL**](a-serverreferencebl.md)                             | Неверно     | **Top**      |
| [**"Показать" — "Расширенный просмотр"**](a-showinadvancedviewonly.md)                 | Неверно     | **Top**      |
| [**Site-Object-BL**](a-siteobjectbl.md)                                       | Неверно     | **Top**      |
| [**Структурный объектный класс**](a-structuralobjectclass.md)                     | Неверно     | **Top**      |
| [**Подразделы-ReFS**](a-subrefs.md)                                                  | Неверно     | **Top**      |
| [**субсчемасубентри**](a-subschemasubentry.md)                               | Неверно     | **Top**      |
| [**Системные флаги**](a-systemflags.md)                                          | Неверно     | **Top**      |
| [**USN-изменено**](a-usnchanged.md)                                            | Неверно     | **Top**      |
| [**Созданный USN**](a-usncreated.md)                                            | Неверно     | **Top**      |
| [**USN-DSA-Last-obj-removed**](a-usndsalastobjremoved.md)                     | Неверно     | **Top**      |
| [**USN — межсайтовая**](a-usnintersite.md)                                        | Неверно     | **Top**      |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                    | Неверно     | **Top**      |
| [**Источник USN**](a-usnsource.md)                                              | Неверно     | **Top**      |
| [**WBEM — путь**](a-wbempath.md)                                                | Неверно     | **Top**      |
| [**Хорошо известные объекты**](a-wellknownobjects.md)                               | Неверно     | **Top**      |
| [**При изменении**](a-whenchanged.md)                                          | Неверно     | **Top**      |
| [**При создании**](a-whencreated.md)                                          | Неверно     | **Top**      |
| [**WWW — Главная страница**](a-wwwhomepage.md)                                         | Неверно     | **Top**      |
| [**WWW-Page — другие**](a-url.md)                                                | Неверно     | **Top**      |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2

-   [Атрибуты](#windows-server-2008-r2-attributes)



| Ввод | Значение |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | True                                                                                         |
| Object-Category             | 2                                                                                            |
| По умолчанию — объект — Категория     | \-                                                                                           |
| Governs-Id                  | 2.5.6.0                                                                                      |
| По умолчанию-скрытие значения        | 1                                                                                            |
| RDN-Атри-ID                  | [**Common-Name**](a-cn.md)<br/>                                                       |
| Подкласс                 | **Top**<br/>                                                                           |
| Возможные старшие          | [**Потерянные и найденные**](c-lostandfound.md)                                                     |
| Вспомогательные классы           | \-                                                                                           |
| NT-Security-дескриптор      | О:БАГ: BAD: S:                                                                                 |
| Дескриптор безопасности по умолчанию | D: (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;;D А) (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;; SY) (A;; РПЛКЛОРК;;; СЛУЖБЫ |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2008-r2-attributes"></a>Атрибуты Windows Server 2008 R2

Этот класс содержит следующие атрибуты для Windows Server 2008 R2:



| attribute                                                                        | Обязательный | Унаследован от |
|----------------------------------------------------------------------------------|-----------|--------------|
| [**Описание администратора**](a-admindescription.md)                                  | Неверно     | **Top**      |
| [**Имя администратора-отображение**](a-admindisplayname.md)                                 | Неверно     | **Top**      |
| [**Allowed-Attributes**](a-allowedattributes.md)                                | Неверно     | **Top**      |
| [**Allowed-Attributes-эффективен**](a-allowedattributeseffective.md)             | Неверно     | **Top**      |
| [**Allowed-Child-classes**](a-allowedchildclasses.md)                           | Неверно     | **Top**      |
| [**Allowed-Child-classes-эффективен**](a-allowedchildclasseseffective.md)        | Неверно     | **Top**      |
| [**Плацдарм-Server-List-BL**](a-bridgeheadserverlistbl.md)                    | Неверно     | **Top**      |
| [**Каноническое имя**](a-canonicalname.md)                                        | Неверно     | **Top**      |
| [**Common-Name**](a-cn.md)                                                      | Неверно     | **Top**      |
| [**Метка времени создания**](a-createtimestamp.md)                                   | Неверно     | **Top**      |
| [**Описание**](a-description.md)                                             | Неверно     | **Top**      |
| [**Отображаемое имя**](a-displayname.md)                                            | Неверно     | **Top**      |
| [**Отображаемое имя — печатаемое**](a-displaynameprintable.md)                         | Неверно     | **Top**      |
| [**DSA-Signature**](a-dsasignature.md)                                          | Неверно     | **Top**      |
| [**DS-Core-распространение-данные**](a-dscorepropagationdata.md)                      | Неверно     | **Top**      |
| [**Имя расширения**](a-extensionname.md)                                        | Неверно     | **Top**      |
| [**Метки**](a-flags.md)                                                         | Неверно     | **Top**      |
| [**Из записи**](a-fromentry.md)                                                | Неверно     | **Top**      |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                    | Неверно     | **Top**      |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                        | Неверно     | **Top**      |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                       | Неверно     | **Top**      |
| [**Тип экземпляра**](a-instancetype.md)                                          | True      | **Top**      |
| [**Является критически важным — системный объект**](a-iscriticalsystemobject.md)                    | Неверно     | **Top**      |
| [**Удалено**](a-isdeleted.md)                                                | Неверно     | **Top**      |
| [**Входит в состав списка рассылки**](a-memberof.md)                                            | Неверно     | **Top**      |
| [**Имеет права владельца**](a-isprivilegeholder.md)                               | Неверно     | **Top**      |
| [**Является перезапущенным**](a-isrecycled.md)                                              | Неверно     | **Top**      |
| [**Последний-известный-родительский**](a-lastknownparent.md)                                   | Неверно     | **Top**      |
| [**Управляемые объекты**](a-managedobjects.md)                                      | Неверно     | **Top**      |
| [**В основном**](a-masteredby.md)                                              | Неверно     | **Top**      |
| [**Метка времени изменения**](a-modifytimestamp.md)                                   | Неверно     | **Top**      |
| [**MS-COM-Партитионсетлинк**](a-mscom-partitionsetlink.md)                      | Неверно     | **Top**      |
| [**MS-COM-Усерлинк**](a-mscom-userlink.md)                                      | Неверно     | **Top**      |
| [**MS-DFSR-Компутерреференцебл**](a-msdfsr-computerreferencebl.md)              | Неверно     | **Top**      |
| [**MS-DFSR-Мемберреференцебл**](a-msdfsr-memberreferencebl.md)                  | Неверно     | **Top**      |
| [**MS-DS-примерно-Иммед-подчиненные**](a-msds-approx-immed-subordinates.md)      | Неверно     | **Top**      |
| [**MS-DS-Аусентикатедто-Аккаунтлист**](a-msds-authenticatedtoaccountlist.md)   | Неверно     | **Top**      |
| [**MS-DS-целостность-дочерняя — количество**](a-ms-ds-consistencychildcount.md)           | Неверно     | **Top**      |
| [**MS-DS-Consistencу-Guid**](a-ms-ds-consistencyguid.md)                        | Неверно     | **Top**      |
| [**Поддержка MS-DS-Feature-BL**](a-msds-enabledfeaturebl.md)                      | Неверно     | **Top**      |
| [**MS-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)             | Неверно     | **Top**      |
| [**MS-DS--домен — для**](a-msds-isdomainfor.md)                                | Неверно     | **Top**      |
| [**MS-DS-является-Full-реплика для**](a-msds-isfullreplicafor.md)                     | Неверно     | **Top**      |
| [**MS-DS-является-partial-реплика для**](a-msds-ispartialreplicafor.md)               | Неверно     | **Top**      |
| [**MS-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                              | Неверно     | **Top**      |
| [**MS-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                              | Неверно     | **Top**      |
| [**MS-DS-локально-эффективное удаление — время**](a-msds-localeffectivedeletiontime.md) | Неверно     | **Top**      |
| [**MS-DS-Local-эффективен — время перезапуска**](a-msds-localeffectiverecycletime.md)   | Неверно     | **Top**      |
| [**MS-DS-Masterd-by**](a-msds-masteredby.md)                                   | Неверно     | **Top**      |
| [**MS-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)                | Неверно     | **Top**      |
| [**MS-DS-NC-REPL-курсоры**](a-msds-ncreplcursors.md)                            | Неверно     | **Top**      |
| [**MS-DS-NC-REPL-Inbound-соседи**](a-msds-ncreplinboundneighbors.md)         | Неверно     | **Top**      |
| [**MS-DS-NC-REPL-Outbound-соседи**](a-msds-ncreploutboundneighbors.md)       | Неверно     | **Top**      |
| [**MS-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)    | Неверно     | **Top**      |
| [**MS-DS-NC-Type**](a-msds-nctype.md)                                           | Неверно     | **Top**      |
| [**MS-DS-не-Members-BL**](a-msds-nonmembersbl.md)                              | Неверно     | **Top**      |
| [**MS-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                    | Неверно     | **Top**      |
| [**MS-DS-Оидтограуп-Link-BL**](a-msds-oidtogrouplinkbl.md)                      | Неверно     | **Top**      |
| [**MS-DS-Operations-для-AZ-Role-BL**](a-msds-operationsforazrolebl.md)          | Неверно     | **Top**      |
| [**MS-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)          | Неверно     | **Top**      |
| [**MS-DS-Principal-Name**](a-msds-principalname.md)                             | Неверно     | **Top**      |
| [**MS-DS-PSO — применяется**](a-msds-psoapplied.md)                                   | Неверно     | **Top**      |
| [**MS-DS-REPL-Attribute-Meta-Data**](a-msds-replattributemetadata.md)           | Неверно     | **Top**      |
| [**MS-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)                   | Неверно     | **Top**      |
| [**MS-DS-выявил-DSA**](a-msds-revealeddsas.md)                               | Неверно     | **Top**      |
| [**MS-DS-выводит-List-BL**](a-msds-revealedlistbl.md)                          | Неверно     | **Top**      |
| [**MS-DS-Tasks-для-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                    | Неверно     | **Top**      |
| [**MS-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                    | Неверно     | **Top**      |
| [**MS-дов-Owner-BL**](a-ownerbl.md)                                            | Неверно     | **Top**      |
| [**Мссфу-30-POSIX-член-of**](a-mssfu30posixmemberof.md)                       | Неверно     | **Top**      |
| [**нетбут-SCP-BL**](a-netbootscpbl.md)                                         | Неверно     | **Top**      |
| [**Не-Security-Member-BL**](a-nonsecuritymemberbl.md)                          | Неверно     | **Top**      |
| [**NT-Security-дескриптор**](a-ntsecuritydescriptor.md)                         | True      | **Top**      |
| [**Obj-расп-имя**](a-distinguishedname.md)                                     | Неверно     | **Top**      |
| [**Объект — Категория**](a-objectcategory.md)                                      | True      | **Top**      |
| [**Объектный класс**](a-objectclass.md)                                            | True      | **Top**      |
| [**Объект — GUID**](a-objectguid.md)                                              | Неверно     | **Top**      |
| [**Версия объекта**](a-objectversion.md)                                        | Неверно     | **Top**      |
| [**Другие хорошо известные объекты**](a-otherwellknownobjects.md)                      | Неверно     | **Top**      |
| [**Разделяемый атрибут-удаление-список**](a-partialattributedeletionlist.md)        | Неверно     | **Top**      |
| [**Разделяемый атрибут-set**](a-partialattributeset.md)                           | Неверно     | **Top**      |
| [**Возможно — подстрочные**](a-possibleinferiors.md)                                | Неверно     | **Top**      |
| [**Прокси-объект-имя**](a-proxiedobjectname.md)                               | Неверно     | **Top**      |
| [**Прокси-адреса**](a-proxyaddresses.md)                                      | Неверно     | **Top**      |
| [**Запрос — политика — BL**](a-querypolicybl.md)                                       | Неверно     | **Top**      |
| [**RDN**](a-name.md)                                                            | Неверно     | **Top**      |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                        | Неверно     | **Top**      |
| [**REPL-Уптодате-Vector**](a-repluptodatevector.md)                             | Неверно     | **Top**      |
| [**Отчеты**](a-directreports.md)                                               | Неверно     | **Top**      |
| [**Представители — от**](a-repsfrom.md)                                                  | Неверно     | **Top**      |
| [**Представители — кому**](a-repsto.md)                                                      | Неверно     | **Top**      |
| [**Редакции**](a-revision.md)                                                   | Неверно     | **Top**      |
| [**SD-Rights-эффективен**](a-sdrightseffective.md)                               | Неверно     | **Top**      |
| [**Server-Reference-BL**](a-serverreferencebl.md)                               | Неверно     | **Top**      |
| [**"Показать" — "Расширенный просмотр"**](a-showinadvancedviewonly.md)                   | Неверно     | **Top**      |
| [**Site-Object-BL**](a-siteobjectbl.md)                                         | Неверно     | **Top**      |
| [**Структурный объектный класс**](a-structuralobjectclass.md)                       | Неверно     | **Top**      |
| [**Подразделы-ReFS**](a-subrefs.md)                                                    | Неверно     | **Top**      |
| [**субсчемасубентри**](a-subschemasubentry.md)                                 | Неверно     | **Top**      |
| [**Системные флаги**](a-systemflags.md)                                            | Неверно     | **Top**      |
| [**USN-изменено**](a-usnchanged.md)                                              | Неверно     | **Top**      |
| [**Созданный USN**](a-usncreated.md)                                              | Неверно     | **Top**      |
| [**USN-DSA-Last-obj-removed**](a-usndsalastobjremoved.md)                       | Неверно     | **Top**      |
| [**USN — межсайтовая**](a-usnintersite.md)                                          | Неверно     | **Top**      |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                      | Неверно     | **Top**      |
| [**Источник USN**](a-usnsource.md)                                                | Неверно     | **Top**      |
| [**WBEM — путь**](a-wbempath.md)                                                  | Неверно     | **Top**      |
| [**Хорошо известные объекты**](a-wellknownobjects.md)                                 | Неверно     | **Top**      |
| [**При изменении**](a-whenchanged.md)                                            | Неверно     | **Top**      |
| [**При создании**](a-whencreated.md)                                            | Неверно     | **Top**      |
| [**WWW — Главная страница**](a-wwwhomepage.md)                                           | Неверно     | **Top**      |
| [**WWW-Page — другие**](a-url.md)                                                  | Неверно     | **Top**      |



## <a name="windows-server-2012"></a>Windows Server 2012

-   [Атрибуты](#windows-server-2012-attributes)



| Ввод | Значение |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | True                                                                                         |
| Object-Category             | 2                                                                                            |
| По умолчанию — объект — Категория     | \-                                                                                           |
| Governs-Id                  | 2.5.6.0                                                                                      |
| По умолчанию-скрытие значения        | 1                                                                                            |
| RDN-Атри-ID                  | [**Common-Name**](a-cn.md)<br/>                                                       |
| Подкласс                 | **Top**<br/>                                                                           |
| Возможные старшие          | [**Потерянные и найденные**](c-lostandfound.md)                                                     |
| Вспомогательные классы           | \-                                                                                           |
| NT-Security-дескриптор      | О:БАГ: BAD: S:                                                                                 |
| Дескриптор безопасности по умолчанию | D: (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;;D А) (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;; SY) (A;; РПЛКЛОРК;;; СЛУЖБЫ |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2012-attributes"></a>Атрибуты Windows Server 2012

Этот класс содержит следующие атрибуты для Windows Server 2012:



| attribute                                                                                    | Обязательный | Унаследован от |
|----------------------------------------------------------------------------------------------|-----------|--------------|
| [**Описание администратора**](a-admindescription.md)                                              | Неверно     | **Top**      |
| [**Имя администратора-отображение**](a-admindisplayname.md)                                             | Неверно     | **Top**      |
| [**Allowed-Attributes**](a-allowedattributes.md)                                            | Неверно     | **Top**      |
| [**Allowed-Attributes-эффективен**](a-allowedattributeseffective.md)                         | Неверно     | **Top**      |
| [**Allowed-Child-classes**](a-allowedchildclasses.md)                                       | Неверно     | **Top**      |
| [**Allowed-Child-classes-эффективен**](a-allowedchildclasseseffective.md)                    | Неверно     | **Top**      |
| [**Плацдарм-Server-List-BL**](a-bridgeheadserverlistbl.md)                                | Неверно     | **Top**      |
| [**Каноническое имя**](a-canonicalname.md)                                                    | Неверно     | **Top**      |
| [**Common-Name**](a-cn.md)                                                                  | Неверно     | **Top**      |
| [**Метка времени создания**](a-createtimestamp.md)                                               | Неверно     | **Top**      |
| [**Описание**](a-description.md)                                                         | Неверно     | **Top**      |
| [**Отображаемое имя**](a-displayname.md)                                                        | Неверно     | **Top**      |
| [**Отображаемое имя — печатаемое**](a-displaynameprintable.md)                                     | Неверно     | **Top**      |
| [**DSA-Signature**](a-dsasignature.md)                                                      | Неверно     | **Top**      |
| [**DS-Core-распространение-данные**](a-dscorepropagationdata.md)                                  | Неверно     | **Top**      |
| [**Имя расширения**](a-extensionname.md)                                                    | Неверно     | **Top**      |
| [**Метки**](a-flags.md)                                                                     | Неверно     | **Top**      |
| [**Из записи**](a-fromentry.md)                                                            | Неверно     | **Top**      |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                                | Неверно     | **Top**      |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                                    | Неверно     | **Top**      |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                                   | Неверно     | **Top**      |
| [**Тип экземпляра**](a-instancetype.md)                                                      | True      | **Top**      |
| [**Является критически важным — системный объект**](a-iscriticalsystemobject.md)                                | Неверно     | **Top**      |
| [**Удалено**](a-isdeleted.md)                                                            | Неверно     | **Top**      |
| [**Входит в состав списка рассылки**](a-memberof.md)                                                        | Неверно     | **Top**      |
| [**Имеет права владельца**](a-isprivilegeholder.md)                                           | Неверно     | **Top**      |
| [**Является перезапущенным**](a-isrecycled.md)                                                          | Неверно     | **Top**      |
| [**Последний-известный-родительский**](a-lastknownparent.md)                                               | Неверно     | **Top**      |
| [**Управляемые объекты**](a-managedobjects.md)                                                  | Неверно     | **Top**      |
| [**В основном**](a-masteredby.md)                                                          | Неверно     | **Top**      |
| [**Метка времени изменения**](a-modifytimestamp.md)                                               | Неверно     | **Top**      |
| [**MS-COM-Партитионсетлинк**](a-mscom-partitionsetlink.md)                                  | Неверно     | **Top**      |
| [**MS-COM-Усерлинк**](a-mscom-userlink.md)                                                  | Неверно     | **Top**      |
| [**MS-DFSR-Компутерреференцебл**](a-msdfsr-computerreferencebl.md)                          | Неверно     | **Top**      |
| [**MS-DFSR-Мемберреференцебл**](a-msdfsr-memberreferencebl.md)                              | Неверно     | **Top**      |
| [**MS-DS-примерно-Иммед-подчиненные**](a-msds-approx-immed-subordinates.md)                  | Неверно     | **Top**      |
| [**MS-DS-Аусентикатедто-Аккаунтлист**](a-msds-authenticatedtoaccountlist.md)               | Неверно     | **Top**      |
| [**MS-DS-ClaimSet-shares-возможные значения-with-BL**](a-msds-claimsharespossiblevalueswithbl.md) | Неверно     | **Top**      |
| [**MS-DS-целостность-дочерняя — количество**](a-ms-ds-consistencychildcount.md)                       | Неверно     | **Top**      |
| [**MS-DS-Consistencу-Guid**](a-ms-ds-consistencyguid.md)                                    | Неверно     | **Top**      |
| [**Поддержка MS-DS-Feature-BL**](a-msds-enabledfeaturebl.md)                                  | Неверно     | **Top**      |
| [**MS-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)                         | Неверно     | **Top**      |
| [**MS-DS--домен — для**](a-msds-isdomainfor.md)                                            | Неверно     | **Top**      |
| [**MS-DS-является-Full-реплика для**](a-msds-isfullreplicafor.md)                                 | Неверно     | **Top**      |
| [**MS-DS-является-partial-реплика для**](a-msds-ispartialreplicafor.md)                           | Неверно     | **Top**      |
| [**MS-DS-является-PRIMARY-Computer-для**](a-msds-isprimarycomputerfor.md)                         | Неверно     | **Top**      |
| [**MS-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                          | Неверно     | **Top**      |
| [**MS-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                                          | Неверно     | **Top**      |
| [**MS-DS-локально-эффективное удаление — время**](a-msds-localeffectivedeletiontime.md)             | Неверно     | **Top**      |
| [**MS-DS-Local-эффективен — время перезапуска**](a-msds-localeffectiverecycletime.md)               | Неверно     | **Top**      |
| [**MS-DS-Masterd-by**](a-msds-masteredby.md)                                               | Неверно     | **Top**      |
| [**MS-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)                            | Неверно     | **Top**      |
| [**MS-DS-Members-of-Resource-Property-List-BL**](a-msds-membersofresourcepropertylistbl.md) | Неверно     | **Top**      |
| [**MS-DS-NC-REPL-курсоры**](a-msds-ncreplcursors.md)                                        | Неверно     | **Top**      |
| [**MS-DS-NC-REPL-Inbound-соседи**](a-msds-ncreplinboundneighbors.md)                     | Неверно     | **Top**      |
| [**MS-DS-NC-REPL-Outbound-соседи**](a-msds-ncreploutboundneighbors.md)                   | Неверно     | **Top**      |
| [**MS-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)                | Неверно     | **Top**      |
| [**MS-DS-NC-Type**](a-msds-nctype.md)                                                       | Неверно     | **Top**      |
| [**MS-DS-не-Members-BL**](a-msds-nonmembersbl.md)                                          | Неверно     | **Top**      |
| [**MS-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                                | Неверно     | **Top**      |
| [**MS-DS-Оидтограуп-Link-BL**](a-msds-oidtogrouplinkbl.md)                                  | Неверно     | **Top**      |
| [**MS-DS-Operations-для-AZ-Role-BL**](a-msds-operationsforazrolebl.md)                      | Неверно     | **Top**      |
| [**MS-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)                      | Неверно     | **Top**      |
| [**MS-DS-Principal-Name**](a-msds-principalname.md)                                         | Неверно     | **Top**      |
| [**MS-DS-PSO — применяется**](a-msds-psoapplied.md)                                               | Неверно     | **Top**      |
| [**MS-DS-REPL-Attribute-Meta-Data**](a-msds-replattributemetadata.md)                       | Неверно     | **Top**      |
| [**MS-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)                               | Неверно     | **Top**      |
| [**MS-DS-выявил-DSA**](a-msds-revealeddsas.md)                                           | Неверно     | **Top**      |
| [**MS-DS-выводит-List-BL**](a-msds-revealedlistbl.md)                                      | Неверно     | **Top**      |
| [**MS-DS-Tasks-для-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                                | Неверно     | **Top**      |
| [**MS-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                                | Неверно     | **Top**      |
| [**MS-DS-TDO-исходящий трафик — BL**](a-msds-tdoegressbl.md)                                            | Неверно     | **Top**      |
| [**MS-DS-TDO-входящий трафик — BL**](a-msds-tdoingressbl.md)                                          | Неверно     | **Top**      |
| [**MS-DS-value-type-Reference-BL**](a-msds-valuetypereferencebl.md)                         | Неверно     | **Top**      |
| [**MS-дов-Owner-BL**](a-ownerbl.md)                                                        | Неверно     | **Top**      |
| [**Мссфу-30-POSIX-член-of**](a-mssfu30posixmemberof.md)                                   | Неверно     | **Top**      |
| [**нетбут-SCP-BL**](a-netbootscpbl.md)                                                     | Неверно     | **Top**      |
| [**Не-Security-Member-BL**](a-nonsecuritymemberbl.md)                                      | Неверно     | **Top**      |
| [**NT-Security-дескриптор**](a-ntsecuritydescriptor.md)                                     | True      | **Top**      |
| [**Obj-расп-имя**](a-distinguishedname.md)                                                 | Неверно     | **Top**      |
| [**Объект — Категория**](a-objectcategory.md)                                                  | True      | **Top**      |
| [**Объектный класс**](a-objectclass.md)                                                        | True      | **Top**      |
| [**Объект — GUID**](a-objectguid.md)                                                          | Неверно     | **Top**      |
| [**Версия объекта**](a-objectversion.md)                                                    | Неверно     | **Top**      |
| [**Другие хорошо известные объекты**](a-otherwellknownobjects.md)                                  | Неверно     | **Top**      |
| [**Разделяемый атрибут-удаление-список**](a-partialattributedeletionlist.md)                    | Неверно     | **Top**      |
| [**Разделяемый атрибут-set**](a-partialattributeset.md)                                       | Неверно     | **Top**      |
| [**Возможно — подстрочные**](a-possibleinferiors.md)                                            | Неверно     | **Top**      |
| [**Прокси-объект-имя**](a-proxiedobjectname.md)                                           | Неверно     | **Top**      |
| [**Прокси-адреса**](a-proxyaddresses.md)                                                  | Неверно     | **Top**      |
| [**Запрос — политика — BL**](a-querypolicybl.md)                                                   | Неверно     | **Top**      |
| [**RDN**](a-name.md)                                                                        | Неверно     | **Top**      |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                                    | Неверно     | **Top**      |
| [**REPL-Уптодате-Vector**](a-repluptodatevector.md)                                         | Неверно     | **Top**      |
| [**Отчеты**](a-directreports.md)                                                           | Неверно     | **Top**      |
| [**Представители — от**](a-repsfrom.md)                                                              | Неверно     | **Top**      |
| [**Представители — кому**](a-repsto.md)                                                                  | Неверно     | **Top**      |
| [**Редакции**](a-revision.md)                                                               | Неверно     | **Top**      |
| [**SD-Rights-эффективен**](a-sdrightseffective.md)                                           | Неверно     | **Top**      |
| [**Server-Reference-BL**](a-serverreferencebl.md)                                           | Неверно     | **Top**      |
| [**"Показать" — "Расширенный просмотр"**](a-showinadvancedviewonly.md)                               | Неверно     | **Top**      |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                     | Неверно     | **Top**      |
| [**Структурный объектный класс**](a-structuralobjectclass.md)                                   | Неверно     | **Top**      |
| [**Подразделы-ReFS**](a-subrefs.md)                                                                | Неверно     | **Top**      |
| [**субсчемасубентри**](a-subschemasubentry.md)                                             | Неверно     | **Top**      |
| [**Системные флаги**](a-systemflags.md)                                                        | Неверно     | **Top**      |
| [**USN-изменено**](a-usnchanged.md)                                                          | Неверно     | **Top**      |
| [**Созданный USN**](a-usncreated.md)                                                          | Неверно     | **Top**      |
| [**USN-DSA-Last-obj-removed**](a-usndsalastobjremoved.md)                                   | Неверно     | **Top**      |
| [**USN — межсайтовая**](a-usnintersite.md)                                                      | Неверно     | **Top**      |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                                  | Неверно     | **Top**      |
| [**Источник USN**](a-usnsource.md)                                                            | Неверно     | **Top**      |
| [**WBEM — путь**](a-wbempath.md)                                                              | Неверно     | **Top**      |
| [**Хорошо известные объекты**](a-wellknownobjects.md)                                             | Неверно     | **Top**      |
| [**При изменении**](a-whenchanged.md)                                                        | Неверно     | **Top**      |
| [**При создании**](a-whencreated.md)                                                        | Неверно     | **Top**      |
| [**WWW — Главная страница**](a-wwwhomepage.md)                                                       | Неверно     | **Top**      |
| [**WWW-Page — другие**](a-url.md)                                                              | Неверно     | **Top**      |



 

 





