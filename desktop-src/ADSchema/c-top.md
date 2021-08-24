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
ms.openlocfilehash: 248726d9fac9c0d39fae5759df08d4ea10f4f012ba1a1ce0cc2f4dbe55d76a6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119580594"
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
| System-Only                 | Верно                                                                                         |
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



## <a name="windows-2000-server-attributes"></a>атрибуты сервера Windows 2000

этот класс содержит следующие атрибуты для сервера Windows 2000:



| attribute                                                                 | Обязательный | Унаследован от |
|---------------------------------------------------------------------------|-----------|--------------|
| [**Описание администратора**](a-admindescription.md)                           | Нет     | **Top**      |
| [**Имя администратора-отображение**](a-admindisplayname.md)                          | Нет     | **Top**      |
| [**Allowed-Attributes**](a-allowedattributes.md)                         | Нет     | **Top**      |
| [**Allowed-Attributes-эффективен**](a-allowedattributeseffective.md)      | Нет     | **Top**      |
| [**Allowed-Child-classes**](a-allowedchildclasses.md)                    | Нет     | **Top**      |
| [**Allowed-Child-classes-эффективен**](a-allowedchildclasseseffective.md) | Нет     | **Top**      |
| [**Плацдарм-Server-List-BL**](a-bridgeheadserverlistbl.md)             | Нет     | **Top**      |
| [**Каноническое имя**](a-canonicalname.md)                                 | Нет     | **Top**      |
| [**Common-Name**](a-cn.md)                                               | Нет     | **Top**      |
| [**Метка времени создания**](a-createtimestamp.md)                            | Нет     | **Top**      |
| [**Описание**](a-description.md)                                      | Нет     | **Top**      |
| [**Отображаемое имя**](a-displayname.md)                                     | Нет     | **Top**      |
| [**Отображаемое имя — печатаемое**](a-displaynameprintable.md)                  | Нет     | **Top**      |
| [**DSA-Signature**](a-dsasignature.md)                                   | Нет     | **Top**      |
| [**DS-Core-распространение-данные**](a-dscorepropagationdata.md)               | Нет     | **Top**      |
| [**Имя расширения**](a-extensionname.md)                                 | Нет     | **Top**      |
| [**Метки**](a-flags.md)                                                  | Нет     | **Top**      |
| [**Из записи**](a-fromentry.md)                                         | Нет     | **Top**      |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)             | Нет     | **Top**      |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                 | Нет     | **Top**      |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                | Нет     | **Top**      |
| [**Тип экземпляра**](a-instancetype.md)                                   | Верно      | **Top**      |
| [**Является критически важным — системный объект**](a-iscriticalsystemobject.md)             | Нет     | **Top**      |
| [**Удалено**](a-isdeleted.md)                                         | Нет     | **Top**      |
| [**Входит в состав списка рассылки**](a-memberof.md)                                     | Нет     | **Top**      |
| [**Имеет права владельца**](a-isprivilegeholder.md)                        | Нет     | **Top**      |
| [**Последний-известный-родительский**](a-lastknownparent.md)                            | Нет     | **Top**      |
| [**Управляемые объекты**](a-managedobjects.md)                               | Нет     | **Top**      |
| [**В основном**](a-masteredby.md)                                       | Нет     | **Top**      |
| [**Метка времени изменения**](a-modifytimestamp.md)                            | Нет     | **Top**      |
| [**MS-DS-целостность-дочерняя — количество**](a-ms-ds-consistencychildcount.md)    | Нет     | **Top**      |
| [**MS-DS-Consistencу-Guid**](a-ms-ds-consistencyguid.md)                 | Нет     | **Top**      |
| [**нетбут-SCP-BL**](a-netbootscpbl.md)                                  | Нет     | **Top**      |
| [**Не-Security-Member-BL**](a-nonsecuritymemberbl.md)                   | Нет     | **Top**      |
| [**NT-Security-дескриптор**](a-ntsecuritydescriptor.md)                  | Верно      | **Top**      |
| [**Obj-расп-имя**](a-distinguishedname.md)                              | Нет     | **Top**      |
| [**Объект — Категория**](a-objectcategory.md)                               | Верно      | **Top**      |
| [**Объектный класс**](a-objectclass.md)                                     | Верно      | **Top**      |
| [**Объект — GUID**](a-objectguid.md)                                       | Нет     | **Top**      |
| [**Версия объекта**](a-objectversion.md)                                 | Нет     | **Top**      |
| [**Другие хорошо известные объекты**](a-otherwellknownobjects.md)               | Нет     | **Top**      |
| [**Разделяемый атрибут-удаление-список**](a-partialattributedeletionlist.md) | Нет     | **Top**      |
| [**Разделяемый атрибут-set**](a-partialattributeset.md)                    | Нет     | **Top**      |
| [**Возможно — подстрочные**](a-possibleinferiors.md)                         | Нет     | **Top**      |
| [**Прокси-объект-имя**](a-proxiedobjectname.md)                        | Нет     | **Top**      |
| [**Прокси-адреса**](a-proxyaddresses.md)                               | Нет     | **Top**      |
| [**Запрос — политика — BL**](a-querypolicybl.md)                                | Нет     | **Top**      |
| [**RDN**](a-name.md)                                                     | Нет     | **Top**      |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                 | Нет     | **Top**      |
| [**REPL-Уптодате-Vector**](a-repluptodatevector.md)                      | Нет     | **Top**      |
| [**Отчеты**](a-directreports.md)                                        | Нет     | **Top**      |
| [**Представители — от**](a-repsfrom.md)                                           | Нет     | **Top**      |
| [**Представители — кому**](a-repsto.md)                                               | Нет     | **Top**      |
| [**Редакции**](a-revision.md)                                            | Нет     | **Top**      |
| [**SD-Rights-эффективен**](a-sdrightseffective.md)                        | Нет     | **Top**      |
| [**Server-Reference-BL**](a-serverreferencebl.md)                        | Нет     | **Top**      |
| [**"Показать" — "Расширенный просмотр"**](a-showinadvancedviewonly.md)            | Нет     | **Top**      |
| [**Site-Object-BL**](a-siteobjectbl.md)                                  | Нет     | **Top**      |
| [**Подразделы-ReFS**](a-subrefs.md)                                             | Нет     | **Top**      |
| [**субсчемасубентри**](a-subschemasubentry.md)                          | Нет     | **Top**      |
| [**Системные флаги**](a-systemflags.md)                                     | Нет     | **Top**      |
| [**USN-изменено**](a-usnchanged.md)                                       | Нет     | **Top**      |
| [**Созданный USN**](a-usncreated.md)                                       | Нет     | **Top**      |
| [**USN-DSA-Last-obj-removed**](a-usndsalastobjremoved.md)                | Нет     | **Top**      |
| [**USN — межсайтовая**](a-usnintersite.md)                                   | Нет     | **Top**      |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                               | Нет     | **Top**      |
| [**Источник USN**](a-usnsource.md)                                         | Нет     | **Top**      |
| [**WBEM — путь**](a-wbempath.md)                                           | Нет     | **Top**      |
| [**Хорошо известные объекты**](a-wellknownobjects.md)                          | Нет     | **Top**      |
| [**При изменении**](a-whenchanged.md)                                     | Нет     | **Top**      |
| [**При создании**](a-whencreated.md)                                     | Нет     | **Top**      |
| [**WWW — Главная страница**](a-wwwhomepage.md)                                    | Нет     | **Top**      |
| [**WWW-Page — другие**](a-url.md)                                           | Нет     | **Top**      |



## <a name="windows-server-2003"></a>Windows Server 2003

