---
title: Объектная модель ADSI для поставщиков LDAP
description: Иллюстрация, показывающая объекты ADSI, используемые поставщиком LDAP и интерфейсами, используемыми для доступа к этим объектам.
ms.assetid: 109fd42e-201e-4b84-a213-2695d81f005b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06ee06c6bbcfc96a84cc3e7f679d7a13988a78b2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986125"
---
# <a name="adsi-object-model-for-ldap-providers"></a>Объектная модель ADSI для поставщиков LDAP

На следующем рисунке показаны объекты ADSI, используемые поставщиком LDAP и интерфейсами, используемыми для доступа к этим объектам.

![Объектная модель для поставщика LDAP](images/adsiobjmodldap-gif-1.png)

| Объект                        | Интерфейс                                                                                                                                                                                                                                                                                      |
|-------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Класс<br/>              | [**IAds**](/windows/desktop/api/Iads/nn-iads-iads), [ **иадскласс**](/windows/desktop/api/Iads/nn-iads-iadsclass)                                                                                                                                                                                                                                           |
| Свойство<br/>           | [**IAds**](/windows/desktop/api/Iads/nn-iads-iads), [ **иадспроперти**](/windows/desktop/api/Iads/nn-iads-iadsproperty)                                                                                                                                                                                                                                     |
| женобжект<br/>          | [**IAds**](/windows/desktop/api/Iads/nn-iads-iads), [**иадсконтаинер**](/windows/desktop/api/Iads/nn-iads-iadscontainer), [**иадсделетеопс**](/windows/desktop/api/Iads/nn-iads-iadsdeleteops), [**иадсобжектоптионс**](/windows/desktop/api/Iads/nn-iads-iadsobjectoptions), [**иадспропертилист**](/windows/desktop/api/Iads/nn-iads-iadspropertylist), [**идиректорйобжект**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject), [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) |
| Пространство имен<br/>          | [**IAds**](/windows/desktop/api/Iads/nn-iads-iads), [**иадсконтаинер**](/windows/desktop/api/Iads/nn-iads-iadscontainer), [**иадсопендсобжект**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject)                                                                                                                                                                                     |
| RootDSE<br/>            | [**IAds**](/windows/desktop/api/Iads/nn-iads-iads), [ **иадспропертилист**](/windows/desktop/api/Iads/nn-iads-iadspropertylist)                                                                                                                                                                                                                             |
| Контура<br/>           | [**IAds**](/windows/desktop/api/Iads/nn-iads-iads), [ **иадспаснаме**](/windows/desktop/api/Iads/nn-iads-iadspathname)                                                                                                                                                                                                                                     |
| схема<br/>             | [**IAds**](/windows/desktop/api/Iads/nn-iads-iads), [ **иадсконтаинер**](/windows/desktop/api/Iads/nn-iads-iadscontainer)                                                                                                                                                                                                                                   |
| Синтаксис<br/>             | [**IAds**](/windows/desktop/api/Iads/nn-iads-iads), [ **иадссинтакс**](/windows/desktop/api/Iads/nn-iads-iadssyntax)                                                                                                                                                                                                                                         |
| План<br/>       | [**иадсо**](/windows/desktop/api/Iads/nn-iads-iadso)                                                                                                                                                                                                                                                                         |
| OrganizationalUnit<br/> | [**иадсау**](/windows/desktop/api/Iads/nn-iads-iadsou)                                                                                                                                                                                                                                                                       |
| GroupCollection<br/>    | [**иадсмемберс**](/windows/desktop/api/Iads/nn-iads-iadsmembers)                                                                                                                                                                                                                                                             |
| Группа<br/>              | [**иадсграуп**](/windows/desktop/api/Iads/nn-iads-iadsgroup)                                                                                                                                                                                                                                                                 |
| усерколлектион<br/>     | [**иадсмемберс**](/windows/desktop/api/Iads/nn-iads-iadsmembers)                                                                                                                                                                                                                                                             |
| Пользователь<br/>               | [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser)                                                                                                                                                                                                                                                                   |
| Местонахождение<br/>           | [**иадслокалити**](/windows/desktop/api/Iads/nn-iads-iadslocality)                                                                                                                                                                                                                                                           |
| наметранслате<br/>      | [**IADsNameTranslate**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate)                                                                                                                                                                                                                                                 |
| PrintQueue<br/>         | [**Иадспринткуеуе**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue), [ **иадспринткуеуеоператионс**](/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations)                                                                                                                                                                                         |



 

 

 





