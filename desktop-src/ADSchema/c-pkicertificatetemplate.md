---
title: PKI — класс сертификата-шаблона
description: Содержит сведения о сертификатах, выданных сервером сертификатов.
ms.assetid: 9b6ca989-058c-461b-ba3d-5b29ea15cbbc
ms.tgt_platform: multiple
keywords:
- PKI — схема AD класса сертификата-шаблона
- Схема AD класса Пкицертификатетемплате
topic_type:
- apiref
api_name:
- PKI-Certificate-Template
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e45c19969a09770e8b37b5bf9a45c4ff4d87806fc8e77b02e1a7e109981110c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753094"
---
# <a name="pki-certificate-template-class"></a>PKI — класс сертификата-шаблона

Содержит сведения о сертификатах, выданных сервером сертификатов.



| Ввод | Значение |
|-------------------|--------------------------------------|
| CN                | PKI — шаблон сертификата             |
| LDAP-отображаемое имя | пкицертификатетемплате               |
| Привилегия обновления  | \-                                   |
| Частота обновления  | \-                                   |
| Schema-ID-GUID    | e5209ca2-3bba-11d2-90cc-00c04fd91ab1 |



## <a name="implementations"></a>Варианты реализации решения

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server

-   [Атрибуты](#windows-2000-server-attributes)
-   [Расширенные права](#windows-2000-server-extended-rights)



| Ввод | Значение |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Неверно                                                                                        |
| Object-Category             | 1                                                                                            |
| По умолчанию — объект — Категория     | \-                                                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.177                                                                       |
| По умолчанию-скрытие значения        | 1                                                                                            |
| RDN-Атри-ID                  | [**Common-Name**](a-cn.md)<br/>                                                       |
| Подкласс                 | [**Вверх**](c-top.md)<br/>                                                              |
| Возможные старшие          | [**Контейнер**](c-container.md)                                                             |
| Вспомогательные классы           | \-                                                                                           |
| NT-Security-дескриптор      | О:БАГ: BAD: S:                                                                                 |
| Дескриптор безопасности по умолчанию | D: (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;;D А) (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;; SY) (A;; РПЛКЛОРК;;; СЛУЖБЫ |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-2000-server-attributes"></a>атрибуты сервера Windows 2000

этот класс содержит следующие атрибуты для сервера Windows 2000:



| attribute                                                                 | Обязательный | Унаследован от                                                 |
|---------------------------------------------------------------------------|-----------|--------------------------------------------------------------|
| [**Описание администратора**](a-admindescription.md)                           | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Имя администратора-отображение**](a-admindisplayname.md)                          | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Allowed-Attributes**](a-allowedattributes.md)                         | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Allowed-Attributes-эффективен**](a-allowedattributeseffective.md)      | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Allowed-Child-classes**](a-allowedchildclasses.md)                    | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Allowed-Child-classes-эффективен**](a-allowedchildclasseseffective.md) | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Плацдарм-Server-List-BL**](a-bridgeheadserverlistbl.md)             | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Каноническое имя**](a-canonicalname.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Common-Name**](a-cn.md)                                               | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Метка времени создания**](a-createtimestamp.md)                            | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Описание**](a-description.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Отображаемое имя**](a-displayname.md)                                     | Неверно     | **PKI — Certificate — шаблон** [ **сверху**](c-top.md)<br/> |
| [**Отображаемое имя — печатаемое**](a-displaynameprintable.md)                  | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**DSA-Signature**](a-dsasignature.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**DS-Core-распространение-данные**](a-dscorepropagationdata.md)               | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Имя расширения**](a-extensionname.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Метки**](a-flags.md)                                                  | Неверно     | **PKI — Certificate — шаблон** [ **сверху**](c-top.md)<br/> |
| [**Из записи**](a-fromentry.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)             | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                 | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Тип экземпляра**](a-instancetype.md)                                   | Верно      | [**Вверх**](c-top.md)<br/>                              |
| [**Является критически важным — системный объект**](a-iscriticalsystemobject.md)             | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Удалено**](a-isdeleted.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Входит в состав списка рассылки**](a-memberof.md)                                     | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Имеет права владельца**](a-isprivilegeholder.md)                        | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Последний-известный-родительский**](a-lastknownparent.md)                            | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Управляемые объекты**](a-managedobjects.md)                               | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**В основном**](a-masteredby.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Метка времени изменения**](a-modifytimestamp.md)                            | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-целостность-дочерняя — количество**](a-ms-ds-consistencychildcount.md)    | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-Consistencу-Guid**](a-ms-ds-consistencyguid.md)                 | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**нетбут-SCP-BL**](a-netbootscpbl.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Не-Security-Member-BL**](a-nonsecuritymemberbl.md)                   | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**NT-Security-дескриптор**](a-ntsecuritydescriptor.md)                  | Верно      | [**Вверх**](c-top.md)<br/>                              |
| [**Obj-расп-имя**](a-distinguishedname.md)                              | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Объект — Категория**](a-objectcategory.md)                               | Верно      | [**Вверх**](c-top.md)<br/>                              |
| [**Объектный класс**](a-objectclass.md)                                     | Верно      | [**Вверх**](c-top.md)<br/>                              |
| [**Объект — GUID**](a-objectguid.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Версия объекта**](a-objectversion.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Другие хорошо известные объекты**](a-otherwellknownobjects.md)               | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Разделяемый атрибут-удаление-список**](a-partialattributedeletionlist.md) | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Разделяемый атрибут-set**](a-partialattributeset.md)                    | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**PKI — критические расширения**](a-pkicriticalextensions.md)                | Неверно     | **PKI — шаблон сертификата**                                 |
| [**PKI-Default-CSP**](a-pkidefaultcsps.md)                              | Неверно     | **PKI — шаблон сертификата**                                 |
| [**PKI-Default-Key-Spec**](a-pkidefaultkeyspec.md)                       | Неверно     | **PKI — шаблон сертификата**                                 |
| [**PKI — доступ к регистрации**](a-pkienrollmentaccess.md)                    | Неверно     | **PKI — шаблон сертификата**                                 |
| [**PKI-срок действия — период**](a-pkiexpirationperiod.md)                    | Неверно     | **PKI — шаблон сертификата**                                 |
| [**PKI — использование расширенного ключа**](a-pkiextendedkeyusage.md)                   | Неверно     | **PKI — шаблон сертификата**                                 |
| [**PKI — использование ключа**](a-pkikeyusage.md)                                    | Неверно     | **PKI — шаблон сертификата**                                 |
| [**PKI-max-глубина выдачи**](a-pkimaxissuingdepth.md)                     | Неверно     | **PKI — шаблон сертификата**                                 |
| [**PKI — перекрытие — точка**](a-pkioverlapperiod.md)                          | Неверно     | **PKI — шаблон сертификата**                                 |
| [**Возможно — подстрочные**](a-possibleinferiors.md)                         | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Прокси-объект-имя**](a-proxiedobjectname.md)                        | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Прокси-адреса**](a-proxyaddresses.md)                               | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Запрос — политика — BL**](a-querypolicybl.md)                                | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**RDN**](a-name.md)                                                     | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                 | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**REPL-Уптодате-Vector**](a-repluptodatevector.md)                      | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Отчеты**](a-directreports.md)                                        | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Представители — от**](a-repsfrom.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Представители — кому**](a-repsto.md)                                               | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Редакции**](a-revision.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**SD-Rights-эффективен**](a-sdrightseffective.md)                        | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Server-Reference-BL**](a-serverreferencebl.md)                        | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**"Показать" — "Расширенный просмотр"**](a-showinadvancedviewonly.md)            | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Site-Object-BL**](a-siteobjectbl.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Подразделы-ReFS**](a-subrefs.md)                                             | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**субсчемасубентри**](a-subschemasubentry.md)                          | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Системные флаги**](a-systemflags.md)                                     | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**USN-изменено**](a-usnchanged.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Созданный USN**](a-usncreated.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**USN-DSA-Last-obj-removed**](a-usndsalastobjremoved.md)                | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**USN — межсайтовая**](a-usnintersite.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                               | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Источник USN**](a-usnsource.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**WBEM — путь**](a-wbempath.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Хорошо известные объекты**](a-wellknownobjects.md)                          | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**При изменении**](a-whenchanged.md)                                     | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**При создании**](a-whencreated.md)                                     | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**WWW — Главная страница**](a-wwwhomepage.md)                                    | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**WWW-Page — другие**](a-url.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/>                              |



## <a name="windows-2000-server-extended-rights"></a>расширенные права сервера Windows 2000

этот класс содержит следующие расширенные права для сервера Windows 2000:



| Общее имя                                                |
|------------------------------------------------------------|
| [**Регистрация сертификата**](r-certificate-enrollment.md) |



## <a name="windows-server-2003"></a>Windows Server 2003

-   [Атрибуты](#windows-server-2003-attributes)
-   [Расширенные права](#windows-server-2003-extended-rights)



| Ввод | Значение |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Неверно                                                                                        |
| Object-Category             | 1                                                                                            |
| По умолчанию — объект — Категория     | \-                                                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.177                                                                       |
| По умолчанию-скрытие значения        | 1                                                                                            |
| RDN-Атри-ID                  | [**Common-Name**](a-cn.md)<br/>                                                       |
| Подкласс                 | [**Вверх**](c-top.md)<br/>                                                              |
| Возможные старшие          | [**Контейнер**](c-container.md)                                                             |
| Вспомогательные классы           | \-                                                                                           |
| NT-Security-дескриптор      | О:БАГ: BAD: S:                                                                                 |
| Дескриптор безопасности по умолчанию | D: (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;;D А) (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;; SY) (A;; РПЛКЛОРК;;; СЛУЖБЫ |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2003-attributes"></a>Windows Атрибуты сервера 2003

этот класс содержит следующие атрибуты для Windows Server 2003:



| attribute                                                                               | Обязательный | Унаследован от                                                 |
|-----------------------------------------------------------------------------------------|-----------|--------------------------------------------------------------|
| [**Описание администратора**](a-admindescription.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Имя администратора-отображение**](a-admindisplayname.md)                                        | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Allowed-Attributes**](a-allowedattributes.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Allowed-Attributes-эффективен**](a-allowedattributeseffective.md)                    | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Allowed-Child-classes**](a-allowedchildclasses.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Allowed-Child-classes-эффективен**](a-allowedchildclasseseffective.md)               | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Плацдарм-Server-List-BL**](a-bridgeheadserverlistbl.md)                           | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Каноническое имя**](a-canonicalname.md)                                               | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Common-Name**](a-cn.md)                                                             | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Метка времени создания**](a-createtimestamp.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Описание**](a-description.md)                                                    | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Отображаемое имя**](a-displayname.md)                                                   | Неверно     | **PKI — Certificate — шаблон** [ **сверху**](c-top.md)<br/> |
| [**Отображаемое имя — печатаемое**](a-displaynameprintable.md)                                | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**DSA-Signature**](a-dsasignature.md)                                                 | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**DS-Core-распространение-данные**](a-dscorepropagationdata.md)                             | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Имя расширения**](a-extensionname.md)                                               | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Метки**](a-flags.md)                                                                | Неверно     | **PKI — Certificate — шаблон** [ **сверху**](c-top.md)<br/> |
| [**Из записи**](a-fromentry.md)                                                       | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                           | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                               | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Тип экземпляра**](a-instancetype.md)                                                 | Верно      | [**Вверх**](c-top.md)<br/>                              |
| [**Является критически важным — системный объект**](a-iscriticalsystemobject.md)                           | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Удалено**](a-isdeleted.md)                                                       | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Входит в состав списка рассылки**](a-memberof.md)                                                   | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Имеет права владельца**](a-isprivilegeholder.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Последний-известный-родительский**](a-lastknownparent.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Управляемые объекты**](a-managedobjects.md)                                             | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**В основном**](a-masteredby.md)                                                     | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Метка времени изменения**](a-modifytimestamp.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-COM-Партитионсетлинк**](a-mscom-partitionsetlink.md)                             | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-COM-Усерлинк**](a-mscom-userlink.md)                                             | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-примерно-Иммед-подчиненные**](a-msds-approx-immed-subordinates.md)             | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-целостность-дочерняя — количество**](a-ms-ds-consistencychildcount.md)                  | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-Consistencу-Guid**](a-ms-ds-consistencyguid.md)                               | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-Masterd-by**](a-msds-masteredby.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)                       | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-NC-REPL-курсоры**](a-msds-ncreplcursors.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-NC-REPL-Inbound-соседи**](a-msds-ncreplinboundneighbors.md)                | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-NC-REPL-Outbound-соседи**](a-msds-ncreploutboundneighbors.md)              | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-не-Members-BL**](a-msds-nonmembersbl.md)                                     | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                           | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-Operations-для-AZ-Role-BL**](a-msds-operationsforazrolebl.md)                 | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)                 | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-REPL-Attribute-Meta-Data**](a-msds-replattributemetadata.md)                  | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)                          | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-Tasks-для-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                           | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                           | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-дов-Owner-BL**](a-ownerbl.md)                                                   | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-PKI-Certificate-приложение-политика**](a-mspki-certificate-application-policy.md) | Неверно     | **PKI — шаблон сертификата**                                 |
| [**MS-PKI-Certificate-Name — флаг**](a-mspki-certificate-name-flag.md)                   | Неверно     | **PKI — шаблон сертификата**                                 |
| [**MS-PKI-Certificate-политика**](a-mspki-certificate-policy.md)                         | Неверно     | **PKI — шаблон сертификата**                                 |
| [**MS-PKI-CERT-Template-OID**](a-mspki-cert-template-oid.md)                           | Неверно     | **PKI — шаблон сертификата**                                 |
| [**Флаг MS-PKI-регистрации**](a-mspki-enrollment-flag.md)                               | Неверно     | **PKI — шаблон сертификата**                                 |
| [**MS-PKI-минимальный-ключ-размер**](a-mspki-minimal-key-size.md)                             | Неверно     | **PKI — шаблон сертификата**                                 |
| [**MS-PKI-закрытый-Key-флаг**](a-mspki-private-key-flag.md)                             | Неверно     | **PKI — шаблон сертификата**                                 |
| [**MS-PKI-RA-приложения — политики**](a-mspki-ra-application-policies.md)               | Неверно     | **PKI — шаблон сертификата**                                 |
| [**MS-PKI-RA-политики**](a-mspki-ra-policies.md)                                       | Неверно     | **PKI — шаблон сертификата**                                 |
| [**MS-PKI-RA-Signature**](a-mspki-ra-signature.md)                                     | Неверно     | **PKI — шаблон сертификата**                                 |
| [**MS-PKI-замена — шаблоны**](a-mspki-supersede-templates.md)                       | Неверно     | **PKI — шаблон сертификата**                                 |
| [**MS-PKI-Template — дополнительный номер редакции**](a-mspki-template-minor-revision.md)               | Неверно     | **PKI — шаблон сертификата**                                 |
| [**MS-PKI-Template-Schema-Version**](a-mspki-template-schema-version.md)               | Неверно     | **PKI — шаблон сертификата**                                 |
| [**нетбут-SCP-BL**](a-netbootscpbl.md)                                                | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Не-Security-Member-BL**](a-nonsecuritymemberbl.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**NT-Security-дескриптор**](a-ntsecuritydescriptor.md)                                | Верно      | [**Вверх**](c-top.md)<br/>                              |
| [**Obj-расп-имя**](a-distinguishedname.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Объект — Категория**](a-objectcategory.md)                                             | Верно      | [**Вверх**](c-top.md)<br/>                              |
| [**Объектный класс**](a-objectclass.md)                                                   | Верно      | [**Вверх**](c-top.md)<br/>                              |
| [**Объект — GUID**](a-objectguid.md)                                                     | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Версия объекта**](a-objectversion.md)                                               | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Другие хорошо известные объекты**](a-otherwellknownobjects.md)                             | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Разделяемый атрибут-удаление-список**](a-partialattributedeletionlist.md)               | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Разделяемый атрибут-set**](a-partialattributeset.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**PKI — критические расширения**](a-pkicriticalextensions.md)                              | Неверно     | **PKI — шаблон сертификата**                                 |
| [**PKI-Default-CSP**](a-pkidefaultcsps.md)                                            | Неверно     | **PKI — шаблон сертификата**                                 |
| [**PKI-Default-Key-Spec**](a-pkidefaultkeyspec.md)                                     | Неверно     | **PKI — шаблон сертификата**                                 |
| [**PKI — доступ к регистрации**](a-pkienrollmentaccess.md)                                  | Неверно     | **PKI — шаблон сертификата**                                 |
| [**PKI-срок действия — период**](a-pkiexpirationperiod.md)                                  | Неверно     | **PKI — шаблон сертификата**                                 |
| [**PKI — использование расширенного ключа**](a-pkiextendedkeyusage.md)                                 | Неверно     | **PKI — шаблон сертификата**                                 |
| [**PKI — использование ключа**](a-pkikeyusage.md)                                                  | Неверно     | **PKI — шаблон сертификата**                                 |
| [**PKI-max-глубина выдачи**](a-pkimaxissuingdepth.md)                                   | Неверно     | **PKI — шаблон сертификата**                                 |
| [**PKI — перекрытие — точка**](a-pkioverlapperiod.md)                                        | Неверно     | **PKI — шаблон сертификата**                                 |
| [**Возможно — подстрочные**](a-possibleinferiors.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Прокси-объект-имя**](a-proxiedobjectname.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Прокси-адреса**](a-proxyaddresses.md)                                             | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Запрос — политика — BL**](a-querypolicybl.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**RDN**](a-name.md)                                                                   | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                               | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**REPL-Уптодате-Vector**](a-repluptodatevector.md)                                    | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Отчеты**](a-directreports.md)                                                      | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Представители — от**](a-repsfrom.md)                                                         | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Представители — кому**](a-repsto.md)                                                             | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Редакции**](a-revision.md)                                                          | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**SD-Rights-эффективен**](a-sdrightseffective.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Server-Reference-BL**](a-serverreferencebl.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**"Показать" — "Расширенный просмотр"**](a-showinadvancedviewonly.md)                          | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Структурный объектный класс**](a-structuralobjectclass.md)                              | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Подразделы-ReFS**](a-subrefs.md)                                                           | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**субсчемасубентри**](a-subschemasubentry.md)                                        | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Системные флаги**](a-systemflags.md)                                                   | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**USN-изменено**](a-usnchanged.md)                                                     | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Созданный USN**](a-usncreated.md)                                                     | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**USN-DSA-Last-obj-removed**](a-usndsalastobjremoved.md)                              | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**USN — межсайтовая**](a-usnintersite.md)                                                 | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                             | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Источник USN**](a-usnsource.md)                                                       | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**WBEM — путь**](a-wbempath.md)                                                         | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Хорошо известные объекты**](a-wellknownobjects.md)                                        | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**При изменении**](a-whenchanged.md)                                                   | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**При создании**](a-whencreated.md)                                                   | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**WWW — Главная страница**](a-wwwhomepage.md)                                                  | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**WWW-Page — другие**](a-url.md)                                                         | Неверно     | [**Вверх**](c-top.md)<br/>                              |