-   [Атрибуты](#windows-server-2003-attributes)



| Ввод | Значение |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Верно                                                                                         |
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



## <a name="windows-server-2003-attributes"></a>Windows Атрибуты сервера 2003

этот класс содержит следующие атрибуты для Windows Server 2003:



| attribute                                                                   | Обязательный | Унаследован от |
|-----------------------------------------------------------------------------|-----------|--------------|
| [**Описание администратора**](a-admindescription.md)                             | Нет     | **Top**      |
| [**Имя администратора-отображение**](a-admindisplayname.md)                            | Нет     | **Top**      |
| [**Allowed-Attributes**](a-allowedattributes.md)                           | Нет     | **Top**      |
| [**Allowed-Attributes-эффективен**](a-allowedattributeseffective.md)        | Нет     | **Top**      |
| [**Allowed-Child-classes**](a-allowedchildclasses.md)                      | Нет     | **Top**      |
| [**Allowed-Child-classes-эффективен**](a-allowedchildclasseseffective.md)   | Нет     | **Top**      |
| [**Плацдарм-Server-List-BL**](a-bridgeheadserverlistbl.md)               | Нет     | **Top**      |
| [**Каноническое имя**](a-canonicalname.md)                                   | Нет     | **Top**      |
| [**Common-Name**](a-cn.md)                                                 | Нет     | **Top**      |
| [**Метка времени создания**](a-createtimestamp.md)                              | Нет     | **Top**      |
| [**Описание**](a-description.md)                                        | Нет     | **Top**      |
| [**Отображаемое имя**](a-displayname.md)                                       | Нет     | **Top**      |
| [**Отображаемое имя — печатаемое**](a-displaynameprintable.md)                    | Нет     | **Top**      |
| [**DSA-Signature**](a-dsasignature.md)                                     | Нет     | **Top**      |
| [**DS-Core-распространение-данные**](a-dscorepropagationdata.md)                 | Нет     | **Top**      |
| [**Имя расширения**](a-extensionname.md)                                   | Нет     | **Top**      |
| [**Метки**](a-flags.md)                                                    | Нет     | **Top**      |
| [**Из записи**](a-fromentry.md)                                           | Нет     | **Top**      |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | Нет     | **Top**      |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | Нет     | **Top**      |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | Нет     | **Top**      |
| [**Тип экземпляра**](a-instancetype.md)                                     | Верно      | **Top**      |
| [**Является критически важным — системный объект**](a-iscriticalsystemobject.md)               | Нет     | **Top**      |
| [**Удалено**](a-isdeleted.md)                                           | Нет     | **Top**      |
| [**Входит в состав списка рассылки**](a-memberof.md)                                       | Нет     | **Top**      |
| [**Имеет права владельца**](a-isprivilegeholder.md)                          | Нет     | **Top**      |
| [**Последний-известный-родительский**](a-lastknownparent.md)                              | Нет     | **Top**      |
| [**Управляемые объекты**](a-managedobjects.md)                                 | Нет     | **Top**      |
| [**В основном**](a-masteredby.md)                                         | Нет     | **Top**      |
| [**Метка времени изменения**](a-modifytimestamp.md)                              | Нет     | **Top**      |
| [**MS-COM-Партитионсетлинк**](a-mscom-partitionsetlink.md)                 | Нет     | **Top**      |
| [**MS-COM-Усерлинк**](a-mscom-userlink.md)                                 | Нет     | **Top**      |
| [**MS-DS-примерно-Иммед-подчиненные**](a-msds-approx-immed-subordinates.md) | Нет     | **Top**      |
| [**MS-DS-целостность-дочерняя — количество**](a-ms-ds-consistencychildcount.md)      | Нет     | **Top**      |
| [**MS-DS-Consistencу-Guid**](a-ms-ds-consistencyguid.md)                   | Нет     | **Top**      |
| [**MS-DS-Masterd-by**](a-msds-masteredby.md)                              | Нет     | **Top**      |
| [**MS-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)           | Нет     | **Top**      |
| [**MS-DS-NC-REPL-курсоры**](a-msds-ncreplcursors.md)                       | Нет     | **Top**      |
| [**MS-DS-NC-REPL-Inbound-соседи**](a-msds-ncreplinboundneighbors.md)    | Нет     | **Top**      |
| [**MS-DS-NC-REPL-Outbound-соседи**](a-msds-ncreploutboundneighbors.md)  | Нет     | **Top**      |
| [**MS-DS-не-Members-BL**](a-msds-nonmembersbl.md)                         | Нет     | **Top**      |
| [**MS-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | Нет     | **Top**      |
| [**MS-DS-Operations-для-AZ-Role-BL**](a-msds-operationsforazrolebl.md)     | Нет     | **Top**      |
| [**MS-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)     | Нет     | **Top**      |
| [**MS-DS-REPL-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | Нет     | **Top**      |
| [**MS-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)              | Нет     | **Top**      |
| [**MS-DS-Tasks-для-AZ-Role-BL**](a-msds-tasksforazrolebl.md)               | Нет     | **Top**      |
| [**MS-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)               | Нет     | **Top**      |
| [**MS-дов-Owner-BL**](a-ownerbl.md)                                       | Нет     | **Top**      |
| [**нетбут-SCP-BL**](a-netbootscpbl.md)                                    | Нет     | **Top**      |
| [**Не-Security-Member-BL**](a-nonsecuritymemberbl.md)                     | Нет     | **Top**      |
| [**NT-Security-дескриптор**](a-ntsecuritydescriptor.md)                    | Верно      | **Top**      |
| [**Obj-расп-имя**](a-distinguishedname.md)                                | Нет     | **Top**      |
| [**Объект — Категория**](a-objectcategory.md)                                 | Верно      | **Top**      |
| [**Объектный класс**](a-objectclass.md)                                       | Верно      | **Top**      |
| [**Объект — GUID**](a-objectguid.md)                                         | Нет     | **Top**      |
| [**Версия объекта**](a-objectversion.md)                                   | Нет     | **Top**      |
| [**Другие хорошо известные объекты**](a-otherwellknownobjects.md)                 | Нет     | **Top**      |
| [**Разделяемый атрибут-удаление-список**](a-partialattributedeletionlist.md)   | Нет     | **Top**      |
| [**Разделяемый атрибут-set**](a-partialattributeset.md)                      | Нет     | **Top**      |
| [**Возможно — подстрочные**](a-possibleinferiors.md)                           | Нет     | **Top**      |
| [**Прокси-объект-имя**](a-proxiedobjectname.md)                          | Нет     | **Top**      |
| [**Прокси-адреса**](a-proxyaddresses.md)                                 | Нет     | **Top**      |
| [**Запрос — политика — BL**](a-querypolicybl.md)                                  | Нет     | **Top**      |
| [**RDN**](a-name.md)                                                       | Нет     | **Top**      |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                   | Нет     | **Top**      |
| [**REPL-Уптодате-Vector**](a-repluptodatevector.md)                        | Нет     | **Top**      |
| [**Отчеты**](a-directreports.md)                                          | Нет     | **Top**      |
| [**Представители — от**](a-repsfrom.md)                                             | Нет     | **Top**      |
| [**Представители — кому**](a-repsto.md)                                                 | Нет     | **Top**      |
| [**Редакции**](a-revision.md)                                              | Нет     | **Top**      |
| [**SD-Rights-эффективен**](a-sdrightseffective.md)                          | Нет     | **Top**      |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | Нет     | **Top**      |
| [**"Показать" — "Расширенный просмотр"**](a-showinadvancedviewonly.md)              | Нет     | **Top**      |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Нет     | **Top**      |
| [**Структурный объектный класс**](a-structuralobjectclass.md)                  | Нет     | **Top**      |
| [**Подразделы-ReFS**](a-subrefs.md)                                               | Нет     | **Top**      |
| [**субсчемасубентри**](a-subschemasubentry.md)                            | Нет     | **Top**      |
| [**Системные флаги**](a-systemflags.md)                                       | Нет     | **Top**      |
| [**USN-изменено**](a-usnchanged.md)                                         | Нет     | **Top**      |
| [**Созданный USN**](a-usncreated.md)                                         | Нет     | **Top**      |
| [**USN-DSA-Last-obj-removed**](a-usndsalastobjremoved.md)                  | Нет     | **Top**      |
| [**USN — межсайтовая**](a-usnintersite.md)                                     | Нет     | **Top**      |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                 | Нет     | **Top**      |
| [**Источник USN**](a-usnsource.md)                                           | Нет     | **Top**      |
| [**WBEM — путь**](a-wbempath.md)                                             | Нет     | **Top**      |
| [**Хорошо известные объекты**](a-wellknownobjects.md)                            | Нет     | **Top**      |
| [**При изменении**](a-whenchanged.md)                                       | Нет     | **Top**      |
| [**При создании**](a-whencreated.md)                                       | Нет     | **Top**      |
| [**WWW — Главная страница**](a-wwwhomepage.md)                                      | Нет     | **Top**      |
| [**WWW-Page — другие**](a-url.md)                                             | Нет     | **Top**      |



## <a name="adam"></a>ADAM

-   [Атрибуты](#adam-attributes)



| Ввод | Значение |
|-----------------------------|------------------------------------------|
| System-Only                 | Верно                                     |
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
| [**Описание администратора**](a-admindescription.md)                             | Нет     | **Top**      |
| [**Имя администратора-отображение**](a-admindisplayname.md)                            | Нет     | **Top**      |
| [**Allowed-Attributes**](a-allowedattributes.md)                           | Нет     | **Top**      |
| [**Allowed-Attributes-эффективен**](a-allowedattributeseffective.md)        | Нет     | **Top**      |
| [**Allowed-Child-classes**](a-allowedchildclasses.md)                      | Нет     | **Top**      |
| [**Allowed-Child-classes-эффективен**](a-allowedchildclasseseffective.md)   | Нет     | **Top**      |
| [**Плацдарм-Server-List-BL**](a-bridgeheadserverlistbl.md)               | Нет     | **Top**      |
| [**Каноническое имя**](a-canonicalname.md)                                   | Нет     | **Top**      |
| [**Common-Name**](a-cn.md)                                                 | Нет     | **Top**      |
| [**Метка времени создания**](a-createtimestamp.md)                              | Нет     | **Top**      |
| [**Описание**](a-description.md)                                        | Нет     | **Top**      |
| [**Отображаемое имя**](a-displayname.md)                                       | Нет     | **Top**      |
| [**DSA-Signature**](a-dsasignature.md)                                     | Нет     | **Top**      |
| [**DS-Core-распространение-данные**](a-dscorepropagationdata.md)                 | Нет     | **Top**      |
| [**Из записи**](a-fromentry.md)                                           | Нет     | **Top**      |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | Нет     | **Top**      |
| [**Тип экземпляра**](a-instancetype.md)                                     | Верно      | **Top**      |
| [**Является критически важным — системный объект**](a-iscriticalsystemobject.md)               | Нет     | **Top**      |
| [**Удалено**](a-isdeleted.md)                                           | Нет     | **Top**      |
| [**Входит в состав списка рассылки**](a-memberof.md)                                       | Нет     | **Top**      |
| [**Последний-известный-родительский**](a-lastknownparent.md)                              | Нет     | **Top**      |
| [**Управляемые объекты**](a-managedobjects.md)                                 | Нет     | **Top**      |
| [**В основном**](a-masteredby.md)                                         | Нет     | **Top**      |
| [**Метка времени изменения**](a-modifytimestamp.md)                              | Нет     | **Top**      |
| [**MS-DS-примерно-Иммед-подчиненные**](a-msds-approx-immed-subordinates.md) | Нет     | **Top**      |
| [**MS-DS-целостность-дочерняя — количество**](a-ms-ds-consistencychildcount.md)      | Нет     | **Top**      |
| [**MS-DS-Consistencу-Guid**](a-ms-ds-consistencyguid.md)                   | Нет     | **Top**      |
| [**MS-DS-Disabled-for-Instances-BL**](a-msds-disableforinstancesbl.md)      | Нет     | **Top**      |
| [**MS-DS-Masterd-by**](a-msds-masteredby.md)                              | Нет     | **Top**      |
| [**MS-DS-NC-REPL-курсоры**](a-msds-ncreplcursors.md)                       | Нет     | **Top**      |
| [**MS-DS-NC-REPL-Inbound-соседи**](a-msds-ncreplinboundneighbors.md)    | Нет     | **Top**      |
| [**MS-DS-NC-REPL-Outbound-соседи**](a-msds-ncreploutboundneighbors.md)  | Нет     | **Top**      |
| [**MS-DS-REPL-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | Нет     | **Top**      |
| [**MS-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)              | Нет     | **Top**      |
| [**MS-DS-Service-Account-BL**](a-msds-serviceaccountbl.md)                 | Нет     | **Top**      |
| [**NT-Security-дескриптор**](a-ntsecuritydescriptor.md)                    | Верно      | **Top**      |
| [**Obj-расп-имя**](a-distinguishedname.md)                                | Нет     | **Top**      |
| [**Объект — Категория**](a-objectcategory.md)                                 | Верно      | **Top**      |
| [**Объектный класс**](a-objectclass.md)                                       | Верно      | **Top**      |
| [**Объект — GUID**](a-objectguid.md)                                         | Нет     | **Top**      |
| [**Версия объекта**](a-objectversion.md)                                   | Нет     | **Top**      |
| [**Другие хорошо известные объекты**](a-otherwellknownobjects.md)                 | Нет     | **Top**      |
| [**Разделяемый атрибут-удаление-список**](a-partialattributedeletionlist.md)   | Нет     | **Top**      |
| [**Разделяемый атрибут-set**](a-partialattributeset.md)                      | Нет     | **Top**      |
| [**Возможно — подстрочные**](a-possibleinferiors.md)                           | Нет     | **Top**      |
| [**Прокси-объект-имя**](a-proxiedobjectname.md)                          | Нет     | **Top**      |
| [**Прокси-адреса**](a-proxyaddresses.md)                                 | Нет     | **Top**      |
| [**Запрос — политика — BL**](a-querypolicybl.md)                                  | Нет     | **Top**      |
| [**RDN**](a-name.md)                                                       | Нет     | **Top**      |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                   | Нет     | **Top**      |
| [**REPL-Уптодате-Vector**](a-repluptodatevector.md)                        | Нет     | **Top**      |
| [**Представители — от**](a-repsfrom.md)                                             | Нет     | **Top**      |
| [**Представители — кому**](a-repsto.md)                                                 | Нет     | **Top**      |
| [**Редакции**](a-revision.md)                                              | Нет     | **Top**      |
| [**SD-Rights-эффективен**](a-sdrightseffective.md)                          | Нет     | **Top**      |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | Нет     | **Top**      |
| [**"Показать" — "Расширенный просмотр"**](a-showinadvancedviewonly.md)              | Нет     | **Top**      |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Нет     | **Top**      |
| [**Структурный объектный класс**](a-structuralobjectclass.md)                  | Нет     | **Top**      |
| [**Подразделы-ReFS**](a-subrefs.md)                                               | Нет     | **Top**      |
| [**субсчемасубентри**](a-subschemasubentry.md)                            | Нет     | **Top**      |
| [**Системные флаги**](a-systemflags.md)                                       | Нет     | **Top**      |
| [**USN-изменено**](a-usnchanged.md)                                         | Нет     | **Top**      |
| [**Созданный USN**](a-usncreated.md)                                         | Нет     | **Top**      |
| [**USN-DSA-Last-obj-removed**](a-usndsalastobjremoved.md)                  | Нет     | **Top**      |
| [**USN — межсайтовая**](a-usnintersite.md)                                     | Нет     | **Top**      |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                 | Нет     | **Top**      |
| [**Источник USN**](a-usnsource.md)                                           | Нет     | **Top**      |
| [**WBEM — путь**](a-wbempath.md)                                             | Нет     | **Top**      |
| [**Хорошо известные объекты**](a-wellknownobjects.md)                            | Нет     | **Top**      |
| [**При изменении**](a-whenchanged.md)                                       | Нет     | **Top**      |
| [**При создании**](a-whencreated.md)                                       | Нет     | **Top**      |
| [**WWW — Главная страница**](a-wwwhomepage.md)                                      | Нет     | **Top**      |
| [**WWW-Page — другие**](a-url.md)                                             | Нет     | **Top**      |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2

-   [Атрибуты](#windows-server-2003-r2-attributes)



| Ввод | Значение |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Верно                                                                                         |
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



## <a name="windows-server-2003-r2-attributes"></a>Windows Атрибуты сервера 2003 R2

этот класс содержит следующие атрибуты для Windows Server 2003 R2:



| attribute                                                                   | Обязательный | Унаследован от |
|-----------------------------------------------------------------------------|-----------|--------------|
| [**Описание администратора**](a-admindescription.md)                             | Нет     | **Top**      |
| [**Имя администратора-отображение**](a-admindisplayname.md)                            | Нет     | **Top**      |
| [**Allowed-Attributes**](a-allowedattributes.md)                           | Нет     | **Top**      |
| [**Allowed-Attributes-эффективен**](a-allowedattributeseffective.md)        | Нет     | **Top**      |
| [**Allowed-Child-classes**](a-allowedchildclasses.md)                      | Нет     | **Top**      |
| [**Allowed-Child-classes-эффективен**](a-allowedchildclasseseffective.md)   | Нет     | **Top**      |
| [**Плацдарм-Server-List-BL**](a-bridgeheadserverlistbl.md)               | Нет     | **Top**      |
| [**Каноническое имя**](a-canonicalname.md)                                   | Нет     | **Top**      |
| [**Common-Name**](a-cn.md)                                                 | Нет     | **Top**      |
| [**Метка времени создания**](a-createtimestamp.md)                              | Нет     | **Top**      |
| [**Описание**](a-description.md)                                        | Нет     | **Top**      |
| [**Отображаемое имя**](a-displayname.md)                                       | Нет     | **Top**      |
| [**Отображаемое имя — печатаемое**](a-displaynameprintable.md)                    | Нет     | **Top**      |
| [**DSA-Signature**](a-dsasignature.md)                                     | Нет     | **Top**      |
| [**DS-Core-распространение-данные**](a-dscorepropagationdata.md)                 | Нет     | **Top**      |
| [**Имя расширения**](a-extensionname.md)                                   | Нет     | **Top**      |
| [**Метки**](a-flags.md)                                                    | Нет     | **Top**      |
| [**Из записи**](a-fromentry.md)                                           | Нет     | **Top**      |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | Нет     | **Top**      |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | Нет     | **Top**      |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | Нет     | **Top**      |
| [**Тип экземпляра**](a-instancetype.md)                                     | Верно      | **Top**      |
| [**Является критически важным — системный объект**](a-iscriticalsystemobject.md)               | Нет     | **Top**      |
| [**Удалено**](a-isdeleted.md)                                           | Нет     | **Top**      |
| [**Входит в состав списка рассылки**](a-memberof.md)                                       | Нет     | **Top**      |
| [**Имеет права владельца**](a-isprivilegeholder.md)                          | Нет     | **Top**      |
| [**Последний-известный-родительский**](a-lastknownparent.md)                              | Нет     | **Top**      |
| [**Управляемые объекты**](a-managedobjects.md)                                 | Нет     | **Top**      |
| [**В основном**](a-masteredby.md)                                         | Нет     | **Top**      |
| [**Метка времени изменения**](a-modifytimestamp.md)                              | Нет     | **Top**      |
| [**MS-COM-Партитионсетлинк**](a-mscom-partitionsetlink.md)                 | Нет     | **Top**      |
| [**MS-COM-Усерлинк**](a-mscom-userlink.md)                                 | Нет     | **Top**      |
| [**MS-DFSR-Компутерреференцебл**](a-msdfsr-computerreferencebl.md)         | Нет     | **Top**      |
| [**MS-DFSR-Мемберреференцебл**](a-msdfsr-memberreferencebl.md)             | Нет     | **Top**      |
| [**MS-DS-примерно-Иммед-подчиненные**](a-msds-approx-immed-subordinates.md) | Нет     | **Top**      |
| [**MS-DS-целостность-дочерняя — количество**](a-ms-ds-consistencychildcount.md)      | Нет     | **Top**      |
| [**MS-DS-Consistencу-Guid**](a-ms-ds-consistencyguid.md)                   | Нет     | **Top**      |
| [**MS-DS-Masterd-by**](a-msds-masteredby.md)                              | Нет     | **Top**      |
| [**MS-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)           | Нет     | **Top**      |
| [**MS-DS-NC-REPL-курсоры**](a-msds-ncreplcursors.md)                       | Нет     | **Top**      |
| [**MS-DS-NC-REPL-Inbound-соседи**](a-msds-ncreplinboundneighbors.md)    | Нет     | **Top**      |
| [**MS-DS-NC-REPL-Outbound-соседи**](a-msds-ncreploutboundneighbors.md)  | Нет     | **Top**      |
| [**MS-DS-не-Members-BL**](a-msds-nonmembersbl.md)                         | Нет     | **Top**      |
| [**MS-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | Нет     | **Top**      |
| [**MS-DS-Operations-для-AZ-Role-BL**](a-msds-operationsforazrolebl.md)     | Нет     | **Top**      |
| [**MS-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)     | Нет     | **Top**      |
| [**MS-DS-REPL-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | Нет     | **Top**      |
| [**MS-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)              | Нет     | **Top**      |
| [**MS-DS-Tasks-для-AZ-Role-BL**](a-msds-tasksforazrolebl.md)               | Нет     | **Top**      |
| [**MS-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)               | Нет     | **Top**      |
| [**MS-дов-Owner-BL**](a-ownerbl.md)                                       | Нет     | **Top**      |
| [**Мссфу-30-POSIX-член-of**](a-mssfu30posixmemberof.md)                  | Нет     | **Top**      |
| [**нетбут-SCP-BL**](a-netbootscpbl.md)                                    | Нет     | **Top**      |
| [**Не-Security-Member-BL**](a-nonsecuritymemberbl.md)                     | Нет     | **Top**      |
| [**NT-Security-дескриптор**](a-ntsecuritydescriptor.md)                    | Верно      | **Top**      |
| [**Obj-расп-имя**](a-distinguishedname.md)                                | Нет     | **Top**      |
| [**Объект — Категория**](a-objectcategory.md)                                 | Верно      | **Top**      |
| [**Объектный класс**](a-objectclass.md)                                       | Верно      | **Top**      |
| [**Объект — GUID**](a-objectguid.md)                                         | Нет     | **Top**      |
| [**Версия объекта**](a-objectversion.md)                                   | Нет     | **Top**      |
| [**Другие хорошо известные объекты**](a-otherwellknownobjects.md)                 | Нет     | **Top**      |
| [**Разделяемый атрибут-удаление-список**](a-partialattributedeletionlist.md)   | Нет     | **Top**      |
| [**Разделяемый атрибут-set**](a-partialattributeset.md)                      | Нет     | **Top**      |
| [**Возможно — подстрочные**](a-possibleinferiors.md)                           | Нет     | **Top**      |
| [**Прокси-объект-имя**](a-proxiedobjectname.md)                          | Нет     | **Top**      |
| [**Прокси-адреса**](a-proxyaddresses.md)                                 | Нет     | **Top**      |
| [**Запрос — политика — BL**](a-querypolicybl.md)                                  | Нет     | **Top**      |
| [**RDN**](a-name.md)                                                       | Нет     | **Top**      |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                   | Нет     | **Top**      |
| [**REPL-Уптодате-Vector**](a-repluptodatevector.md)                        | Нет     | **Top**      |
| [**Отчеты**](a-directreports.md)                                          | Нет     | **Top**      |
| [**Представители — от**](a-repsfrom.md)                                             | Нет     | **Top**      |
| [**Представители — кому**](a-repsto.md)                                                 | Нет     | **Top**      |
| [**Редакции**](a-revision.md)                                              | Нет     | **Top**      |
| [**SD-Rights-эффективен**](a-sdrightseffective.md)                          | Нет     | **Top**      |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | Нет     | **Top**      |
| [**"Показать" — "Расширенный просмотр"**](a-showinadvancedviewonly.md)              | Нет     | **Top**      |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Нет     | **Top**      |
| [**Структурный объектный класс**](a-structuralobjectclass.md)                  | Нет     | **Top**      |
| [**Подразделы-ReFS**](a-subrefs.md)                                               | Нет     | **Top**      |
| [**субсчемасубентри**](a-subschemasubentry.md)                            | Нет     | **Top**      |
| [**Системные флаги**](a-systemflags.md)                                       | Нет     | **Top**      |
| [**USN-изменено**](a-usnchanged.md)                                         | Нет     | **Top**      |
| [**Созданный USN**](a-usncreated.md)                                         | Нет     | **Top**      |
| [**USN-DSA-Last-obj-removed**](a-usndsalastobjremoved.md)                  | Нет     | **Top**      |
| [**USN — межсайтовая**](a-usnintersite.md)                                     | Нет     | **Top**      |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                 | Нет     | **Top**      |
| [**Источник USN**](a-usnsource.md)                                           | Нет     | **Top**      |
| [**WBEM — путь**](a-wbempath.md)                                             | Нет     | **Top**      |
| [**Хорошо известные объекты**](a-wellknownobjects.md)                            | Нет     | **Top**      |
| [**При изменении**](a-whenchanged.md)                                       | Нет     | **Top**      |
| [**При создании**](a-whencreated.md)                                       | Нет     | **Top**      |
| [**WWW — Главная страница**](a-wwwhomepage.md)                                      | Нет     | **Top**      |
| [**WWW-Page — другие**](a-url.md)                                             | Нет     | **Top**      |



## <a name="windows-server-2008"></a>Windows Server 2008

-   [Атрибуты](#windows-server-2008-attributes)



| Ввод | Значение |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Верно                                                                                         |
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



## <a name="windows-server-2008-attributes"></a>Windows Атрибуты сервера 2008

этот класс содержит следующие атрибуты для Windows Server 2008:



| attribute                                                                      | Обязательный | Унаследован от |
|--------------------------------------------------------------------------------|-----------|--------------|
| [**Описание администратора**](a-admindescription.md)                                | Нет     | **Top**      |
| [**Имя администратора-отображение**](a-admindisplayname.md)                               | Нет     | **Top**      |
| [**Allowed-Attributes**](a-allowedattributes.md)                              | Нет     | **Top**      |
| [**Allowed-Attributes-эффективен**](a-allowedattributeseffective.md)           | Нет     | **Top**      |
| [**Allowed-Child-classes**](a-allowedchildclasses.md)                         | Нет     | **Top**      |
| [**Allowed-Child-classes-эффективен**](a-allowedchildclasseseffective.md)      | Нет     | **Top**      |
| [**Плацдарм-Server-List-BL**](a-bridgeheadserverlistbl.md)                  | Нет     | **Top**      |
| [**Каноническое имя**](a-canonicalname.md)                                      | Нет     | **Top**      |
| [**Common-Name**](a-cn.md)                                                    | Нет     | **Top**      |
| [**Метка времени создания**](a-createtimestamp.md)                                 | Нет     | **Top**      |
| [**Описание**](a-description.md)                                           | Нет     | **Top**      |
| [**Отображаемое имя**](a-displayname.md)                                          | Нет     | **Top**      |
| [**Отображаемое имя — печатаемое**](a-displaynameprintable.md)                       | Нет     | **Top**      |
| [**DSA-Signature**](a-dsasignature.md)                                        | Нет     | **Top**      |
| [**DS-Core-распространение-данные**](a-dscorepropagationdata.md)                    | Нет     | **Top**      |
| [**Имя расширения**](a-extensionname.md)                                      | Нет     | **Top**      |
| [**Метки**](a-flags.md)                                                       | Нет     | **Top**      |
| [**Из записи**](a-fromentry.md)                                              | Нет     | **Top**      |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                  | Нет     | **Top**      |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                      | Нет     | **Top**      |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                     | Нет     | **Top**      |
| [**Тип экземпляра**](a-instancetype.md)                                        | Верно      | **Top**      |
| [**Является критически важным — системный объект**](a-iscriticalsystemobject.md)                  | Нет     | **Top**      |
| [**Удалено**](a-isdeleted.md)                                              | Нет     | **Top**      |
| [**Входит в состав списка рассылки**](a-memberof.md)                                          | Нет     | **Top**      |
| [**Имеет права владельца**](a-isprivilegeholder.md)                             | Нет     | **Top**      |
| [**Последний-известный-родительский**](a-lastknownparent.md)                                 | Нет     | **Top**      |
| [**Управляемые объекты**](a-managedobjects.md)                                    | Нет     | **Top**      |
| [**В основном**](a-masteredby.md)                                            | Нет     | **Top**      |
| [**Метка времени изменения**](a-modifytimestamp.md)                                 | Нет     | **Top**      |
| [**MS-COM-Партитионсетлинк**](a-mscom-partitionsetlink.md)                    | Нет     | **Top**      |
| [**MS-COM-Усерлинк**](a-mscom-userlink.md)                                    | Нет     | **Top**      |
| [**MS-DFSR-Компутерреференцебл**](a-msdfsr-computerreferencebl.md)            | Нет     | **Top**      |
| [**MS-DFSR-Мемберреференцебл**](a-msdfsr-memberreferencebl.md)                | Нет     | **Top**      |
| [**MS-DS-примерно-Иммед-подчиненные**](a-msds-approx-immed-subordinates.md)    | Нет     | **Top**      |
| [**MS-DS-Аусентикатедто-Аккаунтлист**](a-msds-authenticatedtoaccountlist.md) | Нет     | **Top**      |
| [**MS-DS-целостность-дочерняя — количество**](a-ms-ds-consistencychildcount.md)         | Нет     | **Top**      |
| [**MS-DS-Consistencу-Guid**](a-ms-ds-consistencyguid.md)                      | Нет     | **Top**      |
| [**MS-DS--домен — для**](a-msds-isdomainfor.md)                              | Нет     | **Top**      |
| [**MS-DS-является-Full-реплика для**](a-msds-isfullreplicafor.md)                   | Нет     | **Top**      |
| [**MS-DS-является-partial-реплика для**](a-msds-ispartialreplicafor.md)             | Нет     | **Top**      |
| [**MS-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                            | Нет     | **Top**      |
| [**MS-DS-Masterd-by**](a-msds-masteredby.md)                                 | Нет     | **Top**      |
| [**MS-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)              | Нет     | **Top**      |
| [**MS-DS-NC-REPL-курсоры**](a-msds-ncreplcursors.md)                          | Нет     | **Top**      |
| [**MS-DS-NC-REPL-Inbound-соседи**](a-msds-ncreplinboundneighbors.md)       | Нет     | **Top**      |
| [**MS-DS-NC-REPL-Outbound-соседи**](a-msds-ncreploutboundneighbors.md)     | Нет     | **Top**      |
| [**MS-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)  | Нет     | **Top**      |
| [**MS-DS-NC-Type**](a-msds-nctype.md)                                         | Нет     | **Top**      |
| [**MS-DS-не-Members-BL**](a-msds-nonmembersbl.md)                            | Нет     | **Top**      |
| [**MS-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                  | Нет     | **Top**      |
| [**MS-DS-Operations-для-AZ-Role-BL**](a-msds-operationsforazrolebl.md)        | Нет     | **Top**      |
| [**MS-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)        | Нет     | **Top**      |
| [**MS-DS-Principal-Name**](a-msds-principalname.md)                           | Нет     | **Top**      |
| [**MS-DS-PSO — применяется**](a-msds-psoapplied.md)                                 | Нет     | **Top**      |
| [**MS-DS-REPL-Attribute-Meta-Data**](a-msds-replattributemetadata.md)         | Нет     | **Top**      |
| [**MS-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)                 | Нет     | **Top**      |
| [**MS-DS-выявил-DSA**](a-msds-revealeddsas.md)                             | Нет     | **Top**      |
| [**MS-DS-выводит-List-BL**](a-msds-revealedlistbl.md)                        | Нет     | **Top**      |
| [**MS-DS-Tasks-для-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                  | Нет     | **Top**      |
| [**MS-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                  | Нет     | **Top**      |
| [**MS-дов-Owner-BL**](a-ownerbl.md)                                          | Нет     | **Top**      |
| [**Мссфу-30-POSIX-член-of**](a-mssfu30posixmemberof.md)                     | Нет     | **Top**      |
| [**нетбут-SCP-BL**](a-netbootscpbl.md)                                       | Нет     | **Top**      |
| [**Не-Security-Member-BL**](a-nonsecuritymemberbl.md)                        | Нет     | **Top**      |
| [**NT-Security-дескриптор**](a-ntsecuritydescriptor.md)                       | Верно      | **Top**      |
| [**Obj-расп-имя**](a-distinguishedname.md)                                   | Нет     | **Top**      |
| [**Объект — Категория**](a-objectcategory.md)                                    | Верно      | **Top**      |
| [**Объектный класс**](a-objectclass.md)                                          | Верно      | **Top**      |
| [**Объект — GUID**](a-objectguid.md)                                            | Нет     | **Top**      |
| [**Версия объекта**](a-objectversion.md)                                      | Нет     | **Top**      |
| [**Другие хорошо известные объекты**](a-otherwellknownobjects.md)                    | Нет     | **Top**      |
| [**Разделяемый атрибут-удаление-список**](a-partialattributedeletionlist.md)      | Нет     | **Top**      |
| [**Разделяемый атрибут-set**](a-partialattributeset.md)                         | Нет     | **Top**      |
| [**Возможно — подстрочные**](a-possibleinferiors.md)                              | Нет     | **Top**      |
| [**Прокси-объект-имя**](a-proxiedobjectname.md)                             | Нет     | **Top**      |
| [**Прокси-адреса**](a-proxyaddresses.md)                                    | Нет     | **Top**      |
| [**Запрос — политика — BL**](a-querypolicybl.md)                                     | Нет     | **Top**      |
| [**RDN**](a-name.md)                                                          | Нет     | **Top**      |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                      | Нет     | **Top**      |
| [**REPL-Уптодате-Vector**](a-repluptodatevector.md)                           | Нет     | **Top**      |
| [**Отчеты**](a-directreports.md)                                             | Нет     | **Top**      |
| [**Представители — от**](a-repsfrom.md)                                                | Нет     | **Top**      |
| [**Представители — кому**](a-repsto.md)                                                    | Нет     | **Top**      |
| [**Редакции**](a-revision.md)                                                 | Нет     | **Top**      |
| [**SD-Rights-эффективен**](a-sdrightseffective.md)                             | Нет     | **Top**      |
| [**Server-Reference-BL**](a-serverreferencebl.md)                             | Нет     | **Top**      |
| [**"Показать" — "Расширенный просмотр"**](a-showinadvancedviewonly.md)                 | Нет     | **Top**      |
| [**Site-Object-BL**](a-siteobjectbl.md)                                       | Нет     | **Top**      |
| [**Структурный объектный класс**](a-structuralobjectclass.md)                     | Нет     | **Top**      |
| [**Подразделы-ReFS**](a-subrefs.md)                                                  | Нет     | **Top**      |
| [**субсчемасубентри**](a-subschemasubentry.md)                               | Нет     | **Top**      |
| [**Системные флаги**](a-systemflags.md)                                          | Нет     | **Top**      |
| [**USN-изменено**](a-usnchanged.md)                                            | Нет     | **Top**      |
| [**Созданный USN**](a-usncreated.md)                                            | Нет     | **Top**      |
| [**USN-DSA-Last-obj-removed**](a-usndsalastobjremoved.md)                     | Нет     | **Top**      |
| [**USN — межсайтовая**](a-usnintersite.md)                                        | Нет     | **Top**      |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                    | Нет     | **Top**      |
| [**Источник USN**](a-usnsource.md)                                              | Нет     | **Top**      |
| [**WBEM — путь**](a-wbempath.md)                                                | Нет     | **Top**      |
| [**Хорошо известные объекты**](a-wellknownobjects.md)                               | Нет     | **Top**      |
| [**При изменении**](a-whenchanged.md)                                          | Нет     | **Top**      |
| [**При создании**](a-whencreated.md)                                          | Нет     | **Top**      |
| [**WWW — Главная страница**](a-wwwhomepage.md)                                         | Нет     | **Top**      |
| [**WWW-Page — другие**](a-url.md)                                                | Нет     | **Top**      |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2

-   [Атрибуты](#windows-server-2008-r2-attributes)



| Ввод | Значение |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Верно                                                                                         |
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



## <a name="windows-server-2008-r2-attributes"></a>Windows Атрибуты сервера 2008 R2

этот класс содержит следующие атрибуты для Windows Server 2008 R2:



| attribute                                                                        | Обязательный | Унаследован от |
|----------------------------------------------------------------------------------|-----------|--------------|
| [**Описание администратора**](a-admindescription.md)                                  | Нет     | **Top**      |
| [**Имя администратора-отображение**](a-admindisplayname.md)                                 | Нет     | **Top**      |
| [**Allowed-Attributes**](a-allowedattributes.md)                                | Нет     | **Top**      |
| [**Allowed-Attributes-эффективен**](a-allowedattributeseffective.md)             | Нет     | **Top**      |
| [**Allowed-Child-classes**](a-allowedchildclasses.md)                           | Нет     | **Top**      |
| [**Allowed-Child-classes-эффективен**](a-allowedchildclasseseffective.md)        | Нет     | **Top**      |
| [**Плацдарм-Server-List-BL**](a-bridgeheadserverlistbl.md)                    | Нет     | **Top**      |
| [**Каноническое имя**](a-canonicalname.md)                                        | Нет     | **Top**      |
| [**Common-Name**](a-cn.md)                                                      | Нет     | **Top**      |
| [**Метка времени создания**](a-createtimestamp.md)                                   | Нет     | **Top**      |
| [**Описание**](a-description.md)                                             | Нет     | **Top**      |
| [**Отображаемое имя**](a-displayname.md)                                            | Нет     | **Top**      |
| [**Отображаемое имя — печатаемое**](a-displaynameprintable.md)                         | Нет     | **Top**      |
| [**DSA-Signature**](a-dsasignature.md)                                          | Нет     | **Top**      |
| [**DS-Core-распространение-данные**](a-dscorepropagationdata.md)                      | Нет     | **Top**      |
| [**Имя расширения**](a-extensionname.md)                                        | Нет     | **Top**      |
| [**Метки**](a-flags.md)                                                         | Нет     | **Top**      |
| [**Из записи**](a-fromentry.md)                                                | Нет     | **Top**      |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                    | Нет     | **Top**      |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                        | Нет     | **Top**      |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                       | Нет     | **Top**      |
| [**Тип экземпляра**](a-instancetype.md)                                          | Верно      | **Top**      |
| [**Является критически важным — системный объект**](a-iscriticalsystemobject.md)                    | Нет     | **Top**      |
| [**Удалено**](a-isdeleted.md)                                                | Нет     | **Top**      |
| [**Входит в состав списка рассылки**](a-memberof.md)                                            | Нет     | **Top**      |
| [**Имеет права владельца**](a-isprivilegeholder.md)                               | Нет     | **Top**      |
| [**Является перезапущенным**](a-isrecycled.md)                                              | Нет     | **Top**      |
| [**Последний-известный-родительский**](a-lastknownparent.md)                                   | Нет     | **Top**      |
| [**Управляемые объекты**](a-managedobjects.md)                                      | Нет     | **Top**      |
| [**В основном**](a-masteredby.md)                                              | Нет     | **Top**      |
| [**Метка времени изменения**](a-modifytimestamp.md)                                   | Нет     | **Top**      |
| [**MS-COM-Партитионсетлинк**](a-mscom-partitionsetlink.md)                      | Нет     | **Top**      |
| [**MS-COM-Усерлинк**](a-mscom-userlink.md)                                      | Нет     | **Top**      |
| [**MS-DFSR-Компутерреференцебл**](a-msdfsr-computerreferencebl.md)              | Нет     | **Top**      |
| [**MS-DFSR-Мемберреференцебл**](a-msdfsr-memberreferencebl.md)                  | Нет     | **Top**      |
| [**MS-DS-примерно-Иммед-подчиненные**](a-msds-approx-immed-subordinates.md)      | Нет     | **Top**      |
| [**MS-DS-Аусентикатедто-Аккаунтлист**](a-msds-authenticatedtoaccountlist.md)   | Нет     | **Top**      |
| [**MS-DS-целостность-дочерняя — количество**](a-ms-ds-consistencychildcount.md)           | Нет     | **Top**      |
| [**MS-DS-Consistencу-Guid**](a-ms-ds-consistencyguid.md)                        | Нет     | **Top**      |
| [**Поддержка MS-DS-Feature-BL**](a-msds-enabledfeaturebl.md)                      | Нет     | **Top**      |
| [**MS-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)             | Нет     | **Top**      |
| [**MS-DS--домен — для**](a-msds-isdomainfor.md)                                | Нет     | **Top**      |
| [**MS-DS-является-Full-реплика для**](a-msds-isfullreplicafor.md)                     | Нет     | **Top**      |
| [**MS-DS-является-partial-реплика для**](a-msds-ispartialreplicafor.md)               | Нет     | **Top**      |
| [**MS-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                              | Нет     | **Top**      |
| [**MS-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                              | Нет     | **Top**      |
| [**MS-DS-локально-эффективное удаление — время**](a-msds-localeffectivedeletiontime.md) | Нет     | **Top**      |
| [**MS-DS-Local-эффективен — время перезапуска**](a-msds-localeffectiverecycletime.md)   | Нет     | **Top**      |
| [**MS-DS-Masterd-by**](a-msds-masteredby.md)                                   | Нет     | **Top**      |
| [**MS-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)                | Нет     | **Top**      |
| [**MS-DS-NC-REPL-курсоры**](a-msds-ncreplcursors.md)                            | Нет     | **Top**      |
| [**MS-DS-NC-REPL-Inbound-соседи**](a-msds-ncreplinboundneighbors.md)         | Нет     | **Top**      |
| [**MS-DS-NC-REPL-Outbound-соседи**](a-msds-ncreploutboundneighbors.md)       | Нет     | **Top**      |
| [**MS-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)    | Нет     | **Top**      |
| [**MS-DS-NC-Type**](a-msds-nctype.md)                                           | Нет     | **Top**      |
| [**MS-DS-не-Members-BL**](a-msds-nonmembersbl.md)                              | Нет     | **Top**      |
| [**MS-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                    | Нет     | **Top**      |
| [**MS-DS-Оидтограуп-Link-BL**](a-msds-oidtogrouplinkbl.md)                      | Нет     | **Top**      |
| [**MS-DS-Operations-для-AZ-Role-BL**](a-msds-operationsforazrolebl.md)          | Нет     | **Top**      |
| [**MS-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)          | Нет     | **Top**      |
| [**MS-DS-Principal-Name**](a-msds-principalname.md)                             | Нет     | **Top**      |
| [**MS-DS-PSO — применяется**](a-msds-psoapplied.md)                                   | Нет     | **Top**      |
| [**MS-DS-REPL-Attribute-Meta-Data**](a-msds-replattributemetadata.md)           | Нет     | **Top**      |
| [**MS-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)                   | Нет     | **Top**      |
| [**MS-DS-выявил-DSA**](a-msds-revealeddsas.md)                               | Нет     | **Top**      |
| [**MS-DS-выводит-List-BL**](a-msds-revealedlistbl.md)                          | Нет     | **Top**      |
| [**MS-DS-Tasks-для-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                    | Нет     | **Top**      |
| [**MS-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                    | Нет     | **Top**      |
| [**MS-дов-Owner-BL**](a-ownerbl.md)                                            | Нет     | **Top**      |
| [**Мссфу-30-POSIX-член-of**](a-mssfu30posixmemberof.md)                       | Нет     | **Top**      |
| [**нетбут-SCP-BL**](a-netbootscpbl.md)                                         | Нет     | **Top**      |
| [**Не-Security-Member-BL**](a-nonsecuritymemberbl.md)                          | Нет     | **Top**      |
| [**NT-Security-дескриптор**](a-ntsecuritydescriptor.md)                         | Верно      | **Top**      |
| [**Obj-расп-имя**](a-distinguishedname.md)                                     | Нет     | **Top**      |
| [**Объект — Категория**](a-objectcategory.md)                                      | Верно      | **Top**      |
| [**Объектный класс**](a-objectclass.md)                                            | Верно      | **Top**      |
| [**Объект — GUID**](a-objectguid.md)                                              | Нет     | **Top**      |
| [**Версия объекта**](a-objectversion.md)                                        | Нет     | **Top**      |
| [**Другие хорошо известные объекты**](a-otherwellknownobjects.md)                      | Нет     | **Top**      |
| [**Разделяемый атрибут-удаление-список**](a-partialattributedeletionlist.md)        | Нет     | **Top**      |
| [**Разделяемый атрибут-set**](a-partialattributeset.md)                           | Нет     | **Top**      |
| [**Возможно — подстрочные**](a-possibleinferiors.md)                                | Нет     | **Top**      |
| [**Прокси-объект-имя**](a-proxiedobjectname.md)                               | Нет     | **Top**      |
| [**Прокси-адреса**](a-proxyaddresses.md)                                      | Нет     | **Top**      |
| [**Запрос — политика — BL**](a-querypolicybl.md)                                       | Нет     | **Top**      |
| [**RDN**](a-name.md)                                                            | Нет     | **Top**      |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                        | Нет     | **Top**      |
| [**REPL-Уптодате-Vector**](a-repluptodatevector.md)                             | Нет     | **Top**      |
| [**Отчеты**](a-directreports.md)                                               | Нет     | **Top**      |
| [**Представители — от**](a-repsfrom.md)                                                  | Нет     | **Top**      |
| [**Представители — кому**](a-repsto.md)                                                      | Нет     | **Top**      |
| [**Редакции**](a-revision.md)                                                   | Нет     | **Top**      |
| [**SD-Rights-эффективен**](a-sdrightseffective.md)                               | Нет     | **Top**      |
| [**Server-Reference-BL**](a-serverreferencebl.md)                               | Нет     | **Top**      |
| [**"Показать" — "Расширенный просмотр"**](a-showinadvancedviewonly.md)                   | Нет     | **Top**      |
| [**Site-Object-BL**](a-siteobjectbl.md)                                         | Нет     | **Top**      |
| [**Структурный объектный класс**](a-structuralobjectclass.md)                       | Нет     | **Top**      |
| [**Подразделы-ReFS**](a-subrefs.md)                                                    | Нет     | **Top**      |
| [**субсчемасубентри**](a-subschemasubentry.md)                                 | Нет     | **Top**      |
| [**Системные флаги**](a-systemflags.md)                                            | Нет     | **Top**      |
| [**USN-изменено**](a-usnchanged.md)                                              | Нет     | **Top**      |
| [**Созданный USN**](a-usncreated.md)                                              | Нет     | **Top**      |
| [**USN-DSA-Last-obj-removed**](a-usndsalastobjremoved.md)                       | Нет     | **Top**      |
| [**USN — межсайтовая**](a-usnintersite.md)                                          | Нет     | **Top**      |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                      | Нет     | **Top**      |
| [**Источник USN**](a-usnsource.md)                                                | Нет     | **Top**      |
| [**WBEM — путь**](a-wbempath.md)                                                  | Нет     | **Top**      |
| [**Хорошо известные объекты**](a-wellknownobjects.md)                                 | Нет     | **Top**      |
| [**При изменении**](a-whenchanged.md)                                            | Нет     | **Top**      |
| [**При создании**](a-whencreated.md)                                            | Нет     | **Top**      |
| [**WWW — Главная страница**](a-wwwhomepage.md)                                           | Нет     | **Top**      |
| [**WWW-Page — другие**](a-url.md)                                                  | Нет     | **Top**      |



## <a name="windows-server-2012"></a>Windows Server 2012

-   [Атрибуты](#windows-server-2012-attributes)



| Ввод | Значение |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Верно                                                                                         |
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



## <a name="windows-server-2012-attributes"></a>Windows Server 2012 Атрибута

Этот класс содержит следующие атрибуты для Windows Server 2012:



| attribute                                                                                    | Обязательный | Унаследован от |
|----------------------------------------------------------------------------------------------|-----------|--------------|
| [**Описание администратора**](a-admindescription.md)                                              | Нет     | **Top**      |
| [**Имя администратора-отображение**](a-admindisplayname.md)                                             | Нет     | **Top**      |
| [**Allowed-Attributes**](a-allowedattributes.md)                                            | Нет     | **Top**      |
| [**Allowed-Attributes-эффективен**](a-allowedattributeseffective.md)                         | Нет     | **Top**      |
| [**Allowed-Child-classes**](a-allowedchildclasses.md)                                       | Нет     | **Top**      |
| [**Allowed-Child-classes-эффективен**](a-allowedchildclasseseffective.md)                    | Нет     | **Top**      |
| [**Плацдарм-Server-List-BL**](a-bridgeheadserverlistbl.md)                                | Нет     | **Top**      |
| [**Каноническое имя**](a-canonicalname.md)                                                    | Нет     | **Top**      |
| [**Common-Name**](a-cn.md)                                                                  | Нет     | **Top**      |
| [**Метка времени создания**](a-createtimestamp.md)                                               | Нет     | **Top**      |
| [**Описание**](a-description.md)                                                         | Нет     | **Top**      |
| [**Отображаемое имя**](a-displayname.md)                                                        | Нет     | **Top**      |
| [**Отображаемое имя — печатаемое**](a-displaynameprintable.md)                                     | Нет     | **Top**      |
| [**DSA-Signature**](a-dsasignature.md)                                                      | Нет     | **Top**      |
| [**DS-Core-распространение-данные**](a-dscorepropagationdata.md)                                  | Нет     | **Top**      |
| [**Имя расширения**](a-extensionname.md)                                                    | Нет     | **Top**      |
| [**Метки**](a-flags.md)                                                                     | Нет     | **Top**      |
| [**Из записи**](a-fromentry.md)                                                            | Нет     | **Top**      |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                                | Нет     | **Top**      |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                                    | Нет     | **Top**      |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                                   | Нет     | **Top**      |
| [**Тип экземпляра**](a-instancetype.md)                                                      | Верно      | **Top**      |
| [**Является критически важным — системный объект**](a-iscriticalsystemobject.md)                                | Нет     | **Top**      |
| [**Удалено**](a-isdeleted.md)                                                            | Нет     | **Top**      |
| [**Входит в состав списка рассылки**](a-memberof.md)                                                        | Нет     | **Top**      |
| [**Имеет права владельца**](a-isprivilegeholder.md)                                           | Нет     | **Top**      |
| [**Является перезапущенным**](a-isrecycled.md)                                                          | Нет     | **Top**      |
| [**Последний-известный-родительский**](a-lastknownparent.md)                                               | Нет     | **Top**      |
| [**Управляемые объекты**](a-managedobjects.md)                                                  | Нет     | **Top**      |
| [**В основном**](a-masteredby.md)                                                          | Нет     | **Top**      |
| [**Метка времени изменения**](a-modifytimestamp.md)                                               | Нет     | **Top**      |
| [**MS-COM-Партитионсетлинк**](a-mscom-partitionsetlink.md)                                  | Нет     | **Top**      |
| [**MS-COM-Усерлинк**](a-mscom-userlink.md)                                                  | Нет     | **Top**      |
| [**MS-DFSR-Компутерреференцебл**](a-msdfsr-computerreferencebl.md)                          | Нет     | **Top**      |
| [**MS-DFSR-Мемберреференцебл**](a-msdfsr-memberreferencebl.md)                              | Нет     | **Top**      |
| [**MS-DS-примерно-Иммед-подчиненные**](a-msds-approx-immed-subordinates.md)                  | Нет     | **Top**      |
| [**MS-DS-Аусентикатедто-Аккаунтлист**](a-msds-authenticatedtoaccountlist.md)               | Нет     | **Top**      |
| [**MS-DS-ClaimSet-shares-возможные значения-with-BL**](a-msds-claimsharespossiblevalueswithbl.md) | Нет     | **Top**      |
| [**MS-DS-целостность-дочерняя — количество**](a-ms-ds-consistencychildcount.md)                       | Нет     | **Top**      |
| [**MS-DS-Consistencу-Guid**](a-ms-ds-consistencyguid.md)                                    | Нет     | **Top**      |
| [**Поддержка MS-DS-Feature-BL**](a-msds-enabledfeaturebl.md)                                  | Нет     | **Top**      |
| [**MS-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)                         | Нет     | **Top**      |
| [**MS-DS--домен — для**](a-msds-isdomainfor.md)                                            | Нет     | **Top**      |
| [**MS-DS-является-Full-реплика для**](a-msds-isfullreplicafor.md)                                 | Нет     | **Top**      |
| [**MS-DS-является-partial-реплика для**](a-msds-ispartialreplicafor.md)                           | Нет     | **Top**      |
| [**MS-DS-является-PRIMARY-Computer-для**](a-msds-isprimarycomputerfor.md)                         | Нет     | **Top**      |
| [**MS-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                          | Нет     | **Top**      |
| [**MS-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                                          | Нет     | **Top**      |
| [**MS-DS-локально-эффективное удаление — время**](a-msds-localeffectivedeletiontime.md)             | Нет     | **Top**      |
| [**MS-DS-Local-эффективен — время перезапуска**](a-msds-localeffectiverecycletime.md)               | Нет     | **Top**      |
| [**MS-DS-Masterd-by**](a-msds-masteredby.md)                                               | Нет     | **Top**      |
| [**MS-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)                            | Нет     | **Top**      |
| [**MS-DS-Members-of-Resource-Property-List-BL**](a-msds-membersofresourcepropertylistbl.md) | Нет     | **Top**      |
| [**MS-DS-NC-REPL-курсоры**](a-msds-ncreplcursors.md)                                        | Нет     | **Top**      |
| [**MS-DS-NC-REPL-Inbound-соседи**](a-msds-ncreplinboundneighbors.md)                     | Нет     | **Top**      |
| [**MS-DS-NC-REPL-Outbound-соседи**](a-msds-ncreploutboundneighbors.md)                   | Нет     | **Top**      |
| [**MS-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)                | Нет     | **Top**      |
| [**MS-DS-NC-Type**](a-msds-nctype.md)                                                       | Нет     | **Top**      |
| [**MS-DS-не-Members-BL**](a-msds-nonmembersbl.md)                                          | Нет     | **Top**      |
| [**MS-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                                | Нет     | **Top**      |
| [**MS-DS-Оидтограуп-Link-BL**](a-msds-oidtogrouplinkbl.md)                                  | Нет     | **Top**      |
| [**MS-DS-Operations-для-AZ-Role-BL**](a-msds-operationsforazrolebl.md)                      | Нет     | **Top**      |
| [**MS-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)                      | Нет     | **Top**      |
| [**MS-DS-Principal-Name**](a-msds-principalname.md)                                         | Нет     | **Top**      |
| [**MS-DS-PSO — применяется**](a-msds-psoapplied.md)                                               | Нет     | **Top**      |
| [**MS-DS-REPL-Attribute-Meta-Data**](a-msds-replattributemetadata.md)                       | Нет     | **Top**      |
| [**MS-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)                               | Нет     | **Top**      |
| [**MS-DS-выявил-DSA**](a-msds-revealeddsas.md)                                           | Нет     | **Top**      |
| [**MS-DS-выводит-List-BL**](a-msds-revealedlistbl.md)                                      | Нет     | **Top**      |
| [**MS-DS-Tasks-для-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                                | Нет     | **Top**      |
| [**MS-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                                | Нет     | **Top**      |
| [**ms-DS-TDO-Egress-BL**](a-msds-tdoegressbl.md)                                            | Нет     | **Top**      |
| [**MS-DS-TDO-входящий трафик — BL**](a-msds-tdoingressbl.md)                                          | Нет     | **Top**      |
| [**MS-DS-value-type-Reference-BL**](a-msds-valuetypereferencebl.md)                         | Нет     | **Top**      |
| [**MS-дов-Owner-BL**](a-ownerbl.md)                                                        | Нет     | **Top**      |
| [**Мссфу-30-POSIX-член-of**](a-mssfu30posixmemberof.md)                                   | Нет     | **Top**      |
| [**нетбут-SCP-BL**](a-netbootscpbl.md)                                                     | Нет     | **Top**      |
| [**Не-Security-Member-BL**](a-nonsecuritymemberbl.md)                                      | Нет     | **Top**      |
| [**NT-Security-дескриптор**](a-ntsecuritydescriptor.md)                                     | Верно      | **Top**      |
| [**Obj-расп-имя**](a-distinguishedname.md)                                                 | Нет     | **Top**      |
| [**Объект — Категория**](a-objectcategory.md)                                                  | Верно      | **Top**      |
| [**Объектный класс**](a-objectclass.md)                                                        | Верно      | **Top**      |
| [**Объект — GUID**](a-objectguid.md)                                                          | Нет     | **Top**      |
| [**Версия объекта**](a-objectversion.md)                                                    | Нет     | **Top**      |
| [**Другие хорошо известные объекты**](a-otherwellknownobjects.md)                                  | Нет     | **Top**      |
| [**Разделяемый атрибут-удаление-список**](a-partialattributedeletionlist.md)                    | Нет     | **Top**      |
| [**Разделяемый атрибут-set**](a-partialattributeset.md)                                       | Нет     | **Top**      |
| [**Возможно — подстрочные**](a-possibleinferiors.md)                                            | Нет     | **Top**      |
| [**Прокси-объект-имя**](a-proxiedobjectname.md)                                           | Нет     | **Top**      |
| [**Прокси-адреса**](a-proxyaddresses.md)                                                  | Нет     | **Top**      |
| [**Запрос — политика — BL**](a-querypolicybl.md)                                                   | Нет     | **Top**      |
| [**RDN**](a-name.md)                                                                        | Нет     | **Top**      |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                                    | Нет     | **Top**      |
| [**REPL-Уптодате-Vector**](a-repluptodatevector.md)                                         | Нет     | **Top**      |
| [**Отчеты**](a-directreports.md)                                                           | Нет     | **Top**      |
| [**Представители — от**](a-repsfrom.md)                                                              | Нет     | **Top**      |
| [**Представители — кому**](a-repsto.md)                                                                  | Нет     | **Top**      |
| [**Редакции**](a-revision.md)                                                               | Нет     | **Top**      |
| [**SD-Rights-эффективен**](a-sdrightseffective.md)                                           | Нет     | **Top**      |
| [**Server-Reference-BL**](a-serverreferencebl.md)                                           | Нет     | **Top**      |
| [**"Показать" — "Расширенный просмотр"**](a-showinadvancedviewonly.md)                               | Нет     | **Top**      |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                     | Нет     | **Top**      |
| [**Структурный объектный класс**](a-structuralobjectclass.md)                                   | Нет     | **Top**      |
| [**Подразделы-ReFS**](a-subrefs.md)                                                                | Нет     | **Top**      |
| [**субсчемасубентри**](a-subschemasubentry.md)                                             | Нет     | **Top**      |
| [**Системные флаги**](a-systemflags.md)                                                        | Нет     | **Top**      |
| [**USN-изменено**](a-usnchanged.md)                                                          | Нет     | **Top**      |
| [**Созданный USN**](a-usncreated.md)                                                          | Нет     | **Top**      |
| [**USN-DSA-Last-obj-removed**](a-usndsalastobjremoved.md)                                   | Нет     | **Top**      |
| [**USN — межсайтовая**](a-usnintersite.md)                                                      | Нет     | **Top**      |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                                  | Нет     | **Top**      |
| [**Источник USN**](a-usnsource.md)                                                            | Нет     | **Top**      |
| [**WBEM — путь**](a-wbempath.md)                                                              | Нет     | **Top**      |
| [**Хорошо известные объекты**](a-wellknownobjects.md)                                             | Нет     | **Top**      |
| [**При изменении**](a-whenchanged.md)                                                        | Нет     | **Top**      |
| [**При создании**](a-whencreated.md)                                                        | Нет     | **Top**      |
| [**WWW — Главная страница**](a-wwwhomepage.md)                                                       | Нет     | **Top**      |
| [**WWW-Page — другие**](a-url.md)                                                              | Нет     | **Top**      |



 

 





