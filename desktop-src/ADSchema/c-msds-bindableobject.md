---
title: класс объектов MS-DS-BIND-Object
description: Вспомогательный класс для представления связываемого объекта. Любой определяемый пользователем класс, представляющий сущность, которую можно использовать для привязки к каталогу (то есть пользователю), должна включать этот вспомогательный класс.
ms.assetid: 181b3e2b-9442-4f11-9af7-4697491115f3
ms.tgt_platform: multiple
keywords:
- Схема AD класса объектов в службе MS-DS-BIND
- Схема AD для класса msDS-BindableObject
topic_type:
- apiref
api_name:
- ms-DS-Bindable-Object
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: feb69036ad9cd33b8f0a60f5356192acbea8dd71
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893193"
---
# <a name="ms-ds-bindable-object-class"></a>класс объектов MS-DS-BIND-Object

Вспомогательный класс для представления связываемого объекта. Любой определяемый пользователем класс, представляющий сущность, которую можно использовать для привязки к каталогу (то есть пользователю), должна включать этот вспомогательный класс.



| Ввод | Значение |
|-------------------|--------------------------------------|
| CN                | Объект MS-DS-BIND-Object                |
| LDAP-отображаемое имя | msDS-BindableObject                  |
| Привилегия обновления  | \-                                   |
| Частота обновления  | \-                                   |
| Schema-ID-GUID    | 89f4a69f-4416-6b49-821d-6e3c4a0ff802 |



## <a name="implementations"></a>Варианты реализации решения