## <a name="windows-server-2003-extended-rights"></a>Windows Расширенные права сервера 2003

этот класс содержит следующие расширенные права для Windows Server 2003:



| Общее имя                                                |
|------------------------------------------------------------|
| [**Регистрация сертификата**](r-certificate-enrollment.md) |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2

-   [Атрибуты](#windows-server-2003-r2-attributes)
-   [Расширенные права](#windows-server-2003-r2-extended-rights)



| Ввод | Значение |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Неверно                                                                                        |
| Object-Category             | 1                                                                                            |
| По умолчанию — объект — Категория     | \-                                                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.177                                                                       |
| По умолчанию-скрытие значения        | 1                                                                                            |
| RDN-Атри-ID                  | [**Common-Name**](a-cn.md)<br/>                                                       |
| Подкласс                 | [**Вверх**](c-top.md)<br/>                                                              |
| Возможные старшие          | [**Контейнер**](c-container.md)                                                             |
| Вспомогательные классы           | \-                                                                                           |
| NT-Security-дескриптор      | О:БАГ: BAD: S:                                                                                 |
| Дескриптор безопасности по умолчанию | D: (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;;D А) (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;; SY) (A;; РПЛКЛОРК;;; СЛУЖБЫ |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2003-r2-attributes"></a>Windows Атрибуты сервера 2003 R2

этот класс содержит следующие атрибуты для Windows Server 2003 R2:



| attribute                                                                               | Обязательный | Унаследован от                                                 |
|-----------------------------------------------------------------------------------------|-----------|--------------------------------------------------------------|
| [**Описание администратора**](a-admindescription.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Имя администратора-отображение**](a-admindisplayname.md)                                        | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Allowed-Attributes**](a-allowedattributes.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Allowed-Attributes-эффективен**](a-allowedattributeseffective.md)                    | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Allowed-Child-classes**](a-allowedchildclasses.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Allowed-Child-classes-эффективен**](a-allowedchildclasseseffective.md)               | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Плацдарм-Server-List-BL**](a-bridgeheadserverlistbl.md)                           | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Каноническое имя**](a-canonicalname.md)                                               | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Common-Name**](a-cn.md)                                                             | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Метка времени создания**](a-createtimestamp.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Описание**](a-description.md)                                                    | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Отображаемое имя**](a-displayname.md)                                                   | Неверно     | **PKI — Certificate — шаблон** [ **сверху**](c-top.md)<br/> |
| [**Отображаемое имя — печатаемое**](a-displaynameprintable.md)                                | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**DSA-Signature**](a-dsasignature.md)                                                 | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**DS-Core-распространение-данные**](a-dscorepropagationdata.md)                             | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Имя расширения**](a-extensionname.md)                                               | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Метки**](a-flags.md)                                                                | Неверно     | **PKI — Certificate — шаблон** [ **сверху**](c-top.md)<br/> |
| [**Из записи**](a-fromentry.md)                                                       | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                           | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                               | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Тип экземпляра**](a-instancetype.md)                                                 | Верно      | [**Вверх**](c-top.md)<br/>                              |
| [**Является критически важным — системный объект**](a-iscriticalsystemobject.md)                           | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Удалено**](a-isdeleted.md)                                                       | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Входит в состав списка рассылки**](a-memberof.md)                                                   | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Имеет права владельца**](a-isprivilegeholder.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Последний-известный-родительский**](a-lastknownparent.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Управляемые объекты**](a-managedobjects.md)                                             | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**В основном**](a-masteredby.md)                                                     | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Метка времени изменения**](a-modifytimestamp.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-COM-Партитионсетлинк**](a-mscom-partitionsetlink.md)                             | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-COM-Усерлинк**](a-mscom-userlink.md)                                             | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DFSR-Компутерреференцебл**](a-msdfsr-computerreferencebl.md)                     | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DFSR-Мемберреференцебл**](a-msdfsr-memberreferencebl.md)                         | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-примерно-Иммед-подчиненные**](a-msds-approx-immed-subordinates.md)             | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-целостность-дочерняя — количество**](a-ms-ds-consistencychildcount.md)                  | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-Consistencу-Guid**](a-ms-ds-consistencyguid.md)                               | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-Masterd-by**](a-msds-masteredby.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)                       | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-NC-REPL-курсоры**](a-msds-ncreplcursors.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-NC-REPL-Inbound-соседи**](a-msds-ncreplinboundneighbors.md)                | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-NC-REPL-Outbound-соседи**](a-msds-ncreploutboundneighbors.md)              | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-не-Members-BL**](a-msds-nonmembersbl.md)                                     | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                           | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-Operations-для-AZ-Role-BL**](a-msds-operationsforazrolebl.md)                 | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)                 | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-REPL-Attribute-Meta-Data**](a-msds-replattributemetadata.md)                  | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)                          | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-Tasks-для-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                           | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                           | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-дов-Owner-BL**](a-ownerbl.md)                                                   | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-PKI-Certificate-приложение-политика**](a-mspki-certificate-application-policy.md) | Неверно     | **PKI — шаблон сертификата**                                 |
| [**MS-PKI-Certificate-Name — флаг**](a-mspki-certificate-name-flag.md)                   | Неверно     | **PKI — шаблон сертификата**                                 |
| [**MS-PKI-Certificate-политика**](a-mspki-certificate-policy.md)                         | Неверно     | **PKI — шаблон сертификата**                                 |
| [**MS-PKI-CERT-Template-OID**](a-mspki-cert-template-oid.md)                           | Неверно     | **PKI — шаблон сертификата**                                 |
| [**Флаг MS-PKI-регистрации**](a-mspki-enrollment-flag.md)                               | Неверно     | **PKI — шаблон сертификата**                                 |
| [**MS-PKI-минимальный-ключ-размер**](a-mspki-minimal-key-size.md)                             | Неверно     | **PKI — шаблон сертификата**                                 |
| [**MS-PKI-закрытый-Key-флаг**](a-mspki-private-key-flag.md)                             | Неверно     | **PKI — шаблон сертификата**                                 |
| [**MS-PKI-RA-приложения — политики**](a-mspki-ra-application-policies.md)               | Неверно     | **PKI — шаблон сертификата**                                 |
| [**MS-PKI-RA-политики**](a-mspki-ra-policies.md)                                       | Неверно     | **PKI — шаблон сертификата**                                 |
| [**MS-PKI-RA-Signature**](a-mspki-ra-signature.md)                                     | Неверно     | **PKI — шаблон сертификата**                                 |
| [**MS-PKI-замена — шаблоны**](a-mspki-supersede-templates.md)                       | Неверно     | **PKI — шаблон сертификата**                                 |
| [**MS-PKI-Template — дополнительный номер редакции**](a-mspki-template-minor-revision.md)               | Неверно     | **PKI — шаблон сертификата**                                 |
| [**MS-PKI-Template-Schema-Version**](a-mspki-template-schema-version.md)               | Неверно     | **PKI — шаблон сертификата**                                 |
| [**Мссфу-30-POSIX-член-of**](a-mssfu30posixmemberof.md)                              | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**нетбут-SCP-BL**](a-netbootscpbl.md)                                                | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Не-Security-Member-BL**](a-nonsecuritymemberbl.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**NT-Security-дескриптор**](a-ntsecuritydescriptor.md)                                | Верно      | [**Вверх**](c-top.md)<br/>                              |
| [**Obj-расп-имя**](a-distinguishedname.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Объект — Категория**](a-objectcategory.md)                                             | Верно      | [**Вверх**](c-top.md)<br/>                              |
| [**Объектный класс**](a-objectclass.md)                                                   | Верно      | [**Вверх**](c-top.md)<br/>                              |
| [**Объект — GUID**](a-objectguid.md)                                                     | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Версия объекта**](a-objectversion.md)                                               | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Другие хорошо известные объекты**](a-otherwellknownobjects.md)                             | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Разделяемый атрибут-удаление-список**](a-partialattributedeletionlist.md)               | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Разделяемый атрибут-set**](a-partialattributeset.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**PKI — критические расширения**](a-pkicriticalextensions.md)                              | Неверно     | **PKI — шаблон сертификата**                                 |
| [**PKI-Default-CSP**](a-pkidefaultcsps.md)                                            | Неверно     | **PKI — шаблон сертификата**                                 |
| [**PKI-Default-Key-Spec**](a-pkidefaultkeyspec.md)                                     | Неверно     | **PKI — шаблон сертификата**                                 |
| [**PKI — доступ к регистрации**](a-pkienrollmentaccess.md)                                  | Неверно     | **PKI — шаблон сертификата**                                 |
| [**PKI-срок действия — период**](a-pkiexpirationperiod.md)                                  | Неверно     | **PKI — шаблон сертификата**                                 |
| [**PKI — использование расширенного ключа**](a-pkiextendedkeyusage.md)                                 | Неверно     | **PKI — шаблон сертификата**                                 |
| [**PKI — использование ключа**](a-pkikeyusage.md)                                                  | Неверно     | **PKI — шаблон сертификата**                                 |
| [**PKI-max-глубина выдачи**](a-pkimaxissuingdepth.md)                                   | Неверно     | **PKI — шаблон сертификата**                                 |
| [**PKI — перекрытие — точка**](a-pkioverlapperiod.md)                                        | Неверно     | **PKI — шаблон сертификата**                                 |
| [**Возможно — подстрочные**](a-possibleinferiors.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Прокси-объект-имя**](a-proxiedobjectname.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Прокси-адреса**](a-proxyaddresses.md)                                             | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Запрос — политика — BL**](a-querypolicybl.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**RDN**](a-name.md)                                                                   | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                               | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**REPL-Уптодате-Vector**](a-repluptodatevector.md)                                    | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Отчеты**](a-directreports.md)                                                      | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Представители — от**](a-repsfrom.md)                                                         | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Представители — кому**](a-repsto.md)                                                             | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Редакции**](a-revision.md)                                                          | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**SD-Rights-эффективен**](a-sdrightseffective.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Server-Reference-BL**](a-serverreferencebl.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**"Показать" — "Расширенный просмотр"**](a-showinadvancedviewonly.md)                          | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Структурный объектный класс**](a-structuralobjectclass.md)                              | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Подразделы-ReFS**](a-subrefs.md)                                                           | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**субсчемасубентри**](a-subschemasubentry.md)                                        | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Системные флаги**](a-systemflags.md)                                                   | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**USN-изменено**](a-usnchanged.md)                                                     | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Созданный USN**](a-usncreated.md)                                                     | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**USN-DSA-Last-obj-removed**](a-usndsalastobjremoved.md)                              | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**USN — межсайтовая**](a-usnintersite.md)                                                 | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                             | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Источник USN**](a-usnsource.md)                                                       | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**WBEM — путь**](a-wbempath.md)                                                         | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Хорошо известные объекты**](a-wellknownobjects.md)                                        | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**При изменении**](a-whenchanged.md)                                                   | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**При создании**](a-whencreated.md)                                                   | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**WWW — Главная страница**](a-wwwhomepage.md)                                                  | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**WWW-Page — другие**](a-url.md)                                                         | Неверно     | [**Вверх**](c-top.md)<br/>                              |



