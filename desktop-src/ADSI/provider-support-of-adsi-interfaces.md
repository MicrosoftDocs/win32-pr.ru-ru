---
title: Поддержка интерфейсов ADSI поставщиком
description: В следующей таблице перечислены краткие описания интерфейсов, поддерживаемых поставщиками, входящими в состав ADSI для Windows 2000 и клиента DS.
ms.assetid: 8eb9a88c-cf18-4fe4-b256-1d6fcaf96c62
ms.tgt_platform: multiple
keywords:
- Поддержка поставщика интерфейсов ADSI ADSI
- ADSI ADSI, поставщики услуг, интерфейсы, поддерживаемые каждым поставщиком
- Поддержка поставщика для IADsUser
- Поддержка поставщика для Иадскомпутер
- Поддержка поставщика для Иадскомпутероператионс
- Поддержка поставщика для Иадсдомаин
- Поддержка поставщика для Иадсфилесервице
- Поддержка поставщика для Иадсграуп
- Поддержка поставщика для Иадскласс
- Поддержка поставщика для Иадспроперти
- Поддержка поставщика для Иадссинтакс
- Поддержка поставщика для Иадсконтаинер
- Поддержка поставщика для Иадснамеспацес
- Поддержка поставщика для Иадсакцессконтролентри
- Поддержка поставщика для Иадсакцессконтроллист
- Поддержка поставщика для Иадссекуритидескриптор
- Поддержка поставщика для Иадсобжектоптионс
- Поддержка поставщика для Иадсколлектион
- Поддержка поставщика для Иадсмемберс
- Поддержка поставщика для Иадспаснаме
- Поддержка поставщика для Иадспринткуеуе
- Поддержка поставщика для Иадспринткуеуеоператионс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf12803929d96a61aac6603be2c528084c91693c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328392"
---
# <a name="provider-support-of-adsi-interfaces"></a>Поддержка интерфейсов ADSI поставщиком

В следующей таблице перечислены краткие описания интерфейсов, поддерживаемых поставщиками, входящими в состав ADSI для Windows 2000 и клиента DS. Запись, помеченная "Yes", указывает, что по крайней мере один объект ADSI указанного поставщика поддерживает связанный интерфейс. "Нет" означает, что ни один объект поставщика не поддерживает интерфейс в этом выпуске. В будущем в настоящее время неподдерживаемые интерфейсы могут поддерживаться предоставляемыми системой поставщиками.

Дополнительные сведения о реализации, относящейся к поставщику ADSI, см. в следующих статьях:

-   [Поставщик LDAP ADSI](adsi-ldap-provider.md)
-   [Поставщик ADSI WinNT](adsi-winnt-provider.md)
-   [МАРШРУТИЗАТОР ADSI](adsi-router.md)

Чтобы получить дополнительные сведения о том, какое свойство или метод поддерживается для каждого интерфейса, щелкните имя соответствующего интерфейса в первом столбце таблицы.



