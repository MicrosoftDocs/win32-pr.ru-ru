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
ms.openlocfilehash: ab728fbd87007f01076405730dcfee9f6d935a23
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104493644"
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
| System-Only                 | Неверно                                                                                        |
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



## <a name="windows-2000-server-attributes"></a>Атрибуты сервера Windows 2000

Этот класс содержит следующие атрибуты для сервера Windows 2000:



| attribute                                                                 | Обязательный | Унаследован от                                                                                                                           |
|---------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**Дополнительные сведения**](a-notes.md)                                 | Неверно     | **Contact**                                                                                                                            |
| [**Address**](a-streetaddress.md)                                        | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Адрес — Домашняя страница**](a-homepostaladdress.md)                               | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Описание администратора**](a-admindescription.md)                           | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Имя администратора-отображение**](a-admindisplayname.md)                          | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Attributes**](a-allowedattributes.md)                         | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Attributes-эффективен**](a-allowedattributeseffective.md)      | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Child-classes**](a-allowedchildclasses.md)                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Child-classes-эффективен**](a-allowedchildclasseseffective.md) | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Средство**](a-assistant.md)                                          | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Плацдарм-Server-List-BL**](a-bridgeheadserverlistbl.md)             | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Каноническое имя**](a-canonicalname.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Комментировать**](a-info.md)                                                 | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**Common-Name**](a-cn.md)                                               | True      | **Контактное** [ **лицо**](c-person.md)<br/> [**Получатель почты**](c-mailrecipient.md)<br/> [**Вверх**](c-top.md)<br/> |
| [**Во**](a-company.md)                                              | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Код страны**](a-countrycode.md)                                     | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Название страны**](a-c.md)                                               | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Метка времени создания**](a-createtimestamp.md)                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Название**](a-department.md)                                        | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Описание**](a-description.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Целевой индикатор**](a-destinationindicator.md)                   | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Отображаемое имя**](a-displayname.md)                                     | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Отображаемое имя — печатаемое**](a-displaynameprintable.md)                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Отдел**](a-division.md)                                            | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**DSA-Signature**](a-dsasignature.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**DS-Core-распространение-данные**](a-dscorepropagationdata.md)               | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Адреса электронной почты**](a-mail.md)                                        | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Идентификатор сотрудника**](a-employeeid.md)                                       | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Имя расширения**](a-extensionname.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Факс-телефон — номер**](a-facsimiletelephonenumber.md)          | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Метки**](a-flags.md)                                                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Из записи**](a-fromentry.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)             | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                 | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Мусор-Coll-период**](a-garbagecollperiod.md)                        | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**Квалификатор поколения**](a-generationqualifier.md)                     | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Заданное имя**](a-givenname.md)                                         | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Инициалы**](a-initials.md)                                            | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Тип экземпляра**](a-instancetype.md)                                   | True      | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Международный-ISDN-номер**](a-internationalisdnnumber.md)            | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Является критически важным — системный объект**](a-iscriticalsystemobject.md)             | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Удалено**](a-isdeleted.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Входит в состав списка рассылки**](a-memberof.md)                                     | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Имеет права владельца**](a-isprivilegeholder.md)                        | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Последний-известный-родительский**](a-lastknownparent.md)                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Устаревший — Exchange-DN**](a-legacyexchangedn.md)                          | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**Локальное имя**](a-l.md)                                              | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Эмблема**](a-thumbnaillogo.md)                                           | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Управляемые объекты**](a-managedobjects.md)                               | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Configuration**](a-manager.md)                                              | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**В основном**](a-masteredby.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**МХС-или-Address**](a-mhsoraddress.md)                                  | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Метка времени изменения**](a-modifytimestamp.md)                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-целостность-дочерняя — количество**](a-ms-ds-consistencychildcount.md)    | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Consistencу-Guid**](a-ms-ds-consistencyguid.md)                 | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**нетбут-SCP-BL**](a-netbootscpbl.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Не-Security-Member-BL**](a-nonsecuritymemberbl.md)                   | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**NT-Security-дескриптор**](a-ntsecuritydescriptor.md)                  | True      | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Obj-расп-имя**](a-distinguishedname.md)                              | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Объект — Категория**](a-objectcategory.md)                               | True      | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Объектный класс**](a-objectclass.md)                                     | True      | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Объект — GUID**](a-objectguid.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Версия объекта**](a-objectversion.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Организация — имя подразделения**](a-ou.md)                                  | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Название организации**](a-o.md)                                          | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Другие — почтовый ящик**](a-othermailbox.md)                                   | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Другое имя**](a-middlename.md)                                        | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Другие хорошо известные объекты**](a-otherwellknownobjects.md)               | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Разделяемый атрибут-удаление-список**](a-partialattributedeletionlist.md) | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Разделяемый атрибут-set**](a-partialattributeset.md)                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Личный заголовок**](a-personaltitle.md)                                 | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон — Факс — другие**](a-otherfacsimiletelephonenumber.md)                | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон — Главная страница — другие**](a-otherhomephone.md)                              | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон — Главная страница**](a-homephone.md)                                 | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Phone — IP — другие**](a-otheripphone.md)                                  | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон — IP-адрес — основной**](a-ipphone.md)                                     | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон — ISDN — первичный**](a-primaryinternationalisdnnumber.md)            | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон — Mobile — другие**](a-othermobile.md)                               | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон — Mobile — первичный**](a-mobile.md)                                  | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон — Office — другие**](a-othertelephone.md)                            | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон — пейджер — другие**](a-otherpager.md)                                 | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон — пейджер — первичный**](a-pager.md)                                    | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Физическая доставка — офис — имя**](a-physicaldeliveryofficename.md)     | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Picture**](a-thumbnailphoto.md)                                       | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Возможно — подстрочные**](a-possibleinferiors.md)                         | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Почтовый адрес**](a-postaladdress.md)                                 | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Почтовый код**](a-postalcode.md)                                       | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Пост-Office-Box**](a-postofficebox.md)                                | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Предпочтительный метод доставки**](a-preferreddeliverymethod.md)            | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Прокси-объект-имя**](a-proxiedobjectname.md)                        | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Прокси-адреса**](a-proxyaddresses.md)                               | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Запрос — политика — BL**](a-querypolicybl.md)                                | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**RDN**](a-name.md)                                                     | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Зарегистрированный адрес**](a-registeredaddress.md)                         | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                 | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**REPL-Уптодате-Vector**](a-repluptodatevector.md)                      | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Отчеты**](a-directreports.md)                                        | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Представители — от**](a-repsfrom.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Представители — кому**](a-repsto.md)                                               | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Редакции**](a-revision.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**SD-Rights-эффективен**](a-sdrightseffective.md)                        | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**См. также**](a-seealso.md)                                             | Неверно     | [**Человек**](c-person.md)<br/>                                                                                                  |
| [**Server-Reference-BL**](a-serverreferencebl.md)                        | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Отображение в адресной книге**](a-showinaddressbook.md)                       | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**"Показать" — "Расширенный просмотр"**](a-showinadvancedviewonly.md)            | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Site-Object-BL**](a-siteobjectbl.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**State-или-провинция-Name**](a-st.md)                                    | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Улица-адрес**](a-street.md)                                        | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Подразделы-ReFS**](a-subrefs.md)                                             | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**субсчемасубентри**](a-subschemasubentry.md)                          | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Образование**](a-sn.md)                                                   | Неверно     | [**Человек**](c-person.md)<br/>                                                                                                  |
| [**Системные флаги**](a-systemflags.md)                                     | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Номер телефона**](a-telephonenumber.md)                             | Неверно     | [**Человек**](c-person.md)<br/> [**Получатель почты**](c-mailrecipient.md)<br/>                                             |
| [**Teletex — идентификатор терминала**](a-teletexterminalidentifier.md)        | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Номер телекса**](a-telexnumber.md)                                     | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Номер телекса (первичный)**](a-primarytelexnumber.md)                             | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Текст — страна**](a-co.md)                                              | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**С текстовым кодированием или адресом**](a-textencodedoraddress.md)                 | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**Заголовок**](a-title.md)                                                  | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**User-CERT**](a-usercert.md)                                           | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**Комментарий пользователя**](a-comment.md)                                         | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Пароль пользователя**](a-userpassword.md)                                   | Неверно     | [**Человек**](c-person.md)<br/>                                                                                                  |
| [**Пользователь-SMIME-Certificate**](a-usersmimecertificate.md)                  | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**USN-изменено**](a-usnchanged.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Созданный USN**](a-usncreated.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**USN-DSA-Last-obj-removed**](a-usndsalastobjremoved.md)                | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**USN — межсайтовая**](a-usnintersite.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                               | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Источник USN**](a-usnsource.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**WBEM — путь**](a-wbempath.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Хорошо известные объекты**](a-wellknownobjects.md)                          | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**При изменении**](a-whenchanged.md)                                     | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**При создании**](a-whencreated.md)                                     | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**WWW — Главная страница**](a-wwwhomepage.md)                                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**WWW-Page — другие**](a-url.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**X121 — адрес**](a-x121address.md)                                     | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**X509 — CERT**](a-usercertificate.md)                                    | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |



## <a name="windows-2000-server-property-sets"></a>Наборы свойств сервера Windows 2000

Этот класс содержит следующие наборы свойств для сервера Windows 2000:



| Общее имя                                            |
|--------------------------------------------------------|
| [**Личные сведения**](r-personal-information.md) |
| [**Веб-информация**](r-web-information.md)           |



## <a name="windows-server-2003"></a>Windows Server 2003

-   [Атрибуты](#windows-server-2003-attributes)
-   [Наборы свойств](#windows-server-2003-property-sets)



| Ввод | Значение |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Неверно                                                                                        |
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



## <a name="windows-server-2003-attributes"></a>Атрибуты Windows Server 2003

Этот класс содержит следующие атрибуты для Windows Server 2003:



| attribute                                                                   | Обязательный | Унаследован от                                                                                                                           |
|-----------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**Дополнительные сведения**](a-notes.md)                                   | Неверно     | **Contact**                                                                                                                            |
| [**Address**](a-streetaddress.md)                                          | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Адрес — Домашняя страница**](a-homepostaladdress.md)                                 | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Описание администратора**](a-admindescription.md)                             | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Имя администратора-отображение**](a-admindisplayname.md)                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Attributes**](a-allowedattributes.md)                           | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Attributes-эффективен**](a-allowedattributeseffective.md)        | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Child-classes**](a-allowedchildclasses.md)                      | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Child-classes-эффективен**](a-allowedchildclasseseffective.md)   | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Средство**](a-assistant.md)                                            | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**аттрибутецертификатеаттрибуте**](a-attributecertificateattribute.md)    | Неверно     | [**Человек**](c-person.md)<br/>                                                                                                  |
| [**Плацдарм-Server-List-BL**](a-bridgeheadserverlistbl.md)               | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Каноническое имя**](a-canonicalname.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Комментировать**](a-info.md)                                                   | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**Common-Name**](a-cn.md)                                                 | True      | **Контактное** [ **лицо**](c-person.md)<br/> [**Получатель почты**](c-mailrecipient.md)<br/> [**Вверх**](c-top.md)<br/> |
| [**Во**](a-company.md)                                                | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Код страны**](a-countrycode.md)                                       | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Название страны**](a-c.md)                                                 | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Метка времени создания**](a-createtimestamp.md)                              | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Название**](a-department.md)                                          | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Описание**](a-description.md)                                        | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Целевой индикатор**](a-destinationindicator.md)                     | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Отображаемое имя**](a-displayname.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Отображаемое имя — печатаемое**](a-displaynameprintable.md)                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Отдел**](a-division.md)                                              | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**DSA-Signature**](a-dsasignature.md)                                     | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**DS-Core-распространение-данные**](a-dscorepropagationdata.md)                 | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Адреса электронной почты**](a-mail.md)                                          | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Идентификатор сотрудника**](a-employeeid.md)                                         | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Имя расширения**](a-extensionname.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Факс-телефон — номер**](a-facsimiletelephonenumber.md)            | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Метки**](a-flags.md)                                                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Из записи**](a-fromentry.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Мусор-Coll-период**](a-garbagecollperiod.md)                          | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**Квалификатор поколения**](a-generationqualifier.md)                       | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Заданное имя**](a-givenname.md)                                           | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**хаусеидентифиер**](a-houseidentifier.md)                                | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Инициалы**](a-initials.md)                                              | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Тип экземпляра**](a-instancetype.md)                                     | True      | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Международный-ISDN-номер**](a-internationalisdnnumber.md)              | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Является критически важным — системный объект**](a-iscriticalsystemobject.md)               | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Удалено**](a-isdeleted.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Входит в состав списка рассылки**](a-memberof.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Имеет права владельца**](a-isprivilegeholder.md)                          | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**лабеледури**](a-labeleduri.md)                                          | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**Последний-известный-родительский**](a-lastknownparent.md)                              | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Устаревший — Exchange-DN**](a-legacyexchangedn.md)                            | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**Локальное имя**](a-l.md)                                                | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Эмблема**](a-thumbnaillogo.md)                                             | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Управляемые объекты**](a-managedobjects.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Configuration**](a-manager.md)                                                | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**В основном**](a-masteredby.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**МХС-или-Address**](a-mhsoraddress.md)                                    | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Метка времени изменения**](a-modifytimestamp.md)                              | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-COM-Партитионсетлинк**](a-mscom-partitionsetlink.md)                 | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-COM-Усерлинк**](a-mscom-userlink.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Allowed-to-Delegate-to**](a-msds-allowedtodelegateto.md)          | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**MS-DS-примерно-Иммед-подчиненные**](a-msds-approx-immed-subordinates.md) | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-целостность-дочерняя — количество**](a-ms-ds-consistencychildcount.md)      | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Consistencу-Guid**](a-ms-ds-consistencyguid.md)                   | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Masterd-by**](a-msds-masteredby.md)                              | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)           | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-NC-REPL-курсоры**](a-msds-ncreplcursors.md)                       | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-NC-REPL-Inbound-соседи**](a-msds-ncreplinboundneighbors.md)    | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-NC-REPL-Outbound-соседи**](a-msds-ncreploutboundneighbors.md)  | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-не-Members-BL**](a-msds-nonmembersbl.md)                         | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Operations-для-AZ-Role-BL**](a-msds-operationsforazrolebl.md)     | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)     | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-REPL-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)              | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Tasks-для-AZ-Role-BL**](a-msds-tasksforazrolebl.md)               | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)               | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-дов-Assistant-Name**](a-msexchassistantname.md)                     | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**MS-дов-House-identifier**](a-msexchhouseidentifier.md)                 | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**MS-дов-Лабеледури**](a-msexchlabeleduri.md)                            | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**MS-дов-Owner-BL**](a-ownerbl.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**нетбут-SCP-BL**](a-netbootscpbl.md)                                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Не-Security-Member-BL**](a-nonsecuritymemberbl.md)                     | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**NT-Security-дескриптор**](a-ntsecuritydescriptor.md)                    | True      | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Obj-расп-имя**](a-distinguishedname.md)                                | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Объект — Категория**](a-objectcategory.md)                                 | True      | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Объектный класс**](a-objectclass.md)                                       | True      | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Объект — GUID**](a-objectguid.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Версия объекта**](a-objectversion.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Организация — имя подразделения**](a-ou.md)                                    | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Название организации**](a-o.md)                                            | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Другие — почтовый ящик**](a-othermailbox.md)                                     | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Другое имя**](a-middlename.md)                                          | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Другие хорошо известные объекты**](a-otherwellknownobjects.md)                 | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Разделяемый атрибут-удаление-список**](a-partialattributedeletionlist.md)   | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Разделяемый атрибут-set**](a-partialattributeset.md)                      | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Личный заголовок**](a-personaltitle.md)                                   | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон — Факс — другие**](a-otherfacsimiletelephonenumber.md)                  | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон — Главная страница — другие**](a-otherhomephone.md)                                | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон — Главная страница**](a-homephone.md)                                   | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Phone — IP — другие**](a-otheripphone.md)                                    | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон — IP-адрес — основной**](a-ipphone.md)                                       | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон — ISDN — первичный**](a-primaryinternationalisdnnumber.md)              | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон — Mobile — другие**](a-othermobile.md)                                 | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон — Mobile — первичный**](a-mobile.md)                                    | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон — Office — другие**](a-othertelephone.md)                              | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон — пейджер — другие**](a-otherpager.md)                                   | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон — пейджер — первичный**](a-pager.md)                                      | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Физическая доставка — офис — имя**](a-physicaldeliveryofficename.md)       | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Picture**](a-thumbnailphoto.md)                                         | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Возможно — подстрочные**](a-possibleinferiors.md)                           | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Почтовый адрес**](a-postaladdress.md)                                   | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Почтовый код**](a-postalcode.md)                                         | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Пост-Office-Box**](a-postofficebox.md)                                  | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Предпочтительный метод доставки**](a-preferreddeliverymethod.md)              | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Прокси-объект-имя**](a-proxiedobjectname.md)                          | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Прокси-адреса**](a-proxyaddresses.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Запрос — политика — BL**](a-querypolicybl.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**RDN**](a-name.md)                                                       | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Зарегистрированный адрес**](a-registeredaddress.md)                           | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                   | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**REPL-Уптодате-Vector**](a-repluptodatevector.md)                        | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Отчеты**](a-directreports.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Представители — от**](a-repsfrom.md)                                             | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Представители — кому**](a-repsto.md)                                                 | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Редакции**](a-revision.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**SD-Rights-эффективен**](a-sdrightseffective.md)                          | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**секретарь**](a-secretary.md)                                            | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**См. также**](a-seealso.md)                                               | Неверно     | [**Человек**](c-person.md)<br/>                                                                                                  |
| [**Серийный номер**](a-serialnumber.md)                                     | Неверно     | [**Человек**](c-person.md)<br/>                                                                                                  |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Отображение в адресной книге**](a-showinaddressbook.md)                         | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**"Показать" — "Расширенный просмотр"**](a-showinadvancedviewonly.md)              | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**State-или-провинция-Name**](a-st.md)                                      | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Улица-адрес**](a-street.md)                                          | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Структурный объектный класс**](a-structuralobjectclass.md)                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Подразделы-ReFS**](a-subrefs.md)                                               | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**субсчемасубентри**](a-subschemasubentry.md)                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Образование**](a-sn.md)                                                     | Неверно     | [**Человек**](c-person.md)<br/>                                                                                                  |
| [**Системные флаги**](a-systemflags.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Номер телефона**](a-telephonenumber.md)                               | Неверно     | [**Человек**](c-person.md)<br/> [**Получатель почты**](c-mailrecipient.md)<br/>                                             |
| [**Teletex — идентификатор терминала**](a-teletexterminalidentifier.md)          | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Номер телекса**](a-telexnumber.md)                                       | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Номер телекса (первичный)**](a-primarytelexnumber.md)                               | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Текст — страна**](a-co.md)                                                | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**С текстовым кодированием или адресом**](a-textencodedoraddress.md)                   | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**Заголовок**](a-title.md)                                                    | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**User-CERT**](a-usercert.md)                                             | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**Комментарий пользователя**](a-comment.md)                                           | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Пароль пользователя**](a-userpassword.md)                                     | Неверно     | [**Человек**](c-person.md)<br/>                                                                                                  |
| [**Пользователь-SMIME-Certificate**](a-usersmimecertificate.md)                    | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**USN-изменено**](a-usnchanged.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Созданный USN**](a-usncreated.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**USN-DSA-Last-obj-removed**](a-usndsalastobjremoved.md)                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**USN — межсайтовая**](a-usnintersite.md)                                     | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Источник USN**](a-usnsource.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**WBEM — путь**](a-wbempath.md)                                             | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Хорошо известные объекты**](a-wellknownobjects.md)                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**При изменении**](a-whenchanged.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**При создании**](a-whencreated.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**WWW — Главная страница**](a-wwwhomepage.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**WWW-Page — другие**](a-url.md)                                             | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**X121 — адрес**](a-x121address.md)                                       | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**X509 — CERT**](a-usercertificate.md)                                      | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |



## <a name="windows-server-2003-property-sets"></a>Наборы свойств Windows Server 2003

Этот класс содержит следующие наборы свойств для Windows Server 2003:



| Общее имя                                            |
|--------------------------------------------------------|
| [**Личные сведения**](r-personal-information.md) |
| [**Веб-информация**](r-web-information.md)           |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2

-   [Атрибуты](#windows-server-2003-r2-attributes)
-   [Наборы свойств](#windows-server-2003-r2-property-sets)



| Ввод | Значение |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Неверно                                                                                        |
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



## <a name="windows-server-2003-r2-attributes"></a>Атрибуты Windows Server 2003 R2

Этот класс содержит следующие атрибуты для Windows Server 2003 R2:



| attribute                                                                   | Обязательный | Унаследован от                                                                                                                           |
|-----------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**Дополнительные сведения**](a-notes.md)                                   | Неверно     | **Contact**                                                                                                                            |
| [**Address**](a-streetaddress.md)                                          | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Адрес — Домашняя страница**](a-homepostaladdress.md)                                 | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Описание администратора**](a-admindescription.md)                             | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Имя администратора-отображение**](a-admindisplayname.md)                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Attributes**](a-allowedattributes.md)                           | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Attributes-эффективен**](a-allowedattributeseffective.md)        | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Child-classes**](a-allowedchildclasses.md)                      | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Child-classes-эффективен**](a-allowedchildclasseseffective.md)   | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Средство**](a-assistant.md)                                            | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**аттрибутецертификатеаттрибуте**](a-attributecertificateattribute.md)    | Неверно     | [**Человек**](c-person.md)<br/>                                                                                                  |
| [**Плацдарм-Server-List-BL**](a-bridgeheadserverlistbl.md)               | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Каноническое имя**](a-canonicalname.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Комментировать**](a-info.md)                                                   | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**Common-Name**](a-cn.md)                                                 | True      | **Контактное** [ **лицо**](c-person.md)<br/> [**Получатель почты**](c-mailrecipient.md)<br/> [**Вверх**](c-top.md)<br/> |
| [**Во**](a-company.md)                                                | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Код страны**](a-countrycode.md)                                       | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Название страны**](a-c.md)                                                 | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Метка времени создания**](a-createtimestamp.md)                              | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Название**](a-department.md)                                          | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Описание**](a-description.md)                                        | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Целевой индикатор**](a-destinationindicator.md)                     | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Отображаемое имя**](a-displayname.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Отображаемое имя — печатаемое**](a-displaynameprintable.md)                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Отдел**](a-division.md)                                              | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**DSA-Signature**](a-dsasignature.md)                                     | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**DS-Core-распространение-данные**](a-dscorepropagationdata.md)                 | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Адреса электронной почты**](a-mail.md)                                          | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Идентификатор сотрудника**](a-employeeid.md)                                         | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Имя расширения**](a-extensionname.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Факс-телефон — номер**](a-facsimiletelephonenumber.md)            | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Метки**](a-flags.md)                                                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Из записи**](a-fromentry.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Мусор-Coll-период**](a-garbagecollperiod.md)                          | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**Квалификатор поколения**](a-generationqualifier.md)                       | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Заданное имя**](a-givenname.md)                                           | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**хаусеидентифиер**](a-houseidentifier.md)                                | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Инициалы**](a-initials.md)                                              | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Тип экземпляра**](a-instancetype.md)                                     | True      | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Международный-ISDN-номер**](a-internationalisdnnumber.md)              | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Является критически важным — системный объект**](a-iscriticalsystemobject.md)               | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Удалено**](a-isdeleted.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Входит в состав списка рассылки**](a-memberof.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Имеет права владельца**](a-isprivilegeholder.md)                          | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**лабеледури**](a-labeleduri.md)                                          | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**Последний-известный-родительский**](a-lastknownparent.md)                              | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Устаревший — Exchange-DN**](a-legacyexchangedn.md)                            | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**Локальное имя**](a-l.md)                                                | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Эмблема**](a-thumbnaillogo.md)                                             | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Управляемые объекты**](a-managedobjects.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Configuration**](a-manager.md)                                                | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**В основном**](a-masteredby.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**МХС-или-Address**](a-mhsoraddress.md)                                    | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Метка времени изменения**](a-modifytimestamp.md)                              | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-COM-Партитионсетлинк**](a-mscom-partitionsetlink.md)                 | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-COM-Усерлинк**](a-mscom-userlink.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DFSR-Компутерреференцебл**](a-msdfsr-computerreferencebl.md)         | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DFSR-Мемберреференцебл**](a-msdfsr-memberreferencebl.md)             | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Allowed-to-Delegate-to**](a-msds-allowedtodelegateto.md)          | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**MS-DS-примерно-Иммед-подчиненные**](a-msds-approx-immed-subordinates.md) | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-целостность-дочерняя — количество**](a-ms-ds-consistencychildcount.md)      | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Consistencу-Guid**](a-ms-ds-consistencyguid.md)                   | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Masterd-by**](a-msds-masteredby.md)                              | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)           | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-NC-REPL-курсоры**](a-msds-ncreplcursors.md)                       | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-NC-REPL-Inbound-соседи**](a-msds-ncreplinboundneighbors.md)    | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-NC-REPL-Outbound-соседи**](a-msds-ncreploutboundneighbors.md)  | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-не-Members-BL**](a-msds-nonmembersbl.md)                         | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)               | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Operations-для-AZ-Role-BL**](a-msds-operationsforazrolebl.md)     | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)     | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-REPL-Attribute-Meta-Data**](a-msds-replattributemetadata.md)      | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)              | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Source-Object-DN**](a-msds-sourceobjectdn.md)                     | Неверно     | **Contact**                                                                                                                            |
| [**MS-DS-Tasks-для-AZ-Role-BL**](a-msds-tasksforazrolebl.md)               | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)               | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-дов-Assistant-Name**](a-msexchassistantname.md)                     | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**MS-дов-House-identifier**](a-msexchhouseidentifier.md)                 | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**MS-дов-Лабеледури**](a-msexchlabeleduri.md)                            | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**MS-дов-Owner-BL**](a-ownerbl.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Мссфу-30-POSIX-член-of**](a-mssfu30posixmemberof.md)                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**нетбут-SCP-BL**](a-netbootscpbl.md)                                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Не-Security-Member-BL**](a-nonsecuritymemberbl.md)                     | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**NT-Security-дескриптор**](a-ntsecuritydescriptor.md)                    | True      | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Obj-расп-имя**](a-distinguishedname.md)                                | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Объект — Категория**](a-objectcategory.md)                                 | True      | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Объектный класс**](a-objectclass.md)                                       | True      | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Объект — GUID**](a-objectguid.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Версия объекта**](a-objectversion.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Организация — имя подразделения**](a-ou.md)                                    | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Название организации**](a-o.md)                                            | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Другие — почтовый ящик**](a-othermailbox.md)                                     | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Другое имя**](a-middlename.md)                                          | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Другие хорошо известные объекты**](a-otherwellknownobjects.md)                 | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Разделяемый атрибут-удаление-список**](a-partialattributedeletionlist.md)   | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Разделяемый атрибут-set**](a-partialattributeset.md)                      | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Личный заголовок**](a-personaltitle.md)                                   | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон — Факс — другие**](a-otherfacsimiletelephonenumber.md)                  | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон — Главная страница — другие**](a-otherhomephone.md)                                | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон — Главная страница**](a-homephone.md)                                   | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Phone — IP — другие**](a-otheripphone.md)                                    | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон — IP-адрес — основной**](a-ipphone.md)                                       | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон — ISDN — первичный**](a-primaryinternationalisdnnumber.md)              | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон — Mobile — другие**](a-othermobile.md)                                 | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон — Mobile — первичный**](a-mobile.md)                                    | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон — Office — другие**](a-othertelephone.md)                              | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон — пейджер — другие**](a-otherpager.md)                                   | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон — пейджер — первичный**](a-pager.md)                                      | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Физическая доставка — офис — имя**](a-physicaldeliveryofficename.md)       | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Picture**](a-thumbnailphoto.md)                                         | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Возможно — подстрочные**](a-possibleinferiors.md)                           | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Почтовый адрес**](a-postaladdress.md)                                   | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Почтовый код**](a-postalcode.md)                                         | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Пост-Office-Box**](a-postofficebox.md)                                  | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Предпочтительный метод доставки**](a-preferreddeliverymethod.md)              | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Прокси-объект-имя**](a-proxiedobjectname.md)                          | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Прокси-адреса**](a-proxyaddresses.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Запрос — политика — BL**](a-querypolicybl.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**RDN**](a-name.md)                                                       | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Зарегистрированный адрес**](a-registeredaddress.md)                           | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                   | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**REPL-Уптодате-Vector**](a-repluptodatevector.md)                        | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Отчеты**](a-directreports.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Представители — от**](a-repsfrom.md)                                             | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Представители — кому**](a-repsto.md)                                                 | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Редакции**](a-revision.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**SD-Rights-эффективен**](a-sdrightseffective.md)                          | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**секретарь**](a-secretary.md)                                            | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**См. также**](a-seealso.md)                                               | Неверно     | [**Человек**](c-person.md)<br/>                                                                                                  |
| [**Серийный номер**](a-serialnumber.md)                                     | Неверно     | [**Человек**](c-person.md)<br/>                                                                                                  |
| [**Server-Reference-BL**](a-serverreferencebl.md)                          | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Отображение в адресной книге**](a-showinaddressbook.md)                         | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**"Показать" — "Расширенный просмотр"**](a-showinadvancedviewonly.md)              | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Site-Object-BL**](a-siteobjectbl.md)                                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**State-или-провинция-Name**](a-st.md)                                      | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Улица-адрес**](a-street.md)                                          | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Структурный объектный класс**](a-structuralobjectclass.md)                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Подразделы-ReFS**](a-subrefs.md)                                               | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**субсчемасубентри**](a-subschemasubentry.md)                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Образование**](a-sn.md)                                                     | Неверно     | [**Человек**](c-person.md)<br/>                                                                                                  |
| [**Системные флаги**](a-systemflags.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Номер телефона**](a-telephonenumber.md)                               | Неверно     | [**Человек**](c-person.md)<br/> [**Получатель почты**](c-mailrecipient.md)<br/>                                             |
| [**Teletex — идентификатор терминала**](a-teletexterminalidentifier.md)          | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Номер телекса**](a-telexnumber.md)                                       | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Номер телекса (первичный)**](a-primarytelexnumber.md)                               | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Текст — страна**](a-co.md)                                                | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**С текстовым кодированием или адресом**](a-textencodedoraddress.md)                   | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**Заголовок**](a-title.md)                                                    | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**User-CERT**](a-usercert.md)                                             | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**Комментарий пользователя**](a-comment.md)                                           | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Пароль пользователя**](a-userpassword.md)                                     | Неверно     | [**Человек**](c-person.md)<br/>                                                                                                  |
| [**Пользователь-SMIME-Certificate**](a-usersmimecertificate.md)                    | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**USN-изменено**](a-usnchanged.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Созданный USN**](a-usncreated.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**USN-DSA-Last-obj-removed**](a-usndsalastobjremoved.md)                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**USN — межсайтовая**](a-usnintersite.md)                                     | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Источник USN**](a-usnsource.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**WBEM — путь**](a-wbempath.md)                                             | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Хорошо известные объекты**](a-wellknownobjects.md)                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**При изменении**](a-whenchanged.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**При создании**](a-whencreated.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**WWW — Главная страница**](a-wwwhomepage.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**WWW-Page — другие**](a-url.md)                                             | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**X121 — адрес**](a-x121address.md)                                       | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**X509 — CERT**](a-usercertificate.md)                                      | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |



## <a name="windows-server-2003-r2-property-sets"></a>Наборы свойств Windows Server 2003 R2

Этот класс содержит следующие наборы свойств для Windows Server 2003 R2:



| Общее имя                                            |
|--------------------------------------------------------|
| [**Личные сведения**](r-personal-information.md) |
| [**Веб-информация**](r-web-information.md)           |



## <a name="windows-server-2008"></a>Windows Server 2008

-   [Атрибуты](#windows-server-2008-attributes)
-   [Наборы свойств](#windows-server-2008-property-sets)



| Ввод | Значение |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Неверно                                                                                        |
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



## <a name="windows-server-2008-attributes"></a>Атрибуты Windows Server 2008

Этот класс содержит следующие атрибуты для Windows Server 2008:



| attribute                                                                      | Обязательный | Унаследован от                                                                                                                           |
|--------------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**Дополнительные сведения**](a-notes.md)                                      | Неверно     | **Contact**                                                                                                                            |
| [**Address**](a-streetaddress.md)                                             | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Адрес — Домашняя страница**](a-homepostaladdress.md)                                    | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Описание администратора**](a-admindescription.md)                                | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Имя администратора-отображение**](a-admindisplayname.md)                               | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Attributes**](a-allowedattributes.md)                              | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Attributes-эффективен**](a-allowedattributeseffective.md)           | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Child-classes**](a-allowedchildclasses.md)                         | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Child-classes-эффективен**](a-allowedchildclasseseffective.md)      | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Средство**](a-assistant.md)                                               | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**аттрибутецертификатеаттрибуте**](a-attributecertificateattribute.md)       | Неверно     | [**Человек**](c-person.md)<br/>                                                                                                  |
| [**Плацдарм-Server-List-BL**](a-bridgeheadserverlistbl.md)                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Каноническое имя**](a-canonicalname.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Комментировать**](a-info.md)                                                      | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**Common-Name**](a-cn.md)                                                    | True      | **Контактное** [ **лицо**](c-person.md)<br/> [**Получатель почты**](c-mailrecipient.md)<br/> [**Вверх**](c-top.md)<br/> |
| [**Во**](a-company.md)                                                   | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Код страны**](a-countrycode.md)                                          | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Название страны**](a-c.md)                                                    | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Метка времени создания**](a-createtimestamp.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Название**](a-department.md)                                             | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Описание**](a-description.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Целевой индикатор**](a-destinationindicator.md)                        | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Отображаемое имя**](a-displayname.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Отображаемое имя — печатаемое**](a-displaynameprintable.md)                       | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Отдел**](a-division.md)                                                 | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**DSA-Signature**](a-dsasignature.md)                                        | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**DS-Core-распространение-данные**](a-dscorepropagationdata.md)                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Адреса электронной почты**](a-mail.md)                                             | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Идентификатор сотрудника**](a-employeeid.md)                                            | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Имя расширения**](a-extensionname.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Факс-телефон — номер**](a-facsimiletelephonenumber.md)               | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Метки**](a-flags.md)                                                       | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Из записи**](a-fromentry.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                      | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                     | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Мусор-Coll-период**](a-garbagecollperiod.md)                             | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**Квалификатор поколения**](a-generationqualifier.md)                          | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Заданное имя**](a-givenname.md)                                              | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**хаусеидентифиер**](a-houseidentifier.md)                                   | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Инициалы**](a-initials.md)                                                 | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Тип экземпляра**](a-instancetype.md)                                        | True      | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Международный-ISDN-номер**](a-internationalisdnnumber.md)                 | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Является критически важным — системный объект**](a-iscriticalsystemobject.md)                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Удалено**](a-isdeleted.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Входит в состав списка рассылки**](a-memberof.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Имеет права владельца**](a-isprivilegeholder.md)                             | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**лабеледури**](a-labeleduri.md)                                             | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**Последний-известный-родительский**](a-lastknownparent.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Устаревший — Exchange-DN**](a-legacyexchangedn.md)                               | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**Локальное имя**](a-l.md)                                                   | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Эмблема**](a-thumbnaillogo.md)                                                | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Управляемые объекты**](a-managedobjects.md)                                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Configuration**](a-manager.md)                                                   | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**В основном**](a-masteredby.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**МХС-или-Address**](a-mhsoraddress.md)                                       | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Метка времени изменения**](a-modifytimestamp.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-COM-Партитионсетлинк**](a-mscom-partitionsetlink.md)                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-COM-Усерлинк**](a-mscom-userlink.md)                                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DFSR-Компутерреференцебл**](a-msdfsr-computerreferencebl.md)            | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DFSR-Мемберреференцебл**](a-msdfsr-memberreferencebl.md)                | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Allowed-to-Delegate-to**](a-msds-allowedtodelegateto.md)             | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**MS-DS-примерно-Иммед-подчиненные**](a-msds-approx-immed-subordinates.md)    | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Аусентикатедто-Аккаунтлист**](a-msds-authenticatedtoaccountlist.md) | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-целостность-дочерняя — количество**](a-ms-ds-consistencychildcount.md)         | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Consistencу-Guid**](a-ms-ds-consistencyguid.md)                      | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-ИЕРАРХИя — старший стаж — индекс**](a-msds-habseniorityindex.md)                  | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**MS-DS--домен — для**](a-msds-isdomainfor.md)                              | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-является-Full-реплика для**](a-msds-isfullreplicafor.md)                   | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-является-partial-реплика для**](a-msds-ispartialreplicafor.md)             | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Masterd-by**](a-msds-masteredby.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)              | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-NC-REPL-курсоры**](a-msds-ncreplcursors.md)                          | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-NC-REPL-Inbound-соседи**](a-msds-ncreplinboundneighbors.md)       | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-NC-REPL-Outbound-соседи**](a-msds-ncreploutboundneighbors.md)     | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)  | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-NC-Type**](a-msds-nctype.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-не-Members-BL**](a-msds-nonmembersbl.md)                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Operations-для-AZ-Role-BL**](a-msds-operationsforazrolebl.md)        | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)        | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Фонетическое название компании**](a-msds-phoneticcompanyname.md)              | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**MS-DS-фонетический отдел**](a-msds-phoneticdepartment.md)                 | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**MS-DS-фонетическо-отображаемое имя**](a-msds-phoneticdisplayname.md)              | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Получатель почты**](c-mailrecipient.md)<br/>                |
| [**MS-DS-фонетическо-First-Name**](a-msds-phoneticfirstname.md)                  | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**MS-DS-фонетическое имя (фамилия)**](a-msds-phoneticlastname.md)                    | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**MS-DS-Principal-Name**](a-msds-principalname.md)                           | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-PSO — применяется**](a-msds-psoapplied.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-REPL-Attribute-Meta-Data**](a-msds-replattributemetadata.md)         | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)                 | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-выявил-DSA**](a-msds-revealeddsas.md)                             | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-выводит-List-BL**](a-msds-revealedlistbl.md)                        | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Source-Object-DN**](a-msds-sourceobjectdn.md)                        | Неверно     | **Contact**                                                                                                                            |
| [**MS-DS-Tasks-для-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-дов-Assistant-Name**](a-msexchassistantname.md)                        | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**MS-дов-House-identifier**](a-msexchhouseidentifier.md)                    | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**MS-дов-Лабеледури**](a-msexchlabeleduri.md)                               | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**MS-дов-Owner-BL**](a-ownerbl.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Мссфу-30-POSIX-член-of**](a-mssfu30posixmemberof.md)                     | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**нетбут-SCP-BL**](a-netbootscpbl.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Не-Security-Member-BL**](a-nonsecuritymemberbl.md)                        | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**NT-Security-дескриптор**](a-ntsecuritydescriptor.md)                       | True      | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Obj-расп-имя**](a-distinguishedname.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Объект — Категория**](a-objectcategory.md)                                    | True      | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Объектный класс**](a-objectclass.md)                                          | True      | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Объект — GUID**](a-objectguid.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Версия объекта**](a-objectversion.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Организация — имя подразделения**](a-ou.md)                                       | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Название организации**](a-o.md)                                               | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Другие — почтовый ящик**](a-othermailbox.md)                                        | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Другое имя**](a-middlename.md)                                             | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Другие хорошо известные объекты**](a-otherwellknownobjects.md)                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Разделяемый атрибут-удаление-список**](a-partialattributedeletionlist.md)      | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Разделяемый атрибут-set**](a-partialattributeset.md)                         | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Личный заголовок**](a-personaltitle.md)                                      | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон — Факс — другие**](a-otherfacsimiletelephonenumber.md)                     | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон — Главная страница — другие**](a-otherhomephone.md)                                   | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон — Главная страница**](a-homephone.md)                                      | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Phone — IP — другие**](a-otheripphone.md)                                       | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон — IP-адрес — основной**](a-ipphone.md)                                          | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон — ISDN — первичный**](a-primaryinternationalisdnnumber.md)                 | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон — Mobile — другие**](a-othermobile.md)                                    | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон — Mobile — первичный**](a-mobile.md)                                       | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон — Office — другие**](a-othertelephone.md)                                 | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон — пейджер — другие**](a-otherpager.md)                                      | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон — пейджер — первичный**](a-pager.md)                                         | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Физическая доставка — офис — имя**](a-physicaldeliveryofficename.md)          | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Picture**](a-thumbnailphoto.md)                                            | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Возможно — подстрочные**](a-possibleinferiors.md)                              | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Почтовый адрес**](a-postaladdress.md)                                      | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Почтовый код**](a-postalcode.md)                                            | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Пост-Office-Box**](a-postofficebox.md)                                     | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Предпочтительный метод доставки**](a-preferreddeliverymethod.md)                 | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Прокси-объект-имя**](a-proxiedobjectname.md)                             | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Прокси-адреса**](a-proxyaddresses.md)                                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Запрос — политика — BL**](a-querypolicybl.md)                                     | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**RDN**](a-name.md)                                                          | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Зарегистрированный адрес**](a-registeredaddress.md)                              | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                      | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**REPL-Уптодате-Vector**](a-repluptodatevector.md)                           | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Отчеты**](a-directreports.md)                                             | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Представители — от**](a-repsfrom.md)                                                | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Представители — кому**](a-repsto.md)                                                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Редакции**](a-revision.md)                                                 | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**SD-Rights-эффективен**](a-sdrightseffective.md)                             | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**секретарь**](a-secretary.md)                                               | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**См. также**](a-seealso.md)                                                  | Неверно     | [**Человек**](c-person.md)<br/>                                                                                                  |
| [**Серийный номер**](a-serialnumber.md)                                        | Неверно     | [**Человек**](c-person.md)<br/>                                                                                                  |
| [**Server-Reference-BL**](a-serverreferencebl.md)                             | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Отображение в адресной книге**](a-showinaddressbook.md)                            | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**"Показать" — "Расширенный просмотр"**](a-showinadvancedviewonly.md)                 | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Site-Object-BL**](a-siteobjectbl.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**State-или-провинция-Name**](a-st.md)                                         | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Улица-адрес**](a-street.md)                                             | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Структурный объектный класс**](a-structuralobjectclass.md)                     | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Подразделы-ReFS**](a-subrefs.md)                                                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**субсчемасубентри**](a-subschemasubentry.md)                               | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Образование**](a-sn.md)                                                        | Неверно     | [**Человек**](c-person.md)<br/>                                                                                                  |
| [**Системные флаги**](a-systemflags.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Номер телефона**](a-telephonenumber.md)                                  | Неверно     | [**Человек**](c-person.md)<br/> [**Получатель почты**](c-mailrecipient.md)<br/>                                             |
| [**Teletex — идентификатор терминала**](a-teletexterminalidentifier.md)             | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Номер телекса**](a-telexnumber.md)                                          | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Номер телекса (первичный)**](a-primarytelexnumber.md)                                  | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Текст — страна**](a-co.md)                                                   | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**С текстовым кодированием или адресом**](a-textencodedoraddress.md)                      | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**Заголовок**](a-title.md)                                                       | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**User-CERT**](a-usercert.md)                                                | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**Комментарий пользователя**](a-comment.md)                                              | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Пароль пользователя**](a-userpassword.md)                                        | Неверно     | [**Человек**](c-person.md)<br/>                                                                                                  |
| [**Пользователь-SMIME-Certificate**](a-usersmimecertificate.md)                       | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**USN-изменено**](a-usnchanged.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Созданный USN**](a-usncreated.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**USN-DSA-Last-obj-removed**](a-usndsalastobjremoved.md)                     | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**USN — межсайтовая**](a-usnintersite.md)                                        | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Источник USN**](a-usnsource.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**WBEM — путь**](a-wbempath.md)                                                | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Хорошо известные объекты**](a-wellknownobjects.md)                               | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**При изменении**](a-whenchanged.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**При создании**](a-whencreated.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**WWW — Главная страница**](a-wwwhomepage.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**WWW-Page — другие**](a-url.md)                                                | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**X121 — адрес**](a-x121address.md)                                          | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**X509 — CERT**](a-usercertificate.md)                                         | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |



## <a name="windows-server-2008-property-sets"></a>Наборы свойств Windows Server 2008

Этот класс содержит следующие наборы свойств для Windows Server 2008:



| Общее имя                                            |
|--------------------------------------------------------|
| [**Личные сведения**](r-personal-information.md) |
| [**Веб-информация**](r-web-information.md)           |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2

-   [Атрибуты](#windows-server-2008-r2-attributes)
-   [Наборы свойств](#windows-server-2008-r2-property-sets)



| Ввод | Значение |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Неверно                                                                                        |
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



## <a name="windows-server-2008-r2-attributes"></a>Атрибуты Windows Server 2008 R2

Этот класс содержит следующие атрибуты для Windows Server 2008 R2:



| attribute                                                                        | Обязательный | Унаследован от                                                                                                                           |
|----------------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**Дополнительные сведения**](a-notes.md)                                        | Неверно     | **Contact**                                                                                                                            |
| [**Address**](a-streetaddress.md)                                               | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Адрес — Домашняя страница**](a-homepostaladdress.md)                                      | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Описание администратора**](a-admindescription.md)                                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Имя администратора-отображение**](a-admindisplayname.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Attributes**](a-allowedattributes.md)                                | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Attributes-эффективен**](a-allowedattributeseffective.md)             | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Child-classes**](a-allowedchildclasses.md)                           | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Child-classes-эффективен**](a-allowedchildclasseseffective.md)        | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Средство**](a-assistant.md)                                                 | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**аттрибутецертификатеаттрибуте**](a-attributecertificateattribute.md)         | Неверно     | [**Человек**](c-person.md)<br/>                                                                                                  |
| [**Плацдарм-Server-List-BL**](a-bridgeheadserverlistbl.md)                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Каноническое имя**](a-canonicalname.md)                                        | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Комментировать**](a-info.md)                                                        | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**Common-Name**](a-cn.md)                                                      | True      | **Контактное** [ **лицо**](c-person.md)<br/> [**Получатель почты**](c-mailrecipient.md)<br/> [**Вверх**](c-top.md)<br/> |
| [**Во**](a-company.md)                                                     | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Код страны**](a-countrycode.md)                                            | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Название страны**](a-c.md)                                                      | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Метка времени создания**](a-createtimestamp.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Название**](a-department.md)                                               | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Описание**](a-description.md)                                             | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Целевой индикатор**](a-destinationindicator.md)                          | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Отображаемое имя**](a-displayname.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Отображаемое имя — печатаемое**](a-displaynameprintable.md)                         | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Отдел**](a-division.md)                                                   | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**DSA-Signature**](a-dsasignature.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**DS-Core-распространение-данные**](a-dscorepropagationdata.md)                      | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Адреса электронной почты**](a-mail.md)                                               | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Идентификатор сотрудника**](a-employeeid.md)                                              | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Имя расширения**](a-extensionname.md)                                        | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Факс-телефон — номер**](a-facsimiletelephonenumber.md)                 | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Метки**](a-flags.md)                                                         | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Из записи**](a-fromentry.md)                                                | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                        | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Мусор-Coll-период**](a-garbagecollperiod.md)                               | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**Квалификатор поколения**](a-generationqualifier.md)                            | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Заданное имя**](a-givenname.md)                                                | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**хаусеидентифиер**](a-houseidentifier.md)                                     | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Инициалы**](a-initials.md)                                                   | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Тип экземпляра**](a-instancetype.md)                                          | True      | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Международный-ISDN-номер**](a-internationalisdnnumber.md)                   | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Является критически важным — системный объект**](a-iscriticalsystemobject.md)                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Удалено**](a-isdeleted.md)                                                | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Входит в состав списка рассылки**](a-memberof.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Имеет права владельца**](a-isprivilegeholder.md)                               | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Является перезапущенным**](a-isrecycled.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**лабеледури**](a-labeleduri.md)                                               | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**Последний-известный-родительский**](a-lastknownparent.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Устаревший — Exchange-DN**](a-legacyexchangedn.md)                                 | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**Локальное имя**](a-l.md)                                                     | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Эмблема**](a-thumbnaillogo.md)                                                  | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Управляемые объекты**](a-managedobjects.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Configuration**](a-manager.md)                                                     | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**В основном**](a-masteredby.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**МХС-или-Address**](a-mhsoraddress.md)                                         | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Метка времени изменения**](a-modifytimestamp.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-COM-Партитионсетлинк**](a-mscom-partitionsetlink.md)                      | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-COM-Усерлинк**](a-mscom-userlink.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DFSR-Компутерреференцебл**](a-msdfsr-computerreferencebl.md)              | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DFSR-Мемберреференцебл**](a-msdfsr-memberreferencebl.md)                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Allowed-to-Delegate-to**](a-msds-allowedtodelegateto.md)               | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**MS-DS-примерно-Иммед-подчиненные**](a-msds-approx-immed-subordinates.md)      | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Аусентикатедто-Аккаунтлист**](a-msds-authenticatedtoaccountlist.md)   | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-целостность-дочерняя — количество**](a-ms-ds-consistencychildcount.md)           | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Consistencу-Guid**](a-ms-ds-consistencyguid.md)                        | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Поддержка MS-DS-Feature-BL**](a-msds-enabledfeaturebl.md)                      | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-ИЕРАРХИя — старший стаж — индекс**](a-msds-habseniorityindex.md)                    | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**MS-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)             | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS--домен — для**](a-msds-isdomainfor.md)                                | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-является-Full-реплика для**](a-msds-isfullreplicafor.md)                     | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-является-partial-реплика для**](a-msds-ispartialreplicafor.md)               | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                              | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                              | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-локально-эффективное удаление — время**](a-msds-localeffectivedeletiontime.md) | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Local-эффективен — время перезапуска**](a-msds-localeffectiverecycletime.md)   | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Masterd-by**](a-msds-masteredby.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)                | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-NC-REPL-курсоры**](a-msds-ncreplcursors.md)                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-NC-REPL-Inbound-соседи**](a-msds-ncreplinboundneighbors.md)         | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-NC-REPL-Outbound-соседи**](a-msds-ncreploutboundneighbors.md)       | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)    | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-NC-Type**](a-msds-nctype.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-не-Members-BL**](a-msds-nonmembersbl.md)                              | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Оидтограуп-Link-BL**](a-msds-oidtogrouplinkbl.md)                      | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Operations-для-AZ-Role-BL**](a-msds-operationsforazrolebl.md)          | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)          | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Фонетическое название компании**](a-msds-phoneticcompanyname.md)                | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**MS-DS-фонетический отдел**](a-msds-phoneticdepartment.md)                   | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**MS-DS-фонетическо-отображаемое имя**](a-msds-phoneticdisplayname.md)                | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Получатель почты**](c-mailrecipient.md)<br/>                |
| [**MS-DS-фонетическо-First-Name**](a-msds-phoneticfirstname.md)                    | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**MS-DS-фонетическое имя (фамилия)**](a-msds-phoneticlastname.md)                      | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**MS-DS-Principal-Name**](a-msds-principalname.md)                             | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-PSO — применяется**](a-msds-psoapplied.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-REPL-Attribute-Meta-Data**](a-msds-replattributemetadata.md)           | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)                   | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-выявил-DSA**](a-msds-revealeddsas.md)                               | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-выводит-List-BL**](a-msds-revealedlistbl.md)                          | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Source-Object-DN**](a-msds-sourceobjectdn.md)                          | Неверно     | **Contact**                                                                                                                            |
| [**MS-DS-Tasks-для-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-дов-Assistant-Name**](a-msexchassistantname.md)                          | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**MS-дов-House-identifier**](a-msexchhouseidentifier.md)                      | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**MS-дов-Лабеледури**](a-msexchlabeleduri.md)                                 | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**MS-дов-Owner-BL**](a-ownerbl.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Мссфу-30-POSIX-член-of**](a-mssfu30posixmemberof.md)                       | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**нетбут-SCP-BL**](a-netbootscpbl.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Не-Security-Member-BL**](a-nonsecuritymemberbl.md)                          | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**NT-Security-дескриптор**](a-ntsecuritydescriptor.md)                         | True      | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Obj-расп-имя**](a-distinguishedname.md)                                     | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Объект — Категория**](a-objectcategory.md)                                      | True      | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Объектный класс**](a-objectclass.md)                                            | True      | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Объект — GUID**](a-objectguid.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Версия объекта**](a-objectversion.md)                                        | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Организация — имя подразделения**](a-ou.md)                                         | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Название организации**](a-o.md)                                                 | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Другие — почтовый ящик**](a-othermailbox.md)                                          | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Другое имя**](a-middlename.md)                                               | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Другие хорошо известные объекты**](a-otherwellknownobjects.md)                      | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Разделяемый атрибут-удаление-список**](a-partialattributedeletionlist.md)        | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Разделяемый атрибут-set**](a-partialattributeset.md)                           | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Личный заголовок**](a-personaltitle.md)                                        | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон — Факс — другие**](a-otherfacsimiletelephonenumber.md)                       | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон — Главная страница — другие**](a-otherhomephone.md)                                     | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон — Главная страница**](a-homephone.md)                                        | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Phone — IP — другие**](a-otheripphone.md)                                         | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон — IP-адрес — основной**](a-ipphone.md)                                            | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон — ISDN — первичный**](a-primaryinternationalisdnnumber.md)                   | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон — Mobile — другие**](a-othermobile.md)                                      | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон — Mobile — первичный**](a-mobile.md)                                         | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон — Office — другие**](a-othertelephone.md)                                   | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон — пейджер — другие**](a-otherpager.md)                                        | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон — пейджер — первичный**](a-pager.md)                                           | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Физическая доставка — офис — имя**](a-physicaldeliveryofficename.md)            | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Picture**](a-thumbnailphoto.md)                                              | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Возможно — подстрочные**](a-possibleinferiors.md)                                | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Почтовый адрес**](a-postaladdress.md)                                        | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Почтовый код**](a-postalcode.md)                                              | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Пост-Office-Box**](a-postofficebox.md)                                       | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Предпочтительный метод доставки**](a-preferreddeliverymethod.md)                   | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Прокси-объект-имя**](a-proxiedobjectname.md)                               | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Прокси-адреса**](a-proxyaddresses.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Запрос — политика — BL**](a-querypolicybl.md)                                       | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**RDN**](a-name.md)                                                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Зарегистрированный адрес**](a-registeredaddress.md)                                | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                        | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**REPL-Уптодате-Vector**](a-repluptodatevector.md)                             | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Отчеты**](a-directreports.md)                                               | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Представители — от**](a-repsfrom.md)                                                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Представители — кому**](a-repsto.md)                                                      | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Редакции**](a-revision.md)                                                   | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**SD-Rights-эффективен**](a-sdrightseffective.md)                               | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**секретарь**](a-secretary.md)                                                 | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**См. также**](a-seealso.md)                                                    | Неверно     | [**Человек**](c-person.md)<br/>                                                                                                  |
| [**Серийный номер**](a-serialnumber.md)                                          | Неверно     | [**Человек**](c-person.md)<br/>                                                                                                  |
| [**Server-Reference-BL**](a-serverreferencebl.md)                               | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Отображение в адресной книге**](a-showinaddressbook.md)                              | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**"Показать" — "Расширенный просмотр"**](a-showinadvancedviewonly.md)                   | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Site-Object-BL**](a-siteobjectbl.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**State-или-провинция-Name**](a-st.md)                                           | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Улица-адрес**](a-street.md)                                               | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Структурный объектный класс**](a-structuralobjectclass.md)                       | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Подразделы-ReFS**](a-subrefs.md)                                                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**субсчемасубентри**](a-subschemasubentry.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Образование**](a-sn.md)                                                          | Неверно     | [**Человек**](c-person.md)<br/>                                                                                                  |
| [**Системные флаги**](a-systemflags.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Номер телефона**](a-telephonenumber.md)                                    | Неверно     | [**Человек**](c-person.md)<br/> [**Получатель почты**](c-mailrecipient.md)<br/>                                             |
| [**Teletex — идентификатор терминала**](a-teletexterminalidentifier.md)               | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Номер телекса**](a-telexnumber.md)                                            | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Номер телекса (первичный)**](a-primarytelexnumber.md)                                    | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Текст — страна**](a-co.md)                                                     | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**С текстовым кодированием или адресом**](a-textencodedoraddress.md)                        | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**Заголовок**](a-title.md)                                                         | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**User-CERT**](a-usercert.md)                                                  | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**Комментарий пользователя**](a-comment.md)                                                | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Пароль пользователя**](a-userpassword.md)                                          | Неверно     | [**Человек**](c-person.md)<br/>                                                                                                  |
| [**Пользователь-SMIME-Certificate**](a-usersmimecertificate.md)                         | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**USN-изменено**](a-usnchanged.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Созданный USN**](a-usncreated.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**USN-DSA-Last-obj-removed**](a-usndsalastobjremoved.md)                       | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**USN — межсайтовая**](a-usnintersite.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Источник USN**](a-usnsource.md)                                                | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**WBEM — путь**](a-wbempath.md)                                                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Хорошо известные объекты**](a-wellknownobjects.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**При изменении**](a-whenchanged.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**При создании**](a-whencreated.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**WWW — Главная страница**](a-wwwhomepage.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**WWW-Page — другие**](a-url.md)                                                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**X121 — адрес**](a-x121address.md)                                            | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**X509 — CERT**](a-usercertificate.md)                                           | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |



## <a name="windows-server-2008-r2-property-sets"></a>Наборы свойств Windows Server 2008 R2

Этот класс содержит следующие наборы свойств для Windows Server 2008 R2:



| Общее имя                                            |
|--------------------------------------------------------|
| [**Личные сведения**](r-personal-information.md) |
| [**Веб-информация**](r-web-information.md)           |



## <a name="windows-server-2012"></a>Windows Server 2012

-   [Атрибуты](#windows-server-2012-attributes)
-   [Наборы свойств](#windows-server-2012-property-sets)



| Ввод | Значение |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Неверно                                                                                        |
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



## <a name="windows-server-2012-attributes"></a>Атрибуты Windows Server 2012

Этот класс содержит следующие атрибуты для Windows Server 2012:



| attribute                                                                                              | Обязательный | Унаследован от                                                                                                                           |
|--------------------------------------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**Дополнительные сведения**](a-notes.md)                                                              | Неверно     | **Contact**                                                                                                                            |
| [**Address**](a-streetaddress.md)                                                                     | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Адрес — Домашняя страница**](a-homepostaladdress.md)                                                            | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Описание администратора**](a-admindescription.md)                                                        | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Имя администратора-отображение**](a-admindisplayname.md)                                                       | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Attributes**](a-allowedattributes.md)                                                      | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Attributes-эффективен**](a-allowedattributeseffective.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Child-classes**](a-allowedchildclasses.md)                                                 | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Allowed-Child-classes-эффективен**](a-allowedchildclasseseffective.md)                              | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Средство**](a-assistant.md)                                                                       | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**аттрибутецертификатеаттрибуте**](a-attributecertificateattribute.md)                               | Неверно     | [**Человек**](c-person.md)<br/>                                                                                                  |
| [**Плацдарм-Server-List-BL**](a-bridgeheadserverlistbl.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Каноническое имя**](a-canonicalname.md)                                                              | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Комментировать**](a-info.md)                                                                              | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**Common-Name**](a-cn.md)                                                                            | True      | **Контактное** [ **лицо**](c-person.md)<br/> [**Получатель почты**](c-mailrecipient.md)<br/> [**Вверх**](c-top.md)<br/> |
| [**Во**](a-company.md)                                                                           | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Код страны**](a-countrycode.md)                                                                  | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Название страны**](a-c.md)                                                                            | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Метка времени создания**](a-createtimestamp.md)                                                         | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Название**](a-department.md)                                                                     | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Описание**](a-description.md)                                                                   | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Целевой индикатор**](a-destinationindicator.md)                                                | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Отображаемое имя**](a-displayname.md)                                                                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Отображаемое имя — печатаемое**](a-displaynameprintable.md)                                               | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Отдел**](a-division.md)                                                                         | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**DSA-Signature**](a-dsasignature.md)                                                                | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**DS-Core-распространение-данные**](a-dscorepropagationdata.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Адреса электронной почты**](a-mail.md)                                                                     | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Идентификатор сотрудника**](a-employeeid.md)                                                                    | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Имя расширения**](a-extensionname.md)                                                              | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Факс-телефон — номер**](a-facsimiletelephonenumber.md)                                       | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Метки**](a-flags.md)                                                                               | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Из записи**](a-fromentry.md)                                                                      | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**FSMO-Role-Owner**](a-fsmoroleowner.md)                                                             | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Мусор-Coll-период**](a-garbagecollperiod.md)                                                     | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**Квалификатор поколения**](a-generationqualifier.md)                                                  | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Заданное имя**](a-givenname.md)                                                                      | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**хаусеидентифиер**](a-houseidentifier.md)                                                           | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Инициалы**](a-initials.md)                                                                         | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Тип экземпляра**](a-instancetype.md)                                                                | True      | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Международный-ISDN-номер**](a-internationalisdnnumber.md)                                         | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Является критически важным — системный объект**](a-iscriticalsystemobject.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Удалено**](a-isdeleted.md)                                                                      | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Входит в состав списка рассылки**](a-memberof.md)                                                                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Имеет права владельца**](a-isprivilegeholder.md)                                                     | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Является перезапущенным**](a-isrecycled.md)                                                                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**лабеледури**](a-labeleduri.md)                                                                     | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**Последний-известный-родительский**](a-lastknownparent.md)                                                         | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Устаревший — Exchange-DN**](a-legacyexchangedn.md)                                                       | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**Локальное имя**](a-l.md)                                                                           | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Эмблема**](a-thumbnaillogo.md)                                                                        | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Управляемые объекты**](a-managedobjects.md)                                                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Configuration**](a-manager.md)                                                                           | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**В основном**](a-masteredby.md)                                                                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**МХС-или-Address**](a-mhsoraddress.md)                                                               | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Метка времени изменения**](a-modifytimestamp.md)                                                         | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-COM-Партитионсетлинк**](a-mscom-partitionsetlink.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-COM-Усерлинк**](a-mscom-userlink.md)                                                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DFSR-Компутерреференцебл**](a-msdfsr-computerreferencebl.md)                                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DFSR-Мемберреференцебл**](a-msdfsr-memberreferencebl.md)                                        | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Allowed-to-"Active-on-чужое удостоверение"**](a-msds-allowedtoactonbehalfofotheridentity.md) | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**MS-DS-Allowed-to-Delegate-to**](a-msds-allowedtodelegateto.md)                                     | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**MS-DS-примерно-Иммед-подчиненные**](a-msds-approx-immed-subordinates.md)                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Аусентикатедто-Аккаунтлист**](a-msds-authenticatedtoaccountlist.md)                         | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-ClaimSet-shares-возможные значения-with-BL**](a-msds-claimsharespossiblevalueswithbl.md)           | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-целостность-дочерняя — количество**](a-ms-ds-consistencychildcount.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Consistencу-Guid**](a-ms-ds-consistencyguid.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Поддержка MS-DS-Feature-BL**](a-msds-enabledfeaturebl.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-геокоординаты — высота**](a-msds-geocoordinatesaltitude.md)                                 | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**MS-DS-геокоординаты — Широта**](a-msds-geocoordinateslatitude.md)                                 | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**MS-DS-геокоординаты — Долгота**](a-msds-geocoordinateslongitude.md)                               | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**MS-DS-ИЕРАРХИя — старший стаж — индекс**](a-msds-habseniorityindex.md)                                          | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**MS-DS-Host-Service-Account-BL**](a-msds-hostserviceaccountbl.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS--домен — для**](a-msds-isdomainfor.md)                                                      | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-является-Full-реплика для**](a-msds-isfullreplicafor.md)                                           | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-является-partial-реплика для**](a-msds-ispartialreplicafor.md)                                     | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-является-PRIMARY-Computer-для**](a-msds-isprimarycomputerfor.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Last-Known-RDN**](a-msds-lastknownrdn.md)                                                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-локально-эффективное удаление — время**](a-msds-localeffectivedeletiontime.md)                       | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Local-эффективен — время перезапуска**](a-msds-localeffectiverecycletime.md)                         | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Masterd-by**](a-msds-masteredby.md)                                                         | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)                                      | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Members-of-Resource-Property-List-BL**](a-msds-membersofresourcepropertylistbl.md)           | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-NC-REPL-курсоры**](a-msds-ncreplcursors.md)                                                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-NC-REPL-Inbound-соседи**](a-msds-ncreplinboundneighbors.md)                               | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-NC-REPL-Outbound-соседи**](a-msds-ncreploutboundneighbors.md)                             | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)                          | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-NC-Type**](a-msds-nctype.md)                                                                 | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-не-Members-BL**](a-msds-nonmembersbl.md)                                                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Object-Reference-BL**](a-msds-objectreferencebl.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Оидтограуп-Link-BL**](a-msds-oidtogrouplinkbl.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Operations-для-AZ-Role-BL**](a-msds-operationsforazrolebl.md)                                | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)                                | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Фонетическое название компании**](a-msds-phoneticcompanyname.md)                                      | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**MS-DS-фонетический отдел**](a-msds-phoneticdepartment.md)                                         | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**MS-DS-фонетическо-отображаемое имя**](a-msds-phoneticdisplayname.md)                                      | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/> [**Получатель почты**](c-mailrecipient.md)<br/>                |
| [**MS-DS-фонетическо-First-Name**](a-msds-phoneticfirstname.md)                                          | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**MS-DS-фонетическое имя (фамилия)**](a-msds-phoneticlastname.md)                                            | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**MS-DS-Principal-Name**](a-msds-principalname.md)                                                   | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-PSO — применяется**](a-msds-psoapplied.md)                                                         | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-REPL-Attribute-Meta-Data**](a-msds-replattributemetadata.md)                                 | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-выявил-DSA**](a-msds-revealeddsas.md)                                                     | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-выводит-List-BL**](a-msds-revealedlistbl.md)                                                | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Source-Object-DN**](a-msds-sourceobjectdn.md)                                                | Неверно     | **Contact**                                                                                                                            |
| [**MS-DS-Tasks-для-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Tasks-for-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                                          | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-TDO-исходящий трафик — BL**](a-msds-tdoegressbl.md)                                                      | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-TDO-входящий трафик — BL**](a-msds-tdoingressbl.md)                                                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-value-type-Reference-BL**](a-msds-valuetypereferencebl.md)                                   | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**MS-дов-Assistant-Name**](a-msexchassistantname.md)                                                | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**MS-дов-House-identifier**](a-msexchhouseidentifier.md)                                            | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**MS-дов-Лабеледури**](a-msexchlabeleduri.md)                                                       | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**MS-дов-Owner-BL**](a-ownerbl.md)                                                                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Мссфу-30-POSIX-член-of**](a-mssfu30posixmemberof.md)                                             | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**нетбут-SCP-BL**](a-netbootscpbl.md)                                                               | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Не-Security-Member-BL**](a-nonsecuritymemberbl.md)                                                | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**NT-Security-дескриптор**](a-ntsecuritydescriptor.md)                                               | True      | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Obj-расп-имя**](a-distinguishedname.md)                                                           | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Объект — Категория**](a-objectcategory.md)                                                            | True      | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Объектный класс**](a-objectclass.md)                                                                  | True      | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Объект — GUID**](a-objectguid.md)                                                                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Версия объекта**](a-objectversion.md)                                                              | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Организация — имя подразделения**](a-ou.md)                                                               | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Название организации**](a-o.md)                                                                       | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Другие — почтовый ящик**](a-othermailbox.md)                                                                | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Другое имя**](a-middlename.md)                                                                     | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Другие хорошо известные объекты**](a-otherwellknownobjects.md)                                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Разделяемый атрибут-удаление-список**](a-partialattributedeletionlist.md)                              | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Разделяемый атрибут-set**](a-partialattributeset.md)                                                 | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Личный заголовок**](a-personaltitle.md)                                                              | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон — Факс — другие**](a-otherfacsimiletelephonenumber.md)                                             | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон — Главная страница — другие**](a-otherhomephone.md)                                                           | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон — Главная страница**](a-homephone.md)                                                              | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Phone — IP — другие**](a-otheripphone.md)                                                               | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон — IP-адрес — основной**](a-ipphone.md)                                                                  | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон — ISDN — первичный**](a-primaryinternationalisdnnumber.md)                                         | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон — Mobile — другие**](a-othermobile.md)                                                            | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон — Mobile — первичный**](a-mobile.md)                                                               | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон — Office — другие**](a-othertelephone.md)                                                         | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон — пейджер — другие**](a-otherpager.md)                                                              | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Телефон — пейджер — первичный**](a-pager.md)                                                                 | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Физическая доставка — офис — имя**](a-physicaldeliveryofficename.md)                                  | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Picture**](a-thumbnailphoto.md)                                                                    | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Возможно — подстрочные**](a-possibleinferiors.md)                                                      | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Почтовый адрес**](a-postaladdress.md)                                                              | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Почтовый код**](a-postalcode.md)                                                                    | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Пост-Office-Box**](a-postofficebox.md)                                                             | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Предпочтительный метод доставки**](a-preferreddeliverymethod.md)                                         | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Прокси-объект-имя**](a-proxiedobjectname.md)                                                     | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Прокси-адреса**](a-proxyaddresses.md)                                                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Запрос — политика — BL**](a-querypolicybl.md)                                                             | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**RDN**](a-name.md)                                                                                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Зарегистрированный адрес**](a-registeredaddress.md)                                                      | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                                              | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**REPL-Уптодате-Vector**](a-repluptodatevector.md)                                                   | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Отчеты**](a-directreports.md)                                                                     | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Представители — от**](a-repsfrom.md)                                                                        | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Представители — кому**](a-repsto.md)                                                                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Редакции**](a-revision.md)                                                                         | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**SD-Rights-эффективен**](a-sdrightseffective.md)                                                     | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**секретарь**](a-secretary.md)                                                                       | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**См. также**](a-seealso.md)                                                                          | Неверно     | [**Человек**](c-person.md)<br/>                                                                                                  |
| [**Серийный номер**](a-serialnumber.md)                                                                | Неверно     | [**Человек**](c-person.md)<br/>                                                                                                  |
| [**Server-Reference-BL**](a-serverreferencebl.md)                                                     | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Отображение в адресной книге**](a-showinaddressbook.md)                                                    | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**"Показать" — "Расширенный просмотр"**](a-showinadvancedviewonly.md)                                         | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Site-Object-BL**](a-siteobjectbl.md)                                                               | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**State-или-провинция-Name**](a-st.md)                                                                 | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Улица-адрес**](a-street.md)                                                                     | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Структурный объектный класс**](a-structuralobjectclass.md)                                             | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Подразделы-ReFS**](a-subrefs.md)                                                                          | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**субсчемасубентри**](a-subschemasubentry.md)                                                       | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Образование**](a-sn.md)                                                                                | Неверно     | [**Человек**](c-person.md)<br/>                                                                                                  |
| [**Системные флаги**](a-systemflags.md)                                                                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Номер телефона**](a-telephonenumber.md)                                                          | Неверно     | [**Человек**](c-person.md)<br/> [**Получатель почты**](c-mailrecipient.md)<br/>                                             |
| [**Teletex — идентификатор терминала**](a-teletexterminalidentifier.md)                                     | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Номер телекса**](a-telexnumber.md)                                                                  | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Номер телекса (первичный)**](a-primarytelexnumber.md)                                                          | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Текст — страна**](a-co.md)                                                                           | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**С текстовым кодированием или адресом**](a-textencodedoraddress.md)                                              | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**Заголовок**](a-title.md)                                                                               | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**User-CERT**](a-usercert.md)                                                                        | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**Комментарий пользователя**](a-comment.md)                                                                      | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Пароль пользователя**](a-userpassword.md)                                                                | Неверно     | [**Человек**](c-person.md)<br/>                                                                                                  |
| [**Пользователь-SMIME-Certificate**](a-usersmimecertificate.md)                                               | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |
| [**USN-изменено**](a-usnchanged.md)                                                                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Созданный USN**](a-usncreated.md)                                                                    | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**USN-DSA-Last-obj-removed**](a-usndsalastobjremoved.md)                                             | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**USN — межсайтовая**](a-usnintersite.md)                                                                | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                                            | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Источник USN**](a-usnsource.md)                                                                      | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**WBEM — путь**](a-wbempath.md)                                                                        | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**Хорошо известные объекты**](a-wellknownobjects.md)                                                       | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**При изменении**](a-whenchanged.md)                                                                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**При создании**](a-whencreated.md)                                                                  | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**WWW — Главная страница**](a-wwwhomepage.md)                                                                 | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**WWW-Page — другие**](a-url.md)                                                                        | Неверно     | [**Вверх**](c-top.md)<br/>                                                                                                        |
| [**X121 — адрес**](a-x121address.md)                                                                  | Неверно     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**X509 — CERT**](a-usercertificate.md)                                                                 | Неверно     | [**Получатель почты**](c-mailrecipient.md)<br/>                                                                                   |



## <a name="windows-server-2012-property-sets"></a>Наборы свойств Windows Server 2012

Этот класс содержит следующие наборы свойств для Windows Server 2012:



| Общее имя                                            |
|--------------------------------------------------------|
| [**Личные сведения**](r-personal-information.md) |
| [**Веб-информация**](r-web-information.md)           |



 

 