## <a name="windows-server-2003-r2-extended-rights"></a>Windows Расширенные права сервера 2003 R2

этот класс содержит следующие расширенные права для Windows Server 2003 R2:



| Общее имя                                                |
|------------------------------------------------------------|
| [**Регистрация сертификата**](r-certificate-enrollment.md) |



## <a name="windows-server-2008"></a>Windows Server 2008

-   [Атрибуты](#windows-server-2008-attributes)
-   [Расширенные права](#windows-server-2008-extended-rights)



| Ввод | Значение |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Неверно                                                                                        |
| Object-Category             | 1                                                                                            |
| По умолчанию — объект — Категория     | \-                                                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.177                                                                       |
| По умолчанию-скрытие значения        | 1                                                                                            |
| RDN-Атри-ID                  | [**Common-Name**](a-cn.md)<br/>                                                       |
| Подкласс                 | [**Вверх**](c-top.md)<br/>                                                              |
| Возможные старшие          | [**Контейнер**](c-container.md)                                                             |
| Вспомогательные классы           | \-                                                                                           |
| NT-Security-дескриптор      | О:БАГ: BAD: S:                                                                                 |
| Дескриптор безопасности по умолчанию | D: (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;;D А) (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;; SY) (A;; РПЛКЛОРК;;; СЛУЖБЫ |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2008-attributes"></a>Windows Атрибуты сервера 2008

этот класс содержит следующие атрибуты для Windows Server 2008:



| attribute                                                                               | Обязательный | Унаследован от                                                 |
|-----------------------------------------------------------------------------------------|-----------|--------------------------------------------------------------|
| [**Описание администратора**](a-admindescription.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Имя администратора-отображение**](a-admindisplayname.md)                                        | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Allowed-Attributes**](a-allowedattributes.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Allowed-Attributes-эффективен**](a-allowedattributeseffective.md)                    | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Allowed-Child-classes**](a-allowedchildclasses.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Allowed-Child-classes-эффективен**](a-allowedchildclasseseffective.md)               | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Плацдарм-Server-List-BL**](a-bridgeheadserverlistbl.md)                           | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Каноническое имя**](a-canonicalname.md)                                               | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Common-Name**](a-cn.md)                                                             | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Метка времени создания**](a-createtimestamp.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Описание**](a-description.md)                                                    | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Отображаемое имя**](a-displayname.md)                                                   | Неверно     | **PKI — Certificate — шаблон** [ **сверху**](c-top.md)<br/> |
| [**Отображаемое имя — печатаемое**](a-displaynameprintable.md)                                | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**DSA-Signature**](a-dsasignature.md)                                                 | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**DS-Core-распространение-данные**](a-dscorepropagationdata.md)                             | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Имя расширения**](a-extensionname.md)                                               | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Метки**](a-flags.md)                                                                | Неверно     | **PKI — Certificate — шаблон** [ **сверху**](c-top.md)<br/> |
| [**Из записи**](a-fromentry.md)                                                       | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                           | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                               | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Тип экземпляра**](a-instancetype.md)                                                 | Верно      | [**Вверх**](c-top.md)<br/>                              |
| [**Является критически важным — системный объект**](a-iscriticalsystemobject.md)                           | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Удалено**](a-isdeleted.md)                                                       | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Входит в состав списка рассылки**](a-memberof.md)                                                   | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Имеет права владельца**](a-isprivilegeholder.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Последний-известный-родительский**](a-lastknownparent.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Управляемые объекты**](a-managedobjects.md)                                             | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**В основном**](a-masteredby.md)                                                     | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Метка времени изменения**](a-modifytimestamp.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-COM-Партитионсетлинк**](a-mscom-partitionsetlink.md)                             | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-COM-Усерлинк**](a-mscom-userlink.md)                                             | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DFSR-Компутерреференцебл**](a-msdfsr-computerreferencebl.md)                     | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DFSR-Мемберреференцебл**](a-msdfsr-memberreferencebl.md)                         | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-примерно-Иммед-подчиненные**](a-msds-approx-immed-subordinates.md)             | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-Аусентикатедто-Аккаунтлист**](a-msds-authenticatedtoaccountlist.md)          | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-целостность-дочерняя — количество**](a-ms-ds-consistencychildcount.md)                  | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-Consistencу-Guid**](a-ms-ds-consistencyguid.md)                               | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS--домен — для**](a-msds-isdomainfor.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-является-Full-реплика для**](a-msds-isfullreplicafor.md)                            | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-является-partial-реплика для**](a-msds-ispartialreplicafor.md)                      | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                     | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-Masterd-by**](a-msds-masteredby.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)                       | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-NC-REPL-курсоры**](a-msds-ncreplcursors.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-NC-REPL-Inbound-соседи**](a-msds-ncreplinboundneighbors.md)                | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-NC-REPL-Outbound-соседи**](a-msds-ncreploutboundneighbors.md)              | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)           | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-NC-Type**](a-msds-nctype.md)                                                  | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-не-Members-BL**](a-msds-nonmembersbl.md)                                     | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                           | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-Operations-для-AZ-Role-BL**](a-msds-operationsforazrolebl.md)                 | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)                 | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-Principal-Name**](a-msds-principalname.md)                                    | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-PSO — применяется**](a-msds-psoapplied.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-REPL-Attribute-Meta-Data**](a-msds-replattributemetadata.md)                  | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)                          | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-выявил-DSA**](a-msds-revealeddsas.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-выводит-List-BL**](a-msds-revealedlistbl.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-Tasks-для-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                           | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                           | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-дов-Owner-BL**](a-ownerbl.md)                                                   | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-PKI-Certificate-приложение-политика**](a-mspki-certificate-application-policy.md) | Неверно     | **PKI — шаблон сертификата**                                 |
| [**MS-PKI-Certificate-Name — флаг**](a-mspki-certificate-name-flag.md)                   | Неверно     | **PKI — шаблон сертификата**                                 |
| [**MS-PKI-Certificate-политика**](a-mspki-certificate-policy.md)                         | Неверно     | **PKI — шаблон сертификата**                                 |
| [**MS-PKI-CERT-Template-OID**](a-mspki-cert-template-oid.md)                           | Неверно     | **PKI — шаблон сертификата**                                 |
| [**Флаг MS-PKI-регистрации**](a-mspki-enrollment-flag.md)                               | Неверно     | **PKI — шаблон сертификата**                                 |
| [**MS-PKI-минимальный-ключ-размер**](a-mspki-minimal-key-size.md)                             | Неверно     | **PKI — шаблон сертификата**                                 |
| [**MS-PKI-закрытый-Key-флаг**](a-mspki-private-key-flag.md)                             | Нет     | **PKI — шаблон сертификата**                                 |
| [**MS-PKI-RA-приложения — политики**](a-mspki-ra-application-policies.md)               | Нет     | **PKI — шаблон сертификата**                                 |
| [**MS-PKI-RA-политики**](a-mspki-ra-policies.md)                                       | Нет     | **PKI — шаблон сертификата**                                 |
| [**MS-PKI-RA-Signature**](a-mspki-ra-signature.md)                                     | Нет     | **PKI — шаблон сертификата**                                 |
| [**MS-PKI-замена — шаблоны**](a-mspki-supersede-templates.md)                       | Нет     | **PKI — шаблон сертификата**                                 |
| [**MS-PKI-Template — дополнительный номер редакции**](a-mspki-template-minor-revision.md)               | Нет     | **PKI — шаблон сертификата**                                 |
| [**MS-PKI-Template-Schema-Version**](a-mspki-template-schema-version.md)               | Нет     | **PKI — шаблон сертификата**                                 |
| [**Мссфу-30-POSIX-член-of**](a-mssfu30posixmemberof.md)                              | Нет     | [**Вверх**](c-top.md)<br/>                              |
| [**нетбут-SCP-BL**](a-netbootscpbl.md)                                                | Нет     | [**Вверх**](c-top.md)<br/>                              |
| [**Не-Security-Member-BL**](a-nonsecuritymemberbl.md)                                 | Нет     | [**Вверх**](c-top.md)<br/>                              |
| [**NT-Security-дескриптор**](a-ntsecuritydescriptor.md)                                | Верно      | [**Вверх**](c-top.md)<br/>                              |
| [**Obj-расп-имя**](a-distinguishedname.md)                                            | Нет     | [**Вверх**](c-top.md)<br/>                              |
| [**Объект — Категория**](a-objectcategory.md)                                             | Верно      | [**Вверх**](c-top.md)<br/>                              |
| [**Объектный класс**](a-objectclass.md)                                                   | Верно      | [**Вверх**](c-top.md)<br/>                              |
| [**Объект — GUID**](a-objectguid.md)                                                     | Нет     | [**Вверх**](c-top.md)<br/>                              |
| [**Версия объекта**](a-objectversion.md)                                               | Нет     | [**Вверх**](c-top.md)<br/>                              |
| [**Другие хорошо известные объекты**](a-otherwellknownobjects.md)                             | Нет     | [**Вверх**](c-top.md)<br/>                              |
| [**Разделяемый атрибут-удаление-список**](a-partialattributedeletionlist.md)               | Нет     | [**Вверх**](c-top.md)<br/>                              |
| [**Разделяемый атрибут-set**](a-partialattributeset.md)                                  | Нет     | [**Вверх**](c-top.md)<br/>                              |
| [**PKI — критические расширения**](a-pkicriticalextensions.md)                              | Нет     | **PKI — шаблон сертификата**                                 |
| [**PKI-Default-CSP**](a-pkidefaultcsps.md)                                            | Нет     | **PKI — шаблон сертификата**                                 |
| [**PKI-Default-Key-Spec**](a-pkidefaultkeyspec.md)                                     | Нет     | **PKI — шаблон сертификата**                                 |
| [**PKI — доступ к регистрации**](a-pkienrollmentaccess.md)                                  | Нет     | **PKI — шаблон сертификата**                                 |
| [**PKI-срок действия — период**](a-pkiexpirationperiod.md)                                  | Нет     | **PKI — шаблон сертификата**                                 |
| [**PKI — использование расширенного ключа**](a-pkiextendedkeyusage.md)                                 | Нет     | **PKI — шаблон сертификата**                                 |
| [**PKI — использование ключа**](a-pkikeyusage.md)                                                  | Нет     | **PKI — шаблон сертификата**                                 |
| [**PKI-max-глубина выдачи**](a-pkimaxissuingdepth.md)                                   | Нет     | **PKI — шаблон сертификата**                                 |
| [**PKI — перекрытие — точка**](a-pkioverlapperiod.md)                                        | Нет     | **PKI — шаблон сертификата**                                 |
| [**Возможно — подстрочные**](a-possibleinferiors.md)                                       | Нет     | [**Вверх**](c-top.md)<br/>                              |
| [**Прокси-объект-имя**](a-proxiedobjectname.md)                                      | Нет     | [**Вверх**](c-top.md)<br/>                              |
| [**Прокси-адреса**](a-proxyaddresses.md)                                             | Нет     | [**Вверх**](c-top.md)<br/>                              |
| [**Запрос — политика — BL**](a-querypolicybl.md)                                              | Нет     | [**Вверх**](c-top.md)<br/>                              |
| [**RDN**](a-name.md)                                                                   | Нет     | [**Вверх**](c-top.md)<br/>                              |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                               | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**REPL-Уптодате-Vector**](a-repluptodatevector.md)                                    | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Отчеты**](a-directreports.md)                                                      | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Представители — от**](a-repsfrom.md)                                                         | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Представители — кому**](a-repsto.md)                                                             | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Редакции**](a-revision.md)                                                          | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**SD-Rights-эффективен**](a-sdrightseffective.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Server-Reference-BL**](a-serverreferencebl.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**"Показать" — "Расширенный просмотр"**](a-showinadvancedviewonly.md)                          | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Структурный объектный класс**](a-structuralobjectclass.md)                              | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Подразделы-ReFS**](a-subrefs.md)                                                           | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**субсчемасубентри**](a-subschemasubentry.md)                                        | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Системные флаги**](a-systemflags.md)                                                   | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**USN-изменено**](a-usnchanged.md)                                                     | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Созданный USN**](a-usncreated.md)                                                     | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**USN-DSA-Last-obj-removed**](a-usndsalastobjremoved.md)                              | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**USN — межсайтовая**](a-usnintersite.md)                                                 | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                             | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Источник USN**](a-usnsource.md)                                                       | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**WBEM — путь**](a-wbempath.md)                                                         | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Хорошо известные объекты**](a-wellknownobjects.md)                                        | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**При изменении**](a-whenchanged.md)                                                   | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**При создании**](a-whencreated.md)                                                   | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**WWW — Главная страница**](a-wwwhomepage.md)                                                  | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**WWW-Page — другие**](a-url.md)                                                         | Неверно     | [**Вверх**](c-top.md)<br/>                              |