| Имя_интерфейса                                                 | LDAP | WinNT |
|----------------------------------------------------------------|------|-------|
| [**IADs**](/windows/desktop/api/Iads/nn-iads-iads)                                           | Да  | Да   |
| [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)       | Да  | Нет    |
| [**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)         | Да  | Нет    |
| [**IADsAcl**](/windows/desktop/api/Iads/nn-iads-iadsacl)                                     | Нет   | Нет    |
| [**IADsBackLink**](/windows/desktop/api/Iads/nn-iads-iadsbacklink)                           | Нет   | Нет    |
| [**IADsCaseIgnoreList**](/windows/desktop/api/Iads/nn-iads-iadscaseignorelist)               | Нет   | Нет    |
| [**иадскласс**](/windows/desktop/api/Iads/nn-iads-iadsclass)                                 | Да  | Да   |
| [**иадсколлектион**](/windows/desktop/api/Iads/nn-iads-iadscollection)                       | Нет   | Да   |
| [**иадскомпутер**](/windows/desktop/api/Iads/nn-iads-iadscomputer)                           | Нет   | Да   |
| [**иадскомпутероператионс**](/windows/desktop/api/Iads/nn-iads-iadscomputeroperations)       | Нет   | Да   |
| [**иадсконтаинер**](/windows/desktop/api/Iads/nn-iads-iadscontainer)                         | Да  | Да   |
| [**иадсделетеопс**](/windows/desktop/api/Iads/nn-iads-iadsdeleteops)                         | Да  | Нет    |
| [**иадсдомаин**](/windows/desktop/api/Iads/nn-iads-iadsdomain)                               | Нет   | Да   |
| [**IADsEmail**](/windows/desktop/api/Iads/nn-iads-iadsemail)                                 | Нет   | Нет    |
| [**иадсекстенсион**](/windows/desktop/api/Iads/nn-iads-iadsextension)                         | Да  | Да   |
| [**IADsFaxNumber**](/windows/desktop/api/Iads/nn-iads-iadsfaxnumber)                         | Нет   | Нет    |
| [**иадсфилесервице**](/windows/desktop/api/Iads/nn-iads-iadsfileservice)                     | Нет   | Да   |
| [**иадсфилесервицеоператионс**](/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations) | Нет   | Да   |
| [**иадсфилешаре**](/windows/desktop/api/Iads/nn-iads-iadsfileshare)                         | Нет   | Да   |
| [**иадсграуп**](/windows/desktop/api/Iads/nn-iads-iadsgroup)                                 | Да  | Да   |
| [**IADsHold**](/windows/desktop/api/Iads/nn-iads-iadshold)                                   | Нет   | Нет    |
| [**IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger)                   | Да  | Нет    |
| [**иадслокалити**](/windows/desktop/api/Iads/nn-iads-iadslocality)                           | Да  | Нет    |
| [**иадсмемберс**](/windows/desktop/api/Iads/nn-iads-iadsmembers)                             | Да  | Да   |
| [**иадснамеспацес**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces)                       | Да  | Да   |
| [**IADsNetAddress**](/windows/desktop/api/Iads/nn-iads-iadsnetaddress)                       | Нет   | Нет    |
| [**иадсо**](/windows/desktop/api/Iads/nn-iads-iadso)                                         | Да  | Нет    |
| [**IADsObjectOptions**](/windows/desktop/api/Iads/nn-iads-iadsobjectoptions)                 | Да  | Нет    |
| [**IADsOctetList**](/windows/desktop/api/Iads/nn-iads-iadsoctetlist)                         | Нет   | Нет    |
| [**иадсопендсобжект**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject)                   | Да  | Да   |
| [**иадсау**](/windows/desktop/api/Iads/nn-iads-iadsou)                                       | Да  | Нет    |
| [**IADsPath**](/windows/desktop/api/Iads/nn-iads-iadspath)                                   | Нет   | Нет    |
| [**иадспаснаме**](/windows/desktop/api/Iads/nn-iads-iadspathname)                           | Да  | Да   |
| [**IADsPostalAddress**](/windows/desktop/api/Iads/nn-iads-iadspostaladdress)                 | Нет   | Нет    |
| [**иадспринтжоб**](/windows/desktop/api/Iads/nn-iads-iadsprintjob)                           | Нет   | Да   |
| [**иадспринтжобоператионс**](/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations)       | Нет   | Да   |
| [**иадспринткуеуе**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)                       | Да  | Да   |
| [**иадспринткуеуеоператионс**](/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations)   | Да  | Да   |
| [**иадспроперти**](/windows/desktop/api/Iads/nn-iads-iadsproperty)                           | Да  | Да   |
| [**иадспропертентри**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry)                 | Да  | Да   |
| [**иадспропертилист**](/windows/desktop/api/Iads/nn-iads-iadspropertylist)                   | Да  | Да   |
| [**иадспропертивалуе**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue)                 | Да  | Да   |
| [**IADsPropertyValue2**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue2)               | Да  | Да   |
| [**IADsReplicaPointer**](/windows/desktop/api/Iads/nn-iads-iadsreplicapointer)               | Нет   | Нет    |
| [**иадсресаурце**](/windows/desktop/api/Iads/nn-iads-iadsresource)                           | Нет   | Да   |
| [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)       | Да  | Нет    |
| [**иадссервице**](/windows/desktop/api/Iads/nn-iads-iadsservice)                             | Нет   | Да   |
| [**иадссервицеоператионс**](/windows/desktop/api/Iads/nn-iads-iadsserviceoperations)         | Нет   | Да   |
| [**иадссессион**](/windows/desktop/api/Iads/nn-iads-iadssession)                             | Нет   | Да   |
| [**иадссинтакс**](/windows/desktop/api/Iads/nn-iads-iadssyntax)                               | Да  | Да   |
| [**IADsTimestamp**](/windows/desktop/api/Iads/nn-iads-iadstimestamp)                         | Нет   | Нет    |
| [**IADsTypedName**](/windows/desktop/api/Iads/nn-iads-iadstypedname)                         | Нет   | Нет    |
| [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser)                                   | Да  | Да   |
| [**идиректорйобжект**](/windows/desktop/api/Iads/nn-iads-idirectoryobject)                   | Да  | Нет    |
| [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)                   | Да  | Нет    |



 

