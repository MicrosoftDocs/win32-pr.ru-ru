---
title: Класс Trusted-Domain
description: Объект, представляющий домен, являющийся доверенным (или доверенным) локальным доменом.
ms.assetid: dd455d89-2ad0-4bc7-a84e-449b4c334bd2
ms.tgt_platform: multiple
keywords:
- Схема AD Trusted-Domain класса
- Схема AD класса Трустеддомаин
topic_type:
- apiref
api_name:
- Trusted-Domain
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0810bde186aeacc9b7507102049f3cbdbcb084d1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804475"
---
# <a name="trusted-domain-class"></a>Класс Trusted-Domain

Объект, представляющий домен, являющийся доверенным (или доверенным) локальным доменом.



| Ввод | Значение |
|-------------------|--------------------------------------|
| CN                | Trusted-Domain                       |
| LDAP-отображаемое имя | трустеддомаин                        |
| Привилегия обновления  | Это значение задается системой.     |
| Частота обновления  | При создании нового доверия.         |
| Schema-ID-GUID    | bf967ab8-0de6-11d0-a285-00aa003049e2 |



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
| System-Only                 | Неверно                                                                                        |
| Object-Category             | 1                                                                                            |
| По умолчанию — объект — Категория     | \-                                                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.34                                                                        |
| По умолчанию-скрытие значения        | 1                                                                                            |
| RDN-Атри-ID                  | [**Common-Name**](a-cn.md)<br/>                                                       |
| Подкласс                 | [**Leaf**](c-leaf.md)<br/>                                                            |
| Возможные старшие          | [**Контейнер**](c-container.md)                                                             |
| Вспомогательные классы           | \-                                                                                           |
| NT-Security-дескриптор      | О:БАГ: BAD: S:                                                                                 |
| Дескриптор безопасности по умолчанию | D: (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;;D А) (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;; SY) (A;; РПЛКЛОРК;;; СЛУЖБЫ |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-2000-server-attributes"></a>Атрибуты сервера Windows 2000

Этот класс содержит следующие атрибуты для сервера Windows 2000:



| attribute                                                                   | Обязательный | Унаследован от                    |
|-----------------------------------------------------------------------------|-----------|---------------------------------|
| [**Дополнительные-доверенные имена служб**](a-additionaltrustedservicenames.md) | Неверно     | **Доверенный домен**              |
| [**Описание администратора**](a-admindescription.md)                             | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Имя администратора-отображение**](a-admindisplayname.md)                            | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Allowed-Attributes**](a-allowedattributes.md)                           | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Allowed-Attributes-эффективен**](a-allowedattributeseffective.md)        | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Allowed-Child-classes**](a-allowedchildclasses.md)                      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Allowed-Child-classes-эффективен**](a-allowedchildclasseseffective.md)   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Плацдарм-Server-List-BL**](a-bridgeheadserverlistbl.md)               | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Каноническое имя**](a-canonicalname.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Common-Name**](a-cn.md)                                                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Метка времени создания**](a-createtimestamp.md)                              | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Описание**](a-description.md)                                        | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Отображаемое имя**](a-displayname.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Отображаемое имя — печатаемое**](a-displaynameprintable.md)                    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Домен-перекрестная ссылка**](a-domaincrossref.md)                                | Неверно     | **Доверенный домен**              |
| [**Идентификатор домена**](a-domainidentifier.md)                             | Неверно     | **Доверенный домен**              |
| [**DSA-Signature**](a-dsasignature.md)                                     | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**DS-Core-распространение-данные**](a-dscorepropagationdata.md)                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Имя расширения**](a-extensionname.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Метки**](a-flags.md)                                                    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Неструктурированное имя**](a-flatname.md)                                             | Неверно     | **Доверенный домен**              |
| [**Из записи**](a-fromentry.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Initial-auth-входящий**](a-initialauthincoming.md)                      | Неверно     | **Доверенный домен**              |
| [**Initial-auth-исходящий трафик**](a-initialauthoutgoing.md)                      | Неверно     | **Доверенный домен**              |
| [**Тип экземпляра**](a-instancetype.md)                                     | True      | [**Вверх**](c-top.md)<br/> |
| [**Является критически важным — системный объект**](a-iscriticalsystemobject.md)               | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Удалено**](a-isdeleted.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Входит в состав списка рассылки**](a-memberof.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Имеет права владельца**](a-isprivilegeholder.md)                          | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Последний-известный-родительский**](a-lastknownparent.md)                              | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Управляемые объекты**](a-managedobjects.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**В основном**](a-masteredby.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Метка времени изменения**](a-modifytimestamp.md)                              | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-целостность-дочерняя — количество**](a-ms-ds-consistencychildcount.md)      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Consistencу-Guid**](a-ms-ds-consistencyguid.md)                   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**нетбут-SCP-BL**](a-netbootscpbl.md)                                    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Не-Security-Member-BL**](a-nonsecuritymemberbl.md)                     | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**NT-Security-дескриптор**](a-ntsecuritydescriptor.md)                    | True      | [**Вверх**](c-top.md)<br/> |
| [**Obj-расп-имя**](a-distinguishedname.md)                                | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Объект — Категория**](a-objectcategory.md)                                 | True      | [**Вверх**](c-top.md)<br/> |
| [**Объектный класс**](a-objectclass.md)                                       | True      | [**Вверх**](c-top.md)<br/> |
| [**Объект — GUID**](a-objectguid.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Версия объекта**](a-objectversion.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Другие хорошо известные объекты**](a-otherwellknownobjects.md)                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Разделяемый атрибут-удаление-список**](a-partialattributedeletionlist.md)   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Разделяемый атрибут-set**](a-partialattributeset.md)                      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Возможно — подстрочные**](a-possibleinferiors.md)                           | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Прокси-объект-имя**](a-proxiedobjectname.md)                          | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Прокси-адреса**](a-proxyaddresses.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Запрос — политика — BL**](a-querypolicybl.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**RDN**](a-name.md)                                                       | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**REPL-Уптодате-Vector**](a-repluptodatevector.md)                        | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Отчеты**](a-directreports.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Представители — от**](a-repsfrom.md)                                             | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Представители — кому**](a-repsto.md)                                                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Редакции**](a-revision.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**SD-Rights-эффективен**](a-sdrightseffective.md)                          | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Безопасность — идентификатор**](a-securityidentifier.md)                         | Неверно     | **Доверенный домен**              |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**"Показать" — "Расширенный просмотр"**](a-showinadvancedviewonly.md)              | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Подразделы-ReFS**](a-subrefs.md)                                               | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**субсчемасубентри**](a-subschemasubentry.md)                            | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Системные флаги**](a-systemflags.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Trust-атрибуты**](a-trustattributes.md)                               | Неверно     | **Доверенный домен**              |
| [**Trust-auth-входящий**](a-trustauthincoming.md)                          | Неверно     | **Доверенный домен**              |
| [**Trust-auth-исходящий трафик**](a-trustauthoutgoing.md)                          | Неверно     | **Доверенный домен**              |
| [**Направление доверия**](a-trustdirection.md)                                 | Неверно     | **Доверенный домен**              |
| [**Доверие — партнер**](a-trustpartner.md)                                     | Неверно     | **Доверенный домен**              |
| [**Отношение доверия-POSIX-offset**](a-trustposixoffset.md)                            | Неверно     | **Доверенный домен**              |
| [**Тип доверия**](a-trusttype.md)                                           | Неверно     | **Доверенный домен**              |
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



