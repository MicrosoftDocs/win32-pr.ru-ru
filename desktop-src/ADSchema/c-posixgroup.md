---
title: класс Посиксграуп
description: Представляет абстракцию группы учетных записей.
ms.assetid: d6fa3aab-cb98-4774-b419-afae975c6917
ms.tgt_platform: multiple
keywords:
- Схема AD класса Посиксграуп
topic_type:
- apiref
api_name:
- posixGroup
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3787ae7f918c9829de61a15ed146adc6bc19a178019304cc3f38894e9afd5d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118680509"
---
# <a name="posixgroup-class"></a>класс Посиксграуп

Представляет абстракцию группы учетных записей.



| Ввод | Значение |
|-------------------|--------------------------------------|
| CN                | посиксграуп                           |
| LDAP-отображаемое имя | посиксграуп                           |
| Привилегия обновления  | \-                                   |
| Частота обновления  | \-                                   |
| Schema-ID-GUID    | 2a9350b8-062c-4ed0-9903-dde10d06deba |



## <a name="implementations"></a>Варианты реализации решения

-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2

-   [Атрибуты](#windows-server-2003-r2-attributes)



| Ввод | Значение |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Неверно                                                                                        |
| Object-Category             | 3                                                                                            |
| По умолчанию — объект — Категория     | \-                                                                                           |
| Governs-Id                  | 1.3.6.1.1.1.2.2                                                                              |
| По умолчанию-скрытие значения        | 1                                                                                            |
| RDN-Атри-ID                  | [**Common-Name**](a-cn.md)<br/>                                                       |
| Подкласс                 | [**Начало**](c-top.md)<br/>                                                              |
| Возможные старшие          | \-                                                                                           |
| Вспомогательные классы           | \-                                                                                           |
| NT-Security-дескриптор      | О:БАГ: BAD: S:                                                                                 |
| Дескриптор безопасности по умолчанию | D: (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;;D А) (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;; SY) (A;; РПЛКЛОРК;;; СЛУЖБЫ |
| System-Flags                | 0x00000000                                                                                   |



## <a name="windows-server-2003-r2-attributes"></a>Windows Атрибуты сервера 2003 R2

этот класс содержит следующие атрибуты для Windows Server 2003 R2:



| attribute                                                                   | Обязательный | Унаследован от                                   |
|-----------------------------------------------------------------------------|-----------|------------------------------------------------|
| [**Описание администратора**](a-admindescription.md)                             | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Имя администратора-отображение**](a-admindisplayname.md)                            | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Allowed-Attributes**](a-allowedattributes.md)                           | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Allowed-Attributes-эффективен**](a-allowedattributeseffective.md)        | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Allowed-Child-classes**](a-allowedchildclasses.md)                      | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Allowed-Child-classes-эффективен**](a-allowedchildclasseseffective.md)   | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Плацдарм-Server-List-BL**](a-bridgeheadserverlistbl.md)               | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Каноническое имя**](a-canonicalname.md)                                   | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Common-Name**](a-cn.md)                                                 | Неверно     | **посиксграуп** [ **сверху**](c-top.md)<br/> |
| [**Метка времени создания**](a-createtimestamp.md)                              | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Описание**](a-description.md)                                        | Неверно     | **посиксграуп** [ **сверху**](c-top.md)<br/> |
| [**Отображаемое имя**](a-displayname.md)                                       | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Отображаемое имя — печатаемое**](a-displaynameprintable.md)                    | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**DSA-Signature**](a-dsasignature.md)                                     | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**DS-Core-распространение-данные**](a-dscorepropagationdata.md)                 | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Имя расширения**](a-extensionname.md)                                   | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Флаги**](a-flags.md)                                                    | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Из записи**](a-fromentry.md)                                           | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**gidNumber**](a-gidnumber.md)                                            | Неверно     | **посиксграуп**                                 |
| [**Тип экземпляра**](a-instancetype.md)                                     | True      | [**Начало**](c-top.md)<br/>                |
| [**Является критически важным — системный объект**](a-iscriticalsystemobject.md)               | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Удалено**](a-isdeleted.md)                                           | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Входит в состав списка рассылки**](a-memberof.md)                                       | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Имеет права владельца**](a-isprivilegeholder.md)                          | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Последний-известный-родительский**](a-lastknownparent.md)                              | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Управляемые объекты**](a-managedobjects.md)                                 | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**В основном**](a-masteredby.md)                                         | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**мемберуид**](a-memberuid.md)                                            | Неверно     | **посиксграуп**                                 |
| [**Метка времени изменения**](a-modifytimestamp.md)                              | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-COM-Партитионсетлинк**](a-mscom-partitionsetlink.md)                 | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-COM-Усерлинк**](a-mscom-userlink.md)                                 | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DFSR-Компутерреференцебл**](a-msdfsr-computerreferencebl.md)         | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DFSR-Мемберреференцебл**](a-msdfsr-memberreferencebl.md)             | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-примерно-Иммед-подчиненные**](a-msds-approx-immed-subordinates.md) | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-целостность-дочерняя — количество**](a-ms-ds-consistencychildcount.md)      | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-Consistencу-Guid**](a-ms-ds-consistencyguid.md)                   | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-Masterd-by**](a-msds-masteredby.md)                              | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)           | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-NC-REPL-курсоры**](a-msds-ncreplcursors.md)                       | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-NC-REPL-Inbound-соседи**](a-msds-ncreplinboundneighbors.md)    | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-NC-REPL-Outbound-соседи**](a-msds-ncreploutboundneighbors.md)  | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-не-Members-BL**](a-msds-nonmembersbl.md)                         | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-Operations-для-AZ-Role-BL**](a-msds-operationsforazrolebl.md)     | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)     | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-REPL-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)              | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-Tasks-для-AZ-Role-BL**](a-msds-tasksforazrolebl.md)               | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)               | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-дов-Owner-BL**](a-ownerbl.md)                                       | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Мссфу-30-POSIX-член-of**](a-mssfu30posixmemberof.md)                  | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**нетбут-SCP-BL**](a-netbootscpbl.md)                                    | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Не-Security-Member-BL**](a-nonsecuritymemberbl.md)                     | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**NT-Security-дескриптор**](a-ntsecuritydescriptor.md)                    | Верно      | [**Начало**](c-top.md)<br/>                |
| [**Obj-расп-имя**](a-distinguishedname.md)                                | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Объект — Категория**](a-objectcategory.md)                                 | Верно      | [**Начало**](c-top.md)<br/>                |
| [**Объектный класс**](a-objectclass.md)                                       | True      | [**Начало**](c-top.md)<br/>                |
| [**Объект — GUID**](a-objectguid.md)                                         | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Версия объекта**](a-objectversion.md)                                   | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Другие хорошо известные объекты**](a-otherwellknownobjects.md)                 | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Разделяемый атрибут-удаление-список**](a-partialattributedeletionlist.md)   | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Разделяемый атрибут-set**](a-partialattributeset.md)                      | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Возможно — подстрочные**](a-possibleinferiors.md)                           | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Прокси-объект-имя**](a-proxiedobjectname.md)                          | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Прокси-адреса**](a-proxyaddresses.md)                                 | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Запрос — политика — BL**](a-querypolicybl.md)                                  | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**RDN**](a-name.md)                                                       | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                   | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**REPL-Уптодате-Vector**](a-repluptodatevector.md)                        | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Отчеты**](a-directreports.md)                                          | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Представители — от**](a-repsfrom.md)                                             | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Представители — кому**](a-repsto.md)                                                 | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Редакции**](a-revision.md)                                              | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**SD-Rights-эффективен**](a-sdrightseffective.md)                          | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**"Показать" — "Расширенный просмотр"**](a-showinadvancedviewonly.md)              | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Структурный объектный класс**](a-structuralobjectclass.md)                  | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Подразделы-ReFS**](a-subrefs.md)                                               | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**субсчемасубентри**](a-subschemasubentry.md)                            | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Системные флаги**](a-systemflags.md)                                       | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**униксусерпассворд**](a-unixuserpassword.md)                              | Неверно     | **посиксграуп**                                 |
| [**Пароль пользователя**](a-userpassword.md)                                     | Неверно     | **посиксграуп**                                 |
| [**USN-изменено**](a-usnchanged.md)                                         | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Созданный USN**](a-usncreated.md)                                         | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**USN-DSA-Last-obj-removed**](a-usndsalastobjremoved.md)                  | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**USN — межсайтовая**](a-usnintersite.md)                                     | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                 | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Источник USN**](a-usnsource.md)                                           | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**WBEM — путь**](a-wbempath.md)                                             | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Хорошо известные объекты**](a-wellknownobjects.md)                            | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**При изменении**](a-whenchanged.md)                                       | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**При создании**](a-whencreated.md)                                       | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**WWW — Главная страница**](a-wwwhomepage.md)                                      | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**WWW-Page — другие**](a-url.md)                                             | Неверно     | [**Начало**](c-top.md)<br/>                |