## <a name="provider-support-for-iadsuser"></a>Поддержка поставщика для IADsUser



| Свойство                                                    | LDAP          | WinNT         |
|-------------------------------------------------------------|---------------|---------------|
| [**аккаунтдисаблед**](iadsuser-property-methods.md)        | Поддерживается     | Поддерживается     |
| [**аккаунтекспиратиондате**](iadsuser-property-methods.md)  | Поддерживается     | Поддерживается     |
| [**бадлогинаддресс**](iadsuser-property-methods.md)        | Не поддерживается   | Не поддерживается |
| [**бадлогинкаунт**](iadsuser-property-methods.md)          | Поддерживается     | Поддерживается     |
| [**Название**](iadsuser-property-methods.md)             | Поддерживается     | Не поддерживается   |
| [**Описание**](iadsuser-property-methods.md)            | Поддерживается     | Поддерживается     |
| [**Отдел**](iadsuser-property-methods.md)               | Поддерживается     | Не поддерживается   |
| [**EmailAddress**](iadsuser-property-methods.md)           | Поддерживается     | Не поддерживается   |
| [**КодСотрудника**](iadsuser-property-methods.md)             | Поддерживается     | Не поддерживается   |
| [**факснумбер**](iadsuser-property-methods.md)              | Поддерживается     | Не поддерживается   |
| [**FirstName**](iadsuser-property-methods.md)              | Поддерживается     | Не поддерживается   |
| [**FullName**](iadsuser-property-methods.md)               | Поддерживается     | Поддерживается     |
| [**грацелогинсалловед**](iadsuser-property-methods.md)     | Не поддерживается | Не поддерживается   |
| [**грацелогинсремаининг**](iadsuser-property-methods.md)   | Не поддерживается | Не поддерживается   |
| [**HomeDirectory**](iadsuser-property-methods.md)          | Поддерживается     | Поддерживается     |
| [**Домашней**](iadsuser-property-methods.md)               | Поддерживается     | Не поддерживается   |
| [**исаккаунтлоккед**](iadsuser-property-methods.md)        | Поддерживается     | Поддерживается     |
| [**Языки**](iadsuser-property-methods.md)              | Не поддерживается | Не поддерживается   |
| [**ластфаиледлогин**](iadsuser-property-methods.md)        | Поддерживается     | Не поддерживается   |
| [**LastLogin**](iadsuser-property-methods.md)              | Поддерживается     | Поддерживается     |
| [**ластлогофф**](iadsuser-property-methods.md)             | Поддерживается     | Поддерживается     |
| [**LastName**](iadsuser-property-methods.md)               | Поддерживается     | Не поддерживается   |
| [**логинхаурс**](iadsuser-property-methods.md)             | Поддерживается     | Поддерживается     |
| [**логинскрипт**](iadsuser-property-methods.md)            | Поддерживается     | Поддерживается     |
| [**логинворкстатионс**](iadsuser-property-methods.md)      | Поддерживается     | Поддерживается     |
| [**Configuration**](iadsuser-property-methods.md)                | Поддерживается     | Не поддерживается   |
| [**макслогинс**](iadsuser-property-methods.md)              | Не поддерживается   | Не поддерживается   |
| [**максстораже**](iadsuser-property-methods.md)             | Поддерживается     | Поддерживается     |
| [**NamePrefix**](iadsuser-property-methods.md)             | Поддерживается     | Не поддерживается   |
| [**NameSuffix**](iadsuser-property-methods.md)             | Поддерживается     | Не поддерживается   |
| [**оффицелокатионс**](iadsuser-property-methods.md)        | Поддерживается     | Не поддерживается   |
| [**осернаме**](iadsuser-property-methods.md)              | Поддерживается     | Не поддерживается   |
| [**пассвордекспиратиондате**](iadsuser-property-methods.md) | Не поддерживается   | Поддерживается     |
| [**пассвордластчанжед**](iadsuser-property-methods.md)    | Поддерживается     | Не поддерживается   |
| [**пассвордминимумленгс**](iadsuser-property-methods.md)  | Не поддерживается   | Поддерживается     |
| [**пассвордрекуиред**](iadsuser-property-methods.md)       | Поддерживается     | Поддерживается     |
| [**Picture**](iadsuser-property-methods.md)                | Поддерживается     | Не поддерживается   |
| [**посталаддрессес**](iadsuser-property-methods.md)        | Поддерживается     | Не поддерживается   |
| [**посталкодес**](iadsuser-property-methods.md)            | Поддерживается     | Не поддерживается   |
| [**Профиль**](iadsuser-property-methods.md)                | Поддерживается     | Поддерживается     |
| [**рекуиреуникуепассворд**](iadsuser-property-methods.md)  | Не поддерживается   | Не поддерживается   |
| [**SeeAlso**](iadsuser-property-methods.md)                | Поддерживается     | Не поддерживается   |
| [**телефонехоме**](iadsuser-property-methods.md)          | Поддерживается     | Не поддерживается   |
| [**телефонемобиле**](iadsuser-property-methods.md)        | Поддерживается     | Не поддерживается   |
| [**TelephoneNumber**](iadsuser-property-methods.md)        | Поддерживается     | Не поддерживается   |
| [**телефонепажер**](iadsuser-property-methods.md)         | Поддерживается     | Не поддерживается   |
| [**Заголовок**](iadsuser-property-methods.md)                  | Поддерживается     | Не поддерживается   |



 