## <a name="windows-server-2003"></a>Windows Server 2003

-   [Атрибуты](#windows-server-2003-attributes)



| Ввод | Значение |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Неверно                                                                                                                                                                                         |
| Object-Category             | 1                                                                                                                                                                                             |
| По умолчанию — объект — Категория     | \-                                                                                                                                                                                            |
| Governs-Id                  | 1.2.840.113556.1.5.34                                                                                                                                                                         |
| По умолчанию-скрытие значения        | 1                                                                                                                                                                                             |
| RDN-Атри-ID                  | [**Common-Name**](a-cn.md)<br/>                                                                                                                                                        |
| Подкласс                 | [**Leaf**](c-leaf.md)<br/>                                                                                                                                                             |
| Возможные старшие          | [**Контейнер**](c-container.md)                                                                                                                                                              |
| Вспомогательные классы           | \-                                                                                                                                                                                            |
| NT-Security-дескриптор      | О:БАГ: BAD: S:                                                                                                                                                                                  |
| Дескриптор безопасности по умолчанию | D: (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;;D А) (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;; SY) (A;; РПЛКЛОРК;;; AU) (OA;; WP; 736e4812-af31-11d2-b7df-00805f48caeb; bf967ab8-0de6-11D0-a285-00aa003049e2; CO) (A;; SD;;; СОСТАВ |
| System-Flags                | 0x00000010                                                                                                                                                                                    |



## <a name="windows-server-2003-attributes"></a>Атрибуты Windows Server 2003

Этот класс содержит следующие атрибуты для Windows Server 2003:



| attribute                                                                   | Обязательный | Унаследован от                    |
|-----------------------------------------------------------------------------|-----------|---------------------------------|
| [**Дополнительные-доверенные имена служб**](a-additionaltrustedservicenames.md) | Неверно     | **Доверенный домен**              |
| [**Описание администратора**](a-admindescription.md)                             | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Имя администратора-отображение**](a-admindisplayname.md)                            | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Allowed-Attributes**](a-allowedattributes.md)                           | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Allowed-Attributes-эффективен**](a-allowedattributeseffective.md)        | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Allowed-Child-classes**](a-allowedchildclasses.md)                      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Allowed-Child-classes-эффективен**](a-allowedchildclasseseffective.md)   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Плацдарм-Server-List-BL**](a-bridgeheadserverlistbl.md)               | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Каноническое имя**](a-canonicalname.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Common-Name**](a-cn.md)                                                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Метка времени создания**](a-createtimestamp.md)                              | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Описание**](a-description.md)                                        | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Отображаемое имя**](a-displayname.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Отображаемое имя — печатаемое**](a-displaynameprintable.md)                    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Домен-перекрестная ссылка**](a-domaincrossref.md)                                | Неверно     | **Доверенный домен**              |
| [**Идентификатор домена**](a-domainidentifier.md)                             | Неверно     | **Доверенный домен**              |
| [**DSA-Signature**](a-dsasignature.md)                                     | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**DS-Core-распространение-данные**](a-dscorepropagationdata.md)                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Имя расширения**](a-extensionname.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Метки**](a-flags.md)                                                    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Неструктурированное имя**](a-flatname.md)                                             | Неверно     | **Доверенный домен**              |
| [**Из записи**](a-fromentry.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Initial-auth-входящий**](a-initialauthincoming.md)                      | Неверно     | **Доверенный домен**              |
| [**Initial-auth-исходящий трафик**](a-initialauthoutgoing.md)                      | Неверно     | **Доверенный домен**              |
| [**Тип экземпляра**](a-instancetype.md)                                     | True      | [**Вверх**](c-top.md)<br/> |
| [**Является критически важным — системный объект**](a-iscriticalsystemobject.md)               | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Удалено**](a-isdeleted.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Входит в состав списка рассылки**](a-memberof.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Имеет права владельца**](a-isprivilegeholder.md)                          | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Последний-известный-родительский**](a-lastknownparent.md)                              | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Управляемые объекты**](a-managedobjects.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**В основном**](a-masteredby.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Метка времени изменения**](a-modifytimestamp.md)                              | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-COM-Партитионсетлинк**](a-mscom-partitionsetlink.md)                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-COM-Усерлинк**](a-mscom-userlink.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-примерно-Иммед-подчиненные**](a-msds-approx-immed-subordinates.md) | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-целостность-дочерняя — количество**](a-ms-ds-consistencychildcount.md)      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Consistencу-Guid**](a-ms-ds-consistencyguid.md)                   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Creator-SID**](a-ms-ds-creatorsid.md)                             | Неверно     | **Доверенный домен**              |
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
| [**MS-DS-Trust-лес-Trust-сведения**](a-msds-trustforesttrustinfo.md)        | Неверно     | **Доверенный домен**              |
| [**MS-дов-Owner-BL**](a-ownerbl.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**нетбут-SCP-BL**](a-netbootscpbl.md)                                    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Не-Security-Member-BL**](a-nonsecuritymemberbl.md)                     | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**NT-Security-дескриптор**](a-ntsecuritydescriptor.md)                    | True      | [**Вверх**](c-top.md)<br/> |
| [**Obj-расп-имя**](a-distinguishedname.md)                                | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Объект — Категория**](a-objectcategory.md)                                 | True      | [**Вверх**](c-top.md)<br/> |
| [**Объектный класс**](a-objectclass.md)                                       | True      | [**Вверх**](c-top.md)<br/> |
| [**Объект — GUID**](a-objectguid.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Версия объекта**](a-objectversion.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Другие хорошо известные объекты**](a-otherwellknownobjects.md)                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Разделяемый атрибут-удаление-список**](a-partialattributedeletionlist.md)   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Разделяемый атрибут-set**](a-partialattributeset.md)                      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Возможно — подстрочные**](a-possibleinferiors.md)                           | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Прокси-объект-имя**](a-proxiedobjectname.md)                          | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Прокси-адреса**](a-proxyaddresses.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Запрос — политика — BL**](a-querypolicybl.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**RDN**](a-name.md)                                                       | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**REPL-Уптодате-Vector**](a-repluptodatevector.md)                        | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Отчеты**](a-directreports.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Представители — от**](a-repsfrom.md)                                             | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Представители — кому**](a-repsto.md)                                                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Редакции**](a-revision.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**SD-Rights-эффективен**](a-sdrightseffective.md)                          | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Безопасность — идентификатор**](a-securityidentifier.md)                         | Неверно     | **Доверенный домен**              |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**"Показать" — "Расширенный просмотр"**](a-showinadvancedviewonly.md)              | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Структурный объектный класс**](a-structuralobjectclass.md)                  | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Подразделы-ReFS**](a-subrefs.md)                                               | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**субсчемасубентри**](a-subschemasubentry.md)                            | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Системные флаги**](a-systemflags.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Trust-атрибуты**](a-trustattributes.md)                               | Неверно     | **Доверенный домен**              |
| [**Trust-auth-входящий**](a-trustauthincoming.md)                          | Неверно     | **Доверенный домен**              |
| [**Trust-auth-исходящий трафик**](a-trustauthoutgoing.md)                          | Неверно     | **Доверенный домен**              |
| [**Направление доверия**](a-trustdirection.md)                                 | Неверно     | **Доверенный домен**              |
| [**Доверие — партнер**](a-trustpartner.md)                                     | Неверно     | **Доверенный домен**              |
| [**Отношение доверия-POSIX-offset**](a-trustposixoffset.md)                            | Неверно     | **Доверенный домен**              |
| [**Тип доверия**](a-trusttype.md)                                           | Неверно     | **Доверенный домен**              |
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



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2

