---
title: Класс Application-Process
description: базовый класс X. 500 для приложений Exchange использует только подкласс DSA-Application.
ms.assetid: 3ab2e166-e9db-400b-80c5-e8cd871d407e
ms.tgt_platform: multiple
keywords:
- Схема AD Application-Process класса
- Схема AD класса Аппликатионпроцесс
topic_type:
- apiref
api_name:
- Application-Process
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7b59243d11fa4df829493d9eac0fd400668d5b35745f6696bf7c2b0566ffff1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119702064"
---
# <a name="application-process-class"></a>Класс Application-Process

базовый класс X. 500 для приложений: Exchange использует только подкласс DSA-Application.



| Ввод | Значение |
|-------------------|--------------------------------------|
| CN                | Application-Process                  |
| LDAP-отображаемое имя | аппликатионпроцесс                   |
| Привилегия обновления  | \-                                   |
| Частота обновления  | \-                                   |
| Schema-ID-GUID    | 5fd4250b-1262-11d0-a060-00aa006c33ed |



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
| System-Only                 | Верно                                                                                         |
| Object-Category             | 1                                                                                            |
| По умолчанию — объект — Категория     | \-                                                                                           |
| Governs-Id                  | 2.5.6.11                                                                                     |
| По умолчанию-скрытие значения        | 1                                                                                            |
| RDN-Атри-ID                  | [**Common-Name**](a-cn.md)<br/>                                                       |
| Подкласс                 | [**Вверх**](c-top.md)<br/>                                                              |
| Возможные старшие          | [](c-computer.md)[**Контейнер** компьютера](c-container.md)                               |
| Вспомогательные классы           | \-                                                                                           |
| NT-Security-дескриптор      | О:БАГ: BAD: S:                                                                                 |
| Дескриптор безопасности по умолчанию | D: (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;;D А) (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;; SY) (A;; РПЛКЛОРК;;; СЛУЖБЫ |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-2000-server-attributes"></a>атрибуты сервера Windows 2000

этот класс содержит следующие атрибуты для сервера Windows 2000:



| attribute                                                                 | Обязательный | Унаследован от                                            |
|---------------------------------------------------------------------------|-----------|---------------------------------------------------------|
| [**Описание администратора**](a-admindescription.md)                           | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Имя администратора-отображение**](a-admindisplayname.md)                          | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Allowed-Attributes**](a-allowedattributes.md)                         | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Allowed-Attributes-эффективен**](a-allowedattributeseffective.md)      | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Allowed-Child-classes**](a-allowedchildclasses.md)                    | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Allowed-Child-classes-эффективен**](a-allowedchildclasseseffective.md) | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Плацдарм-Server-List-BL**](a-bridgeheadserverlistbl.md)             | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Каноническое имя**](a-canonicalname.md)                                 | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Common-Name**](a-cn.md)                                               | Верно      | **Приложение — процесс** [ **сверху**](c-top.md)<br/> |
| [**Метка времени создания**](a-createtimestamp.md)                            | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Описание**](a-description.md)                                      | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Отображаемое имя**](a-displayname.md)                                     | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Отображаемое имя — печатаемое**](a-displaynameprintable.md)                  | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**DSA-Signature**](a-dsasignature.md)                                   | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**DS-Core-распространение-данные**](a-dscorepropagationdata.md)               | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Имя расширения**](a-extensionname.md)                                 | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Метки**](a-flags.md)                                                  | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Из записи**](a-fromentry.md)                                         | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)             | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                 | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Тип экземпляра**](a-instancetype.md)                                   | Верно      | [**Вверх**](c-top.md)<br/>                         |
| [**Является критически важным — системный объект**](a-iscriticalsystemobject.md)             | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Удалено**](a-isdeleted.md)                                         | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Входит в состав списка рассылки**](a-memberof.md)                                     | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Имеет права владельца**](a-isprivilegeholder.md)                        | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Последний-известный-родительский**](a-lastknownparent.md)                            | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Локальное имя**](a-l.md)                                              | Нет     | **Процесс приложения**                                 |
| [**Управляемые объекты**](a-managedobjects.md)                               | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**В основном**](a-masteredby.md)                                       | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Метка времени изменения**](a-modifytimestamp.md)                            | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-целостность-дочерняя — количество**](a-ms-ds-consistencychildcount.md)    | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-Consistencу-Guid**](a-ms-ds-consistencyguid.md)                 | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**нетбут-SCP-BL**](a-netbootscpbl.md)                                  | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Не-Security-Member-BL**](a-nonsecuritymemberbl.md)                   | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**NT-Security-дескриптор**](a-ntsecuritydescriptor.md)                  | Верно      | [**Вверх**](c-top.md)<br/>                         |
| [**Obj-расп-имя**](a-distinguishedname.md)                              | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Объект — Категория**](a-objectcategory.md)                               | Верно      | [**Вверх**](c-top.md)<br/>                         |
| [**Объектный класс**](a-objectclass.md)                                     | Верно      | [**Вверх**](c-top.md)<br/>                         |
| [**Объект — GUID**](a-objectguid.md)                                       | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Версия объекта**](a-objectversion.md)                                 | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Организация — имя подразделения**](a-ou.md)                                  | Нет     | **Процесс приложения**                                 |
| [**Другие хорошо известные объекты**](a-otherwellknownobjects.md)               | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Разделяемый атрибут-удаление-список**](a-partialattributedeletionlist.md) | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Разделяемый атрибут-set**](a-partialattributeset.md)                    | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Возможно — подстрочные**](a-possibleinferiors.md)                         | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Прокси-объект-имя**](a-proxiedobjectname.md)                        | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Прокси-адреса**](a-proxyaddresses.md)                               | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Запрос — политика — BL**](a-querypolicybl.md)                                | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**RDN**](a-name.md)                                                     | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                 | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**REPL-Уптодате-Vector**](a-repluptodatevector.md)                      | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Отчеты**](a-directreports.md)                                        | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Представители — от**](a-repsfrom.md)                                           | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Представители — кому**](a-repsto.md)                                               | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Редакции**](a-revision.md)                                            | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**SD-Rights-эффективен**](a-sdrightseffective.md)                        | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**См. также**](a-seealso.md)                                             | Нет     | **Процесс приложения**                                 |
| [**Server-Reference-BL**](a-serverreferencebl.md)                        | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**"Показать" — "Расширенный просмотр"**](a-showinadvancedviewonly.md)            | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Site-Object-BL**](a-siteobjectbl.md)                                  | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Подразделы-ReFS**](a-subrefs.md)                                             | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**субсчемасубентри**](a-subschemasubentry.md)                          | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Системные флаги**](a-systemflags.md)                                     | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**USN-изменено**](a-usnchanged.md)                                       | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Созданный USN**](a-usncreated.md)                                       | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**USN-DSA-Last-obj-removed**](a-usndsalastobjremoved.md)                | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**USN — межсайтовая**](a-usnintersite.md)                                   | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                               | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Источник USN**](a-usnsource.md)                                         | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**WBEM — путь**](a-wbempath.md)                                           | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Хорошо известные объекты**](a-wellknownobjects.md)                          | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**При изменении**](a-whenchanged.md)                                     | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**При создании**](a-whencreated.md)                                     | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**WWW — Главная страница**](a-wwwhomepage.md)                                    | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**WWW-Page — другие**](a-url.md)                                           | Нет     | [**Вверх**](c-top.md)<br/>                         |