## <a name="provider-support-for-iadscomputer"></a>Поддержка поставщика для Иадскомпутер



| Свойства                                     | LDAP                    | WinNT       |
|------------------------------------------------|-------------------------|-------------|
| [**компутерид**](/windows/desktop/api/Iads/nn-iads-iadscomputer)             | Интерфейс не поддерживается | Не поддерживается |
| [**Название**](/windows/desktop/api/Iads/nn-iads-iadscomputer)             | Интерфейс не поддерживается | Не поддерживается |
| [**Описание**](/windows/desktop/api/Iads/nn-iads-iadscomputer)            | Интерфейс не поддерживается | Не поддерживается |
| [**Отдел**](/windows/desktop/api/Iads/nn-iads-iadscomputer)               | Интерфейс не поддерживается | Поддерживается   |
| [**Расположение**](/windows/desktop/api/Iads/nn-iads-iadscomputer)               | Интерфейс не поддерживается | Не поддерживается |
| [**MemorySize**](/windows/desktop/api/Iads/nn-iads-iadscomputer)             | Интерфейс не поддерживается | Не поддерживается |
| [**Моделировать**](/windows/desktop/api/Iads/nn-iads-iadscomputer)                  | Интерфейс не поддерживается | Не поддерживается |
| [**нетаддрессес**](/windows/desktop/api/Iads/nn-iads-iadscomputer)           | Интерфейс не поддерживается | Не поддерживается |
| [**OperatingSystem**](/windows/desktop/api/Iads/nn-iads-iadscomputer)        | Интерфейс не поддерживается | Поддерживается   |
| [**оператингсистемверсион**](/windows/desktop/api/Iads/nn-iads-iadscomputer) | Интерфейс не поддерживается | Поддерживается   |
| [**Владелец**](/windows/desktop/api/Iads/nn-iads-iadscomputer)                  | Интерфейс не поддерживается | Поддерживается   |
| [**PrimaryUser**](/windows/desktop/api/Iads/nn-iads-iadscomputer)            | Интерфейс не поддерживается | Не поддерживается |
| [**Процессор**](/windows/desktop/api/Iads/nn-iads-iadscomputer)              | Интерфейс не поддерживается | Поддерживается   |
| [**ProcessorCount**](/windows/desktop/api/Iads/nn-iads-iadscomputer)         | Интерфейс не поддерживается | Поддерживается   |
| [**Role**](/windows/desktop/api/Iads/nn-iads-iadscomputer)                   | Интерфейс не поддерживается | Не поддерживается |
| [**Сайт**](/windows/desktop/api/Iads/nn-iads-iadscomputer)                   | Интерфейс не поддерживается | Не поддерживается |
| [**сторажекапаЦити**](/windows/desktop/api/Iads/nn-iads-iadscomputer)        | Интерфейс не поддерживается | Не поддерживается |



 

