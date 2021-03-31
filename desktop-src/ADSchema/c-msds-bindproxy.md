---
title: класс MS-DS-BIND-proxy
description: Вспомогательный класс для представления прокси-сервера привязки в AD/AM.
ms.assetid: de837926-9d40-41f6-8c56-c4e436fd66b6
ms.tgt_platform: multiple
keywords:
- Схема AD класса прокси-сервера MS-DS-BIND
- Схема AD для класса msDS-BindProxy
topic_type:
- apiref
api_name:
- ms-DS-Bind-Proxy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db4fbb48080c83c3ea82b72c598e2a5a06037562
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804223"
---
# <a name="ms-ds-bind-proxy-class"></a>класс MS-DS-BIND-proxy

Вспомогательный класс для представления прокси-сервера привязки в AD/AM. BIND proxy ссылается на субъект безопасности Windows с помощью атрибута objectSid. Когда пользователь выполняет простую привязку к объекту BIND-proxy, привязка перенаправляется соответствующему субъекту Windows.



| Ввод | Значение |
|-------------------|--------------------------------------|
| CN                | MS-DS-BIND-proxy                     |
| LDAP-отображаемое имя | msDS-BindProxy                       |
| Привилегия обновления  | \-                                   |
| Частота обновления  | \-                                   |
| Schema-ID-GUID    | 717532ab-66e9-684d-a62b-8af1e3985e2f |



## <a name="implementations"></a>Варианты реализации решения

-   [**ADAM**](#adam-attributes)

## <a name="adam"></a>ADAM

-   [Атрибуты](#adam-attributes)



| Ввод | Значение |
|-----------------------------|---------------------------------|
| System-Only                 | Неверно                           |
| Object-Category             | 3                               |
| По умолчанию — объект — Категория     | \-                              |
| Governs-Id                  | 1.2.840.113556.1.5.245          |
| По умолчанию-скрытие значения        | 1                               |
| RDN-Атри-ID                  | \-                              |
| Подкласс                 | [**Вверх**](c-top.md)<br/> |
| Возможные старшие          | \-                              |
| Вспомогательные классы           | \-                              |
| NT-Security-дескриптор      | О:БАГ: BAD: S:                    |
| Дескриптор безопасности по умолчанию | \-                              |
| System-Flags                | 0x00000010                      |



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
| [**Каноническое имя**](a-canonicalname.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Common-Name**](a-cn.md)                                                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Метка времени создания**](a-createtimestamp.md)                              | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Описание**](a-description.md)                                        | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Отображаемое имя**](a-displayname.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**DSA-Signature**](a-dsasignature.md)                                     | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**DS-Core-распространение-данные**](a-dscorepropagationdata.md)                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Из записи**](a-fromentry.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Тип экземпляра**](a-instancetype.md)                                     | True      | [**Вверх**](c-top.md)<br/> |
| [**Является критически важным — системный объект**](a-iscriticalsystemobject.md)               | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Удалено**](a-isdeleted.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Входит в состав списка рассылки**](a-memberof.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Последний-известный-родительский**](a-lastknownparent.md)                              | Неверно     | [**Вверх**](c-top.md)<br/> |
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
| [**MS-DS-Principal-Name**](a-msds-principalname.md)                        | Неверно     | **MS-DS-BIND-proxy**            |
| [**MS-DS-REPL-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)              | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**MS-DS-Service-Account-BL**](a-msds-serviceaccountbl.md)                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**NT-Security-дескриптор**](a-ntsecuritydescriptor.md)                    | True      | [**Вверх**](c-top.md)<br/> |
| [**Obj-расп-имя**](a-distinguishedname.md)                                | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Объект — Категория**](a-objectcategory.md)                                 | True      | [**Вверх**](c-top.md)<br/> |
| [**Объектный класс**](a-objectclass.md)                                       | True      | [**Вверх**](c-top.md)<br/> |
| [**Объект — GUID**](a-objectguid.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Идентификатор безопасности объекта**](a-objectsid.md)                                           | True      | **MS-DS-BIND-proxy**            |
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
| [**Представители — от**](a-repsfrom.md)                                             | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Представители — кому**](a-repsto.md)                                                 | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Редакции**](a-revision.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**SD-Rights-эффективен**](a-sdrightseffective.md)                          | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**"Показать" — "Расширенный просмотр"**](a-showinadvancedviewonly.md)              | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Структурный объектный класс**](a-structuralobjectclass.md)                  | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Подразделы-ReFS**](a-subrefs.md)                                               | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**субсчемасубентри**](a-subschemasubentry.md)                            | Неверно     | [**Вверх**](c-top.md)<br/> |
| [**Системные флаги**](a-systemflags.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/> |
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



 

 