## <a name="windows-server-2003"></a>Windows Server 2003

-   [Атрибуты](#windows-server-2003-attributes)



| Ввод | Значение |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Верно                                                                                                                                                    |
| Object-Category             | 1                                                                                                                                                       |
| По умолчанию — объект — Категория     | \-                                                                                                                                                      |
| Governs-Id                  | 2.5.6.11                                                                                                                                                |
| По умолчанию-скрытие значения        | 1                                                                                                                                                       |
| RDN-Атри-ID                  | [**Common-Name**](a-cn.md)<br/>                                                                                                                  |
| Подкласс                 | [**Вверх**](c-top.md)<br/>                                                                                                                         |
| Возможные старшие          | [**Организационная единица**](c-organizationalunit.md) [**Организации**](c-organization.md)[**контейнера**](c-container.md) [**компьютера**](c-computer.md) |
| Вспомогательные классы           | \-                                                                                                                                                      |
| NT-Security-дескриптор      | О:БАГ: BAD: S:                                                                                                                                            |
| Дескриптор безопасности по умолчанию | D: (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;;D А) (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;; SY) (A;; РПЛКЛОРК;;; СЛУЖБЫ                                                            |
| System-Flags                | 0x00000010                                                                                                                                              |



## <a name="windows-server-2003-attributes"></a>Windows Атрибуты сервера 2003

этот класс содержит следующие атрибуты для Windows Server 2003:



| attribute                                                                   | Обязательный | Унаследован от                                            |
|-----------------------------------------------------------------------------|-----------|---------------------------------------------------------|
| [**Описание администратора**](a-admindescription.md)                             | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Имя администратора-отображение**](a-admindisplayname.md)                            | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Allowed-Attributes**](a-allowedattributes.md)                           | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Allowed-Attributes-эффективен**](a-allowedattributeseffective.md)        | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Allowed-Child-classes**](a-allowedchildclasses.md)                      | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Allowed-Child-classes-эффективен**](a-allowedchildclasseseffective.md)   | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Плацдарм-Server-List-BL**](a-bridgeheadserverlistbl.md)               | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Каноническое имя**](a-canonicalname.md)                                   | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Common-Name**](a-cn.md)                                                 | Верно      | **Приложение — процесс** [ **сверху**](c-top.md)<br/> |
| [**Метка времени создания**](a-createtimestamp.md)                              | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Описание**](a-description.md)                                        | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Отображаемое имя**](a-displayname.md)                                       | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Отображаемое имя — печатаемое**](a-displaynameprintable.md)                    | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**DSA-Signature**](a-dsasignature.md)                                     | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**DS-Core-распространение-данные**](a-dscorepropagationdata.md)                 | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Имя расширения**](a-extensionname.md)                                   | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Метки**](a-flags.md)                                                    | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Из записи**](a-fromentry.md)                                           | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Тип экземпляра**](a-instancetype.md)                                     | Верно      | [**Вверх**](c-top.md)<br/>                         |
| [**Является критически важным — системный объект**](a-iscriticalsystemobject.md)               | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Удалено**](a-isdeleted.md)                                           | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Входит в состав списка рассылки**](a-memberof.md)                                       | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Имеет права владельца**](a-isprivilegeholder.md)                          | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Последний-известный-родительский**](a-lastknownparent.md)                              | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Локальное имя**](a-l.md)                                                | Нет     | **Процесс приложения**                                 |
| [**Управляемые объекты**](a-managedobjects.md)                                 | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**В основном**](a-masteredby.md)                                         | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Метка времени изменения**](a-modifytimestamp.md)                              | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-COM-Партитионсетлинк**](a-mscom-partitionsetlink.md)                 | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-COM-Усерлинк**](a-mscom-userlink.md)                                 | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-примерно-Иммед-подчиненные**](a-msds-approx-immed-subordinates.md) | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-целостность-дочерняя — количество**](a-ms-ds-consistencychildcount.md)      | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-Consistencу-Guid**](a-ms-ds-consistencyguid.md)                   | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-Masterd-by**](a-msds-masteredby.md)                              | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)           | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-NC-REPL-курсоры**](a-msds-ncreplcursors.md)                       | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-NC-REPL-Inbound-соседи**](a-msds-ncreplinboundneighbors.md)    | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-NC-REPL-Outbound-соседи**](a-msds-ncreploutboundneighbors.md)  | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-не-Members-BL**](a-msds-nonmembersbl.md)                         | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-Operations-для-AZ-Role-BL**](a-msds-operationsforazrolebl.md)     | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)     | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-REPL-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)              | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-Tasks-для-AZ-Role-BL**](a-msds-tasksforazrolebl.md)               | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)               | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-дов-Owner-BL**](a-ownerbl.md)                                       | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**нетбут-SCP-BL**](a-netbootscpbl.md)                                    | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Не-Security-Member-BL**](a-nonsecuritymemberbl.md)                     | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**NT-Security-дескриптор**](a-ntsecuritydescriptor.md)                    | Верно      | [**Вверх**](c-top.md)<br/>                         |
| [**Obj-расп-имя**](a-distinguishedname.md)                                | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Объект — Категория**](a-objectcategory.md)                                 | Верно      | [**Вверх**](c-top.md)<br/>                         |
| [**Объектный класс**](a-objectclass.md)                                       | Верно      | [**Вверх**](c-top.md)<br/>                         |
| [**Объект — GUID**](a-objectguid.md)                                         | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Версия объекта**](a-objectversion.md)                                   | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Организация — имя подразделения**](a-ou.md)                                    | Нет     | **Процесс приложения**                                 |
| [**Другие хорошо известные объекты**](a-otherwellknownobjects.md)                 | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Разделяемый атрибут-удаление-список**](a-partialattributedeletionlist.md)   | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Разделяемый атрибут-set**](a-partialattributeset.md)                      | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Возможно — подстрочные**](a-possibleinferiors.md)                           | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Прокси-объект-имя**](a-proxiedobjectname.md)                          | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Прокси-адреса**](a-proxyaddresses.md)                                 | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Запрос — политика — BL**](a-querypolicybl.md)                                  | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**RDN**](a-name.md)                                                       | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                   | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**REPL-Уптодате-Vector**](a-repluptodatevector.md)                        | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Отчеты**](a-directreports.md)                                          | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Представители — от**](a-repsfrom.md)                                             | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Представители — кому**](a-repsto.md)                                                 | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Редакции**](a-revision.md)                                              | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**SD-Rights-эффективен**](a-sdrightseffective.md)                          | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**См. также**](a-seealso.md)                                               | Нет     | **Процесс приложения**                                 |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**"Показать" — "Расширенный просмотр"**](a-showinadvancedviewonly.md)              | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Структурный объектный класс**](a-structuralobjectclass.md)                  | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Подразделы-ReFS**](a-subrefs.md)                                               | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**субсчемасубентри**](a-subschemasubentry.md)                            | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Системные флаги**](a-systemflags.md)                                       | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**USN-изменено**](a-usnchanged.md)                                         | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Созданный USN**](a-usncreated.md)                                         | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**USN-DSA-Last-obj-removed**](a-usndsalastobjremoved.md)                  | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**USN — межсайтовая**](a-usnintersite.md)                                     | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                 | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Источник USN**](a-usnsource.md)                                           | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**WBEM — путь**](a-wbempath.md)                                             | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Хорошо известные объекты**](a-wellknownobjects.md)                            | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**При изменении**](a-whenchanged.md)                                       | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**При создании**](a-whencreated.md)                                       | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**WWW — Главная страница**](a-wwwhomepage.md)                                      | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**WWW-Page — другие**](a-url.md)                                             | Нет     | [**Вверх**](c-top.md)<br/>                         |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2