## <a name="provider-support-for-iadscomputeroperations"></a>Поддержка поставщика для Иадскомпутероператионс



| Свойство                                   | LDAP                    | WinNT           |
|--------------------------------------------|-------------------------|-----------------|
| [**Закрытия**](/windows/desktop/api/Iads/nn-iads-iadscomputeroperations) | Интерфейс не поддерживается | Не реализовано |
| [**Состояние**](/windows/desktop/api/Iads/nn-iads-iadscomputeroperations)   | Интерфейс не поддерживается | Не реализовано |



 

## <a name="provider-support-for-iadsdomain"></a>Поддержка поставщика для Иадсдомаин



| Свойство                                         | LDAP                    | WinNT           |
|--------------------------------------------------|-------------------------|-----------------|
| [**Рабочая группа**](/windows/desktop/api/Iads/nn-iads-iadsdomain)                | Интерфейс не поддерживается | Не реализовано |
| [**минпассвордленгс**](/windows/desktop/api/Iads/nn-iads-iadsdomain)          | Интерфейс не поддерживается | Поддерживается       |
| [**минпассвордаже**](/windows/desktop/api/Iads/nn-iads-iadsdomain)             | Интерфейс не поддерживается | Поддерживается       |
| [**макспассвордаже**](/windows/desktop/api/Iads/nn-iads-iadsdomain)             | Интерфейс не поддерживается | Поддерживается       |
| [**максбадпассвордсалловед**](/windows/desktop/api/Iads/nn-iads-iadsdomain)     | Интерфейс не поддерживается | Поддерживается       |
| [**пассвордхисториленгс**](/windows/desktop/api/Iads/nn-iads-iadsdomain)      | Интерфейс не поддерживается | Поддерживается       |
| [**пассвордаттрибутес**](/windows/desktop/api/Iads/nn-iads-iadsdomain)         | Интерфейс не поддерживается | Не поддерживается     |
| [**аутаунлоккинтервал**](/windows/desktop/api/Iads/nn-iads-iadsdomain)         | Интерфейс не поддерживается | Поддерживается       |
| [**локкаутобсерватионинтервал**](/windows/desktop/api/Iads/nn-iads-iadsdomain) | Интерфейс не поддерживается | Поддерживается       |



 

## <a name="provider-support-for-iadsfileservice"></a>Поддержка поставщика для Иадсфилесервице



| Свойство                                | LDAP                    | WinNT     |
|-----------------------------------------|-------------------------|-----------|
| [**Описание**](/windows/desktop/api/Iads/nn-iads-iadsfileservice)  | Интерфейс не поддерживается | Поддерживается |
| [**максусеркаунт**](/windows/desktop/api/Iads/nn-iads-iadsfileservice) | Интерфейс не поддерживается | Поддерживается |



 

## <a name="provider-support-for-iadsgroup"></a>Поддержка поставщика для Иадсграуп



| Свойство                         | LDAP      | WinNT     |
|----------------------------------|-----------|-----------|
| [**Описание**](/windows/desktop/api/Iads/nn-iads-iadsgroup) | Поддерживается | Поддерживается |



 

## <a name="provider-support-for-iadsclass"></a>Поддержка поставщика для Иадскласс