-   [Атрибуты](#windows-server-2003-r2-attributes)



| Ввод | Значение |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Неверно                                                                                                                                                                                         |
| Object-Category             | 1                                                                                                                                                                                             |
| По умолчанию — объект — Категория     | \-                                                                                                                                                                                            |
| Governs-Id                  | 1.2.840.113556.1.5.34                                                                                                                                                                         |
| По умолчанию-скрытие значения        | 1                                                                                                                                                                                             |
| RDN-Атри-ID                  | [**Common-Name**](a-cn.md)<br/>                                                                                                                                                        |
| Подкласс                 | [**Leaf**](c-leaf.md)<br/>                                                                                                                                                             |
| Возможные старшие          | [**Контейнер**](c-container.md)                                                                                                                                                              |
| Вспомогательные классы           | \-                                                                                                                                                                                            |
| NT-Security-дескриптор      | О:БАГ: BAD: S:                                                                                                                                                                                  |
| Дескриптор безопасности по умолчанию | D: (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;;D А) (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;; SY) (A;; РПЛКЛОРК;;; AU) (OA;; WP; 736e4812-af31-11d2-b7df-00805f48caeb; bf967ab8-0de6-11D0-a285-00aa003049e2; CO) (A;; SD;;; СОСТАВ |
| System-Flags                | 0x00000010                                                                                                                                                                                    |



## <a name="windows-server-2003-r2-attributes"></a>Атрибуты Windows Server 2003 R2

Этот класс содержит следующие атрибуты для Windows Server 2003 R2:



| attribute                                                                   | Обязательный | Унаследован от                    |
|-----------------------------------------------------------------------------|-----------|---------------------------------|
| [**Дополнительные-доверенные имена служб**](a-additionaltrustedservicenames.md) | Неверно     | **Доверенный домен**              |
| [**Описание администратора**](a-admindescription.md)                             | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Имя администратора-отображение**](a-admindisplayname.md)                            | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Allowed-Attributes**](a-allowedattributes.md)                           | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Allowed-Attributes-эффективен**](a-allowedattributeseffective.md)        | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Allowed-Child-classes**](a-allowedchildclasses.md)                      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Allowed-Child-classes-эффективен**](a-allowedchildclasseseffective.md)   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Плацдарм-Server-List-BL**](a-bridgeheadserverlistbl.md)               | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Каноническое имя**](a-canonicalname.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Common-Name**](a-cn.md)                                                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Метка времени создания**](a-createtimestamp.md)                              | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Описание**](a-description.md)                                        | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Отображаемое имя**](a-displayname.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Отображаемое имя — печатаемое**](a-displaynameprintable.md)                    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Домен-перекрестная ссылка**](a-domaincrossref.md)                                | Неверно     | **Доверенный домен**              |
| [**Идентификатор домена**](a-domainidentifier.md)                             | Неверно     | **Доверенный домен**              |
| [**DSA-Signature**](a-dsasignature.md)                                     | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**DS-Core-распространение-данные**](a-dscorepropagationdata.md)                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Имя расширения**](a-extensionname.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Метки**](a-flags.md)                                                    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Неструктурированное имя**](a-flatname.md)                                             | Неверно     | **Доверенный домен**              |
| [**Из записи**](a-fromentry.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Initial-auth-входящий**](a-initialauthincoming.md)                      | Неверно     | **Доверенный домен**              |
| [**Initial-auth-исходящий трафик**](a-initialauthoutgoing.md)                      | Неверно     | **Доверенный домен**              |
| [**Тип экземпляра**](a-instancetype.md)                                     | True      | [**Вверх**](c-top.md)<br/> |
| [**Является критически важным — системный объект**](a-iscriticalsystemobject.md)               | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Удалено**](a-isdeleted.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Входит в состав списка рассылки**](a-memberof.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Имеет права владельца**](a-isprivilegeholder.md)                          | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Последний-известный-родительский**](a-lastknownparent.md)                              | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Управляемые объекты**](a-managedobjects.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**В основном**](a-masteredby.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Метка времени изменения**](a-modifytimestamp.md)                              | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-COM-Партитионсетлинк**](a-mscom-partitionsetlink.md)                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-COM-Усерлинк**](a-mscom-userlink.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DFSR-Компутерреференцебл**](a-msdfsr-computerreferencebl.md)         | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DFSR-Мемберреференцебл**](a-msdfsr-memberreferencebl.md)             | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-примерно-Иммед-подчиненные**](a-msds-approx-immed-subordinates.md) | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-целостность-дочерняя — количество**](a-ms-ds-consistencychildcount.md)      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Consistencу-Guid**](a-ms-ds-consistencyguid.md)                   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Creator-SID**](a-ms-ds-creatorsid.md)                             | Неверно     | **Доверенный домен**              |
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
| [**MS-DS-Trust-лес-Trust-сведения**](a-msds-trustforesttrustinfo.md)        | Неверно     | **Доверенный домен**              |
| [**MS-дов-Owner-BL**](a-ownerbl.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Мссфу-30-POSIX-член-of**](a-mssfu30posixmemberof.md)                  | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**нетбут-SCP-BL**](a-netbootscpbl.md)                                    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Не-Security-Member-BL**](a-nonsecuritymemberbl.md)                     | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**NT-Security-дескриптор**](a-ntsecuritydescriptor.md)                    | True      | [**Вверх**](c-top.md)<br/> |
| [**Obj-расп-имя**](a-distinguishedname.md)                                | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Объект — Категория**](a-objectcategory.md)                                 | True      | [**Вверх**](c-top.md)<br/> |
| [**Объектный класс**](a-objectclass.md)                                       | True      | [**Вверх**](c-top.md)<br/> |
| [**Объект — GUID**](a-objectguid.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Версия объекта**](a-objectversion.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Другие хорошо известные объекты**](a-otherwellknownobjects.md)                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Разделяемый атрибут-удаление-список**](a-partialattributedeletionlist.md)   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Разделяемый атрибут-set**](a-partialattributeset.md)                      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Возможно — подстрочные**](a-possibleinferiors.md)                           | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Прокси-объект-имя**](a-proxiedobjectname.md)                          | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Прокси-адреса**](a-proxyaddresses.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Запрос — политика — BL**](a-querypolicybl.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**RDN**](a-name.md)                                                       | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**REPL-Уптодате-Vector**](a-repluptodatevector.md)                        | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Отчеты**](a-directreports.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Представители — от**](a-repsfrom.md)                                             | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Представители — кому**](a-repsto.md)                                                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Редакции**](a-revision.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**SD-Rights-эффективен**](a-sdrightseffective.md)                          | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Безопасность — идентификатор**](a-securityidentifier.md)                         | Неверно     | **Доверенный домен**              |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**"Показать" — "Расширенный просмотр"**](a-showinadvancedviewonly.md)              | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Структурный объектный класс**](a-structuralobjectclass.md)                  | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Подразделы-ReFS**](a-subrefs.md)                                               | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**субсчемасубентри**](a-subschemasubentry.md)                            | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Системные флаги**](a-systemflags.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Trust-атрибуты**](a-trustattributes.md)                               | Неверно     | **Доверенный домен**              |
| [**Trust-auth-входящий**](a-trustauthincoming.md)                          | Неверно     | **Доверенный домен**              |
| [**Trust-auth-исходящий трафик**](a-trustauthoutgoing.md)                          | Неверно     | **Доверенный домен**              |
| [**Направление доверия**](a-trustdirection.md)                                 | Неверно     | **Доверенный домен**              |
| [**Доверие — партнер**](a-trustpartner.md)                                     | Неверно     | **Доверенный домен**              |
| [**Отношение доверия-POSIX-offset**](a-trustposixoffset.md)                            | Неверно     | **Доверенный домен**              |
| [**Тип доверия**](a-trusttype.md)                                           | Неверно     | **Доверенный домен**              |
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