## <a name="windows-server-2008"></a>Windows Server 2008

-   [Атрибуты](#windows-server-2008-attributes)



| Ввод | Значение |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Неверно                                                                                        |
| Object-Category             | 3                                                                                            |
| По умолчанию — объект — Категория     | \-                                                                                           |
| Governs-Id                  | 1.3.6.1.1.1.2.2                                                                              |
| По умолчанию-скрытие значения        | 1                                                                                            |
| RDN-Атри-ID                  | [**Common-Name**](a-cn.md)<br/>                                                       |
| Подкласс                 | [**Начало**](c-top.md)<br/>                                                              |
| Возможные старшие          | \-                                                                                           |
| Вспомогательные классы           | \-                                                                                           |
| NT-Security-дескриптор      | О:БАГ: BAD: S:                                                                                 |
| Дескриптор безопасности по умолчанию | D: (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;;D А) (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;; SY) (A;; РПЛКЛОРК;;; СЛУЖБЫ |
| System-Flags                | 0x00000000                                                                                   |



## <a name="windows-server-2008-attributes"></a>Windows Атрибуты сервера 2008

этот класс содержит следующие атрибуты для Windows Server 2008:



| attribute                                                                      | Обязательный | Унаследован от                                   |
|--------------------------------------------------------------------------------|-----------|------------------------------------------------|
| [**Описание администратора**](a-admindescription.md)                                | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Имя администратора-отображение**](a-admindisplayname.md)                               | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Allowed-Attributes**](a-allowedattributes.md)                              | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Allowed-Attributes-эффективен**](a-allowedattributeseffective.md)           | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Allowed-Child-classes**](a-allowedchildclasses.md)                         | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Allowed-Child-classes-эффективен**](a-allowedchildclasseseffective.md)      | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Плацдарм-Server-List-BL**](a-bridgeheadserverlistbl.md)                  | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Каноническое имя**](a-canonicalname.md)                                      | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Common-Name**](a-cn.md)                                                    | Неверно     | **посиксграуп** [ **сверху**](c-top.md)<br/> |
| [**Метка времени создания**](a-createtimestamp.md)                                 | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Описание**](a-description.md)                                           | Неверно     | **посиксграуп** [ **сверху**](c-top.md)<br/> |
| [**Отображаемое имя**](a-displayname.md)                                          | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Отображаемое имя — печатаемое**](a-displaynameprintable.md)                       | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**DSA-Signature**](a-dsasignature.md)                                        | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**DS-Core-распространение-данные**](a-dscorepropagationdata.md)                    | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Имя расширения**](a-extensionname.md)                                      | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Флаги**](a-flags.md)                                                       | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Из записи**](a-fromentry.md)                                              | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                  | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                      | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                     | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**gidNumber**](a-gidnumber.md)                                               | Неверно     | **посиксграуп**                                 |
| [**Тип экземпляра**](a-instancetype.md)                                        | True      | [**Начало**](c-top.md)<br/>                |
| [**Является критически важным — системный объект**](a-iscriticalsystemobject.md)                  | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Удалено**](a-isdeleted.md)                                              | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Входит в состав списка рассылки**](a-memberof.md)                                          | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Имеет права владельца**](a-isprivilegeholder.md)                             | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Последний-известный-родительский**](a-lastknownparent.md)                                 | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Управляемые объекты**](a-managedobjects.md)                                    | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**В основном**](a-masteredby.md)                                            | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**мемберуид**](a-memberuid.md)                                               | Неверно     | **посиксграуп**                                 |
| [**Метка времени изменения**](a-modifytimestamp.md)                                 | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-COM-Партитионсетлинк**](a-mscom-partitionsetlink.md)                    | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-COM-Усерлинк**](a-mscom-userlink.md)                                    | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DFSR-Компутерреференцебл**](a-msdfsr-computerreferencebl.md)            | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DFSR-Мемберреференцебл**](a-msdfsr-memberreferencebl.md)                | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-примерно-Иммед-подчиненные**](a-msds-approx-immed-subordinates.md)    | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-Аусентикатедто-Аккаунтлист**](a-msds-authenticatedtoaccountlist.md) | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-целостность-дочерняя — количество**](a-ms-ds-consistencychildcount.md)         | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-Consistencу-Guid**](a-ms-ds-consistencyguid.md)                      | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS--домен — для**](a-msds-isdomainfor.md)                              | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-является-Full-реплика для**](a-msds-isfullreplicafor.md)                   | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-является-partial-реплика для**](a-msds-ispartialreplicafor.md)             | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                            | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-Masterd-by**](a-msds-masteredby.md)                                 | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)              | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-NC-REPL-курсоры**](a-msds-ncreplcursors.md)                          | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-NC-REPL-Inbound-соседи**](a-msds-ncreplinboundneighbors.md)       | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-NC-REPL-Outbound-соседи**](a-msds-ncreploutboundneighbors.md)     | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)  | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-NC-Type**](a-msds-nctype.md)                                         | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-не-Members-BL**](a-msds-nonmembersbl.md)                            | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                  | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-Operations-для-AZ-Role-BL**](a-msds-operationsforazrolebl.md)        | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)        | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-Principal-Name**](a-msds-principalname.md)                           | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-PSO — применяется**](a-msds-psoapplied.md)                                 | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-REPL-Attribute-Meta-Data**](a-msds-replattributemetadata.md)         | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)                 | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-выявил-DSA**](a-msds-revealeddsas.md)                             | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-выводит-List-BL**](a-msds-revealedlistbl.md)                        | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-Tasks-для-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                  | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                  | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-дов-Owner-BL**](a-ownerbl.md)                                          | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Мссфу-30-POSIX-член-of**](a-mssfu30posixmemberof.md)                     | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**нетбут-SCP-BL**](a-netbootscpbl.md)                                       | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Не-Security-Member-BL**](a-nonsecuritymemberbl.md)                        | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**NT-Security-дескриптор**](a-ntsecuritydescriptor.md)                       | Верно      | [**Начало**](c-top.md)<br/>                |
| [**Obj-расп-имя**](a-distinguishedname.md)                                   | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Объект — Категория**](a-objectcategory.md)                                    | True      | [**Начало**](c-top.md)<br/>                |
| [**Объектный класс**](a-objectclass.md)                                          | True      | [**Начало**](c-top.md)<br/>                |
| [**Объект — GUID**](a-objectguid.md)                                            | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Версия объекта**](a-objectversion.md)                                      | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Другие хорошо известные объекты**](a-otherwellknownobjects.md)                    | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Разделяемый атрибут-удаление-список**](a-partialattributedeletionlist.md)      | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Разделяемый атрибут-set**](a-partialattributeset.md)                         | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Возможно — подстрочные**](a-possibleinferiors.md)                              | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Прокси-объект-имя**](a-proxiedobjectname.md)                             | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Прокси-адреса**](a-proxyaddresses.md)                                    | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Запрос — политика — BL**](a-querypolicybl.md)                                     | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**RDN**](a-name.md)                                                          | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                      | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**REPL-Уптодате-Vector**](a-repluptodatevector.md)                           | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Отчеты**](a-directreports.md)                                             | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Представители — от**](a-repsfrom.md)                                                | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Представители — кому**](a-repsto.md)                                                    | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Редакции**](a-revision.md)                                                 | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**SD-Rights-эффективен**](a-sdrightseffective.md)                             | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Server-Reference-BL**](a-serverreferencebl.md)                             | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**"Показать" — "Расширенный просмотр"**](a-showinadvancedviewonly.md)                 | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Site-Object-BL**](a-siteobjectbl.md)                                       | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Структурный объектный класс**](a-structuralobjectclass.md)                     | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Подразделы-ReFS**](a-subrefs.md)                                                  | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**субсчемасубентри**](a-subschemasubentry.md)                               | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Системные флаги**](a-systemflags.md)                                          | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**униксусерпассворд**](a-unixuserpassword.md)                                 | Неверно     | **посиксграуп**                                 |
| [**Пароль пользователя**](a-userpassword.md)                                        | Неверно     | **посиксграуп**                                 |
| [**USN-изменено**](a-usnchanged.md)                                            | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Созданный USN**](a-usncreated.md)                                            | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**USN-DSA-Last-obj-removed**](a-usndsalastobjremoved.md)                     | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**USN — межсайтовая**](a-usnintersite.md)                                        | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                    | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Источник USN**](a-usnsource.md)                                              | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**WBEM — путь**](a-wbempath.md)                                                | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Хорошо известные объекты**](a-wellknownobjects.md)                               | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**При изменении**](a-whenchanged.md)                                          | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**При создании**](a-whencreated.md)                                          | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**WWW — Главная страница**](a-wwwhomepage.md)                                         | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**WWW-Page — другие**](a-url.md)                                                | Неверно     | [**Начало**](c-top.md)<br/>                |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2