## <a name="windows-server-2008-extended-rights"></a>Windows Расширенные права сервера 2008

этот класс содержит следующие расширенные права для Windows Server 2008:



| Общее имя                                                |
|------------------------------------------------------------|
| [**Регистрация сертификата**](r-certificate-enrollment.md) |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2

-   [Атрибуты](#windows-server-2008-r2-attributes)
-   [Расширенные права](#windows-server-2008-r2-extended-rights)



| Ввод | Значение |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Неверно                                                                                        |
| Object-Category             | 1                                                                                            |
| По умолчанию — объект — Категория     | \-                                                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.177                                                                       |
| По умолчанию-скрытие значения        | 1                                                                                            |
| RDN-Атри-ID                  | [**Common-Name**](a-cn.md)<br/>                                                       |
| Подкласс                 | [**Вверх**](c-top.md)<br/>                                                              |
| Возможные старшие          | [**Контейнер**](c-container.md)                                                             |
| Вспомогательные классы           | \-                                                                                           |
| NT-Security-дескриптор      | О:БАГ: BAD: S:                                                                                 |
| Дескриптор безопасности по умолчанию | D: (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;;D А) (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;; SY) (A;; РПЛКЛОРК;;; СЛУЖБЫ |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2008-r2-attributes"></a>Windows Атрибуты сервера 2008 R2

этот класс содержит следующие атрибуты для Windows Server 2008 R2:



| attribute                                                                               | Обязательный | Унаследован от                                                 |
|-----------------------------------------------------------------------------------------|-----------|--------------------------------------------------------------|
| [**Описание администратора**](a-admindescription.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Имя администратора-отображение**](a-admindisplayname.md)                                        | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Allowed-Attributes**](a-allowedattributes.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Allowed-Attributes-эффективен**](a-allowedattributeseffective.md)                    | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Allowed-Child-classes**](a-allowedchildclasses.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Allowed-Child-classes-эффективен**](a-allowedchildclasseseffective.md)               | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Плацдарм-Server-List-BL**](a-bridgeheadserverlistbl.md)                           | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Каноническое имя**](a-canonicalname.md)                                               | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Common-Name**](a-cn.md)                                                             | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Метка времени создания**](a-createtimestamp.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Описание**](a-description.md)                                                    | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Отображаемое имя**](a-displayname.md)                                                   | Неверно     | **PKI — Certificate — шаблон** [ **сверху**](c-top.md)<br/> |
| [**Отображаемое имя — печатаемое**](a-displaynameprintable.md)                                | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**DSA-Signature**](a-dsasignature.md)                                                 | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**DS-Core-распространение-данные**](a-dscorepropagationdata.md)                             | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Имя расширения**](a-extensionname.md)                                               | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Метки**](a-flags.md)                                                                | Неверно     | **PKI — Certificate — шаблон** [ **сверху**](c-top.md)<br/> |
| [**Из записи**](a-fromentry.md)                                                       | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                           | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                               | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Тип экземпляра**](a-instancetype.md)                                                 | Верно      | [**Вверх**](c-top.md)<br/>                              |
| [**Является критически важным — системный объект**](a-iscriticalsystemobject.md)                           | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Удалено**](a-isdeleted.md)                                                       | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Входит в состав списка рассылки**](a-memberof.md)                                                   | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Имеет права владельца**](a-isprivilegeholder.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Является перезапущенным**](a-isrecycled.md)                                                     | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Последний-известный-родительский**](a-lastknownparent.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Управляемые объекты**](a-managedobjects.md)                                             | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**В основном**](a-masteredby.md)                                                     | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Метка времени изменения**](a-modifytimestamp.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-COM-Партитионсетлинк**](a-mscom-partitionsetlink.md)                             | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-COM-Усерлинк**](a-mscom-userlink.md)                                             | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DFSR-Компутерреференцебл**](a-msdfsr-computerreferencebl.md)                     | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DFSR-Мемберреференцебл**](a-msdfsr-memberreferencebl.md)                         | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-примерно-Иммед-подчиненные**](a-msds-approx-immed-subordinates.md)             | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-Аусентикатедто-Аккаунтлист**](a-msds-authenticatedtoaccountlist.md)          | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-целостность-дочерняя — количество**](a-ms-ds-consistencychildcount.md)                  | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-Consistencу-Guid**](a-ms-ds-consistencyguid.md)                               | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Поддержка MS-DS-Feature-BL**](a-msds-enabledfeaturebl.md)                             | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)                    | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS--домен — для**](a-msds-isdomainfor.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-является-Full-реплика для**](a-msds-isfullreplicafor.md)                            | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-является-partial-реплика для**](a-msds-ispartialreplicafor.md)                      | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                     | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                                     | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-локально-эффективное удаление — время**](a-msds-localeffectivedeletiontime.md)        | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-Local-эффективен — время перезапуска**](a-msds-localeffectiverecycletime.md)          | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-Masterd-by**](a-msds-masteredby.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)                       | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-NC-REPL-курсоры**](a-msds-ncreplcursors.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-NC-REPL-Inbound-соседи**](a-msds-ncreplinboundneighbors.md)                | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-NC-REPL-Outbound-соседи**](a-msds-ncreploutboundneighbors.md)              | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)           | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-NC-Type**](a-msds-nctype.md)                                                  | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-не-Members-BL**](a-msds-nonmembersbl.md)                                     | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                           | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-Оидтограуп-Link-BL**](a-msds-oidtogrouplinkbl.md)                             | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-Operations-для-AZ-Role-BL**](a-msds-operationsforazrolebl.md)                 | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)                 | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-Principal-Name**](a-msds-principalname.md)                                    | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-PSO — применяется**](a-msds-psoapplied.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-REPL-Attribute-Meta-Data**](a-msds-replattributemetadata.md)                  | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)                          | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-выявил-DSA**](a-msds-revealeddsas.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-выводит-List-BL**](a-msds-revealedlistbl.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-Tasks-для-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                           | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                           | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-дов-Owner-BL**](a-ownerbl.md)                                                   | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-PKI-Certificate-приложение-политика**](a-mspki-certificate-application-policy.md) | Неверно     | **PKI — шаблон сертификата**                                 |
| [**MS-PKI-Certificate-Name — флаг**](a-mspki-certificate-name-flag.md)                   | Неверно     | **PKI — шаблон сертификата**                                 |
| [**MS-PKI-Certificate-политика**](a-mspki-certificate-policy.md)                         | Неверно     | **PKI — шаблон сертификата**                                 |
| [**MS-PKI-CERT-Template-OID**](a-mspki-cert-template-oid.md)                           | Неверно     | **PKI — шаблон сертификата**                                 |
| [**Флаг MS-PKI-регистрации**](a-mspki-enrollment-flag.md)                               | Неверно     | **PKI — шаблон сертификата**                                 |
| [**MS-PKI-минимальный-ключ-размер**](a-mspki-minimal-key-size.md)                             | Неверно     | **PKI — шаблон сертификата**                                 |
| [**MS-PKI-закрытый-Key-флаг**](a-mspki-private-key-flag.md)                             | Неверно     | **PKI — шаблон сертификата**                                 |
| [**MS-PKI-RA-приложения — политики**](a-mspki-ra-application-policies.md)               | Неверно     | **PKI — шаблон сертификата**                                 |
| [**MS-PKI-RA-политики**](a-mspki-ra-policies.md)                                       | Неверно     | **PKI — шаблон сертификата**                                 |
| [**MS-PKI-RA-Signature**](a-mspki-ra-signature.md)                                     | Неверно     | **PKI — шаблон сертификата**                                 |
| [**MS-PKI-замена — шаблоны**](a-mspki-supersede-templates.md)                       | Неверно     | **PKI — шаблон сертификата**                                 |
| [**MS-PKI-Template — дополнительный номер редакции**](a-mspki-template-minor-revision.md)               | Неверно     | **PKI — шаблон сертификата**                                 |
| [**MS-PKI-Template-Schema-Version**](a-mspki-template-schema-version.md)               | Неверно     | **PKI — шаблон сертификата**                                 |
| [**Мссфу-30-POSIX-член-of**](a-mssfu30posixmemberof.md)                              | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**нетбут-SCP-BL**](a-netbootscpbl.md)                                                | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Не-Security-Member-BL**](a-nonsecuritymemberbl.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**NT-Security-дескриптор**](a-ntsecuritydescriptor.md)                                | Верно      | [**Вверх**](c-top.md)<br/>                              |
| [**Obj-расп-имя**](a-distinguishedname.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Объект — Категория**](a-objectcategory.md)                                             | Верно      | [**Вверх**](c-top.md)<br/>                              |
| [**Объектный класс**](a-objectclass.md)                                                   | Верно      | [**Вверх**](c-top.md)<br/>                              |
| [**Объект — GUID**](a-objectguid.md)                                                     | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Версия объекта**](a-objectversion.md)                                               | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Другие хорошо известные объекты**](a-otherwellknownobjects.md)                             | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Разделяемый атрибут-удаление-список**](a-partialattributedeletionlist.md)               | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Разделяемый атрибут-set**](a-partialattributeset.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**PKI — критические расширения**](a-pkicriticalextensions.md)                              | Неверно     | **PKI — шаблон сертификата**                                 |
| [**PKI-Default-CSP**](a-pkidefaultcsps.md)                                            | Неверно     | **PKI — шаблон сертификата**                                 |
| [**PKI-Default-Key-Spec**](a-pkidefaultkeyspec.md)                                     | Неверно     | **PKI — шаблон сертификата**                                 |
| [**PKI — доступ к регистрации**](a-pkienrollmentaccess.md)                                  | Неверно     | **PKI — шаблон сертификата**                                 |
| [**PKI-срок действия — период**](a-pkiexpirationperiod.md)                                  | Неверно     | **PKI — шаблон сертификата**                                 |
| [**PKI — использование расширенного ключа**](a-pkiextendedkeyusage.md)                                 | Неверно     | **PKI — шаблон сертификата**                                 |
| [**PKI — использование ключа**](a-pkikeyusage.md)                                                  | Неверно     | **PKI — шаблон сертификата**                                 |
| [**PKI-max-глубина выдачи**](a-pkimaxissuingdepth.md)                                   | Неверно     | **PKI — шаблон сертификата**                                 |
| [**PKI — перекрытие — точка**](a-pkioverlapperiod.md)                                        | Неверно     | **PKI — шаблон сертификата**                                 |
| [**Возможно — подстрочные**](a-possibleinferiors.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Прокси-объект-имя**](a-proxiedobjectname.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Прокси-адреса**](a-proxyaddresses.md)                                             | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Запрос — политика — BL**](a-querypolicybl.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**RDN**](a-name.md)                                                                   | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                               | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**REPL-Уптодате-Vector**](a-repluptodatevector.md)                                    | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Отчеты**](a-directreports.md)                                                      | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Представители — от**](a-repsfrom.md)                                                         | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Представители — кому**](a-repsto.md)                                                             | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Редакции**](a-revision.md)                                                          | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**SD-Rights-эффективен**](a-sdrightseffective.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Server-Reference-BL**](a-serverreferencebl.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**"Показать" — "Расширенный просмотр"**](a-showinadvancedviewonly.md)                          | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Структурный объектный класс**](a-structuralobjectclass.md)                              | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Подразделы-ReFS**](a-subrefs.md)                                                           | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**субсчемасубентри**](a-subschemasubentry.md)                                        | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Системные флаги**](a-systemflags.md)                                                   | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**USN-изменено**](a-usnchanged.md)                                                     | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Созданный USN**](a-usncreated.md)                                                     | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**USN-DSA-Last-obj-removed**](a-usndsalastobjremoved.md)                              | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**USN — межсайтовая**](a-usnintersite.md)                                                 | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                             | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Источник USN**](a-usnsource.md)                                                       | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**WBEM — путь**](a-wbempath.md)                                                         | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Хорошо известные объекты**](a-wellknownobjects.md)                                        | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**При изменении**](a-whenchanged.md)                                                   | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**При создании**](a-whencreated.md)                                                   | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**WWW — Главная страница**](a-wwwhomepage.md)                                                  | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**WWW-Page — другие**](a-url.md)                                                         | Неверно     | [**Вверх**](c-top.md)<br/>                              |