-   [Атрибуты](#windows-server-2003-r2-attributes)



| Ввод | Значение |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Верно                                                                                                                                                    |
| Object-Category             | 1                                                                                                                                                       |
| По умолчанию — объект — Категория     | \-                                                                                                                                                      |
| Governs-Id                  | 2.5.6.11                                                                                                                                                |
| По умолчанию-скрытие значения        | 1                                                                                                                                                       |
| RDN-Атри-ID                  | [**Common-Name**](a-cn.md)<br/>                                                                                                                  |
| Подкласс                 | [**Вверх**](c-top.md)<br/>                                                                                                                         |
| Возможные старшие          | [**Организационная единица**](c-organizationalunit.md) [**Организации**](c-organization.md)[**контейнера**](c-container.md) [**компьютера**](c-computer.md) |
| Вспомогательные классы           | \-                                                                                                                                                      |
| NT-Security-дескриптор      | О:БАГ: BAD: S:                                                                                                                                            |
| Дескриптор безопасности по умолчанию | D: (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;;D А) (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;; SY) (A;; РПЛКЛОРК;;; СЛУЖБЫ                                                            |
| System-Flags                | 0x00000010                                                                                                                                              |



## <a name="windows-server-2003-r2-attributes"></a>Windows Атрибуты сервера 2003 R2

этот класс содержит следующие атрибуты для Windows Server 2003 R2:



| attribute                                                                   | Обязательный | Унаследован от                                            |
|-----------------------------------------------------------------------------|-----------|---------------------------------------------------------|
| [**Описание администратора**](a-admindescription.md)                             | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Имя администратора-отображение**](a-admindisplayname.md)                            | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Allowed-Attributes**](a-allowedattributes.md)                           | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Allowed-Attributes-эффективен**](a-allowedattributeseffective.md)        | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Allowed-Child-classes**](a-allowedchildclasses.md)                      | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Allowed-Child-classes-эффективен**](a-allowedchildclasseseffective.md)   | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Плацдарм-Server-List-BL**](a-bridgeheadserverlistbl.md)               | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Каноническое имя**](a-canonicalname.md)                                   | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Common-Name**](a-cn.md)                                                 | Верно      | **Приложение — процесс** [ **сверху**](c-top.md)<br/> |
| [**Метка времени создания**](a-createtimestamp.md)                              | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Описание**](a-description.md)                                        | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Отображаемое имя**](a-displayname.md)                                       | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Отображаемое имя — печатаемое**](a-displaynameprintable.md)                    | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**DSA-Signature**](a-dsasignature.md)                                     | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**DS-Core-распространение-данные**](a-dscorepropagationdata.md)                 | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Имя расширения**](a-extensionname.md)                                   | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Метки**](a-flags.md)                                                    | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Из записи**](a-fromentry.md)                                           | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Тип экземпляра**](a-instancetype.md)                                     | Верно      | [**Вверх**](c-top.md)<br/>                         |
| [**Является критически важным — системный объект**](a-iscriticalsystemobject.md)               | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Удалено**](a-isdeleted.md)                                           | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Входит в состав списка рассылки**](a-memberof.md)                                       | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Имеет права владельца**](a-isprivilegeholder.md)                          | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Последний-известный-родительский**](a-lastknownparent.md)                              | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Локальное имя**](a-l.md)                                                | Нет     | **Процесс приложения**                                 |
| [**Управляемые объекты**](a-managedobjects.md)                                 | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**В основном**](a-masteredby.md)                                         | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Метка времени изменения**](a-modifytimestamp.md)                              | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-COM-Партитионсетлинк**](a-mscom-partitionsetlink.md)                 | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-COM-Усерлинк**](a-mscom-userlink.md)                                 | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DFSR-Компутерреференцебл**](a-msdfsr-computerreferencebl.md)         | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DFSR-Мемберреференцебл**](a-msdfsr-memberreferencebl.md)             | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-примерно-Иммед-подчиненные**](a-msds-approx-immed-subordinates.md) | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-целостность-дочерняя — количество**](a-ms-ds-consistencychildcount.md)      | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-Consistencу-Guid**](a-ms-ds-consistencyguid.md)                   | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-Masterd-by**](a-msds-masteredby.md)                              | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)           | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-NC-REPL-курсоры**](a-msds-ncreplcursors.md)                       | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-NC-REPL-Inbound-соседи**](a-msds-ncreplinboundneighbors.md)    | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-NC-REPL-Outbound-соседи**](a-msds-ncreploutboundneighbors.md)  | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-не-Members-BL**](a-msds-nonmembersbl.md)                         | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-Operations-для-AZ-Role-BL**](a-msds-operationsforazrolebl.md)     | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)     | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-REPL-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)              | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-Tasks-для-AZ-Role-BL**](a-msds-tasksforazrolebl.md)               | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)               | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-дов-Owner-BL**](a-ownerbl.md)                                       | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Мссфу-30-POSIX-член-of**](a-mssfu30posixmemberof.md)                  | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**нетбут-SCP-BL**](a-netbootscpbl.md)                                    | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Не-Security-Member-BL**](a-nonsecuritymemberbl.md)                     | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**NT-Security-дескриптор**](a-ntsecuritydescriptor.md)                    | Верно      | [**Вверх**](c-top.md)<br/>                         |
| [**Obj-расп-имя**](a-distinguishedname.md)                                | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Объект — Категория**](a-objectcategory.md)                                 | Верно      | [**Вверх**](c-top.md)<br/>                         |
| [**Объектный класс**](a-objectclass.md)                                       | Верно      | [**Вверх**](c-top.md)<br/>                         |
| [**Объект — GUID**](a-objectguid.md)                                         | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Версия объекта**](a-objectversion.md)                                   | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Организация — имя подразделения**](a-ou.md)                                    | Нет     | **Процесс приложения**                                 |
| [**Другие хорошо известные объекты**](a-otherwellknownobjects.md)                 | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Разделяемый атрибут-удаление-список**](a-partialattributedeletionlist.md)   | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Разделяемый атрибут-set**](a-partialattributeset.md)                      | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Возможно — подстрочные**](a-possibleinferiors.md)                           | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Прокси-объект-имя**](a-proxiedobjectname.md)                          | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Прокси-адреса**](a-proxyaddresses.md)                                 | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Запрос — политика — BL**](a-querypolicybl.md)                                  | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**RDN**](a-name.md)                                                       | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                   | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**REPL-Уптодате-Vector**](a-repluptodatevector.md)                        | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Отчеты**](a-directreports.md)                                          | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Представители — от**](a-repsfrom.md)                                             | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Представители — кому**](a-repsto.md)                                                 | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Редакции**](a-revision.md)                                              | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**SD-Rights-эффективен**](a-sdrightseffective.md)                          | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**См. также**](a-seealso.md)                                               | Нет     | **Процесс приложения**                                 |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**"Показать" — "Расширенный просмотр"**](a-showinadvancedviewonly.md)              | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Структурный объектный класс**](a-structuralobjectclass.md)                  | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Подразделы-ReFS**](a-subrefs.md)                                               | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**субсчемасубентри**](a-subschemasubentry.md)                            | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Системные флаги**](a-systemflags.md)                                       | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**USN-изменено**](a-usnchanged.md)                                         | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Созданный USN**](a-usncreated.md)                                         | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**USN-DSA-Last-obj-removed**](a-usndsalastobjremoved.md)                  | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**USN — межсайтовая**](a-usnintersite.md)                                     | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                 | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Источник USN**](a-usnsource.md)                                           | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**WBEM — путь**](a-wbempath.md)                                             | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Хорошо известные объекты**](a-wellknownobjects.md)                            | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**При изменении**](a-whenchanged.md)                                       | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**При создании**](a-whencreated.md)                                       | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**WWW — Главная страница**](a-wwwhomepage.md)                                      | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**WWW-Page — другие**](a-url.md)                                             | Нет     | [**Вверх**](c-top.md)<br/>                         |