-   [Атрибуты](#windows-server-2008-r2-attributes)



| Ввод | Значение |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Неверно                                                                                        |
| Object-Category             | 3                                                                                            |
| По умолчанию — объект — Категория     | \-                                                                                           |
| Governs-Id                  | 1.3.6.1.1.1.2.2                                                                              |
| По умолчанию-скрытие значения        | 1                                                                                            |
| RDN-Атри-ID                  | [**Common-Name**](a-cn.md)<br/>                                                       |
| Подкласс                 | [**Начало**](c-top.md)<br/>                                                              |
| Возможные старшие          | \-                                                                                           |
| Вспомогательные классы           | \-                                                                                           |
| NT-Security-дескриптор      | О:БАГ: BAD: S:                                                                                 |
| Дескриптор безопасности по умолчанию | D: (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;;D А) (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;; SY) (A;; РПЛКЛОРК;;; СЛУЖБЫ |
| System-Flags                | 0x00000000                                                                                   |



## <a name="windows-server-2008-r2-attributes"></a>Windows Атрибуты сервера 2008 R2

этот класс содержит следующие атрибуты для Windows Server 2008 R2:



| attribute                                                                        | Обязательный | Унаследован от                                   |
|----------------------------------------------------------------------------------|-----------|------------------------------------------------|
| [**Описание администратора**](a-admindescription.md)                                  | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Имя администратора-отображение**](a-admindisplayname.md)                                 | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Allowed-Attributes**](a-allowedattributes.md)                                | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Allowed-Attributes-эффективен**](a-allowedattributeseffective.md)             | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Allowed-Child-classes**](a-allowedchildclasses.md)                           | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Allowed-Child-classes-эффективен**](a-allowedchildclasseseffective.md)        | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Плацдарм-Server-List-BL**](a-bridgeheadserverlistbl.md)                    | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Каноническое имя**](a-canonicalname.md)                                        | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Common-Name**](a-cn.md)                                                      | Неверно     | **посиксграуп** [ **сверху**](c-top.md)<br/> |
| [**Метка времени создания**](a-createtimestamp.md)                                   | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Описание**](a-description.md)                                             | Неверно     | **посиксграуп** [ **сверху**](c-top.md)<br/> |
| [**Отображаемое имя**](a-displayname.md)                                            | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Отображаемое имя — печатаемое**](a-displaynameprintable.md)                         | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**DSA-Signature**](a-dsasignature.md)                                          | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**DS-Core-распространение-данные**](a-dscorepropagationdata.md)                      | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Имя расширения**](a-extensionname.md)                                        | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Флаги**](a-flags.md)                                                         | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Из записи**](a-fromentry.md)                                                | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                    | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                        | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                       | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**gidNumber**](a-gidnumber.md)                                                 | Неверно     | **посиксграуп**                                 |
| [**Тип экземпляра**](a-instancetype.md)                                          | True      | [**Начало**](c-top.md)<br/>                |
| [**Является критически важным — системный объект**](a-iscriticalsystemobject.md)                    | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Удалено**](a-isdeleted.md)                                                | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Входит в состав списка рассылки**](a-memberof.md)                                            | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Имеет права владельца**](a-isprivilegeholder.md)                               | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Является перезапущенным**](a-isrecycled.md)                                              | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Последний-известный-родительский**](a-lastknownparent.md)                                   | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Управляемые объекты**](a-managedobjects.md)                                      | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**В основном**](a-masteredby.md)                                              | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**мемберуид**](a-memberuid.md)                                                 | Неверно     | **посиксграуп**                                 |
| [**Метка времени изменения**](a-modifytimestamp.md)                                   | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-COM-Партитионсетлинк**](a-mscom-partitionsetlink.md)                      | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-COM-Усерлинк**](a-mscom-userlink.md)                                      | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DFSR-Компутерреференцебл**](a-msdfsr-computerreferencebl.md)              | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DFSR-Мемберреференцебл**](a-msdfsr-memberreferencebl.md)                  | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-примерно-Иммед-подчиненные**](a-msds-approx-immed-subordinates.md)      | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-Аусентикатедто-Аккаунтлист**](a-msds-authenticatedtoaccountlist.md)   | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-целостность-дочерняя — количество**](a-ms-ds-consistencychildcount.md)           | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-Consistencу-Guid**](a-ms-ds-consistencyguid.md)                        | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Поддержка MS-DS-Feature-BL**](a-msds-enabledfeaturebl.md)                      | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)             | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS--домен — для**](a-msds-isdomainfor.md)                                | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-является-Full-реплика для**](a-msds-isfullreplicafor.md)                     | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-является-partial-реплика для**](a-msds-ispartialreplicafor.md)               | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                              | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                              | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-локально-эффективное удаление — время**](a-msds-localeffectivedeletiontime.md) | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-Local-эффективен — время перезапуска**](a-msds-localeffectiverecycletime.md)   | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-Masterd-by**](a-msds-masteredby.md)                                   | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)                | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-NC-REPL-курсоры**](a-msds-ncreplcursors.md)                            | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-NC-REPL-Inbound-соседи**](a-msds-ncreplinboundneighbors.md)         | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-NC-REPL-Outbound-соседи**](a-msds-ncreploutboundneighbors.md)       | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)    | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-NC-Type**](a-msds-nctype.md)                                           | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-не-Members-BL**](a-msds-nonmembersbl.md)                              | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                    | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-Оидтограуп-Link-BL**](a-msds-oidtogrouplinkbl.md)                      | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-Operations-для-AZ-Role-BL**](a-msds-operationsforazrolebl.md)          | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)          | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-Principal-Name**](a-msds-principalname.md)                             | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-PSO — применяется**](a-msds-psoapplied.md)                                   | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-REPL-Attribute-Meta-Data**](a-msds-replattributemetadata.md)           | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)                   | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-выявил-DSA**](a-msds-revealeddsas.md)                               | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-выводит-List-BL**](a-msds-revealedlistbl.md)                          | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-Tasks-для-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                    | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                    | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-дов-Owner-BL**](a-ownerbl.md)                                            | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Мссфу-30-POSIX-член-of**](a-mssfu30posixmemberof.md)                       | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**нетбут-SCP-BL**](a-netbootscpbl.md)                                         | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Не-Security-Member-BL**](a-nonsecuritymemberbl.md)                          | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**NT-Security-дескриптор**](a-ntsecuritydescriptor.md)                         | Верно      | [**Начало**](c-top.md)<br/>                |
| [**Obj-расп-имя**](a-distinguishedname.md)                                     | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Объект — Категория**](a-objectcategory.md)                                      | Верно      | [**Начало**](c-top.md)<br/>                |
| [**Объектный класс**](a-objectclass.md)                                            | Верно      | [**Начало**](c-top.md)<br/>                |
| [**Объект — GUID**](a-objectguid.md)                                              | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Версия объекта**](a-objectversion.md)                                        | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Другие хорошо известные объекты**](a-otherwellknownobjects.md)                      | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Разделяемый атрибут-удаление-список**](a-partialattributedeletionlist.md)        | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Разделяемый атрибут-set**](a-partialattributeset.md)                           | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Возможно — подстрочные**](a-possibleinferiors.md)                                | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Прокси-объект-имя**](a-proxiedobjectname.md)                               | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Прокси-адреса**](a-proxyaddresses.md)                                      | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Запрос — политика — BL**](a-querypolicybl.md)                                       | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**RDN**](a-name.md)                                                            | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                        | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**REPL-Уптодате-Vector**](a-repluptodatevector.md)                             | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Отчеты**](a-directreports.md)                                               | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Представители — от**](a-repsfrom.md)                                                  | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Представители — кому**](a-repsto.md)                                                      | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Редакции**](a-revision.md)                                                   | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**SD-Rights-эффективен**](a-sdrightseffective.md)                               | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Server-Reference-BL**](a-serverreferencebl.md)                               | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**"Показать" — "Расширенный просмотр"**](a-showinadvancedviewonly.md)                   | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Site-Object-BL**](a-siteobjectbl.md)                                         | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Структурный объектный класс**](a-structuralobjectclass.md)                       | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Подразделы-ReFS**](a-subrefs.md)                                                    | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**субсчемасубентри**](a-subschemasubentry.md)                                 | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Системные флаги**](a-systemflags.md)                                            | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**униксусерпассворд**](a-unixuserpassword.md)                                   | Неверно     | **посиксграуп**                                 |
| [**Пароль пользователя**](a-userpassword.md)                                          | Неверно     | **посиксграуп**                                 |
| [**USN-изменено**](a-usnchanged.md)                                              | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Созданный USN**](a-usncreated.md)                                              | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**USN-DSA-Last-obj-removed**](a-usndsalastobjremoved.md)                       | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**USN — межсайтовая**](a-usnintersite.md)                                          | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                      | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Источник USN**](a-usnsource.md)                                                | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**WBEM — путь**](a-wbempath.md)                                                  | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Хорошо известные объекты**](a-wellknownobjects.md)                                 | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**При изменении**](a-whenchanged.md)                                            | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**При создании**](a-whencreated.md)                                            | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**WWW — Главная страница**](a-wwwhomepage.md)                                           | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**WWW-Page — другие**](a-url.md)                                                  | Неверно     | [**Начало**](c-top.md)<br/>                |