-   [**ADAM**](#adam-attributes)

## <a name="adam"></a>ADAM

-   [Атрибуты](#adam-attributes)



| Ввод | Значение |
|-----------------------------|--------------------------------------------------------------|
| System-Only                 | Неверно                                                        |
| Object-Category             | 3                                                            |
| По умолчанию — объект — Категория     | \-                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.244                                       |
| По умолчанию-скрытие значения        | 1                                                            |
| RDN-Атри-ID                  | \-                                                           |
| Подкласс                 | [**Безопасность — участник**](c-securityprincipal.md)<br/> |
| Возможные старшие          | \-                                                           |
| Вспомогательные классы           | \-                                                           |
| NT-Security-дескриптор      | О:БАГ: BAD: S:                                                 |
| Дескриптор безопасности по умолчанию | \-                                                           |
| System-Flags                | 0x00000010                                                   |



## <a name="adam-attributes"></a>Атрибуты ADAM

Этот класс содержит следующие атрибуты для ADAM:



| attribute                                                                                      | Обязательный | Унаследован от                                                                                 |
|------------------------------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------|
| [**Учетная запись — истекает срок действия**](a-accountexpires.md)                                                    | Неверно     | **Объект MS-DS-BIND-Object**                                                                    |
| [**Описание администратора**](a-admindescription.md)                                                | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Имя администратора-отображение**](a-admindisplayname.md)                                               | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Allowed-Attributes**](a-allowedattributes.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Allowed-Attributes-эффективен**](a-allowedattributeseffective.md)                           | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Allowed-Child-classes**](a-allowedchildclasses.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Allowed-Child-classes-эффективен**](a-allowedchildclasseseffective.md)                      | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Ошибка-пароль-время**](a-badpasswordtime.md)                                                 | Неверно     | **Объект MS-DS-BIND-Object**                                                                    |
| [**Bad-PWD-число**](a-badpwdcount.md)                                                         | Неверно     | **Объект MS-DS-BIND-Object**                                                                    |
| [**Плацдарм-Server-List-BL**](a-bridgeheadserverlistbl.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Каноническое имя**](a-canonicalname.md)                                                      | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Common-Name**](a-cn.md)                                                                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Метка времени создания**](a-createtimestamp.md)                                                 | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Описание**](a-description.md)                                                           | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Отображаемое имя**](a-displayname.md)                                                          | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**DSA-Signature**](a-dsasignature.md)                                                        | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**DS-Core-распространение-данные**](a-dscorepropagationdata.md)                                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Из записи**](a-fromentry.md)                                                              | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                                     | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Тип экземпляра**](a-instancetype.md)                                                        | True      | [**Вверх**](c-top.md)<br/>                                                              |
| [**Является критически важным — системный объект**](a-iscriticalsystemobject.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Удалено**](a-isdeleted.md)                                                              | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Входит в состав списка рассылки**](a-memberof.md)                                                          | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Последний-известный-родительский**](a-lastknownparent.md)                                                 | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Метка времени последнего входа**](a-lastlogontimestamp.md)                                           | Неверно     | **Объект MS-DS-BIND-Object**                                                                    |
| [**Время блокировки**](a-lockouttime.md)                                                          | Неверно     | **Объект MS-DS-BIND-Object**                                                                    |
| [**Управляемые объекты**](a-managedobjects.md)                                                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**В основном**](a-masteredby.md)                                                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Метка времени изменения**](a-modifytimestamp.md)                                                 | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**MS-DS-примерно-Иммед-подчиненные**](a-msds-approx-immed-subordinates.md)                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**MS-DS-целостность-дочерняя — количество**](a-ms-ds-consistencychildcount.md)                         | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**MS-DS-Consistencу-Guid**](a-ms-ds-consistencyguid.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**MS-DS-Disabled-for-Instances-BL**](a-msds-disableforinstancesbl.md)                         | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**MS-DS-Masterd-by**](a-msds-masteredby.md)                                                 | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**MS-DS-NC-REPL-курсоры**](a-msds-ncreplcursors.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**MS-DS-NC-REPL-Inbound-соседи**](a-msds-ncreplinboundneighbors.md)                       | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**MS-DS-NC-REPL-Outbound-соседи**](a-msds-ncreploutboundneighbors.md)                     | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**MS-DS-REPL-Attribute-Meta-Data**](a-msds-replattributemetadata.md)                         | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**MS-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**MS-DS-Service-Account-BL**](a-msds-serviceaccountbl.md)                                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**MS-DS-пользователь-учетная запись — автоматическая блокировка**](a-ms-ds-useraccountautolocked.md)                        | Неверно     | **Объект MS-DS-BIND-Object**                                                                    |
| [**MS-DS-User-Account-Control — вычисленный**](a-msds-user-account-control-computed.md)            | Неверно     | **Объект MS-DS-BIND-Object**                                                                    |
| [**MS-DS-User-Account-Disabled**](a-msds-useraccountdisabled.md)                              | Неверно     | **Объект MS-DS-BIND-Object**                                                                    |
| [**MS-DS-User-не-Expires — пароль**](a-msds-userdontexpirepassword.md)                       | Неверно     | **Объект MS-DS-BIND-Object**                                                                    |
| [**MS-DS-User-encrypted-Text-Password-Allowed**](a-ms-ds-userencryptedtextpasswordallowed.md) | Неверно     | **Объект MS-DS-BIND-Object**                                                                    |
| [**MS-DS-User-Password-срок действия истек**](a-msds-userpasswordexpired.md)                              | Неверно     | **Объект MS-DS-BIND-Object**                                                                    |
| [**MS-DS-User-Password — не требуется**](a-ms-ds-userpasswordnotrequired.md)                    | Неверно     | **Объект MS-DS-BIND-Object**                                                                    |
| [**NT-PWD-History**](a-ntpwdhistory.md)                                                       | Неверно     | **Объект MS-DS-BIND-Object**                                                                    |
| [**NT-Security-дескриптор**](a-ntsecuritydescriptor.md)                                       | True      | [**Безопасность — участник**](c-securityprincipal.md)<br/> [**Вверх**](c-top.md)<br/> |
| [**Obj-расп-имя**](a-distinguishedname.md)                                                   | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Объект — Категория**](a-objectcategory.md)                                                    | True      | [**Вверх**](c-top.md)<br/>                                                              |
| [**Объектный класс**](a-objectclass.md)                                                          | True      | [**Вверх**](c-top.md)<br/>                                                              |
| [**Объект — GUID**](a-objectguid.md)                                                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Идентификатор безопасности объекта**](a-objectsid.md)                                                              | True      | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                 |
| [**Версия объекта**](a-objectversion.md)                                                      | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Другие хорошо известные объекты**](a-otherwellknownobjects.md)                                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Разделяемый атрибут-удаление-список**](a-partialattributedeletionlist.md)                      | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Разделяемый атрибут-set**](a-partialattributeset.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Возможно — подстрочные**](a-possibleinferiors.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Прокси-объект-имя**](a-proxiedobjectname.md)                                             | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Прокси-адреса**](a-proxyaddresses.md)                                                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**PWD-Last-Set**](a-pwdlastset.md)                                                           | Неверно     | **Объект MS-DS-BIND-Object**                                                                    |
| [**Запрос — политика — BL**](a-querypolicybl.md)                                                     | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**RDN**](a-name.md)                                                                          | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**REPL-Уптодате-Vector**](a-repluptodatevector.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Представители — от**](a-repsfrom.md)                                                                | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Представители — кому**](a-repsto.md)                                                                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Редакции**](a-revision.md)                                                                 | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**SD-Rights-эффективен**](a-sdrightseffective.md)                                             | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Server-Reference-BL**](a-serverreferencebl.md)                                             | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**"Показать" — "Расширенный просмотр"**](a-showinadvancedviewonly.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                       | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Структурный объектный класс**](a-structuralobjectclass.md)                                     | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Подразделы-ReFS**](a-subrefs.md)                                                                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**субсчемасубентри**](a-subschemasubentry.md)                                               | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Дополнительные учетные данные**](a-supplementalcredentials.md)                                  | Неверно     | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                 |
| [**Системные флаги**](a-systemflags.md)                                                          | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Группы токенов**](a-tokengroups.md)                                                          | Неверно     | [**Безопасность — участник**](c-securityprincipal.md)<br/>                                 |
| [**Юникод-PWD**](a-unicodepwd.md)                                                            | Неверно     | **Объект MS-DS-BIND-Object**                                                                    |
| [**USN-изменено**](a-usnchanged.md)                                                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Созданный USN**](a-usncreated.md)                                                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**USN-DSA-Last-obj-removed**](a-usndsalastobjremoved.md)                                     | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**USN — межсайтовая**](a-usnintersite.md)                                                        | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Источник USN**](a-usnsource.md)                                                              | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**WBEM — путь**](a-wbempath.md)                                                                | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**Хорошо известные объекты**](a-wellknownobjects.md)                                               | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**При изменении**](a-whenchanged.md)                                                          | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**При создании**](a-whencreated.md)                                                          | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**WWW — Главная страница**](a-wwwhomepage.md)                                                         | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |
| [**WWW-Page — другие**](a-url.md)                                                                | Неверно     | [**Вверх**](c-top.md)<br/>                                                              |



 

 