| Свойство                                   | LDAP               | WinNT           |
|--------------------------------------------|--------------------|-----------------|
| [**примаринтерфаце**](/windows/desktop/api/Iads/nn-iads-iadsclass)      | Поддерживается          | Поддерживается       |
| [**ЭТОМУ**](/windows/desktop/api/Iads/nn-iads-iadsclass)                 | Поддерживается          | Поддерживается       |
| [**КОДА**](/windows/desktop/api/Iads/nn-iads-iadsclass)                   | Поддерживается          | Поддерживается       |
| [**Выделяет**](/windows/desktop/api/Iads/nn-iads-iadsclass)              | Поддерживается          | Поддерживается       |
| [**Четки**](/windows/desktop/api/Iads/nn-iads-iadsclass)             | Поддерживается          | Поддерживается       |
| [**мандаторипропертиес**](/windows/desktop/api/Iads/nn-iads-iadsclass)   | Поддерживается          | Поддерживается       |
| [**OptionalProperties**](/windows/desktop/api/Iads/nn-iads-iadsclass)    | Поддерживается          | Поддерживается       |
| [**намингпропертиес**](/windows/desktop/api/Iads/nn-iads-iadsclass)      | Поддерживается          | Не реализовано |
| [**дериведфром**](/windows/desktop/api/Iads/nn-iads-iadsclass)           | Поддерживается          | Не поддерживается     |
| [**ауксдериведфром**](/windows/desktop/api/Iads/nn-iads-iadsclass)        | Поддерживается          | Не поддерживается     |
| [**поссиблесупериорс**](/windows/desktop/api/Iads/nn-iads-iadsclass)     | Поддерживается          | Поддерживается       |
| [**Containment**](/windows/desktop/api/Iads/nn-iads-iadsclass)           | Поддерживается для чтения | Поддерживается       |
| [**Контейнер**](/windows/desktop/api/Iads/nn-iads-iadsclass)             | Поддерживается для чтения | Поддерживается       |
| [**хелпфиленаме**](/windows/desktop/api/Iads/nn-iads-iadsclass)          | Поддерживается          | Поддерживается       |
| [**хелпфилеконтекст**](/windows/desktop/api/Iads/nn-iads-iadsclass)       | Поддерживается          | Поддерживается       |
| Метод                                     | LDAP               | WinNT           |
| [**Квалификаторы**](/windows/desktop/api/Iads/nf-iads-iadsclass-qualifiers) | Не реализовано    | Не реализовано |



 

## <a name="provider-support-for-iadsproperty"></a>Поддержка поставщика для Иадспроперти



| Свойство                            | LDAP      | WinNT     |
|-------------------------------------|-----------|-----------|
| [**КОДА**](/windows/desktop/api/Iads/nn-iads-iadsproperty)         | Поддерживается | Поддерживается |
| [**Синтаксис**](/windows/desktop/api/Iads/nn-iads-iadsproperty)      | Поддерживается | Поддерживается |
| [**максранже**](/windows/desktop/api/Iads/nn-iads-iadsproperty)    | Поддерживается | Поддерживается |
| [**минранже**](/windows/desktop/api/Iads/nn-iads-iadsproperty)    | Поддерживается | Поддерживается |
| [**Многозначных**](/windows/desktop/api/Iads/nn-iads-iadsproperty) | Поддерживается | Поддерживается |



 

## <a name="provider-support-for-iadssyntax"></a>Поддержка поставщика для Иадссинтакс



| Свойство                              | LDAP      | WinNT     |
|---------------------------------------|-----------|-----------|
| [**олеаутодататипе**](/windows/desktop/api/Iads/nn-iads-iadssyntax) | Поддерживается | Поддерживается |



 

## <a name="provider-support-for-iadscontainer"></a>Поддержка поставщика для Иадсконтаинер



| Свойство                        | LDAP            | WinNT           |
|---------------------------------|-----------------|-----------------|
| [**Расчета**](/windows/desktop/api/Iads/nn-iads-iadscontainer)  | Не реализовано | Не реализовано |
| [**Указания**](/windows/desktop/api/Iads/nn-iads-iadscontainer)  | Поддерживается       | Не реализовано |
| [**Фильтр**](/windows/desktop/api/Iads/nn-iads-iadscontainer) | Поддерживается       | Поддерживается       |



 

## <a name="provider-support-for-iadsnamespaces"></a>Поддержка поставщика для Иадснамеспацес



| Свойство                                   | LDAP      | WinNT     |
|--------------------------------------------|-----------|-----------|
| [**дефаултконтаинер**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces) | Поддерживается | Поддерживается |



 

## <a name="provider-support-for-iadsaccesscontrolentry"></a>Поддержка поставщика для Иадсакцессконтролентри



| Свойство                                              | LDAP      | WinNT       |
|-------------------------------------------------------|-----------|-------------|
| [**AccessMask**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)          | Поддерживается | Не поддерживается |
| [**акцесстипе**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)          | Поддерживается | Не поддерживается |
| [**AccessFlags**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)         | Поддерживается | Не поддерживается |
| [**Метки**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)               | Поддерживается | Не поддерживается |
| [**ObjectType**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)          | Поддерживается | Не поддерживается |
| [**инхеритедобжекттипе**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) | Поддерживается | Не поддерживается |
| [**Доверенное лицо**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)             | Поддерживается | Не поддерживается |



 