## <a name="windows-server-2012"></a>Windows Server 2012

-   [Атрибуты](#windows-server-2012-attributes)



| Ввод | Значение |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Неверно                                                                                        |
| Object-Category             | 3                                                                                            |
| По умолчанию — объект — Категория     | \-                                                                                           |
| Governs-Id                  | 1.3.6.1.1.1.2.2                                                                              |
| По умолчанию-скрытие значения        | 1                                                                                            |
| RDN-Атри-ID                  | [**Common-Name**](a-cn.md)<br/>                                                       |
| Подкласс                 | [**Начало**](c-top.md)<br/>                                                              |
| Возможные старшие          | \-                                                                                           |
| Вспомогательные классы           | \-                                                                                           |
| NT-Security-дескриптор      | О:БАГ: BAD: S:                                                                                 |
| Дескриптор безопасности по умолчанию | D: (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;;D А) (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;; SY) (A;; РПЛКЛОРК;;; СЛУЖБЫ |
| System-Flags                | 0x00000000                                                                                   |



## <a name="windows-server-2012-attributes"></a>Windows Server 2012 Атрибута

Этот класс содержит следующие атрибуты для Windows Server 2012:



| attribute                                                                                    | Обязательный | Унаследован от                                   |
|----------------------------------------------------------------------------------------------|-----------|------------------------------------------------|
| [**Описание администратора**](a-admindescription.md)                                              | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Имя администратора-отображение**](a-admindisplayname.md)                                             | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Allowed-Attributes**](a-allowedattributes.md)                                            | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Allowed-Attributes-эффективен**](a-allowedattributeseffective.md)                         | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Allowed-Child-classes**](a-allowedchildclasses.md)                                       | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Allowed-Child-classes-эффективен**](a-allowedchildclasseseffective.md)                    | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Плацдарм-Server-List-BL**](a-bridgeheadserverlistbl.md)                                | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Каноническое имя**](a-canonicalname.md)                                                    | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Common-Name**](a-cn.md)                                                                  | Неверно     | **посиксграуп** [ **сверху**](c-top.md)<br/> |
| [**Метка времени создания**](a-createtimestamp.md)                                               | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Описание**](a-description.md)                                                         | Неверно     | **посиксграуп** [ **сверху**](c-top.md)<br/> |
| [**Отображаемое имя**](a-displayname.md)                                                        | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Отображаемое имя — печатаемое**](a-displaynameprintable.md)                                     | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**DSA-Signature**](a-dsasignature.md)                                                      | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**DS-Core-распространение-данные**](a-dscorepropagationdata.md)                                  | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Имя расширения**](a-extensionname.md)                                                    | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Флаги**](a-flags.md)                                                                     | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Из записи**](a-fromentry.md)                                                            | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                                | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                                    | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                                   | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**gidNumber**](a-gidnumber.md)                                                             | Неверно     | **посиксграуп**                                 |
| [**Тип экземпляра**](a-instancetype.md)                                                      | True      | [**Начало**](c-top.md)<br/>                |
| [**Является критически важным — системный объект**](a-iscriticalsystemobject.md)                                | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Удалено**](a-isdeleted.md)                                                            | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Входит в состав списка рассылки**](a-memberof.md)                                                        | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Имеет права владельца**](a-isprivilegeholder.md)                                           | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Является перезапущенным**](a-isrecycled.md)                                                          | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Последний-известный-родительский**](a-lastknownparent.md)                                               | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Управляемые объекты**](a-managedobjects.md)                                                  | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**В основном**](a-masteredby.md)                                                          | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**мемберуид**](a-memberuid.md)                                                             | Неверно     | **посиксграуп**                                 |
| [**Метка времени изменения**](a-modifytimestamp.md)                                               | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-COM-Партитионсетлинк**](a-mscom-partitionsetlink.md)                                  | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-COM-Усерлинк**](a-mscom-userlink.md)                                                  | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DFSR-Компутерреференцебл**](a-msdfsr-computerreferencebl.md)                          | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DFSR-Мемберреференцебл**](a-msdfsr-memberreferencebl.md)                              | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-примерно-Иммед-подчиненные**](a-msds-approx-immed-subordinates.md)                  | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-Аусентикатедто-Аккаунтлист**](a-msds-authenticatedtoaccountlist.md)               | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-ClaimSet-shares-возможные значения-with-BL**](a-msds-claimsharespossiblevalueswithbl.md) | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-целостность-дочерняя — количество**](a-ms-ds-consistencychildcount.md)                       | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-Consistencу-Guid**](a-ms-ds-consistencyguid.md)                                    | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Поддержка MS-DS-Feature-BL**](a-msds-enabledfeaturebl.md)                                  | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)                         | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS--домен — для**](a-msds-isdomainfor.md)                                            | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-является-Full-реплика для**](a-msds-isfullreplicafor.md)                                 | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-является-partial-реплика для**](a-msds-ispartialreplicafor.md)                           | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-является-PRIMARY-Computer-для**](a-msds-isprimarycomputerfor.md)                         | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                          | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                                          | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-локально-эффективное удаление — время**](a-msds-localeffectivedeletiontime.md)             | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-Local-эффективен — время перезапуска**](a-msds-localeffectiverecycletime.md)               | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-Masterd-by**](a-msds-masteredby.md)                                               | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)                            | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-Members-of-Resource-Property-List-BL**](a-msds-membersofresourcepropertylistbl.md) | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-NC-REPL-курсоры**](a-msds-ncreplcursors.md)                                        | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-NC-REPL-Inbound-соседи**](a-msds-ncreplinboundneighbors.md)                     | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-NC-REPL-Outbound-соседи**](a-msds-ncreploutboundneighbors.md)                   | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)                | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-NC-Type**](a-msds-nctype.md)                                                       | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-не-Members-BL**](a-msds-nonmembersbl.md)                                          | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                                | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-Оидтограуп-Link-BL**](a-msds-oidtogrouplinkbl.md)                                  | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-Operations-для-AZ-Role-BL**](a-msds-operationsforazrolebl.md)                      | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)                      | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-Principal-Name**](a-msds-principalname.md)                                         | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-PSO — применяется**](a-msds-psoapplied.md)                                               | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-REPL-Attribute-Meta-Data**](a-msds-replattributemetadata.md)                       | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)                               | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-выявил-DSA**](a-msds-revealeddsas.md)                                           | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-выводит-List-BL**](a-msds-revealedlistbl.md)                                      | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-Tasks-для-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                                | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                                | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**ms-DS-TDO-Egress-BL**](a-msds-tdoegressbl.md)                                            | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-TDO-входящий трафик — BL**](a-msds-tdoingressbl.md)                                          | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-DS-value-type-Reference-BL**](a-msds-valuetypereferencebl.md)                         | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**MS-дов-Owner-BL**](a-ownerbl.md)                                                        | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Мссфу-30-POSIX-член-of**](a-mssfu30posixmemberof.md)                                   | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**нетбут-SCP-BL**](a-netbootscpbl.md)                                                     | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Не-Security-Member-BL**](a-nonsecuritymemberbl.md)                                      | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**NT-Security-дескриптор**](a-ntsecuritydescriptor.md)                                     | Верно      | [**Начало**](c-top.md)<br/>                |
| [**Obj-расп-имя**](a-distinguishedname.md)                                                 | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Объект — Категория**](a-objectcategory.md)                                                  | True      | [**Начало**](c-top.md)<br/>                |
| [**Объектный класс**](a-objectclass.md)                                                        | Верно      | [**Начало**](c-top.md)<br/>                |
| [**Объект — GUID**](a-objectguid.md)                                                          | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Версия объекта**](a-objectversion.md)                                                    | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Другие хорошо известные объекты**](a-otherwellknownobjects.md)                                  | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Разделяемый атрибут-удаление-список**](a-partialattributedeletionlist.md)                    | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Разделяемый атрибут-set**](a-partialattributeset.md)                                       | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Возможно — подстрочные**](a-possibleinferiors.md)                                            | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Прокси-объект-имя**](a-proxiedobjectname.md)                                           | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Прокси-адреса**](a-proxyaddresses.md)                                                  | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Запрос — политика — BL**](a-querypolicybl.md)                                                   | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**RDN**](a-name.md)                                                                        | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                                    | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**REPL-Уптодате-Vector**](a-repluptodatevector.md)                                         | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Отчеты**](a-directreports.md)                                                           | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Представители — от**](a-repsfrom.md)                                                              | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Представители — кому**](a-repsto.md)                                                                  | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Редакции**](a-revision.md)                                                               | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**SD-Rights-эффективен**](a-sdrightseffective.md)                                           | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Server-Reference-BL**](a-serverreferencebl.md)                                           | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**"Показать" — "Расширенный просмотр"**](a-showinadvancedviewonly.md)                               | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                     | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Структурный объектный класс**](a-structuralobjectclass.md)                                   | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Подразделы-ReFS**](a-subrefs.md)                                                                | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**субсчемасубентри**](a-subschemasubentry.md)                                             | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Системные флаги**](a-systemflags.md)                                                        | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**униксусерпассворд**](a-unixuserpassword.md)                                               | Неверно     | **посиксграуп**                                 |
| [**Пароль пользователя**](a-userpassword.md)                                                      | Неверно     | **посиксграуп**                                 |
| [**USN-изменено**](a-usnchanged.md)                                                          | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Созданный USN**](a-usncreated.md)                                                          | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**USN-DSA-Last-obj-removed**](a-usndsalastobjremoved.md)                                   | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**USN — межсайтовая**](a-usnintersite.md)                                                      | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                                  | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Источник USN**](a-usnsource.md)                                                            | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**WBEM — путь**](a-wbempath.md)                                                              | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**Хорошо известные объекты**](a-wellknownobjects.md)                                             | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**При изменении**](a-whenchanged.md)                                                        | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**При создании**](a-whencreated.md)                                                        | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**WWW — Главная страница**](a-wwwhomepage.md)                                                       | Неверно     | [**Начало**](c-top.md)<br/>                |
| [**WWW-Page — другие**](a-url.md)                                                              | Неверно     | [**Начало**](c-top.md)<br/>                |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[RFC 2307](https://www.ietf.org/rfc/rfc2307.txt)
</dt> </dl>

 

 