## <a name="windows-server-2008"></a>Windows Server 2008

-   [Атрибуты](#windows-server-2008-attributes)



| Ввод | Значение |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Неверно                                                                                                                                                                                         |
| Object-Category             | 1                                                                                                                                                                                             |
| По умолчанию — объект — Категория     | \-                                                                                                                                                                                            |
| Governs-Id                  | 1.2.840.113556.1.5.34                                                                                                                                                                         |
| По умолчанию-скрытие значения        | 1                                                                                                                                                                                             |
| RDN-Атри-ID                  | [**Common-Name**](a-cn.md)<br/>                                                                                                                                                        |
| Подкласс                 | [**Leaf**](c-leaf.md)<br/>                                                                                                                                                             |
| Возможные старшие          | [**Контейнер**](c-container.md)                                                                                                                                                              |
| Вспомогательные классы           | \-                                                                                                                                                                                            |
| NT-Security-дескриптор      | О:БАГ: BAD: S:                                                                                                                                                                                  |
| Дескриптор безопасности по умолчанию | D: (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;;D А) (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;; SY) (A;; РПЛКЛОРК;;; AU) (OA;; WP; 736e4812-af31-11d2-b7df-00805f48caeb; bf967ab8-0de6-11D0-a285-00aa003049e2; CO) (A;; SD;;; СОСТАВ |
| System-Flags                | 0x00000010                                                                                                                                                                                    |



## <a name="windows-server-2008-attributes"></a>Атрибуты Windows Server 2008

Этот класс содержит следующие атрибуты для Windows Server 2008:



| attribute                                                                      | Обязательный | Унаследован от                    |
|--------------------------------------------------------------------------------|-----------|---------------------------------|
| [**Дополнительные-доверенные имена служб**](a-additionaltrustedservicenames.md)    | Неверно     | **Доверенный домен**              |
| [**Описание администратора**](a-admindescription.md)                                | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Имя администратора-отображение**](a-admindisplayname.md)                               | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Allowed-Attributes**](a-allowedattributes.md)                              | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Allowed-Attributes-эффективен**](a-allowedattributeseffective.md)           | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Allowed-Child-classes**](a-allowedchildclasses.md)                         | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Allowed-Child-classes-эффективен**](a-allowedchildclasseseffective.md)      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Плацдарм-Server-List-BL**](a-bridgeheadserverlistbl.md)                  | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Каноническое имя**](a-canonicalname.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Common-Name**](a-cn.md)                                                    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Метка времени создания**](a-createtimestamp.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Описание**](a-description.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Отображаемое имя**](a-displayname.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Отображаемое имя — печатаемое**](a-displaynameprintable.md)                       | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Домен-перекрестная ссылка**](a-domaincrossref.md)                                   | Неверно     | **Доверенный домен**              |
| [**Идентификатор домена**](a-domainidentifier.md)                                | Неверно     | **Доверенный домен**              |
| [**DSA-Signature**](a-dsasignature.md)                                        | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**DS-Core-распространение-данные**](a-dscorepropagationdata.md)                    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Имя расширения**](a-extensionname.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Метки**](a-flags.md)                                                       | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Неструктурированное имя**](a-flatname.md)                                                | Неверно     | **Доверенный домен**              |
| [**Из записи**](a-fromentry.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                  | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                     | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Initial-auth-входящий**](a-initialauthincoming.md)                         | Неверно     | **Доверенный домен**              |
| [**Initial-auth-исходящий трафик**](a-initialauthoutgoing.md)                         | Неверно     | **Доверенный домен**              |
| [**Тип экземпляра**](a-instancetype.md)                                        | True      | [**Вверх**](c-top.md)<br/> |
| [**Является критически важным — системный объект**](a-iscriticalsystemobject.md)                  | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Удалено**](a-isdeleted.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Входит в состав списка рассылки**](a-memberof.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Имеет права владельца**](a-isprivilegeholder.md)                             | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Последний-известный-родительский**](a-lastknownparent.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Управляемые объекты**](a-managedobjects.md)                                    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**В основном**](a-masteredby.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Метка времени изменения**](a-modifytimestamp.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-COM-Партитионсетлинк**](a-mscom-partitionsetlink.md)                    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-COM-Усерлинк**](a-mscom-userlink.md)                                    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DFSR-Компутерреференцебл**](a-msdfsr-computerreferencebl.md)            | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DFSR-Мемберреференцебл**](a-msdfsr-memberreferencebl.md)                | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-примерно-Иммед-подчиненные**](a-msds-approx-immed-subordinates.md)    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Аусентикатедто-Аккаунтлист**](a-msds-authenticatedtoaccountlist.md) | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-целостность-дочерняя — количество**](a-ms-ds-consistencychildcount.md)         | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Consistencу-Guid**](a-ms-ds-consistencyguid.md)                      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Creator-SID**](a-ms-ds-creatorsid.md)                                | Неверно     | **Доверенный домен**              |
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
| [**MS-DS-Supported-Encryption-Types**](a-msds-supportedencryptiontypes.md)    | Неверно     | **Доверенный домен**              |
| [**MS-DS-Tasks-для-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                  | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                  | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Trust-лес-Trust-сведения**](a-msds-trustforesttrustinfo.md)           | Неверно     | **Доверенный домен**              |
| [**MS-дов-Owner-BL**](a-ownerbl.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Мссфу-30-POSIX-член-of**](a-mssfu30posixmemberof.md)                     | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**нетбут-SCP-BL**](a-netbootscpbl.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Не-Security-Member-BL**](a-nonsecuritymemberbl.md)                        | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**NT-Security-дескриптор**](a-ntsecuritydescriptor.md)                       | True      | [**Вверх**](c-top.md)<br/> |
| [**Obj-расп-имя**](a-distinguishedname.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Объект — Категория**](a-objectcategory.md)                                    | True      | [**Вверх**](c-top.md)<br/> |
| [**Объектный класс**](a-objectclass.md)                                          | True      | [**Вверх**](c-top.md)<br/> |
| [**Объект — GUID**](a-objectguid.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Версия объекта**](a-objectversion.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Другие хорошо известные объекты**](a-otherwellknownobjects.md)                    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Разделяемый атрибут-удаление-список**](a-partialattributedeletionlist.md)      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Разделяемый атрибут-set**](a-partialattributeset.md)                         | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Возможно — подстрочные**](a-possibleinferiors.md)                              | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Прокси-объект-имя**](a-proxiedobjectname.md)                             | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Прокси-адреса**](a-proxyaddresses.md)                                    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Запрос — политика — BL**](a-querypolicybl.md)                                     | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**RDN**](a-name.md)                                                          | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**REPL-Уптодате-Vector**](a-repluptodatevector.md)                           | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Отчеты**](a-directreports.md)                                             | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Представители — от**](a-repsfrom.md)                                                | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Представители — кому**](a-repsto.md)                                                    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Редакции**](a-revision.md)                                                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**SD-Rights-эффективен**](a-sdrightseffective.md)                             | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Безопасность — идентификатор**](a-securityidentifier.md)                            | Неверно     | **Доверенный домен**              |
| [**Server-Reference-BL**](a-serverreferencebl.md)                             | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**"Показать" — "Расширенный просмотр"**](a-showinadvancedviewonly.md)                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Site-Object-BL**](a-siteobjectbl.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Структурный объектный класс**](a-structuralobjectclass.md)                     | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Подразделы-ReFS**](a-subrefs.md)                                                  | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**субсчемасубентри**](a-subschemasubentry.md)                               | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Системные флаги**](a-systemflags.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Trust-атрибуты**](a-trustattributes.md)                                  | Неверно     | **Доверенный домен**              |
| [**Trust-auth-входящий**](a-trustauthincoming.md)                             | Неверно     | **Доверенный домен**              |
| [**Trust-auth-исходящий трафик**](a-trustauthoutgoing.md)                             | Неверно     | **Доверенный домен**              |
| [**Направление доверия**](a-trustdirection.md)                                    | Неверно     | **Доверенный домен**              |
| [**Доверие — партнер**](a-trustpartner.md)                                        | Неверно     | **Доверенный домен**              |
| [**Отношение доверия-POSIX-offset**](a-trustposixoffset.md)                               | Неверно     | **Доверенный домен**              |
| [**Тип доверия**](a-trusttype.md)                                              | Неверно     | **Доверенный домен**              |
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



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2