## <a name="provider-support-for-iadsaccesscontrollist"></a>Поддержка поставщика для Иадсакцессконтроллист



| Свойство                                                       | LDAP      | WinNT       |
|----------------------------------------------------------------|-----------|-------------|
| [**ацекаунт**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)                      | Поддерживается | Не поддерживается |
| [**ацеревисион**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)                   | Поддерживается | Не поддерживается |
| Метод                                                         | LDAP      | WinNT       |
| [**аддаце**](/windows/desktop/api/Iads/nf-iads-iadsaccesscontrollist-addace)                 | Поддерживается | Не поддерживается |
| [**копякцесслист**](/windows/desktop/api/Iads/nf-iads-iadsaccesscontrollist-copyaccesslist) | Поддерживается | Не поддерживается |
| [**ремовеаце**](/windows/desktop/api/Iads/nf-iads-iadsaccesscontrollist-removeace)           | Поддерживается | Не поддерживается |
| [**получить \_ \_ NewEnum**](/windows/desktop/api/Iads/nf-iads-iadsaccesscontrollist-get__newenum)   | Поддерживается | Не поддерживается |



 

## <a name="provider-support-for-iadssecuritydescriptor"></a>Поддержка поставщика для Иадссекуритидескриптор



| Свойство                                                                        | LDAP      | WinNT       |
|---------------------------------------------------------------------------------|-----------|-------------|
| [**Элемента**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                                       | Поддерживается | Не поддерживается |
| [**даклдефаултед**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                                 | Поддерживается | Не поддерживается |
| [**дискретионарякл**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                              | Поддерживается | Не поддерживается |
| [**Группа**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                                         | Поддерживается | Не поддерживается |
| [**граупдефаултед**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                                | Поддерживается | Не поддерживается |
| [**Владелец**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                                         | Поддерживается | Не поддерживается |
| [**овнердефаултед**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                                | Поддерживается | Не поддерживается |
| [**саклдефаултед**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                                 | Поддерживается | Не поддерживается |
| [**системакл**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                                     | Поддерживается | Не поддерживается |
| Метод                                                                          | LDAP      | WinNT       |
| [**кописекуритидескриптор**](/windows/desktop/api/Iads/nf-iads-iadssecuritydescriptor-copysecuritydescriptor) | Поддерживается | Не поддерживается |



 

## <a name="provider-support-for-iadsobjectoptions"></a>Поддержка поставщика для Иадсобжектоптионс



| Метод                                           | LDAP      | WinNT                   |
|--------------------------------------------------|-----------|-------------------------|
| [**GetOption**](/windows/desktop/api/Iads/nf-iads-iadsobjectoptions-getoption) | Поддерживается | Интерфейс не поддерживается |
| [**SetOption**](/windows/desktop/api/Iads/nf-iads-iadsobjectoptions-setoption) | Поддерживается | Интерфейс не поддерживается |



 

## <a name="provider-support-for-iadscollection"></a>Поддержка поставщика для Иадсколлектион



| Метод                                                | LDAP                    | WinNT       |
|-------------------------------------------------------|-------------------------|-------------|
| [**Добавить**](/windows/desktop/api/Iads/nf-iads-iadscollection-add)                     | Интерфейс не поддерживается | Не поддерживается |
| [**получить \_ \_ NewEnum**](/windows/desktop/api/Iads/nf-iads-iadscollection-get__newenum) | Интерфейс не поддерживается | Поддерживается   |
| [**GetObject**](/windows/desktop/api/Iads/nf-iads-iadscollection-getobject)         | Интерфейс не поддерживается | Поддерживается   |
| [**Отменит**](/windows/desktop/api/Iads/nf-iads-iadscollection-remove)               | Интерфейс не поддерживается | Поддерживается   |



 

## <a name="provider-support-for-iadsmembers"></a>Поддержка поставщика для Иадсмемберс



| Свойство                                           | LDAP                                                      | WinNT       |
|----------------------------------------------------|-----------------------------------------------------------|-------------|
| [**Расчета**](/windows/desktop/api/Iads/nn-iads-iadsmembers)                       | Поддерживается для GroupCollection, но не для Усерколлектион | Не поддерживается |
| [**Фильтр**](/windows/desktop/api/Iads/nn-iads-iadsmembers)                      | Поддерживается                                                 | Поддерживается   |
| Метод                                             | LDAP                                                      | WinNT       |
| [**получить \_ \_ NewEnum**](/windows/desktop/api/Iads/nf-iads-iadsmembers-get__newenum) | Поддерживается                                                 | Поддерживается   |



 

## <a name="provider-support-for-iadspathname"></a>Поддержка поставщика для Иадспаснаме



| Свойство                                                    | LDAP      | WinNT       |
|-------------------------------------------------------------|-----------|-------------|
| [**ескапедмоде**](/windows/desktop/api/Iads/nn-iads-iadspathname)                         | Поддерживается | Поддерживается   |
| Метод                                                      | LDAP      | WinNT       |
| [**Параметр**](/windows/desktop/api/Iads/nf-iads-iadspathname-set)                             | Поддерживается | Поддерживается   |
| [**сетдисплайтипе**](/windows/desktop/api/Iads/nf-iads-iadspathname-setdisplaytype)       | Поддерживается | Поддерживается   |
| [**Получение**](/windows/desktop/api/Iads/nf-iads-iadspathname-retrieve)                   | Поддерживается | Поддерживается   |
| [**жетнумелементс**](/windows/desktop/api/Iads/nf-iads-iadspathname-getnumelements)       | Поддерживается | Поддерживается   |
| [**GetElement**](/windows/desktop/api/Iads/nf-iads-iadspathname-getelement)               | Поддерживается | Поддерживается   |
| [**жетескапеделемент**](/windows/desktop/api/Iads/nf-iads-iadspathname-getescapedelement) | Поддерживается | Не поддерживается |
| [**ремовелеафелемент**](/windows/desktop/api/Iads/nf-iads-iadspathname-removeleafelement) | Поддерживается | Поддерживается   |
| [**копипас**](/windows/desktop/api/Iads/nf-iads-iadspathname-copypath)                   | Поддерживается | Поддерживается   |



 

## <a name="provider-support-for-iadsprintqueue"></a>Поддержка поставщика для Иадспринткуеуе



| Свойство                                     | LDAP        | WinNT       |
|----------------------------------------------|-------------|-------------|
| [**принтерпас**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)        | Поддерживается   | Не поддерживается |
| [**Моделировать**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)              | Поддерживается   | Поддерживается.  |
| [**Заданий**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)           | Не поддерживается | Поддерживается   |
| [**принтпроцессор**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)     | Не поддерживается | Поддерживается   |
| [**Описание**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)        | Поддерживается   | Поддерживается   |
| [**Расположение**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)           | Поддерживается   | Поддерживается   |
| [**StartTime**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)          | Поддерживается   | Поддерживается   |
| [**унтилтиме**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)          | Поддерживается   | Поддерживается   |
| [**дефаултжобприорити**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue) | Не поддерживается | Поддерживается   |
| [**Priority**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)           | Поддерживается   | Поддерживается   |
| [**баннерпаже**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)         | Поддерживается   | Поддерживается   |
| [**принтдевицес**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)       | Поддерживается   | Поддерживается   |
| [**нетаддрессес**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)       | Не поддерживается | Не поддерживается |



 

## <a name="provider-support-for-iadsprintqueueoperations"></a>Поддержка поставщика для Иадспринткуеуеоператионс



| Свойство                                                | LDAP      | WinNT      |
|---------------------------------------------------------|-----------|------------|
| [**Состояние**](/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations)              | Поддерживается | Поддерживается  |
| Метод                                                  | LDAP      | WinNT      |
| [**Пауза**](/windows/desktop/api/Iads/nf-iads-iadsprintqueueoperations-pause)         | Поддерживается | Поддерживается. |
| [**PrintJobs**](/windows/desktop/api/Iads/nf-iads-iadsprintqueueoperations-printjobs) | Поддерживается | Поддерживается  |
| [**Purge**](/windows/desktop/api/Iads/nf-iads-iadsprintqueueoperations-purge)         | Поддерживается | Поддерживается  |
| [**Возобновить**](/windows/desktop/api/Iads/nf-iads-iadsprintqueueoperations-resume)       | Поддерживается | Поддерживается  |



 

 

 




