---
title: Класс Contact
description: Этот класс содержит сведения о лице или компании, к которым может потребоваться регулярно обращаться.
ms.assetid: 2372ea2b-1ac3-4173-950f-4ee00138fe22
ms.tgt_platform: multiple
keywords:
- Схема AD класса Contact
- Схема AD класса Contact
topic_type:
- apiref
api_name:
- Contact
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4b54d5929e11382c1680090adf376f670d8610fd767a193e349a31f54c1f2cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119021892"
---
# <a name="contact-class"></a>Класс Contact

Этот класс содержит сведения о лице или компании, к которым может потребоваться регулярно обращаться.



| Ввод | Значение |
|-------------------|------------------------------------------------|
| CN                | Contact                                        |
| LDAP-отображаемое имя | contact                                        |
| Привилегия обновления  | Это значение задается администратором домена. |
| Частота обновления  | \-                                             |
| Schema-ID-GUID    | 5cb41ed0-0e4c-11d0-a286-00aa003049e2           |



## <a name="implementations"></a>Варианты реализации решения

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server

-   [Атрибуты](#windows-2000-server-attributes)
-   [Наборы свойств](#windows-2000-server-property-sets)



| Ввод | Значение |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Нет.                                                                                        |
| Object-Category             | 1                                                                                            |
| По умолчанию — объект — Категория     | [**Человек**](c-person.md)<br/>                                                        |
| Governs-Id                  | 1.2.840.113556.1.5.15                                                                        |
| По умолчанию-скрытие значения        | 0                                                                                            |
| RDN-Атри-ID                  | [**Common-Name**](a-cn.md)<br/>                                                       |
| Подкласс                 | [**Organizational-Person**](c-organizationalperson.md)<br/>                           |
| Возможные старшие          | [](c-domaindns.md)[**Организационное подразделение** домена DNS](c-organizationalunit.md)         |
| Вспомогательные классы           | [**Mail-получатель**](c-mailrecipient.md) (система)                                           |
| NT-Security-дескриптор      | О:БАГ: BAD: S:                                                                                 |
| Дескриптор безопасности по умолчанию | D: (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;;D А) (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;; SY) (A;; РПЛКЛОРК;;; СЛУЖБЫ |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-2000-server-attributes"></a>атрибуты сервера Windows 2000

этот класс содержит следующие атрибуты для сервера Windows 2000:



| attribute                                                                 | Обязательный | Унаследован от                                                                                                                           |
|---------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**Дополнительные сведения**](a-notes.md)                                 | Нет.     | **Contact**                                                                                                                            |
| [**Адрес**](a-streetaddress.md)                                        | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Адрес — Домашняя страница**](a-homepostaladdress.md)                               | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Описание администратора**](a-admindescription.md)                           | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Имя администратора-отображение**](a-admindisplayname.md)                          | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Attributes**](a-allowedattributes.md)                         | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Attributes-эффективен**](a-allowedattributeseffective.md)      | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Child-classes**](a-allowedchildclasses.md)                    | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Child-classes-эффективен**](a-allowedchildclasseseffective.md) | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Средство**](a-assistant.md)                                          | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Плацдарм-Server-List-BL**](a-bridgeheadserverlistbl.md)             | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Каноническое имя**](a-canonicalname.md)                                 | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Комментировать**](a-info.md)                                                 | Нет.     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**Common-Name**](a-cn.md)                                               | Верно      | **Контактное** [ **лицо**](c-person.md)<br/> [**Получатель почты**](c-mailrecipient.md)<br/> [**Вверх**](c-top.md)<br/> |
| [**Company**](a-company.md)                                              | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Код страны**](a-countrycode.md)                                     | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Название страны**](a-c.md)                                               | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Метка времени создания**](a-createtimestamp.md)                            | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Отдел**](a-department.md)                                        | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Описание**](a-description.md)                                      | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Целевой индикатор**](a-destinationindicator.md)                   | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Отображаемое имя**](a-displayname.md)                                     | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Отображаемое имя — печатаемое**](a-displaynameprintable.md)                  | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Отдел**](a-division.md)                                            | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**DSA-Signature**](a-dsasignature.md)                                   | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**DS-Core-распространение-данные**](a-dscorepropagationdata.md)               | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Адреса электронной почты**](a-mail.md)                                        | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Идентификатор сотрудника**](a-employeeid.md)                                       | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Имя расширения**](a-extensionname.md)                                 | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Факс-телефон — номер**](a-facsimiletelephonenumber.md)          | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Метки**](a-flags.md)                                                  | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Из записи**](a-fromentry.md)                                         | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)             | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                 | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Мусор-Coll-период**](a-garbagecollperiod.md)                        | Нет.     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**Квалификатор поколения**](a-generationqualifier.md)                     | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Заданное имя**](a-givenname.md)                                         | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Инициалы**](a-initials.md)                                            | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Тип экземпляра**](a-instancetype.md)                                   | Верно      | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Международный-ISDN-номер**](a-internationalisdnnumber.md)            | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Является критически важным — системный объект**](a-iscriticalsystemobject.md)             | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Удалено**](a-isdeleted.md)                                         | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Входит в состав списка рассылки**](a-memberof.md)                                     | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Имеет права владельца**](a-isprivilegeholder.md)                        | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Последний-известный-родительский**](a-lastknownparent.md)                            | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Legacy-Exchange-DN**](a-legacyexchangedn.md)                          | Нет.     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**Локальное имя**](a-l.md)                                              | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Эмблема**](a-thumbnaillogo.md)                                           | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Управляемые объекты**](a-managedobjects.md)                               | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Manager**](a-manager.md)                                              | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**В основном**](a-masteredby.md)                                       | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**МХС-или-Address**](a-mhsoraddress.md)                                  | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Метка времени изменения**](a-modifytimestamp.md)                            | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-целостность-дочерняя — количество**](a-ms-ds-consistencychildcount.md)    | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Consistencу-Guid**](a-ms-ds-consistencyguid.md)                 | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**нетбут-SCP-BL**](a-netbootscpbl.md)                                  | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Не-Security-Member-BL**](a-nonsecuritymemberbl.md)                   | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**NT-Security-дескриптор**](a-ntsecuritydescriptor.md)                  | Верно      | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Obj-расп-имя**](a-distinguishedname.md)                              | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Объект — Категория**](a-objectcategory.md)                               | Верно      | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Объектный класс**](a-objectclass.md)                                     | Верно      | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Объект — GUID**](a-objectguid.md)                                       | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Версия объекта**](a-objectversion.md)                                 | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Организация — имя подразделения**](a-ou.md)                                  | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Название организации**](a-o.md)                                          | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Другие — почтовый ящик**](a-othermailbox.md)                                   | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Другое имя**](a-middlename.md)                                        | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Другие хорошо известные объекты**](a-otherwellknownobjects.md)               | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Разделяемый атрибут-удаление-список**](a-partialattributedeletionlist.md) | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Разделяемый атрибут-set**](a-partialattributeset.md)                    | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Личный заголовок**](a-personaltitle.md)                                 | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон-Fax — другие**](a-otherfacsimiletelephonenumber.md)                | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон-Home — другие**](a-otherhomephone.md)                              | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон-Home — основной**](a-homephone.md)                                 | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон-Ip — другие**](a-otheripphone.md)                                  | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон-Ip-Primary**](a-ipphone.md)                                     | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон-ISDN-Primary**](a-primaryinternationalisdnnumber.md)            | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон-Mobile — другие**](a-othermobile.md)                               | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон — Mobile — Primary**](a-mobile.md)                                  | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон-Office-Other**](a-othertelephone.md)                            | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон-пейджер — другие**](a-otherpager.md)                                 | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон-пейджер-основной**](a-pager.md)                                    | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**физическая доставка — Office-имя**](a-physicaldeliveryofficename.md)     | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Снимки**](a-thumbnailphoto.md)                                       | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Возможно — подстрочные**](a-possibleinferiors.md)                         | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Почтовый адрес**](a-postaladdress.md)                                 | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Почтовый код**](a-postalcode.md)                                       | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**флажок после Office**](a-postofficebox.md)                                | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Предпочтительный метод доставки**](a-preferreddeliverymethod.md)            | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Прокси-объект-имя**](a-proxiedobjectname.md)                        | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Прокси-адреса**](a-proxyaddresses.md)                               | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Запрос — политика — BL**](a-querypolicybl.md)                                | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**RDN**](a-name.md)                                                     | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Зарегистрированный адрес**](a-registeredaddress.md)                         | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                 | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**REPL-Уптодате-Vector**](a-repluptodatevector.md)                      | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Отчеты**](a-directreports.md)                                        | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Представители — от**](a-repsfrom.md)                                           | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Представители — кому**](a-repsto.md)                                               | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Редакции**](a-revision.md)                                            | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**SD-Rights-эффективен**](a-sdrightseffective.md)                        | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**См. также**](a-seealso.md)                                             | Нет.     | [**Человек**](c-person.md)<br/>                                                                                                  |
| [**Server-Reference-BL**](a-serverreferencebl.md)                        | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Отображение в адресной книге**](a-showinaddressbook.md)                       | Нет.     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**"Показать" — "Расширенный просмотр"**](a-showinadvancedviewonly.md)            | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Site-Object-BL**](a-siteobjectbl.md)                                  | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**State-или-провинция-Name**](a-st.md)                                    | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Улица-адрес**](a-street.md)                                        | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Подразделы-ReFS**](a-subrefs.md)                                             | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**субсчемасубентри**](a-subschemasubentry.md)                          | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Образование**](a-sn.md)                                                   | Нет.     | [**Человек**](c-person.md)<br/>                                                                                                  |
| [**Системные флаги**](a-systemflags.md)                                     | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Номер телефона**](a-telephonenumber.md)                             | Нет.     | [**Человек**](c-person.md)<br/> [**Получатель почты**](c-mailrecipient.md)<br/>                                             |
| [**Teletex — идентификатор терминала**](a-teletexterminalidentifier.md)        | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Номер телекса**](a-telexnumber.md)                                     | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Номер телекса (первичный)**](a-primarytelexnumber.md)                             | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Текст — страна**](a-co.md)                                              | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**С текстовым кодированием или адресом**](a-textencodedoraddress.md)                 | Нет.     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**Название**](a-title.md)                                                  | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**User-CERT**](a-usercert.md)                                           | Нет.     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**Комментарий пользователя**](a-comment.md)                                         | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Пароль пользователя**](a-userpassword.md)                                   | Нет.     | [**Человек**](c-person.md)<br/>                                                                                                  |
| [**Пользователь-SMIME-Certificate**](a-usersmimecertificate.md)                  | Нет.     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**USN-изменено**](a-usnchanged.md)                                       | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Созданный USN**](a-usncreated.md)                                       | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**USN-DSA-Last-obj-removed**](a-usndsalastobjremoved.md)                | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**USN — межсайтовая**](a-usnintersite.md)                                   | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                               | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Источник USN**](a-usnsource.md)                                         | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**WBEM — путь**](a-wbempath.md)                                           | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Хорошо известные объекты**](a-wellknownobjects.md)                          | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**При изменении**](a-whenchanged.md)                                     | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**При создании**](a-whencreated.md)                                     | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**WWW — Главная страница**](a-wwwhomepage.md)                                    | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**WWW-Page — другие**](a-url.md)                                           | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**X121 — адрес**](a-x121address.md)                                     | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**X509 — CERT**](a-usercertificate.md)                                    | Нет.     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |



## <a name="windows-2000-server-property-sets"></a>наборы свойств сервера Windows 2000

этот класс содержит следующие наборы свойств для сервера Windows 2000:



| Общее имя                                            |
|--------------------------------------------------------|
| [**Личные сведения**](r-personal-information.md) |
| [**Веб-информация**](r-web-information.md)           |



## <a name="windows-server-2003"></a>Windows Server 2003

-   [Атрибуты](#windows-server-2003-attributes)
-   [Наборы свойств](#windows-server-2003-property-sets)



| Ввод | Значение |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Нет.                                                                                        |
| Object-Category             | 1                                                                                            |
| По умолчанию — объект — Категория     | [**Человек**](c-person.md)<br/>                                                        |
| Governs-Id                  | 1.2.840.113556.1.5.15                                                                        |
| По умолчанию-скрытие значения        | 0                                                                                            |
| RDN-Атри-ID                  | [**Common-Name**](a-cn.md)<br/>                                                       |
| Подкласс                 | [**Organizational-Person**](c-organizationalperson.md)<br/>                           |
| Возможные старшие          | [](c-domaindns.md)[**Организационное подразделение** домена DNS](c-organizationalunit.md)         |
| Вспомогательные классы           | [**Mail-получатель**](c-mailrecipient.md) (система)                                           |
| NT-Security-дескриптор      | О:БАГ: BAD: S:                                                                                 |
| Дескриптор безопасности по умолчанию | D: (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;;D А) (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;; SY) (A;; РПЛКЛОРК;;; СЛУЖБЫ |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2003-attributes"></a>Windows Атрибуты сервера 2003

этот класс содержит следующие атрибуты для Windows Server 2003:



| attribute                                                                   | Обязательный | Унаследован от                                                                                                                           |
|-----------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**Дополнительные сведения**](a-notes.md)                                   | Нет.     | **Contact**                                                                                                                            |
| [**Адрес**](a-streetaddress.md)                                          | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Адрес — Домашняя страница**](a-homepostaladdress.md)                                 | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Описание администратора**](a-admindescription.md)                             | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Имя администратора-отображение**](a-admindisplayname.md)                            | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Attributes**](a-allowedattributes.md)                           | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Attributes-эффективен**](a-allowedattributeseffective.md)        | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Child-classes**](a-allowedchildclasses.md)                      | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Child-classes-эффективен**](a-allowedchildclasseseffective.md)   | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Средство**](a-assistant.md)                                            | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**аттрибутецертификатеаттрибуте**](a-attributecertificateattribute.md)    | Нет.     | [**Человек**](c-person.md)<br/>                                                                                                  |
| [**Плацдарм-Server-List-BL**](a-bridgeheadserverlistbl.md)               | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Каноническое имя**](a-canonicalname.md)                                   | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Комментировать**](a-info.md)                                                   | Нет.     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**Common-Name**](a-cn.md)                                                 | Верно      | **Контактное** [ **лицо**](c-person.md)<br/> [**Получатель почты**](c-mailrecipient.md)<br/> [**Вверх**](c-top.md)<br/> |
| [**Company**](a-company.md)                                                | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Код страны**](a-countrycode.md)                                       | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Название страны**](a-c.md)                                                 | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Метка времени создания**](a-createtimestamp.md)                              | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Отдел**](a-department.md)                                          | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Описание**](a-description.md)                                        | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Целевой индикатор**](a-destinationindicator.md)                     | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Отображаемое имя**](a-displayname.md)                                       | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Отображаемое имя — печатаемое**](a-displaynameprintable.md)                    | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Отдел**](a-division.md)                                              | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**DSA-Signature**](a-dsasignature.md)                                     | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**DS-Core-распространение-данные**](a-dscorepropagationdata.md)                 | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Адреса электронной почты**](a-mail.md)                                          | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Идентификатор сотрудника**](a-employeeid.md)                                         | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Имя расширения**](a-extensionname.md)                                   | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Факс-телефон — номер**](a-facsimiletelephonenumber.md)            | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Метки**](a-flags.md)                                                    | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Из записи**](a-fromentry.md)                                           | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Мусор-Coll-период**](a-garbagecollperiod.md)                          | Нет.     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**Квалификатор поколения**](a-generationqualifier.md)                       | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Заданное имя**](a-givenname.md)                                           | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**хаусеидентифиер**](a-houseidentifier.md)                                | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Инициалы**](a-initials.md)                                              | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Тип экземпляра**](a-instancetype.md)                                     | Верно      | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Международный-ISDN-номер**](a-internationalisdnnumber.md)              | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Является критически важным — системный объект**](a-iscriticalsystemobject.md)               | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Удалено**](a-isdeleted.md)                                           | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Входит в состав списка рассылки**](a-memberof.md)                                       | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Имеет права владельца**](a-isprivilegeholder.md)                          | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**лабеледури**](a-labeleduri.md)                                          | Нет.     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**Последний-известный-родительский**](a-lastknownparent.md)                              | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Legacy-Exchange-DN**](a-legacyexchangedn.md)                            | Нет.     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**Локальное имя**](a-l.md)                                                | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Эмблема**](a-thumbnaillogo.md)                                             | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Управляемые объекты**](a-managedobjects.md)                                 | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Manager**](a-manager.md)                                                | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**В основном**](a-masteredby.md)                                         | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**МХС-или-Address**](a-mhsoraddress.md)                                    | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Метка времени изменения**](a-modifytimestamp.md)                              | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-COM-Партитионсетлинк**](a-mscom-partitionsetlink.md)                 | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-COM-Усерлинк**](a-mscom-userlink.md)                                 | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Allowed-to-Delegate-to**](a-msds-allowedtodelegateto.md)          | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**MS-DS-примерно-Иммед-подчиненные**](a-msds-approx-immed-subordinates.md) | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-целостность-дочерняя — количество**](a-ms-ds-consistencychildcount.md)      | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Consistencу-Guid**](a-ms-ds-consistencyguid.md)                   | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Masterd-by**](a-msds-masteredby.md)                              | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)           | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-NC-REPL-курсоры**](a-msds-ncreplcursors.md)                       | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-NC-REPL-Inbound-соседи**](a-msds-ncreplinboundneighbors.md)    | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-NC-REPL-Outbound-соседи**](a-msds-ncreploutboundneighbors.md)  | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-не-Members-BL**](a-msds-nonmembersbl.md)                         | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Operations-для-AZ-Role-BL**](a-msds-operationsforazrolebl.md)     | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)     | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-REPL-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)              | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Tasks-для-AZ-Role-BL**](a-msds-tasksforazrolebl.md)               | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)               | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-дов-Assistant-Name**](a-msexchassistantname.md)                     | Нет.     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**MS-дов-House-identifier**](a-msexchhouseidentifier.md)                 | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**MS-дов-Лабеледури**](a-msexchlabeleduri.md)                            | Нет.     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**MS-дов-Owner-BL**](a-ownerbl.md)                                       | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**нетбут-SCP-BL**](a-netbootscpbl.md)                                    | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Не-Security-Member-BL**](a-nonsecuritymemberbl.md)                     | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**NT-Security-дескриптор**](a-ntsecuritydescriptor.md)                    | Верно      | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Obj-расп-имя**](a-distinguishedname.md)                                | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Объект — Категория**](a-objectcategory.md)                                 | Верно      | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Объектный класс**](a-objectclass.md)                                       | Верно      | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Объект — GUID**](a-objectguid.md)                                         | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Версия объекта**](a-objectversion.md)                                   | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Организация — имя подразделения**](a-ou.md)                                    | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Название организации**](a-o.md)                                            | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Другие — почтовый ящик**](a-othermailbox.md)                                     | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Другое имя**](a-middlename.md)                                          | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Другие хорошо известные объекты**](a-otherwellknownobjects.md)                 | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Разделяемый атрибут-удаление-список**](a-partialattributedeletionlist.md)   | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Разделяемый атрибут-set**](a-partialattributeset.md)                      | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Личный заголовок**](a-personaltitle.md)                                   | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон-Fax — другие**](a-otherfacsimiletelephonenumber.md)                  | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон-Home — другие**](a-otherhomephone.md)                                | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон-Home — основной**](a-homephone.md)                                   | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон-Ip — другие**](a-otheripphone.md)                                    | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон-Ip-Primary**](a-ipphone.md)                                       | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон-ISDN-Primary**](a-primaryinternationalisdnnumber.md)              | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон-Mobile — другие**](a-othermobile.md)                                 | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон — Mobile — Primary**](a-mobile.md)                                    | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон-Office-Other**](a-othertelephone.md)                              | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон-пейджер — другие**](a-otherpager.md)                                   | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон-пейджер-основной**](a-pager.md)                                      | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**физическая доставка — Office-имя**](a-physicaldeliveryofficename.md)       | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Снимки**](a-thumbnailphoto.md)                                         | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Возможно — подстрочные**](a-possibleinferiors.md)                           | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Почтовый адрес**](a-postaladdress.md)                                   | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Почтовый код**](a-postalcode.md)                                         | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**флажок после Office**](a-postofficebox.md)                                  | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Предпочтительный метод доставки**](a-preferreddeliverymethod.md)              | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Прокси-объект-имя**](a-proxiedobjectname.md)                          | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Прокси-адреса**](a-proxyaddresses.md)                                 | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Запрос — политика — BL**](a-querypolicybl.md)                                  | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**RDN**](a-name.md)                                                       | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Зарегистрированный адрес**](a-registeredaddress.md)                           | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                   | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**REPL-Уптодате-Vector**](a-repluptodatevector.md)                        | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Отчеты**](a-directreports.md)                                          | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Представители — от**](a-repsfrom.md)                                             | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Представители — кому**](a-repsto.md)                                                 | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Редакции**](a-revision.md)                                              | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**SD-Rights-эффективен**](a-sdrightseffective.md)                          | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**секретарь**](a-secretary.md)                                            | Нет.     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**См. также**](a-seealso.md)                                               | Нет.     | [**Человек**](c-person.md)<br/>                                                                                                  |
| [**Серийный номер**](a-serialnumber.md)                                     | Нет.     | [**Человек**](c-person.md)<br/>                                                                                                  |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Отображение в адресной книге**](a-showinaddressbook.md)                         | Нет.     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**"Показать" — "Расширенный просмотр"**](a-showinadvancedviewonly.md)              | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**State-или-провинция-Name**](a-st.md)                                      | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Улица-адрес**](a-street.md)                                          | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Структурный объектный класс**](a-structuralobjectclass.md)                  | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Подразделы-ReFS**](a-subrefs.md)                                               | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**субсчемасубентри**](a-subschemasubentry.md)                            | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Образование**](a-sn.md)                                                     | Нет.     | [**Человек**](c-person.md)<br/>                                                                                                  |
| [**Системные флаги**](a-systemflags.md)                                       | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Номер телефона**](a-telephonenumber.md)                               | Нет.     | [**Человек**](c-person.md)<br/> [**Получатель почты**](c-mailrecipient.md)<br/>                                             |
| [**Teletex — идентификатор терминала**](a-teletexterminalidentifier.md)          | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Номер телекса**](a-telexnumber.md)                                       | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Номер телекса (первичный)**](a-primarytelexnumber.md)                               | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Текст — страна**](a-co.md)                                                | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**С текстовым кодированием или адресом**](a-textencodedoraddress.md)                   | Нет.     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**Название**](a-title.md)                                                    | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**User-CERT**](a-usercert.md)                                             | Нет.     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**Комментарий пользователя**](a-comment.md)                                           | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Пароль пользователя**](a-userpassword.md)                                     | Нет.     | [**Человек**](c-person.md)<br/>                                                                                                  |
| [**Пользователь-SMIME-Certificate**](a-usersmimecertificate.md)                    | Нет.     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**USN-изменено**](a-usnchanged.md)                                         | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Созданный USN**](a-usncreated.md)                                         | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**USN-DSA-Last-obj-removed**](a-usndsalastobjremoved.md)                  | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**USN — межсайтовая**](a-usnintersite.md)                                     | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                 | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Источник USN**](a-usnsource.md)                                           | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**WBEM — путь**](a-wbempath.md)                                             | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Хорошо известные объекты**](a-wellknownobjects.md)                            | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**При изменении**](a-whenchanged.md)                                       | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**При создании**](a-whencreated.md)                                       | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**WWW — Главная страница**](a-wwwhomepage.md)                                      | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**WWW-Page — другие**](a-url.md)                                             | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**X121 — адрес**](a-x121address.md)                                       | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**X509 — CERT**](a-usercertificate.md)                                      | Нет.     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |



## <a name="windows-server-2003-property-sets"></a>Windows Сервер 2003 наборы свойств

этот класс содержит следующие наборы свойств для Windows Server 2003:



| Общее имя                                            |
|--------------------------------------------------------|
| [**Личные сведения**](r-personal-information.md) |
| [**Веб-информация**](r-web-information.md)           |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2

-   [Атрибуты](#windows-server-2003-r2-attributes)
-   [Наборы свойств](#windows-server-2003-r2-property-sets)



| Ввод | Значение |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Нет.                                                                                        |
| Object-Category             | 1                                                                                            |
| По умолчанию — объект — Категория     | [**Человек**](c-person.md)<br/>                                                        |
| Governs-Id                  | 1.2.840.113556.1.5.15                                                                        |
| По умолчанию-скрытие значения        | 0                                                                                            |
| RDN-Атри-ID                  | [**Common-Name**](a-cn.md)<br/>                                                       |
| Подкласс                 | [**Organizational-Person**](c-organizationalperson.md)<br/>                           |
| Возможные старшие          | [](c-domaindns.md)[**Организационное подразделение** домена DNS](c-organizationalunit.md)         |
| Вспомогательные классы           | [**Mail-получатель**](c-mailrecipient.md) (система)                                           |
| NT-Security-дескриптор      | О:БАГ: BAD: S:                                                                                 |
| Дескриптор безопасности по умолчанию | D: (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;;D А) (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;; SY) (A;; РПЛКЛОРК;;; СЛУЖБЫ |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2003-r2-attributes"></a>Windows Атрибуты сервера 2003 R2

этот класс содержит следующие атрибуты для Windows Server 2003 R2:



| attribute                                                                   | Обязательный | Унаследован от                                                                                                                           |
|-----------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**Дополнительные сведения**](a-notes.md)                                   | Нет.     | **Contact**                                                                                                                            |
| [**Адрес**](a-streetaddress.md)                                          | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Адрес — Домашняя страница**](a-homepostaladdress.md)                                 | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Описание администратора**](a-admindescription.md)                             | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Имя администратора-отображение**](a-admindisplayname.md)                            | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Attributes**](a-allowedattributes.md)                           | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Attributes-эффективен**](a-allowedattributeseffective.md)        | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Child-classes**](a-allowedchildclasses.md)                      | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Child-classes-эффективен**](a-allowedchildclasseseffective.md)   | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Средство**](a-assistant.md)                                            | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**аттрибутецертификатеаттрибуте**](a-attributecertificateattribute.md)    | Нет.     | [**Человек**](c-person.md)<br/>                                                                                                  |
| [**Плацдарм-Server-List-BL**](a-bridgeheadserverlistbl.md)               | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Каноническое имя**](a-canonicalname.md)                                   | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Комментировать**](a-info.md)                                                   | Нет.     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**Common-Name**](a-cn.md)                                                 | Верно      | **Контактное** [ **лицо**](c-person.md)<br/> [**Получатель почты**](c-mailrecipient.md)<br/> [**Вверх**](c-top.md)<br/> |
| [**Company**](a-company.md)                                                | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Код страны**](a-countrycode.md)                                       | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Название страны**](a-c.md)                                                 | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Метка времени создания**](a-createtimestamp.md)                              | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Отдел**](a-department.md)                                          | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Описание**](a-description.md)                                        | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Целевой индикатор**](a-destinationindicator.md)                     | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Отображаемое имя**](a-displayname.md)                                       | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Отображаемое имя — печатаемое**](a-displaynameprintable.md)                    | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Отдел**](a-division.md)                                              | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**DSA-Signature**](a-dsasignature.md)                                     | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**DS-Core-распространение-данные**](a-dscorepropagationdata.md)                 | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Адреса электронной почты**](a-mail.md)                                          | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Идентификатор сотрудника**](a-employeeid.md)                                         | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Имя расширения**](a-extensionname.md)                                   | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Факс-телефон — номер**](a-facsimiletelephonenumber.md)            | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Метки**](a-flags.md)                                                    | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Из записи**](a-fromentry.md)                                           | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Мусор-Coll-период**](a-garbagecollperiod.md)                          | Нет.     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**Квалификатор поколения**](a-generationqualifier.md)                       | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Заданное имя**](a-givenname.md)                                           | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**хаусеидентифиер**](a-houseidentifier.md)                                | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Инициалы**](a-initials.md)                                              | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Тип экземпляра**](a-instancetype.md)                                     | Верно      | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Международный-ISDN-номер**](a-internationalisdnnumber.md)              | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Является критически важным — системный объект**](a-iscriticalsystemobject.md)               | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Удалено**](a-isdeleted.md)                                           | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Входит в состав списка рассылки**](a-memberof.md)                                       | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Имеет права владельца**](a-isprivilegeholder.md)                          | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**лабеледури**](a-labeleduri.md)                                          | Нет.     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**Последний-известный-родительский**](a-lastknownparent.md)                              | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Legacy-Exchange-DN**](a-legacyexchangedn.md)                            | Нет.     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**Локальное имя**](a-l.md)                                                | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Эмблема**](a-thumbnaillogo.md)                                             | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Управляемые объекты**](a-managedobjects.md)                                 | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Manager**](a-manager.md)                                                | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**В основном**](a-masteredby.md)                                         | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**МХС-или-Address**](a-mhsoraddress.md)                                    | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Метка времени изменения**](a-modifytimestamp.md)                              | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-COM-Партитионсетлинк**](a-mscom-partitionsetlink.md)                 | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-COM-Усерлинк**](a-mscom-userlink.md)                                 | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DFSR-Компутерреференцебл**](a-msdfsr-computerreferencebl.md)         | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DFSR-Мемберреференцебл**](a-msdfsr-memberreferencebl.md)             | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Allowed-to-Delegate-to**](a-msds-allowedtodelegateto.md)          | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**MS-DS-примерно-Иммед-подчиненные**](a-msds-approx-immed-subordinates.md) | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-целостность-дочерняя — количество**](a-ms-ds-consistencychildcount.md)      | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Consistencу-Guid**](a-ms-ds-consistencyguid.md)                   | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Masterd-by**](a-msds-masteredby.md)                              | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)           | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-NC-REPL-курсоры**](a-msds-ncreplcursors.md)                       | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-NC-REPL-Inbound-соседи**](a-msds-ncreplinboundneighbors.md)    | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-NC-REPL-Outbound-соседи**](a-msds-ncreploutboundneighbors.md)  | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-не-Members-BL**](a-msds-nonmembersbl.md)                         | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Operations-для-AZ-Role-BL**](a-msds-operationsforazrolebl.md)     | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)     | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-REPL-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)              | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Source-Object-DN**](a-msds-sourceobjectdn.md)                     | Нет.     | **Contact**                                                                                                                            |
| [**MS-DS-Tasks-для-AZ-Role-BL**](a-msds-tasksforazrolebl.md)               | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)               | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-дов-Assistant-Name**](a-msexchassistantname.md)                     | Нет.     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**MS-дов-House-identifier**](a-msexchhouseidentifier.md)                 | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**MS-дов-Лабеледури**](a-msexchlabeleduri.md)                            | Нет.     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**MS-дов-Owner-BL**](a-ownerbl.md)                                       | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Мссфу-30-POSIX-член-of**](a-mssfu30posixmemberof.md)                  | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**нетбут-SCP-BL**](a-netbootscpbl.md)                                    | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Не-Security-Member-BL**](a-nonsecuritymemberbl.md)                     | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**NT-Security-дескриптор**](a-ntsecuritydescriptor.md)                    | Верно      | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Obj-расп-имя**](a-distinguishedname.md)                                | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Объект — Категория**](a-objectcategory.md)                                 | Верно      | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Объектный класс**](a-objectclass.md)                                       | Верно      | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Объект — GUID**](a-objectguid.md)                                         | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Версия объекта**](a-objectversion.md)                                   | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Организация — имя подразделения**](a-ou.md)                                    | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Название организации**](a-o.md)                                            | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Другие — почтовый ящик**](a-othermailbox.md)                                     | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Другое имя**](a-middlename.md)                                          | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Другие хорошо известные объекты**](a-otherwellknownobjects.md)                 | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Разделяемый атрибут-удаление-список**](a-partialattributedeletionlist.md)   | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Разделяемый атрибут-set**](a-partialattributeset.md)                      | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Личный заголовок**](a-personaltitle.md)                                   | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон-Fax — другие**](a-otherfacsimiletelephonenumber.md)                  | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон-Home — другие**](a-otherhomephone.md)                                | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон-Home — основной**](a-homephone.md)                                   | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон-Ip — другие**](a-otheripphone.md)                                    | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон-Ip-Primary**](a-ipphone.md)                                       | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон-ISDN-Primary**](a-primaryinternationalisdnnumber.md)              | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон-Mobile — другие**](a-othermobile.md)                                 | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон — Mobile — Primary**](a-mobile.md)                                    | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон-Office-Other**](a-othertelephone.md)                              | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон-пейджер — другие**](a-otherpager.md)                                   | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон-пейджер-основной**](a-pager.md)                                      | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**физическая доставка — Office-имя**](a-physicaldeliveryofficename.md)       | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Снимки**](a-thumbnailphoto.md)                                         | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Возможно — подстрочные**](a-possibleinferiors.md)                           | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Почтовый адрес**](a-postaladdress.md)                                   | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Почтовый код**](a-postalcode.md)                                         | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**флажок после Office**](a-postofficebox.md)                                  | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Предпочтительный метод доставки**](a-preferreddeliverymethod.md)              | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Прокси-объект-имя**](a-proxiedobjectname.md)                          | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Прокси-адреса**](a-proxyaddresses.md)                                 | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Запрос — политика — BL**](a-querypolicybl.md)                                  | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**RDN**](a-name.md)                                                       | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Зарегистрированный адрес**](a-registeredaddress.md)                           | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                   | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**REPL-Уптодате-Vector**](a-repluptodatevector.md)                        | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Отчеты**](a-directreports.md)                                          | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Представители — от**](a-repsfrom.md)                                             | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Представители — кому**](a-repsto.md)                                                 | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Редакции**](a-revision.md)                                              | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**SD-Rights-эффективен**](a-sdrightseffective.md)                          | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**секретарь**](a-secretary.md)                                            | Нет.     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**См. также**](a-seealso.md)                                               | Нет.     | [**Человек**](c-person.md)<br/>                                                                                                  |
| [**Серийный номер**](a-serialnumber.md)                                     | Нет.     | [**Человек**](c-person.md)<br/>                                                                                                  |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Отображение в адресной книге**](a-showinaddressbook.md)                         | Нет.     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**"Показать" — "Расширенный просмотр"**](a-showinadvancedviewonly.md)              | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**State-или-провинция-Name**](a-st.md)                                      | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Улица-адрес**](a-street.md)                                          | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Структурный объектный класс**](a-structuralobjectclass.md)                  | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Подразделы-ReFS**](a-subrefs.md)                                               | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**субсчемасубентри**](a-subschemasubentry.md)                            | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Образование**](a-sn.md)                                                     | Нет.     | [**Человек**](c-person.md)<br/>                                                                                                  |
| [**Системные флаги**](a-systemflags.md)                                       | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Номер телефона**](a-telephonenumber.md)                               | Нет.     | [**Человек**](c-person.md)<br/> [**Получатель почты**](c-mailrecipient.md)<br/>                                             |
| [**Teletex — идентификатор терминала**](a-teletexterminalidentifier.md)          | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Номер телекса**](a-telexnumber.md)                                       | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Номер телекса (первичный)**](a-primarytelexnumber.md)                               | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Текст — страна**](a-co.md)                                                | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**С текстовым кодированием или адресом**](a-textencodedoraddress.md)                   | Нет.     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**Название**](a-title.md)                                                    | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**User-CERT**](a-usercert.md)                                             | Нет.     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**Комментарий пользователя**](a-comment.md)                                           | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Пароль пользователя**](a-userpassword.md)                                     | Нет.     | [**Человек**](c-person.md)<br/>                                                                                                  |
| [**Пользователь-SMIME-Certificate**](a-usersmimecertificate.md)                    | Нет.     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**USN-изменено**](a-usnchanged.md)                                         | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Созданный USN**](a-usncreated.md)                                         | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**USN-DSA-Last-obj-removed**](a-usndsalastobjremoved.md)                  | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**USN — межсайтовая**](a-usnintersite.md)                                     | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                 | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Источник USN**](a-usnsource.md)                                           | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**WBEM — путь**](a-wbempath.md)                                             | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Хорошо известные объекты**](a-wellknownobjects.md)                            | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**При изменении**](a-whenchanged.md)                                       | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**При создании**](a-whencreated.md)                                       | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**WWW — Главная страница**](a-wwwhomepage.md)                                      | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**WWW-Page — другие**](a-url.md)                                             | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**X121 — адрес**](a-x121address.md)                                       | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**X509 — CERT**](a-usercertificate.md)                                      | Нет.     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |



## <a name="windows-server-2003-r2-property-sets"></a>Windows Наборы свойств Server 2003 R2

этот класс содержит следующие наборы свойств для Windows Server 2003 R2:



| Общее имя                                            |
|--------------------------------------------------------|
| [**Личные сведения**](r-personal-information.md) |
| [**Веб-информация**](r-web-information.md)           |



## <a name="windows-server-2008"></a>Windows Server 2008

-   [Атрибуты](#windows-server-2008-attributes)
-   [Наборы свойств](#windows-server-2008-property-sets)



| Ввод | Значение |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Нет.                                                                                        |
| Object-Category             | 1                                                                                            |
| По умолчанию — объект — Категория     | [**Человек**](c-person.md)<br/>                                                        |
| Governs-Id                  | 1.2.840.113556.1.5.15                                                                        |
| По умолчанию-скрытие значения        | 0                                                                                            |
| RDN-Атри-ID                  | [**Common-Name**](a-cn.md)<br/>                                                       |
| Подкласс                 | [**Organizational-Person**](c-organizationalperson.md)<br/>                           |
| Возможные старшие          | [](c-domaindns.md)[**Организационное подразделение** домена DNS](c-organizationalunit.md)         |
| Вспомогательные классы           | [**Mail-получатель**](c-mailrecipient.md) (система)                                           |
| NT-Security-дескриптор      | О:БАГ: BAD: S:                                                                                 |
| Дескриптор безопасности по умолчанию | D: (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;;D А) (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;; SY) (A;; РПЛКЛОРК;;; СЛУЖБЫ |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2008-attributes"></a>Windows Атрибуты сервера 2008

этот класс содержит следующие атрибуты для Windows Server 2008:



| attribute                                                                      | Обязательный | Унаследован от                                                                                                                           |
|--------------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**Дополнительные сведения**](a-notes.md)                                      | Нет.     | **Contact**                                                                                                                            |
| [**Адрес**](a-streetaddress.md)                                             | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Адрес — Домашняя страница**](a-homepostaladdress.md)                                    | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Описание администратора**](a-admindescription.md)                                | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Имя администратора-отображение**](a-admindisplayname.md)                               | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Attributes**](a-allowedattributes.md)                              | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Attributes-эффективен**](a-allowedattributeseffective.md)           | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Child-classes**](a-allowedchildclasses.md)                         | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Child-classes-эффективен**](a-allowedchildclasseseffective.md)      | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Средство**](a-assistant.md)                                               | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**аттрибутецертификатеаттрибуте**](a-attributecertificateattribute.md)       | Нет.     | [**Человек**](c-person.md)<br/>                                                                                                  |
| [**Плацдарм-Server-List-BL**](a-bridgeheadserverlistbl.md)                  | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Каноническое имя**](a-canonicalname.md)                                      | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Комментировать**](a-info.md)                                                      | Нет.     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**Common-Name**](a-cn.md)                                                    | Верно      | **Контактное** [ **лицо**](c-person.md)<br/> [**Получатель почты**](c-mailrecipient.md)<br/> [**Вверх**](c-top.md)<br/> |
| [**Company**](a-company.md)                                                   | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Код страны**](a-countrycode.md)                                          | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Название страны**](a-c.md)                                                    | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Метка времени создания**](a-createtimestamp.md)                                 | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Отдел**](a-department.md)                                             | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Описание**](a-description.md)                                           | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Целевой индикатор**](a-destinationindicator.md)                        | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Отображаемое имя**](a-displayname.md)                                          | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Отображаемое имя — печатаемое**](a-displaynameprintable.md)                       | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Отдел**](a-division.md)                                                 | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**DSA-Signature**](a-dsasignature.md)                                        | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**DS-Core-распространение-данные**](a-dscorepropagationdata.md)                    | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Адреса электронной почты**](a-mail.md)                                             | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Идентификатор сотрудника**](a-employeeid.md)                                            | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Имя расширения**](a-extensionname.md)                                      | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Факс-телефон — номер**](a-facsimiletelephonenumber.md)               | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Метки**](a-flags.md)                                                       | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Из записи**](a-fromentry.md)                                              | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                  | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                      | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                     | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Мусор-Coll-период**](a-garbagecollperiod.md)                             | Нет.     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**Квалификатор поколения**](a-generationqualifier.md)                          | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Заданное имя**](a-givenname.md)                                              | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**хаусеидентифиер**](a-houseidentifier.md)                                   | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Инициалы**](a-initials.md)                                                 | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Тип экземпляра**](a-instancetype.md)                                        | Верно      | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Международный-ISDN-номер**](a-internationalisdnnumber.md)                 | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Является критически важным — системный объект**](a-iscriticalsystemobject.md)                  | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Удалено**](a-isdeleted.md)                                              | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Входит в состав списка рассылки**](a-memberof.md)                                          | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Имеет права владельца**](a-isprivilegeholder.md)                             | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**лабеледури**](a-labeleduri.md)                                             | Нет.     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**Последний-известный-родительский**](a-lastknownparent.md)                                 | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Legacy-Exchange-DN**](a-legacyexchangedn.md)                               | Нет.     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**Локальное имя**](a-l.md)                                                   | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Эмблема**](a-thumbnaillogo.md)                                                | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Управляемые объекты**](a-managedobjects.md)                                    | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Manager**](a-manager.md)                                                   | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**В основном**](a-masteredby.md)                                            | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**МХС-или-Address**](a-mhsoraddress.md)                                       | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Метка времени изменения**](a-modifytimestamp.md)                                 | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-COM-Партитионсетлинк**](a-mscom-partitionsetlink.md)                    | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-COM-Усерлинк**](a-mscom-userlink.md)                                    | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DFSR-Компутерреференцебл**](a-msdfsr-computerreferencebl.md)            | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DFSR-Мемберреференцебл**](a-msdfsr-memberreferencebl.md)                | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Allowed-to-Delegate-to**](a-msds-allowedtodelegateto.md)             | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**MS-DS-примерно-Иммед-подчиненные**](a-msds-approx-immed-subordinates.md)    | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Аусентикатедто-Аккаунтлист**](a-msds-authenticatedtoaccountlist.md) | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-целостность-дочерняя — количество**](a-ms-ds-consistencychildcount.md)         | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Consistencу-Guid**](a-ms-ds-consistencyguid.md)                      | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-ИЕРАРХИя — старший стаж — индекс**](a-msds-habseniorityindex.md)                  | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**MS-DS--домен — для**](a-msds-isdomainfor.md)                              | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-является-Full-реплика для**](a-msds-isfullreplicafor.md)                   | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-является-partial-реплика для**](a-msds-ispartialreplicafor.md)             | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                            | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Masterd-by**](a-msds-masteredby.md)                                 | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)              | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-NC-REPL-курсоры**](a-msds-ncreplcursors.md)                          | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-NC-REPL-Inbound-соседи**](a-msds-ncreplinboundneighbors.md)       | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-NC-REPL-Outbound-соседи**](a-msds-ncreploutboundneighbors.md)     | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)  | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-NC-Type**](a-msds-nctype.md)                                         | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-не-Members-BL**](a-msds-nonmembersbl.md)                            | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                  | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Operations-для-AZ-Role-BL**](a-msds-operationsforazrolebl.md)        | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)        | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Фонетическое название компании**](a-msds-phoneticcompanyname.md)              | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**MS-DS-фонетический отдел**](a-msds-phoneticdepartment.md)                 | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**MS-DS-фонетическо-отображаемое имя**](a-msds-phoneticdisplayname.md)              | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Получатель почты**](c-mailrecipient.md)<br/>                |
| [**MS-DS-фонетическо-First-Name**](a-msds-phoneticfirstname.md)                  | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**MS-DS-фонетическое имя (фамилия)**](a-msds-phoneticlastname.md)                    | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**MS-DS-Principal-Name**](a-msds-principalname.md)                           | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-PSO — применяется**](a-msds-psoapplied.md)                                 | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-REPL-Attribute-Meta-Data**](a-msds-replattributemetadata.md)         | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)                 | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-выявил-DSA**](a-msds-revealeddsas.md)                             | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-выводит-List-BL**](a-msds-revealedlistbl.md)                        | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Source-Object-DN**](a-msds-sourceobjectdn.md)                        | Нет.     | **Contact**                                                                                                                            |
| [**MS-DS-Tasks-для-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                  | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                  | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-дов-Assistant-Name**](a-msexchassistantname.md)                        | Нет.     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**MS-дов-House-identifier**](a-msexchhouseidentifier.md)                    | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**MS-дов-Лабеледури**](a-msexchlabeleduri.md)                               | Нет.     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**MS-дов-Owner-BL**](a-ownerbl.md)                                          | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Мссфу-30-POSIX-член-of**](a-mssfu30posixmemberof.md)                     | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**нетбут-SCP-BL**](a-netbootscpbl.md)                                       | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Не-Security-Member-BL**](a-nonsecuritymemberbl.md)                        | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**NT-Security-дескриптор**](a-ntsecuritydescriptor.md)                       | Верно      | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Obj-расп-имя**](a-distinguishedname.md)                                   | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Объект — Категория**](a-objectcategory.md)                                    | Верно      | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Объектный класс**](a-objectclass.md)                                          | Верно      | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Объект — GUID**](a-objectguid.md)                                            | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Версия объекта**](a-objectversion.md)                                      | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Организация — имя подразделения**](a-ou.md)                                       | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Название организации**](a-o.md)                                               | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Другие — почтовый ящик**](a-othermailbox.md)                                        | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Другое имя**](a-middlename.md)                                             | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Другие хорошо известные объекты**](a-otherwellknownobjects.md)                    | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Разделяемый атрибут-удаление-список**](a-partialattributedeletionlist.md)      | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Разделяемый атрибут-set**](a-partialattributeset.md)                         | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Личный заголовок**](a-personaltitle.md)                                      | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон-Fax — другие**](a-otherfacsimiletelephonenumber.md)                     | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон-Home — другие**](a-otherhomephone.md)                                   | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон-Home — основной**](a-homephone.md)                                      | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон-Ip — другие**](a-otheripphone.md)                                       | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон-Ip-Primary**](a-ipphone.md)                                          | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон-ISDN-Primary**](a-primaryinternationalisdnnumber.md)                 | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон-Mobile — другие**](a-othermobile.md)                                    | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон — Mobile — Primary**](a-mobile.md)                                       | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон-Office-Other**](a-othertelephone.md)                                 | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон-пейджер — другие**](a-otherpager.md)                                      | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон-пейджер-основной**](a-pager.md)                                         | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**физическая доставка — Office-имя**](a-physicaldeliveryofficename.md)          | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Снимки**](a-thumbnailphoto.md)                                            | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Возможно — подстрочные**](a-possibleinferiors.md)                              | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Почтовый адрес**](a-postaladdress.md)                                      | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Почтовый код**](a-postalcode.md)                                            | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**флажок после Office**](a-postofficebox.md)                                     | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Предпочтительный метод доставки**](a-preferreddeliverymethod.md)                 | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Прокси-объект-имя**](a-proxiedobjectname.md)                             | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Прокси-адреса**](a-proxyaddresses.md)                                    | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Запрос — политика — BL**](a-querypolicybl.md)                                     | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**RDN**](a-name.md)                                                          | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Зарегистрированный адрес**](a-registeredaddress.md)                              | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                      | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**REPL-Уптодате-Vector**](a-repluptodatevector.md)                           | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Отчеты**](a-directreports.md)                                             | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Представители — от**](a-repsfrom.md)                                                | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Представители — кому**](a-repsto.md)                                                    | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Редакции**](a-revision.md)                                                 | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**SD-Rights-эффективен**](a-sdrightseffective.md)                             | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**секретарь**](a-secretary.md)                                               | Нет.     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**См. также**](a-seealso.md)                                                  | Нет.     | [**Человек**](c-person.md)<br/>                                                                                                  |
| [**Серийный номер**](a-serialnumber.md)                                        | Нет.     | [**Человек**](c-person.md)<br/>                                                                                                  |
| [**Server-Reference-BL**](a-serverreferencebl.md)                             | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Отображение в адресной книге**](a-showinaddressbook.md)                            | Нет.     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**"Показать" — "Расширенный просмотр"**](a-showinadvancedviewonly.md)                 | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Site-Object-BL**](a-siteobjectbl.md)                                       | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**State-или-провинция-Name**](a-st.md)                                         | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Улица-адрес**](a-street.md)                                             | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Структурный объектный класс**](a-structuralobjectclass.md)                     | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Подразделы-ReFS**](a-subrefs.md)                                                  | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**субсчемасубентри**](a-subschemasubentry.md)                               | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Образование**](a-sn.md)                                                        | Нет.     | [**Человек**](c-person.md)<br/>                                                                                                  |
| [**Системные флаги**](a-systemflags.md)                                          | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Номер телефона**](a-telephonenumber.md)                                  | Нет.     | [**Человек**](c-person.md)<br/> [**Получатель почты**](c-mailrecipient.md)<br/>                                             |
| [**Teletex — идентификатор терминала**](a-teletexterminalidentifier.md)             | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Номер телекса**](a-telexnumber.md)                                          | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Номер телекса (первичный)**](a-primarytelexnumber.md)                                  | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Текст — страна**](a-co.md)                                                   | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**С текстовым кодированием или адресом**](a-textencodedoraddress.md)                      | Нет.     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**Название**](a-title.md)                                                       | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**User-CERT**](a-usercert.md)                                                | Нет.     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**Комментарий пользователя**](a-comment.md)                                              | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Пароль пользователя**](a-userpassword.md)                                        | Нет.     | [**Человек**](c-person.md)<br/>                                                                                                  |
| [**Пользователь-SMIME-Certificate**](a-usersmimecertificate.md)                       | Нет.     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**USN-изменено**](a-usnchanged.md)                                            | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Созданный USN**](a-usncreated.md)                                            | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**USN-DSA-Last-obj-removed**](a-usndsalastobjremoved.md)                     | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**USN — межсайтовая**](a-usnintersite.md)                                        | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                    | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Источник USN**](a-usnsource.md)                                              | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**WBEM — путь**](a-wbempath.md)                                                | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Хорошо известные объекты**](a-wellknownobjects.md)                               | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**При изменении**](a-whenchanged.md)                                          | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**При создании**](a-whencreated.md)                                          | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**WWW — Главная страница**](a-wwwhomepage.md)                                         | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**WWW-Page — другие**](a-url.md)                                                | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**X121 — адрес**](a-x121address.md)                                          | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**X509 — CERT**](a-usercertificate.md)                                         | Нет.     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |



## <a name="windows-server-2008-property-sets"></a>Windows Сервер 2008 наборы свойств

этот класс содержит следующие наборы свойств для Windows Server 2008:



| Общее имя                                            |
|--------------------------------------------------------|
| [**Личные сведения**](r-personal-information.md) |
| [**Веб-информация**](r-web-information.md)           |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2

-   [Атрибуты](#windows-server-2008-r2-attributes)
-   [Наборы свойств](#windows-server-2008-r2-property-sets)



| Ввод | Значение |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Нет.                                                                                        |
| Object-Category             | 1                                                                                            |
| По умолчанию — объект — Категория     | [**Человек**](c-person.md)<br/>                                                        |
| Governs-Id                  | 1.2.840.113556.1.5.15                                                                        |
| По умолчанию-скрытие значения        | 0                                                                                            |
| RDN-Атри-ID                  | [**Common-Name**](a-cn.md)<br/>                                                       |
| Подкласс                 | [**Organizational-Person**](c-organizationalperson.md)<br/>                           |
| Возможные старшие          | [](c-domaindns.md)[**Организационное подразделение** домена DNS](c-organizationalunit.md)         |
| Вспомогательные классы           | [**Mail-получатель**](c-mailrecipient.md) (система)                                           |
| NT-Security-дескриптор      | О:БАГ: BAD: S:                                                                                 |
| Дескриптор безопасности по умолчанию | D: (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;;D А) (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;; SY) (A;; РПЛКЛОРК;;; СЛУЖБЫ |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2008-r2-attributes"></a>Windows Атрибуты сервера 2008 R2

этот класс содержит следующие атрибуты для Windows Server 2008 R2:



| attribute                                                                        | Обязательный | Унаследован от                                                                                                                           |
|----------------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**Дополнительные сведения**](a-notes.md)                                        | Нет.     | **Contact**                                                                                                                            |
| [**Адрес**](a-streetaddress.md)                                               | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Адрес — Домашняя страница**](a-homepostaladdress.md)                                      | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Описание администратора**](a-admindescription.md)                                  | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Имя администратора-отображение**](a-admindisplayname.md)                                 | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Attributes**](a-allowedattributes.md)                                | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Attributes-эффективен**](a-allowedattributeseffective.md)             | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Child-classes**](a-allowedchildclasses.md)                           | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Child-classes-эффективен**](a-allowedchildclasseseffective.md)        | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Средство**](a-assistant.md)                                                 | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**аттрибутецертификатеаттрибуте**](a-attributecertificateattribute.md)         | Нет.     | [**Человек**](c-person.md)<br/>                                                                                                  |
| [**Плацдарм-Server-List-BL**](a-bridgeheadserverlistbl.md)                    | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Каноническое имя**](a-canonicalname.md)                                        | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Комментировать**](a-info.md)                                                        | Нет.     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**Common-Name**](a-cn.md)                                                      | Верно      | **Контактное** [ **лицо**](c-person.md)<br/> [**Получатель почты**](c-mailrecipient.md)<br/> [**Вверх**](c-top.md)<br/> |
| [**Company**](a-company.md)                                                     | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Код страны**](a-countrycode.md)                                            | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Название страны**](a-c.md)                                                      | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Метка времени создания**](a-createtimestamp.md)                                   | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Отдел**](a-department.md)                                               | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Описание**](a-description.md)                                             | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Целевой индикатор**](a-destinationindicator.md)                          | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Отображаемое имя**](a-displayname.md)                                            | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Отображаемое имя — печатаемое**](a-displaynameprintable.md)                         | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Отдел**](a-division.md)                                                   | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**DSA-Signature**](a-dsasignature.md)                                          | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**DS-Core-распространение-данные**](a-dscorepropagationdata.md)                      | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Адреса электронной почты**](a-mail.md)                                               | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Идентификатор сотрудника**](a-employeeid.md)                                              | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Имя расширения**](a-extensionname.md)                                        | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Факс-телефон — номер**](a-facsimiletelephonenumber.md)                 | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Метки**](a-flags.md)                                                         | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Из записи**](a-fromentry.md)                                                | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                    | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                        | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                       | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Мусор-Coll-период**](a-garbagecollperiod.md)                               | Нет.     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**Квалификатор поколения**](a-generationqualifier.md)                            | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Заданное имя**](a-givenname.md)                                                | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**хаусеидентифиер**](a-houseidentifier.md)                                     | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Инициалы**](a-initials.md)                                                   | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Тип экземпляра**](a-instancetype.md)                                          | Верно      | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Международный-ISDN-номер**](a-internationalisdnnumber.md)                   | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Является критически важным — системный объект**](a-iscriticalsystemobject.md)                    | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Удалено**](a-isdeleted.md)                                                | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Входит в состав списка рассылки**](a-memberof.md)                                            | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Имеет права владельца**](a-isprivilegeholder.md)                               | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Является перезапущенным**](a-isrecycled.md)                                              | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**лабеледури**](a-labeleduri.md)                                               | Нет.     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**Последний-известный-родительский**](a-lastknownparent.md)                                   | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Legacy-Exchange-DN**](a-legacyexchangedn.md)                                 | Нет.     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**Локальное имя**](a-l.md)                                                     | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Эмблема**](a-thumbnaillogo.md)                                                  | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Управляемые объекты**](a-managedobjects.md)                                      | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Manager**](a-manager.md)                                                     | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**В основном**](a-masteredby.md)                                              | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**МХС-или-Address**](a-mhsoraddress.md)                                         | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Метка времени изменения**](a-modifytimestamp.md)                                   | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-COM-Партитионсетлинк**](a-mscom-partitionsetlink.md)                      | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-COM-Усерлинк**](a-mscom-userlink.md)                                      | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DFSR-Компутерреференцебл**](a-msdfsr-computerreferencebl.md)              | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DFSR-Мемберреференцебл**](a-msdfsr-memberreferencebl.md)                  | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Allowed-to-Delegate-to**](a-msds-allowedtodelegateto.md)               | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**MS-DS-примерно-Иммед-подчиненные**](a-msds-approx-immed-subordinates.md)      | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Аусентикатедто-Аккаунтлист**](a-msds-authenticatedtoaccountlist.md)   | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-целостность-дочерняя — количество**](a-ms-ds-consistencychildcount.md)           | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Consistencу-Guid**](a-ms-ds-consistencyguid.md)                        | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Поддержка MS-DS-Feature-BL**](a-msds-enabledfeaturebl.md)                      | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-ИЕРАРХИя — старший стаж — индекс**](a-msds-habseniorityindex.md)                    | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**MS-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)             | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS--домен — для**](a-msds-isdomainfor.md)                                | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-является-Full-реплика для**](a-msds-isfullreplicafor.md)                     | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-является-partial-реплика для**](a-msds-ispartialreplicafor.md)               | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                              | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                              | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-локально-эффективное удаление — время**](a-msds-localeffectivedeletiontime.md) | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Local-эффективен — время перезапуска**](a-msds-localeffectiverecycletime.md)   | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Masterd-by**](a-msds-masteredby.md)                                   | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)                | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-NC-REPL-курсоры**](a-msds-ncreplcursors.md)                            | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-NC-REPL-Inbound-соседи**](a-msds-ncreplinboundneighbors.md)         | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-NC-REPL-Outbound-соседи**](a-msds-ncreploutboundneighbors.md)       | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)    | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-NC-Type**](a-msds-nctype.md)                                           | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-не-Members-BL**](a-msds-nonmembersbl.md)                              | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                    | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Оидтограуп-Link-BL**](a-msds-oidtogrouplinkbl.md)                      | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Operations-для-AZ-Role-BL**](a-msds-operationsforazrolebl.md)          | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)          | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Фонетическое название компании**](a-msds-phoneticcompanyname.md)                | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**MS-DS-фонетический отдел**](a-msds-phoneticdepartment.md)                   | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**MS-DS-фонетическо-отображаемое имя**](a-msds-phoneticdisplayname.md)                | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Получатель почты**](c-mailrecipient.md)<br/>                |
| [**MS-DS-фонетическо-First-Name**](a-msds-phoneticfirstname.md)                    | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**MS-DS-фонетическое имя (фамилия)**](a-msds-phoneticlastname.md)                      | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**MS-DS-Principal-Name**](a-msds-principalname.md)                             | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-PSO — применяется**](a-msds-psoapplied.md)                                   | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-REPL-Attribute-Meta-Data**](a-msds-replattributemetadata.md)           | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)                   | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-выявил-DSA**](a-msds-revealeddsas.md)                               | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-выводит-List-BL**](a-msds-revealedlistbl.md)                          | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Source-Object-DN**](a-msds-sourceobjectdn.md)                          | Нет.     | **Contact**                                                                                                                            |
| [**MS-DS-Tasks-для-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                    | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                    | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-дов-Assistant-Name**](a-msexchassistantname.md)                          | Нет.     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**MS-дов-House-identifier**](a-msexchhouseidentifier.md)                      | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**MS-дов-Лабеледури**](a-msexchlabeleduri.md)                                 | Нет.     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**MS-дов-Owner-BL**](a-ownerbl.md)                                            | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Мссфу-30-POSIX-член-of**](a-mssfu30posixmemberof.md)                       | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**нетбут-SCP-BL**](a-netbootscpbl.md)                                         | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Не-Security-Member-BL**](a-nonsecuritymemberbl.md)                          | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**NT-Security-дескриптор**](a-ntsecuritydescriptor.md)                         | Верно      | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Obj-расп-имя**](a-distinguishedname.md)                                     | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Объект — Категория**](a-objectcategory.md)                                      | Верно      | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Объектный класс**](a-objectclass.md)                                            | Верно      | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Объект — GUID**](a-objectguid.md)                                              | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Версия объекта**](a-objectversion.md)                                        | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Организация — имя подразделения**](a-ou.md)                                         | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Название организации**](a-o.md)                                                 | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Другие — почтовый ящик**](a-othermailbox.md)                                          | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Другое имя**](a-middlename.md)                                               | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Другие хорошо известные объекты**](a-otherwellknownobjects.md)                      | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Разделяемый атрибут-удаление-список**](a-partialattributedeletionlist.md)        | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Разделяемый атрибут-set**](a-partialattributeset.md)                           | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Личный заголовок**](a-personaltitle.md)                                        | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон-Fax — другие**](a-otherfacsimiletelephonenumber.md)                       | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон-Home — другие**](a-otherhomephone.md)                                     | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон-Home — основной**](a-homephone.md)                                        | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон-Ip — другие**](a-otheripphone.md)                                         | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон-Ip-Primary**](a-ipphone.md)                                            | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон-ISDN-Primary**](a-primaryinternationalisdnnumber.md)                   | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон-Mobile — другие**](a-othermobile.md)                                      | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон — Mobile — Primary**](a-mobile.md)                                         | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон-Office-Other**](a-othertelephone.md)                                   | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон-пейджер — другие**](a-otherpager.md)                                        | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон-пейджер-основной**](a-pager.md)                                           | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**физическая доставка — Office-имя**](a-physicaldeliveryofficename.md)            | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Снимки**](a-thumbnailphoto.md)                                              | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Возможно — подстрочные**](a-possibleinferiors.md)                                | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Почтовый адрес**](a-postaladdress.md)                                        | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Почтовый код**](a-postalcode.md)                                              | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**флажок после Office**](a-postofficebox.md)                                       | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Предпочтительный метод доставки**](a-preferreddeliverymethod.md)                   | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Прокси-объект-имя**](a-proxiedobjectname.md)                               | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Прокси-адреса**](a-proxyaddresses.md)                                      | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Запрос — политика — BL**](a-querypolicybl.md)                                       | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**RDN**](a-name.md)                                                            | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Зарегистрированный адрес**](a-registeredaddress.md)                                | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                        | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**REPL-Уптодате-Vector**](a-repluptodatevector.md)                             | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Отчеты**](a-directreports.md)                                               | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Представители — от**](a-repsfrom.md)                                                  | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Представители — кому**](a-repsto.md)                                                      | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Редакции**](a-revision.md)                                                   | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**SD-Rights-эффективен**](a-sdrightseffective.md)                               | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**секретарь**](a-secretary.md)                                                 | Нет.     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**См. также**](a-seealso.md)                                                    | Нет.     | [**Человек**](c-person.md)<br/>                                                                                                  |
| [**Серийный номер**](a-serialnumber.md)                                          | Нет.     | [**Человек**](c-person.md)<br/>                                                                                                  |
| [**Server-Reference-BL**](a-serverreferencebl.md)                               | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Отображение в адресной книге**](a-showinaddressbook.md)                              | Нет.     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**"Показать" — "Расширенный просмотр"**](a-showinadvancedviewonly.md)                   | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Site-Object-BL**](a-siteobjectbl.md)                                         | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**State-или-провинция-Name**](a-st.md)                                           | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Улица-адрес**](a-street.md)                                               | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Структурный объектный класс**](a-structuralobjectclass.md)                       | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Подразделы-ReFS**](a-subrefs.md)                                                    | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**субсчемасубентри**](a-subschemasubentry.md)                                 | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Образование**](a-sn.md)                                                          | Нет.     | [**Человек**](c-person.md)<br/>                                                                                                  |
| [**Системные флаги**](a-systemflags.md)                                            | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Номер телефона**](a-telephonenumber.md)                                    | Нет.     | [**Человек**](c-person.md)<br/> [**Получатель почты**](c-mailrecipient.md)<br/>                                             |
| [**Teletex — идентификатор терминала**](a-teletexterminalidentifier.md)               | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Номер телекса**](a-telexnumber.md)                                            | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Номер телекса (первичный)**](a-primarytelexnumber.md)                                    | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Текст — страна**](a-co.md)                                                     | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**С текстовым кодированием или адресом**](a-textencodedoraddress.md)                        | Нет.     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**Название**](a-title.md)                                                         | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**User-CERT**](a-usercert.md)                                                  | Нет.     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**Комментарий пользователя**](a-comment.md)                                                | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Пароль пользователя**](a-userpassword.md)                                          | Нет.     | [**Человек**](c-person.md)<br/>                                                                                                  |
| [**Пользователь-SMIME-Certificate**](a-usersmimecertificate.md)                         | Нет.     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**USN-изменено**](a-usnchanged.md)                                              | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Созданный USN**](a-usncreated.md)                                              | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**USN-DSA-Last-obj-removed**](a-usndsalastobjremoved.md)                       | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**USN — межсайтовая**](a-usnintersite.md)                                          | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                      | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Источник USN**](a-usnsource.md)                                                | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**WBEM — путь**](a-wbempath.md)                                                  | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Хорошо известные объекты**](a-wellknownobjects.md)                                 | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**При изменении**](a-whenchanged.md)                                            | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**При создании**](a-whencreated.md)                                            | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**WWW — Главная страница**](a-wwwhomepage.md)                                           | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**WWW-Page — другие**](a-url.md)                                                  | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**X121 — адрес**](a-x121address.md)                                            | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**X509 — CERT**](a-usercertificate.md)                                           | Нет.     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |



## <a name="windows-server-2008-r2-property-sets"></a>Windows Наборы свойств Server 2008 R2

этот класс содержит следующие наборы свойств для Windows Server 2008 R2:



| Общее имя                                            |
|--------------------------------------------------------|
| [**Личные сведения**](r-personal-information.md) |
| [**Веб-информация**](r-web-information.md)           |



## <a name="windows-server-2012"></a>Windows Server 2012

-   [Атрибуты](#windows-server-2012-attributes)
-   [Наборы свойств](#windows-server-2012-property-sets)



| Ввод | Значение |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Нет.                                                                                        |
| Object-Category             | 1                                                                                            |
| По умолчанию — объект — Категория     | [**Человек**](c-person.md)<br/>                                                        |
| Governs-Id                  | 1.2.840.113556.1.5.15                                                                        |
| По умолчанию-скрытие значения        | 0                                                                                            |
| RDN-Атри-ID                  | [**Common-Name**](a-cn.md)<br/>                                                       |
| Подкласс                 | [**Organizational-Person**](c-organizationalperson.md)<br/>                           |
| Возможные старшие          | [](c-domaindns.md)[**Организационное подразделение** домена DNS](c-organizationalunit.md)         |
| Вспомогательные классы           | [**Mail-получатель**](c-mailrecipient.md) (система)                                           |
| NT-Security-дескриптор      | О:БАГ: BAD: S:                                                                                 |
| Дескриптор безопасности по умолчанию | D: (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;;D А) (A;; РПВПКРККДКЛКЛОРКВОВДСДДТСВ;;; SY) (A;; РПЛКЛОРК;;; СЛУЖБЫ |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2012-attributes"></a>Windows Server 2012 Атрибута

Этот класс содержит следующие атрибуты для Windows Server 2012:



| attribute                                                                                              | Обязательный | Унаследован от                                                                                                                           |
|--------------------------------------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**Дополнительные сведения**](a-notes.md)                                                              | Нет.     | **Contact**                                                                                                                            |
| [**Адрес**](a-streetaddress.md)                                                                     | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Адрес — Домашняя страница**](a-homepostaladdress.md)                                                            | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Описание администратора**](a-admindescription.md)                                                        | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Имя администратора-отображение**](a-admindisplayname.md)                                                       | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Attributes**](a-allowedattributes.md)                                                      | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Attributes-эффективен**](a-allowedattributeseffective.md)                                   | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Child-classes**](a-allowedchildclasses.md)                                                 | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Child-classes-эффективен**](a-allowedchildclasseseffective.md)                              | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Средство**](a-assistant.md)                                                                       | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**аттрибутецертификатеаттрибуте**](a-attributecertificateattribute.md)                               | Нет.     | [**Человек**](c-person.md)<br/>                                                                                                  |
| [**Плацдарм-Server-List-BL**](a-bridgeheadserverlistbl.md)                                          | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Каноническое имя**](a-canonicalname.md)                                                              | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Комментировать**](a-info.md)                                                                              | Нет.     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**Common-Name**](a-cn.md)                                                                            | Верно      | **Контактное** [ **лицо**](c-person.md)<br/> [**Получатель почты**](c-mailrecipient.md)<br/> [**Вверх**](c-top.md)<br/> |
| [**Company**](a-company.md)                                                                           | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Код страны**](a-countrycode.md)                                                                  | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Название страны**](a-c.md)                                                                            | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Метка времени создания**](a-createtimestamp.md)                                                         | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Отдел**](a-department.md)                                                                     | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Описание**](a-description.md)                                                                   | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Целевой индикатор**](a-destinationindicator.md)                                                | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Отображаемое имя**](a-displayname.md)                                                                  | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Отображаемое имя — печатаемое**](a-displaynameprintable.md)                                               | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Отдел**](a-division.md)                                                                         | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**DSA-Signature**](a-dsasignature.md)                                                                | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**DS-Core-распространение-данные**](a-dscorepropagationdata.md)                                            | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Адреса электронной почты**](a-mail.md)                                                                     | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Идентификатор сотрудника**](a-employeeid.md)                                                                    | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Имя расширения**](a-extensionname.md)                                                              | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Факс-телефон — номер**](a-facsimiletelephonenumber.md)                                       | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Метки**](a-flags.md)                                                                               | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Из записи**](a-fromentry.md)                                                                      | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                                          | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                                              | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                                             | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Мусор-Coll-период**](a-garbagecollperiod.md)                                                     | Нет.     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**Квалификатор поколения**](a-generationqualifier.md)                                                  | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Заданное имя**](a-givenname.md)                                                                      | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**хаусеидентифиер**](a-houseidentifier.md)                                                           | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Инициалы**](a-initials.md)                                                                         | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Тип экземпляра**](a-instancetype.md)                                                                | Верно      | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Международный-ISDN-номер**](a-internationalisdnnumber.md)                                         | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Является критически важным — системный объект**](a-iscriticalsystemobject.md)                                          | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Удалено**](a-isdeleted.md)                                                                      | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Входит в состав списка рассылки**](a-memberof.md)                                                                  | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Имеет права владельца**](a-isprivilegeholder.md)                                                     | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Является перезапущенным**](a-isrecycled.md)                                                                    | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**лабеледури**](a-labeleduri.md)                                                                     | Нет.     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**Последний-известный-родительский**](a-lastknownparent.md)                                                         | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Legacy-Exchange-DN**](a-legacyexchangedn.md)                                                       | Нет.     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**Локальное имя**](a-l.md)                                                                           | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Эмблема**](a-thumbnaillogo.md)                                                                        | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Управляемые объекты**](a-managedobjects.md)                                                            | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Manager**](a-manager.md)                                                                           | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**В основном**](a-masteredby.md)                                                                    | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**МХС-или-Address**](a-mhsoraddress.md)                                                               | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Метка времени изменения**](a-modifytimestamp.md)                                                         | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-COM-Партитионсетлинк**](a-mscom-partitionsetlink.md)                                            | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-COM-Усерлинк**](a-mscom-userlink.md)                                                            | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DFSR-Компутерреференцебл**](a-msdfsr-computerreferencebl.md)                                    | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DFSR-Мемберреференцебл**](a-msdfsr-memberreferencebl.md)                                        | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Allowed-to-"Active-on-чужое удостоверение"**](a-msds-allowedtoactonbehalfofotheridentity.md) | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**MS-DS-Allowed-to-Delegate-to**](a-msds-allowedtodelegateto.md)                                     | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**MS-DS-примерно-Иммед-подчиненные**](a-msds-approx-immed-subordinates.md)                            | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Аусентикатедто-Аккаунтлист**](a-msds-authenticatedtoaccountlist.md)                         | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-ClaimSet-shares-возможные значения-with-BL**](a-msds-claimsharespossiblevalueswithbl.md)           | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-целостность-дочерняя — количество**](a-ms-ds-consistencychildcount.md)                                 | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Consistencу-Guid**](a-ms-ds-consistencyguid.md)                                              | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Поддержка MS-DS-Feature-BL**](a-msds-enabledfeaturebl.md)                                            | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-геокоординаты — высота**](a-msds-geocoordinatesaltitude.md)                                 | Нет.     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**MS-DS-геокоординаты — Широта**](a-msds-geocoordinateslatitude.md)                                 | Нет.     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**MS-DS-геокоординаты — Долгота**](a-msds-geocoordinateslongitude.md)                               | Нет.     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**MS-DS-ИЕРАРХИя — старший стаж — индекс**](a-msds-habseniorityindex.md)                                          | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**MS-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)                                   | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS--домен — для**](a-msds-isdomainfor.md)                                                      | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-является-Full-реплика для**](a-msds-isfullreplicafor.md)                                           | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-является-partial-реплика для**](a-msds-ispartialreplicafor.md)                                     | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-является-PRIMARY-Computer-для**](a-msds-isprimarycomputerfor.md)                                   | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                                    | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                                                    | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-локально-эффективное удаление — время**](a-msds-localeffectivedeletiontime.md)                       | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Local-эффективен — время перезапуска**](a-msds-localeffectiverecycletime.md)                         | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Masterd-by**](a-msds-masteredby.md)                                                         | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)                                      | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Members-of-Resource-Property-List-BL**](a-msds-membersofresourcepropertylistbl.md)           | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-NC-REPL-курсоры**](a-msds-ncreplcursors.md)                                                  | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-NC-REPL-Inbound-соседи**](a-msds-ncreplinboundneighbors.md)                               | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-NC-REPL-Outbound-соседи**](a-msds-ncreploutboundneighbors.md)                             | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)                          | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-NC-Type**](a-msds-nctype.md)                                                                 | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-не-Members-BL**](a-msds-nonmembersbl.md)                                                    | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                                          | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Оидтограуп-Link-BL**](a-msds-oidtogrouplinkbl.md)                                            | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Operations-для-AZ-Role-BL**](a-msds-operationsforazrolebl.md)                                | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)                                | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Фонетическое название компании**](a-msds-phoneticcompanyname.md)                                      | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**MS-DS-фонетический отдел**](a-msds-phoneticdepartment.md)                                         | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**MS-DS-фонетическо-отображаемое имя**](a-msds-phoneticdisplayname.md)                                      | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Получатель почты**](c-mailrecipient.md)<br/>                |
| [**MS-DS-фонетическо-First-Name**](a-msds-phoneticfirstname.md)                                          | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**MS-DS-фонетическое имя (фамилия)**](a-msds-phoneticlastname.md)                                            | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**MS-DS-Principal-Name**](a-msds-principalname.md)                                                   | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-PSO — применяется**](a-msds-psoapplied.md)                                                         | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-REPL-Attribute-Meta-Data**](a-msds-replattributemetadata.md)                                 | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)                                         | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-выявил-DSA**](a-msds-revealeddsas.md)                                                     | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-выводит-List-BL**](a-msds-revealedlistbl.md)                                                | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Source-Object-DN**](a-msds-sourceobjectdn.md)                                                | Нет.     | **Contact**                                                                                                                            |
| [**MS-DS-Tasks-для-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                                          | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                                          | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-TDO-Egress-BL**](a-msds-tdoegressbl.md)                                                      | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-TDO-входящий трафик — BL**](a-msds-tdoingressbl.md)                                                    | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-value-type-Reference-BL**](a-msds-valuetypereferencebl.md)                                   | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-дов-Assistant-Name**](a-msexchassistantname.md)                                                | Нет.     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**MS-дов-House-identifier**](a-msexchhouseidentifier.md)                                            | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**MS-дов-Лабеледури**](a-msexchlabeleduri.md)                                                       | Нет.     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**MS-дов-Owner-BL**](a-ownerbl.md)                                                                  | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Мссфу-30-POSIX-член-of**](a-mssfu30posixmemberof.md)                                             | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**нетбут-SCP-BL**](a-netbootscpbl.md)                                                               | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Не-Security-Member-BL**](a-nonsecuritymemberbl.md)                                                | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**NT-Security-дескриптор**](a-ntsecuritydescriptor.md)                                               | Верно      | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Obj-расп-имя**](a-distinguishedname.md)                                                           | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Объект — Категория**](a-objectcategory.md)                                                            | Верно      | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Объектный класс**](a-objectclass.md)                                                                  | Верно      | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Объект — GUID**](a-objectguid.md)                                                                    | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Версия объекта**](a-objectversion.md)                                                              | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Организация — имя подразделения**](a-ou.md)                                                               | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Название организации**](a-o.md)                                                                       | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Другие — почтовый ящик**](a-othermailbox.md)                                                                | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Другое имя**](a-middlename.md)                                                                     | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Другие хорошо известные объекты**](a-otherwellknownobjects.md)                                            | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Разделяемый атрибут-удаление-список**](a-partialattributedeletionlist.md)                              | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Разделяемый атрибут-set**](a-partialattributeset.md)                                                 | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Личный заголовок**](a-personaltitle.md)                                                              | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон-Fax — другие**](a-otherfacsimiletelephonenumber.md)                                             | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон-Home — другие**](a-otherhomephone.md)                                                           | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон-Home — основной**](a-homephone.md)                                                              | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон-Ip — другие**](a-otheripphone.md)                                                               | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон-Ip-Primary**](a-ipphone.md)                                                                  | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон-ISDN-Primary**](a-primaryinternationalisdnnumber.md)                                         | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон-Mobile — другие**](a-othermobile.md)                                                            | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон — Mobile — Primary**](a-mobile.md)                                                               | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон-Office-Other**](a-othertelephone.md)                                                         | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон-пейджер — другие**](a-otherpager.md)                                                              | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон-пейджер-основной**](a-pager.md)                                                                 | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**физическая доставка — Office-имя**](a-physicaldeliveryofficename.md)                                  | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Снимки**](a-thumbnailphoto.md)                                                                    | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Возможно — подстрочные**](a-possibleinferiors.md)                                                      | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Почтовый адрес**](a-postaladdress.md)                                                              | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Почтовый код**](a-postalcode.md)                                                                    | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**флажок после Office**](a-postofficebox.md)                                                             | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Предпочтительный метод доставки**](a-preferreddeliverymethod.md)                                         | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Прокси-объект-имя**](a-proxiedobjectname.md)                                                     | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Прокси-адреса**](a-proxyaddresses.md)                                                            | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Запрос — политика — BL**](a-querypolicybl.md)                                                             | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**RDN**](a-name.md)                                                                                  | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Зарегистрированный адрес**](a-registeredaddress.md)                                                      | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                                              | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**REPL-Уптодате-Vector**](a-repluptodatevector.md)                                                   | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Отчеты**](a-directreports.md)                                                                     | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Представители — от**](a-repsfrom.md)                                                                        | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Представители — кому**](a-repsto.md)                                                                            | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Редакции**](a-revision.md)                                                                         | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**SD-Rights-эффективен**](a-sdrightseffective.md)                                                     | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**секретарь**](a-secretary.md)                                                                       | Нет.     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**См. также**](a-seealso.md)                                                                          | Нет.     | [**Человек**](c-person.md)<br/>                                                                                                  |
| [**Серийный номер**](a-serialnumber.md)                                                                | Нет.     | [**Человек**](c-person.md)<br/>                                                                                                  |
| [**Server-Reference-BL**](a-serverreferencebl.md)                                                     | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Отображение в адресной книге**](a-showinaddressbook.md)                                                    | Нет.     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**"Показать" — "Расширенный просмотр"**](a-showinadvancedviewonly.md)                                         | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                               | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**State-или-провинция-Name**](a-st.md)                                                                 | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Улица-адрес**](a-street.md)                                                                     | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Структурный объектный класс**](a-structuralobjectclass.md)                                             | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Подразделы-ReFS**](a-subrefs.md)                                                                          | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**субсчемасубентри**](a-subschemasubentry.md)                                                       | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Образование**](a-sn.md)                                                                                | Нет.     | [**Человек**](c-person.md)<br/>                                                                                                  |
| [**Системные флаги**](a-systemflags.md)                                                                  | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Номер телефона**](a-telephonenumber.md)                                                          | Нет.     | [**Человек**](c-person.md)<br/> [**Получатель почты**](c-mailrecipient.md)<br/>                                             |
| [**Teletex — идентификатор терминала**](a-teletexterminalidentifier.md)                                     | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Номер телекса**](a-telexnumber.md)                                                                  | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Номер телекса (первичный)**](a-primarytelexnumber.md)                                                          | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Текст — страна**](a-co.md)                                                                           | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**С текстовым кодированием или адресом**](a-textencodedoraddress.md)                                              | Нет.     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**Название**](a-title.md)                                                                               | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**User-CERT**](a-usercert.md)                                                                        | Нет.     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**Комментарий пользователя**](a-comment.md)                                                                      | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Пароль пользователя**](a-userpassword.md)                                                                | Нет.     | [**Человек**](c-person.md)<br/>                                                                                                  |
| [**Пользователь-SMIME-Certificate**](a-usersmimecertificate.md)                                               | Нет.     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**USN-изменено**](a-usnchanged.md)                                                                    | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Созданный USN**](a-usncreated.md)                                                                    | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**USN-DSA-Last-obj-removed**](a-usndsalastobjremoved.md)                                             | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**USN — межсайтовая**](a-usnintersite.md)                                                                | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                                            | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Источник USN**](a-usnsource.md)                                                                      | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**WBEM — путь**](a-wbempath.md)                                                                        | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Хорошо известные объекты**](a-wellknownobjects.md)                                                       | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**При изменении**](a-whenchanged.md)                                                                  | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**При создании**](a-whencreated.md)                                                                  | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**WWW — Главная страница**](a-wwwhomepage.md)                                                                 | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**WWW-Page — другие**](a-url.md)                                                                        | Нет.     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**X121 — адрес**](a-x121address.md)                                                                  | Нет.     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**X509 — CERT**](a-usercertificate.md)                                                                 | Нет.     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |



## <a name="windows-server-2012-property-sets"></a>Windows Server 2012 Наборы свойств

Этот класс содержит следующие наборы свойств для Windows Server 2012:



| Общее имя                                            |
|--------------------------------------------------------|
| [**Личные сведения**](r-personal-information.md) |
| [**Веб-информация**](r-web-information.md)           |



 

 