-   [Атрибуты](#windows-server-2008-r2-attributes)



| Ввод | Значение |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Неверно                                                                                                                                                                                         |
| Object-Category             | 1                                                                                                                                                                                             |
| По умолчанию — объект — Категория     | \-                                                                                                                                                                                            |
| Governs-Id                  | 1.2.840.113556.1.5.34                                                                                                                                                                         |
| По умолчанию-скрытие значения        | 1                                                                                                                                                                                             |
| RDN-Атри-ID                  | [**Common-Name**](a-cn.md)<br/>                                                                                                                                                        |
| Подкласс                 | [**Leaf**](c-leaf.md)<br/>                                                                                                                                                             |
| Возможные старшие          | [**Контейнер**](c-container.md)                                                                                                                                                              |
| Вспомогательные классы           | \-                                                                                                                                                                                            |
| NT-Security-дескриптор      | О:БАГ: BAD: S:                                                                                                                                                                                  |
| Дескриптор безопасности по умолчанию | D: (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;;D А) (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;; SY) (A;; РПЛКЛОРК;;; AU) (OA;; WP; 736e4812-af31-11d2-b7df-00805f48caeb; bf967ab8-0de6-11D0-a285-00aa003049e2; CO) (A;; SD;;; СОСТАВ |
| System-Flags                | 0x00000010                                                                                                                                                                                    |



## <a name="windows-server-2008-r2-attributes"></a>Атрибуты Windows Server 2008 R2

Этот класс содержит следующие атрибуты для Windows Server 2008 R2:



| attribute                                                                        | Обязательный | Унаследован от                    |
|----------------------------------------------------------------------------------|-----------|---------------------------------|
| [**Дополнительные-доверенные имена служб**](a-additionaltrustedservicenames.md)      | Неверно     | **Доверенный домен**              |
| [**Описание администратора**](a-admindescription.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Имя администратора-отображение**](a-admindisplayname.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Allowed-Attributes**](a-allowedattributes.md)                                | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Allowed-Attributes-эффективен**](a-allowedattributeseffective.md)             | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Allowed-Child-classes**](a-allowedchildclasses.md)                           | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Allowed-Child-classes-эффективен**](a-allowedchildclasseseffective.md)        | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Плацдарм-Server-List-BL**](a-bridgeheadserverlistbl.md)                    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Каноническое имя**](a-canonicalname.md)                                        | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Common-Name**](a-cn.md)                                                      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Метка времени создания**](a-createtimestamp.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Описание**](a-description.md)                                             | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Отображаемое имя**](a-displayname.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Отображаемое имя — печатаемое**](a-displaynameprintable.md)                         | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Домен-перекрестная ссылка**](a-domaincrossref.md)                                     | Неверно     | **Доверенный домен**              |
| [**Идентификатор домена**](a-domainidentifier.md)                                  | Неверно     | **Доверенный домен**              |
| [**DSA-Signature**](a-dsasignature.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**DS-Core-распространение-данные**](a-dscorepropagationdata.md)                      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Имя расширения**](a-extensionname.md)                                        | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Метки**](a-flags.md)                                                         | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Неструктурированное имя**](a-flatname.md)                                                  | Неверно     | **Доверенный домен**              |
| [**Из записи**](a-fromentry.md)                                                | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                        | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Initial-auth-входящий**](a-initialauthincoming.md)                           | Неверно     | **Доверенный домен**              |
| [**Initial-auth-исходящий трафик**](a-initialauthoutgoing.md)                           | Неверно     | **Доверенный домен**              |
| [**Тип экземпляра**](a-instancetype.md)                                          | True      | [**Вверх**](c-top.md)<br/> |
| [**Является критически важным — системный объект**](a-iscriticalsystemobject.md)                    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Удалено**](a-isdeleted.md)                                                | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Входит в состав списка рассылки**](a-memberof.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Имеет права владельца**](a-isprivilegeholder.md)                               | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Является перезапущенным**](a-isrecycled.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Последний-известный-родительский**](a-lastknownparent.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Управляемые объекты**](a-managedobjects.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**В основном**](a-masteredby.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Метка времени изменения**](a-modifytimestamp.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-COM-Партитионсетлинк**](a-mscom-partitionsetlink.md)                      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-COM-Усерлинк**](a-mscom-userlink.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DFSR-Компутерреференцебл**](a-msdfsr-computerreferencebl.md)              | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DFSR-Мемберреференцебл**](a-msdfsr-memberreferencebl.md)                  | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-примерно-Иммед-подчиненные**](a-msds-approx-immed-subordinates.md)      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Аусентикатедто-Аккаунтлист**](a-msds-authenticatedtoaccountlist.md)   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-целостность-дочерняя — количество**](a-ms-ds-consistencychildcount.md)           | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Consistencу-Guid**](a-ms-ds-consistencyguid.md)                        | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Creator-SID**](a-ms-ds-creatorsid.md)                                  | Неверно     | **Доверенный домен**              |
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
| [**MS-DS-Supported-Encryption-Types**](a-msds-supportedencryptiontypes.md)      | Неверно     | **Доверенный домен**              |
| [**MS-DS-Tasks-для-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Trust-лес-Trust-сведения**](a-msds-trustforesttrustinfo.md)             | Неверно     | **Доверенный домен**              |
| [**MS-дов-Owner-BL**](a-ownerbl.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Мссфу-30-POSIX-член-of**](a-mssfu30posixmemberof.md)                       | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**нетбут-SCP-BL**](a-netbootscpbl.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Не-Security-Member-BL**](a-nonsecuritymemberbl.md)                          | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**NT-Security-дескриптор**](a-ntsecuritydescriptor.md)                         | True      | [**Вверх**](c-top.md)<br/> |
| [**Obj-расп-имя**](a-distinguishedname.md)                                     | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Объект — Категория**](a-objectcategory.md)                                      | True      | [**Вверх**](c-top.md)<br/> |
| [**Объектный класс**](a-objectclass.md)                                            | True      | [**Вверх**](c-top.md)<br/> |
| [**Объект — GUID**](a-objectguid.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Версия объекта**](a-objectversion.md)                                        | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Другие хорошо известные объекты**](a-otherwellknownobjects.md)                      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Разделяемый атрибут-удаление-список**](a-partialattributedeletionlist.md)        | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Разделяемый атрибут-set**](a-partialattributeset.md)                           | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Возможно — подстрочные**](a-possibleinferiors.md)                                | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Прокси-объект-имя**](a-proxiedobjectname.md)                               | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Прокси-адреса**](a-proxyaddresses.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Запрос — политика — BL**](a-querypolicybl.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**RDN**](a-name.md)                                                            | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                        | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**REPL-Уптодате-Vector**](a-repluptodatevector.md)                             | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Отчеты**](a-directreports.md)                                               | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Представители — от**](a-repsfrom.md)                                                  | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Представители — кому**](a-repsto.md)                                                      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Редакции**](a-revision.md)                                                   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**SD-Rights-эффективен**](a-sdrightseffective.md)                               | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Безопасность — идентификатор**](a-securityidentifier.md)                              | Неверно     | **Доверенный домен**              |
| [**Server-Reference-BL**](a-serverreferencebl.md)                               | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**"Показать" — "Расширенный просмотр"**](a-showinadvancedviewonly.md)                   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Site-Object-BL**](a-siteobjectbl.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Структурный объектный класс**](a-structuralobjectclass.md)                       | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Подразделы-ReFS**](a-subrefs.md)                                                    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**субсчемасубентри**](a-subschemasubentry.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Системные флаги**](a-systemflags.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Trust-атрибуты**](a-trustattributes.md)                                    | Неверно     | **Доверенный домен**              |
| [**Trust-auth-входящий**](a-trustauthincoming.md)                               | Неверно     | **Доверенный домен**              |
| [**Trust-auth-исходящий трафик**](a-trustauthoutgoing.md)                               | Неверно     | **Доверенный домен**              |
| [**Направление доверия**](a-trustdirection.md)                                      | Неверно     | **Доверенный домен**              |
| [**Доверие — партнер**](a-trustpartner.md)                                          | Неверно     | **Доверенный домен**              |
| [**Отношение доверия-POSIX-offset**](a-trustposixoffset.md)                                 | Неверно     | **Доверенный домен**              |
| [**Тип доверия**](a-trusttype.md)                                                | Неверно     | **Доверенный домен**              |
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