## <a name="windows-server-2008"></a>Windows Server 2008

-   [Атрибуты](#windows-server-2008-attributes)



| Ввод | Значение |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Верно                                                                                                                                                    |
| Object-Category             | 1                                                                                                                                                       |
| По умолчанию — объект — Категория     | \-                                                                                                                                                      |
| Governs-Id                  | 2.5.6.11                                                                                                                                                |
| По умолчанию-скрытие значения        | 1                                                                                                                                                       |
| RDN-Атри-ID                  | [**Common-Name**](a-cn.md)<br/>                                                                                                                  |
| Подкласс                 | [**Вверх**](c-top.md)<br/>                                                                                                                         |
| Возможные старшие          | [**Организационная единица**](c-organizationalunit.md) [**Организации**](c-organization.md)[**контейнера**](c-container.md) [**компьютера**](c-computer.md) |
| Вспомогательные классы           | \-                                                                                                                                                      |
| NT-Security-дескриптор      | О:БАГ: BAD: S:                                                                                                                                            |
| Дескриптор безопасности по умолчанию | D: (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;;D А) (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;; SY) (A;; РПЛКЛОРК;;; СЛУЖБЫ                                                            |
| System-Flags                | 0x00000010                                                                                                                                              |



## <a name="windows-server-2008-attributes"></a>Windows Атрибуты сервера 2008

этот класс содержит следующие атрибуты для Windows Server 2008:



| attribute                                                                      | Обязательный | Унаследован от                                            |
|--------------------------------------------------------------------------------|-----------|---------------------------------------------------------|
| [**Описание администратора**](a-admindescription.md)                                | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Имя администратора-отображение**](a-admindisplayname.md)                               | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Allowed-Attributes**](a-allowedattributes.md)                              | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Allowed-Attributes-эффективен**](a-allowedattributeseffective.md)           | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Allowed-Child-classes**](a-allowedchildclasses.md)                         | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Allowed-Child-classes-эффективен**](a-allowedchildclasseseffective.md)      | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Плацдарм-Server-List-BL**](a-bridgeheadserverlistbl.md)                  | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Каноническое имя**](a-canonicalname.md)                                      | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Common-Name**](a-cn.md)                                                    | Верно      | **Приложение — процесс** [ **сверху**](c-top.md)<br/> |
| [**Метка времени создания**](a-createtimestamp.md)                                 | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Описание**](a-description.md)                                           | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Отображаемое имя**](a-displayname.md)                                          | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Отображаемое имя — печатаемое**](a-displaynameprintable.md)                       | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**DSA-Signature**](a-dsasignature.md)                                        | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**DS-Core-распространение-данные**](a-dscorepropagationdata.md)                    | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Имя расширения**](a-extensionname.md)                                      | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Метки**](a-flags.md)                                                       | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Из записи**](a-fromentry.md)                                              | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                  | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                      | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                     | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Тип экземпляра**](a-instancetype.md)                                        | Верно      | [**Вверх**](c-top.md)<br/>                         |
| [**Является критически важным — системный объект**](a-iscriticalsystemobject.md)                  | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Удалено**](a-isdeleted.md)                                              | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Входит в состав списка рассылки**](a-memberof.md)                                          | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Имеет права владельца**](a-isprivilegeholder.md)                             | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Последний-известный-родительский**](a-lastknownparent.md)                                 | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Локальное имя**](a-l.md)                                                   | Нет     | **Процесс приложения**                                 |
| [**Управляемые объекты**](a-managedobjects.md)                                    | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**В основном**](a-masteredby.md)                                            | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Метка времени изменения**](a-modifytimestamp.md)                                 | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-COM-Партитионсетлинк**](a-mscom-partitionsetlink.md)                    | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-COM-Усерлинк**](a-mscom-userlink.md)                                    | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DFSR-Компутерреференцебл**](a-msdfsr-computerreferencebl.md)            | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DFSR-Мемберреференцебл**](a-msdfsr-memberreferencebl.md)                | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-примерно-Иммед-подчиненные**](a-msds-approx-immed-subordinates.md)    | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-Аусентикатедто-Аккаунтлист**](a-msds-authenticatedtoaccountlist.md) | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-целостность-дочерняя — количество**](a-ms-ds-consistencychildcount.md)         | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-Consistencу-Guid**](a-ms-ds-consistencyguid.md)                      | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS--домен — для**](a-msds-isdomainfor.md)                              | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-является-Full-реплика для**](a-msds-isfullreplicafor.md)                   | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-является-partial-реплика для**](a-msds-ispartialreplicafor.md)             | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                            | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-Masterd-by**](a-msds-masteredby.md)                                 | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)              | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-NC-REPL-курсоры**](a-msds-ncreplcursors.md)                          | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-NC-REPL-Inbound-соседи**](a-msds-ncreplinboundneighbors.md)       | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-NC-REPL-Outbound-соседи**](a-msds-ncreploutboundneighbors.md)     | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)  | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-NC-Type**](a-msds-nctype.md)                                         | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-не-Members-BL**](a-msds-nonmembersbl.md)                            | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                  | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-Operations-для-AZ-Role-BL**](a-msds-operationsforazrolebl.md)        | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)        | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-Principal-Name**](a-msds-principalname.md)                           | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-PSO — применяется**](a-msds-psoapplied.md)                                 | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-REPL-Attribute-Meta-Data**](a-msds-replattributemetadata.md)         | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)                 | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-выявил-DSA**](a-msds-revealeddsas.md)                             | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-выводит-List-BL**](a-msds-revealedlistbl.md)                        | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-Tasks-для-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                  | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                  | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-дов-Owner-BL**](a-ownerbl.md)                                          | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Мссфу-30-POSIX-член-of**](a-mssfu30posixmemberof.md)                     | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**нетбут-SCP-BL**](a-netbootscpbl.md)                                       | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Не-Security-Member-BL**](a-nonsecuritymemberbl.md)                        | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**NT-Security-дескриптор**](a-ntsecuritydescriptor.md)                       | Верно      | [**Вверх**](c-top.md)<br/>                         |
| [**Obj-расп-имя**](a-distinguishedname.md)                                   | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Объект — Категория**](a-objectcategory.md)                                    | Верно      | [**Вверх**](c-top.md)<br/>                         |
| [**Объектный класс**](a-objectclass.md)                                          | Верно      | [**Вверх**](c-top.md)<br/>                         |
| [**Объект — GUID**](a-objectguid.md)                                            | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Версия объекта**](a-objectversion.md)                                      | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Организация — имя подразделения**](a-ou.md)                                       | Нет     | **Процесс приложения**                                 |
| [**Другие хорошо известные объекты**](a-otherwellknownobjects.md)                    | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Разделяемый атрибут-удаление-список**](a-partialattributedeletionlist.md)      | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Разделяемый атрибут-set**](a-partialattributeset.md)                         | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Возможно — подстрочные**](a-possibleinferiors.md)                              | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Прокси-объект-имя**](a-proxiedobjectname.md)                             | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Прокси-адреса**](a-proxyaddresses.md)                                    | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Запрос — политика — BL**](a-querypolicybl.md)                                     | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**RDN**](a-name.md)                                                          | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                      | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**REPL-Уптодате-Vector**](a-repluptodatevector.md)                           | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Отчеты**](a-directreports.md)                                             | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Представители — от**](a-repsfrom.md)                                                | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Представители — кому**](a-repsto.md)                                                    | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Редакции**](a-revision.md)                                                 | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**SD-Rights-эффективен**](a-sdrightseffective.md)                             | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**См. также**](a-seealso.md)                                                  | Нет     | **Процесс приложения**                                 |
| [**Server-Reference-BL**](a-serverreferencebl.md)                             | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**"Показать" — "Расширенный просмотр"**](a-showinadvancedviewonly.md)                 | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Site-Object-BL**](a-siteobjectbl.md)                                       | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Структурный объектный класс**](a-structuralobjectclass.md)                     | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Подразделы-ReFS**](a-subrefs.md)                                                  | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**субсчемасубентри**](a-subschemasubentry.md)                               | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Системные флаги**](a-systemflags.md)                                          | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**USN-изменено**](a-usnchanged.md)                                            | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Созданный USN**](a-usncreated.md)                                            | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**USN-DSA-Last-obj-removed**](a-usndsalastobjremoved.md)                     | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**USN — межсайтовая**](a-usnintersite.md)                                        | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                    | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Источник USN**](a-usnsource.md)                                              | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**WBEM — путь**](a-wbempath.md)                                                | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Хорошо известные объекты**](a-wellknownobjects.md)                               | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**При изменении**](a-whenchanged.md)                                          | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**При создании**](a-whencreated.md)                                          | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**WWW — Главная страница**](a-wwwhomepage.md)                                         | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**WWW-Page — другие**](a-url.md)                                                | Нет     | [**Вверх**](c-top.md)<br/>                         |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2