## <a name="windows-server-2008-r2-extended-rights"></a>Windows Расширенные права сервера 2008 R2

этот класс содержит следующие расширенные права для Windows Server 2008 R2:



| Общее имя                                                |
|------------------------------------------------------------|
| [**Регистрация сертификата**](r-certificate-enrollment.md) |



## <a name="windows-server-2012"></a>Windows Server 2012

-   [Атрибуты](#windows-server-2012-attributes)
-   [Расширенные права](#windows-server-2012-extended-rights)



| Ввод | Значение |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Неверно                                                                                        |
| Object-Category             | 1                                                                                            |
| По умолчанию — объект — Категория     | \-                                                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.177                                                                       |
| По умолчанию-скрытие значения        | 1                                                                                            |
| RDN-Атри-ID                  | [**Common-Name**](a-cn.md)<br/>                                                       |
| Подкласс                 | [**Вверх**](c-top.md)<br/>                                                              |
| Возможные старшие          | [**Контейнер**](c-container.md)                                                             |
| Вспомогательные классы           | \-                                                                                           |
| NT-Security-дескриптор      | О:БАГ: BAD: S:                                                                                 |
| Дескриптор безопасности по умолчанию | D: (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;;D А) (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;; SY) (A;; РПЛКЛОРК;;; СЛУЖБЫ |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2012-attributes"></a>Windows Server 2012 Атрибута

Этот класс содержит следующие атрибуты для Windows Server 2012:



| attribute                                                                                    | Обязательный | Унаследован от                                                 |
|----------------------------------------------------------------------------------------------|-----------|--------------------------------------------------------------|
| [**Описание администратора**](a-admindescription.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Имя администратора-отображение**](a-admindisplayname.md)                                             | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Allowed-Attributes**](a-allowedattributes.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Allowed-Attributes-эффективен**](a-allowedattributeseffective.md)                         | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Allowed-Child-classes**](a-allowedchildclasses.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Allowed-Child-classes-эффективен**](a-allowedchildclasseseffective.md)                    | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Плацдарм-Server-List-BL**](a-bridgeheadserverlistbl.md)                                | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Каноническое имя**](a-canonicalname.md)                                                    | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Common-Name**](a-cn.md)                                                                  | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Метка времени создания**](a-createtimestamp.md)                                               | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Описание**](a-description.md)                                                         | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Отображаемое имя**](a-displayname.md)                                                        | Неверно     | **PKI — Certificate — шаблон** [ **сверху**](c-top.md)<br/> |
| [**Отображаемое имя — печатаемое**](a-displaynameprintable.md)                                     | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**DSA-Signature**](a-dsasignature.md)                                                      | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**DS-Core-распространение-данные**](a-dscorepropagationdata.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Имя расширения**](a-extensionname.md)                                                    | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Метки**](a-flags.md)                                                                     | Неверно     | **PKI — Certificate — шаблон** [ **сверху**](c-top.md)<br/> |
| [**Из записи**](a-fromentry.md)                                                            | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                                | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                                    | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                                   | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Тип экземпляра**](a-instancetype.md)                                                      | Верно      | [**Вверх**](c-top.md)<br/>                              |
| [**Является критически важным — системный объект**](a-iscriticalsystemobject.md)                                | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Удалено**](a-isdeleted.md)                                                            | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Входит в состав списка рассылки**](a-memberof.md)                                                        | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Имеет права владельца**](a-isprivilegeholder.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Является перезапущенным**](a-isrecycled.md)                                                          | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Последний-известный-родительский**](a-lastknownparent.md)                                               | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Управляемые объекты**](a-managedobjects.md)                                                  | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**В основном**](a-masteredby.md)                                                          | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Метка времени изменения**](a-modifytimestamp.md)                                               | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-COM-Партитионсетлинк**](a-mscom-partitionsetlink.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-COM-Усерлинк**](a-mscom-userlink.md)                                                  | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DFSR-Компутерреференцебл**](a-msdfsr-computerreferencebl.md)                          | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DFSR-Мемберреференцебл**](a-msdfsr-memberreferencebl.md)                              | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-примерно-Иммед-подчиненные**](a-msds-approx-immed-subordinates.md)                  | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-Аусентикатедто-Аккаунтлист**](a-msds-authenticatedtoaccountlist.md)               | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-ClaimSet-shares-возможные значения-with-BL**](a-msds-claimsharespossiblevalueswithbl.md) | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-целостность-дочерняя — количество**](a-ms-ds-consistencychildcount.md)                       | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-Consistencу-Guid**](a-ms-ds-consistencyguid.md)                                    | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Поддержка MS-DS-Feature-BL**](a-msds-enabledfeaturebl.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)                         | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS--домен — для**](a-msds-isdomainfor.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-является-Full-реплика для**](a-msds-isfullreplicafor.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-является-partial-реплика для**](a-msds-ispartialreplicafor.md)                           | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-является-PRIMARY-Computer-для**](a-msds-isprimarycomputerfor.md)                         | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-локально-эффективное удаление — время**](a-msds-localeffectivedeletiontime.md)             | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-Local-эффективен — время перезапуска**](a-msds-localeffectiverecycletime.md)               | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-Masterd-by**](a-msds-masteredby.md)                                               | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)                            | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-Members-of-Resource-Property-List-BL**](a-msds-membersofresourcepropertylistbl.md) | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-NC-REPL-курсоры**](a-msds-ncreplcursors.md)                                        | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-NC-REPL-Inbound-соседи**](a-msds-ncreplinboundneighbors.md)                     | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-NC-REPL-Outbound-соседи**](a-msds-ncreploutboundneighbors.md)                   | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)                | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-NC-Type**](a-msds-nctype.md)                                                       | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-не-Members-BL**](a-msds-nonmembersbl.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                                | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-Оидтограуп-Link-BL**](a-msds-oidtogrouplinkbl.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-Operations-для-AZ-Role-BL**](a-msds-operationsforazrolebl.md)                      | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)                      | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-Principal-Name**](a-msds-principalname.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-PSO — применяется**](a-msds-psoapplied.md)                                               | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-REPL-Attribute-Meta-Data**](a-msds-replattributemetadata.md)                       | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)                               | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-выявил-DSA**](a-msds-revealeddsas.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-выводит-List-BL**](a-msds-revealedlistbl.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-Tasks-для-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                                | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                                | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**ms-DS-TDO-Egress-BL**](a-msds-tdoegressbl.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-TDO-входящий трафик — BL**](a-msds-tdoingressbl.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-DS-value-type-Reference-BL**](a-msds-valuetypereferencebl.md)                         | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-дов-Owner-BL**](a-ownerbl.md)                                                        | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**MS-PKI-Certificate-приложение-политика**](a-mspki-certificate-application-policy.md)      | Неверно     | **PKI — шаблон сертификата**                                 |
| [**MS-PKI-Certificate-Name — флаг**](a-mspki-certificate-name-flag.md)                        | Неверно     | **PKI — шаблон сертификата**                                 |
| [**MS-PKI-Certificate-политика**](a-mspki-certificate-policy.md)                              | Неверно     | **PKI — шаблон сертификата**                                 |
| [**MS-PKI-CERT-Template-OID**](a-mspki-cert-template-oid.md)                                | Неверно     | **PKI — шаблон сертификата**                                 |
| [**Флаг MS-PKI-регистрации**](a-mspki-enrollment-flag.md)                                    | Неверно     | **PKI — шаблон сертификата**                                 |
| [**MS-PKI-минимальный-ключ-размер**](a-mspki-minimal-key-size.md)                                  | Неверно     | **PKI — шаблон сертификата**                                 |
| [**MS-PKI-закрытый-Key-флаг**](a-mspki-private-key-flag.md)                                  | Неверно     | **PKI — шаблон сертификата**                                 |
| [**MS-PKI-RA-приложения — политики**](a-mspki-ra-application-policies.md)                    | Неверно     | **PKI — шаблон сертификата**                                 |
| [**MS-PKI-RA-политики**](a-mspki-ra-policies.md)                                            | Неверно     | **PKI — шаблон сертификата**                                 |
| [**MS-PKI-RA-Signature**](a-mspki-ra-signature.md)                                          | Неверно     | **PKI — шаблон сертификата**                                 |
| [**MS-PKI-замена — шаблоны**](a-mspki-supersede-templates.md)                            | Неверно     | **PKI — шаблон сертификата**                                 |
| [**MS-PKI-Template — дополнительный номер редакции**](a-mspki-template-minor-revision.md)                    | Неверно     | **PKI — шаблон сертификата**                                 |
| [**MS-PKI-Template-Schema-Version**](a-mspki-template-schema-version.md)                    | Неверно     | **PKI — шаблон сертификата**                                 |
| [**Мссфу-30-POSIX-член-of**](a-mssfu30posixmemberof.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**нетбут-SCP-BL**](a-netbootscpbl.md)                                                     | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Не-Security-Member-BL**](a-nonsecuritymemberbl.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**NT-Security-дескриптор**](a-ntsecuritydescriptor.md)                                     | Верно      | [**Вверх**](c-top.md)<br/>                              |
| [**Obj-расп-имя**](a-distinguishedname.md)                                                 | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Объект — Категория**](a-objectcategory.md)                                                  | Верно      | [**Вверх**](c-top.md)<br/>                              |
| [**Объектный класс**](a-objectclass.md)                                                        | Верно      | [**Вверх**](c-top.md)<br/>                              |
| [**Объект — GUID**](a-objectguid.md)                                                          | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Версия объекта**](a-objectversion.md)                                                    | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Другие хорошо известные объекты**](a-otherwellknownobjects.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Разделяемый атрибут-удаление-список**](a-partialattributedeletionlist.md)                    | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Разделяемый атрибут-set**](a-partialattributeset.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**PKI — критические расширения**](a-pkicriticalextensions.md)                                   | Неверно     | **PKI — шаблон сертификата**                                 |
| [**PKI-Default-CSP**](a-pkidefaultcsps.md)                                                 | Неверно     | **PKI — шаблон сертификата**                                 |
| [**PKI-Default-Key-Spec**](a-pkidefaultkeyspec.md)                                          | Неверно     | **PKI — шаблон сертификата**                                 |
| [**PKI — доступ к регистрации**](a-pkienrollmentaccess.md)                                       | Неверно     | **PKI — шаблон сертификата**                                 |
| [**PKI-срок действия — период**](a-pkiexpirationperiod.md)                                       | Неверно     | **PKI — шаблон сертификата**                                 |
| [**PKI — использование расширенного ключа**](a-pkiextendedkeyusage.md)                                      | Неверно     | **PKI — шаблон сертификата**                                 |
| [**PKI — использование ключа**](a-pkikeyusage.md)                                                       | Неверно     | **PKI — шаблон сертификата**                                 |
| [**PKI-max-глубина выдачи**](a-pkimaxissuingdepth.md)                                        | Неверно     | **PKI — шаблон сертификата**                                 |
| [**PKI — перекрытие — точка**](a-pkioverlapperiod.md)                                             | Неверно     | **PKI — шаблон сертификата**                                 |
| [**Возможно — подстрочные**](a-possibleinferiors.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Прокси-объект-имя**](a-proxiedobjectname.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Прокси-адреса**](a-proxyaddresses.md)                                                  | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Запрос — политика — BL**](a-querypolicybl.md)                                                   | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**RDN**](a-name.md)                                                                        | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                                    | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**REPL-Уптодате-Vector**](a-repluptodatevector.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Отчеты**](a-directreports.md)                                                           | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Представители — от**](a-repsfrom.md)                                                              | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Представители — кому**](a-repsto.md)                                                                  | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Редакции**](a-revision.md)                                                               | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**SD-Rights-эффективен**](a-sdrightseffective.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Server-Reference-BL**](a-serverreferencebl.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**"Показать" — "Расширенный просмотр"**](a-showinadvancedviewonly.md)                               | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                     | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Структурный объектный класс**](a-structuralobjectclass.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Подразделы-ReFS**](a-subrefs.md)                                                                | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**субсчемасубентри**](a-subschemasubentry.md)                                             | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Системные флаги**](a-systemflags.md)                                                        | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**USN-изменено**](a-usnchanged.md)                                                          | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Созданный USN**](a-usncreated.md)                                                          | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**USN-DSA-Last-obj-removed**](a-usndsalastobjremoved.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**USN — межсайтовая**](a-usnintersite.md)                                                      | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                                  | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Источник USN**](a-usnsource.md)                                                            | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**WBEM — путь**](a-wbempath.md)                                                              | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**Хорошо известные объекты**](a-wellknownobjects.md)                                             | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**При изменении**](a-whenchanged.md)                                                        | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**При создании**](a-whencreated.md)                                                        | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**WWW — Главная страница**](a-wwwhomepage.md)                                                       | Неверно     | [**Вверх**](c-top.md)<br/>                              |
| [**WWW-Page — другие**](a-url.md)                                                              | Неверно     | [**Вверх**](c-top.md)<br/>                              |



## <a name="windows-server-2012-extended-rights"></a>Windows Server 2012 Расширенные права

Этот класс содержит следующие расширенные права для Windows Server 2012:



| Общее имя                                                |
|------------------------------------------------------------|
| [**Регистрация сертификата**](r-certificate-enrollment.md) |



 

 