## <a name="windows-server-2012"></a>Windows Server 2012

-   [Атрибуты](#windows-server-2012-attributes)



| Ввод | Значение |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Неверно                                                                                                                                                                                         |
| Object-Category             | 1                                                                                                                                                                                             |
| По умолчанию — объект — Категория     | \-                                                                                                                                                                                            |
| Governs-Id                  | 1.2.840.113556.1.5.34                                                                                                                                                                         |
| По умолчанию-скрытие значения        | 1                                                                                                                                                                                             |
| RDN-Атри-ID                  | [**Common-Name**](a-cn.md)<br/>                                                                                                                                                        |
| Подкласс                 | [**Leaf**](c-leaf.md)<br/>                                                                                                                                                             |
| Возможные старшие          | [**Контейнер**](c-container.md)                                                                                                                                                              |
| Вспомогательные классы           | \-                                                                                                                                                                                            |
| NT-Security-дескриптор      | О:БАГ: BAD: S:                                                                                                                                                                                  |
| Дескриптор безопасности по умолчанию | D: (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;;D А) (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;; SY) (A;; РПЛКЛОРК;;; AU) (OA;; WP; 736e4812-af31-11d2-b7df-00805f48caeb; bf967ab8-0de6-11D0-a285-00aa003049e2; CO) (A;; SD;;; СОСТАВ |
| System-Flags                | 0x00000010                                                                                                                                                                                    |



## <a name="windows-server-2012-attributes"></a>Атрибуты Windows Server 2012

Этот класс содержит следующие атрибуты для Windows Server 2012:



| attribute                                                                                      | Обязательный | Унаследован от                    |
|------------------------------------------------------------------------------------------------|-----------|---------------------------------|
| [**Дополнительные-доверенные имена служб**](a-additionaltrustedservicenames.md)                    | Неверно     | **Доверенный домен**              |
| [**Описание администратора**](a-admindescription.md)                                                | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Имя администратора-отображение**](a-admindisplayname.md)                                               | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Allowed-Attributes**](a-allowedattributes.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Allowed-Attributes-эффективен**](a-allowedattributeseffective.md)                           | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Allowed-Child-classes**](a-allowedchildclasses.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Allowed-Child-classes-эффективен**](a-allowedchildclasseseffective.md)                      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Плацдарм-Server-List-BL**](a-bridgeheadserverlistbl.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Каноническое имя**](a-canonicalname.md)                                                      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Common-Name**](a-cn.md)                                                                    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Метка времени создания**](a-createtimestamp.md)                                                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Описание**](a-description.md)                                                           | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Отображаемое имя**](a-displayname.md)                                                          | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Отображаемое имя — печатаемое**](a-displaynameprintable.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Домен-перекрестная ссылка**](a-domaincrossref.md)                                                   | Неверно     | **Доверенный домен**              |
| [**Идентификатор домена**](a-domainidentifier.md)                                                | Неверно     | **Доверенный домен**              |
| [**DSA-Signature**](a-dsasignature.md)                                                        | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**DS-Core-распространение-данные**](a-dscorepropagationdata.md)                                    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Имя расширения**](a-extensionname.md)                                                      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Метки**](a-flags.md)                                                                       | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Неструктурированное имя**](a-flatname.md)                                                                | Неверно     | **Доверенный домен**              |
| [**Из записи**](a-fromentry.md)                                                              | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                                     | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Initial-auth-входящий**](a-initialauthincoming.md)                                         | Неверно     | **Доверенный домен**              |
| [**Initial-auth-исходящий трафик**](a-initialauthoutgoing.md)                                         | Неверно     | **Доверенный домен**              |
| [**Тип экземпляра**](a-instancetype.md)                                                        | True      | [**Вверх**](c-top.md)<br/> |
| [**Является критически важным — системный объект**](a-iscriticalsystemobject.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Удалено**](a-isdeleted.md)                                                              | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Входит в состав списка рассылки**](a-memberof.md)                                                          | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Имеет права владельца**](a-isprivilegeholder.md)                                             | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Является перезапущенным**](a-isrecycled.md)                                                            | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Последний-известный-родительский**](a-lastknownparent.md)                                                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Управляемые объекты**](a-managedobjects.md)                                                    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**В основном**](a-masteredby.md)                                                            | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Метка времени изменения**](a-modifytimestamp.md)                                                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-COM-Партитионсетлинк**](a-mscom-partitionsetlink.md)                                    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-COM-Усерлинк**](a-mscom-userlink.md)                                                    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DFSR-Компутерреференцебл**](a-msdfsr-computerreferencebl.md)                            | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DFSR-Мемберреференцебл**](a-msdfsr-memberreferencebl.md)                                | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-примерно-Иммед-подчиненные**](a-msds-approx-immed-subordinates.md)                    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Аусентикатедто-Аккаунтлист**](a-msds-authenticatedtoaccountlist.md)                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-ClaimSet-shares-возможные значения-with-BL**](a-msds-claimsharespossiblevalueswithbl.md)   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-целостность-дочерняя — количество**](a-ms-ds-consistencychildcount.md)                         | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Consistencу-Guid**](a-ms-ds-consistencyguid.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Creator-SID**](a-ms-ds-creatorsid.md)                                                | Неверно     | **Доверенный домен**              |
| [**MS-DS-исходящий трафик — утверждения-преобразование — политика**](a-msds-egressclaimstransformationpolicy.md)   | Неверно     | **Доверенный домен**              |
| [**Поддержка MS-DS-Feature-BL**](a-msds-enabledfeaturebl.md)                                    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)                           | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-входящие-Claims-преобразование — политика**](a-msds-ingressclaimstransformationpolicy.md) | Неверно     | **Доверенный домен**              |
| [**MS-DS--домен — для**](a-msds-isdomainfor.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-является-Full-реплика для**](a-msds-isfullreplicafor.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-является-partial-реплика для**](a-msds-ispartialreplicafor.md)                             | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-является-PRIMARY-Computer-для**](a-msds-isprimarycomputerfor.md)                           | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-локально-эффективное удаление — время**](a-msds-localeffectivedeletiontime.md)               | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Local-эффективен — время перезапуска**](a-msds-localeffectiverecycletime.md)                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Masterd-by**](a-msds-masteredby.md)                                                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)                              | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Members-of-Resource-Property-List-BL**](a-msds-membersofresourcepropertylistbl.md)   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-NC-REPL-курсоры**](a-msds-ncreplcursors.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-NC-REPL-Inbound-соседи**](a-msds-ncreplinboundneighbors.md)                       | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-NC-REPL-Outbound-соседи**](a-msds-ncreploutboundneighbors.md)                     | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)                  | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-NC-Type**](a-msds-nctype.md)                                                         | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-не-Members-BL**](a-msds-nonmembersbl.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Оидтограуп-Link-BL**](a-msds-oidtogrouplinkbl.md)                                    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Operations-для-AZ-Role-BL**](a-msds-operationsforazrolebl.md)                        | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)                        | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Principal-Name**](a-msds-principalname.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-PSO — применяется**](a-msds-psoapplied.md)                                                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-REPL-Attribute-Meta-Data**](a-msds-replattributemetadata.md)                         | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-выявил-DSA**](a-msds-revealeddsas.md)                                             | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-выводит-List-BL**](a-msds-revealedlistbl.md)                                        | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Supported-Encryption-Types**](a-msds-supportedencryptiontypes.md)                    | Неверно     | **Доверенный домен**              |
| [**MS-DS-Tasks-для-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-TDO-исходящий трафик — BL**](a-msds-tdoegressbl.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-TDO-входящий трафик — BL**](a-msds-tdoingressbl.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Trust-лес-Trust-сведения**](a-msds-trustforesttrustinfo.md)                           | Неверно     | **Доверенный домен**              |
| [**MS-DS-value-type-Reference-BL**](a-msds-valuetypereferencebl.md)                           | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-дов-Owner-BL**](a-ownerbl.md)                                                          | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Мссфу-30-POSIX-член-of**](a-mssfu30posixmemberof.md)                                     | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**нетбут-SCP-BL**](a-netbootscpbl.md)                                                       | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Не-Security-Member-BL**](a-nonsecuritymemberbl.md)                                        | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**NT-Security-дескриптор**](a-ntsecuritydescriptor.md)                                       | True      | [**Вверх**](c-top.md)<br/> |
| [**Obj-расп-имя**](a-distinguishedname.md)                                                   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Объект — Категория**](a-objectcategory.md)                                                    | True      | [**Вверх**](c-top.md)<br/> |
| [**Объектный класс**](a-objectclass.md)                                                          | True      | [**Вверх**](c-top.md)<br/> |
| [**Объект — GUID**](a-objectguid.md)                                                            | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Версия объекта**](a-objectversion.md)                                                      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Другие хорошо известные объекты**](a-otherwellknownobjects.md)                                    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Разделяемый атрибут-удаление-список**](a-partialattributedeletionlist.md)                      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Разделяемый атрибут-set**](a-partialattributeset.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Возможно — подстрочные**](a-possibleinferiors.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Прокси-объект-имя**](a-proxiedobjectname.md)                                             | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Прокси-адреса**](a-proxyaddresses.md)                                                    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Запрос — политика — BL**](a-querypolicybl.md)                                                     | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**RDN**](a-name.md)                                                                          | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**REPL-Уптодате-Vector**](a-repluptodatevector.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Отчеты**](a-directreports.md)                                                             | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Представители — от**](a-repsfrom.md)                                                                | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Представители — кому**](a-repsto.md)                                                                    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Редакции**](a-revision.md)                                                                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**SD-Rights-эффективен**](a-sdrightseffective.md)                                             | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Безопасность — идентификатор**](a-securityidentifier.md)                                            | Неверно     | **Доверенный домен**              |
| [**Server-Reference-BL**](a-serverreferencebl.md)                                             | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**"Показать" — "Расширенный просмотр"**](a-showinadvancedviewonly.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                       | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Структурный объектный класс**](a-structuralobjectclass.md)                                     | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Подразделы-ReFS**](a-subrefs.md)                                                                  | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**субсчемасубентри**](a-subschemasubentry.md)                                               | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Системные флаги**](a-systemflags.md)                                                          | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Trust-атрибуты**](a-trustattributes.md)                                                  | Неверно     | **Доверенный домен**              |
| [**Trust-auth-входящий**](a-trustauthincoming.md)                                             | Неверно     | **Доверенный домен**              |
| [**Trust-auth-исходящий трафик**](a-trustauthoutgoing.md)                                             | Неверно     | **Доверенный домен**              |
| [**Направление доверия**](a-trustdirection.md)                                                    | Неверно     | **Доверенный домен**              |
| [**Доверие — партнер**](a-trustpartner.md)                                                        | Неверно     | **Доверенный домен**              |
| [**Отношение доверия-POSIX-offset**](a-trustposixoffset.md)                                               | Неверно     | **Доверенный домен**              |
| [**Тип доверия**](a-trusttype.md)                                                              | Неверно     | **Доверенный домен**              |
| [**USN-изменено**](a-usnchanged.md)                                                            | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Созданный USN**](a-usncreated.md)                                                            | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**USN-DSA-Last-obj-removed**](a-usndsalastobjremoved.md)                                     | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**USN — межсайтовая**](a-usnintersite.md)                                                        | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                                    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Источник USN**](a-usnsource.md)                                                              | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**WBEM — путь**](a-wbempath.md)                                                                | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Хорошо известные объекты**](a-wellknownobjects.md)                                               | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**При изменении**](a-whenchanged.md)                                                          | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**При создании**](a-whencreated.md)                                                          | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**WWW — Главная страница**](a-wwwhomepage.md)                                                         | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**WWW-Page — другие**](a-url.md)                                                                | Неверно     | [**Вверх**](c-top.md)<br/> |



 

 