-   [Атрибуты](#windows-server-2008-r2-attributes)



| Ввод | Значение |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Верно                                                                                                                                                    |
| Object-Category             | 1                                                                                                                                                       |
| По умолчанию — объект — Категория     | \-                                                                                                                                                      |
| Governs-Id                  | 2.5.6.11                                                                                                                                                |
| По умолчанию-скрытие значения        | 1                                                                                                                                                       |
| RDN-Атри-ID                  | [**Common-Name**](a-cn.md)<br/>                                                                                                                  |
| Подкласс                 | [**Вверх**](c-top.md)<br/>                                                                                                                         |
| Возможные старшие          | [**Организационная единица**](c-organizationalunit.md) [**Организации**](c-organization.md)[**контейнера**](c-container.md) [**компьютера**](c-computer.md) |
| Вспомогательные классы           | \-                                                                                                                                                      |
| NT-Security-дескриптор      | О:БАГ: BAD: S:                                                                                                                                            |
| Дескриптор безопасности по умолчанию | D: (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;;D А) (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;; SY) (A;; РПЛКЛОРК;;; СЛУЖБЫ                                                            |
| System-Flags                | 0x00000010                                                                                                                                              |



## <a name="windows-server-2008-r2-attributes"></a>Windows Атрибуты сервера 2008 R2

этот класс содержит следующие атрибуты для Windows Server 2008 R2:



| attribute                                                                        | Обязательный | Унаследован от                                            |
|----------------------------------------------------------------------------------|-----------|---------------------------------------------------------|
| [**Описание администратора**](a-admindescription.md)                                  | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Имя администратора-отображение**](a-admindisplayname.md)                                 | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Allowed-Attributes**](a-allowedattributes.md)                                | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Allowed-Attributes-эффективен**](a-allowedattributeseffective.md)             | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Allowed-Child-classes**](a-allowedchildclasses.md)                           | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Allowed-Child-classes-эффективен**](a-allowedchildclasseseffective.md)        | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Плацдарм-Server-List-BL**](a-bridgeheadserverlistbl.md)                    | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Каноническое имя**](a-canonicalname.md)                                        | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Common-Name**](a-cn.md)                                                      | Верно      | **Приложение — процесс** [ **сверху**](c-top.md)<br/> |
| [**Метка времени создания**](a-createtimestamp.md)                                   | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Описание**](a-description.md)                                             | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Отображаемое имя**](a-displayname.md)                                            | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Отображаемое имя — печатаемое**](a-displaynameprintable.md)                         | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**DSA-Signature**](a-dsasignature.md)                                          | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**DS-Core-распространение-данные**](a-dscorepropagationdata.md)                      | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Имя расширения**](a-extensionname.md)                                        | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Метки**](a-flags.md)                                                         | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Из записи**](a-fromentry.md)                                                | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                    | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                        | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                       | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Тип экземпляра**](a-instancetype.md)                                          | Верно      | [**Вверх**](c-top.md)<br/>                         |
| [**Является критически важным — системный объект**](a-iscriticalsystemobject.md)                    | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Удалено**](a-isdeleted.md)                                                | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Входит в состав списка рассылки**](a-memberof.md)                                            | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Имеет права владельца**](a-isprivilegeholder.md)                               | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Является перезапущенным**](a-isrecycled.md)                                              | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Последний-известный-родительский**](a-lastknownparent.md)                                   | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Локальное имя**](a-l.md)                                                     | Нет     | **Процесс приложения**                                 |
| [**Управляемые объекты**](a-managedobjects.md)                                      | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**В основном**](a-masteredby.md)                                              | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Метка времени изменения**](a-modifytimestamp.md)                                   | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-COM-Партитионсетлинк**](a-mscom-partitionsetlink.md)                      | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-COM-Усерлинк**](a-mscom-userlink.md)                                      | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DFSR-Компутерреференцебл**](a-msdfsr-computerreferencebl.md)              | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DFSR-Мемберреференцебл**](a-msdfsr-memberreferencebl.md)                  | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-примерно-Иммед-подчиненные**](a-msds-approx-immed-subordinates.md)      | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-Аусентикатедто-Аккаунтлист**](a-msds-authenticatedtoaccountlist.md)   | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-целостность-дочерняя — количество**](a-ms-ds-consistencychildcount.md)           | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-Consistencу-Guid**](a-ms-ds-consistencyguid.md)                        | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Поддержка MS-DS-Feature-BL**](a-msds-enabledfeaturebl.md)                      | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)             | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS--домен — для**](a-msds-isdomainfor.md)                                | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-является-Full-реплика для**](a-msds-isfullreplicafor.md)                     | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-является-partial-реплика для**](a-msds-ispartialreplicafor.md)               | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                              | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                              | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-локально-эффективное удаление — время**](a-msds-localeffectivedeletiontime.md) | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-Local-эффективен — время перезапуска**](a-msds-localeffectiverecycletime.md)   | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-Masterd-by**](a-msds-masteredby.md)                                   | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)                | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-NC-REPL-курсоры**](a-msds-ncreplcursors.md)                            | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-NC-REPL-Inbound-соседи**](a-msds-ncreplinboundneighbors.md)         | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-NC-REPL-Outbound-соседи**](a-msds-ncreploutboundneighbors.md)       | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)    | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-NC-Type**](a-msds-nctype.md)                                           | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-не-Members-BL**](a-msds-nonmembersbl.md)                              | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                    | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-Оидтограуп-Link-BL**](a-msds-oidtogrouplinkbl.md)                      | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-Operations-для-AZ-Role-BL**](a-msds-operationsforazrolebl.md)          | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)          | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-Principal-Name**](a-msds-principalname.md)                             | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-PSO — применяется**](a-msds-psoapplied.md)                                   | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-REPL-Attribute-Meta-Data**](a-msds-replattributemetadata.md)           | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)                   | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-выявил-DSA**](a-msds-revealeddsas.md)                               | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-выводит-List-BL**](a-msds-revealedlistbl.md)                          | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-Tasks-для-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                    | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                    | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-дов-Owner-BL**](a-ownerbl.md)                                            | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Мссфу-30-POSIX-член-of**](a-mssfu30posixmemberof.md)                       | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**нетбут-SCP-BL**](a-netbootscpbl.md)                                         | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Не-Security-Member-BL**](a-nonsecuritymemberbl.md)                          | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**NT-Security-дескриптор**](a-ntsecuritydescriptor.md)                         | Верно      | [**Вверх**](c-top.md)<br/>                         |
| [**Obj-расп-имя**](a-distinguishedname.md)                                     | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Объект — Категория**](a-objectcategory.md)                                      | Верно      | [**Вверх**](c-top.md)<br/>                         |
| [**Объектный класс**](a-objectclass.md)                                            | Верно      | [**Вверх**](c-top.md)<br/>                         |
| [**Объект — GUID**](a-objectguid.md)                                              | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Версия объекта**](a-objectversion.md)                                        | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Организация — имя подразделения**](a-ou.md)                                         | Нет     | **Процесс приложения**                                 |
| [**Другие хорошо известные объекты**](a-otherwellknownobjects.md)                      | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Разделяемый атрибут-удаление-список**](a-partialattributedeletionlist.md)        | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Разделяемый атрибут-set**](a-partialattributeset.md)                           | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Возможно — подстрочные**](a-possibleinferiors.md)                                | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Прокси-объект-имя**](a-proxiedobjectname.md)                               | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Прокси-адреса**](a-proxyaddresses.md)                                      | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Запрос — политика — BL**](a-querypolicybl.md)                                       | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**RDN**](a-name.md)                                                            | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                        | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**REPL-Уптодате-Vector**](a-repluptodatevector.md)                             | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Отчеты**](a-directreports.md)                                               | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Представители — от**](a-repsfrom.md)                                                  | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Представители — кому**](a-repsto.md)                                                      | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Редакции**](a-revision.md)                                                   | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**SD-Rights-эффективен**](a-sdrightseffective.md)                               | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**См. также**](a-seealso.md)                                                    | Нет     | **Процесс приложения**                                 |
| [**Server-Reference-BL**](a-serverreferencebl.md)                               | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**"Показать" — "Расширенный просмотр"**](a-showinadvancedviewonly.md)                   | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Site-Object-BL**](a-siteobjectbl.md)                                         | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Структурный объектный класс**](a-structuralobjectclass.md)                       | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Подразделы-ReFS**](a-subrefs.md)                                                    | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**субсчемасубентри**](a-subschemasubentry.md)                                 | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Системные флаги**](a-systemflags.md)                                            | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**USN-изменено**](a-usnchanged.md)                                              | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Созданный USN**](a-usncreated.md)                                              | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**USN-DSA-Last-obj-removed**](a-usndsalastobjremoved.md)                       | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**USN — межсайтовая**](a-usnintersite.md)                                          | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                      | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Источник USN**](a-usnsource.md)                                                | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**WBEM — путь**](a-wbempath.md)                                                  | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Хорошо известные объекты**](a-wellknownobjects.md)                                 | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**При изменении**](a-whenchanged.md)                                            | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**При создании**](a-whencreated.md)                                            | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**WWW — Главная страница**](a-wwwhomepage.md)                                           | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**WWW-Page — другие**](a-url.md)                                                  | Нет     | [**Вверх**](c-top.md)<br/>                         |



## <a name="windows-server-2012"></a>Windows Server 2012

-   [Атрибуты](#windows-server-2012-attributes)



| Ввод | Значение |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Верно                                                                                                                                                    |
| Object-Category             | 1                                                                                                                                                       |
| По умолчанию — объект — Категория     | \-                                                                                                                                                      |
| Governs-Id                  | 2.5.6.11                                                                                                                                                |
| По умолчанию-скрытие значения        | 1                                                                                                                                                       |
| RDN-Атри-ID                  | [**Common-Name**](a-cn.md)<br/>                                                                                                                  |
| Подкласс                 | [**Вверх**](c-top.md)<br/>                                                                                                                         |
| Возможные старшие          | [**Организационная единица**](c-organizationalunit.md) [**Организации**](c-organization.md)[**контейнера**](c-container.md) [**компьютера**](c-computer.md) |
| Вспомогательные классы           | \-                                                                                                                                                      |
| NT-Security-дескриптор      | О:БАГ: BAD: S:                                                                                                                                            |
| Дескриптор безопасности по умолчанию | D: (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;;D А) (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;; SY) (A;; РПЛКЛОРК;;; СЛУЖБЫ                                                            |
| System-Flags                | 0x00000010                                                                                                                                              |



## <a name="windows-server-2012-attributes"></a>Windows Server 2012 Атрибута

Этот класс содержит следующие атрибуты для Windows Server 2012:



| attribute                                                                                    | Обязательный | Унаследован от                                            |
|----------------------------------------------------------------------------------------------|-----------|---------------------------------------------------------|
| [**Описание администратора**](a-admindescription.md)                                              | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Имя администратора-отображение**](a-admindisplayname.md)                                             | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Allowed-Attributes**](a-allowedattributes.md)                                            | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Allowed-Attributes-эффективен**](a-allowedattributeseffective.md)                         | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Allowed-Child-classes**](a-allowedchildclasses.md)                                       | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Allowed-Child-classes-эффективен**](a-allowedchildclasseseffective.md)                    | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Плацдарм-Server-List-BL**](a-bridgeheadserverlistbl.md)                                | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Каноническое имя**](a-canonicalname.md)                                                    | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Common-Name**](a-cn.md)                                                                  | Верно      | **Приложение — процесс** [ **сверху**](c-top.md)<br/> |
| [**Метка времени создания**](a-createtimestamp.md)                                               | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Описание**](a-description.md)                                                         | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Отображаемое имя**](a-displayname.md)                                                        | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Отображаемое имя — печатаемое**](a-displaynameprintable.md)                                     | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**DSA-Signature**](a-dsasignature.md)                                                      | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**DS-Core-распространение-данные**](a-dscorepropagationdata.md)                                  | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Имя расширения**](a-extensionname.md)                                                    | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Метки**](a-flags.md)                                                                     | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Из записи**](a-fromentry.md)                                                            | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                                | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                                    | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                                   | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Тип экземпляра**](a-instancetype.md)                                                      | Верно      | [**Вверх**](c-top.md)<br/>                         |
| [**Является критически важным — системный объект**](a-iscriticalsystemobject.md)                                | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Удалено**](a-isdeleted.md)                                                            | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Входит в состав списка рассылки**](a-memberof.md)                                                        | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Имеет права владельца**](a-isprivilegeholder.md)                                           | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Является перезапущенным**](a-isrecycled.md)                                                          | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Последний-известный-родительский**](a-lastknownparent.md)                                               | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Локальное имя**](a-l.md)                                                                 | Нет     | **Процесс приложения**                                 |
| [**Управляемые объекты**](a-managedobjects.md)                                                  | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**В основном**](a-masteredby.md)                                                          | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Метка времени изменения**](a-modifytimestamp.md)                                               | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-COM-Партитионсетлинк**](a-mscom-partitionsetlink.md)                                  | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-COM-Усерлинк**](a-mscom-userlink.md)                                                  | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DFSR-Компутерреференцебл**](a-msdfsr-computerreferencebl.md)                          | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DFSR-Мемберреференцебл**](a-msdfsr-memberreferencebl.md)                              | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-примерно-Иммед-подчиненные**](a-msds-approx-immed-subordinates.md)                  | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-Аусентикатедто-Аккаунтлист**](a-msds-authenticatedtoaccountlist.md)               | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-ClaimSet-shares-возможные значения-with-BL**](a-msds-claimsharespossiblevalueswithbl.md) | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-целостность-дочерняя — количество**](a-ms-ds-consistencychildcount.md)                       | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-Consistencу-Guid**](a-ms-ds-consistencyguid.md)                                    | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Поддержка MS-DS-Feature-BL**](a-msds-enabledfeaturebl.md)                                  | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)                         | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS--домен — для**](a-msds-isdomainfor.md)                                            | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-является-Full-реплика для**](a-msds-isfullreplicafor.md)                                 | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-является-partial-реплика для**](a-msds-ispartialreplicafor.md)                           | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-является-PRIMARY-Computer-для**](a-msds-isprimarycomputerfor.md)                         | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                          | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                                          | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-локально-эффективное удаление — время**](a-msds-localeffectivedeletiontime.md)             | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-Local-эффективен — время перезапуска**](a-msds-localeffectiverecycletime.md)               | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-Masterd-by**](a-msds-masteredby.md)                                               | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)                            | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-Members-of-Resource-Property-List-BL**](a-msds-membersofresourcepropertylistbl.md) | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-NC-REPL-курсоры**](a-msds-ncreplcursors.md)                                        | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-NC-REPL-Inbound-соседи**](a-msds-ncreplinboundneighbors.md)                     | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-NC-REPL-Outbound-соседи**](a-msds-ncreploutboundneighbors.md)                   | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)                | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-NC-Type**](a-msds-nctype.md)                                                       | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-не-Members-BL**](a-msds-nonmembersbl.md)                                          | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                                | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-Оидтограуп-Link-BL**](a-msds-oidtogrouplinkbl.md)                                  | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-Operations-для-AZ-Role-BL**](a-msds-operationsforazrolebl.md)                      | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)                      | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-Principal-Name**](a-msds-principalname.md)                                         | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-PSO — применяется**](a-msds-psoapplied.md)                                               | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-REPL-Attribute-Meta-Data**](a-msds-replattributemetadata.md)                       | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)                               | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-выявил-DSA**](a-msds-revealeddsas.md)                                           | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-выводит-List-BL**](a-msds-revealedlistbl.md)                                      | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-Tasks-для-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                                | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                                | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**ms-DS-TDO-Egress-BL**](a-msds-tdoegressbl.md)                                            | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-TDO-входящий трафик — BL**](a-msds-tdoingressbl.md)                                          | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-DS-value-type-Reference-BL**](a-msds-valuetypereferencebl.md)                         | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**MS-дов-Owner-BL**](a-ownerbl.md)                                                        | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Мссфу-30-POSIX-член-of**](a-mssfu30posixmemberof.md)                                   | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**нетбут-SCP-BL**](a-netbootscpbl.md)                                                     | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Не-Security-Member-BL**](a-nonsecuritymemberbl.md)                                      | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**NT-Security-дескриптор**](a-ntsecuritydescriptor.md)                                     | Верно      | [**Вверх**](c-top.md)<br/>                         |
| [**Obj-расп-имя**](a-distinguishedname.md)                                                 | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Объект — Категория**](a-objectcategory.md)                                                  | Верно      | [**Вверх**](c-top.md)<br/>                         |
| [**Объектный класс**](a-objectclass.md)                                                        | Верно      | [**Вверх**](c-top.md)<br/>                         |
| [**Объект — GUID**](a-objectguid.md)                                                          | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Версия объекта**](a-objectversion.md)                                                    | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Организация — имя подразделения**](a-ou.md)                                                     | Нет     | **Процесс приложения**                                 |
| [**Другие хорошо известные объекты**](a-otherwellknownobjects.md)                                  | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Разделяемый атрибут-удаление-список**](a-partialattributedeletionlist.md)                    | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Разделяемый атрибут-set**](a-partialattributeset.md)                                       | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Возможно — подстрочные**](a-possibleinferiors.md)                                            | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Прокси-объект-имя**](a-proxiedobjectname.md)                                           | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Прокси-адреса**](a-proxyaddresses.md)                                                  | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Запрос — политика — BL**](a-querypolicybl.md)                                                   | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**RDN**](a-name.md)                                                                        | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                                    | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**REPL-Уптодате-Vector**](a-repluptodatevector.md)                                         | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Отчеты**](a-directreports.md)                                                           | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Представители — от**](a-repsfrom.md)                                                              | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Представители — кому**](a-repsto.md)                                                                  | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Редакции**](a-revision.md)                                                               | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**SD-Rights-эффективен**](a-sdrightseffective.md)                                           | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**См. также**](a-seealso.md)                                                                | Нет     | **Процесс приложения**                                 |
| [**Server-Reference-BL**](a-serverreferencebl.md)                                           | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**"Показать" — "Расширенный просмотр"**](a-showinadvancedviewonly.md)                               | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                     | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Структурный объектный класс**](a-structuralobjectclass.md)                                   | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Подразделы-ReFS**](a-subrefs.md)                                                                | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**субсчемасубентри**](a-subschemasubentry.md)                                             | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Системные флаги**](a-systemflags.md)                                                        | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**USN-изменено**](a-usnchanged.md)                                                          | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Созданный USN**](a-usncreated.md)                                                          | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**USN-DSA-Last-obj-removed**](a-usndsalastobjremoved.md)                                   | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**USN — межсайтовая**](a-usnintersite.md)                                                      | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                                  | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Источник USN**](a-usnsource.md)                                                            | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**WBEM — путь**](a-wbempath.md)                                                              | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**Хорошо известные объекты**](a-wellknownobjects.md)                                             | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**При изменении**](a-whenchanged.md)                                                        | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**При создании**](a-whencreated.md)                                                        | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**WWW — Главная страница**](a-wwwhomepage.md)                                                       | Нет     | [**Вверх**](c-top.md)<br/>                         |
| [**WWW-Page — другие**](a-url.md)                                                              | Нет     | [**Вверх**](c-top.md)<br/>                         |



 

 





